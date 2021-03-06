---
ms.date: 10/17/2018
description: 在 Excel 中使用 JavaScript 创建自定义函数。
title: 在 Excel 中创建自定义函数（预览）
ms.openlocfilehash: 8383b5f6d568a1ce2da036fbacfb90404bbe8297
ms.sourcegitcommit: 2ac7d64bb2db75ace516a604866850fce5cb2174
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/14/2018
ms.locfileid: "26298549"
---
# <a name="create-custom-functions-in-excel-preview"></a>在 Excel 中创建自定义函数（预览）

开发人员可以借助自定义函数向 Excel 添加新函数，方法是在 JavaScript 中将这些函数定义为加载项的一部分。 Excel 中的用户可以访问自定义函数，就像他们访问 Excel 中的任何本机函数一样，比如 `SUM()`。 本文介绍了如何在 Excel 中创建自定义函数。

[!include[Excel custom functions note](../includes/excel-custom-functions-note.md)]

下图演示最终用户将自定义函数插入到 Excel 工作表单元格的过程。 `CONTOSO.ADD42` 自定义函数旨在向用户指定作为函数输入参数的数字对添加 42。

<img alt="animated image showing an end user inserting the CONTOSO.ADD42 custom function into a cell of an Excel worksheet" src="../images/custom-function.gif" width="579" height="383" />

以下代码定义 `ADD42` 自定义函数。

```js
function add42(a, b) {
  return a + b + 42;
}
```

