---
title: UpdateItem 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateItem
api_type:
- schema
ms.assetid: 5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4
description: UpdateItem 操作用于修改 Exchange 存储中现有项的属性。
ms.openlocfilehash: c001b7656862144023e9704cb04e6b4c0030f9df
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459389"
---
# <a name="updateitem-operation"></a><span data-ttu-id="b5907-103">UpdateItem 操作</span><span class="sxs-lookup"><span data-stu-id="b5907-103">UpdateItem operation</span></span>

<span data-ttu-id="b5907-104">**UpdateItem**操作用于修改 Exchange 存储中现有项的属性。</span><span class="sxs-lookup"><span data-stu-id="b5907-104">The **UpdateItem** operation is used to modify the properties of an existing item in the Exchange store.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b5907-105">备注</span><span class="sxs-lookup"><span data-stu-id="b5907-105">Remarks</span></span>

<span data-ttu-id="b5907-106">您可以对项目执行三个基本的更新操作。</span><span class="sxs-lookup"><span data-stu-id="b5907-106">You can perform three basic update actions on an item.</span></span> <span data-ttu-id="b5907-107">下表列出了您可以执行的操作。</span><span class="sxs-lookup"><span data-stu-id="b5907-107">The following table lists the actions that you can perform.</span></span>
  
|<span data-ttu-id="b5907-108">**操作**</span><span class="sxs-lookup"><span data-stu-id="b5907-108">**Action**</span></span>|<span data-ttu-id="b5907-109">**说明**</span><span class="sxs-lookup"><span data-stu-id="b5907-109">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b5907-110">Append</span><span class="sxs-lookup"><span data-stu-id="b5907-110">Append</span></span>  <br/> |<span data-ttu-id="b5907-111">将数据添加到现有属性。</span><span class="sxs-lookup"><span data-stu-id="b5907-111">Adds data to an existing property.</span></span> <span data-ttu-id="b5907-112">此操作将保留当前数据。</span><span class="sxs-lookup"><span data-stu-id="b5907-112">This action preserves the current data.</span></span> <span data-ttu-id="b5907-113">Append 不应用于所有属性。</span><span class="sxs-lookup"><span data-stu-id="b5907-113">Append does not apply to all properties.</span></span>  <br/> |
|<span data-ttu-id="b5907-114">Set</span><span class="sxs-lookup"><span data-stu-id="b5907-114">Set</span></span>  <br/> |<span data-ttu-id="b5907-115">如果属性包含数据，则替换属性的数据; 或者，如果属性不存在，则创建属性并设置其值。</span><span class="sxs-lookup"><span data-stu-id="b5907-115">Replaces data for a property if the property contains data, or creates the property and sets its value if the property does not exist.</span></span> <span data-ttu-id="b5907-116">Set 操作仅适用于可写属性。</span><span class="sxs-lookup"><span data-stu-id="b5907-116">The set action is only applicable to writable properties.</span></span>  <br/> |
|<span data-ttu-id="b5907-117">Delete</span><span class="sxs-lookup"><span data-stu-id="b5907-117">Delete</span></span>  <br/> |<span data-ttu-id="b5907-118">从项目中删除属性。</span><span class="sxs-lookup"><span data-stu-id="b5907-118">Removes a property from an item.</span></span> <span data-ttu-id="b5907-119">这与将属性设置为空值不同。</span><span class="sxs-lookup"><span data-stu-id="b5907-119">This differs from setting a property to an empty value.</span></span> <span data-ttu-id="b5907-120">完成此操作后，该项目的属性不存在。</span><span class="sxs-lookup"><span data-stu-id="b5907-120">When this action is finished, the property does not exist for the item.</span></span> <span data-ttu-id="b5907-121">删除仅适用于可写属性。</span><span class="sxs-lookup"><span data-stu-id="b5907-121">Delete is only applicable to writable properties.</span></span>  <br/> |
   
