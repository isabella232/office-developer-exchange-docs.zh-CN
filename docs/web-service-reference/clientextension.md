---
title: ClientExtension
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3445ef2b-1bb1-43ea-bc93-85c72401e5b6
description: ClientExtension 元素包含有关应用程序的用户和配置信息。
ms.openlocfilehash: 5051248a2c8e664d82666bd7b42ee3c3046f43fe
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753452"
---
# <a name="clientextension"></a><span data-ttu-id="62d48-103">ClientExtension</span><span class="sxs-lookup"><span data-stu-id="62d48-103">ClientExtension</span></span>

<span data-ttu-id="62d48-104">**ClientExtension**元素包含有关应用程序的用户和配置信息。</span><span class="sxs-lookup"><span data-stu-id="62d48-104">The **ClientExtension** element contains user and configuration information about an app.</span></span> 
  
```XML
<ClientExtension IsAvailable=" true | false " IsMandatory=" true | false " IsEnabledByDefault=" true | false " Type="" Scope="" MarketplaceAssetId="" MarketplaceContentMarket="" AppStatus="" Etoken="">
    <SpecificUsers></SpecificUsers>
    <Manifest></Manifest>
</ClientExtension>
```

 <span data-ttu-id="62d48-105">**ClientExtensionType**</span><span class="sxs-lookup"><span data-stu-id="62d48-105">**ClientExtensionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="62d48-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="62d48-106">Attributes and elements</span></span>

<span data-ttu-id="62d48-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="62d48-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="62d48-108">属性</span><span class="sxs-lookup"><span data-stu-id="62d48-108">Attributes</span></span>

|<span data-ttu-id="62d48-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="62d48-109">**Attribute**</span></span>|<span data-ttu-id="62d48-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="62d48-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="62d48-111">IsAvailable</span><span class="sxs-lookup"><span data-stu-id="62d48-111">IsAvailable</span></span>  <br/> |<span data-ttu-id="62d48-112">指定应用程序是否可用。</span><span class="sxs-lookup"><span data-stu-id="62d48-112">Specifies whether the app is available.</span></span> <span data-ttu-id="62d48-113">文本值为**true**的**IsAvailable**属性指示应用程序可用。</span><span class="sxs-lookup"><span data-stu-id="62d48-113">A text value of **true** for the **IsAvailable** attribute indicates that the app is available.</span></span> <span data-ttu-id="62d48-114">如果值为**false**指示应用程序不可用。</span><span class="sxs-lookup"><span data-stu-id="62d48-114">A value of **false** indicates that the app is not available.</span></span> <span data-ttu-id="62d48-115">此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="62d48-115">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="62d48-116">IsMandatory</span><span class="sxs-lookup"><span data-stu-id="62d48-116">IsMandatory</span></span>  <br/> |<span data-ttu-id="62d48-117">指定是否强制应用程序。</span><span class="sxs-lookup"><span data-stu-id="62d48-117">Specifies whether the app is mandatory.</span></span> <span data-ttu-id="62d48-118">文本值为**true**的**IsMandatory**属性指示应用程序是必需的邮箱。</span><span class="sxs-lookup"><span data-stu-id="62d48-118">A text value of **true** for the **IsMandatory** attribute indicates that the app is mandatory for the mailbox.</span></span> <span data-ttu-id="62d48-119">如果值为**false**指示应用程序不是强制性。</span><span class="sxs-lookup"><span data-stu-id="62d48-119">A value of **false** indicates that the app is not mandatory.</span></span> <span data-ttu-id="62d48-120">此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="62d48-120">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="62d48-121">IsEnabledByDefault</span><span class="sxs-lookup"><span data-stu-id="62d48-121">IsEnabledByDefault</span></span>  <br/> |<span data-ttu-id="62d48-122">指定默认情况下是否启用应用程序。</span><span class="sxs-lookup"><span data-stu-id="62d48-122">Specifies whether the app is enabled by default.</span></span> <span data-ttu-id="62d48-123">文本值为**true**的**IsEnabledByDefault**属性指示，默认启用应用程序。</span><span class="sxs-lookup"><span data-stu-id="62d48-123">A text value of **true** for the **IsEnabledByDefault** attribute indicates that the app is enabled by default.</span></span> <span data-ttu-id="62d48-124">如果值为**false**指示，默认情况下不启用应用程序。</span><span class="sxs-lookup"><span data-stu-id="62d48-124">A value of **false** indicates that the app is not enabled by default.</span></span> <span data-ttu-id="62d48-125">此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="62d48-125">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="62d48-126">ProvidedTo</span><span class="sxs-lookup"><span data-stu-id="62d48-126">ProvidedTo</span></span>  <br/> |<span data-ttu-id="62d48-127">指定向其提供应用程序。</span><span class="sxs-lookup"><span data-stu-id="62d48-127">Specifies to whom the app is provided.</span></span> <span data-ttu-id="62d48-128">此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="62d48-128">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="62d48-129">类型</span><span class="sxs-lookup"><span data-stu-id="62d48-129">Type</span></span>  <br/> |<span data-ttu-id="62d48-130">指定应用程序的类型。</span><span class="sxs-lookup"><span data-stu-id="62d48-130">Specifies the type of the app.</span></span>  <br/> |
|<span data-ttu-id="62d48-131">范围</span><span class="sxs-lookup"><span data-stu-id="62d48-131">Scope</span></span>  <br/> |<span data-ttu-id="62d48-132">指定应用程序的范围。</span><span class="sxs-lookup"><span data-stu-id="62d48-132">Specifies the scope of the app.</span></span>  <br/> |
|<span data-ttu-id="62d48-133">MarketplaceAssetId</span><span class="sxs-lookup"><span data-stu-id="62d48-133">MarketplaceAssetId</span></span>  <br/> |<span data-ttu-id="62d48-134">指定应用程序的市场资产标识符。</span><span class="sxs-lookup"><span data-stu-id="62d48-134">Specifies the marketplace asset identifier of the app.</span></span>  <br/> |
|<span data-ttu-id="62d48-135">MarketplaceContentMarket</span><span class="sxs-lookup"><span data-stu-id="62d48-135">MarketplaceContentMarket</span></span>  <br/> |<span data-ttu-id="62d48-136">指定的商城内容的用户看到的详细信息，并回顾有关应用程序。</span><span class="sxs-lookup"><span data-stu-id="62d48-136">Specifies the marketplace content that a user sees for details and reviews about an app.</span></span>  <br/> |
|<span data-ttu-id="62d48-137">AppStatus</span><span class="sxs-lookup"><span data-stu-id="62d48-137">AppStatus</span></span>  <br/> |<span data-ttu-id="62d48-138">在意外状态指定邮件应用程序的状态代码。</span><span class="sxs-lookup"><span data-stu-id="62d48-138">Specifies the status code of a mail app in an unexpected state.</span></span>  <br/> |
|<span data-ttu-id="62d48-139">Etoken</span><span class="sxs-lookup"><span data-stu-id="62d48-139">Etoken</span></span>  <br/> |<span data-ttu-id="62d48-140">指定付费或试用邮件应用程序许可证令牌。</span><span class="sxs-lookup"><span data-stu-id="62d48-140">Specifies the license token for paid or trial mail apps.</span></span>  <br/> |
   
