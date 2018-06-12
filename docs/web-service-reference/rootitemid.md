---
title: RootItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RootItemId
api_type:
- schema
ms.assetid: f613c705-17ce-48ce-aa64-4dc2cea25e31
description: RootItemId 元素标识已删除附件的根项目。
ms.openlocfilehash: 484b185db63c9692eaca7e43c49d6e95375a1a98
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827251"
---
# <a name="rootitemid"></a><span data-ttu-id="8d27e-103">RootItemId</span><span class="sxs-lookup"><span data-stu-id="8d27e-103">RootItemId</span></span>

<span data-ttu-id="8d27e-104">**RootItemId**元素标识已删除附件的根项目。</span><span class="sxs-lookup"><span data-stu-id="8d27e-104">The **RootItemId** element identifies the root item of a deleted attachment.</span></span> 
  
[<span data-ttu-id="8d27e-105">DeleteAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="8d27e-105">DeleteAttachmentResponse</span></span>](deleteattachmentresponse.md)
  
[<span data-ttu-id="8d27e-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="8d27e-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="8d27e-107">DeleteAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="8d27e-107">DeleteAttachmentResponseMessage</span></span>](deleteattachmentresponsemessage.md)
  
[<span data-ttu-id="8d27e-108">RootItemId</span><span class="sxs-lookup"><span data-stu-id="8d27e-108">RootItemId</span></span>](rootitemid.md)
  
```xml
<RootItemId RootItemId="" RootItemChangeKey="" />
```

 <span data-ttu-id="8d27e-109">**RootItemIdType**</span><span class="sxs-lookup"><span data-stu-id="8d27e-109">**RootItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8d27e-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8d27e-110">Attributes and elements</span></span>

<span data-ttu-id="8d27e-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8d27e-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8d27e-112">属性</span><span class="sxs-lookup"><span data-stu-id="8d27e-112">Attributes</span></span>

|<span data-ttu-id="8d27e-113">**属性**</span><span class="sxs-lookup"><span data-stu-id="8d27e-113">**Attribute**</span></span>|<span data-ttu-id="8d27e-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="8d27e-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8d27e-115">**RootItemId**</span><span class="sxs-lookup"><span data-stu-id="8d27e-115">**RootItemId**</span></span> <br/> |<span data-ttu-id="8d27e-116">标识已删除附件的根项目。</span><span class="sxs-lookup"><span data-stu-id="8d27e-116">Identifies the root item of a deleted attachment.</span></span>  <br/> |
|<span data-ttu-id="8d27e-117">**RootItemChangeKey**</span><span class="sxs-lookup"><span data-stu-id="8d27e-117">**RootItemChangeKey**</span></span> <br/> |<span data-ttu-id="8d27e-118">标识已删除附件的根项目的新更改键。</span><span class="sxs-lookup"><span data-stu-id="8d27e-118">Identifies the new change key of the root item of a deleted attachment.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8d27e-119">子元素</span><span class="sxs-lookup"><span data-stu-id="8d27e-119">Child elements</span></span>

<span data-ttu-id="8d27e-120">无。</span><span class="sxs-lookup"><span data-stu-id="8d27e-120">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8d27e-121">父元素</span><span class="sxs-lookup"><span data-stu-id="8d27e-121">Parent elements</span></span>

|<span data-ttu-id="8d27e-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="8d27e-122">**Element**</span></span>|<span data-ttu-id="8d27e-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="8d27e-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8d27e-124">DeleteAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="8d27e-124">DeleteAttachmentResponseMessage</span></span>](deleteattachmentresponsemessage.md) <br/> |<span data-ttu-id="8d27e-125">包含状态和 DeleteAttachment 请求的结果。</span><span class="sxs-lookup"><span data-stu-id="8d27e-125">Contains the status and result of a DeleteAttachment request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8d27e-126">备注</span><span class="sxs-lookup"><span data-stu-id="8d27e-126">Remarks</span></span>

<span data-ttu-id="8d27e-127">在 DeleteAttachment 响应中仅使用**RootItemId**元素。</span><span class="sxs-lookup"><span data-stu-id="8d27e-127">The **RootItemId** element is only used in DeleteAttachment responses.</span></span> <span data-ttu-id="8d27e-128">这标识的根项目标识符，和更重要的是，与父项的新更改键。</span><span class="sxs-lookup"><span data-stu-id="8d27e-128">This identifies the root item identifier, and more importantly, the new change key to the parent item.</span></span> 
  
<span data-ttu-id="8d27e-129">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8d27e-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8d27e-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="8d27e-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8d27e-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="8d27e-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8d27e-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="8d27e-132">Schema name</span></span>  <br/> |<span data-ttu-id="8d27e-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="8d27e-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="8d27e-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="8d27e-134">Validation file</span></span>  <br/> |<span data-ttu-id="8d27e-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8d27e-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8d27e-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="8d27e-136">Can be empty</span></span>  <br/> |<span data-ttu-id="8d27e-137">False</span><span class="sxs-lookup"><span data-stu-id="8d27e-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8d27e-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8d27e-138">See also</span></span>



[<span data-ttu-id="8d27e-139">DeleteAttachment</span><span class="sxs-lookup"><span data-stu-id="8d27e-139">DeleteAttachment</span></span>](deleteattachment.md)
  
[<span data-ttu-id="8d27e-140">DeleteAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="8d27e-140">DeleteAttachment operation</span></span>](deleteattachment-operation.md)


- [<span data-ttu-id="8d27e-141">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="8d27e-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