<span data-ttu-id="b5907-122">**UpdateItem**调用可用于修改一个或多个项目，以及每个项目上的一个或多个属性。</span><span class="sxs-lookup"><span data-stu-id="b5907-122">An **UpdateItem** call can be used to modify one or more items, and one or more properties on each item.</span></span> <span data-ttu-id="b5907-123">[ItemChanges](itemchanges.md)元素包含要作为此调用的一部分执行的所有修改。</span><span class="sxs-lookup"><span data-stu-id="b5907-123">The [ItemChanges](itemchanges.md) element contains all the modifications that are to be performed as part of this call.</span></span> <span data-ttu-id="b5907-124">[ItemChange](itemchange.md)元素（ [ItemChanges](itemchanges.md)元素的子元素）表示要对单个项目执行的修改。</span><span class="sxs-lookup"><span data-stu-id="b5907-124">The [ItemChange](itemchange.md) element, a child of the [ItemChanges](itemchanges.md) element, represents the modifications to be performed on a single item.</span></span> <span data-ttu-id="b5907-125">[ItemChange](itemchange.md)元素包含一组可对单个项目执行的更新操作。</span><span class="sxs-lookup"><span data-stu-id="b5907-125">The [ItemChange](itemchange.md) element contains a set of update actions that can be performed on a single item.</span></span> <span data-ttu-id="b5907-126">这些更改包含在[Updates （Item）](updates-item.md)元素中。</span><span class="sxs-lookup"><span data-stu-id="b5907-126">These changes are contained in the [Updates (Item)](updates-item.md) element.</span></span> <span data-ttu-id="b5907-127">[ItemId](itemid.md)元素标识要更新的项。</span><span class="sxs-lookup"><span data-stu-id="b5907-127">The [ItemId](itemid.md) element identifies the item to update.</span></span> <span data-ttu-id="b5907-128">若要更新一个项的多个属性，必须为需要更新的每个属性提供[SetItemField](setitemfield.md)、 [AppendToItemField](appendtoitemfield.md)或[DeleteItemField](deleteitemfield.md) 。</span><span class="sxs-lookup"><span data-stu-id="b5907-128">To update more than one property on an item, a [SetItemField](setitemfield.md), [AppendToItemField](appendtoitemfield.md), or [DeleteItemField](deleteitemfield.md) must be provided for each property that requires the update.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b5907-129">将按指定的顺序应用更新操作。</span><span class="sxs-lookup"><span data-stu-id="b5907-129">Update actions are applied in the order in which they are specified.</span></span> 
  
<span data-ttu-id="b5907-130">对于每个更改，您必须指定要更改的属性的路径以及该项目的表示形式的新值。</span><span class="sxs-lookup"><span data-stu-id="b5907-130">For each change, you have to specify the path of the property to change and a representation of that item with its new value.</span></span> <span data-ttu-id="b5907-131">删除操作略有不同，只有应删除的属性的路径是必需的。</span><span class="sxs-lookup"><span data-stu-id="b5907-131">The delete action is slightly different in that only the path of the property that should be deleted is required.</span></span> <span data-ttu-id="b5907-132">对于 set 和 append 操作，指定的路径必须引用在项目表示形式中设置的同一属性。</span><span class="sxs-lookup"><span data-stu-id="b5907-132">For set and append actions, the path that is specified must refer to the same property that is being set in the item representation.</span></span> <span data-ttu-id="b5907-133">如果这些不同，将返回错误。</span><span class="sxs-lookup"><span data-stu-id="b5907-133">If these differ, an error will be returned.</span></span>
  
<span data-ttu-id="b5907-134">**UpdateItem**操作可以设置 Exchange 存储项的[开始](start.md)和[结束](end-ex15websvcsotherref.md)时间。</span><span class="sxs-lookup"><span data-stu-id="b5907-134">The **UpdateItem** operation can set the [Start](start.md) and [End ](end-ex15websvcsotherref.md) time of an Exchange store item.</span></span> <span data-ttu-id="b5907-135">在**UpdateItem**请求中，可以设置[开始](start.md)时间，而不同时设置[结束](end-ex15websvcsotherref.md)时间。</span><span class="sxs-lookup"><span data-stu-id="b5907-135">In an **UpdateItem** request, the [Start](start.md) time can be set without also setting the [End ](end-ex15websvcsotherref.md) time.</span></span> <span data-ttu-id="b5907-136">如果[开始](start.md)时间晚于[结束](end-ex15websvcsotherref.md)时间，这可能会导致错误。</span><span class="sxs-lookup"><span data-stu-id="b5907-136">This can cause an error if the [Start](start.md) time is later than the [End ](end-ex15websvcsotherref.md) time.</span></span> <span data-ttu-id="b5907-137">请注意，客户端应用程序必须调整[开始](start.md)时间更改的[结束](end-ex15websvcsotherref.md)时间，以便保留持续时间。</span><span class="sxs-lookup"><span data-stu-id="b5907-137">Be aware that client applications must adjust the [End ](end-ex15websvcsotherref.md) time when the [Start](start.md) time is changed in order to preserve the duration.</span></span> 
  
