---
title: SetItemField
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SetItemField
api_type:
- schema
ms.assetid: 85284fcb-bd1e-4fda-9dab-cb4cd637cd5b
description: SetItemField 元素表示对 UpdateItem 操作中项的单个属性的更新。
ms.openlocfilehash: b4606eb7d94b9d0c4c5bcd5a2b56d73a4d4270cb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467422"
---
# <a name="setitemfield"></a><span data-ttu-id="c2164-103">SetItemField</span><span class="sxs-lookup"><span data-stu-id="c2164-103">SetItemField</span></span>

<span data-ttu-id="c2164-104">**SetItemField**元素表示对[UpdateItem 操作](updateitem-operation.md)中项的单个属性的更新。</span><span class="sxs-lookup"><span data-stu-id="c2164-104">The **SetItemField** element represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>
  
```xml
<SetItemField>
   <FieldURI/>
   <Item/>
</SetItemField>
```

```xml
<SetItemField>
   <ExtendedFieldURI/> 
   <Item/>
</SetItemField>
```

```xml
<SetItemField>
   <ExtendedFieldURI/> 
   <MeetingRequest/>
</SetItemField>
```

```xml
<SetItemField>
   <ExtendedFieldURI/> 
   <MeetingResponse/>
</SetItemField>
```

```xml
<SetItemField>
   <IndexedFieldURI/> 
   <Contact/>
</SetItemField>
```

```xml
<SetItemField>
   <IndexedFieldURI/> 
   <DistributionList/>
</SetItemField>
```

```xml
<SetItemField>
   <IndexedFieldURI/> 
   <MeetingResponse/>
</SetItemField>
```

```xml
<SetItemField>
   <FieldURI/> 
   <MeetingResponse/> 
</SetItemField>
```

```xml
<SetItemField>
   <FieldURI/> 
   <MeetingRequest/> 
</SetItemField>
```

```xml
<SetItemField>
   <FieldURI/> 
   <Contact/>
</SetItemField>
```

```xml
<SetItemField>
   <IndexedFieldURI/> 
   <Message/>
</SetItemField>
```

```xml
<SetItemField>
   <ExtendedFieldURI/> 
   <CalendarItem/>
</SetItemField>
```

```xml
<SetItemField>
   <ExtendedFieldURI/> 
   <Task/>
</SetItemField>
```

```xml
<SetItemField>
   <ExtendedFieldURI/> 
   <Message/> 
</SetItemField>
```

```xml
<SetItemField>
   <FieldURI/> 
   <MeetingCancellation/> 
</SetItemField>
```

```xml
<SetItemField>
   <FieldURI/> 
   <Task/> 
</SetItemField>
```

```xml
<SetItemField>
   <IndexedFieldURI/> 
   <MeetingRequest/>  
</SetItemField>
```

```xml
<SetItemField>
    <FieldURI/> 
    <CalendarItem/>
</SetItemField>
```

```xml
<SetItemField>
    <IndexedFieldURI/> 
    <Item/>
</SetItemField>
```

```xml
<SetItemField>
   <ExtendedFieldURI/> 
   <MeetingCancellation/>
</SetItemField>
```

```xml
<SetItemField>
   <FieldURI/> 
   <DistributionList/> 
</SetItemField>
```

```xml
<SetItemField>
   <IndexedFieldURI/> 
   <MeetingCancellation/>
</SetItemField>
```

```xml
<SetItemField>
   <ExtendedFieldURI/> 
   <MeetingMessage/>
</SetItemField>
```

```xml
<SetItemField>
   <IndexedFieldURI/> 
   <Task/> 
</SetItemField>
```

```xml
<SetItemField>
   <IndexedFieldURI/> 
   <CalendarItem/>
</SetItemField>
```

```xml
<SetItemField>
   <FieldURI/> 
   <MeetingMessage/>
</SetItemField>
```

```xml
<SetItemField>
   <IndexedFieldURI/> 
   <MeetingMessage/>
</SetItemField>
```

```xml
<SetItemField>
   <FieldURI/> 
   <Message/>
</SetItemField>
```

```xml
<SetItemField>
   <ExtendedFieldURI/> 
   <DistributionList/>
</SetItemField>
```

```xml
<SetItemField>
   <ExtendedFieldURI/> 
   <Contact/> 
</SetItemField>
```


<span data-ttu-id="c2164-105">**SetItemFieldType**</span><span class="sxs-lookup"><span data-stu-id="c2164-105">**SetItemFieldType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="c2164-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c2164-106">Attributes and elements</span></span>

<span data-ttu-id="c2164-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c2164-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c2164-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="c2164-108">Attributes</span></span>

<span data-ttu-id="c2164-109">无。</span><span class="sxs-lookup"><span data-stu-id="c2164-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c2164-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c2164-110">Child elements</span></span>

