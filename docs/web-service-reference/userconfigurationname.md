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
description: UserConfigurationName 元素均表示用户配置对象的名称。 用户配置对象名称为用户配置对象的标识符。
ms.openlocfilehash: 40580343e92493c3d39b090371708269ec3274b9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838460"
---
# <a name="userconfigurationname"></a><span data-ttu-id="c706c-104">UserConfigurationName</span><span class="sxs-lookup"><span data-stu-id="c706c-104">UserConfigurationName</span></span>

<span data-ttu-id="c706c-105">**UserConfigurationName**元素均表示用户配置对象的名称。</span><span class="sxs-lookup"><span data-stu-id="c706c-105">The **UserConfigurationName** element represents the name of a user configuration object.</span></span> <span data-ttu-id="c706c-106">用户配置对象名称为用户配置对象的标识符。</span><span class="sxs-lookup"><span data-stu-id="c706c-106">The user configuration object name is the identifier for a user configuration object.</span></span> 
  
```XML
<UserConfigurationName Name="">
   <FolderId/>
</UserConfigurationName>
```

 <span data-ttu-id="c706c-107">**UserConfigurationNameType**</span><span class="sxs-lookup"><span data-stu-id="c706c-107">**UserConfigurationNameType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c706c-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c706c-108">Attributes and elements</span></span>

<span data-ttu-id="c706c-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c706c-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c706c-110">属性</span><span class="sxs-lookup"><span data-stu-id="c706c-110">Attributes</span></span>

|<span data-ttu-id="c706c-111">**属性**</span><span class="sxs-lookup"><span data-stu-id="c706c-111">**Attribute**</span></span>|<span data-ttu-id="c706c-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="c706c-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c706c-113">**名称**</span><span class="sxs-lookup"><span data-stu-id="c706c-113">**Name**</span></span> <br/> |<span data-ttu-id="c706c-114">包含一个 string 值，该值代表用户配置对象的名称。</span><span class="sxs-lookup"><span data-stu-id="c706c-114">Contains a string value that represents the name of a user configuration object.</span></span> <span data-ttu-id="c706c-115">此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="c706c-115">This attribute is required.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c706c-116">子元素</span><span class="sxs-lookup"><span data-stu-id="c706c-116">Child elements</span></span>

|<span data-ttu-id="c706c-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="c706c-117">**Element**</span></span>|<span data-ttu-id="c706c-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="c706c-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c706c-119">文件夹 Id</span><span class="sxs-lookup"><span data-stu-id="c706c-119">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="c706c-120">代表包含用户配置对象的文件夹的文件夹标识符。</span><span class="sxs-lookup"><span data-stu-id="c706c-120">Represents the folder identifier of the folder that contains the user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="c706c-121">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="c706c-121">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="c706c-122">代表包含用户配置对象的文件夹的可分辨的文件夹名称。</span><span class="sxs-lookup"><span data-stu-id="c706c-122">Represents a distinguished folder name of the folder that contains the user configuration object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c706c-123">父元素</span><span class="sxs-lookup"><span data-stu-id="c706c-123">Parent elements</span></span>

|<span data-ttu-id="c706c-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="c706c-124">**Element**</span></span>|<span data-ttu-id="c706c-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="c706c-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c706c-126">DeleteUserConfiguration</span><span class="sxs-lookup"><span data-stu-id="c706c-126">DeleteUserConfiguration</span></span>](deleteuserconfiguration.md) <br/> |<span data-ttu-id="c706c-127">表示要删除的用户配置对象的请求。</span><span class="sxs-lookup"><span data-stu-id="c706c-127">Represents a request to delete a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="c706c-128">GetUserConfiguration</span><span class="sxs-lookup"><span data-stu-id="c706c-128">GetUserConfiguration</span></span>](getuserconfiguration.md) <br/> |<span data-ttu-id="c706c-129">表示要获取的用户配置对象的请求。</span><span class="sxs-lookup"><span data-stu-id="c706c-129">Represents a request to get a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="c706c-130">UserConfiguration</span><span class="sxs-lookup"><span data-stu-id="c706c-130">UserConfiguration</span></span>](userconfiguration.md) <br/> |<span data-ttu-id="c706c-131">定义单个用户配置对象。</span><span class="sxs-lookup"><span data-stu-id="c706c-131">Defines a single user configuration object.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c706c-132">文本值</span><span class="sxs-lookup"><span data-stu-id="c706c-132">Text value</span></span>

<span data-ttu-id="c706c-133">无。</span><span class="sxs-lookup"><span data-stu-id="c706c-133">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c706c-134">备注</span><span class="sxs-lookup"><span data-stu-id="c706c-134">Remarks</span></span>

<span data-ttu-id="c706c-135">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c706c-135">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c706c-136">元素信息</span><span class="sxs-lookup"><span data-stu-id="c706c-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c706c-137">命名空间</span><span class="sxs-lookup"><span data-stu-id="c706c-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c706c-138">架构名称</span><span class="sxs-lookup"><span data-stu-id="c706c-138">Schema Name</span></span>  <br/> |<span data-ttu-id="c706c-139">类型架构</span><span class="sxs-lookup"><span data-stu-id="c706c-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="c706c-140">验证文件</span><span class="sxs-lookup"><span data-stu-id="c706c-140">Validation File</span></span>  <br/> |<span data-ttu-id="c706c-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c706c-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c706c-142">可以为空</span><span class="sxs-lookup"><span data-stu-id="c706c-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="c706c-143">False</span><span class="sxs-lookup"><span data-stu-id="c706c-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c706c-144">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c706c-144">See also</span></span>



- [<span data-ttu-id="c706c-145">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c706c-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

