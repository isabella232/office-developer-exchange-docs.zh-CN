---
title: CreateAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateAttachment
api_type:
- schema
ms.assetid: e33b403a-b7d3-48ee-8d24-6b7abf0d70bc
description: CreateAttachment 元素定义一个请求，用于创建到 Exchange 存储中的项目的附件。
ms.openlocfilehash: 4cba1b8865dae5da58b9617b249a29314c67331a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466435"
---
# <a name="createattachment"></a><span data-ttu-id="efed9-103">CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="efed9-103">CreateAttachment</span></span>

<span data-ttu-id="efed9-104">**CreateAttachment**元素定义一个请求，用于创建到 Exchange 存储中的项目的附件。</span><span class="sxs-lookup"><span data-stu-id="efed9-104">The **CreateAttachment** element defines a request to create an attachment to an item in the Exchange store.</span></span> 
  
```xml
<CreateAttachment>
   <ParentItemId/>
   <Attachments/>
</CreateAttachment>
```

 <span data-ttu-id="efed9-105">**CreateAttachmentType**</span><span class="sxs-lookup"><span data-stu-id="efed9-105">**CreateAttachmentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="efed9-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="efed9-106">Attributes and elements</span></span>

<span data-ttu-id="efed9-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="efed9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="efed9-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="efed9-108">Attributes</span></span>

<span data-ttu-id="efed9-109">无。</span><span class="sxs-lookup"><span data-stu-id="efed9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="efed9-110">子元素</span><span class="sxs-lookup"><span data-stu-id="efed9-110">Child elements</span></span>

|<span data-ttu-id="efed9-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="efed9-111">**Element**</span></span>|<span data-ttu-id="efed9-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="efed9-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="efed9-113">ParentItemId</span><span class="sxs-lookup"><span data-stu-id="efed9-113">ParentItemId</span></span>](parentitemid.md) <br/> |<span data-ttu-id="efed9-114">标识包含创建的附件的父 Exchange 存储项。</span><span class="sxs-lookup"><span data-stu-id="efed9-114">Identifies the parent Exchange store item that contains the created attachment.</span></span> <span data-ttu-id="efed9-115">[ParentItemId](parentitemid.md)元素必须提供实际 Exchange 存储项的 ID。</span><span class="sxs-lookup"><span data-stu-id="efed9-115">The [ParentItemId](parentitemid.md) element must provide the ID of a real Exchange store item.</span></span> <span data-ttu-id="efed9-116">可以使用[GetItem 操作](getitem-operation.md)检索真实的存储项;附件是通过使用[GetAttachment 操作](getattachment-operation.md)检索的。</span><span class="sxs-lookup"><span data-stu-id="efed9-116">Real store items can be retrieved by using the [GetItem operation](getitem-operation.md); attachments are retrieved by using the [GetAttachment operation](getattachment-operation.md).</span></span> <span data-ttu-id="efed9-117">如果[ParentItemId](parentitemid.md)传递的是文件附件的 ID，则会发生错误。</span><span class="sxs-lookup"><span data-stu-id="efed9-117">An error occurs if the [ParentItemId](parentitemid.md) is passed the ID of a file attachment.</span></span> <span data-ttu-id="efed9-118">如果[ParentItemId](parentitemid.md)代表现有项目附件的 ID，则[CreateAttachment 操作](createattachment-operation.md)会将新附件添加到现有附件中。</span><span class="sxs-lookup"><span data-stu-id="efed9-118">If the [ParentItemId](parentitemid.md) represents the ID of an existing item attachment, the [CreateAttachment operation](createattachment-operation.md) adds the new attachment to the existing attachment.</span></span>  <br/> <span data-ttu-id="efed9-119">此元素是[CreateAttachment 操作](createattachment-operation.md)所必需的。</span><span class="sxs-lookup"><span data-stu-id="efed9-119">This element is required for the [CreateAttachment operation](createattachment-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="efed9-120">附件</span><span class="sxs-lookup"><span data-stu-id="efed9-120">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="efed9-121">包含要附加到 Exchange 存储中的项目的项目或文件。</span><span class="sxs-lookup"><span data-stu-id="efed9-121">Contains the items or files to attach to an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="efed9-122">父元素</span><span class="sxs-lookup"><span data-stu-id="efed9-122">Parent elements</span></span>