#### <a name="type"></a><span data-ttu-id="62d48-141">类型</span><span class="sxs-lookup"><span data-stu-id="62d48-141">Type</span></span>

|<span data-ttu-id="62d48-142">**值**</span><span class="sxs-lookup"><span data-stu-id="62d48-142">**Value**</span></span>|<span data-ttu-id="62d48-143">**说明**</span><span class="sxs-lookup"><span data-stu-id="62d48-143">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="62d48-144">默认</span><span class="sxs-lookup"><span data-stu-id="62d48-144">Default</span></span>  <br/> |<span data-ttu-id="62d48-145">指示应用程序是默认情况下可用。</span><span class="sxs-lookup"><span data-stu-id="62d48-145">Indicates that the app is available by default.</span></span>  <br/> |
|<span data-ttu-id="62d48-146">私有</span><span class="sxs-lookup"><span data-stu-id="62d48-146">Private</span></span>  <br/> |<span data-ttu-id="62d48-147">指示专用应用程序。</span><span class="sxs-lookup"><span data-stu-id="62d48-147">Indicates that the app is private.</span></span>  <br/> |
|<span data-ttu-id="62d48-148">市场</span><span class="sxs-lookup"><span data-stu-id="62d48-148">MarketPlace</span></span>  <br/> |<span data-ttu-id="62d48-149">指示应用程序的市场应用程序。</span><span class="sxs-lookup"><span data-stu-id="62d48-149">Indicates that the app is a marketplace app.</span></span>  <br/> |
   
#### <a name="scope"></a><span data-ttu-id="62d48-150">范围</span><span class="sxs-lookup"><span data-stu-id="62d48-150">Scope</span></span>