<span data-ttu-id="b5907-138">如果将单个日历项目更新为定期主日历项目，则必须通过**UpdateItem**操作设置[MeetingTimeZone](meetingtimezone.md)属性，以便保留日历项目的原始时区。</span><span class="sxs-lookup"><span data-stu-id="b5907-138">When a single calendar item is updated to become a recurring master calendar item, the [MeetingTimeZone](meetingtimezone.md) property must be set by the **UpdateItem** operation in order to preserve the calendar item's original time zone.</span></span> 
  
## <a name="setitemfield-request-example"></a><span data-ttu-id="b5907-139">SetItemField 请求示例</span><span class="sxs-lookup"><span data-stu-id="b5907-139">SetItemField request example</span></span>

### <a name="description"></a><span data-ttu-id="b5907-140">Description</span><span class="sxs-lookup"><span data-stu-id="b5907-140">Description</span></span>

<span data-ttu-id="b5907-141">以下示例的**UpdateItem**请求显示如何设置项目的敏感度属性。</span><span class="sxs-lookup"><span data-stu-id="b5907-141">The following example of an **UpdateItem** request shows how to set the sensitivity property on an item.</span></span> 
  
### <a name="code"></a><span data-ttu-id="b5907-142">代码</span><span class="sxs-lookup"><span data-stu-id="b5907-142">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AutoResolve" 
                xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="AAAtAEFkb..." ChangeKey="CQAAABYAAAB..."/>
          <t:Updates>
            <t:SetItemField>
              <t:FieldURI FieldURI="item:Sensitivity"/>
              <t:Message>
                <t:Sensitivity>Normal</t:Sensitivity>
              </t:Message>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
      </ItemChanges>
    </UpdateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="b5907-143">备注</span><span class="sxs-lookup"><span data-stu-id="b5907-143">Comments</span></span>

<span data-ttu-id="b5907-144">项目标识符和更改密钥已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="b5907-144">The item identifier and change key have been shortened to preserve readability.</span></span>
  
### <a name="setitemfield-request-elements"></a><span data-ttu-id="b5907-145">SetItemField 请求元素</span><span class="sxs-lookup"><span data-stu-id="b5907-145">SetItemField Request Elements</span></span>

<span data-ttu-id="b5907-146">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="b5907-146">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="b5907-147">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="b5907-147">UpdateItem</span></span>](updateitem.md)
    
- [<span data-ttu-id="b5907-148">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="b5907-148">ItemChanges</span></span>](itemchanges.md)
    
- [<span data-ttu-id="b5907-149">ItemChange</span><span class="sxs-lookup"><span data-stu-id="b5907-149">ItemChange</span></span>](itemchange.md)
    
- [<span data-ttu-id="b5907-150">ItemId</span><span class="sxs-lookup"><span data-stu-id="b5907-150">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="b5907-151">更新（项目）</span><span class="sxs-lookup"><span data-stu-id="b5907-151">Updates (Item)</span></span>](updates-item.md)
    
- [<span data-ttu-id="b5907-152">SetItemField</span><span class="sxs-lookup"><span data-stu-id="b5907-152">SetItemField</span></span>](setitemfield.md)
    
- [<span data-ttu-id="b5907-153">FieldURI</span><span class="sxs-lookup"><span data-stu-id="b5907-153">FieldURI</span></span>](fielduri.md)
    
- [<span data-ttu-id="b5907-154">消息</span><span class="sxs-lookup"><span data-stu-id="b5907-154">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="b5907-155">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="b5907-155">Sensitivity</span></span>](sensitivity.md)
    
## <a name="appendtoitemfield-request-example"></a><span data-ttu-id="b5907-156">AppendToItemField 请求示例</span><span class="sxs-lookup"><span data-stu-id="b5907-156">AppendToItemField request example</span></span>

### <a name="description"></a><span data-ttu-id="b5907-157">Description</span><span class="sxs-lookup"><span data-stu-id="b5907-157">Description</span></span>

<span data-ttu-id="b5907-158">以下示例的**UpdateItem**请求显示如何将文本追加到项的 body 属性。</span><span class="sxs-lookup"><span data-stu-id="b5907-158">The following example of an **UpdateItem** request shows how to append text to the body property on an item.</span></span> 
  
### <a name="code"></a><span data-ttu-id="b5907-159">代码</span><span class="sxs-lookup"><span data-stu-id="b5907-159">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
  xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AutoResolve" 
                xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="AAAtAEFkbW..." ChangeKey="CQAAABYA..."/>
          <t:Updates>
            <t:AppendToItemField>
              <t:FieldURI FieldURI="item:Body"/>
              <t:Message>
                <t:Body BodyType="Text">Some additional text to append</t:Body>
              </t:Message>
            </t:AppendToItemField>
          </t:Updates>
        </t:ItemChange>
      </ItemChanges>
    </UpdateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="b5907-160">备注</span><span class="sxs-lookup"><span data-stu-id="b5907-160">Comments</span></span>

