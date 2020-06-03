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
ms.openlocfilehash: d3d9ce1d242a63f28da3464f0faff86abde502c9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460195"
---
# <a name="clientextension"></a><span data-ttu-id="f5270-103">ClientExtension</span><span class="sxs-lookup"><span data-stu-id="f5270-103">ClientExtension</span></span>

<span data-ttu-id="f5270-104">**ClientExtension**元素包含有关应用程序的用户和配置信息。</span><span class="sxs-lookup"><span data-stu-id="f5270-104">The **ClientExtension** element contains user and configuration information about an app.</span></span> 
  
```XML
<ClientExtension IsAvailable=" true | false " IsMandatory=" true | false " IsEnabledByDefault=" true | false " Type="" Scope="" MarketplaceAssetId="" MarketplaceContentMarket="" AppStatus="" Etoken="">
    <SpecificUsers></SpecificUsers>
    <Manifest></Manifest>
</ClientExtension>
```

 <span data-ttu-id="f5270-105">**ClientExtensionType**</span><span class="sxs-lookup"><span data-stu-id="f5270-105">**ClientExtensionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f5270-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f5270-106">Attributes and elements</span></span>

<span data-ttu-id="f5270-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f5270-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f5270-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="f5270-108">Attributes</span></span>

|<span data-ttu-id="f5270-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="f5270-109">**Attribute**</span></span>|<span data-ttu-id="f5270-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="f5270-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f5270-111">IsAvailable</span><span class="sxs-lookup"><span data-stu-id="f5270-111">IsAvailable</span></span>  <br/> |<span data-ttu-id="f5270-112">指定应用程序是否可用。</span><span class="sxs-lookup"><span data-stu-id="f5270-112">Specifies whether the app is available.</span></span> <span data-ttu-id="f5270-113">**IsAvailable**属性的文本值为**true**表示应用程序可用。</span><span class="sxs-lookup"><span data-stu-id="f5270-113">A text value of **true** for the **IsAvailable** attribute indicates that the app is available.</span></span> <span data-ttu-id="f5270-114">**如果值为 false** ，则表示应用程序不可用。</span><span class="sxs-lookup"><span data-stu-id="f5270-114">A value of **false** indicates that the app is not available.</span></span> <span data-ttu-id="f5270-115">此特性是可选的。</span><span class="sxs-lookup"><span data-stu-id="f5270-115">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="f5270-116">IsMandatory</span><span class="sxs-lookup"><span data-stu-id="f5270-116">IsMandatory</span></span>  <br/> |<span data-ttu-id="f5270-117">指定应用程序是否是必需的。</span><span class="sxs-lookup"><span data-stu-id="f5270-117">Specifies whether the app is mandatory.</span></span> <span data-ttu-id="f5270-118">**IsMandatory**属性的文本值为**true**表示该应用程序对邮箱是必需的。</span><span class="sxs-lookup"><span data-stu-id="f5270-118">A text value of **true** for the **IsMandatory** attribute indicates that the app is mandatory for the mailbox.</span></span> <span data-ttu-id="f5270-119">**如果值为 false** ，则表示应用程序不是强制性的。</span><span class="sxs-lookup"><span data-stu-id="f5270-119">A value of **false** indicates that the app is not mandatory.</span></span> <span data-ttu-id="f5270-120">此特性是可选的。</span><span class="sxs-lookup"><span data-stu-id="f5270-120">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="f5270-121">IsEnabledByDefault</span><span class="sxs-lookup"><span data-stu-id="f5270-121">IsEnabledByDefault</span></span>  <br/> |<span data-ttu-id="f5270-122">指定是否在默认情况下启用应用程序。</span><span class="sxs-lookup"><span data-stu-id="f5270-122">Specifies whether the app is enabled by default.</span></span> <span data-ttu-id="f5270-123">**IsEnabledByDefault**属性的文本值为**true**表示应用程序在默认情况下处于启用状态。</span><span class="sxs-lookup"><span data-stu-id="f5270-123">A text value of **true** for the **IsEnabledByDefault** attribute indicates that the app is enabled by default.</span></span> <span data-ttu-id="f5270-124">**如果值为 false** ，则表示应用程序默认情况下不启用。</span><span class="sxs-lookup"><span data-stu-id="f5270-124">A value of **false** indicates that the app is not enabled by default.</span></span> <span data-ttu-id="f5270-125">此特性是可选的。</span><span class="sxs-lookup"><span data-stu-id="f5270-125">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="f5270-126">ProvidedTo</span><span class="sxs-lookup"><span data-stu-id="f5270-126">ProvidedTo</span></span>  <br/> |<span data-ttu-id="f5270-127">指定向其提供应用程序的人员。</span><span class="sxs-lookup"><span data-stu-id="f5270-127">Specifies to whom the app is provided.</span></span> <span data-ttu-id="f5270-128">此特性是可选的。</span><span class="sxs-lookup"><span data-stu-id="f5270-128">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="f5270-129">类型</span><span class="sxs-lookup"><span data-stu-id="f5270-129">Type</span></span>  <br/> |<span data-ttu-id="f5270-130">指定应用程序的类型。</span><span class="sxs-lookup"><span data-stu-id="f5270-130">Specifies the type of the app.</span></span>  <br/> |
|<span data-ttu-id="f5270-131">范围</span><span class="sxs-lookup"><span data-stu-id="f5270-131">Scope</span></span>  <br/> |<span data-ttu-id="f5270-132">指定应用程序的范围。</span><span class="sxs-lookup"><span data-stu-id="f5270-132">Specifies the scope of the app.</span></span>  <br/> |
|<span data-ttu-id="f5270-133">MarketplaceAssetId</span><span class="sxs-lookup"><span data-stu-id="f5270-133">MarketplaceAssetId</span></span>  <br/> |<span data-ttu-id="f5270-134">指定应用程序的市场资产标识符。</span><span class="sxs-lookup"><span data-stu-id="f5270-134">Specifies the marketplace asset identifier of the app.</span></span>  <br/> |
|<span data-ttu-id="f5270-135">MarketplaceContentMarket</span><span class="sxs-lookup"><span data-stu-id="f5270-135">MarketplaceContentMarket</span></span>  <br/> |<span data-ttu-id="f5270-136">指定用户查看的有关应用程序的详细信息和评论的市场内容。</span><span class="sxs-lookup"><span data-stu-id="f5270-136">Specifies the marketplace content that a user sees for details and reviews about an app.</span></span>  <br/> |
|<span data-ttu-id="f5270-137">AppStatus</span><span class="sxs-lookup"><span data-stu-id="f5270-137">AppStatus</span></span>  <br/> |<span data-ttu-id="f5270-138">指定邮件应用程序处于意外状态时的状态代码。</span><span class="sxs-lookup"><span data-stu-id="f5270-138">Specifies the status code of a mail app in an unexpected state.</span></span>  <br/> |
|<span data-ttu-id="f5270-139">Etoken</span><span class="sxs-lookup"><span data-stu-id="f5270-139">Etoken</span></span>  <br/> |<span data-ttu-id="f5270-140">指定付费或试用邮件应用程序的许可证令牌。</span><span class="sxs-lookup"><span data-stu-id="f5270-140">Specifies the license token for paid or trial mail apps.</span></span>  <br/> |
   
