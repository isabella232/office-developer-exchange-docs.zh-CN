---
title: Action （SetClientExtensionActionType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c5624a87-3436-40ce-8d6b-cc01eecab64d
description: Action 元素包含 Exchange server 应对应用程序执行的操作。
ms.openlocfilehash: 29579e26377edacb5fb0bb8406144eeb116b8d15
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529684"
---
# <a name="action-setclientextensionactiontype"></a><span data-ttu-id="4efe8-103">Action （SetClientExtensionActionType）</span><span class="sxs-lookup"><span data-stu-id="4efe8-103">Action (SetClientExtensionActionType)</span></span>

<span data-ttu-id="4efe8-104">**Action**元素包含 Exchange server 应对应用程序执行的操作。</span><span class="sxs-lookup"><span data-stu-id="4efe8-104">The **Action** element contains the action that the Exchange server should take on an app.</span></span> 
  
```XML
<Action ActionId="" ExtensionId="">
   <ClientExtension/>
</Action>
```

 <span data-ttu-id="4efe8-105">**SetClientExtensionActionType**</span><span class="sxs-lookup"><span data-stu-id="4efe8-105">**SetClientExtensionActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4efe8-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4efe8-106">Attributes and elements</span></span>

<span data-ttu-id="4efe8-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4efe8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4efe8-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="4efe8-108">Attributes</span></span>

|<span data-ttu-id="4efe8-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="4efe8-109">**Attribute**</span></span>|<span data-ttu-id="4efe8-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="4efe8-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4efe8-111">ActionId</span><span class="sxs-lookup"><span data-stu-id="4efe8-111">ActionId</span></span>  <br/> |<span data-ttu-id="4efe8-112">指定操作的标识符。</span><span class="sxs-lookup"><span data-stu-id="4efe8-112">Specifies the identifier of the action.</span></span> <span data-ttu-id="4efe8-113">此特性是必需的。</span><span class="sxs-lookup"><span data-stu-id="4efe8-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="4efe8-114">ExtensionId</span><span class="sxs-lookup"><span data-stu-id="4efe8-114">ExtensionId</span></span>  <br/> |<span data-ttu-id="4efe8-115">指定扩展的标识符。</span><span class="sxs-lookup"><span data-stu-id="4efe8-115">Specifies the identifier of the extension.</span></span> <span data-ttu-id="4efe8-116">此特性是可选的。</span><span class="sxs-lookup"><span data-stu-id="4efe8-116">This attribute is optional.</span></span>  <br/> |
   
#### <a name="actionid"></a><span data-ttu-id="4efe8-117">ActionId</span><span class="sxs-lookup"><span data-stu-id="4efe8-117">ActionId</span></span>

|<span data-ttu-id="4efe8-118">**值**</span><span class="sxs-lookup"><span data-stu-id="4efe8-118">**Value**</span></span>|<span data-ttu-id="4efe8-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="4efe8-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4efe8-120">配置</span><span class="sxs-lookup"><span data-stu-id="4efe8-120">Configure</span></span>  <br/> |<span data-ttu-id="4efe8-121">指示配置操作。</span><span class="sxs-lookup"><span data-stu-id="4efe8-121">Indicates a configuration action.</span></span>  <br/> |
|<span data-ttu-id="4efe8-122">安装</span><span class="sxs-lookup"><span data-stu-id="4efe8-122">Install</span></span>  <br/> |<span data-ttu-id="4efe8-123">指示安装操作。</span><span class="sxs-lookup"><span data-stu-id="4efe8-123">Indicates an installation action.</span></span>  <br/> |
|<span data-ttu-id="4efe8-124">Uninstall</span><span class="sxs-lookup"><span data-stu-id="4efe8-124">Uninstall</span></span>  <br/> |<span data-ttu-id="4efe8-125">指示卸载操作。</span><span class="sxs-lookup"><span data-stu-id="4efe8-125">Indicates an uninstallation action.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4efe8-126">子元素</span><span class="sxs-lookup"><span data-stu-id="4efe8-126">Child elements</span></span>

|<span data-ttu-id="4efe8-127">**元素**</span><span class="sxs-lookup"><span data-stu-id="4efe8-127">**Element**</span></span>|<span data-ttu-id="4efe8-128">**描述**</span><span class="sxs-lookup"><span data-stu-id="4efe8-128">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4efe8-129">ClientExtension</span><span class="sxs-lookup"><span data-stu-id="4efe8-129">ClientExtension</span></span>](clientextension.md) <br/> |<span data-ttu-id="4efe8-130">包含有关应用程序的用户和配置信息。</span><span class="sxs-lookup"><span data-stu-id="4efe8-130">Contains user and configuration information about an app.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4efe8-131">父元素</span><span class="sxs-lookup"><span data-stu-id="4efe8-131">Parent elements</span></span>

|<span data-ttu-id="4efe8-132">**元素**</span><span class="sxs-lookup"><span data-stu-id="4efe8-132">**Element**</span></span>|<span data-ttu-id="4efe8-133">**描述**</span><span class="sxs-lookup"><span data-stu-id="4efe8-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4efe8-134">操作（ArrayOfSetClientExtensionActionsType）</span><span class="sxs-lookup"><span data-stu-id="4efe8-134">Actions (ArrayOfSetClientExtensionActionsType)</span></span>](actions-arrayofsetclientextensionactionstype.md) <br/> |<span data-ttu-id="4efe8-135">指定**Action**元素的数组。</span><span class="sxs-lookup"><span data-stu-id="4efe8-135">Specifies an array of **Action** elements.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4efe8-136">备注</span><span class="sxs-lookup"><span data-stu-id="4efe8-136">Remarks</span></span>

<span data-ttu-id="4efe8-137">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="4efe8-137">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="4efe8-138">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="4efe8-138">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4efe8-139">元素信息</span><span class="sxs-lookup"><span data-stu-id="4efe8-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4efe8-140">命名空间</span><span class="sxs-lookup"><span data-stu-id="4efe8-140">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4efe8-141">架构名称</span><span class="sxs-lookup"><span data-stu-id="4efe8-141">Schema Name</span></span>  <br/> |<span data-ttu-id="4efe8-142">类型架构</span><span class="sxs-lookup"><span data-stu-id="4efe8-142">Type schema</span></span>  <br/> |
|<span data-ttu-id="4efe8-143">验证文件</span><span class="sxs-lookup"><span data-stu-id="4efe8-143">Validation File</span></span>  <br/> |<span data-ttu-id="4efe8-144">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="4efe8-144">types.xsd</span></span>  <br/> |
|<span data-ttu-id="4efe8-145">可以为空</span><span class="sxs-lookup"><span data-stu-id="4efe8-145">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="4efe8-146">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4efe8-146">See also</span></span>

- [<span data-ttu-id="4efe8-147">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="4efe8-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

