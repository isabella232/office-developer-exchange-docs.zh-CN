---
title: UserConfigurationName
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UserConfigurationName
api_type:
- schema
ms.assetid: 6947dd03-9727-4379-9b9d-42373fa120c7
description: UserConfigurationName 元素表示用户配置对象的名称。 "用户配置" 对象名称是 "用户配置" 对象的标识符。
ms.openlocfilehash: 020b55919f7f81602a5eb072652d82168607d306
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466029"
---
# <a name="userconfigurationname"></a><span data-ttu-id="baa91-104">UserConfigurationName</span><span class="sxs-lookup"><span data-stu-id="baa91-104">UserConfigurationName</span></span>

<span data-ttu-id="baa91-105">**UserConfigurationName**元素表示用户配置对象的名称。</span><span class="sxs-lookup"><span data-stu-id="baa91-105">The **UserConfigurationName** element represents the name of a user configuration object.</span></span> <span data-ttu-id="baa91-106">"用户配置" 对象名称是 "用户配置" 对象的标识符。</span><span class="sxs-lookup"><span data-stu-id="baa91-106">The user configuration object name is the identifier for a user configuration object.</span></span> 
  
```XML
<UserConfigurationName Name="">
   <FolderId/>
</UserConfigurationName>
```

```XML
<UserConfigurationName Name="">
   <DistinguishedFolderId/> 
</UserConfigurationName>
```

<span data-ttu-id="baa91-107">**UserConfigurationNameType**</span><span class="sxs-lookup"><span data-stu-id="baa91-107">**UserConfigurationNameType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="baa91-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="baa91-108">Attributes and elements</span></span>

<span data-ttu-id="baa91-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="baa91-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="baa91-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="baa91-110">Attributes</span></span>

|<span data-ttu-id="baa91-111">**属性**</span><span class="sxs-lookup"><span data-stu-id="baa91-111">**Attribute**</span></span>|<span data-ttu-id="baa91-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="baa91-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="baa91-113">**名称**</span><span class="sxs-lookup"><span data-stu-id="baa91-113">**Name**</span></span> <br/> |<span data-ttu-id="baa91-114">包含一个 string 值，它代表用户配置对象的名称。</span><span class="sxs-lookup"><span data-stu-id="baa91-114">Contains a string value that represents the name of a user configuration object.</span></span> <span data-ttu-id="baa91-115">此特性是必需的。</span><span class="sxs-lookup"><span data-stu-id="baa91-115">This attribute is required.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="baa91-116">子元素</span><span class="sxs-lookup"><span data-stu-id="baa91-116">Child elements</span></span>

|<span data-ttu-id="baa91-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="baa91-117">**Element**</span></span>|<span data-ttu-id="baa91-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="baa91-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="baa91-119">FolderId</span><span class="sxs-lookup"><span data-stu-id="baa91-119">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="baa91-120">表示包含用户配置对象的文件夹的文件夹标识符。</span><span class="sxs-lookup"><span data-stu-id="baa91-120">Represents the folder identifier of the folder that contains the user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="baa91-121">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="baa91-121">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="baa91-122">表示包含用户配置对象的文件夹的可分辨文件夹名称。</span><span class="sxs-lookup"><span data-stu-id="baa91-122">Represents a distinguished folder name of the folder that contains the user configuration object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="baa91-123">父元素</span><span class="sxs-lookup"><span data-stu-id="baa91-123">Parent elements</span></span>

|<span data-ttu-id="baa91-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="baa91-124">**Element**</span></span>|<span data-ttu-id="baa91-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="baa91-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="baa91-126">DeleteUserConfiguration</span><span class="sxs-lookup"><span data-stu-id="baa91-126">DeleteUserConfiguration</span></span>](deleteuserconfiguration.md) <br/> |<span data-ttu-id="baa91-127">表示一个删除用户配置对象的请求。</span><span class="sxs-lookup"><span data-stu-id="baa91-127">Represents a request to delete a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="baa91-128">GetUserConfiguration</span><span class="sxs-lookup"><span data-stu-id="baa91-128">GetUserConfiguration</span></span>](getuserconfiguration.md) <br/> |<span data-ttu-id="baa91-129">表示获取用户配置对象的请求。</span><span class="sxs-lookup"><span data-stu-id="baa91-129">Represents a request to get a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="baa91-130">UserConfiguration</span><span class="sxs-lookup"><span data-stu-id="baa91-130">UserConfiguration</span></span>](userconfiguration.md) <br/> |<span data-ttu-id="baa91-131">定义单个用户配置对象。</span><span class="sxs-lookup"><span data-stu-id="baa91-131">Defines a single user configuration object.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="baa91-132">文本值</span><span class="sxs-lookup"><span data-stu-id="baa91-132">Text value</span></span>

<span data-ttu-id="baa91-133">无。</span><span class="sxs-lookup"><span data-stu-id="baa91-133">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="baa91-134">说明</span><span class="sxs-lookup"><span data-stu-id="baa91-134">Remarks</span></span>

<span data-ttu-id="baa91-135">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="baa91-135">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="baa91-136">元素信息</span><span class="sxs-lookup"><span data-stu-id="baa91-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="baa91-137">命名空间</span><span class="sxs-lookup"><span data-stu-id="baa91-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="baa91-138">架构名称</span><span class="sxs-lookup"><span data-stu-id="baa91-138">Schema Name</span></span>  <br/> |<span data-ttu-id="baa91-139">类型架构</span><span class="sxs-lookup"><span data-stu-id="baa91-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="baa91-140">验证文件</span><span class="sxs-lookup"><span data-stu-id="baa91-140">Validation File</span></span>  <br/> |<span data-ttu-id="baa91-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="baa91-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="baa91-142">可以为空</span><span class="sxs-lookup"><span data-stu-id="baa91-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="baa91-143">False</span><span class="sxs-lookup"><span data-stu-id="baa91-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="baa91-144">另请参阅</span><span class="sxs-lookup"><span data-stu-id="baa91-144">See also</span></span>

- [<span data-ttu-id="baa91-145">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="baa91-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

