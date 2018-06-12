---
title: ResponseCode (InvalidRecipientResponseCodeType)
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
description: ResponseCode 元素提供了有关收件人无效的原因的信息。
ms.openlocfilehash: 3bff99dd1ac6603ce31d5ceb074e73ef48190bb2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827186"
---
# <a name="responsecode-invalidrecipientresponsecodetype"></a><span data-ttu-id="795e1-103">ResponseCode (InvalidRecipientResponseCodeType)</span><span class="sxs-lookup"><span data-stu-id="795e1-103">ResponseCode (InvalidRecipientResponseCodeType)</span></span>

<span data-ttu-id="795e1-104">**ResponseCode**元素提供了有关收件人无效的原因的信息。</span><span class="sxs-lookup"><span data-stu-id="795e1-104">The **ResponseCode** element provides information about why the recipient is invalid.</span></span> 
  
```XML
<ResponseCode>OtherError or RecipientOrganizationNotFederated or CannotObtainTokenFromSTS or SystemPolicyBlocksSharingWithThisRecipient or RecipientOrganizationFederatedWithUnknownTokenIssuer</ResponseCode>
```

 <span data-ttu-id="795e1-105">**InvalidRecipientResponseCodeType**</span><span class="sxs-lookup"><span data-stu-id="795e1-105">**InvalidRecipientResponseCodeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="795e1-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="795e1-106">Attributes and elements</span></span>

<span data-ttu-id="795e1-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="795e1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="795e1-108">属性</span><span class="sxs-lookup"><span data-stu-id="795e1-108">Attributes</span></span>

<span data-ttu-id="795e1-109">无。</span><span class="sxs-lookup"><span data-stu-id="795e1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="795e1-110">子元素</span><span class="sxs-lookup"><span data-stu-id="795e1-110">Child elements</span></span>

<span data-ttu-id="795e1-111">无。</span><span class="sxs-lookup"><span data-stu-id="795e1-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="795e1-112">父元素</span><span class="sxs-lookup"><span data-stu-id="795e1-112">Parent elements</span></span>

|<span data-ttu-id="795e1-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="795e1-113">**Element**</span></span>|<span data-ttu-id="795e1-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="795e1-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="795e1-115">InvalidRecipient</span><span class="sxs-lookup"><span data-stu-id="795e1-115">InvalidRecipient</span></span>](invalidrecipient.md) <br/> |<span data-ttu-id="795e1-116">包含无效的收件人和收件人无效的原因有关的信息的 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="795e1-116">Contains the SMTP address of the invalid recipient and information about why the recipient is invalid.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="795e1-117">文本值</span><span class="sxs-lookup"><span data-stu-id="795e1-117">Text value</span></span>

<span data-ttu-id="795e1-118">下表列出了**ResponseCode**元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="795e1-118">The following table lists the possible values for the **ResponseCode** element.</span></span> 
  
|<span data-ttu-id="795e1-119">**代码**</span><span class="sxs-lookup"><span data-stu-id="795e1-119">**Code**</span></span>|<span data-ttu-id="795e1-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="795e1-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="795e1-121">OtherError</span><span class="sxs-lookup"><span data-stu-id="795e1-121">OtherError</span></span>  <br/> |<span data-ttu-id="795e1-122">指示错误不由其他错误响应代码指定。</span><span class="sxs-lookup"><span data-stu-id="795e1-122">Indicates that the error is not specified by another error response code.</span></span>  <br/> |
|<span data-ttu-id="795e1-123">RecipientOrganizationNotFederated</span><span class="sxs-lookup"><span data-stu-id="795e1-123">RecipientOrganizationNotFederated</span></span>  <br/> |<span data-ttu-id="795e1-124">指示，共享关系都无法与组织中收件人的 SMTP 电子邮件地址指定。</span><span class="sxs-lookup"><span data-stu-id="795e1-124">Indicates that a sharing relationship is not available with the organization specified in the recipient's SMTP e-mail address.</span></span>  <br/> |
|<span data-ttu-id="795e1-125">CannotObtainTokenFromSTS</span><span class="sxs-lookup"><span data-stu-id="795e1-125">CannotObtainTokenFromSTS</span></span>  <br/> |<span data-ttu-id="795e1-126">指示出现从令牌服务器获取安全令牌问题。</span><span class="sxs-lookup"><span data-stu-id="795e1-126">Indicates that there was a problem obtaining a security token from the token server.</span></span>  <br/> |
|<span data-ttu-id="795e1-127">SystemPolicyBlocksSharingWithThisRecipient</span><span class="sxs-lookup"><span data-stu-id="795e1-127">SystemPolicyBlocksSharingWithThisRecipient</span></span>  <br/> |<span data-ttu-id="795e1-128">指示系统管理员已将阻止与指定的收件人共享系统策略设置。</span><span class="sxs-lookup"><span data-stu-id="795e1-128">Indicates that the system administrator has set a system policy that blocks sharing with the specified recipient.</span></span>  <br/> |
|<span data-ttu-id="795e1-129">RecipientOrganizationFederatedWithUnknownTokenIssuer</span><span class="sxs-lookup"><span data-stu-id="795e1-129">RecipientOrganizationFederatedWithUnknownTokenIssuer</span></span>  <br/> |<span data-ttu-id="795e1-130">指示由指定的收件人的安全令牌服务未知。</span><span class="sxs-lookup"><span data-stu-id="795e1-130">Indicates that the secure token service that is used by the specified recipient is unknown.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="795e1-131">备注</span><span class="sxs-lookup"><span data-stu-id="795e1-131">Remarks</span></span>

<span data-ttu-id="795e1-132">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="795e1-132">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="795e1-133">元素信息</span><span class="sxs-lookup"><span data-stu-id="795e1-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="795e1-134">命名空间</span><span class="sxs-lookup"><span data-stu-id="795e1-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="795e1-135">架构名称</span><span class="sxs-lookup"><span data-stu-id="795e1-135">Schema Name</span></span>  <br/> |<span data-ttu-id="795e1-136">类型架构</span><span class="sxs-lookup"><span data-stu-id="795e1-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="795e1-137">验证文件</span><span class="sxs-lookup"><span data-stu-id="795e1-137">Validation File</span></span>  <br/> |<span data-ttu-id="795e1-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="795e1-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="795e1-139">可以为空</span><span class="sxs-lookup"><span data-stu-id="795e1-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="795e1-140">False</span><span class="sxs-lookup"><span data-stu-id="795e1-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="795e1-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="795e1-141">See also</span></span>



[<span data-ttu-id="795e1-142">GetSharingMetadata 操作</span><span class="sxs-lookup"><span data-stu-id="795e1-142">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)


- [<span data-ttu-id="795e1-143">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="795e1-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