#### <a name="type"></a><span data-ttu-id="f5270-141">类型</span><span class="sxs-lookup"><span data-stu-id="f5270-141">Type</span></span>

|<span data-ttu-id="f5270-142">**值**</span><span class="sxs-lookup"><span data-stu-id="f5270-142">**Value**</span></span>|<span data-ttu-id="f5270-143">**说明**</span><span class="sxs-lookup"><span data-stu-id="f5270-143">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f5270-144">默认</span><span class="sxs-lookup"><span data-stu-id="f5270-144">Default</span></span>  <br/> |<span data-ttu-id="f5270-145">指示应用程序在默认情况下可用。</span><span class="sxs-lookup"><span data-stu-id="f5270-145">Indicates that the app is available by default.</span></span>  <br/> |
|<span data-ttu-id="f5270-146">Private</span><span class="sxs-lookup"><span data-stu-id="f5270-146">Private</span></span>  <br/> |<span data-ttu-id="f5270-147">指示应用程序是私有的。</span><span class="sxs-lookup"><span data-stu-id="f5270-147">Indicates that the app is private.</span></span>  <br/> |
|<span data-ttu-id="f5270-148">市场</span><span class="sxs-lookup"><span data-stu-id="f5270-148">MarketPlace</span></span>  <br/> |<span data-ttu-id="f5270-149">指示应用程序是市场应用程序。</span><span class="sxs-lookup"><span data-stu-id="f5270-149">Indicates that the app is a marketplace app.</span></span>  <br/> |
   
#### <a name="scope"></a><span data-ttu-id="f5270-150">范围</span><span class="sxs-lookup"><span data-stu-id="f5270-150">Scope</span></span>

