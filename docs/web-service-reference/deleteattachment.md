---
title: DeleteAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteAttachment
api_type:
- schema
ms.assetid: 43d0c1cb-92ca-4399-9b3a-acb2b5c22624
description: DeleteAttachment 元素是从 Exchange 存储中删除附件的请求中的根元素。
ms.openlocfilehash: 2beedd647febf025f6e3140ec37b196c9aeb7611
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753786"
---
# <a name="deleteattachment"></a><span data-ttu-id="91a7d-103">DeleteAttachment</span><span class="sxs-lookup"><span data-stu-id="91a7d-103">DeleteAttachment</span></span>

<span data-ttu-id="91a7d-104">**DeleteAttachment**元素是从 Exchange 存储中删除附件的请求中的根元素。</span><span class="sxs-lookup"><span data-stu-id="91a7d-104">The **DeleteAttachment** element is the root element in a request to delete an attachment from the Exchange store.</span></span> 
  
```xml
<DeleteAttachment>
   <AttachmentIds/>
</DeleteAttachment>
```

<span data-ttu-id="91a7d-105">**DeleteAttachmentType**</span><span class="sxs-lookup"><span data-stu-id="91a7d-105">**DeleteAttachmentType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="91a7d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="91a7d-106">Attributes and elements</span></span>

<span data-ttu-id="91a7d-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="91a7d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="91a7d-108">属性</span><span class="sxs-lookup"><span data-stu-id="91a7d-108">Attributes</span></span>

<span data-ttu-id="91a7d-109">无。</span><span class="sxs-lookup"><span data-stu-id="91a7d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="91a7d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="91a7d-110">Child elements</span></span>

|<span data-ttu-id="91a7d-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="91a7d-111">**Element**</span></span>|<span data-ttu-id="91a7d-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="91a7d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="91a7d-113">AttachmentIds</span><span class="sxs-lookup"><span data-stu-id="91a7d-113">AttachmentIds</span></span>](attachmentids.md) <br/> |<span data-ttu-id="91a7d-114">包含用于删除附件的附件标识符的数组。</span><span class="sxs-lookup"><span data-stu-id="91a7d-114">Contains an array of attachment identifiers that are used to delete the attachments.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="91a7d-115">父元素</span><span class="sxs-lookup"><span data-stu-id="91a7d-115">Parent elements</span></span>

<span data-ttu-id="91a7d-116">无。</span><span class="sxs-lookup"><span data-stu-id="91a7d-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="91a7d-117">备注</span><span class="sxs-lookup"><span data-stu-id="91a7d-117">Remarks</span></span>

<span data-ttu-id="91a7d-118">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="91a7d-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="91a7d-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="91a7d-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="91a7d-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="91a7d-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="91a7d-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="91a7d-121">Schema Name</span></span>  <br/> |<span data-ttu-id="91a7d-122">消息架构</span><span class="sxs-lookup"><span data-stu-id="91a7d-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="91a7d-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="91a7d-123">Validation File</span></span>  <br/> |<span data-ttu-id="91a7d-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="91a7d-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="91a7d-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="91a7d-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="91a7d-126">False</span><span class="sxs-lookup"><span data-stu-id="91a7d-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="91a7d-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="91a7d-127">See also</span></span>

- [<span data-ttu-id="91a7d-128">DeleteAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="91a7d-128">DeleteAttachment operation</span></span>](deleteattachment-operation.md)