<span data-ttu-id="efed9-123">无。</span><span class="sxs-lookup"><span data-stu-id="efed9-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="efed9-124">说明</span><span class="sxs-lookup"><span data-stu-id="efed9-124">Remarks</span></span>

<span data-ttu-id="efed9-125">项目附件不作为存储项存在。</span><span class="sxs-lookup"><span data-stu-id="efed9-125">An item attachment does not exist as a store item.</span></span> <span data-ttu-id="efed9-126">它仅作为项目附件或其他附件存在。</span><span class="sxs-lookup"><span data-stu-id="efed9-126">It only exists as an attachment to an item or another attachment.</span></span> <span data-ttu-id="efed9-127">仅可使用[GetAttachment](getattachment.md)请求检索项目附件。</span><span class="sxs-lookup"><span data-stu-id="efed9-127">Item attachments can only be retrieved by using the [GetAttachment](getattachment.md) request.</span></span> 
  
<span data-ttu-id="efed9-128">可以创建以下项附件：</span><span class="sxs-lookup"><span data-stu-id="efed9-128">The following item attachments can be created:</span></span>
  
- <span data-ttu-id="efed9-129">项目</span><span class="sxs-lookup"><span data-stu-id="efed9-129">Item</span></span>
    
- <span data-ttu-id="efed9-130">消息</span><span class="sxs-lookup"><span data-stu-id="efed9-130">Message</span></span>
    
- <span data-ttu-id="efed9-131">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="efed9-131">CalendarItem</span></span>
    
- <span data-ttu-id="efed9-132">Contact</span><span class="sxs-lookup"><span data-stu-id="efed9-132">Contact</span></span>
    
- <span data-ttu-id="efed9-133">任务</span><span class="sxs-lookup"><span data-stu-id="efed9-133">Task</span></span>
    
- <span data-ttu-id="efed9-134">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="efed9-134">MeetingMessage</span></span>
    
- <span data-ttu-id="efed9-135">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="efed9-135">MeetingRequest</span></span>
    
<span data-ttu-id="efed9-136">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="efed9-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="efed9-137">示例</span><span class="sxs-lookup"><span data-stu-id="efed9-137">Example</span></span>

<span data-ttu-id="efed9-138">下面的示例演示如何创建项目并将其附加到 Exchange 存储中的其他项目。</span><span class="sxs-lookup"><span data-stu-id="efed9-138">The following example shows how to create and attach an item to another item in the Exchange store.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateAttachment xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" 
                  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <ParentItemId Id="ASkAS"/>
      <Attachments>
        <t:ItemAttachment>
          <t:Name>MyAttachment</t:Name>
          <t:Message>
            <t:ItemClass>IPM>Note</t:ItemClass>
            <t:Subject>My attachment subject</t:Subject>
            <t:Body BodyType="Text">My attachment body</t:Body>
          </t:Message>
        </t:ItemAttachment>
      </Attachments>
    </CreateAttachment>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a><span data-ttu-id="efed9-139">元素信息</span><span class="sxs-lookup"><span data-stu-id="efed9-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="efed9-140">命名空间</span><span class="sxs-lookup"><span data-stu-id="efed9-140">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="efed9-141">架构名称</span><span class="sxs-lookup"><span data-stu-id="efed9-141">Schema Name</span></span>  <br/> |<span data-ttu-id="efed9-142">消息架构</span><span class="sxs-lookup"><span data-stu-id="efed9-142">Messages schema</span></span>  <br/> |
|<span data-ttu-id="efed9-143">验证文件</span><span class="sxs-lookup"><span data-stu-id="efed9-143">Validation File</span></span>  <br/> |<span data-ttu-id="efed9-144">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="efed9-144">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="efed9-145">可以为空</span><span class="sxs-lookup"><span data-stu-id="efed9-145">Can be Empty</span></span>  <br/> |<span data-ttu-id="efed9-146">False</span><span class="sxs-lookup"><span data-stu-id="efed9-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="efed9-147">另请参阅</span><span class="sxs-lookup"><span data-stu-id="efed9-147">See also</span></span>



[<span data-ttu-id="efed9-148">CreateAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="efed9-148">CreateAttachment operation</span></span>](createattachment-operation.md)
  
[<span data-ttu-id="efed9-149">DeleteAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="efed9-149">DeleteAttachment operation</span></span>](deleteattachment-operation.md)
  
[<span data-ttu-id="efed9-150">GetAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="efed9-150">GetAttachment operation</span></span>](getattachment-operation.md)