<span data-ttu-id="b5907-161">以下属性支持 append 操作：</span><span class="sxs-lookup"><span data-stu-id="b5907-161">The following properties support the append action:</span></span>
  
- <span data-ttu-id="b5907-162">**邮件： ReplyTo**</span><span class="sxs-lookup"><span data-stu-id="b5907-162">**message:ReplyTo**</span></span>
    
- <span data-ttu-id="b5907-163">**项目：正文**</span><span class="sxs-lookup"><span data-stu-id="b5907-163">**item:Body**</span></span>
    
- <span data-ttu-id="b5907-164">所有收件人和与会者集合属性</span><span class="sxs-lookup"><span data-stu-id="b5907-164">All the recipient and attendee collection properties</span></span>
    
<span data-ttu-id="b5907-165">项目标识符和更改密钥已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="b5907-165">The item identifier and change key have been shortened to preserve readability.</span></span>
  
### <a name="appendtoitemfield-request-elements"></a><span data-ttu-id="b5907-166">AppendToItemField 请求元素</span><span class="sxs-lookup"><span data-stu-id="b5907-166">AppendToItemField Request Elements</span></span>

<span data-ttu-id="b5907-167">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="b5907-167">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="b5907-168">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="b5907-168">UpdateItem</span></span>](updateitem.md)
    
- [<span data-ttu-id="b5907-169">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="b5907-169">ItemChanges</span></span>](itemchanges.md)
    
- [<span data-ttu-id="b5907-170">ItemChange</span><span class="sxs-lookup"><span data-stu-id="b5907-170">ItemChange</span></span>](itemchange.md)
    
- [<span data-ttu-id="b5907-171">ItemId</span><span class="sxs-lookup"><span data-stu-id="b5907-171">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="b5907-172">更新（项目）</span><span class="sxs-lookup"><span data-stu-id="b5907-172">Updates (Item)</span></span>](updates-item.md)
    
- [<span data-ttu-id="b5907-173">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="b5907-173">AppendToItemField</span></span>](appendtoitemfield.md)
    
- [<span data-ttu-id="b5907-174">FieldURI</span><span class="sxs-lookup"><span data-stu-id="b5907-174">FieldURI</span></span>](fielduri.md)
    
- [<span data-ttu-id="b5907-175">消息</span><span class="sxs-lookup"><span data-stu-id="b5907-175">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="b5907-176">Body</span><span class="sxs-lookup"><span data-stu-id="b5907-176">Body</span></span>](body.md)
    
## <a name="deleteitemfield-request-example"></a><span data-ttu-id="b5907-177">DeleteItemField 请求示例</span><span class="sxs-lookup"><span data-stu-id="b5907-177">DeleteItemField request example</span></span>

### <a name="description"></a><span data-ttu-id="b5907-178">Description</span><span class="sxs-lookup"><span data-stu-id="b5907-178">Description</span></span>

<span data-ttu-id="b5907-179">下面的**UpdateItem**请求示例演示如何删除项的属性。</span><span class="sxs-lookup"><span data-stu-id="b5907-179">The following example of an **UpdateItem** request shows how to delete a property on an item.</span></span> 
  
### <a name="code"></a><span data-ttu-id="b5907-180">代码</span><span class="sxs-lookup"><span data-stu-id="b5907-180">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
  xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AutoResolve" 
                xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="AAAtAEFkbWluaXN0cm..." ChangeKey="CQAAABYAA..."/>
          <t:Updates>
            <t:DeleteItemField>
              <t:FieldURI FieldURI="item:Body"/>
            </t:DeleteItemField>
          </t:Updates>
        </t:ItemChange>
      </ItemChanges>
    </UpdateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="b5907-181">备注</span><span class="sxs-lookup"><span data-stu-id="b5907-181">Comments</span></span>

<span data-ttu-id="b5907-182">项目标识符和更改密钥已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="b5907-182">The item identifier and change key have been shortened to preserve readability.</span></span>
  
### <a name="deleteitemfield-request-elements"></a><span data-ttu-id="b5907-183">DeleteItemField 请求元素</span><span class="sxs-lookup"><span data-stu-id="b5907-183">DeleteItemField Request Elements</span></span>