|<span data-ttu-id="c2164-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="c2164-111">**Element**</span></span>|<span data-ttu-id="c2164-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="c2164-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c2164-113">FieldURI</span><span class="sxs-lookup"><span data-stu-id="c2164-113">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="c2164-114">标识由 URI 频繁引用的属性。</span><span class="sxs-lookup"><span data-stu-id="c2164-114">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="c2164-115">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="c2164-115">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="c2164-116">标识词典中的各个成员。</span><span class="sxs-lookup"><span data-stu-id="c2164-116">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="c2164-117">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="c2164-117">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="c2164-118">确定要设置的扩展 MAPI 属性。</span><span class="sxs-lookup"><span data-stu-id="c2164-118">Identifies extended MAPI properties to set.</span></span>  <br/> |
|[<span data-ttu-id="c2164-119">项目</span><span class="sxs-lookup"><span data-stu-id="c2164-119">Item</span></span>](item.md) <br/> |<span data-ttu-id="c2164-120">表示 Exchange 存储中的项。</span><span class="sxs-lookup"><span data-stu-id="c2164-120">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="c2164-121">消息</span><span class="sxs-lookup"><span data-stu-id="c2164-121">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="c2164-122">表示要更新的 Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="c2164-122">Represents an Exchange e-mail message to update.</span></span>  <br/> |
|[<span data-ttu-id="c2164-123">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="c2164-123">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="c2164-124">表示要更新的 Exchange 日历项目。</span><span class="sxs-lookup"><span data-stu-id="c2164-124">Represents an Exchange calendar item to update.</span></span>  <br/> |
|[<span data-ttu-id="c2164-125">联系人</span><span class="sxs-lookup"><span data-stu-id="c2164-125">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="c2164-126">表示要更新的 Exchange 联系人项目。</span><span class="sxs-lookup"><span data-stu-id="c2164-126">Represents an Exchange contact item to update.</span></span>  <br/> |
|[<span data-ttu-id="c2164-127">DistributionList</span><span class="sxs-lookup"><span data-stu-id="c2164-127">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="c2164-128">表示要更新的通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="c2164-128">Represents a distribution list to update.</span></span>  <br/> |
|[<span data-ttu-id="c2164-129">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="c2164-129">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="c2164-130">表示要更新的会议邮件。</span><span class="sxs-lookup"><span data-stu-id="c2164-130">Represents a meeting message to update.</span></span>  <br/> |
|[<span data-ttu-id="c2164-131">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="c2164-131">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="c2164-132">表示要更新的会议请求。</span><span class="sxs-lookup"><span data-stu-id="c2164-132">Represents a meeting request to update.</span></span>  <br/> |
|[<span data-ttu-id="c2164-133">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="c2164-133">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="c2164-134">表示要更新的会议响应。</span><span class="sxs-lookup"><span data-stu-id="c2164-134">Represents a meeting response to update.</span></span>  <br/> |
|[<span data-ttu-id="c2164-135">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="c2164-135">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="c2164-136">表示要更新的会议取消。</span><span class="sxs-lookup"><span data-stu-id="c2164-136">Represents a meeting cancellation to update.</span></span>  <br/> |
|[<span data-ttu-id="c2164-137">任务</span><span class="sxs-lookup"><span data-stu-id="c2164-137">Task</span></span>](task.md) <br/> |<span data-ttu-id="c2164-138">表示要更新的任务。</span><span class="sxs-lookup"><span data-stu-id="c2164-138">Represents a task to update.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c2164-139">父元素</span><span class="sxs-lookup"><span data-stu-id="c2164-139">Parent elements</span></span>

|<span data-ttu-id="c2164-140">**元素**</span><span class="sxs-lookup"><span data-stu-id="c2164-140">**Element**</span></span>|<span data-ttu-id="c2164-141">**说明**</span><span class="sxs-lookup"><span data-stu-id="c2164-141">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c2164-142">更新（项目）</span><span class="sxs-lookup"><span data-stu-id="c2164-142">Updates (Item)</span></span>](updates-item.md) <br/> |<span data-ttu-id="c2164-143">包含一组元素，这些元素定义追加、设置和删除对项目属性所做的更改。</span><span class="sxs-lookup"><span data-stu-id="c2164-143">Contains a set of elements that define append, set, and delete changes to item properties.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c2164-144">说明</span><span class="sxs-lookup"><span data-stu-id="c2164-144">Remarks</span></span>

<span data-ttu-id="c2164-145">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c2164-145">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c2164-146">元素信息</span><span class="sxs-lookup"><span data-stu-id="c2164-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c2164-147">命名空间</span><span class="sxs-lookup"><span data-stu-id="c2164-147">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c2164-148">架构名称</span><span class="sxs-lookup"><span data-stu-id="c2164-148">Schema Name</span></span>  <br/> |<span data-ttu-id="c2164-149">类型架构</span><span class="sxs-lookup"><span data-stu-id="c2164-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="c2164-150">验证文件</span><span class="sxs-lookup"><span data-stu-id="c2164-150">Validation File</span></span>  <br/> |<span data-ttu-id="c2164-151">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c2164-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c2164-152">可以为空</span><span class="sxs-lookup"><span data-stu-id="c2164-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="c2164-153">False</span><span class="sxs-lookup"><span data-stu-id="c2164-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c2164-154">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c2164-154">See also</span></span>

- [<span data-ttu-id="c2164-155">UpdateItem 操作</span><span class="sxs-lookup"><span data-stu-id="c2164-155">UpdateItem operation</span></span>](updateitem-operation.md)

