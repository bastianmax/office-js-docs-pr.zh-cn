
# <a name="mailbox"></a><span data-ttu-id="ad7b5-101">mailbox</span><span class="sxs-lookup"><span data-stu-id="ad7b5-101">mailbox</span></span>

### <span data-ttu-id="ad7b5-p101">[Office](Office.md)[.context](Office.context.md). mailbox</span><span class="sxs-lookup"><span data-stu-id="ad7b5-p101">[Office](Office.md)[.context](Office.context.md). mailbox</span></span>

<span data-ttu-id="ad7b5-104">为 Microsoft Outlook 和 Microsoft Outlook 网页版提供对 Outlook 加载项对象模型的访问权限。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-104">Provides access to the Outlook Add-in object model for Microsoft Outlook and Microsoft Outlook on the web.</span></span>

##### <a name="requirements"></a><span data-ttu-id="ad7b5-105">要求</span><span class="sxs-lookup"><span data-stu-id="ad7b5-105">Requirements</span></span>

|<span data-ttu-id="ad7b5-106">要求</span><span class="sxs-lookup"><span data-stu-id="ad7b5-106">Requirement</span></span>| <span data-ttu-id="ad7b5-107">值</span><span class="sxs-lookup"><span data-stu-id="ad7b5-107">Value</span></span>|
|---|---|
|[<span data-ttu-id="ad7b5-108">最低邮箱要求集版本</span><span class="sxs-lookup"><span data-stu-id="ad7b5-108">Minimum mailbox requirement set version</span></span>](/office/dev/add-ins/reference/requirement-sets/outlook-api-requirement-sets)| <span data-ttu-id="ad7b5-109">1.0</span><span class="sxs-lookup"><span data-stu-id="ad7b5-109">1.0</span></span>|
|[<span data-ttu-id="ad7b5-110">最低权限级别</span><span class="sxs-lookup"><span data-stu-id="ad7b5-110">Minimum permission level</span></span>](https://docs.microsoft.com/outlook/add-ins/understanding-outlook-add-in-permissions)| <span data-ttu-id="ad7b5-111">Restricted</span><span class="sxs-lookup"><span data-stu-id="ad7b5-111">Restricted</span></span>|
|[<span data-ttu-id="ad7b5-112">适用的 Outlook 模式</span><span class="sxs-lookup"><span data-stu-id="ad7b5-112">Applicable Outlook mode</span></span>](https://docs.microsoft.com/outlook/add-ins/#extension-points)| <span data-ttu-id="ad7b5-113">撰写或阅读​</span><span class="sxs-lookup"><span data-stu-id="ad7b5-113">Compose or read</span></span>|

##### <a name="members-and-methods"></a><span data-ttu-id="ad7b5-114">成员和方法</span><span class="sxs-lookup"><span data-stu-id="ad7b5-114">Members and methods</span></span>

| <span data-ttu-id="ad7b5-115">成员</span><span class="sxs-lookup"><span data-stu-id="ad7b5-115">Member</span></span> | <span data-ttu-id="ad7b5-116">类型</span><span class="sxs-lookup"><span data-stu-id="ad7b5-116">Type</span></span> |
|--------|------|
| [<span data-ttu-id="ad7b5-117">ewsUrl</span><span class="sxs-lookup"><span data-stu-id="ad7b5-117">ewsUrl</span></span>](#ewsurl-string) | <span data-ttu-id="ad7b5-118">成员</span><span class="sxs-lookup"><span data-stu-id="ad7b5-118">Member</span></span> |
| [<span data-ttu-id="ad7b5-119">restUrl</span><span class="sxs-lookup"><span data-stu-id="ad7b5-119">restUrl</span></span>](#resturl-string) | <span data-ttu-id="ad7b5-120">成员</span><span class="sxs-lookup"><span data-stu-id="ad7b5-120">Member</span></span> |
| [<span data-ttu-id="ad7b5-121">addHandlerAsync</span><span class="sxs-lookup"><span data-stu-id="ad7b5-121">addHandlerAsync</span></span>](#addhandlerasynceventtype-handler-options-callback) | <span data-ttu-id="ad7b5-122">方法</span><span class="sxs-lookup"><span data-stu-id="ad7b5-122">Method</span></span> |
| [<span data-ttu-id="ad7b5-123">convertToEwsId</span><span class="sxs-lookup"><span data-stu-id="ad7b5-123">convertToEwsId</span></span>](#converttoewsiditemid-restversion--string) | <span data-ttu-id="ad7b5-124">方法</span><span class="sxs-lookup"><span data-stu-id="ad7b5-124">Method</span></span> |
| [<span data-ttu-id="ad7b5-125">convertToLocalClientTime</span><span class="sxs-lookup"><span data-stu-id="ad7b5-125">convertToLocalClientTime</span></span>](#converttolocalclienttimetimevalue--localclienttimejavascriptapioutlook16officelocalclienttime) | <span data-ttu-id="ad7b5-126">方法</span><span class="sxs-lookup"><span data-stu-id="ad7b5-126">Method</span></span> |
| [<span data-ttu-id="ad7b5-127">convertToRestId</span><span class="sxs-lookup"><span data-stu-id="ad7b5-127">convertToRestId</span></span>](#converttorestiditemid-restversion--string) | <span data-ttu-id="ad7b5-128">方法</span><span class="sxs-lookup"><span data-stu-id="ad7b5-128">Method</span></span> |
| [<span data-ttu-id="ad7b5-129">convertToUtcClientTime</span><span class="sxs-lookup"><span data-stu-id="ad7b5-129">convertToUtcClientTime</span></span>](#converttoutcclienttimeinput--date) | <span data-ttu-id="ad7b5-130">方法</span><span class="sxs-lookup"><span data-stu-id="ad7b5-130">Method</span></span> |
| [<span data-ttu-id="ad7b5-131">displayAppointmentForm</span><span class="sxs-lookup"><span data-stu-id="ad7b5-131">displayAppointmentForm</span></span>](#displayappointmentformitemid) | <span data-ttu-id="ad7b5-132">方法</span><span class="sxs-lookup"><span data-stu-id="ad7b5-132">Method</span></span> |
| [<span data-ttu-id="ad7b5-133">displayMessageForm</span><span class="sxs-lookup"><span data-stu-id="ad7b5-133">displayMessageForm</span></span>](#displaymessageformitemid) | <span data-ttu-id="ad7b5-134">方法</span><span class="sxs-lookup"><span data-stu-id="ad7b5-134">Method</span></span> |
| [<span data-ttu-id="ad7b5-135">displayNewAppointmentForm</span><span class="sxs-lookup"><span data-stu-id="ad7b5-135">displayNewAppointmentForm</span></span>](#displaynewappointmentformparameters) | <span data-ttu-id="ad7b5-136">方法</span><span class="sxs-lookup"><span data-stu-id="ad7b5-136">Method</span></span> |
| [<span data-ttu-id="ad7b5-137">displayNewMessageForm</span><span class="sxs-lookup"><span data-stu-id="ad7b5-137">displayNewMessageForm</span></span>](#displaynewmessageformparameters) | <span data-ttu-id="ad7b5-138">方法</span><span class="sxs-lookup"><span data-stu-id="ad7b5-138">Method</span></span> |
| [<span data-ttu-id="ad7b5-139">getCallbackTokenAsync</span><span class="sxs-lookup"><span data-stu-id="ad7b5-139">getCallbackTokenAsync</span></span>](#getcallbacktokenasyncoptions-callback) | <span data-ttu-id="ad7b5-140">方法</span><span class="sxs-lookup"><span data-stu-id="ad7b5-140">Method</span></span> |
| [<span data-ttu-id="ad7b5-141">getCallbackTokenAsync</span><span class="sxs-lookup"><span data-stu-id="ad7b5-141">getCallbackTokenAsync</span></span>](#getcallbacktokenasynccallback-usercontext) | <span data-ttu-id="ad7b5-142">方法</span><span class="sxs-lookup"><span data-stu-id="ad7b5-142">Method</span></span> |
| [<span data-ttu-id="ad7b5-143">getUserIdentityTokenAsync</span><span class="sxs-lookup"><span data-stu-id="ad7b5-143">getUserIdentityTokenAsync</span></span>](#getuseridentitytokenasynccallback-usercontext) | <span data-ttu-id="ad7b5-144">方法</span><span class="sxs-lookup"><span data-stu-id="ad7b5-144">Method</span></span> |
| [<span data-ttu-id="ad7b5-145">makeEwsRequestAsync</span><span class="sxs-lookup"><span data-stu-id="ad7b5-145">makeEwsRequestAsync</span></span>](#makeewsrequestasyncdata-callback-usercontext) | <span data-ttu-id="ad7b5-146">方法</span><span class="sxs-lookup"><span data-stu-id="ad7b5-146">Method</span></span> |

### <a name="namespaces"></a><span data-ttu-id="ad7b5-147">命名空间</span><span class="sxs-lookup"><span data-stu-id="ad7b5-147">Namespaces</span></span>

<span data-ttu-id="ad7b5-148">[诊断](Office.context.mailbox.diagnostics.md)：将诊断信息提供给 Outlook 外接程序。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-148">[diagnostics](Office.context.mailbox.diagnostics.md): Provides diagnostic information to an Outlook add-in.</span></span>

<span data-ttu-id="ad7b5-149">[item](Office.context.mailbox.item.md)：提供用于访问 Outlook 加载项中的邮件或约会的方法和属性。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-149">[item](Office.context.mailbox.item.md): Provides methods and properties for accessing a message or appointment in an Outlook add-in.</span></span>

<span data-ttu-id="ad7b5-150">[userProfile](Office.context.mailbox.userProfile.md)：提供有关 Outlook 外接程序中的用户信息。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-150">[userProfile](Office.context.mailbox.userProfile.md): Provides information about the user in an Outlook add-in.</span></span>

### <a name="members"></a><span data-ttu-id="ad7b5-151">成员</span><span class="sxs-lookup"><span data-stu-id="ad7b5-151">Members</span></span>

#### <a name="ewsurl-string"></a><span data-ttu-id="ad7b5-152">ewsUrl： 字符串</span><span class="sxs-lookup"><span data-stu-id="ad7b5-152">ewsUrl :String</span></span>

<span data-ttu-id="ad7b5-p102">获取此电子邮件帐户的 Exchange Web 服务 (EWS) 端点 URL。仅限阅读模式。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-p102">Gets the URL of the Exchange Web Services (EWS) endpoint for this email account. Read mode only.</span></span>

> [!NOTE]
> <span data-ttu-id="ad7b5-155">在 Outlook for iOS 或 Outlook for Android 中不支持此成员。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-155">Note: This member is not supported in Outlook for iOS or Outlook for Android.</span></span>

<span data-ttu-id="ad7b5-p103">远程服务可使用 `ewsUrl` 值对用户邮箱进行 EWS 调用。例如，可以创建远程服务来 [获取选定项目中的附件](https://docs.microsoft.com/outlook/add-ins/get-attachments-of-an-outlook-item)。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-p103">The `ewsUrl` value can be used by a remote service to make EWS calls to the user's mailbox. For example, you can create a remote service to [get attachments from the selected item](https://docs.microsoft.com/outlook/add-ins/get-attachments-of-an-outlook-item).</span></span>

<span data-ttu-id="ad7b5-158">应用必须在其清单中指定拥有 **ReadItem** 权限，才能在阅读模式中调用 `ewsUrl` 成员。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-158">Your app must have the **ReadItem** permission specified in its manifest to call the `ewsUrl` member in read mode.</span></span>

<span data-ttu-id="ad7b5-p104">在撰写模式中，必须调用 [`saveAsync`](Office.context.mailbox.item.md#saveasyncoptions-callback) 方法，才能使用 `ewsUrl` 成员。应用必须具有调用 `saveAsync` 方法的 **ReadWriteItem** 权限。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-p104">In compose mode you must call the [`saveAsync`](Office.context.mailbox.item.md#saveasyncoptions-callback) method before you can use the `ewsUrl` member. Your app must have **ReadWriteItem** permissions to call the `saveAsync` method.</span></span>

##### <a name="type"></a><span data-ttu-id="ad7b5-161">类型：</span><span class="sxs-lookup"><span data-stu-id="ad7b5-161">Type:</span></span>

*   <span data-ttu-id="ad7b5-162">字符串</span><span class="sxs-lookup"><span data-stu-id="ad7b5-162">String</span></span>

##### <a name="requirements"></a><span data-ttu-id="ad7b5-163">要求</span><span class="sxs-lookup"><span data-stu-id="ad7b5-163">Requirements</span></span>

|<span data-ttu-id="ad7b5-164">要求</span><span class="sxs-lookup"><span data-stu-id="ad7b5-164">Requirement</span></span>| <span data-ttu-id="ad7b5-165">值</span><span class="sxs-lookup"><span data-stu-id="ad7b5-165">Value</span></span>|
|---|---|
|[<span data-ttu-id="ad7b5-166">最低邮箱要求集版本</span><span class="sxs-lookup"><span data-stu-id="ad7b5-166">Minimum mailbox requirement set version</span></span>](/office/dev/add-ins/reference/requirement-sets/outlook-api-requirement-sets)| <span data-ttu-id="ad7b5-167">1.0</span><span class="sxs-lookup"><span data-stu-id="ad7b5-167">1.0</span></span>|
|[<span data-ttu-id="ad7b5-168">最低权限级别</span><span class="sxs-lookup"><span data-stu-id="ad7b5-168">Minimum permission level</span></span>](https://docs.microsoft.com/outlook/add-ins/understanding-outlook-add-in-permissions)| <span data-ttu-id="ad7b5-169">ReadItem</span><span class="sxs-lookup"><span data-stu-id="ad7b5-169">ReadItem</span></span>|
|[<span data-ttu-id="ad7b5-170">适用的 Outlook 模式</span><span class="sxs-lookup"><span data-stu-id="ad7b5-170">Applicable Outlook mode</span></span>](https://docs.microsoft.com/outlook/add-ins/#extension-points)| <span data-ttu-id="ad7b5-171">撰写或阅读​</span><span class="sxs-lookup"><span data-stu-id="ad7b5-171">Compose or read</span></span>|

#### <a name="resturl-string"></a><span data-ttu-id="ad7b5-172">restUrl :String</span><span class="sxs-lookup"><span data-stu-id="ad7b5-172">restUrl :String</span></span>

<span data-ttu-id="ad7b5-173">获取此电子邮件帐户的 REST 端点 URL。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-173">Gets the URL of the REST endpoint for this email account.</span></span>

<span data-ttu-id="ad7b5-174">`restUrl` 值可用于对用户邮箱进行 [REST API](https://docs.microsoft.com/outlook/rest/) 调用。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-174">The `restUrl` value can be used to make [REST API](https://docs.microsoft.com/outlook/rest/) calls to the user's mailbox.</span></span>

<span data-ttu-id="ad7b5-175">应用必须在其清单中指定拥有 **ReadItem** 权限，才能在阅读模式中调用 `restUrl` 成员。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-175">Your app must have the **ReadItem** permission specified in its manifest to call the `restUrl` member in read mode.</span></span>

<span data-ttu-id="ad7b5-p105">在撰写模式中，必须调用 [`saveAsync`](Office.context.mailbox.item.md#saveasyncoptions-callback) 方法，才能使用 `restUrl` 成员。应用必须具有调用 `saveAsync` 方法的 **ReadWriteItem** 权限。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-p105">In compose mode you must call the [`saveAsync`](Office.context.mailbox.item.md#saveasyncoptions-callback) method before you can use the `restUrl` member. Your app must have **ReadWriteItem** permissions to call the `saveAsync` method.</span></span>

##### <a name="type"></a><span data-ttu-id="ad7b5-178">类型：</span><span class="sxs-lookup"><span data-stu-id="ad7b5-178">Type:</span></span>

*   <span data-ttu-id="ad7b5-179">String</span><span class="sxs-lookup"><span data-stu-id="ad7b5-179">String</span></span>

##### <a name="requirements"></a><span data-ttu-id="ad7b5-180">要求</span><span class="sxs-lookup"><span data-stu-id="ad7b5-180">Requirements</span></span>

|<span data-ttu-id="ad7b5-181">要求</span><span class="sxs-lookup"><span data-stu-id="ad7b5-181">Requirement</span></span>| <span data-ttu-id="ad7b5-182">值</span><span class="sxs-lookup"><span data-stu-id="ad7b5-182">Value</span></span>|
|---|---|
|[<span data-ttu-id="ad7b5-183">最低邮箱要求集版本</span><span class="sxs-lookup"><span data-stu-id="ad7b5-183">Minimum mailbox requirement set version</span></span>](/office/dev/add-ins/reference/requirement-sets/outlook-api-requirement-sets)| <span data-ttu-id="ad7b5-184">1.5</span><span class="sxs-lookup"><span data-stu-id="ad7b5-184">1.5</span></span> |
|[<span data-ttu-id="ad7b5-185">最低权限级别</span><span class="sxs-lookup"><span data-stu-id="ad7b5-185">Minimum permission level</span></span>](https://docs.microsoft.com/outlook/add-ins/understanding-outlook-add-in-permissions)| <span data-ttu-id="ad7b5-186">ReadItem</span><span class="sxs-lookup"><span data-stu-id="ad7b5-186">ReadItem</span></span>|
|[<span data-ttu-id="ad7b5-187">适用的 Outlook 模式</span><span class="sxs-lookup"><span data-stu-id="ad7b5-187">Applicable Outlook mode</span></span>](https://docs.microsoft.com/outlook/add-ins/#extension-points)| <span data-ttu-id="ad7b5-188">撰写或阅读​</span><span class="sxs-lookup"><span data-stu-id="ad7b5-188">Compose or read</span></span>|

### <a name="methods"></a><span data-ttu-id="ad7b5-189">方法</span><span class="sxs-lookup"><span data-stu-id="ad7b5-189">Methods</span></span>

####  <a name="addhandlerasynceventtype-handler-options-callback"></a><span data-ttu-id="ad7b5-190">addHandlerAsync(eventType, handler, [options], [callback])</span><span class="sxs-lookup"><span data-stu-id="ad7b5-190">addHandlerAsync(eventType, handler, [options], [callback])</span></span>

<span data-ttu-id="ad7b5-191">添加支持事件的事件处理程序。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-191">Adds an event handler for a supported event.</span></span>

<span data-ttu-id="ad7b5-p106">目前，唯一支持的事件类型是 `Office.EventType.ItemChanged`，用户选择一个新项目时将调用该事件类型。此事件由实现可固定任务窗格的加载项使用，并允许加载项根据当前选定的项目刷新任务窗格 UI。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-p106">Currently the only supported event type is `Office.EventType.ItemChanged`, which is invoked when the user selects a new item. This event is used by add-ins that implement a pinnable taskpane, and allows the add-in to refresh the taskpane UI based on the currently selected item.</span></span>

##### <a name="parameters"></a><span data-ttu-id="ad7b5-194">参数：</span><span class="sxs-lookup"><span data-stu-id="ad7b5-194">Parameters:</span></span>

| <span data-ttu-id="ad7b5-195">名称</span><span class="sxs-lookup"><span data-stu-id="ad7b5-195">Name</span></span> | <span data-ttu-id="ad7b5-196">类型</span><span class="sxs-lookup"><span data-stu-id="ad7b5-196">Type</span></span> | <span data-ttu-id="ad7b5-197">属性</span><span class="sxs-lookup"><span data-stu-id="ad7b5-197">Attributes</span></span> | <span data-ttu-id="ad7b5-198">说明</span><span class="sxs-lookup"><span data-stu-id="ad7b5-198">Description</span></span> |
|---|---|---|---|
| `eventType` | [<span data-ttu-id="ad7b5-199">Office.EventType</span><span class="sxs-lookup"><span data-stu-id="ad7b5-199">Office.EventType</span></span>](office.md#eventtype-string) || <span data-ttu-id="ad7b5-200">应调用处理程序的事件。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-200">The event that should invoke the handler.</span></span> |
| `handler` | <span data-ttu-id="ad7b5-201">Function</span><span class="sxs-lookup"><span data-stu-id="ad7b5-201">Function</span></span> || <span data-ttu-id="ad7b5-p107">用于处理事件的函数。此函数必须接受单个参数，即对象文本。参数上的 `type` 属性将匹配传递给 `addHandlerAsync` 的 `eventType` 参数。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-p107">The function to handle the event. The function must accept a single parameter, which is an object literal. The `type` property on the parameter will match the `eventType` parameter passed to `addHandlerAsync`.</span></span> |
| `options` | <span data-ttu-id="ad7b5-205">Object</span><span class="sxs-lookup"><span data-stu-id="ad7b5-205">Object</span></span> | <span data-ttu-id="ad7b5-206">&lt;optional&gt;</span><span class="sxs-lookup"><span data-stu-id="ad7b5-206">&lt;optional&gt;</span></span> | <span data-ttu-id="ad7b5-207">包含一个或多个以下属性的对象文本。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-207">An object literal that contains one or more of the following properties.</span></span> |
| `options.asyncContext` | <span data-ttu-id="ad7b5-208">Object</span><span class="sxs-lookup"><span data-stu-id="ad7b5-208">Object</span></span> | <span data-ttu-id="ad7b5-209">&lt;optional&gt;</span><span class="sxs-lookup"><span data-stu-id="ad7b5-209">&lt;optional&gt;</span></span> | <span data-ttu-id="ad7b5-210">开发人员可以提供他们想要在回调方法中访问的任何对象。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-210">Developers can provide any object they wish to access in the callback method.</span></span> |
| `callback` | <span data-ttu-id="ad7b5-211">函数</span><span class="sxs-lookup"><span data-stu-id="ad7b5-211">function</span></span>| <span data-ttu-id="ad7b5-212">&lt;optional&gt;</span><span class="sxs-lookup"><span data-stu-id="ad7b5-212">&lt;optional&gt;</span></span>|<span data-ttu-id="ad7b5-213">方法完成后，使用单个参数 `callback`（一个 [`asyncResult`](/javascript/api/office/office.asyncresult) 对象）调用在 `AsyncResult` 参数中传递的函数。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-213">When the method completes, the function passed in the `callback` parameter is called with a single parameter, `asyncResult`, which is an [`AsyncResult`](/javascript/api/office/office.asyncresult) object.</span></span>|

##### <a name="requirements"></a><span data-ttu-id="ad7b5-214">要求</span><span class="sxs-lookup"><span data-stu-id="ad7b5-214">Requirements</span></span>

|<span data-ttu-id="ad7b5-215">要求</span><span class="sxs-lookup"><span data-stu-id="ad7b5-215">Requirement</span></span>| <span data-ttu-id="ad7b5-216">值</span><span class="sxs-lookup"><span data-stu-id="ad7b5-216">Value</span></span>|
|---|---|
|[<span data-ttu-id="ad7b5-217">最低邮箱要求集版本</span><span class="sxs-lookup"><span data-stu-id="ad7b5-217">Minimum mailbox requirement set version</span></span>](/office/dev/add-ins/reference/requirement-sets/outlook-api-requirement-sets)| <span data-ttu-id="ad7b5-218">1.5</span><span class="sxs-lookup"><span data-stu-id="ad7b5-218">1.5</span></span> |
|[<span data-ttu-id="ad7b5-219">最低权限级别</span><span class="sxs-lookup"><span data-stu-id="ad7b5-219">Minimum permission level</span></span>](https://docs.microsoft.com/outlook/add-ins/understanding-outlook-add-in-permissions)| <span data-ttu-id="ad7b5-220">ReadItem</span><span class="sxs-lookup"><span data-stu-id="ad7b5-220">ReadItem</span></span> |
|[<span data-ttu-id="ad7b5-221">适用的 Outlook 模式</span><span class="sxs-lookup"><span data-stu-id="ad7b5-221">Applicable Outlook mode</span></span>](https://docs.microsoft.com/outlook/add-ins/#extension-points)| <span data-ttu-id="ad7b5-222">撰写或阅读​</span><span class="sxs-lookup"><span data-stu-id="ad7b5-222">Compose or read</span></span>|

##### <a name="example"></a><span data-ttu-id="ad7b5-223">示例</span><span class="sxs-lookup"><span data-stu-id="ad7b5-223">Example</span></span>

```
Office.initialize = function (reason) {
  $(document).ready(function () {
    Office.context.mailbox.addHandlerAsync(Office.EventType.ItemChanged, loadNewItem, function (result) {
      if (result.status === Office.AsyncResultStatus.Failed) {
        // Handle error
      }
    });
  });
};

function loadNewItem(eventArgs) {
  // Load the properties of the newly selected item
  loadProps(Office.context.mailbox.item);
};
```

####  <a name="converttoewsiditemid-restversion--string"></a><span data-ttu-id="ad7b5-224">convertToEwsId(itemId, restVersion) → {String}</span><span class="sxs-lookup"><span data-stu-id="ad7b5-224">convertToEwsId(itemId, restVersion) → {String}</span></span>

<span data-ttu-id="ad7b5-225">将适用 REST 格式化的项目 ID 转换为 EWS 格式。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-225">Converts an item ID formatted for REST into EWS format.</span></span>

> [!NOTE]
> <span data-ttu-id="ad7b5-226">在 Outlook for iOS 或 Outlook for Android 中不支持此方法。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-226">Note: This method is not supported in Outlook for iOS or Outlook for Android.</span></span>

<span data-ttu-id="ad7b5-p108">通过 REST API 检索的项 ID（如 [Outlook 邮件 API](https://docs.microsoft.com/previous-versions/office/office-365-api/api/version-2.0/mail-rest-operations) 或 [Microsoft Graph](http://graph.microsoft.io/)）使用与 Exchange Web 服务 (EWS) 不同的格式。`convertToEwsId` 方法将 REST 格式化的 ID 转换为正确的 EWS 格式。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-p108">Item IDs retrieved via a REST API (such as the [Outlook Mail API](https://docs.microsoft.com/previous-versions/office/office-365-api/api/version-2.0/mail-rest-operations) or the [Microsoft Graph](http://graph.microsoft.io/)) use a different format than the format used by Exchange Web Services (EWS). The `convertToEwsId` method converts a REST-formatted ID into the proper format for EWS.</span></span>

##### <a name="parameters"></a><span data-ttu-id="ad7b5-229">参数：</span><span class="sxs-lookup"><span data-stu-id="ad7b5-229">Parameters:</span></span>

|<span data-ttu-id="ad7b5-230">名称</span><span class="sxs-lookup"><span data-stu-id="ad7b5-230">Name</span></span>| <span data-ttu-id="ad7b5-231">类型</span><span class="sxs-lookup"><span data-stu-id="ad7b5-231">Type</span></span>| <span data-ttu-id="ad7b5-232">说明</span><span class="sxs-lookup"><span data-stu-id="ad7b5-232">Description</span></span>|
|---|---|---|
|`itemId`| <span data-ttu-id="ad7b5-233">字符串</span><span class="sxs-lookup"><span data-stu-id="ad7b5-233">String</span></span>|<span data-ttu-id="ad7b5-234">适用 Outlook REST API 进行格式化的项目 ID。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-234">An item ID formatted for the Outlook REST APIs</span></span>|
|`restVersion`| [<span data-ttu-id="ad7b5-235">Office.MailboxEnums.RestVersion</span><span class="sxs-lookup"><span data-stu-id="ad7b5-235">Office.MailboxEnums.RestVersion</span></span>](/javascript/api/outlook_1_6/office.mailboxenums.restversion)|<span data-ttu-id="ad7b5-236">值指示用于检索项目 ID 的 Outlook REST API 版本。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-236">A value indicating the version of the Outlook REST API used to retrieve the item ID.</span></span>|

##### <a name="requirements"></a><span data-ttu-id="ad7b5-237">要求</span><span class="sxs-lookup"><span data-stu-id="ad7b5-237">Requirements</span></span>

|<span data-ttu-id="ad7b5-238">要求</span><span class="sxs-lookup"><span data-stu-id="ad7b5-238">Requirement</span></span>| <span data-ttu-id="ad7b5-239">值</span><span class="sxs-lookup"><span data-stu-id="ad7b5-239">Value</span></span>|
|---|---|
|[<span data-ttu-id="ad7b5-240">最低邮箱要求集版本</span><span class="sxs-lookup"><span data-stu-id="ad7b5-240">Minimum mailbox requirement set version</span></span>](/office/dev/add-ins/reference/requirement-sets/outlook-api-requirement-sets)| <span data-ttu-id="ad7b5-241">1.3</span><span class="sxs-lookup"><span data-stu-id="ad7b5-241">1.3</span></span>|
|[<span data-ttu-id="ad7b5-242">最低权限级别</span><span class="sxs-lookup"><span data-stu-id="ad7b5-242">Minimum permission level</span></span>](https://docs.microsoft.com/outlook/add-ins/understanding-outlook-add-in-permissions)| <span data-ttu-id="ad7b5-243">Restricted</span><span class="sxs-lookup"><span data-stu-id="ad7b5-243">Restricted</span></span>|
|[<span data-ttu-id="ad7b5-244">适用的 Outlook 模式</span><span class="sxs-lookup"><span data-stu-id="ad7b5-244">Applicable Outlook mode</span></span>](https://docs.microsoft.com/outlook/add-ins/#extension-points)| <span data-ttu-id="ad7b5-245">撰写或阅读​</span><span class="sxs-lookup"><span data-stu-id="ad7b5-245">Compose or read</span></span>|

##### <a name="returns"></a><span data-ttu-id="ad7b5-246">返回：</span><span class="sxs-lookup"><span data-stu-id="ad7b5-246">Returns:</span></span>

<span data-ttu-id="ad7b5-247">类型：String</span><span class="sxs-lookup"><span data-stu-id="ad7b5-247">Type: String</span></span>

##### <a name="example"></a><span data-ttu-id="ad7b5-248">示例</span><span class="sxs-lookup"><span data-stu-id="ad7b5-248">Example</span></span>

```
// Get an item's ID from a REST API
var restId = 'AAMkAGVlOTZjNTM3LW...';

// Treat restId as coming from the v2.0 version of the
// Outlook Mail API
var ewsId = Office.context.mailbox.convertToEwsId(restId, Office.MailboxEnums.RestVersion.v2_0);
```

####  <a name="converttolocalclienttimetimevalue--localclienttimejavascriptapioutlook16officelocalclienttime"></a><span data-ttu-id="ad7b5-249">convertToLocalClientTime(timeValue) → {[LocalClientTime](/javascript/api/outlook_1_6/office.LocalClientTime)}</span><span class="sxs-lookup"><span data-stu-id="ad7b5-249">convertToLocalClientTime(timeValue) → {[LocalClientTime](/javascript/api/outlook_1_6/office.LocalClientTime)}</span></span>

<span data-ttu-id="ad7b5-250">获取包含以本地客户端时间表示时间信息的字典。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-250">Gets a dictionary containing time information in local client time.</span></span>

<span data-ttu-id="ad7b5-p109">Outlook 或 Outlook Web App 邮件应用程序的日期和时间可以使用不同的时区。Outlook 使用客户端计算机时区；Outlook Web App 使用 Exchange 管理中心 (EAC) 中设置的时区。应对日期和时间值进行处理，以便用户界面上显示的值始终与用户预期的时区一致。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-p109">The dates and times used by a mail app for Outlook or Outlook Web App can use different time zones. Outlook uses the client computer time zone; Outlook Web App uses the time zone set on the Exchange Admin Center (EAC). You should handle date and time values so that the values you display on the user interface are always consistent with the time zone that the user expects.</span></span>

<span data-ttu-id="ad7b5-p110">如果在 Outlook 中运行邮件应用程序，`convertToLocalClientTime` 方法将返回多个值设置为客户端计算机时区的字典对象。如果在 Outlook Web App 中运行邮件应用程序，`convertToLocalClientTime` 方法将返回多个值设置为 EAC 中指定的时区的字典对象。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-p110">If the mail app is running in Outlook, the `convertToLocalClientTime` method will return a dictionary object with the values set to the client computer time zone. If the mail app is running in Outlook Web App, the `convertToLocalClientTime` method will return a dictionary object with the values set to the time zone specified in the EAC.</span></span>

##### <a name="parameters"></a><span data-ttu-id="ad7b5-256">参数：</span><span class="sxs-lookup"><span data-stu-id="ad7b5-256">Parameters:</span></span>

|<span data-ttu-id="ad7b5-257">名称</span><span class="sxs-lookup"><span data-stu-id="ad7b5-257">Name</span></span>| <span data-ttu-id="ad7b5-258">类型</span><span class="sxs-lookup"><span data-stu-id="ad7b5-258">Type</span></span>| <span data-ttu-id="ad7b5-259">说明</span><span class="sxs-lookup"><span data-stu-id="ad7b5-259">Description</span></span>|
|---|---|---|
|`timeValue`| <span data-ttu-id="ad7b5-260">Date</span><span class="sxs-lookup"><span data-stu-id="ad7b5-260">Date</span></span>|<span data-ttu-id="ad7b5-261">一个 Date 对象</span><span class="sxs-lookup"><span data-stu-id="ad7b5-261">A Date object</span></span>|

##### <a name="requirements"></a><span data-ttu-id="ad7b5-262">要求</span><span class="sxs-lookup"><span data-stu-id="ad7b5-262">Requirements</span></span>

|<span data-ttu-id="ad7b5-263">要求</span><span class="sxs-lookup"><span data-stu-id="ad7b5-263">Requirement</span></span>| <span data-ttu-id="ad7b5-264">值</span><span class="sxs-lookup"><span data-stu-id="ad7b5-264">Value</span></span>|
|---|---|
|[<span data-ttu-id="ad7b5-265">最低邮箱要求集版本</span><span class="sxs-lookup"><span data-stu-id="ad7b5-265">Minimum mailbox requirement set version</span></span>](/office/dev/add-ins/reference/requirement-sets/outlook-api-requirement-sets)| <span data-ttu-id="ad7b5-266">1.0</span><span class="sxs-lookup"><span data-stu-id="ad7b5-266">1.0</span></span>|
|[<span data-ttu-id="ad7b5-267">最低权限级别</span><span class="sxs-lookup"><span data-stu-id="ad7b5-267">Minimum permission level</span></span>](https://docs.microsoft.com/outlook/add-ins/understanding-outlook-add-in-permissions)| <span data-ttu-id="ad7b5-268">ReadItem</span><span class="sxs-lookup"><span data-stu-id="ad7b5-268">ReadItem</span></span>|
|[<span data-ttu-id="ad7b5-269">适用的 Outlook 模式</span><span class="sxs-lookup"><span data-stu-id="ad7b5-269">Applicable Outlook mode</span></span>](https://docs.microsoft.com/outlook/add-ins/#extension-points)| <span data-ttu-id="ad7b5-270">撰写或阅读​</span><span class="sxs-lookup"><span data-stu-id="ad7b5-270">Compose or read</span></span>|

##### <a name="returns"></a><span data-ttu-id="ad7b5-271">返回：</span><span class="sxs-lookup"><span data-stu-id="ad7b5-271">Returns:</span></span>

<span data-ttu-id="ad7b5-272">返回：LocalClientTime[ ](/javascript/api/outlook_1_6/office.LocalClientTime)</span><span class="sxs-lookup"><span data-stu-id="ad7b5-272">Type: [LocalClientTime](/javascript/api/outlook_1_6/office.LocalClientTime)</span></span>

####  <a name="converttorestiditemid-restversion--string"></a><span data-ttu-id="ad7b5-273">convertToRestId(itemId, restVersion) → {String}</span><span class="sxs-lookup"><span data-stu-id="ad7b5-273">convertToRestId(itemId, restVersion) → {String}</span></span>

<span data-ttu-id="ad7b5-274">将适用 EWS 格式化的项目 ID 转换为 REST 格式。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-274">Converts an item ID formatted for EWS into REST format.</span></span>

> [!NOTE]
> <span data-ttu-id="ad7b5-275">在 Outlook for iOS 或 Outlook for Android 中不支持此方法。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-275">Note: This method is not supported in Outlook for iOS or Outlook for Android.</span></span>

<span data-ttu-id="ad7b5-p111">通过 EWS 或通过 `itemId` 属性检索的项目 ID 使用与 REST API 不同的格式（例如 [Outlook Mail API](https://docs.microsoft.com/previous-versions/office/office-365-api/api/version-2.0/mail-rest-operations) 或 [Microsoft Graph](http://graph.microsoft.io/)）。`convertToRestId` 方法将适用 EWS 格式化的 ID 转换为正确的 REST 格式。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-p111">Item IDs retrieved via EWS or via the `itemId` property use a different format than the format used by REST APIs (such as the [Outlook Mail API](https://docs.microsoft.com/previous-versions/office/office-365-api/api/version-2.0/mail-rest-operations) or the [Microsoft Graph](http://graph.microsoft.io/)). The `convertToRestId` method converts an EWS-formatted ID into the proper format for REST.</span></span>

##### <a name="parameters"></a><span data-ttu-id="ad7b5-278">参数：</span><span class="sxs-lookup"><span data-stu-id="ad7b5-278">Parameters:</span></span>

|<span data-ttu-id="ad7b5-279">名称</span><span class="sxs-lookup"><span data-stu-id="ad7b5-279">Name</span></span>| <span data-ttu-id="ad7b5-280">类型</span><span class="sxs-lookup"><span data-stu-id="ad7b5-280">Type</span></span>| <span data-ttu-id="ad7b5-281">说明</span><span class="sxs-lookup"><span data-stu-id="ad7b5-281">Description</span></span>|
|---|---|---|
|`itemId`| <span data-ttu-id="ad7b5-282">字符串</span><span class="sxs-lookup"><span data-stu-id="ad7b5-282">String</span></span>|<span data-ttu-id="ad7b5-283">适用于 Exchange Web 服务 (EWS) 进行格式化的项目 ID。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-283">An item ID formatted for Exchange Web Services (EWS)</span></span>|
|`restVersion`| [<span data-ttu-id="ad7b5-284">Office.MailboxEnums.RestVersion</span><span class="sxs-lookup"><span data-stu-id="ad7b5-284">Office.MailboxEnums.RestVersion</span></span>](/javascript/api/outlook_1_6/office.mailboxenums.restversion)|<span data-ttu-id="ad7b5-285">值指示转换的 ID 所使用的 Outlook REST API 版本。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-285">A value indicating the version of the Outlook REST API that the converted ID will be used with.</span></span>|

##### <a name="requirements"></a><span data-ttu-id="ad7b5-286">要求</span><span class="sxs-lookup"><span data-stu-id="ad7b5-286">Requirements</span></span>

|<span data-ttu-id="ad7b5-287">要求</span><span class="sxs-lookup"><span data-stu-id="ad7b5-287">Requirement</span></span>| <span data-ttu-id="ad7b5-288">值</span><span class="sxs-lookup"><span data-stu-id="ad7b5-288">Value</span></span>|
|---|---|
|[<span data-ttu-id="ad7b5-289">最低邮箱要求集版本</span><span class="sxs-lookup"><span data-stu-id="ad7b5-289">Minimum mailbox requirement set version</span></span>](/office/dev/add-ins/reference/requirement-sets/outlook-api-requirement-sets)| <span data-ttu-id="ad7b5-290">1.3</span><span class="sxs-lookup"><span data-stu-id="ad7b5-290">1.3</span></span>|
|[<span data-ttu-id="ad7b5-291">最低权限级别</span><span class="sxs-lookup"><span data-stu-id="ad7b5-291">Minimum permission level</span></span>](https://docs.microsoft.com/outlook/add-ins/understanding-outlook-add-in-permissions)| <span data-ttu-id="ad7b5-292">Restricted</span><span class="sxs-lookup"><span data-stu-id="ad7b5-292">Restricted</span></span>|
|[<span data-ttu-id="ad7b5-293">适用的 Outlook 模式</span><span class="sxs-lookup"><span data-stu-id="ad7b5-293">Applicable Outlook mode</span></span>](https://docs.microsoft.com/outlook/add-ins/#extension-points)| <span data-ttu-id="ad7b5-294">撰写或阅读​</span><span class="sxs-lookup"><span data-stu-id="ad7b5-294">Compose or read</span></span>|

##### <a name="returns"></a><span data-ttu-id="ad7b5-295">返回：</span><span class="sxs-lookup"><span data-stu-id="ad7b5-295">Returns:</span></span>

<span data-ttu-id="ad7b5-296">类型：String</span><span class="sxs-lookup"><span data-stu-id="ad7b5-296">Type: String</span></span>

##### <a name="example"></a><span data-ttu-id="ad7b5-297">示例</span><span class="sxs-lookup"><span data-stu-id="ad7b5-297">Example</span></span>

```
// Get the currently selected item's ID
var ewsId = Office.context.mailbox.item.itemId;

// Convert to a REST ID for the v2.0 version of the
// Outlook Mail API
var restId = Office.context.mailbox.convertToRestId(ewsId, Office.MailboxEnums.RestVersion.v2_0);
```

####  <a name="converttoutcclienttimeinput--date"></a><span data-ttu-id="ad7b5-298">convertToUtcClientTime(input) → {Date}</span><span class="sxs-lookup"><span data-stu-id="ad7b5-298">convertToUtcClientTime(input) → {Date}</span></span>

<span data-ttu-id="ad7b5-299">从包含时间信息的字典中获取 Date 对象。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-299">Gets a Date object from a dictionary containing time information.</span></span>

<span data-ttu-id="ad7b5-300">`convertToUtcClientTime` 方法将包含本地日期和时间的字典转换为包含与本地日期和时间对应的正确值的 Date 对象。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-300">The `convertToUtcClientTime` method converts a dictionary containing a local date and time to a Date object with the correct values for the local date and time.</span></span>

##### <a name="parameters"></a><span data-ttu-id="ad7b5-301">参数：</span><span class="sxs-lookup"><span data-stu-id="ad7b5-301">Parameters:</span></span>

|<span data-ttu-id="ad7b5-302">名称</span><span class="sxs-lookup"><span data-stu-id="ad7b5-302">Name</span></span>| <span data-ttu-id="ad7b5-303">类型</span><span class="sxs-lookup"><span data-stu-id="ad7b5-303">Type</span></span>| <span data-ttu-id="ad7b5-304">说明</span><span class="sxs-lookup"><span data-stu-id="ad7b5-304">Description</span></span>|
|---|---|---|
|`input`| [<span data-ttu-id="ad7b5-305">LocalClientTime</span><span class="sxs-lookup"><span data-stu-id="ad7b5-305">LocalClientTime</span></span>](/javascript/api/outlook_1_6/office.LocalClientTime)|<span data-ttu-id="ad7b5-306">要转换的本地时间值。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-306">The local time value to convert.</span></span>|

##### <a name="requirements"></a><span data-ttu-id="ad7b5-307">要求</span><span class="sxs-lookup"><span data-stu-id="ad7b5-307">Requirements</span></span>

|<span data-ttu-id="ad7b5-308">要求</span><span class="sxs-lookup"><span data-stu-id="ad7b5-308">Requirement</span></span>| <span data-ttu-id="ad7b5-309">值</span><span class="sxs-lookup"><span data-stu-id="ad7b5-309">Value</span></span>|
|---|---|
|[<span data-ttu-id="ad7b5-310">最低邮箱要求集版本</span><span class="sxs-lookup"><span data-stu-id="ad7b5-310">Minimum mailbox requirement set version</span></span>](/office/dev/add-ins/reference/requirement-sets/outlook-api-requirement-sets)| <span data-ttu-id="ad7b5-311">1.0</span><span class="sxs-lookup"><span data-stu-id="ad7b5-311">1.0</span></span>|
|[<span data-ttu-id="ad7b5-312">最低权限级别</span><span class="sxs-lookup"><span data-stu-id="ad7b5-312">Minimum permission level</span></span>](https://docs.microsoft.com/outlook/add-ins/understanding-outlook-add-in-permissions)| <span data-ttu-id="ad7b5-313">ReadItem</span><span class="sxs-lookup"><span data-stu-id="ad7b5-313">ReadItem</span></span>|
|[<span data-ttu-id="ad7b5-314">适用的 Outlook 模式</span><span class="sxs-lookup"><span data-stu-id="ad7b5-314">Applicable Outlook mode</span></span>](https://docs.microsoft.com/outlook/add-ins/#extension-points)| <span data-ttu-id="ad7b5-315">撰写或阅读​</span><span class="sxs-lookup"><span data-stu-id="ad7b5-315">Compose or read</span></span>|

##### <a name="returns"></a><span data-ttu-id="ad7b5-316">返回：</span><span class="sxs-lookup"><span data-stu-id="ad7b5-316">Returns:</span></span>

<span data-ttu-id="ad7b5-317">以UTC格式表示时间的 Date 对象</span><span class="sxs-lookup"><span data-stu-id="ad7b5-317">A Date object with the time expressed in UTC.</span></span>

<dl class="param-type"><span data-ttu-id="ad7b5-318">

<dt>类型</dt>

</span><span class="sxs-lookup"><span data-stu-id="ad7b5-318">

<dt>Type</dt>

</span></span><dd><span data-ttu-id="ad7b5-319">Date</span><span class="sxs-lookup"><span data-stu-id="ad7b5-319">Date</span></span></dd>

</dl>

####  <a name="displayappointmentformitemid"></a><span data-ttu-id="ad7b5-320">displayAppointmentForm(itemId)</span><span class="sxs-lookup"><span data-stu-id="ad7b5-320">displayAppointmentForm(itemId)</span></span>

<span data-ttu-id="ad7b5-321">显示现有日历约会。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-321">Displays an existing calendar appointment.</span></span>

> [!NOTE]
> <span data-ttu-id="ad7b5-322">在 Outlook for iOS 或 Outlook for Android 中不支持此方法。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-322">Note: This method is not supported in Outlook for iOS or Outlook for Android.</span></span>

<span data-ttu-id="ad7b5-323">`displayAppointmentForm` 方法将在桌面新窗口中或移动设备对话框中打开现有的日历约会。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-323">The `displayAppointmentForm` method opens an existing calendar appointment in a new window on the desktop or in a dialog box on mobile devices.</span></span>

<span data-ttu-id="ad7b5-p112">在 Outlook for Mac 中，您可以使用此方法来显示非重复性的单个约会，或显示重复系列中的主约会，但无法显示该系列的实例。这是因为在 Outlook for Mac 中，无法访问定期系列实例的属性（包括项目 ID）。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-p112">In Outlook for Mac, you can use this method to display a single appointment that is not part of a recurring series, or the master appointment of a recurring series, but you cannot display an instance of the series. This is because in Outlook for Mac, you cannot access the properties (including the item ID) of instances of a recurring series.</span></span>

<span data-ttu-id="ad7b5-326">在 Outlook Web App 中，此方法仅在窗体正文小于或等于 32KB 字符数时，才会打开指定的窗体。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-326">In Outlook Web App, this method opens the specified form only if the body of the form is less than or equal to 32KB number of characters.</span></span>

<span data-ttu-id="ad7b5-327">如果指定的项目标识符没有识别现有约会，将在客户端计算机或设备上打开一个空白窗格，并且不会返回错误消息。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-327">If the specified item identifier does not identify an existing appointment, a blank pane opens on the client computer or device, and no error message will be returned.</span></span>

##### <a name="parameters"></a><span data-ttu-id="ad7b5-328">参数：</span><span class="sxs-lookup"><span data-stu-id="ad7b5-328">Parameters:</span></span>

|<span data-ttu-id="ad7b5-329">名称</span><span class="sxs-lookup"><span data-stu-id="ad7b5-329">Name</span></span>| <span data-ttu-id="ad7b5-330">类型</span><span class="sxs-lookup"><span data-stu-id="ad7b5-330">Type</span></span>| <span data-ttu-id="ad7b5-331">说明</span><span class="sxs-lookup"><span data-stu-id="ad7b5-331">Description</span></span>|
|---|---|---|
|`itemId`| <span data-ttu-id="ad7b5-332">String</span><span class="sxs-lookup"><span data-stu-id="ad7b5-332">String</span></span>|<span data-ttu-id="ad7b5-333">现有日历约会的 Exchange Web 服务 (EWS) 标识符。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-333">The Exchange Web Services (EWS) identifier for an existing calendar appointment.</span></span>|

##### <a name="requirements"></a><span data-ttu-id="ad7b5-334">要求</span><span class="sxs-lookup"><span data-stu-id="ad7b5-334">Requirements</span></span>

|<span data-ttu-id="ad7b5-335">要求</span><span class="sxs-lookup"><span data-stu-id="ad7b5-335">Requirement</span></span>| <span data-ttu-id="ad7b5-336">值</span><span class="sxs-lookup"><span data-stu-id="ad7b5-336">Value</span></span>|
|---|---|
|[<span data-ttu-id="ad7b5-337">最低邮箱要求集版本</span><span class="sxs-lookup"><span data-stu-id="ad7b5-337">Minimum mailbox requirement set version</span></span>](/office/dev/add-ins/reference/requirement-sets/outlook-api-requirement-sets)| <span data-ttu-id="ad7b5-338">1.0</span><span class="sxs-lookup"><span data-stu-id="ad7b5-338">1.0</span></span>|
|[<span data-ttu-id="ad7b5-339">最低权限级别</span><span class="sxs-lookup"><span data-stu-id="ad7b5-339">Minimum permission level</span></span>](https://docs.microsoft.com/outlook/add-ins/understanding-outlook-add-in-permissions)| <span data-ttu-id="ad7b5-340">ReadItem</span><span class="sxs-lookup"><span data-stu-id="ad7b5-340">ReadItem</span></span>|
|[<span data-ttu-id="ad7b5-341">适用的 Outlook 模式</span><span class="sxs-lookup"><span data-stu-id="ad7b5-341">Applicable Outlook mode</span></span>](https://docs.microsoft.com/outlook/add-ins/#extension-points)| <span data-ttu-id="ad7b5-342">撰写或阅读​</span><span class="sxs-lookup"><span data-stu-id="ad7b5-342">Compose or read</span></span>|

##### <a name="example"></a><span data-ttu-id="ad7b5-343">示例</span><span class="sxs-lookup"><span data-stu-id="ad7b5-343">Example</span></span>

```
Office.context.mailbox.displayAppointmentForm(appointmentId);
```

####  <a name="displaymessageformitemid"></a><span data-ttu-id="ad7b5-344">displayMessageForm(itemId)</span><span class="sxs-lookup"><span data-stu-id="ad7b5-344">displayMessageForm(itemId)</span></span>

<span data-ttu-id="ad7b5-345">显示一封现有邮件。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-345">Displays an existing message.</span></span>

> [!NOTE]
> <span data-ttu-id="ad7b5-346">在 Outlook for iOS 或 Outlook for Android 中不支持此方法。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-346">Note: This method is not supported in Outlook for iOS or Outlook for Android.</span></span>

<span data-ttu-id="ad7b5-347">在 Outlook Web App 中，`displayMessageForm` 方法将在桌面新窗口中或移动设备对话框中打开一封现有邮件。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-347">The `displayMessageForm` method opens an existing message in a new window on the desktop or in a dialog box on mobile devices.</span></span>

<span data-ttu-id="ad7b5-348">在 Outlook Web App 中，此方法仅在窗体正文小于或等于 32 KB 字符数时，才会打开指定的窗体。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-348">In Outlook Web App, this method opens the specified form only if the body of the form is less than or equal to 32 KB number of characters.</span></span>

<span data-ttu-id="ad7b5-349">如果指定的项标识符未识别现有消息，则客户端计算机上不会显示任何消息，并且也不会返回错误消息。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-349">If the specified item identifier does not identify an existing message, no message will be displayed on the client computer, and no error message will be returned.</span></span>

<span data-ttu-id="ad7b5-p113">请勿使用 `displayMessageForm` 配合 `itemId` 表示约会。 使用 `displayAppointmentForm` 方法显示一个现有约会， 并 `displayNewAppointmentForm` 显示一个创建新约会的窗体。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-p113">Do not use the `displayMessageForm` with an `itemId` that represents an appointment. Use the `displayAppointmentForm` method to display an existing appointment, and `displayNewAppointmentForm` to display a form to create a new appointment.</span></span>

##### <a name="parameters"></a><span data-ttu-id="ad7b5-352">参数：</span><span class="sxs-lookup"><span data-stu-id="ad7b5-352">Parameters:</span></span>

|<span data-ttu-id="ad7b5-353">名称</span><span class="sxs-lookup"><span data-stu-id="ad7b5-353">Name</span></span>| <span data-ttu-id="ad7b5-354">类型</span><span class="sxs-lookup"><span data-stu-id="ad7b5-354">Type</span></span>| <span data-ttu-id="ad7b5-355">说明</span><span class="sxs-lookup"><span data-stu-id="ad7b5-355">Description</span></span>|
|---|---|---|
|`itemId`| <span data-ttu-id="ad7b5-356">String</span><span class="sxs-lookup"><span data-stu-id="ad7b5-356">String</span></span>|<span data-ttu-id="ad7b5-357">现有邮件的 Exchange Web 服务 (EWS) 标识符。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-357">The Exchange Web Services (EWS) identifier for an existing message.</span></span>|

##### <a name="requirements"></a><span data-ttu-id="ad7b5-358">要求</span><span class="sxs-lookup"><span data-stu-id="ad7b5-358">Requirements</span></span>

|<span data-ttu-id="ad7b5-359">要求</span><span class="sxs-lookup"><span data-stu-id="ad7b5-359">Requirement</span></span>| <span data-ttu-id="ad7b5-360">值</span><span class="sxs-lookup"><span data-stu-id="ad7b5-360">Value</span></span>|
|---|---|
|[<span data-ttu-id="ad7b5-361">最低邮箱要求集版本</span><span class="sxs-lookup"><span data-stu-id="ad7b5-361">Minimum mailbox requirement set version</span></span>](/office/dev/add-ins/reference/requirement-sets/outlook-api-requirement-sets)| <span data-ttu-id="ad7b5-362">1.0</span><span class="sxs-lookup"><span data-stu-id="ad7b5-362">1.0</span></span>|
|[<span data-ttu-id="ad7b5-363">最低权限级别</span><span class="sxs-lookup"><span data-stu-id="ad7b5-363">Minimum permission level</span></span>](https://docs.microsoft.com/outlook/add-ins/understanding-outlook-add-in-permissions)| <span data-ttu-id="ad7b5-364">ReadItem</span><span class="sxs-lookup"><span data-stu-id="ad7b5-364">ReadItem</span></span>|
|[<span data-ttu-id="ad7b5-365">适用的 Outlook 模式</span><span class="sxs-lookup"><span data-stu-id="ad7b5-365">Applicable Outlook mode</span></span>](https://docs.microsoft.com/outlook/add-ins/#extension-points)| <span data-ttu-id="ad7b5-366">撰写或阅读​</span><span class="sxs-lookup"><span data-stu-id="ad7b5-366">Compose or read</span></span>|

##### <a name="example"></a><span data-ttu-id="ad7b5-367">示例</span><span class="sxs-lookup"><span data-stu-id="ad7b5-367">Example</span></span>

```
Office.context.mailbox.displayMessageForm(messageId);
```

#### <a name="displaynewappointmentformparameters"></a><span data-ttu-id="ad7b5-368">displayNewAppointmentForm(parameters)</span><span class="sxs-lookup"><span data-stu-id="ad7b5-368">displayNewAppointmentForm(parameters)</span></span>

<span data-ttu-id="ad7b5-369">显示用于新建日历约会的窗体。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-369">Displays a form for creating a new calendar appointment.</span></span>

> [!NOTE]
> <span data-ttu-id="ad7b5-370">在 Outlook for iOS 或 Outlook for Android 中不支持此方法。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-370">Note: This method is not supported in Outlook for iOS or Outlook for Android.</span></span>

<span data-ttu-id="ad7b5-p114">`displayNewAppointmentForm` 方法打开可让用户新建约会或会议的窗体。如果指定了参数，将使用参数的内容自动填充参数内容。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-p114">The `displayNewAppointmentForm` method opens a form that enables the user to create a new appointment or meeting. If parameters are specified, the appointment form fields are automatically populated with the contents of the parameters.</span></span>

<span data-ttu-id="ad7b5-p115">在 Outlook Web App 和适用于设备的 OWA 中，此方法始终显示包含与会者字段的窗体。如果你未将任何与会者指定为输入参数，该方法将显示为一个包含**保存**按钮的窗体。如果已指定与会者，窗体将包含与会者和“**发送**”按钮。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-p115">In Outlook Web App and OWA for Devices, this method always displays a form with an attendees field. If you do not specify any attendees as input arguments, the method displays a form with a **Save** button. If you have specified attendees, the form would include the attendees and a **Send** button.</span></span>

<span data-ttu-id="ad7b5-p116">在 Outlook 富客户端和 Outlook RT 中，如果在 `requiredAttendees`、`optionalAttendees` 或 `resources` 参数中指定任何与会者或资源，此方法将显示会议窗体，其中包含一个“**发送**”按钮。如果未指定任何收件人，此方法将显示一个包含“**保存并关闭**”按钮的约会窗体。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-p116">In the Outlook rich client and Outlook RT, if you specify any attendees or resources in the `requiredAttendees`, `optionalAttendees`, or `resources` parameter, this method displays a meeting form with a **Send** button. If you don't specify any recipients, this method displays an appointment form with a **Save & Close** button.</span></span>

<span data-ttu-id="ad7b5-378">如果任何参数超过指定大小限制，或者指定了未知参数名称，则会引发异常。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-378">If any of the parameters exceed the specified size limits, or if an unknown parameter name is specified, an exception is thrown.</span></span>

##### <a name="parameters"></a><span data-ttu-id="ad7b5-379">参数：</span><span class="sxs-lookup"><span data-stu-id="ad7b5-379">Parameters:</span></span>

> [!NOTE]
> <span data-ttu-id="ad7b5-380">所有参数都是可选参数。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-380">Note: All parameters are optional.</span></span>

|<span data-ttu-id="ad7b5-381">名称</span><span class="sxs-lookup"><span data-stu-id="ad7b5-381">Name</span></span>| <span data-ttu-id="ad7b5-382">类型</span><span class="sxs-lookup"><span data-stu-id="ad7b5-382">Type</span></span>| <span data-ttu-id="ad7b5-383">说明</span><span class="sxs-lookup"><span data-stu-id="ad7b5-383">Description</span></span>|
|---|---|---|
| `parameters` | <span data-ttu-id="ad7b5-384">Object</span><span class="sxs-lookup"><span data-stu-id="ad7b5-384">Object</span></span> | <span data-ttu-id="ad7b5-385">描述新约会的参数字典。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-385">A dictionary of parameters describing the new appointment.</span></span> |
| `parameters.requiredAttendees` | <span data-ttu-id="ad7b5-386">数组.&lt;字符串&gt; | 数组.&lt;[EmailAddressDetails](/javascript/api/outlook_1_6/office.emailaddressdetails)&gt;</span><span class="sxs-lookup"><span data-stu-id="ad7b5-386">Array.&lt;String&gt; &#124; Array.&lt;[EmailAddressDetails](/javascript/api/outlook_1_6/office.emailaddressdetails)&gt;</span></span> | <span data-ttu-id="ad7b5-p117">包含电子邮件地址的字符串数组或包含约会的每个必需与会者 `EmailAddressDetails` 对象的数组。数组限制为最多 100 个条目。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-p117">An array of strings containing the email addresses or an array containing an `EmailAddressDetails` object for each of the required attendees for the appointment. The array is limited to a maximum of 100 entries.</span></span> |
| `parameters.optionalAttendees` | <span data-ttu-id="ad7b5-389">数组.&lt;字符串&gt; | 数组.&lt;[EmailAddressDetails](/javascript/api/outlook_1_6/office.emailaddressdetails)&gt;</span><span class="sxs-lookup"><span data-stu-id="ad7b5-389">Array.&lt;String&gt; &#124; Array.&lt;[EmailAddressDetails](/javascript/api/outlook_1_6/office.emailaddressdetails)&gt;</span></span> | <span data-ttu-id="ad7b5-p118">包含电子邮件地址的字符串数组或包含约会的每个可选与会者 `EmailAddressDetails` 对象的数组。数组限制为最多 100 个条目。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-p118">An array of strings containing the email addresses or an array containing an `EmailAddressDetails` object for each of the optional attendees for the appointment. The array is limited to a maximum of 100 entries.</span></span> |
| `parameters.start` | <span data-ttu-id="ad7b5-392">Date</span><span class="sxs-lookup"><span data-stu-id="ad7b5-392">Date</span></span> | <span data-ttu-id="ad7b5-393">指定约会开始日期和时间的 `Date` 对象。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-393">A `Date` object specifying the start date and time of the appointment.</span></span> |
| `parameters.end` | <span data-ttu-id="ad7b5-394">Date</span><span class="sxs-lookup"><span data-stu-id="ad7b5-394">Date</span></span> | <span data-ttu-id="ad7b5-395">指定约会的结束日期和时间的 `Date` 对象。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-395">A `Date` object specifying the end date and time of the appointment.</span></span> |
| `parameters.location` | <span data-ttu-id="ad7b5-396">字符串</span><span class="sxs-lookup"><span data-stu-id="ad7b5-396">String</span></span> | <span data-ttu-id="ad7b5-p119">包含约会位置的字符串。字符串长度限制为最多 255 个字符。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-p119">A string containing the location of the appointment. The string is limited to a maximum of 255 characters.</span></span> |
| `parameters.resources` | <span data-ttu-id="ad7b5-399">数组.&lt;字符串&gt;</span><span class="sxs-lookup"><span data-stu-id="ad7b5-399">Array.&lt;String&gt;</span></span> | <span data-ttu-id="ad7b5-p120">包含约会所需资源的字符串数组。数组限制为最多 100 个条目。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-p120">An array of strings containing the resources required for the appointment. The array is limited to a maximum of 100 entries.</span></span> |
| `parameters.subject` | <span data-ttu-id="ad7b5-402">字符串</span><span class="sxs-lookup"><span data-stu-id="ad7b5-402">String</span></span> | <span data-ttu-id="ad7b5-p121">包含约会主题的字符串。字符串长度限制为最多 255 个字符。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-p121">A string containing the subject of the appointment. The string is limited to a maximum of 255 characters.</span></span> |
| `parameters.body` | <span data-ttu-id="ad7b5-405">String</span><span class="sxs-lookup"><span data-stu-id="ad7b5-405">String</span></span> | <span data-ttu-id="ad7b5-p122">约会的正文。正文内容限制为最大 32 KB。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-p122">The body of the appointment. The body content is limited to a maximum size of 32 KB.</span></span> |

##### <a name="requirements"></a><span data-ttu-id="ad7b5-408">要求</span><span class="sxs-lookup"><span data-stu-id="ad7b5-408">Requirements</span></span>

|<span data-ttu-id="ad7b5-409">要求</span><span class="sxs-lookup"><span data-stu-id="ad7b5-409">Requirement</span></span>| <span data-ttu-id="ad7b5-410">值</span><span class="sxs-lookup"><span data-stu-id="ad7b5-410">Value</span></span>|
|---|---|
|[<span data-ttu-id="ad7b5-411">最低邮箱要求集版本</span><span class="sxs-lookup"><span data-stu-id="ad7b5-411">Minimum mailbox requirement set version</span></span>](/office/dev/add-ins/reference/requirement-sets/outlook-api-requirement-sets)| <span data-ttu-id="ad7b5-412">1.0</span><span class="sxs-lookup"><span data-stu-id="ad7b5-412">1.0</span></span>|
|[<span data-ttu-id="ad7b5-413">最低权限级别</span><span class="sxs-lookup"><span data-stu-id="ad7b5-413">Minimum permission level</span></span>](https://docs.microsoft.com/outlook/add-ins/understanding-outlook-add-in-permissions)| <span data-ttu-id="ad7b5-414">ReadItem</span><span class="sxs-lookup"><span data-stu-id="ad7b5-414">ReadItem</span></span>|
|[<span data-ttu-id="ad7b5-415">适用的 Outlook 模式</span><span class="sxs-lookup"><span data-stu-id="ad7b5-415">Applicable Outlook mode</span></span>](https://docs.microsoft.com/outlook/add-ins/#extension-points)| <span data-ttu-id="ad7b5-416">阅读</span><span class="sxs-lookup"><span data-stu-id="ad7b5-416">Read</span></span>|

##### <a name="example"></a><span data-ttu-id="ad7b5-417">示例</span><span class="sxs-lookup"><span data-stu-id="ad7b5-417">Example</span></span>

```
var start = new Date();
var end = new Date();
end.setHours(start.getHours() + 1);

Office.context.mailbox.displayNewAppointmentForm(
  {
    requiredAttendees: ['bob@contoso.com'],
    optionalAttendees: ['sam@contoso.com'],
    start: start,
    end: end,
    location: 'Home',
    resources: ['projector@contoso.com'],
    subject: 'meeting',
    body: 'Hello World!'
  });
```

#### <a name="displaynewmessageformparameters"></a><span data-ttu-id="ad7b5-418">displayNewMessageForm(parameters)</span><span class="sxs-lookup"><span data-stu-id="ad7b5-418">displayNewMessageForm(parameters)</span></span>

<span data-ttu-id="ad7b5-419">显示用于新建邮件的窗体。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-419">Displays a form for creating a new message.</span></span>

<span data-ttu-id="ad7b5-420">`displayNewMessageForm` 方法将打开可让用户新建邮件的窗体。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-420">The `displayNewMessageForm` method opens a form that enables the user to create a new message.</span></span> <span data-ttu-id="ad7b5-421">如果指定了参数，将使用参数的内容自动填充邮件窗体字段。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-421">If parameters are specified, the message form fields are automatically populated with the contents of the parameters.</span></span>

<span data-ttu-id="ad7b5-422">如果任何参数超过指定大小限制，或者指定了未知参数名称，则会引发异常。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-422">If any of the parameters exceed the specified size limits, or if an unknown parameter name is specified, an exception is thrown.</span></span>

##### <a name="parameters"></a><span data-ttu-id="ad7b5-423">参数：</span><span class="sxs-lookup"><span data-stu-id="ad7b5-423">Parameters:</span></span>

> [!NOTE]
> <span data-ttu-id="ad7b5-424">所有参数都是可选参数。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-424">Note: All parameters are optional.</span></span>

|<span data-ttu-id="ad7b5-425">名称</span><span class="sxs-lookup"><span data-stu-id="ad7b5-425">Name</span></span>| <span data-ttu-id="ad7b5-426">类型</span><span class="sxs-lookup"><span data-stu-id="ad7b5-426">Type</span></span>| <span data-ttu-id="ad7b5-427">说明</span><span class="sxs-lookup"><span data-stu-id="ad7b5-427">Description</span></span>|
|---|---|---|
| `parameters` | <span data-ttu-id="ad7b5-428">Object</span><span class="sxs-lookup"><span data-stu-id="ad7b5-428">Object</span></span> | <span data-ttu-id="ad7b5-429">描述新邮件的参数字典。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-429">A dictionary of parameters describing the new message.</span></span> |
| `parameters.toRecipients` | <span data-ttu-id="ad7b5-430">数组.&lt;字符串&gt; | 数组.&lt;[EmailAddressDetails](/javascript/api/outlook_1_6/office.emailaddressdetails)&gt;</span><span class="sxs-lookup"><span data-stu-id="ad7b5-430">Array.&lt;String&gt; &#124; Array.&lt;[EmailAddressDetails](/javascript/api/outlook_1_6/office.emailaddressdetails)&gt;</span></span> | <span data-ttu-id="ad7b5-431">包含电子邮件地址的字符串数组或包含收件人行上每个收件人的 `EmailAddressDetails` 对象的数组。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-431">An array of strings containing the email addresses or an array containing an `EmailAddressDetails` object for each of the recipients on the To line.</span></span> <span data-ttu-id="ad7b5-432">数组限制为最多 100 个条目。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-432">The array is limited to a maximum of 100 entries.</span></span> |
| `parameters.ccRecipients` | <span data-ttu-id="ad7b5-433">数组.&lt;字符串&gt; | 数组.&lt;[EmailAddressDetails](/javascript/api/outlook_1_6/office.emailaddressdetails)&gt;</span><span class="sxs-lookup"><span data-stu-id="ad7b5-433">Array.&lt;String&gt; &#124; Array.&lt;[EmailAddressDetails](/javascript/api/outlook_1_6/office.emailaddressdetails)&gt;</span></span> | <span data-ttu-id="ad7b5-434">包含电子邮件地址的字符串数组或包含抄送行上每个收件人的 `EmailAddressDetails` 对象的数组。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-434">An array of strings containing the email addresses or an array containing an `EmailAddressDetails` object for each of the recipients on the Cc line.</span></span> <span data-ttu-id="ad7b5-435">数组限制为最多 100 个条目。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-435">The array is limited to a maximum of 100 entries.</span></span> |
| `parameters.bccRecipients` | <span data-ttu-id="ad7b5-436">数组.&lt;字符串&gt; | 数组.&lt;[EmailAddressDetails](/javascript/api/outlook_1_6/office.emailaddressdetails)&gt;</span><span class="sxs-lookup"><span data-stu-id="ad7b5-436">Array.&lt;String&gt; &#124; Array.&lt;[EmailAddressDetails](/javascript/api/outlook_1_6/office.emailaddressdetails)&gt;</span></span> | <span data-ttu-id="ad7b5-437">包含电子邮件地址的字符串数组或包含密件抄送行上每个收件人的 `EmailAddressDetails` 对象的数组。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-437">An array of strings containing the email addresses or an array containing an `EmailAddressDetails` object for each of the recipients on the Bcc line.</span></span> <span data-ttu-id="ad7b5-438">数组限制为最多 100 个条目。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-438">The array is limited to a maximum of 100 entries.</span></span> |
| `parameters.subject` | <span data-ttu-id="ad7b5-439">字符串</span><span class="sxs-lookup"><span data-stu-id="ad7b5-439">String</span></span> | <span data-ttu-id="ad7b5-440">包含邮件主题的字符串。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-440">A string containing the subject of the message.</span></span> <span data-ttu-id="ad7b5-441">字符串长度限制为最多 255 个字符。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-441">The string is limited to a maximum of 255 characters.</span></span> |
| `parameters.htmlBody` | <span data-ttu-id="ad7b5-442">字符串</span><span class="sxs-lookup"><span data-stu-id="ad7b5-442">String</span></span> | <span data-ttu-id="ad7b5-443">邮件的 HTML 正文。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-443">The HTML body of the message.</span></span> <span data-ttu-id="ad7b5-444">正文内容限制为最大 32 KB。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-444">The body content is limited to a maximum size of 32 KB.</span></span> |
| `parameters.attachments` | <span data-ttu-id="ad7b5-445">Array.&lt;Object&gt;</span><span class="sxs-lookup"><span data-stu-id="ad7b5-445">Array.&lt;Object&gt;</span></span> | <span data-ttu-id="ad7b5-446">JSON 对象（是文件或项目附件）的数组。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-446">An array of JSON objects that are either file or item attachments.</span></span> |
| `parameters.attachments.type` | <span data-ttu-id="ad7b5-447">字符串</span><span class="sxs-lookup"><span data-stu-id="ad7b5-447">String</span></span> | <span data-ttu-id="ad7b5-p129">指示附件的类型。必须是文件附件的 `file` 或项目附件的 `item` 。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-p129">Indicates the type of attachment. Must be `file` for a file attachment or `item` for an item attachment.</span></span> |
| `parameters.attachments.name` | <span data-ttu-id="ad7b5-450">字符串</span><span class="sxs-lookup"><span data-stu-id="ad7b5-450">String</span></span> | <span data-ttu-id="ad7b5-451">一个包含附件的名称的字符串，最多包含 255 个字符。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-451">A string that contains the name of the attachment, up to 255 characters in length.</span></span>|
| `parameters.attachments.url` | <span data-ttu-id="ad7b5-452">字符串</span><span class="sxs-lookup"><span data-stu-id="ad7b5-452">String</span></span> | <span data-ttu-id="ad7b5-p130">仅在 `type` 设置为 `file` 时才使用。文件位置的 URI。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-p130">Only used if `type` is set to `file`. The URI of the location for the file.</span></span> |
| `parameters.attachments.isInline` | <span data-ttu-id="ad7b5-455">Boolean</span><span class="sxs-lookup"><span data-stu-id="ad7b5-455">Boolean</span></span> | <span data-ttu-id="ad7b5-p131">仅在 `type` 设置为 `file` 时才使用。如果为 `true`，表示将在邮件正文中嵌入显示附件，并且不应在附件列表中显示。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-p131">Only used if `type` is set to `file`. If `true`, indicates that the attachment will be shown inline in the message body, and should not be displayed in the attachment list.</span></span> |
| `parameters.attachments.itemId` | <span data-ttu-id="ad7b5-458">字符串</span><span class="sxs-lookup"><span data-stu-id="ad7b5-458">String</span></span> | <span data-ttu-id="ad7b5-459">仅在 `type` 设置为 `item` 时才使用。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-459">Only used if `type` is set to `item`.</span></span> <span data-ttu-id="ad7b5-460">你想要附加到新邮件的现有电子邮件的 EWS 项目 id。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-460">The EWS item id of the existing e-mail you want to attach to the new message.</span></span> <span data-ttu-id="ad7b5-461">字符串最多达 100 个字符。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-461">This is a string up to 100 characters.</span></span> |


##### <a name="requirements"></a><span data-ttu-id="ad7b5-462">要求</span><span class="sxs-lookup"><span data-stu-id="ad7b5-462">Requirements</span></span>

|<span data-ttu-id="ad7b5-463">要求</span><span class="sxs-lookup"><span data-stu-id="ad7b5-463">Requirement</span></span>| <span data-ttu-id="ad7b5-464">值</span><span class="sxs-lookup"><span data-stu-id="ad7b5-464">Value</span></span>|
|---|---|
|[<span data-ttu-id="ad7b5-465">最低的邮箱要求集版本</span><span class="sxs-lookup"><span data-stu-id="ad7b5-465">Minimum mailbox requirement set version</span></span>](/office/dev/add-ins/reference/requirement-sets/outlook-api-requirement-sets)| <span data-ttu-id="ad7b5-466">1.6</span><span class="sxs-lookup"><span data-stu-id="ad7b5-466">-16</span></span> |
|[<span data-ttu-id="ad7b5-467">最低权限级别</span><span class="sxs-lookup"><span data-stu-id="ad7b5-467">Minimum permission level</span></span>](https://docs.microsoft.com/outlook/add-ins/understanding-outlook-add-in-permissions)| <span data-ttu-id="ad7b5-468">ReadItem</span><span class="sxs-lookup"><span data-stu-id="ad7b5-468">ReadItem</span></span>|
|[<span data-ttu-id="ad7b5-469">适用的 Outlook 模式</span><span class="sxs-lookup"><span data-stu-id="ad7b5-469">Applicable Outlook mode</span></span>](https://docs.microsoft.com/outlook/add-ins/#extension-points)| <span data-ttu-id="ad7b5-470">阅读</span><span class="sxs-lookup"><span data-stu-id="ad7b5-470">Read</span></span>|

##### <a name="example"></a><span data-ttu-id="ad7b5-471">示例</span><span class="sxs-lookup"><span data-stu-id="ad7b5-471">Example</span></span>

```
Office.context.mailbox.displayNewMessageForm(
  {
    toRecipients: Office.context.mailbox.item.to, // Copy the To line from current item
    ccRecipients: ['sam@contoso.com'],
    subject: 'Outlook add-ins are cool!',
    htmlBody: 'Hello <b>World</b>!<br/><img src="cid:image.png"></i>',
    attachments: [
      {
        type: 'file',
        name: 'image.png',
        url: 'http://contoso.com/image.png',
        isInline: true
      }
    ]
  });
```

#### <a name="getcallbacktokenasyncoptions-callback"></a><span data-ttu-id="ad7b5-472">getCallbackTokenAsync([选项] 回调)</span><span class="sxs-lookup"><span data-stu-id="ad7b5-472">getCallbackTokenAsync([options], callback)</span></span>

<span data-ttu-id="ad7b5-473">获取一个包含用于调用 REST API 或 Exchange Web 服务令牌的字符串。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-473">Gets a string that contains a token used to call REST APIs or Exchange Web Services.</span></span>

<span data-ttu-id="ad7b5-p133">`getCallbackTokenAsync` 方法进行异步调用，从托管用户邮箱的 Exchange Server 获取不透明令牌。回调令牌的生存期为 5 分钟。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-p133">The `getCallbackTokenAsync` method makes an asynchronous call to get an opaque token from the Exchange Server that hosts the user's mailbox. The lifetime of the callback token is 5 minutes.</span></span>

> [!NOTE]
> <span data-ttu-id="ad7b5-476">建议加载项尽可能地使用 REST API 而不是 Exchange Web 服务。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-476">Note: It is recommended that add-ins use the REST APIs instead of Exchange Web Services whenever possible.</span></span> 

<span data-ttu-id="ad7b5-477">**REST 令牌**</span><span class="sxs-lookup"><span data-stu-id="ad7b5-477">**REST Tokens**</span></span>

<span data-ttu-id="ad7b5-p134">请求 REST 令牌 (`options.isRest = true`) 时，生成的令牌将无法对 Exchange Web 服务调用进行身份验证。令牌的作用域限制为对当前项及其附件的只读访问，除非加载项在其清单中指定了 [`ReadWriteMailbox`](https://docs.microsoft.com/outlook/add-ins/understanding-outlook-add-in-permissions#readwritemailbox-permission) 权限。如果指定了 `ReadWriteMailbox` 权限，则生成的令牌将授予对邮件、日历和联系人的读/写权限，包括发送邮件的功能。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-p134">When a REST token is requested (`options.isRest = true`), the resulting token will not work to authenticate Exchange Web Services calls. The token will be limited in scope to read-only access to the current item and its attachments, unless the add-in has specified the [`ReadWriteMailbox`](https://docs.microsoft.com/outlook/add-ins/understanding-outlook-add-in-permissions#readwritemailbox-permission) permission in its manifest. If the `ReadWriteMailbox` permission is specified, the resulting token will grant read/write access to mail, calendar, and contacts, including the ability to send mail.</span></span>

<span data-ttu-id="ad7b5-481">在进行 REST API 调用时，外接程序应使用 `restUrl` 属性来确定要使用的正确 URL。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-481">The add-in should use the `restUrl` property to determine the correct URL to use when making REST API calls.</span></span>

<span data-ttu-id="ad7b5-482">**EWS 令牌**</span><span class="sxs-lookup"><span data-stu-id="ad7b5-482">**EWS Tokens**</span></span>

<span data-ttu-id="ad7b5-p135">请求 EWS 令牌 (`options.isRest = false`) 时，生成的令牌将无法对 REST API 调用进行身份验证。令牌的作用域限制为访问当前项。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-p135">When an EWS token is requested (`options.isRest = false`), the resulting token will not work to authenticate REST API calls. The token will be limited in scope to accessing the current item.</span></span>

<span data-ttu-id="ad7b5-485">加载项应使用 `ewsUrl` 属性来确定进行 EWS 调用时要使用的正确 URL。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-485">The add-in should use the `ewsUrl` property to determine the correct URL to use when making EWS calls.</span></span>

##### <a name="parameters"></a><span data-ttu-id="ad7b5-486">参数：</span><span class="sxs-lookup"><span data-stu-id="ad7b5-486">Parameters:</span></span>

|<span data-ttu-id="ad7b5-487">名称</span><span class="sxs-lookup"><span data-stu-id="ad7b5-487">Name</span></span>| <span data-ttu-id="ad7b5-488">类型</span><span class="sxs-lookup"><span data-stu-id="ad7b5-488">Type</span></span>| <span data-ttu-id="ad7b5-489">属性</span><span class="sxs-lookup"><span data-stu-id="ad7b5-489">Attributes</span></span>| <span data-ttu-id="ad7b5-490">说明</span><span class="sxs-lookup"><span data-stu-id="ad7b5-490">Description</span></span>|
|---|---|---|---|
| `options` | <span data-ttu-id="ad7b5-491">Object</span><span class="sxs-lookup"><span data-stu-id="ad7b5-491">Object</span></span> | <span data-ttu-id="ad7b5-492">&lt;optional&gt;</span><span class="sxs-lookup"><span data-stu-id="ad7b5-492">&lt;optional&gt;</span></span> | <span data-ttu-id="ad7b5-493">包含一个或多个以下属性的对象文本。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-493">An object literal that contains one or more of the following properties.</span></span> |
| `options.isRest` | <span data-ttu-id="ad7b5-494">Boolean</span><span class="sxs-lookup"><span data-stu-id="ad7b5-494">Boolean</span></span> |  <span data-ttu-id="ad7b5-495">&lt;optional&gt;</span><span class="sxs-lookup"><span data-stu-id="ad7b5-495">&lt;optional&gt;</span></span> | <span data-ttu-id="ad7b5-p136">确定所提供的令牌是否将用于 Outlook REST API 或 Exchange Web 服务。默认值为 `false`。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-p136">Determines if the token provided will be used for the Outlook REST APIs or Exchange Web Services. Default value is `false`.</span></span> |
| `options.asyncContext` | <span data-ttu-id="ad7b5-498">Object</span><span class="sxs-lookup"><span data-stu-id="ad7b5-498">Object</span></span> |  <span data-ttu-id="ad7b5-499">&lt;optional&gt;</span><span class="sxs-lookup"><span data-stu-id="ad7b5-499">&lt;optional&gt;</span></span> | <span data-ttu-id="ad7b5-500">传递给异步方法的任何状态数据。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-500">Any state data that is passed to the asynchronous method.</span></span> |
|`callback`| <span data-ttu-id="ad7b5-501">function</span><span class="sxs-lookup"><span data-stu-id="ad7b5-501">function</span></span>||<span data-ttu-id="ad7b5-p137">方法完成后，通过单个参数调用 `callback` 参数中传递的函数， `asyncResult`, 是一个 [`AsyncResult`](/javascript/api/office/office.asyncresult) 对象。令牌以 `asyncResult.value` 属性字符串形式提供。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-p137">When the method completes, the function passed in the `callback` parameter is called with a single parameter, `asyncResult`, which is an [`AsyncResult`](/javascript/api/office/office.asyncresult) object. The token is provided as a string in the `asyncResult.value` property.</span></span>|

##### <a name="requirements"></a><span data-ttu-id="ad7b5-504">要求</span><span class="sxs-lookup"><span data-stu-id="ad7b5-504">Requirements</span></span>

|<span data-ttu-id="ad7b5-505">要求</span><span class="sxs-lookup"><span data-stu-id="ad7b5-505">Requirement</span></span>| <span data-ttu-id="ad7b5-506">值</span><span class="sxs-lookup"><span data-stu-id="ad7b5-506">Value</span></span>|
|---|---|
|[<span data-ttu-id="ad7b5-507">最低邮箱要求集版本</span><span class="sxs-lookup"><span data-stu-id="ad7b5-507">Minimum mailbox requirement set version</span></span>](/office/dev/add-ins/reference/requirement-sets/outlook-api-requirement-sets)| <span data-ttu-id="ad7b5-508">1.5</span><span class="sxs-lookup"><span data-stu-id="ad7b5-508">1.5</span></span> |
|[<span data-ttu-id="ad7b5-509">最低权限级别</span><span class="sxs-lookup"><span data-stu-id="ad7b5-509">Minimum permission level</span></span>](https://docs.microsoft.com/outlook/add-ins/understanding-outlook-add-in-permissions)| <span data-ttu-id="ad7b5-510">ReadItem</span><span class="sxs-lookup"><span data-stu-id="ad7b5-510">ReadItem</span></span>|
|[<span data-ttu-id="ad7b5-511">适用的 Outlook 模式</span><span class="sxs-lookup"><span data-stu-id="ad7b5-511">Applicable Outlook mode</span></span>](https://docs.microsoft.com/outlook/add-ins/#extension-points)| <span data-ttu-id="ad7b5-512">撰写和阅读</span><span class="sxs-lookup"><span data-stu-id="ad7b5-512">Compose and read</span></span>|

##### <a name="example"></a><span data-ttu-id="ad7b5-513">示例</span><span class="sxs-lookup"><span data-stu-id="ad7b5-513">Example</span></span>

```js
function getCallbackToken() {
  var options = {
    isRest: true,
    asyncContext: { message: 'Hello World!' }
  };

  Office.context.mailbox.getCallbackTokenAsync(options, cb);
}

function cb(asyncResult) {
  var token = asyncResult.value;
}
```

#### <a name="getcallbacktokenasynccallback-usercontext"></a><span data-ttu-id="ad7b5-514">getCallbackTokenAsync(回调, [userContext])</span><span class="sxs-lookup"><span data-stu-id="ad7b5-514">getCallbackTokenAsync(callback, [userContext])</span></span>

<span data-ttu-id="ad7b5-515">获取一个字符串，其中包含用于从 Exchange Server 获取附件或项目的令牌。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-515">Gets a string that contains a token used to get an attachment or item from an Exchange Server.</span></span>

<span data-ttu-id="ad7b5-p138">`getCallbackTokenAsync` 方法进行异步调用，从托管用户邮箱的 Exchange Server 获取不透明令牌。回调令牌的生存期为 5 分钟。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-p138">The `getCallbackTokenAsync` method makes an asynchronous call to get an opaque token from the Exchange Server that hosts the user's mailbox. The lifetime of the callback token is 5 minutes.</span></span>

<span data-ttu-id="ad7b5-p139">可以将令牌和附件标识符或项标识符传递至第三方系统。第三方系统使用令牌作为持有者身份验证令牌调用 Exchange Web 服务 (EWS) [GetAttachment](https://docs.microsoft.com/exchange/client-developer/web-service-reference/getattachment-operation) 或 [GetItem](https://docs.microsoft.com/exchange/client-developer/web-service-reference/getitem-operation)，以返回附件或项目。例如，可以创建远程服务来[获取选定项目中的附件](https://docs.microsoft.com/outlook/add-ins/get-attachments-of-an-outlook-item)。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-p139">You can pass the token and an attachment identifier or item identifier to a third-party system. The third-party system uses the token as a bearer authorization token to call the Exchange Web Services (EWS) [GetAttachment](https://docs.microsoft.com/exchange/client-developer/web-service-reference/getattachment-operation) or [GetItem](https://docs.microsoft.com/exchange/client-developer/web-service-reference/getitem-operation) operation to return an attachment or item. For example, you can create a remote service to [get attachments from the selected item](https://docs.microsoft.com/outlook/add-ins/get-attachments-of-an-outlook-item).</span></span>

<span data-ttu-id="ad7b5-521">应用必须在其清单中指定拥有 **ReadItem** 权限，才能在阅读模式中调用 `getCallbackTokenAsync` 方法。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-521">Your app must have the **ReadItem** permission specified in its manifest to call the `getCallbackTokenAsync` method in read mode.</span></span>

<span data-ttu-id="ad7b5-p140">在撰写模式中，必须调用 [`saveAsync`](Office.context.mailbox.item.md#saveasyncoptions-callback) 方法来获取传递给 `getCallbackTokenAsync` 方法的项目标识符。应用必须具有调用 `saveAsync` 方法的 **ReadWriteItem** 权限。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-p140">In compose mode you must call the [`saveAsync`](Office.context.mailbox.item.md#saveasyncoptions-callback) method to get an item identifier to pass to the `getCallbackTokenAsync` method. Your app must have **ReadWriteItem** permissions to call the `saveAsync` method.</span></span>

##### <a name="parameters"></a><span data-ttu-id="ad7b5-524">参数：</span><span class="sxs-lookup"><span data-stu-id="ad7b5-524">Parameters:</span></span>

|<span data-ttu-id="ad7b5-525">名称</span><span class="sxs-lookup"><span data-stu-id="ad7b5-525">Name</span></span>| <span data-ttu-id="ad7b5-526">类型</span><span class="sxs-lookup"><span data-stu-id="ad7b5-526">Type</span></span>| <span data-ttu-id="ad7b5-527">属性</span><span class="sxs-lookup"><span data-stu-id="ad7b5-527">Attributes</span></span>| <span data-ttu-id="ad7b5-528">说明</span><span class="sxs-lookup"><span data-stu-id="ad7b5-528">Description</span></span>|
|---|---|---|---|
|`callback`| <span data-ttu-id="ad7b5-529">function</span><span class="sxs-lookup"><span data-stu-id="ad7b5-529">function</span></span>||<span data-ttu-id="ad7b5-p141">方法完成后，通过单个参数 `asyncResult`（这是一个 [`AsyncResult`](/javascript/api/office/office.asyncresult) 对象）调用 `callback` 参数中传递的函数。令牌作为 `asyncResult.value` 属性中的字符串提供。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-p141">When the method completes, the function passed in the `callback` parameter is called with a single parameter, `asyncResult`, which is an [`AsyncResult`](/javascript/api/office/office.asyncresult) object. The token is provided as a string in the `asyncResult.value` property.</span></span>|
|`userContext`| <span data-ttu-id="ad7b5-532">Object</span><span class="sxs-lookup"><span data-stu-id="ad7b5-532">Object</span></span>| <span data-ttu-id="ad7b5-533">&lt;optional&gt;</span><span class="sxs-lookup"><span data-stu-id="ad7b5-533">&lt;optional&gt;</span></span>|<span data-ttu-id="ad7b5-534">传递给异步方法的任何状态数据。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-534">Any state data that is passed to the asynchronous method.</span></span>|

##### <a name="requirements"></a><span data-ttu-id="ad7b5-535">要求</span><span class="sxs-lookup"><span data-stu-id="ad7b5-535">Requirements</span></span>

|<span data-ttu-id="ad7b5-536">要求</span><span class="sxs-lookup"><span data-stu-id="ad7b5-536">Requirement</span></span>| <span data-ttu-id="ad7b5-537">值</span><span class="sxs-lookup"><span data-stu-id="ad7b5-537">Value</span></span>|
|---|---|
|[<span data-ttu-id="ad7b5-538">最低邮箱要求集版本</span><span class="sxs-lookup"><span data-stu-id="ad7b5-538">Minimum mailbox requirement set version</span></span>](/office/dev/add-ins/reference/requirement-sets/outlook-api-requirement-sets)| <span data-ttu-id="ad7b5-539">1.3</span><span class="sxs-lookup"><span data-stu-id="ad7b5-539">1.3</span></span>|
|[<span data-ttu-id="ad7b5-540">最低权限级别</span><span class="sxs-lookup"><span data-stu-id="ad7b5-540">Minimum permission level</span></span>](https://docs.microsoft.com/outlook/add-ins/understanding-outlook-add-in-permissions)| <span data-ttu-id="ad7b5-541">ReadItem</span><span class="sxs-lookup"><span data-stu-id="ad7b5-541">ReadItem</span></span>|
|[<span data-ttu-id="ad7b5-542">适用的 Outlook 模式</span><span class="sxs-lookup"><span data-stu-id="ad7b5-542">Applicable Outlook mode</span></span>](https://docs.microsoft.com/outlook/add-ins/#extension-points)| <span data-ttu-id="ad7b5-543">撰写和阅读</span><span class="sxs-lookup"><span data-stu-id="ad7b5-543">Compose and read</span></span>|

##### <a name="example"></a><span data-ttu-id="ad7b5-544">示例</span><span class="sxs-lookup"><span data-stu-id="ad7b5-544">Example</span></span>

```js
function getCallbackToken() {
  Office.context.mailbox.getCallbackTokenAsync(cb);
}

function cb(asyncResult) {
  var token = asyncResult.value;
}
```

####  <a name="getuseridentitytokenasynccallback-usercontext"></a><span data-ttu-id="ad7b5-545">getUserIdentityTokenAsync(callback, [userContext])</span><span class="sxs-lookup"><span data-stu-id="ad7b5-545">getUserIdentityTokenAsync(callback, [userContext])</span></span>

<span data-ttu-id="ad7b5-546">获取用于标识用户和 Office 加载项的令牌。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-546">Gets a token identifying the user and the Office Add-in.</span></span>

<span data-ttu-id="ad7b5-547">`getUserIdentityTokenAsync` 方法返回可以用于标识和[在第三方系统上验证加载项和用户](https://docs.microsoft.com/outlook/add-ins/authentication)的令牌。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-547">The `getUserIdentityTokenAsync` method returns a token that you can use to identify and [authenticate the add-in and user with a third-party system](https://docs.microsoft.com/outlook/add-ins/authentication).</span></span>

##### <a name="parameters"></a><span data-ttu-id="ad7b5-548">参数：</span><span class="sxs-lookup"><span data-stu-id="ad7b5-548">Parameters:</span></span>

|<span data-ttu-id="ad7b5-549">名称</span><span class="sxs-lookup"><span data-stu-id="ad7b5-549">Name</span></span>| <span data-ttu-id="ad7b5-550">类型</span><span class="sxs-lookup"><span data-stu-id="ad7b5-550">Type</span></span>| <span data-ttu-id="ad7b5-551">属性</span><span class="sxs-lookup"><span data-stu-id="ad7b5-551">Attributes</span></span>| <span data-ttu-id="ad7b5-552">说明</span><span class="sxs-lookup"><span data-stu-id="ad7b5-552">Description</span></span>|
|---|---|---|---|
|`callback`| <span data-ttu-id="ad7b5-553">function</span><span class="sxs-lookup"><span data-stu-id="ad7b5-553">function</span></span>||<span data-ttu-id="ad7b5-554">方法完成后，使用单个参数 `asyncResult`（一个 [`AsyncResult`](/javascript/api/office/office.asyncresult)对象）调用在 `callback` 参数中传递的函数。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-554">When the method completes, the function passed in the `callback` parameter is called with a single parameter, `asyncResult`, which is an [`AsyncResult`](/javascript/api/office/office.asyncresult) object.</span></span><br/><br/><span data-ttu-id="ad7b5-555">令牌作为 `asyncResult.value` 属性中的字符串提供。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-555">The token is provided as a string in the `asyncResult.value` property.</span></span>|
|`userContext`| <span data-ttu-id="ad7b5-556">Object</span><span class="sxs-lookup"><span data-stu-id="ad7b5-556">Object</span></span>| <span data-ttu-id="ad7b5-557">&lt;optional&gt;</span><span class="sxs-lookup"><span data-stu-id="ad7b5-557">&lt;optional&gt;</span></span>|<span data-ttu-id="ad7b5-558">传递给异步方法的任何状态数据。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-558">Any state data that is passed to the asynchronous method.</span></span>|

##### <a name="requirements"></a><span data-ttu-id="ad7b5-559">要求</span><span class="sxs-lookup"><span data-stu-id="ad7b5-559">Requirements</span></span>

|<span data-ttu-id="ad7b5-560">要求</span><span class="sxs-lookup"><span data-stu-id="ad7b5-560">Requirement</span></span>| <span data-ttu-id="ad7b5-561">值</span><span class="sxs-lookup"><span data-stu-id="ad7b5-561">Value</span></span>|
|---|---|
|[<span data-ttu-id="ad7b5-562">最低邮箱要求集版本</span><span class="sxs-lookup"><span data-stu-id="ad7b5-562">Minimum mailbox requirement set version</span></span>](/office/dev/add-ins/reference/requirement-sets/outlook-api-requirement-sets)| <span data-ttu-id="ad7b5-563">1.0</span><span class="sxs-lookup"><span data-stu-id="ad7b5-563">1.0</span></span>|
|[<span data-ttu-id="ad7b5-564">最低权限级别</span><span class="sxs-lookup"><span data-stu-id="ad7b5-564">Minimum permission level</span></span>](https://docs.microsoft.com/outlook/add-ins/understanding-outlook-add-in-permissions)| <span data-ttu-id="ad7b5-565">ReadItem</span><span class="sxs-lookup"><span data-stu-id="ad7b5-565">ReadItem</span></span>|
|[<span data-ttu-id="ad7b5-566">适用的 Outlook 模式</span><span class="sxs-lookup"><span data-stu-id="ad7b5-566">Applicable Outlook mode</span></span>](https://docs.microsoft.com/outlook/add-ins/#extension-points)| <span data-ttu-id="ad7b5-567">撰写或阅读​</span><span class="sxs-lookup"><span data-stu-id="ad7b5-567">Compose or read</span></span>|

##### <a name="example"></a><span data-ttu-id="ad7b5-568">示例</span><span class="sxs-lookup"><span data-stu-id="ad7b5-568">Example</span></span>

```js
function getIdentityToken() {
  Office.context.mailbox.getUserIdentityTokenAsync(cb);
}

function cb(asyncResult) {
  var token = asyncResult.value;
}
```

####  <a name="makeewsrequestasyncdata-callback-usercontext"></a><span data-ttu-id="ad7b5-569">makeEwsRequestAsync(data, callback, [userContext])</span><span class="sxs-lookup"><span data-stu-id="ad7b5-569">makeEwsRequestAsync(data, callback, [userContext])</span></span>

<span data-ttu-id="ad7b5-570">向托管用户邮箱的 Exchange 服务器上的 Exchange Web 服务 (EWS) 发出异步请求。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-570">Makes an asynchronous request to an Exchange Web Services (EWS) service on the Exchange server that hosts the user’s mailbox.</span></span>

> [!NOTE]
> <span data-ttu-id="ad7b5-571">在以下方案中不支持此方法。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-571">This method is not supported in the following scenarios.</span></span>
> - <span data-ttu-id="ad7b5-572">在 Outlook for iOS 或 Outlook for Android 中</span><span class="sxs-lookup"><span data-stu-id="ad7b5-572">In Outlook for iOS or Outlook for Android</span></span>
> - <span data-ttu-id="ad7b5-573">在 Gmail 邮箱中加载加载项时</span><span class="sxs-lookup"><span data-stu-id="ad7b5-573">When the add-in is loaded in a Gmail mailbox</span></span>
> 
> <span data-ttu-id="ad7b5-574">在这些情况下, 加载项应转而[使用 REST API](https://docs.microsoft.com/outlook/add-ins/use-rest-api) 访问用户的邮箱。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-574">In these cases, add-ins should [use REST APIs](https://docs.microsoft.com/outlook/add-ins/use-rest-api) to access the user's mailbox instead.</span></span>

<span data-ttu-id="ad7b5-575">`makeEwsRequestAsync` 方法代表加载项向 Exchange 发送 EWS 请求。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-575">The `makeEwsRequestAsync` method sends an EWS request on behalf of the add-in to Exchange.</span></span> <span data-ttu-id="ad7b5-576">有关支持的 EWS 操作列表，请参阅[从 Outlook 加载项调用 Web 服务](https://docs.microsoft.com/outlook/add-ins/web-services#ews-operations-that-add-ins-support) 。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-576">See [Call web services from an Outlook add-in](https://docs.microsoft.com/outlook/add-ins/web-services#ews-operations-that-add-ins-support) for a list of the supported EWS operations.</span></span>

<span data-ttu-id="ad7b5-577">不能通过 `makeEwsRequestAsync` 方法请求与“文件夹”关联的项。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-577">You cannot request Folder Associated Items with the `makeEwsRequestAsync` method.</span></span>

<span data-ttu-id="ad7b5-578">XML 请求必须指定 UTF-8 编码。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-578">The XML request must specify UTF-8 encoding.</span></span>

```
<?xml version="1.0" encoding="utf-8"?>
```

<span data-ttu-id="ad7b5-p143">加载项必须具有 **ReadWriteMailbox** 权限才能使用 `makeEwsRequestAsync` 方法。欲知使用 **ReadWriteMailbox** 权限和可使用 `makeEwsRequestAsync` 方法调用 EWS 操作的信息，请参阅[指定邮件加载项访问用户邮箱的权限](https://docs.microsoft.com/outlook/add-ins/understanding-outlook-add-in-permissions)。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-p143">Your add-in must have the **ReadWriteMailbox** permission to use the `makeEwsRequestAsync` method. For information about using the **ReadWriteMailbox** permission and the EWS operations that you can call with the `makeEwsRequestAsync` method, see [Specify permissions for mail add-in access to the user's mailbox](https://docs.microsoft.com/outlook/add-ins/understanding-outlook-add-in-permissions).</span></span>

> [!NOTE]
> <span data-ttu-id="ad7b5-581">服务器管理员必须在 Client Access Server EWS 目录上将 `OAuthAuthentication` 设置为 true，`makeEwsRequestAsync` 方法才能发出 EWS 请求。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-581">NOTE: The server administrator must set `OAuthAuthentication` to true on the Client Access Server EWS directory to enable the `makeEwsRequestAsync` method to make EWS requests.</span></span>

##### <a name="version-differences"></a><span data-ttu-id="ad7b5-582">版本差异</span><span class="sxs-lookup"><span data-stu-id="ad7b5-582">Version differences</span></span>

<span data-ttu-id="ad7b5-583">当你在较 15.0.4535.1004 版本更早的 Outlook 版本中运行的邮件应用程序中使用 `makeEwsRequestAsync` 方法时，应当将编码值设置为 `ISO-8859-1`。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-583">When you use the `makeEwsRequestAsync` method in mail apps running in Outlook versions earlier than version 15.0.4535.1004, you should set the encoding value to `ISO-8859-1`.</span></span>

```
<?xml version="1.0" encoding="iso-8859-1"?>
```

<span data-ttu-id="ad7b5-p144">当邮件应用在 Outlook 网页版中运行时，不需要设置编码值。可以通过使用 mailbox.diagnostics.hostName 属性来确定邮件应用是正在 Outlook 中运行还是在 Outlook 网页版中运行。可以通过使用 mailbox.diagnostics.hostVersion 属性来确定正在运行的 Outlook 版本。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-p144">You do not need to set the encoding value when your mail app is running in Outlook on the web. You can determine whether your mail app is running in Outlook or Outlook on the web by using the mailbox.diagnostics.hostName property. You can determine what version of Outlook is running by using the mailbox.diagnostics.hostVersion property.</span></span>

##### <a name="parameters"></a><span data-ttu-id="ad7b5-587">参数：</span><span class="sxs-lookup"><span data-stu-id="ad7b5-587">Parameters:</span></span>

|<span data-ttu-id="ad7b5-588">名称</span><span class="sxs-lookup"><span data-stu-id="ad7b5-588">Name</span></span>| <span data-ttu-id="ad7b5-589">类型</span><span class="sxs-lookup"><span data-stu-id="ad7b5-589">Type</span></span>| <span data-ttu-id="ad7b5-590">属性</span><span class="sxs-lookup"><span data-stu-id="ad7b5-590">Attributes</span></span>| <span data-ttu-id="ad7b5-591">说明</span><span class="sxs-lookup"><span data-stu-id="ad7b5-591">Description</span></span>|
|---|---|---|---|
|`data`| <span data-ttu-id="ad7b5-592">字符串</span><span class="sxs-lookup"><span data-stu-id="ad7b5-592">String</span></span>||<span data-ttu-id="ad7b5-593">EWS 请求。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-593">The EWS request.</span></span>|
|`callback`| <span data-ttu-id="ad7b5-594">function</span><span class="sxs-lookup"><span data-stu-id="ad7b5-594">function</span></span>||<span data-ttu-id="ad7b5-595">方法完成后，使用单个参数 `callback`（一个 [`asyncResult`](/javascript/api/office/office.asyncresult) 对象）调用在 `AsyncResult` 参数中传递的函数。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-595">When the method completes, the function passed in the `callback` parameter is called with a single parameter, `asyncResult`, which is an [`AsyncResult`](/javascript/api/office/office.asyncresult) object.</span></span><br/><br/><span data-ttu-id="ad7b5-596">EWS 调用的 XML 结果作为 `asyncResult.value` 属性中的字符串提供。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-596">The XML result of the EWS call is provided as a string in the `asyncResult.value` property.</span></span> <span data-ttu-id="ad7b5-597">如果结果的大小超过 1 MB，将转而返回一条错误消息。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-597">If the result exceeds 1 MB in size, an error message is returned instead.| | Object| optional|Any state data that is passed to the asynchronous method.|</span></span>|
|`userContext`| <span data-ttu-id="ad7b5-598">Object</span><span class="sxs-lookup"><span data-stu-id="ad7b5-598">Object</span></span>| <span data-ttu-id="ad7b5-599">&lt;optional&gt;</span><span class="sxs-lookup"><span data-stu-id="ad7b5-599">&lt;optional&gt;</span></span>|<span data-ttu-id="ad7b5-600">传递给异步方法的任何状态数据。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-600">Any state data that is passed to the asynchronous method.</span></span>|

##### <a name="requirements"></a><span data-ttu-id="ad7b5-601">要求</span><span class="sxs-lookup"><span data-stu-id="ad7b5-601">Requirements</span></span>

|<span data-ttu-id="ad7b5-602">要求</span><span class="sxs-lookup"><span data-stu-id="ad7b5-602">Requirement</span></span>| <span data-ttu-id="ad7b5-603">值</span><span class="sxs-lookup"><span data-stu-id="ad7b5-603">Value</span></span>|
|---|---|
|[<span data-ttu-id="ad7b5-604">最低邮箱要求集版本</span><span class="sxs-lookup"><span data-stu-id="ad7b5-604">Minimum mailbox requirement set version</span></span>](/office/dev/add-ins/reference/requirement-sets/outlook-api-requirement-sets)| <span data-ttu-id="ad7b5-605">1.0</span><span class="sxs-lookup"><span data-stu-id="ad7b5-605">1.0</span></span>|
|[<span data-ttu-id="ad7b5-606">最低权限级别</span><span class="sxs-lookup"><span data-stu-id="ad7b5-606">Minimum permission level</span></span>](https://docs.microsoft.com/outlook/add-ins/understanding-outlook-add-in-permissions)| <span data-ttu-id="ad7b5-607">ReadWriteMailbox</span><span class="sxs-lookup"><span data-stu-id="ad7b5-607">ReadWriteMailbox</span></span>|
|[<span data-ttu-id="ad7b5-608">适用的 Outlook 模式</span><span class="sxs-lookup"><span data-stu-id="ad7b5-608">Applicable Outlook mode</span></span>](https://docs.microsoft.com/outlook/add-ins/#extension-points)| <span data-ttu-id="ad7b5-609">撰写或阅读​</span><span class="sxs-lookup"><span data-stu-id="ad7b5-609">Compose or read</span></span>|

##### <a name="example"></a><span data-ttu-id="ad7b5-610">示例</span><span class="sxs-lookup"><span data-stu-id="ad7b5-610">Example</span></span>

<span data-ttu-id="ad7b5-611">下面的示例调用 `makeEwsRequestAsync`  以使用  `GetItem` 操作获取项目的主题。</span><span class="sxs-lookup"><span data-stu-id="ad7b5-611">The following example calls `makeEwsRequestAsync` to use the `GetItem` operation to get the subject of an item.</span></span>

```js
function getSubjectRequest(id) {
   // Return a GetItem operation request for the subject of the specified item.
   var request =
    '<?xml version="1.0" encoding="utf-8"?>' +
    '<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"' +
    '               xmlns:xsd="http://www.w3.org/2001/XMLSchema"' +
    '               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"' +
    '               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">' +
    '  <soap:Header>' +
    '    <RequestServerVersion Version="Exchange2013" xmlns="http://schemas.microsoft.com/exchange/services/2006/types" soap:mustUnderstand="0" />' +
    '  </soap:Header>' +
    '  <soap:Body>' +
    '    <GetItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">' +
    '      <ItemShape>' +
    '        <t:BaseShape>IdOnly</t:BaseShape>' +
    '        <t:AdditionalProperties>' +
    '            <t:FieldURI FieldURI="item:Subject"/>' +
    '        </t:AdditionalProperties>' +
    '      </ItemShape>' +
    '      <ItemIds><t:ItemId Id="' + id + '"/></ItemIds>' +
    '    </GetItem>' +
    '  </soap:Body>' +
    '</soap:Envelope>';

   return request;
}

function sendRequest() {
   // Create a local variable that contains the mailbox.
   Office.context.mailbox.makeEwsRequestAsync(
    getSubjectRequest(mailbox.item.itemId), callback);
}

function callback(asyncResult)  {
   var result = asyncResult.value;
   var context = asyncResult.asyncContext;

   // Process the returned response here.
}
```