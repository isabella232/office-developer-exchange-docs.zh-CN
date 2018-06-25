---
title: InvalidRecipients
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- InvalidRecipients
api_type:
- schema
ms.assetid: e4e7b50e-2fa9-4649-94a6-6002f341ecc4
description: InvalidRecipients元素表示无效的收件人共享请求的文件夹。
ms.openlocfilehash: 02ad8935bde347c563875bf5bfb31968b70d81b6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825966"
---
# <a name="invalidrecipients"></a><span data-ttu-id="fdaed-103">InvalidRecipients</span><span class="sxs-lookup"><span data-stu-id="fdaed-103">InvalidRecipients</span></span>

<span data-ttu-id="fdaed-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **InvalidRecipients**元素表示无效的收件人共享请求的文件夹。</span><span class="sxs-lookup"><span data-stu-id="fdaed-104">The **InvalidRecipients** element represents the recipients of a folder sharing request that are invalid.</span></span> 
  
```XML
<InvalidRecipients>
   <InvalidRecipient/>
</InvalidRecipients>
```

 <span data-ttu-id="fdaed-105">**ArrayOfInvalidRecipientsType**</span><span class="sxs-lookup"><span data-stu-id="fdaed-105">**ArrayOfInvalidRecipientsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fdaed-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fdaed-106">Attributes and elements</span></span>

<span data-ttu-id="fdaed-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fdaed-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fdaed-108">属性</span><span class="sxs-lookup"><span data-stu-id="fdaed-108">Attributes</span></span>

<span data-ttu-id="fdaed-109">无。</span><span class="sxs-lookup"><span data-stu-id="fdaed-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fdaed-110">子元素</span><span class="sxs-lookup"><span data-stu-id="fdaed-110">Child elements</span></span>

|<span data-ttu-id="fdaed-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="fdaed-111">**Element**</span></span>|<span data-ttu-id="fdaed-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="fdaed-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fdaed-113">InvalidRecipient</span><span class="sxs-lookup"><span data-stu-id="fdaed-113">InvalidRecipient</span></span>](invalidrecipient.md) <br/> |<span data-ttu-id="fdaed-114">包含无效的收件人和收件人无效的原因有关的信息的 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="fdaed-114">Contains the SMTP address of the invalid recipient and information about why the recipient is invalid.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fdaed-115">父元素</span><span class="sxs-lookup"><span data-stu-id="fdaed-115">Parent elements</span></span>

|<span data-ttu-id="fdaed-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="fdaed-116">**Element**</span></span>|<span data-ttu-id="fdaed-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="fdaed-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fdaed-118">GetSharingMetadataResponse</span><span class="sxs-lookup"><span data-stu-id="fdaed-118">GetSharingMetadataResponse</span></span>](getsharingmetadataresponse.md) <br/> |<span data-ttu-id="fdaed-119">定义一个[GetSharingMetadata 操作](getsharingmetadata-operation.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="fdaed-119">Defines a response to a [GetSharingMetadata operation](getsharingmetadata-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="fdaed-120">GetSharingMetadataResponseMessage</span><span class="sxs-lookup"><span data-stu-id="fdaed-120">GetSharingMetadataResponseMessage</span></span>](getsharingmetadataresponsemessage.md) <br/> |<span data-ttu-id="fdaed-121">包含状态和一个[GetSharingMetadata 操作](getsharingmetadata-operation.md)请求的结果。</span><span class="sxs-lookup"><span data-stu-id="fdaed-121">Contains the status and result of a single [GetSharingMetadata operation](getsharingmetadata-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fdaed-122">备注</span><span class="sxs-lookup"><span data-stu-id="fdaed-122">Remarks</span></span>

<span data-ttu-id="fdaed-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="fdaed-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fdaed-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="fdaed-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fdaed-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="fdaed-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="fdaed-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="fdaed-126">Schema Name</span></span>  <br/> |<span data-ttu-id="fdaed-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="fdaed-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="fdaed-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="fdaed-128">Validation File</span></span>  <br/> |<span data-ttu-id="fdaed-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="fdaed-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="fdaed-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="fdaed-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="fdaed-131">False</span><span class="sxs-lookup"><span data-stu-id="fdaed-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fdaed-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fdaed-132">See also</span></span>



[<span data-ttu-id="fdaed-133">GetSharingMetadata 操作</span><span class="sxs-lookup"><span data-stu-id="fdaed-133">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)


- [<span data-ttu-id="fdaed-134">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="fdaed-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