> [!NOTE]
> 本文后面的[已知问题](#known-issues)部分指定自定义函数的当前限制。

## <a name="components-of-a-custom-functions-add-in-project"></a>自定义函数加载项项目的组件

如果使用 [Yo Office 生成器](https://github.com/OfficeDev/generator-office)创建 Excel 自定义函数加载项项目，将在生成器创建的项目中看到以下文件：

| 文件 | 文件格式 | 说明 |
|------|-------------|-------------|
| **./src/customfunctions.js**<br/>或<br/>**./src/customfunctions.ts** | JavaScript<br/>或<br/>TypeScript | 包含定义自定义函数的代码。 |
| **./config/customfunctions.json** | JSON | 包含描述自定义函数的元数据，使 Excel 能够注册自定义函数，并使其可供最终用户使用。 |
| **./index.html** | HTML | 提供对定义自定义函数的 JavaScript 文件的&lt;脚本&gt;引用。 |
| **./manifest.xml** | XML | 指定加载项中所有自定义函数的命名空间以及此表中前面列出的 JavaScript、JSON 和 HTML 文件的位置。 |

下列部分将提供有关这些文件的详细信息。

### <a name="script-file"></a>脚本文件 

脚本文件（Yo Office 生成器创建的项目中的 **./src/customfunctions.js** 或 **./src/customfunctions.ts**）包含定义自定义函数并将自定义函数名称映射到 [JSON 元数据文件](#json-metadata-file)中的对象的代码。 

例如，以下代码定义自定义函数 `add` 和 `increment`，然后指定这两个函数的映射信息。 将 `add` 函数映射到 JSON 元数据文件中的对象，其中 `id` 属性的值为 **ADD**，将 `increment` 函数映射到元数据文件中的对象，其中 `id` 属性的值为 **INCREMENT**。 有关将脚本文件中的函数名称映射到 JSON 元数据文件中的对象的更多信息，请参阅[自定义函数最佳实践](custom-functions-best-practices.md#mapping-function-names-to-json-metadata)。

```js
function add(first, second){
  return first + second;
}

function increment(incrementBy, callback) {
  var result = 0;
  var timer = setInterval(function() {
    result += incrementBy;
    callback.setResult(result);
  }, 1000);

  callback.onCanceled = function() {
    clearInterval(timer);
  };
}

// map `id` values in the JSON metadata file to the JavaScript function names
CustomFunctionMappings.ADD = add;
CustomFunctionMappings.INCREMENT = increment;
```

### <a name="json-metadata-file"></a>JSON 元数据文件 

自定义函数元数据文件（Yo Office 生成器创建的项目中的 **./config/customfunctions.json**）提供 Excel 注册自定义函数并使其可供最终用户使用所需的信息。 自定义函数在用户首次运行加载项时注册。 之后，它们可在所有工作簿（即，不仅仅是在加载项初始运行的工作簿）中供同一用户使用。

> [!TIP]
> 托管 JSON 文件的服务器上的服务器设置必须启用 [CORS](https://developer.mozilla.org/docs/Web/HTTP/CORS)，以便自定义函数在 Excel Online 中正常工作。

**customfunctions.json** 中的以下代码指定上述 `add` 函数和 `increment` 函数的元数据。 此代码示例后面的表提供了有关此 JSON 对象中各个属性的详细信息。 有关在 JSON 元数据文件中指定 `id` 和 `name` 属性值的详细信息，请参阅[自定义函数最佳实践](custom-functions-best-practices.md#mapping-function-names-to-json-metadata)。

```json
{
  "$schema": "https://developer.microsoft.com/en-us/json-schemas/office-js/custom-functions.schema.json",
  "functions": [
    {
      "id": "ADD",
      "name": "ADD",
      "description": "Add two numbers",
      "helpUrl": "http://www.contoso.com",
      "result": {
        "type": "number",
        "dimensionality": "scalar"
      },
      "parameters": [
        {
          "name": "first",
          "description": "first number to add",
          "type": "number",
          "dimensionality": "scalar"
        },
        {
          "name": "second",
          "description": "second number to add",
          "type": "number",
          "dimensionality": "scalar"
        }
      ]
    },
    {
      "id": "INCREMENT",
      "name": "INCREMENT",
      "description": "Periodically increment a value",
      "helpUrl": "http://www.contoso.com",
      "result": {
          "type": "number",
          "dimensionality": "scalar"
    },
    "parameters": [
        {
            "name": "increment",
            "description": "Amount to increment",
            "type": "number",
            "dimensionality": "scalar"
        }
    ],
    "options": {
        "cancelable": true,
        "stream": true
      }
    }
  ]
}
```

下表列出了 JSON 元数据文件中的常见属性。 有关 JSON 元数据文件的更多详细信息，请参阅[自定义函数元数据](custom-functions-json.md)。

| 属性  | 说明 |
|---------|---------|
| `id` | 函数的唯一 ID。 此 ID 只能包含字母数字字符和句点，设置后不应更改。 |
| `name` | 最终用户在 Excel 中看到的函数名称。 在 Excel 中，此函数名称将以 [XML 清单文件](#manifest-file)中指定的自定义函数命名空间作为前缀。 |
| `helpUrl` | 当用户请求帮助时显示的页面的 URL。 |
| `description` | 说明函数的功能。 当函数是 Excel 自动完成菜单中的选中项时，此值将作为工具提示显示。 |
| `result`  | 定义函数返回的信息类型的对象。 有关此对象的详细信息，请参阅[结果](custom-functions-json.md#result)。 |
| `parameters` | 定义函数的输入参数的数组。 有关此对象的详细信息，请参阅[参数](custom-functions-json.md#parameters)。 |
| `options` | 使用户能够自定义 Excel 执行函数的方式和时间。 有关如何使用此属性的详细信息，请参阅本文后面的[流式处理函数](#streaming-functions)和[取消函数](#canceling-a-function)。 |

### <a name="manifest-file"></a>清单文件

定义自定义函数的加载项的 XML 清单文件（Yo Office 生成器创建的项目中的 **./manifest.xml**）指定加载项中所有自定义函数的命名空间以及 JavaScript、JSON 和 HTML 文件的位置。 下面的 XML 标记显示了 `<ExtensionPoint>` 和 `<Resources>` 元素的一个示例，必须在加载项清单中包含这些元素才能启用自定义函数。  

```xml
<VersionOverrides xmlns="http://schemas.microsoft.com/office/taskpaneappversionoverrides" xsi:type="VersionOverridesV1_0">
    <Hosts>
        <Host xsi:type="Workbook">
            <AllFormFactors>
                <ExtensionPoint xsi:type="CustomFunctions">
                    <Script>
                        <SourceLocation resid="JS-URL" /> <!--resid points to location of JavaScript file-->
                    </Script>
                    <Page>
                        <SourceLocation resid="HTML-URL"/> <!--resid points to location of HTML file-->
                    </Page>
                    <Metadata>
                        <SourceLocation resid="JSON-URL" /> <!--resid points to location of JSON file-->
                    </Metadata>
                    <Namespace resid="namespace" />
                </ExtensionPoint>
            </AllFormFactors>
        </Host>
    </Hosts>
    <Resources>
        <bt:Urls>
            <bt:Url id="JSON-URL" DefaultValue="http://127.0.0.1:8080/customfunctions.json" /> <!--specifies the location of your JSON file-->
            <bt:Url id="JS-URL" DefaultValue="http://127.0.0.1:8080/customfunctions.js" /> <!--specifies the location of your JavaScript file-->
            <bt:Url id="HTML-URL" DefaultValue="http://127.0.0.1:8080/index.html" /> <!--specifies the location of your HTML file-->
        </bt:Urls>
        <bt:ShortStrings>
            <bt:String id="namespace" DefaultValue="CONTOSO" /> <!--specifies the namespace that will be prepended to a function's name when it is called in Excel. Can only contain alphanumeric characters and periods.-->
        </bt:ShortStrings>
    </Resources>
</VersionOverrides>
```

> [!NOTE]
> Excel 中的函数在前面追加 XML 清单文件中指定的命名空间作为前缀。 函数的命名空间在函数名称之前，并用句点分隔。 例如，若要在 Excel 工作表的单元格中调用函数 `ADD42`，需输入 `=CONTOSO.ADD42`，因为 `CONTOSO` 是命名空间，`ADD42` 是 JSON 文件中指定的函数的名称。 命名空间旨在作为公司或加载项的标识符使用。 命名空间只能包含字母数字字符和句点。

## <a name="functions-that-return-data-from-external-sources"></a>从外部源返回数据的函数

如果自定义函数从外部源（如 Web）检索数据，则必须：

1. 将 JavaScript Promise 返回到 Excel。

2. 使用回调函数解析带有最终值的 Promise。

在 Excel 等待最终结果时，自定义函数会在单元格中显示一个 `#GETTING_DATA` 临时结果。 在等待结果时，用户可以与工作表的其余部分正常交互。

在下面的代码示例中，`getTemperature()` 自定义函数检索温度计的当前温度。 注意，`sendWebRequest` 是一个假设函数（此处未指定），它使用 [XHR](custom-functions-runtime.md#xhr-example) 调用温度 Web 服务。

```js
function getTemperature(thermometerID){
    return new Promise(function(setResult){
        sendWebRequest(thermometerID, function(data){
            setResult(data.temperature);
        });
    });
}
```

## <a name="streaming-functions"></a>流式处理函数

流式处理自定义函数使用户能够在不需要用户显式请求数据刷新的情况下，随着时间的推移向单元格重复输出数据。 下面的代码示例是一个自定义函数，它每秒向结果添加一个数字。 关于此代码，请注意以下几点：

- Excel 使用 `setResult` 回调自动显示每个新值。

- 当最终用户从自动完成菜单中选择函数时，不会在 Excel 中向其显示第二个输入参数 `handler`。

- `onCanceled` 回调定义取消函数时执行的函数。 对于任何流式处理函数，都必须实现此类取消处理程序。 有关详细信息，请参阅[取消函数](#canceling-a-function)。

```js
function incrementValue(increment, handler){
  var result = 0;
  setInterval(function(){
    result += increment;
    handler.setResult(result);
  }, 1000);

  handler.onCanceled = function(){
    clearInterval(timer);
  }
}
```

在 JSON 元数据文件中为流式处理函数指定元数据时，必须在 `options` 对象中设置属性 `"cancelable": true` 和 `"stream": true`，如以下示例所示。

```json
{
  "id": "INCREMENT",
  "name": "INCREMENT",
  "description": "Periodically increment a value",
  "helpUrl": "http://www.contoso.com",
  "result": {
    "type": "number",
    "dimensionality": "scalar"
  },
  "parameters": [
    {
      "name": "increment",
      "description": "Amount to increment",
      "type": "number",
      "dimensionality": "scalar"
    }
  ],
  "options": {
    "cancelable": true,
    "stream": true
  }
}
```

## <a name="canceling-a-function"></a>取消函数

在某些情况下，可能需要取消执行流式处理自定义函数，以减少其带宽消耗、工作内存和 CPU 负载。 Excel 会在以下情况下取消函数的执行：

- 用户编辑或删除引用函数的单元格。

- 函数的参数（输入）之一发生变化。 在这种情况下，取消之后还会触发新的函数调用。

- 用户手动触发重新计算。 在这种情况下，取消之后还会触发新的函数调用。

为了能够取消函数，必须在 JavaScript 函数中实现一个取消处理程序，并在说明函数的 JSON 元数据中指定 `options` 对象中的属性 `"cancelable": true`。 本文前一部分中的代码示例提供了这些方法的示例。

## <a name="saving-and-sharing-state"></a>保存和共享状态

自定义函数可以将数据保存在全局 JavaScript 变量中，可用于后续调用。 当用户从多个单元格调用同一个自定义函数时，保存状态非常有用，因为函数的所有实例都可以访问该状态。 例如，可以保存调用某个 Web 资源时返回的数据，以避免再次调用同一个 Web 资源。

下面的代码示例演示温度流式处理函数的实现过程，该函数在全局范围内保存状态。 关于此代码，请注意以下几点：

- `streamTemperature` 函数每秒更新单元格中显示的温度值，并使用 `savedTemperatures` 变量作为其数据源。

- 因为 `streamTemperature` 是一个流式处理函数，它将实现一个取消处理程序，当函数被取消时该处理程序将运行。

- 如果用户从 Excel 中的多个单元格调用 `streamTemperature` 函数，则 `streamTemperature` 函数在每次运行时都会从相同的 `savedTemperatures` 变量读取数据。 

- `refreshTemperature` 函数每秒读取特定温度计的温度，并将结果存储在 `savedTemperatures` 变量中。 因为 `refreshTemperature` 函数不在 Excel 中向最终用户显示，所以不需要在 JSON 文件中注册。

```js
var savedTemperatures;

function streamTemperature(thermometerID, handler){
  if(!savedTemperatures[thermometerID]){
    refreshTemperature(thermometerID); // starts fetching temperatures if the thermometer hasn't been read yet
  }

  function getNextTemperature(){
    handler.setResult(savedTemperatures[thermometerID]); // setResult sends the saved temperature value to Excel.
    var delayTime = 1000; // Amount of milliseconds to delay a request by.
    setTimeout(getNextTemperature, delayTime); // Wait 1 second before updating Excel again.

    handler.onCancelled() = function {
      clearTimeout(delayTime);
    }
  }
  getNextTemperature();
}

function refreshTemperature(thermometerID){
  sendWebRequest(thermometerID, function(data){
    savedTemperatures[thermometerID] = data.temperature;
  });
  setTimeout(function(){
    refreshTemperature(thermometerID);
  }, 1000); // Wait 1 second before reading the thermometer again, and then update the saved temperature of thermometerID.
}
```

## <a name="working-with-ranges-of-data"></a>使用数据区域

自定义函数可以接受数据区域作为输入参数，也可以返回数据区域。 在 JavaScript，数据区域表示为一个二维数组。

例如，假设函数从 Excel 中存储的数字区域返回第二个最高值。 下面的函数接受参数 `values`，即 `Excel.CustomFunctionDimensionality.matrix` 类型。 请注意，在此函数的 JSON 元数据中，将参数的 `type` 属性设置为 `matrix`。

```js
function secondHighest(values){
  let highest = values[0][0], secondHighest = values[0][0];
  for(var i = 0; i < values.length; i++){
    for(var j = 1; j < values[i].length; j++){
      if(values[i][j] >= highest){
        secondHighest = highest;
        highest = values[i][j];
      }
      else if(values[i][j] >= secondHighest){
        secondHighest = values[i][j];
      }
    }
  }
  return secondHighest;
}
```

## <a name="handling-errors"></a>处理错误

在生成定义自定义函数的加载项时，请务必加入错误处理逻辑，以便解决运行时错误。 自定义函数的错误处理与 [Excel JavaScript API 的错误处理](excel-add-ins-error-handling.md)大致相同。 在以下代码示例中，`.catch` 将处理之前发生在代码中的任何错误。

```js
function getComment(x) {
  let url = "https://www.contoso.com/comments/" + x;

  return fetch(url)
    .then(function (data) {
      return data.json();
    })
    .then((json) => {
      return json.body;
    })
    .catch(function (error) {
      throw error;
    })
}
```

## <a name="known-issues"></a>已知问题

- Excel 暂未使用帮助 URL 和参数说明。
- 移动客户端目前还不能在 Excel 上使用自定义函数。
- 尚不支持 Volatile 函数（每当电子表格中不相关的数据发生变化时都会自动重新计算的函数）。
- 尚未启用通过 Office 365 管理门户和 AppSource 进行部署。
- 在一段时间处于非活动状态后，Excel Online 中的自定义函数可能会在会话期间停止工作。 刷新浏览器页面 (F5) 并重新输入自定义函数以恢复该功能。
- 如果在 Excel for Windows 上运行多个加载项，可能会在工作表单元格中看到 **#GETTING_DATA** 临时结果。 关闭所有 Excel 窗口并重启 Excel。
- 将来可能会推出专门针对自定义函数的调试工具。 在此期间，可以使用 F12 开发人员工具在 Excel Online 上进行调试。 有关详细信息，请参阅[自定义函数最佳实践](custom-functions-best-practices.md)。

## <a name="changelog"></a>更改日志

- **2017 年 11 月 7 日**：发布了*自定义函数（预览）和示例
- **2017 年 11 月 20 日**：修复了使用内部版本 8801 及更高版本的函数的兼容性问题
- **2017 年 11 月 28 日**：发布了*对取消异步函数的支持（需要对流式处理函数进行相应更改）
- **2018 年 5 月 7 日**：发布了*对 Mac、Excel Online 和在进程中运行的异步函数的支持
- **2018 年 9 月 20 日**：发布了对自定义函数 JavaScript 运行时的支持。 有关详细信息，请参阅 [Excel 自定义函数的运行时](custom-functions-runtime.md)。
- **2018 年 10 月 20 日**：随着 [10 月预览体验内部版本](https://support.office.com/zh-CN/article/what-s-new-for-office-insiders-c152d1e2-96ff-4ce9-8c14-e74e13847a24)的推出，自定义函数现在需要适用于 Windows Desktop 和 Online 的[自定义函数元数据](custom-functions-json.md)中的“id”参数。 在 Mac 上，应忽略此参数。


\* 转到 [Office 预览体验成员](https://products.office.com/office-insider)频道（以前称为“预览体验成员 - 快”）

## <a name="see-also"></a>另请参阅

* [自定义函数元数据](custom-functions-json.md)
* [Excel 自定义函数的运行时](custom-functions-runtime.md)
* [自定义函数最佳实践](custom-functions-best-practices.md)
* [Excel 自定义函数教程](excel-tutorial-custom-functions.md)