<span data-ttu-id="b5907-184">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="b5907-184">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="b5907-185">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="b5907-185">UpdateItem</span></span>](updateitem.md)
    
- [<span data-ttu-id="b5907-186">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="b5907-186">ItemChanges</span></span>](itemchanges.md)
    
- [<span data-ttu-id="b5907-187">ItemChange</span><span class="sxs-lookup"><span data-stu-id="b5907-187">ItemChange</span></span>](itemchange.md)
    
- [<span data-ttu-id="b5907-188">ItemId</span><span class="sxs-lookup"><span data-stu-id="b5907-188">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="b5907-189">更新（项目）</span><span class="sxs-lookup"><span data-stu-id="b5907-189">Updates (Item)</span></span>](updates-item.md)
    
- [<span data-ttu-id="b5907-190">DeleteItemField</span><span class="sxs-lookup"><span data-stu-id="b5907-190">DeleteItemField</span></span>](deleteitemfield.md)
    
- [<span data-ttu-id="b5907-191">FieldURI</span><span class="sxs-lookup"><span data-stu-id="b5907-191">FieldURI</span></span>](fielduri.md)
    
## <a name="successful-response-example"></a><span data-ttu-id="b5907-192">成功的响应示例</span><span class="sxs-lookup"><span data-stu-id="b5907-192">Successful response example</span></span>

### <a name="description"></a><span data-ttu-id="b5907-193">Description</span><span class="sxs-lookup"><span data-stu-id="b5907-193">Description</span></span>

<span data-ttu-id="b5907-194">下面的示例演示对**UpdateItem**请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="b5907-194">The following example shows a successful response to an **UpdateItem** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="b5907-195">代码</span><span class="sxs-lookup"><span data-stu-id="b5907-195">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
  xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="664" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <UpdateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:UpdateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:ItemId Id="AAAtAEFkbW..." ChangeKey="CQAAABYAAA..."/>
            </t:Message>
          </m:Items>
        </m:UpdateItemResponseMessage>
      </m:ResponseMessages>
    </UpdateItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="b5907-196">备注</span><span class="sxs-lookup"><span data-stu-id="b5907-196">Comments</span></span>

<span data-ttu-id="b5907-197">项目标识符和更改密钥已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="b5907-197">The item identifier and change key have been shortened to preserve readability.</span></span>
  
### <a name="successful-response-elements"></a><span data-ttu-id="b5907-198">成功的响应元素</span><span class="sxs-lookup"><span data-stu-id="b5907-198">Successful response elements</span></span>

<span data-ttu-id="b5907-199">响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="b5907-199">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="b5907-200">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="b5907-200">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="b5907-201">UpdateItemResponse</span><span class="sxs-lookup"><span data-stu-id="b5907-201">UpdateItemResponse</span></span>](updateitemresponse.md)
    
- [<span data-ttu-id="b5907-202">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="b5907-202">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="b5907-203">UpdateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="b5907-203">UpdateItemResponseMessage</span></span>](updateitemresponsemessage.md)
    
- [<span data-ttu-id="b5907-204">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="b5907-204">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="b5907-205">Items</span><span class="sxs-lookup"><span data-stu-id="b5907-205">Items</span></span>](items.md)
    
- [<span data-ttu-id="b5907-206">消息</span><span class="sxs-lookup"><span data-stu-id="b5907-206">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="b5907-207">ItemId</span><span class="sxs-lookup"><span data-stu-id="b5907-207">ItemId</span></span>](itemid.md)
    
## <a name="see-also"></a><span data-ttu-id="b5907-208">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b5907-208">See also</span></span>



[<span data-ttu-id="b5907-209">UpdateItem 操作（任务）</span><span class="sxs-lookup"><span data-stu-id="b5907-209">UpdateItem operation (task)</span></span>](updateitem-operation-task.md)
  
[<span data-ttu-id="b5907-210">UpdateItem 操作（联系人）</span><span class="sxs-lookup"><span data-stu-id="b5907-210">UpdateItem operation (contact)</span></span>](updateitem-operation-contact.md)


- [<span data-ttu-id="b5907-211">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b5907-211">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="b5907-212">更新联系人</span><span class="sxs-lookup"><span data-stu-id="b5907-212">Updating Contacts</span></span>](https://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
  
[<span data-ttu-id="b5907-213">更新任务</span><span class="sxs-lookup"><span data-stu-id="b5907-213">Updating Tasks</span></span>](https://msdn.microsoft.com/library/0a1bf360-d40c-4a99-929b-4c73a14394d5%28Office.15%29.aspx)

