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
description: SetItemField 元素表示更新到单个 UpdateItem 操作中的项目的属性。
ms.openlocfilehash: bd3e5bca3d61325ef3f218c5ada535346247f391
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353796"
---
# <a name="setitemfield"></a><span data-ttu-id="deb24-103">SetItemField</span><span class="sxs-lookup"><span data-stu-id="deb24-103">SetItemField</span></span>

<span data-ttu-id="deb24-104">**SetItemField**元素表示更新到单个[UpdateItem 操作](updateitem-operation.md)中的项目的属性。</span><span class="sxs-lookup"><span data-stu-id="deb24-104">The **SetItemField** element represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>
  
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


<span data-ttu-id="deb24-105">**SetItemFieldType**</span><span class="sxs-lookup"><span data-stu-id="deb24-105">**SetItemFieldType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="deb24-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="deb24-106">Attributes and elements</span></span>

<span data-ttu-id="deb24-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="deb24-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="deb24-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="deb24-108">Attributes</span></span>

<span data-ttu-id="deb24-109">无。</span><span class="sxs-lookup"><span data-stu-id="deb24-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="deb24-110">子元素</span><span class="sxs-lookup"><span data-stu-id="deb24-110">Child elements</span></span>

|<span data-ttu-id="deb24-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="deb24-111">**Element**</span></span>|<span data-ttu-id="deb24-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="deb24-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="deb24-113">FieldURI</span><span class="sxs-lookup"><span data-stu-id="deb24-113">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="deb24-114">标识由 URI 频繁引用的属性。</span><span class="sxs-lookup"><span data-stu-id="deb24-114">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="deb24-115">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="deb24-115">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="deb24-116">标识词典中的各个成员。</span><span class="sxs-lookup"><span data-stu-id="deb24-116">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="deb24-117">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="deb24-117">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="deb24-118">标识扩展的 MAPI 属性设置。</span><span class="sxs-lookup"><span data-stu-id="deb24-118">Identifies extended MAPI properties to set.</span></span>  <br/> |
|[<span data-ttu-id="deb24-119">项目</span><span class="sxs-lookup"><span data-stu-id="deb24-119">Item</span></span>](item.md) <br/> |<span data-ttu-id="deb24-120">表示 Exchange 存储中的项。</span><span class="sxs-lookup"><span data-stu-id="deb24-120">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="deb24-121">邮件</span><span class="sxs-lookup"><span data-stu-id="deb24-121">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="deb24-122">代表要更新 Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="deb24-122">Represents an Exchange e-mail message to update.</span></span>  <br/> |
|[<span data-ttu-id="deb24-123">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="deb24-123">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="deb24-124">代表要更新 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="deb24-124">Represents an Exchange calendar item to update.</span></span>  <br/> |
|[<span data-ttu-id="deb24-125">Contact</span><span class="sxs-lookup"><span data-stu-id="deb24-125">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="deb24-126">代表要更新 Exchange 联系人项。</span><span class="sxs-lookup"><span data-stu-id="deb24-126">Represents an Exchange contact item to update.</span></span>  <br/> |
|[<span data-ttu-id="deb24-127">DistributionList</span><span class="sxs-lookup"><span data-stu-id="deb24-127">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="deb24-128">代表要更新的通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="deb24-128">Represents a distribution list to update.</span></span>  <br/> |
|[<span data-ttu-id="deb24-129">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="deb24-129">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="deb24-130">代表要更新的会议消息。</span><span class="sxs-lookup"><span data-stu-id="deb24-130">Represents a meeting message to update.</span></span>  <br/> |
|[<span data-ttu-id="deb24-131">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="deb24-131">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="deb24-132">表示要更新的会议请求。</span><span class="sxs-lookup"><span data-stu-id="deb24-132">Represents a meeting request to update.</span></span>  <br/> |
|[<span data-ttu-id="deb24-133">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="deb24-133">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="deb24-134">代表要更新的会议响应。</span><span class="sxs-lookup"><span data-stu-id="deb24-134">Represents a meeting response to update.</span></span>  <br/> |
|[<span data-ttu-id="deb24-135">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="deb24-135">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="deb24-136">代表要更新会议取消。</span><span class="sxs-lookup"><span data-stu-id="deb24-136">Represents a meeting cancellation to update.</span></span>  <br/> |
|[<span data-ttu-id="deb24-137">任务</span><span class="sxs-lookup"><span data-stu-id="deb24-137">Task</span></span>](task.md) <br/> |<span data-ttu-id="deb24-138">代表要更新的任务。</span><span class="sxs-lookup"><span data-stu-id="deb24-138">Represents a task to update.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="deb24-139">父元素</span><span class="sxs-lookup"><span data-stu-id="deb24-139">Parent elements</span></span>

|<span data-ttu-id="deb24-140">**元素**</span><span class="sxs-lookup"><span data-stu-id="deb24-140">**Element**</span></span>|<span data-ttu-id="deb24-141">**说明**</span><span class="sxs-lookup"><span data-stu-id="deb24-141">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="deb24-142">Updates (Item)</span><span class="sxs-lookup"><span data-stu-id="deb24-142">Updates (Item)</span></span>](updates-item.md) <br/> |<span data-ttu-id="deb24-143">包含一组定义的元素的 append、 设置和删除项目属性更改。</span><span class="sxs-lookup"><span data-stu-id="deb24-143">Contains a set of elements that define append, set, and delete changes to item properties.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="deb24-144">说明</span><span class="sxs-lookup"><span data-stu-id="deb24-144">Remarks</span></span>

<span data-ttu-id="deb24-145">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="deb24-145">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="deb24-146">元素信息</span><span class="sxs-lookup"><span data-stu-id="deb24-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="deb24-147">命名空间</span><span class="sxs-lookup"><span data-stu-id="deb24-147">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="deb24-148">架构名称</span><span class="sxs-lookup"><span data-stu-id="deb24-148">Schema Name</span></span>  <br/> |<span data-ttu-id="deb24-149">类型架构</span><span class="sxs-lookup"><span data-stu-id="deb24-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="deb24-150">验证文件</span><span class="sxs-lookup"><span data-stu-id="deb24-150">Validation File</span></span>  <br/> |<span data-ttu-id="deb24-151">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="deb24-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="deb24-152">可以为空</span><span class="sxs-lookup"><span data-stu-id="deb24-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="deb24-153">False</span><span class="sxs-lookup"><span data-stu-id="deb24-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="deb24-154">另请参阅</span><span class="sxs-lookup"><span data-stu-id="deb24-154">See also</span></span>

- [<span data-ttu-id="deb24-155">UpdateItem 操作</span><span class="sxs-lookup"><span data-stu-id="deb24-155">UpdateItem operation</span></span>](updateitem-operation.md)

