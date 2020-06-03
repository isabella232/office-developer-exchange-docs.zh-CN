---
title: ResponseCode （InvalidRecipientResponseCodeType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResponseCode
api_type:
- schema
ms.assetid: 582e9caa-d2bc-4be1-a460-739294f9ef18
description: ResponseCode 元素提供有关收件人无效的原因的信息。
ms.openlocfilehash: d78de64de7725007ec51a55dad13d1cc892a25e6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529719"
---
# <a name="responsecode-invalidrecipientresponsecodetype"></a><span data-ttu-id="7ef01-103">ResponseCode （InvalidRecipientResponseCodeType）</span><span class="sxs-lookup"><span data-stu-id="7ef01-103">ResponseCode (InvalidRecipientResponseCodeType)</span></span>

<span data-ttu-id="7ef01-104">**ResponseCode**元素提供有关收件人无效的原因的信息。</span><span class="sxs-lookup"><span data-stu-id="7ef01-104">The **ResponseCode** element provides information about why the recipient is invalid.</span></span> 
  
```XML
<ResponseCode>OtherError or RecipientOrganizationNotFederated or CannotObtainTokenFromSTS or SystemPolicyBlocksSharingWithThisRecipient or RecipientOrganizationFederatedWithUnknownTokenIssuer</ResponseCode>
```

 <span data-ttu-id="7ef01-105">**InvalidRecipientResponseCodeType**</span><span class="sxs-lookup"><span data-stu-id="7ef01-105">**InvalidRecipientResponseCodeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7ef01-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7ef01-106">Attributes and elements</span></span>

<span data-ttu-id="7ef01-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7ef01-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7ef01-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="7ef01-108">Attributes</span></span>

<span data-ttu-id="7ef01-109">无。</span><span class="sxs-lookup"><span data-stu-id="7ef01-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7ef01-110">子元素</span><span class="sxs-lookup"><span data-stu-id="7ef01-110">Child elements</span></span>

<span data-ttu-id="7ef01-111">无。</span><span class="sxs-lookup"><span data-stu-id="7ef01-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7ef01-112">父元素</span><span class="sxs-lookup"><span data-stu-id="7ef01-112">Parent elements</span></span>

|<span data-ttu-id="7ef01-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="7ef01-113">**Element**</span></span>|<span data-ttu-id="7ef01-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="7ef01-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7ef01-115">InvalidRecipient</span><span class="sxs-lookup"><span data-stu-id="7ef01-115">InvalidRecipient</span></span>](invalidrecipient.md) <br/> |<span data-ttu-id="7ef01-116">包含无效的收件人和收件人无效的原因有关的信息的 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="7ef01-116">Contains the SMTP address of the invalid recipient and information about why the recipient is invalid.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7ef01-117">文本值</span><span class="sxs-lookup"><span data-stu-id="7ef01-117">Text value</span></span>

<span data-ttu-id="7ef01-118">下表列出了**ResponseCode**元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="7ef01-118">The following table lists the possible values for the **ResponseCode** element.</span></span> 
  
|<span data-ttu-id="7ef01-119">**代码**</span><span class="sxs-lookup"><span data-stu-id="7ef01-119">**Code**</span></span>|<span data-ttu-id="7ef01-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="7ef01-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7ef01-121">OtherError</span><span class="sxs-lookup"><span data-stu-id="7ef01-121">OtherError</span></span>  <br/> |<span data-ttu-id="7ef01-122">指示错误不是由另一个错误响应代码指定的。</span><span class="sxs-lookup"><span data-stu-id="7ef01-122">Indicates that the error is not specified by another error response code.</span></span>  <br/> |
|<span data-ttu-id="7ef01-123">RecipientOrganizationNotFederated</span><span class="sxs-lookup"><span data-stu-id="7ef01-123">RecipientOrganizationNotFederated</span></span>  <br/> |<span data-ttu-id="7ef01-124">表示共享关系对收件人的 SMTP 电子邮件地址中指定的组织不可用。</span><span class="sxs-lookup"><span data-stu-id="7ef01-124">Indicates that a sharing relationship is not available with the organization specified in the recipient's SMTP e-mail address.</span></span>  <br/> |
|<span data-ttu-id="7ef01-125">CannotObtainTokenFromSTS</span><span class="sxs-lookup"><span data-stu-id="7ef01-125">CannotObtainTokenFromSTS</span></span>  <br/> |<span data-ttu-id="7ef01-126">指示从令牌服务器获取安全令牌时出现问题。</span><span class="sxs-lookup"><span data-stu-id="7ef01-126">Indicates that there was a problem obtaining a security token from the token server.</span></span>  <br/> |
|<span data-ttu-id="7ef01-127">SystemPolicyBlocksSharingWithThisRecipient</span><span class="sxs-lookup"><span data-stu-id="7ef01-127">SystemPolicyBlocksSharingWithThisRecipient</span></span>  <br/> |<span data-ttu-id="7ef01-128">指示系统管理员已设置阻止与指定收件人共享的系统策略。</span><span class="sxs-lookup"><span data-stu-id="7ef01-128">Indicates that the system administrator has set a system policy that blocks sharing with the specified recipient.</span></span>  <br/> |
|<span data-ttu-id="7ef01-129">RecipientOrganizationFederatedWithUnknownTokenIssuer</span><span class="sxs-lookup"><span data-stu-id="7ef01-129">RecipientOrganizationFederatedWithUnknownTokenIssuer</span></span>  <br/> |<span data-ttu-id="7ef01-130">指示指定的收件人所使用的安全令牌服务是未知的。</span><span class="sxs-lookup"><span data-stu-id="7ef01-130">Indicates that the secure token service that is used by the specified recipient is unknown.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7ef01-131">说明</span><span class="sxs-lookup"><span data-stu-id="7ef01-131">Remarks</span></span>

<span data-ttu-id="7ef01-132">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7ef01-132">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7ef01-133">元素信息</span><span class="sxs-lookup"><span data-stu-id="7ef01-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7ef01-134">命名空间</span><span class="sxs-lookup"><span data-stu-id="7ef01-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7ef01-135">架构名称</span><span class="sxs-lookup"><span data-stu-id="7ef01-135">Schema Name</span></span>  <br/> |<span data-ttu-id="7ef01-136">类型架构</span><span class="sxs-lookup"><span data-stu-id="7ef01-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="7ef01-137">验证文件</span><span class="sxs-lookup"><span data-stu-id="7ef01-137">Validation File</span></span>  <br/> |<span data-ttu-id="7ef01-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7ef01-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7ef01-139">可以为空</span><span class="sxs-lookup"><span data-stu-id="7ef01-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="7ef01-140">False</span><span class="sxs-lookup"><span data-stu-id="7ef01-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7ef01-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7ef01-141">See also</span></span>



[<span data-ttu-id="7ef01-142">GetSharingMetadata 操作</span><span class="sxs-lookup"><span data-stu-id="7ef01-142">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)


- [<span data-ttu-id="7ef01-143">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="7ef01-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

