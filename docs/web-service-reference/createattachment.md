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
description: CreateAttachment 元素定义一个请求在 Exchange 存储中创建项目的附件。
ms.openlocfilehash: d403eb5ca15623d3a973f7b224dbcde5529cf1bc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753625"
---
# <a name="createattachment"></a><span data-ttu-id="a6ea7-103">CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="a6ea7-103">CreateAttachment</span></span>

<span data-ttu-id="a6ea7-104">**CreateAttachment**元素定义一个请求在 Exchange 存储中创建项目的附件。</span><span class="sxs-lookup"><span data-stu-id="a6ea7-104">The **CreateAttachment** element defines a request to create an attachment to an item in the Exchange store.</span></span> 
  
```xml
<CreateAttachment>
   <ParentItemId/>
   <Attachments/>
</CreateAttachment>
```

 <span data-ttu-id="a6ea7-105">**CreateAttachmentType**</span><span class="sxs-lookup"><span data-stu-id="a6ea7-105">**CreateAttachmentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a6ea7-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a6ea7-106">Attributes and elements</span></span>

<span data-ttu-id="a6ea7-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a6ea7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a6ea7-108">属性</span><span class="sxs-lookup"><span data-stu-id="a6ea7-108">Attributes</span></span>

<span data-ttu-id="a6ea7-109">无。</span><span class="sxs-lookup"><span data-stu-id="a6ea7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a6ea7-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a6ea7-110">Child elements</span></span>