|<span data-ttu-id="f5270-151">**值**</span><span class="sxs-lookup"><span data-stu-id="f5270-151">**Value**</span></span>|<span data-ttu-id="f5270-152">**说明**</span><span class="sxs-lookup"><span data-stu-id="f5270-152">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f5270-153">无</span><span class="sxs-lookup"><span data-stu-id="f5270-153">None</span></span>  <br/> |<span data-ttu-id="f5270-154">指示应用程序没有作用域。</span><span class="sxs-lookup"><span data-stu-id="f5270-154">Indicates that the app has no scope.</span></span>  <br/> |
|<span data-ttu-id="f5270-155">User</span><span class="sxs-lookup"><span data-stu-id="f5270-155">User</span></span>  <br/> |<span data-ttu-id="f5270-156">指示应用程序是每个用户。</span><span class="sxs-lookup"><span data-stu-id="f5270-156">Indicates that the app is per user.</span></span>  <br/> |
|<span data-ttu-id="f5270-157">组织</span><span class="sxs-lookup"><span data-stu-id="f5270-157">Organization</span></span>  <br/> |<span data-ttu-id="f5270-158">指示应用程序适用于组织。</span><span class="sxs-lookup"><span data-stu-id="f5270-158">Indicates that the app is for an organization.</span></span>  <br/> |
|<span data-ttu-id="f5270-159">默认</span><span class="sxs-lookup"><span data-stu-id="f5270-159">Default</span></span>  <br/> |<span data-ttu-id="f5270-160">指示应用程序是默认应用程序。</span><span class="sxs-lookup"><span data-stu-id="f5270-160">Indicates that the app is a default app.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f5270-161">子元素</span><span class="sxs-lookup"><span data-stu-id="f5270-161">Child elements</span></span>

|<span data-ttu-id="f5270-162">**元素**</span><span class="sxs-lookup"><span data-stu-id="f5270-162">**Element**</span></span>|<span data-ttu-id="f5270-163">**描述**</span><span class="sxs-lookup"><span data-stu-id="f5270-163">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f5270-164">SpecificUsers</span><span class="sxs-lookup"><span data-stu-id="f5270-164">SpecificUsers</span></span>](specificusers.md) <br/> |<span data-ttu-id="f5270-165">指定可访问应用程序的电子邮件帐户。</span><span class="sxs-lookup"><span data-stu-id="f5270-165">Specifies the email accounts that can access the app.</span></span>  <br/> |
|[<span data-ttu-id="f5270-166">清单</span><span class="sxs-lookup"><span data-stu-id="f5270-166">Manifest</span></span>](manifest.md) <br/> |<span data-ttu-id="f5270-167">包含 base-64 编码的应用程序清单文件。</span><span class="sxs-lookup"><span data-stu-id="f5270-167">Contains the base-64 encoded app manifest file.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f5270-168">父元素</span><span class="sxs-lookup"><span data-stu-id="f5270-168">Parent elements</span></span>

|<span data-ttu-id="f5270-169">**元素**</span><span class="sxs-lookup"><span data-stu-id="f5270-169">**Element**</span></span>|<span data-ttu-id="f5270-170">**描述**</span><span class="sxs-lookup"><span data-stu-id="f5270-170">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f5270-171">ClientExtensions</span><span class="sxs-lookup"><span data-stu-id="f5270-171">ClientExtensions</span></span>](clientextensions.md) <br/> |<span data-ttu-id="f5270-172">指定**ClientExtension**元素的数组。</span><span class="sxs-lookup"><span data-stu-id="f5270-172">Specifies an array of **ClientExtension** elements.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f5270-173">备注</span><span class="sxs-lookup"><span data-stu-id="f5270-173">Remarks</span></span>

<span data-ttu-id="f5270-174">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="f5270-174">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="f5270-175">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f5270-175">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f5270-176">元素信息</span><span class="sxs-lookup"><span data-stu-id="f5270-176">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f5270-177">命名空间</span><span class="sxs-lookup"><span data-stu-id="f5270-177">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f5270-178">架构名称</span><span class="sxs-lookup"><span data-stu-id="f5270-178">Schema Name</span></span>  <br/> |<span data-ttu-id="f5270-179">类型架构</span><span class="sxs-lookup"><span data-stu-id="f5270-179">Type schema</span></span>  <br/> |
|<span data-ttu-id="f5270-180">验证文件</span><span class="sxs-lookup"><span data-stu-id="f5270-180">Validation File</span></span>  <br/> |<span data-ttu-id="f5270-181">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="f5270-181">types.xsd</span></span>  <br/> |
|<span data-ttu-id="f5270-182">可以为空</span><span class="sxs-lookup"><span data-stu-id="f5270-182">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="f5270-183">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f5270-183">See also</span></span>



- [<span data-ttu-id="f5270-184">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f5270-184">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

