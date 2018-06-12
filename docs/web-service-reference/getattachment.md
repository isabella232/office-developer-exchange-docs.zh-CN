---
title: GetAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetAttachment
api_type:
- schema
ms.assetid: 9443cf96-b451-4530-b868-490dff798673
description: GetAttachment 元素是从 Exchange 存储中获取附件的请求中的根元素。
ms.openlocfilehash: fb639c86a0654e8f9e9601310f7c2f5b0fc7d729
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754466"
---
# <a name="getattachment"></a><span data-ttu-id="c446e-103">GetAttachment</span><span class="sxs-lookup"><span data-stu-id="c446e-103">GetAttachment</span></span>

<span data-ttu-id="c446e-104">**GetAttachment**元素是从 Exchange 存储中获取附件的请求中的根元素。</span><span class="sxs-lookup"><span data-stu-id="c446e-104">The **GetAttachment** element is the root element in a request to get an attachment from the Exchange store.</span></span> 
  
```xml
<GetAttachment>
   <AttachmentShape/>
   <AttachmentIds/>
</GetAttachment>
```

 <span data-ttu-id="c446e-105">**GetAttachmentType**</span><span class="sxs-lookup"><span data-stu-id="c446e-105">**GetAttachmentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c446e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c446e-106">Attributes and elements</span></span>

<span data-ttu-id="c446e-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c446e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c446e-108">属性</span><span class="sxs-lookup"><span data-stu-id="c446e-108">Attributes</span></span>

<span data-ttu-id="c446e-109">无。</span><span class="sxs-lookup"><span data-stu-id="c446e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c446e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c446e-110">Child elements</span></span>

|<span data-ttu-id="c446e-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="c446e-111">**Element**</span></span>|<span data-ttu-id="c446e-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="c446e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c446e-113">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="c446e-113">AttachmentShape</span></span>](attachmentshape.md) <br/> |<span data-ttu-id="c446e-114">标识要[GetAttachment](getattachment.md)请求的响应中返回的其他扩展的项属性。</span><span class="sxs-lookup"><span data-stu-id="c446e-114">Identifies additional extended item properties to return in a response to a [GetAttachment](getattachment.md) request.</span></span> <span data-ttu-id="c446e-115">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="c446e-115">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="c446e-116">AttachmentIds</span><span class="sxs-lookup"><span data-stu-id="c446e-116">AttachmentIds</span></span>](attachmentids.md) <br/> |<span data-ttu-id="c446e-117">包含附件标识符的数组。</span><span class="sxs-lookup"><span data-stu-id="c446e-117">Contains an array of attachment identifiers.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c446e-118">父元素</span><span class="sxs-lookup"><span data-stu-id="c446e-118">Parent elements</span></span>

<span data-ttu-id="c446e-119">无。</span><span class="sxs-lookup"><span data-stu-id="c446e-119">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c446e-120">备注</span><span class="sxs-lookup"><span data-stu-id="c446e-120">Remarks</span></span>

<span data-ttu-id="c446e-121">[AttachmentShape](attachmentshape.md)元素不需要确定在响应中返回的属性。</span><span class="sxs-lookup"><span data-stu-id="c446e-121">The [AttachmentShape](attachmentshape.md) element is not required to identify the properties returned in the response.</span></span> <span data-ttu-id="c446e-122">[GetAttachment 操作](getattachment-operation.md)返回的名称、 ContentType、 ContentId、 ContentLocation 和附件的文件的内容属性。</span><span class="sxs-lookup"><span data-stu-id="c446e-122">The [GetAttachment operation](getattachment-operation.md) returns the Name, ContentType, ContentId, ContentLocation, and the Content properties for file attachments.</span></span> <span data-ttu-id="c446e-123">对于项目的附件，返回的属性的名称、 ContentType、 ContentId、 ContentLocation 和附加的项的所有属性。</span><span class="sxs-lookup"><span data-stu-id="c446e-123">For item attachments, the returned properties are the Name, ContentType, ContentId, ContentLocation, and all the attached item's properties.</span></span> <span data-ttu-id="c446e-124">这是等价于[GetItem](getitem.md)请求中使用 AllProperties 基本形状。</span><span class="sxs-lookup"><span data-stu-id="c446e-124">This is equivalent to using the AllProperties base shape in a [GetItem](getitem.md) request.</span></span> 
  
<span data-ttu-id="c446e-125">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c446e-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c446e-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="c446e-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c446e-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="c446e-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c446e-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="c446e-128">Schema Name</span></span>  <br/> |<span data-ttu-id="c446e-129">消息架构</span><span class="sxs-lookup"><span data-stu-id="c446e-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c446e-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="c446e-130">Validation File</span></span>  <br/> |<span data-ttu-id="c446e-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c446e-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c446e-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="c446e-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="c446e-133">False</span><span class="sxs-lookup"><span data-stu-id="c446e-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c446e-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c446e-134">See also</span></span>



[<span data-ttu-id="c446e-135">GetAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="c446e-135">GetAttachment operation</span></span>](getattachment-operation.md)
  
[<span data-ttu-id="c446e-136">GetAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="c446e-136">GetAttachmentResponse</span></span>](getattachmentresponse.md)