|<span data-ttu-id="a6ea7-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="a6ea7-111">**Element**</span></span>|<span data-ttu-id="a6ea7-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="a6ea7-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a6ea7-113">ParentItemId</span><span class="sxs-lookup"><span data-stu-id="a6ea7-113">ParentItemId</span></span>](parentitemid.md) <br/> |<span data-ttu-id="a6ea7-114">标识父 Exchange 存储项包含创建的附件。</span><span class="sxs-lookup"><span data-stu-id="a6ea7-114">Identifies the parent Exchange store item that contains the created attachment.</span></span> <span data-ttu-id="a6ea7-115">[ParentItemId](parentitemid.md)元素必须提供的实际 Exchange ID 存储项。</span><span class="sxs-lookup"><span data-stu-id="a6ea7-115">The [ParentItemId](parentitemid.md) element must provide the ID of a real Exchange store item.</span></span> <span data-ttu-id="a6ea7-116">可以通过使用[GetItem 操作](getitem-operation.md); 来检索实际存储项目通过使用[GetAttachment 操作](getattachment-operation.md)检索附件。</span><span class="sxs-lookup"><span data-stu-id="a6ea7-116">Real store items can be retrieved by using the [GetItem operation](getitem-operation.md); attachments are retrieved by using the [GetAttachment operation](getattachment-operation.md).</span></span> <span data-ttu-id="a6ea7-117">如果[ParentItemId](parentitemid.md)传递的文件附件 ID，将发生错误。</span><span class="sxs-lookup"><span data-stu-id="a6ea7-117">An error occurs if the [ParentItemId](parentitemid.md) is passed the ID of a file attachment.</span></span> <span data-ttu-id="a6ea7-118">如果[ParentItemId](parentitemid.md)表示现有项目附件的 ID， [CreateAttachment 操作](createattachment-operation.md)添加到现有的附件的新附件。</span><span class="sxs-lookup"><span data-stu-id="a6ea7-118">If the [ParentItemId](parentitemid.md) represents the ID of an existing item attachment, the [CreateAttachment operation](createattachment-operation.md) adds the new attachment to the existing attachment.</span></span>  <br/> <span data-ttu-id="a6ea7-119">此元素是[CreateAttachment 操作](createattachment-operation.md)所必需的。</span><span class="sxs-lookup"><span data-stu-id="a6ea7-119">This element is required for the [CreateAttachment operation](createattachment-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="a6ea7-120">附件</span><span class="sxs-lookup"><span data-stu-id="a6ea7-120">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="a6ea7-121">包含的项目或文件附加到 Exchange 存储中的项。</span><span class="sxs-lookup"><span data-stu-id="a6ea7-121">Contains the items or files to attach to an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a6ea7-122">父元素</span><span class="sxs-lookup"><span data-stu-id="a6ea7-122">Parent elements</span></span>

<span data-ttu-id="a6ea7-123">无。</span><span class="sxs-lookup"><span data-stu-id="a6ea7-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a6ea7-124">备注</span><span class="sxs-lookup"><span data-stu-id="a6ea7-124">Remarks</span></span>

<span data-ttu-id="a6ea7-125">为存储项不存在项目附件。</span><span class="sxs-lookup"><span data-stu-id="a6ea7-125">An item attachment does not exist as a store item.</span></span> <span data-ttu-id="a6ea7-126">仅存在为项目附件或另一个附件。</span><span class="sxs-lookup"><span data-stu-id="a6ea7-126">It only exists as an attachment to an item or another attachment.</span></span> <span data-ttu-id="a6ea7-127">只能通过使用[GetAttachment](getattachment.md)请求检索项附件。</span><span class="sxs-lookup"><span data-stu-id="a6ea7-127">Item attachments can only be retrieved by using the [GetAttachment](getattachment.md) request.</span></span> 
  
<span data-ttu-id="a6ea7-128">可以创建以下项附件：</span><span class="sxs-lookup"><span data-stu-id="a6ea7-128">The following item attachments can be created:</span></span>
  
- <span data-ttu-id="a6ea7-129">项目</span><span class="sxs-lookup"><span data-stu-id="a6ea7-129">Item</span></span>
    
- <span data-ttu-id="a6ea7-130">邮件</span><span class="sxs-lookup"><span data-stu-id="a6ea7-130">Message</span></span>
    
- <span data-ttu-id="a6ea7-131">日历项目</span><span class="sxs-lookup"><span data-stu-id="a6ea7-131">CalendarItem</span></span>
    
- <span data-ttu-id="a6ea7-132">联系人</span><span class="sxs-lookup"><span data-stu-id="a6ea7-132">Contact</span></span>
    
- <span data-ttu-id="a6ea7-133">任务</span><span class="sxs-lookup"><span data-stu-id="a6ea7-133">Task</span></span>
    
- <span data-ttu-id="a6ea7-134">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="a6ea7-134">MeetingMessage</span></span>
    
- <span data-ttu-id="a6ea7-135">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="a6ea7-135">MeetingRequest</span></span>
    
<span data-ttu-id="a6ea7-136">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a6ea7-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="a6ea7-137">示例</span><span class="sxs-lookup"><span data-stu-id="a6ea7-137">Example</span></span>

<span data-ttu-id="a6ea7-138">下面的示例演示如何创建并附加到 Exchange 存储中的另一个项目的项目。</span><span class="sxs-lookup"><span data-stu-id="a6ea7-138">The following example shows how to create and attach an item to another item in the Exchange store.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateAttachment xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" 
                  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="element-information"></a><span data-ttu-id="a6ea7-139">元素信息</span><span class="sxs-lookup"><span data-stu-id="a6ea7-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a6ea7-140">命名空间</span><span class="sxs-lookup"><span data-stu-id="a6ea7-140">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a6ea7-141">架构名称</span><span class="sxs-lookup"><span data-stu-id="a6ea7-141">Schema Name</span></span>  <br/> |<span data-ttu-id="a6ea7-142">消息架构</span><span class="sxs-lookup"><span data-stu-id="a6ea7-142">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a6ea7-143">验证文件</span><span class="sxs-lookup"><span data-stu-id="a6ea7-143">Validation File</span></span>  <br/> |<span data-ttu-id="a6ea7-144">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a6ea7-144">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a6ea7-145">可以为空</span><span class="sxs-lookup"><span data-stu-id="a6ea7-145">Can be Empty</span></span>  <br/> |<span data-ttu-id="a6ea7-146">False</span><span class="sxs-lookup"><span data-stu-id="a6ea7-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a6ea7-147">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a6ea7-147">See also</span></span>



[<span data-ttu-id="a6ea7-148">CreateAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="a6ea7-148">CreateAttachment operation</span></span>](createattachment-operation.md)
  
[<span data-ttu-id="a6ea7-149">DeleteAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="a6ea7-149">DeleteAttachment operation</span></span>](deleteattachment-operation.md)
  
[<span data-ttu-id="a6ea7-150">GetAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="a6ea7-150">GetAttachment operation</span></span>](getattachment-operation.md)

