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
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467422"
---
# <a name="setitemfield"></a><span data-ttu-id="f29b3-103">SetItemField</span><span class="sxs-lookup"><span data-stu-id="f29b3-103">SetItemField</span></span>

<span data-ttu-id="f29b3-104">**SetItemField**元素表示对[UpdateItem 操作](updateitem-operation.md)中项的单个属性的更新。</span><span class="sxs-lookup"><span data-stu-id="f29b3-104">The **SetItemField** element represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>
  
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


<span data-ttu-id="f29b3-105">**SetItemFieldType**</span><span class="sxs-lookup"><span data-stu-id="f29b3-105">**SetItemFieldType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="f29b3-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f29b3-106">Attributes and elements</span></span>

<span data-ttu-id="f29b3-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f29b3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f29b3-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="f29b3-108">Attributes</span></span>

<span data-ttu-id="f29b3-109">无。</span><span class="sxs-lookup"><span data-stu-id="f29b3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f29b3-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f29b3-110">Child elements</span></span>

|<span data-ttu-id="f29b3-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="f29b3-111">**Element**</span></span>|<span data-ttu-id="f29b3-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="f29b3-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f29b3-113">FieldURI</span><span class="sxs-lookup"><span data-stu-id="f29b3-113">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="f29b3-114">标识由 URI 频繁引用的属性。</span><span class="sxs-lookup"><span data-stu-id="f29b3-114">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="f29b3-115">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="f29b3-115">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="f29b3-116">标识词典中的各个成员。</span><span class="sxs-lookup"><span data-stu-id="f29b3-116">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="f29b3-117">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="f29b3-117">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="f29b3-118">确定要设置的扩展 MAPI 属性。</span><span class="sxs-lookup"><span data-stu-id="f29b3-118">Identifies extended MAPI properties to set.</span></span>  <br/> |
|[<span data-ttu-id="f29b3-119">项目</span><span class="sxs-lookup"><span data-stu-id="f29b3-119">Item</span></span>](item.md) <br/> |<span data-ttu-id="f29b3-120">表示 Exchange 存储中的项。</span><span class="sxs-lookup"><span data-stu-id="f29b3-120">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="f29b3-121">邮件</span><span class="sxs-lookup"><span data-stu-id="f29b3-121">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="f29b3-122">表示要更新的 Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="f29b3-122">Represents an Exchange e-mail message to update.</span></span>  <br/> |
|[<span data-ttu-id="f29b3-123">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="f29b3-123">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="f29b3-124">表示要更新的 Exchange 日历项目。</span><span class="sxs-lookup"><span data-stu-id="f29b3-124">Represents an Exchange calendar item to update.</span></span>  <br/> |
|[<span data-ttu-id="f29b3-125">联系人</span><span class="sxs-lookup"><span data-stu-id="f29b3-125">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="f29b3-126">表示要更新的 Exchange 联系人项目。</span><span class="sxs-lookup"><span data-stu-id="f29b3-126">Represents an Exchange contact item to update.</span></span>  <br/> |
|[<span data-ttu-id="f29b3-127">DistributionList</span><span class="sxs-lookup"><span data-stu-id="f29b3-127">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="f29b3-128">表示要更新的通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="f29b3-128">Represents a distribution list to update.</span></span>  <br/> |
|[<span data-ttu-id="f29b3-129">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="f29b3-129">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="f29b3-130">表示要更新的会议邮件。</span><span class="sxs-lookup"><span data-stu-id="f29b3-130">Represents a meeting message to update.</span></span>  <br/> |
|[<span data-ttu-id="f29b3-131">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="f29b3-131">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="f29b3-132">表示要更新的会议请求。</span><span class="sxs-lookup"><span data-stu-id="f29b3-132">Represents a meeting request to update.</span></span>  <br/> |
|[<span data-ttu-id="f29b3-133">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="f29b3-133">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="f29b3-134">表示要更新的会议响应。</span><span class="sxs-lookup"><span data-stu-id="f29b3-134">Represents a meeting response to update.</span></span>  <br/> |
|[<span data-ttu-id="f29b3-135">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="f29b3-135">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="f29b3-136">表示要更新的会议取消。</span><span class="sxs-lookup"><span data-stu-id="f29b3-136">Represents a meeting cancellation to update.</span></span>  <br/> |
|[<span data-ttu-id="f29b3-137">Task</span><span class="sxs-lookup"><span data-stu-id="f29b3-137">Task</span></span>](task.md) <br/> |<span data-ttu-id="f29b3-138">表示要更新的任务。</span><span class="sxs-lookup"><span data-stu-id="f29b3-138">Represents a task to update.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f29b3-139">父元素</span><span class="sxs-lookup"><span data-stu-id="f29b3-139">Parent elements</span></span>

|<span data-ttu-id="f29b3-140">**元素**</span><span class="sxs-lookup"><span data-stu-id="f29b3-140">**Element**</span></span>|<span data-ttu-id="f29b3-141">**说明**</span><span class="sxs-lookup"><span data-stu-id="f29b3-141">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f29b3-142">更新（项目）</span><span class="sxs-lookup"><span data-stu-id="f29b3-142">Updates (Item)</span></span>](updates-item.md) <br/> |<span data-ttu-id="f29b3-143">包含一组元素，这些元素定义追加、设置和删除对项目属性所做的更改。</span><span class="sxs-lookup"><span data-stu-id="f29b3-143">Contains a set of elements that define append, set, and delete changes to item properties.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f29b3-144">说明</span><span class="sxs-lookup"><span data-stu-id="f29b3-144">Remarks</span></span>

<span data-ttu-id="f29b3-145">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f29b3-145">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f29b3-146">元素信息</span><span class="sxs-lookup"><span data-stu-id="f29b3-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f29b3-147">命名空间</span><span class="sxs-lookup"><span data-stu-id="f29b3-147">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f29b3-148">架构名称</span><span class="sxs-lookup"><span data-stu-id="f29b3-148">Schema Name</span></span>  <br/> |<span data-ttu-id="f29b3-149">类型架构</span><span class="sxs-lookup"><span data-stu-id="f29b3-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="f29b3-150">验证文件</span><span class="sxs-lookup"><span data-stu-id="f29b3-150">Validation File</span></span>  <br/> |<span data-ttu-id="f29b3-151">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f29b3-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f29b3-152">可以为空</span><span class="sxs-lookup"><span data-stu-id="f29b3-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="f29b3-153">False</span><span class="sxs-lookup"><span data-stu-id="f29b3-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f29b3-154">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f29b3-154">See also</span></span>

- [<span data-ttu-id="f29b3-155">UpdateItem 操作</span><span class="sxs-lookup"><span data-stu-id="f29b3-155">UpdateItem operation</span></span>](updateitem-operation.md)

