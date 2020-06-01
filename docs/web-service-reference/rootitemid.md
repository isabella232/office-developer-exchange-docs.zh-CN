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
ms.openlocfilehash: d8badd465fd5a93e1a6354d55ac5c4b080897152
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457093"
---
# <a name="rootitemid"></a><span data-ttu-id="7af2c-103">RootItemId</span><span class="sxs-lookup"><span data-stu-id="7af2c-103">RootItemId</span></span>

<span data-ttu-id="7af2c-104">**RootItemId**元素标识已删除附件的根项目。</span><span class="sxs-lookup"><span data-stu-id="7af2c-104">The **RootItemId** element identifies the root item of a deleted attachment.</span></span> 
  
[<span data-ttu-id="7af2c-105">DeleteAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="7af2c-105">DeleteAttachmentResponse</span></span>](deleteattachmentresponse.md)
  
[<span data-ttu-id="7af2c-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="7af2c-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="7af2c-107">DeleteAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="7af2c-107">DeleteAttachmentResponseMessage</span></span>](deleteattachmentresponsemessage.md)
  
[<span data-ttu-id="7af2c-108">RootItemId</span><span class="sxs-lookup"><span data-stu-id="7af2c-108">RootItemId</span></span>](rootitemid.md)
  
```xml
<RootItemId RootItemId="" RootItemChangeKey="" />
```

 <span data-ttu-id="7af2c-109">**RootItemIdType**</span><span class="sxs-lookup"><span data-stu-id="7af2c-109">**RootItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7af2c-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7af2c-110">Attributes and elements</span></span>

<span data-ttu-id="7af2c-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7af2c-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7af2c-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="7af2c-112">Attributes</span></span>

|<span data-ttu-id="7af2c-113">**属性**</span><span class="sxs-lookup"><span data-stu-id="7af2c-113">**Attribute**</span></span>|<span data-ttu-id="7af2c-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="7af2c-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7af2c-115">**RootItemId**</span><span class="sxs-lookup"><span data-stu-id="7af2c-115">**RootItemId**</span></span> <br/> |<span data-ttu-id="7af2c-116">标识已删除附件的根项目。</span><span class="sxs-lookup"><span data-stu-id="7af2c-116">Identifies the root item of a deleted attachment.</span></span>  <br/> |
|<span data-ttu-id="7af2c-117">**RootItemChangeKey**</span><span class="sxs-lookup"><span data-stu-id="7af2c-117">**RootItemChangeKey**</span></span> <br/> |<span data-ttu-id="7af2c-118">标识已删除附件的根项的新更改键。</span><span class="sxs-lookup"><span data-stu-id="7af2c-118">Identifies the new change key of the root item of a deleted attachment.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7af2c-119">子元素</span><span class="sxs-lookup"><span data-stu-id="7af2c-119">Child elements</span></span>

<span data-ttu-id="7af2c-120">无。</span><span class="sxs-lookup"><span data-stu-id="7af2c-120">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7af2c-121">父元素</span><span class="sxs-lookup"><span data-stu-id="7af2c-121">Parent elements</span></span>

|<span data-ttu-id="7af2c-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="7af2c-122">**Element**</span></span>|<span data-ttu-id="7af2c-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="7af2c-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7af2c-124">DeleteAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="7af2c-124">DeleteAttachmentResponseMessage</span></span>](deleteattachmentresponsemessage.md) <br/> |<span data-ttu-id="7af2c-125">包含 DeleteAttachment 请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="7af2c-125">Contains the status and result of a DeleteAttachment request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7af2c-126">备注</span><span class="sxs-lookup"><span data-stu-id="7af2c-126">Remarks</span></span>

<span data-ttu-id="7af2c-127">**RootItemId**元素仅在 DeleteAttachment 响应中使用。</span><span class="sxs-lookup"><span data-stu-id="7af2c-127">The **RootItemId** element is only used in DeleteAttachment responses.</span></span> <span data-ttu-id="7af2c-128">这将标识根项标识符，更重要的是，新的更改键到父项。</span><span class="sxs-lookup"><span data-stu-id="7af2c-128">This identifies the root item identifier, and more importantly, the new change key to the parent item.</span></span> 
  
<span data-ttu-id="7af2c-129">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7af2c-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7af2c-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="7af2c-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7af2c-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="7af2c-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7af2c-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="7af2c-132">Schema name</span></span>  <br/> |<span data-ttu-id="7af2c-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="7af2c-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="7af2c-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="7af2c-134">Validation file</span></span>  <br/> |<span data-ttu-id="7af2c-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7af2c-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7af2c-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="7af2c-136">Can be empty</span></span>  <br/> |<span data-ttu-id="7af2c-137">False</span><span class="sxs-lookup"><span data-stu-id="7af2c-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7af2c-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7af2c-138">See also</span></span>



[<span data-ttu-id="7af2c-139">DeleteAttachment</span><span class="sxs-lookup"><span data-stu-id="7af2c-139">DeleteAttachment</span></span>](deleteattachment.md)
  
[<span data-ttu-id="7af2c-140">DeleteAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="7af2c-140">DeleteAttachment operation</span></span>](deleteattachment-operation.md)


- [<span data-ttu-id="7af2c-141">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="7af2c-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

