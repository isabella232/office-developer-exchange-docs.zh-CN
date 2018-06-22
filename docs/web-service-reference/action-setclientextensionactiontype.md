---
title: 操作 (SetClientExtensionActionType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c5624a87-3436-40ce-8d6b-cc01eecab64d
description: Action 元素包含 Exchange server 上应用程序应采取的操作。
ms.openlocfilehash: a231cedfa6e4759dabfcbecfbe9a9b851f834247
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753099"
---
# <a name="action-setclientextensionactiontype"></a><span data-ttu-id="e853f-103">操作 (SetClientExtensionActionType)</span><span class="sxs-lookup"><span data-stu-id="e853f-103">Action (SetClientExtensionActionType)</span></span>

<span data-ttu-id="e853f-104">**Action**元素包含 Exchange server 上应用程序应采取的操作。</span><span class="sxs-lookup"><span data-stu-id="e853f-104">The **Action** element contains the action that the Exchange server should take on an app.</span></span> 
  
```XML
<Action ActionId="" ExtensionId="">
   <ClientExtension/>
</Action>
```

 <span data-ttu-id="e853f-105">**SetClientExtensionActionType**</span><span class="sxs-lookup"><span data-stu-id="e853f-105">**SetClientExtensionActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e853f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e853f-106">Attributes and elements</span></span>

<span data-ttu-id="e853f-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e853f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e853f-108">属性</span><span class="sxs-lookup"><span data-stu-id="e853f-108">Attributes</span></span>

|<span data-ttu-id="e853f-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="e853f-109">**Attribute**</span></span>|<span data-ttu-id="e853f-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="e853f-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e853f-111">ActionId</span><span class="sxs-lookup"><span data-stu-id="e853f-111">ActionId</span></span>  <br/> |<span data-ttu-id="e853f-112">指定操作的标识符。</span><span class="sxs-lookup"><span data-stu-id="e853f-112">Specifies the identifier of the action.</span></span> <span data-ttu-id="e853f-113">此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="e853f-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="e853f-114">ExtensionId</span><span class="sxs-lookup"><span data-stu-id="e853f-114">ExtensionId</span></span>  <br/> |<span data-ttu-id="e853f-115">指定的扩展的标识符。</span><span class="sxs-lookup"><span data-stu-id="e853f-115">Specifies the identifier of the extension.</span></span> <span data-ttu-id="e853f-116">此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="e853f-116">This attribute is optional.</span></span>  <br/> |
   
#### <a name="actionid"></a><span data-ttu-id="e853f-117">ActionId</span><span class="sxs-lookup"><span data-stu-id="e853f-117">ActionId</span></span>

|<span data-ttu-id="e853f-118">**值**</span><span class="sxs-lookup"><span data-stu-id="e853f-118">**Value**</span></span>|<span data-ttu-id="e853f-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="e853f-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e853f-120">配置</span><span class="sxs-lookup"><span data-stu-id="e853f-120">Configure</span></span>  <br/> |<span data-ttu-id="e853f-121">指示配置操作。</span><span class="sxs-lookup"><span data-stu-id="e853f-121">Indicates a configuration action.</span></span>  <br/> |
|<span data-ttu-id="e853f-122">安装</span><span class="sxs-lookup"><span data-stu-id="e853f-122">Install</span></span>  <br/> |<span data-ttu-id="e853f-123">指示安装操作。</span><span class="sxs-lookup"><span data-stu-id="e853f-123">Indicates an installation action.</span></span>  <br/> |
|<span data-ttu-id="e853f-124">卸载</span><span class="sxs-lookup"><span data-stu-id="e853f-124">Uninstall</span></span>  <br/> |<span data-ttu-id="e853f-125">指示卸载操作。</span><span class="sxs-lookup"><span data-stu-id="e853f-125">Indicates an uninstallation action.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e853f-126">子元素</span><span class="sxs-lookup"><span data-stu-id="e853f-126">Child elements</span></span>

|<span data-ttu-id="e853f-127">**元素**</span><span class="sxs-lookup"><span data-stu-id="e853f-127">**Element**</span></span>|<span data-ttu-id="e853f-128">**说明**</span><span class="sxs-lookup"><span data-stu-id="e853f-128">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e853f-129">ClientExtension</span><span class="sxs-lookup"><span data-stu-id="e853f-129">ClientExtension</span></span>](clientextension.md) <br/> |<span data-ttu-id="e853f-130">包含有关应用程序的用户和配置信息。</span><span class="sxs-lookup"><span data-stu-id="e853f-130">Contains user and configuration information about an app.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e853f-131">父元素</span><span class="sxs-lookup"><span data-stu-id="e853f-131">Parent elements</span></span>

|<span data-ttu-id="e853f-132">**元素**</span><span class="sxs-lookup"><span data-stu-id="e853f-132">**Element**</span></span>|<span data-ttu-id="e853f-133">**说明**</span><span class="sxs-lookup"><span data-stu-id="e853f-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e853f-134">操作 (ArrayOfSetClientExtensionActionsType)</span><span class="sxs-lookup"><span data-stu-id="e853f-134">Actions (ArrayOfSetClientExtensionActionsType)</span></span>](actions-arrayofsetclientextensionactionstype.md) <br/> |<span data-ttu-id="e853f-135">指定**Action**元素的数组。</span><span class="sxs-lookup"><span data-stu-id="e853f-135">Specifies an array of **Action** elements.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e853f-136">备注</span><span class="sxs-lookup"><span data-stu-id="e853f-136">Remarks</span></span>

<span data-ttu-id="e853f-137">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="e853f-137">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e853f-138">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e853f-138">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e853f-139">元素信息</span><span class="sxs-lookup"><span data-stu-id="e853f-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e853f-140">命名空间</span><span class="sxs-lookup"><span data-stu-id="e853f-140">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e853f-141">架构名称</span><span class="sxs-lookup"><span data-stu-id="e853f-141">Schema Name</span></span>  <br/> |<span data-ttu-id="e853f-142">类型架构</span><span class="sxs-lookup"><span data-stu-id="e853f-142">Type schema</span></span>  <br/> |
|<span data-ttu-id="e853f-143">验证文件</span><span class="sxs-lookup"><span data-stu-id="e853f-143">Validation File</span></span>  <br/> |<span data-ttu-id="e853f-144">types.xsd</span><span class="sxs-lookup"><span data-stu-id="e853f-144">types.xsd</span></span>  <br/> |
|<span data-ttu-id="e853f-145">可以为空</span><span class="sxs-lookup"><span data-stu-id="e853f-145">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="e853f-146">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e853f-146">See also</span></span>

- [<span data-ttu-id="e853f-147">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e853f-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

