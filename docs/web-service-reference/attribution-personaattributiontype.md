---
title: 归属 (PersonaAttributionType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dc59e17e-baea-4617-8ca1-4382a89de0d7
description: 属性元素指定实例 PersonaType 元素的属性数组中。
ms.openlocfilehash: 0e800c92c75bf0c475d4bffd33d6ab49f9ad9a9a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753291"
---
# <a name="attribution-personaattributiontype"></a><span data-ttu-id="8ee61-103">归属 (PersonaAttributionType)</span><span class="sxs-lookup"><span data-stu-id="8ee61-103">Attribution (PersonaAttributionType)</span></span>

<span data-ttu-id="8ee61-104">**属性**元素指定实例**PersonaType**元素的属性数组中。</span><span class="sxs-lookup"><span data-stu-id="8ee61-104">The **Attribution** element specifies an instance in an array of attributes for a **PersonaType** element.</span></span> 
  
```XML
<Attribution>
    <Id></Id>
    <SourceId></SourceId>
    <DisplayName></DisplayName>
    <IsWritable></IsWritable>
    <IsQuickContact></IsQuickContact>
    <IsHidden></IsHidden>
    <FolderId></FolderId>
</Attribution>
```

 <span data-ttu-id="8ee61-105">**PersonaAttributionType**</span><span class="sxs-lookup"><span data-stu-id="8ee61-105">**PersonaAttributionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8ee61-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8ee61-106">Attributes and elements</span></span>

<span data-ttu-id="8ee61-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8ee61-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8ee61-108">属性</span><span class="sxs-lookup"><span data-stu-id="8ee61-108">Attributes</span></span>

<span data-ttu-id="8ee61-109">无。</span><span class="sxs-lookup"><span data-stu-id="8ee61-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8ee61-110">子元素</span><span class="sxs-lookup"><span data-stu-id="8ee61-110">Child elements</span></span>

|<span data-ttu-id="8ee61-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="8ee61-111">**Element**</span></span>|<span data-ttu-id="8ee61-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="8ee61-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8ee61-113">ID （字符串）</span><span class="sxs-lookup"><span data-stu-id="8ee61-113">ID (String)</span></span>](id-string.md) <br/> |<span data-ttu-id="8ee61-114">指定一个唯一标识应用程序或在角色归属的字符串。</span><span class="sxs-lookup"><span data-stu-id="8ee61-114">Specifies a string that uniquely identifies an app or an attribution in a persona.</span></span>  <br/> |
|[<span data-ttu-id="8ee61-115">SourceId</span><span class="sxs-lookup"><span data-stu-id="8ee61-115">SourceId</span></span>](sourceid.md) <br/> |<span data-ttu-id="8ee61-116">指定的联系人或 Active Directory 收件人的标识符。</span><span class="sxs-lookup"><span data-stu-id="8ee61-116">Specifies the identifier of the contact or Active Directory recipient.</span></span>  <br/> |
|[<span data-ttu-id="8ee61-117">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="8ee61-117">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="8ee61-118">定义文件夹、 联系人、 通讯组列表、 代理用户或规则的显示名称。</span><span class="sxs-lookup"><span data-stu-id="8ee61-118">Defines the display name of a folder, contact, distribution list, delegate user, or rule.</span></span>  <br/> |
|[<span data-ttu-id="8ee61-119">IsWritable</span><span class="sxs-lookup"><span data-stu-id="8ee61-119">IsWritable</span></span>](iswritable.md) <br/> |<span data-ttu-id="8ee61-120">指定是否可以向写入基础联系人或 Active Directory 收件人。</span><span class="sxs-lookup"><span data-stu-id="8ee61-120">Specifies whether the underlying contact or Active Directory recipient can be written to.</span></span>  <br/> |
|[<span data-ttu-id="8ee61-121">IsQuickContact</span><span class="sxs-lookup"><span data-stu-id="8ee61-121">IsQuickContact</span></span>](isquickcontact.md) <br/> |<span data-ttu-id="8ee61-122">指定一个布尔值，指示快速联系人基础联系人或 Active Directory 收件人。</span><span class="sxs-lookup"><span data-stu-id="8ee61-122">Specifies a Boolean value that indicates whether the underlying contact or Active Directory recipient is a quick contact.</span></span>  <br/> |
|[<span data-ttu-id="8ee61-123">IsHidden</span><span class="sxs-lookup"><span data-stu-id="8ee61-123">IsHidden</span></span>](ishidden.md) <br/> |<span data-ttu-id="8ee61-124">包含一个布尔值，该值指示是否应隐藏或显示该角色的一部分的基础联系人或 Active Directory 收件人。</span><span class="sxs-lookup"><span data-stu-id="8ee61-124">Contains a Boolean value that indicates whether the underlying contact or Active Directory recipient should be hidden or displayed as part of the persona.</span></span>  <br/> |
|[<span data-ttu-id="8ee61-125">文件夹 Id</span><span class="sxs-lookup"><span data-stu-id="8ee61-125">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="8ee61-126">包含一个文件夹的标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="8ee61-126">Contains the identifier and change key of a folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8ee61-127">父元素</span><span class="sxs-lookup"><span data-stu-id="8ee61-127">Parent elements</span></span>

|<span data-ttu-id="8ee61-128">**元素**</span><span class="sxs-lookup"><span data-stu-id="8ee61-128">**Element**</span></span>|<span data-ttu-id="8ee61-129">**说明**</span><span class="sxs-lookup"><span data-stu-id="8ee61-129">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8ee61-130">归属 (ArrayOfPersonaAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="8ee61-130">Attributions (ArrayOfPersonaAttributionsType)</span></span>](attributions-arrayofpersonaattributionstype.md) <br/> |<span data-ttu-id="8ee61-131">指定一个或多个联系人或聚合到相关联的角色的 active directory (AD) 收件人的归属信息的数组。</span><span class="sxs-lookup"><span data-stu-id="8ee61-131">Specifies an array of attribution information for one or more of the contacts or active directory (AD) recipients aggregated into the associated persona.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8ee61-132">备注</span><span class="sxs-lookup"><span data-stu-id="8ee61-132">Remarks</span></span>

<span data-ttu-id="8ee61-133">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="8ee61-133">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="8ee61-134">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8ee61-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8ee61-135">元素信息</span><span class="sxs-lookup"><span data-stu-id="8ee61-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8ee61-136">命名空间</span><span class="sxs-lookup"><span data-stu-id="8ee61-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8ee61-137">架构名称</span><span class="sxs-lookup"><span data-stu-id="8ee61-137">Schema Name</span></span>  <br/> |<span data-ttu-id="8ee61-138">类型架构</span><span class="sxs-lookup"><span data-stu-id="8ee61-138">Type schema</span></span>  <br/> |
|<span data-ttu-id="8ee61-139">验证文件</span><span class="sxs-lookup"><span data-stu-id="8ee61-139">Validation File</span></span>  <br/> |<span data-ttu-id="8ee61-140">types.xsd</span><span class="sxs-lookup"><span data-stu-id="8ee61-140">types.xsd</span></span>  <br/> |
|<span data-ttu-id="8ee61-141">可以为空</span><span class="sxs-lookup"><span data-stu-id="8ee61-141">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="8ee61-142">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8ee61-142">See also</span></span>

- [<span data-ttu-id="8ee61-143">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="8ee61-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

