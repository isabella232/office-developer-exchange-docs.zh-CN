---
title: SearchParameters
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SearchParameters
api_type:
- schema
ms.assetid: 34602cb1-dc33-4552-a98c-3e77f614daa3
description: SearchParameters 元素表示用于定义搜索文件夹的参数。
ms.openlocfilehash: cd9f255621b17d01113392e67a0301b01b70f326
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466666"
---
# <a name="searchparameters"></a><span data-ttu-id="54e05-103">SearchParameters</span><span class="sxs-lookup"><span data-stu-id="54e05-103">SearchParameters</span></span>

<span data-ttu-id="54e05-104">**SearchParameters**元素表示用于定义搜索文件夹的参数。</span><span class="sxs-lookup"><span data-stu-id="54e05-104">The **SearchParameters** element represents the parameters that define a search folder.</span></span> 
  
```xml
<SearchParameters Traversal="">
   <Restriction/>
   <BaseFolderIds/>
</SearchParameters>
```

 <span data-ttu-id="54e05-105">**SearchParametersType**</span><span class="sxs-lookup"><span data-stu-id="54e05-105">**SearchParametersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="54e05-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="54e05-106">Attributes and elements</span></span>

<span data-ttu-id="54e05-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="54e05-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="54e05-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="54e05-108">Attributes</span></span>

|<span data-ttu-id="54e05-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="54e05-109">**Attribute**</span></span>|<span data-ttu-id="54e05-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="54e05-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="54e05-111">**遍历**</span><span class="sxs-lookup"><span data-stu-id="54e05-111">**Traversal**</span></span> <br/> |<span data-ttu-id="54e05-112">介绍搜索文件夹如何遍历文件夹层次结构。</span><span class="sxs-lookup"><span data-stu-id="54e05-112">Describes how a search folder traverses the folder hierarchy.</span></span> <span data-ttu-id="54e05-113">选项包括**深度**搜索或**浅表**搜索。</span><span class="sxs-lookup"><span data-stu-id="54e05-113">The options are for either a **Deep** or a **Shallow** search.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="54e05-114">子元素</span><span class="sxs-lookup"><span data-stu-id="54e05-114">Child elements</span></span>

|<span data-ttu-id="54e05-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="54e05-115">**Element**</span></span>|<span data-ttu-id="54e05-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="54e05-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="54e05-117">限制</span><span class="sxs-lookup"><span data-stu-id="54e05-117">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="54e05-118">表示用于在 FindItem/FindFolder 中筛选项目或文件夹和搜索文件夹操作的限制或查询。</span><span class="sxs-lookup"><span data-stu-id="54e05-118">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="54e05-119">BaseFolderIds</span><span class="sxs-lookup"><span data-stu-id="54e05-119">BaseFolderIds</span></span>](basefolderids.md) <br/> |<span data-ttu-id="54e05-120">表示将挖掘的文件夹集合，以确定搜索文件夹的内容。</span><span class="sxs-lookup"><span data-stu-id="54e05-120">Represents the collection of folders that will be mined to determine the contents of a search folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="54e05-121">父元素</span><span class="sxs-lookup"><span data-stu-id="54e05-121">Parent elements</span></span>

|<span data-ttu-id="54e05-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="54e05-122">**Element**</span></span>|<span data-ttu-id="54e05-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="54e05-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="54e05-124">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="54e05-124">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="54e05-125">表示邮箱中包含的搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="54e05-125">Represents a search folder that is contained in a mailbox.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="54e05-126">说明</span><span class="sxs-lookup"><span data-stu-id="54e05-126">Remarks</span></span>

<span data-ttu-id="54e05-127">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="54e05-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="54e05-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="54e05-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="54e05-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="54e05-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="54e05-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="54e05-130">Schema Name</span></span>  <br/> |<span data-ttu-id="54e05-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="54e05-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="54e05-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="54e05-132">Validation File</span></span>  <br/> |<span data-ttu-id="54e05-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="54e05-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="54e05-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="54e05-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="54e05-135">False</span><span class="sxs-lookup"><span data-stu-id="54e05-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="54e05-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="54e05-136">See also</span></span>



- [<span data-ttu-id="54e05-137">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="54e05-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

