---
title: AttachmentId （GetAttachment 和 DeleteAttachment）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AttachmentId
api_type:
- schema
ms.assetid: 4bea1cb5-0a0f-4e14-9b09-f91af8cf9899
description: AttachmentId 元素标识单个附件。
ms.openlocfilehash: 1096487490f6066f70d2da861b3015f0fbf5a68f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460853"
---
# <a name="attachmentid-getattachment-and-deleteattachment"></a><span data-ttu-id="1bc69-103">AttachmentId （GetAttachment 和 DeleteAttachment）</span><span class="sxs-lookup"><span data-stu-id="1bc69-103">AttachmentId (GetAttachment and DeleteAttachment)</span></span>

<span data-ttu-id="1bc69-104">**AttachmentId**元素标识单个附件。</span><span class="sxs-lookup"><span data-stu-id="1bc69-104">The **AttachmentId** element identifies a single attachment.</span></span> 
  
```xml
<AttachmentId Id="" />
```

 <span data-ttu-id="1bc69-105">**RequestAttachmentIdType**</span><span class="sxs-lookup"><span data-stu-id="1bc69-105">**RequestAttachmentIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1bc69-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1bc69-106">Attributes and elements</span></span>

<span data-ttu-id="1bc69-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1bc69-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1bc69-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="1bc69-108">Attributes</span></span>

|<span data-ttu-id="1bc69-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="1bc69-109">**Attribute**</span></span>|<span data-ttu-id="1bc69-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="1bc69-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1bc69-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="1bc69-111">**Id**</span></span> <br/> |<span data-ttu-id="1bc69-112">指定附件标识符。</span><span class="sxs-lookup"><span data-stu-id="1bc69-112">Specifies the attachment identifier.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1bc69-113">子元素</span><span class="sxs-lookup"><span data-stu-id="1bc69-113">Child elements</span></span>

<span data-ttu-id="1bc69-114">无。</span><span class="sxs-lookup"><span data-stu-id="1bc69-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1bc69-115">父元素</span><span class="sxs-lookup"><span data-stu-id="1bc69-115">Parent elements</span></span>

|<span data-ttu-id="1bc69-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="1bc69-116">**Element**</span></span>|<span data-ttu-id="1bc69-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="1bc69-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1bc69-118">会话</span><span class="sxs-lookup"><span data-stu-id="1bc69-118">AttachmentIds</span></span>](attachmentids.md) <br/> | <span data-ttu-id="1bc69-119">包含附件标识符的数组。</span><span class="sxs-lookup"><span data-stu-id="1bc69-119">Contains an array of attachment identifiers.</span></span><br/><br/>  <span data-ttu-id="1bc69-120">下面是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="1bc69-120">The following are the XPath expressions to this element:</span></span><br/><br/>`/DeleteAttachment/AttachmentIds`<br/><br/>`/GetAttachment/AttachmentIds` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1bc69-121">说明</span><span class="sxs-lookup"><span data-stu-id="1bc69-121">Remarks</span></span>

<span data-ttu-id="1bc69-122">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1bc69-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1bc69-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="1bc69-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1bc69-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="1bc69-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1bc69-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="1bc69-125">Schema Name</span></span>  <br/> |<span data-ttu-id="1bc69-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="1bc69-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="1bc69-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="1bc69-127">Validation File</span></span>  <br/> |<span data-ttu-id="1bc69-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1bc69-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1bc69-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="1bc69-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="1bc69-130">False</span><span class="sxs-lookup"><span data-stu-id="1bc69-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1bc69-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1bc69-131">See also</span></span>

- [<span data-ttu-id="1bc69-132">DeleteAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="1bc69-132">DeleteAttachment operation</span></span>](deleteattachment-operation.md)
- [<span data-ttu-id="1bc69-133">GetAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="1bc69-133">GetAttachment operation</span></span>](getattachment-operation.md)