|<span data-ttu-id="62d48-151">**值**</span><span class="sxs-lookup"><span data-stu-id="62d48-151">**Value**</span></span>|<span data-ttu-id="62d48-152">**说明**</span><span class="sxs-lookup"><span data-stu-id="62d48-152">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="62d48-153">无</span><span class="sxs-lookup"><span data-stu-id="62d48-153">None</span></span>  <br/> |<span data-ttu-id="62d48-154">指示应用程序有无作用域。</span><span class="sxs-lookup"><span data-stu-id="62d48-154">Indicates that the app has no scope.</span></span>  <br/> |
|<span data-ttu-id="62d48-155">用户</span><span class="sxs-lookup"><span data-stu-id="62d48-155">User</span></span>  <br/> |<span data-ttu-id="62d48-156">指示应用程序是每个用户。</span><span class="sxs-lookup"><span data-stu-id="62d48-156">Indicates that the app is per user.</span></span>  <br/> |
|<span data-ttu-id="62d48-157">组织</span><span class="sxs-lookup"><span data-stu-id="62d48-157">Organization</span></span>  <br/> |<span data-ttu-id="62d48-158">指示应用程序的组织。</span><span class="sxs-lookup"><span data-stu-id="62d48-158">Indicates that the app is for an organization.</span></span>  <br/> |
|<span data-ttu-id="62d48-159">默认</span><span class="sxs-lookup"><span data-stu-id="62d48-159">Default</span></span>  <br/> |<span data-ttu-id="62d48-160">指示应用程序的默认应用程序。</span><span class="sxs-lookup"><span data-stu-id="62d48-160">Indicates that the app is a default app.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="62d48-161">子元素</span><span class="sxs-lookup"><span data-stu-id="62d48-161">Child elements</span></span>

|<span data-ttu-id="62d48-162">**元素**</span><span class="sxs-lookup"><span data-stu-id="62d48-162">**Element**</span></span>|<span data-ttu-id="62d48-163">**说明**</span><span class="sxs-lookup"><span data-stu-id="62d48-163">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="62d48-164">SpecificUsers</span><span class="sxs-lookup"><span data-stu-id="62d48-164">SpecificUsers</span></span>](specificusers.md) <br/> |<span data-ttu-id="62d48-165">指定可以访问应用程序的电子邮件帐户。</span><span class="sxs-lookup"><span data-stu-id="62d48-165">Specifies the email accounts that can access the app.</span></span>  <br/> |
|[<span data-ttu-id="62d48-166">Manifest</span><span class="sxs-lookup"><span data-stu-id="62d48-166">Manifest</span></span>](manifest.md) <br/> |<span data-ttu-id="62d48-167">包含 base64 编码的应用程序清单文件。</span><span class="sxs-lookup"><span data-stu-id="62d48-167">Contains the base-64 encoded app manifest file.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="62d48-168">父元素</span><span class="sxs-lookup"><span data-stu-id="62d48-168">Parent elements</span></span>

|<span data-ttu-id="62d48-169">**元素**</span><span class="sxs-lookup"><span data-stu-id="62d48-169">**Element**</span></span>|<span data-ttu-id="62d48-170">**说明**</span><span class="sxs-lookup"><span data-stu-id="62d48-170">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="62d48-171">ClientExtensions</span><span class="sxs-lookup"><span data-stu-id="62d48-171">ClientExtensions</span></span>](clientextensions.md) <br/> |<span data-ttu-id="62d48-172">指定**ClientExtension**元素的数组。</span><span class="sxs-lookup"><span data-stu-id="62d48-172">Specifies an array of **ClientExtension** elements.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="62d48-173">备注</span><span class="sxs-lookup"><span data-stu-id="62d48-173">Remarks</span></span>

<span data-ttu-id="62d48-174">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="62d48-174">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="62d48-175">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="62d48-175">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="62d48-176">元素信息</span><span class="sxs-lookup"><span data-stu-id="62d48-176">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="62d48-177">命名空间</span><span class="sxs-lookup"><span data-stu-id="62d48-177">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="62d48-178">架构名称</span><span class="sxs-lookup"><span data-stu-id="62d48-178">Schema Name</span></span>  <br/> |<span data-ttu-id="62d48-179">类型架构</span><span class="sxs-lookup"><span data-stu-id="62d48-179">Type schema</span></span>  <br/> |
|<span data-ttu-id="62d48-180">验证文件</span><span class="sxs-lookup"><span data-stu-id="62d48-180">Validation File</span></span>  <br/> |<span data-ttu-id="62d48-181">types.xsd</span><span class="sxs-lookup"><span data-stu-id="62d48-181">types.xsd</span></span>  <br/> |
|<span data-ttu-id="62d48-182">可以为空</span><span class="sxs-lookup"><span data-stu-id="62d48-182">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="62d48-183">另请参阅</span><span class="sxs-lookup"><span data-stu-id="62d48-183">See also</span></span>



- [<span data-ttu-id="62d48-184">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="62d48-184">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

