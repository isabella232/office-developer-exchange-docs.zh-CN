---
title: BaseFolderIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- BaseFolderIds
api_type:
- schema
ms.assetid: bdaa6093-f960-469a-b338-0e75aaa536c6
description: BaseFolderIds 元素均表示将用于确定搜索文件夹的内容的文件夹的集合。
ms.openlocfilehash: 960e4d9c1d6eb37bf988bf163e696cbba3e1ef6f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753308"
---
# <a name="basefolderids"></a><span data-ttu-id="4f61d-103">BaseFolderIds</span><span class="sxs-lookup"><span data-stu-id="4f61d-103">BaseFolderIds</span></span>

<span data-ttu-id="4f61d-104">**BaseFolderIds**元素均表示将用于确定搜索文件夹的内容的文件夹的集合。</span><span class="sxs-lookup"><span data-stu-id="4f61d-104">The **BaseFolderIds** element represents the collection of folders that will be mined to determine the contents of a search folder.</span></span> 
  
```xml
<BaseFolderIds>
   <FolderId/>
   <DistinguishedFolderId/>
</BaseFolderIds>
```

 <span data-ttu-id="4f61d-105">**NonEmptyArrayOfBaseFolderIdsType**</span><span class="sxs-lookup"><span data-stu-id="4f61d-105">**NonEmptyArrayOfBaseFolderIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4f61d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4f61d-106">Attributes and elements</span></span>

<span data-ttu-id="4f61d-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4f61d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4f61d-108">属性</span><span class="sxs-lookup"><span data-stu-id="4f61d-108">Attributes</span></span>

<span data-ttu-id="4f61d-109">无。</span><span class="sxs-lookup"><span data-stu-id="4f61d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4f61d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="4f61d-110">Child elements</span></span>

|<span data-ttu-id="4f61d-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="4f61d-111">**Element**</span></span>|<span data-ttu-id="4f61d-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="4f61d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4f61d-113">文件夹 Id</span><span class="sxs-lookup"><span data-stu-id="4f61d-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="4f61d-114">包含一个文件夹的标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="4f61d-114">Contains the identifier and change key of a folder.</span></span>  <br/> |
|[<span data-ttu-id="4f61d-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="4f61d-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="4f61d-116">标识可以通过名称引用的 MicrosoftExchange Server 2007 文件夹。</span><span class="sxs-lookup"><span data-stu-id="4f61d-116">Identifies MicrosoftExchange Server 2007 folders that can be referenced by name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4f61d-117">父元素</span><span class="sxs-lookup"><span data-stu-id="4f61d-117">Parent elements</span></span>

|<span data-ttu-id="4f61d-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="4f61d-118">**Element**</span></span>|<span data-ttu-id="4f61d-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="4f61d-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4f61d-120">SearchParameters</span><span class="sxs-lookup"><span data-stu-id="4f61d-120">SearchParameters</span></span>](searchparameters.md) <br/> |<span data-ttu-id="4f61d-121">表示定义搜索文件夹的参数。</span><span class="sxs-lookup"><span data-stu-id="4f61d-121">Represents the parameters that define a search folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4f61d-122">备注</span><span class="sxs-lookup"><span data-stu-id="4f61d-122">Remarks</span></span>

<span data-ttu-id="4f61d-123">**BaseFolderIds**元素必须包含至少一个[文件夹 Id](folderid.md)或[DistinguishedFolderId](distinguishedfolderid.md)元素。</span><span class="sxs-lookup"><span data-stu-id="4f61d-123">The **BaseFolderIds** element must contain at least one [FolderId](folderid.md) or [DistinguishedFolderId](distinguishedfolderid.md) element.</span></span> 
  
<span data-ttu-id="4f61d-124">描述此元素的架构位于运行 Exchange Server 2007 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="4f61d-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4f61d-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="4f61d-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4f61d-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="4f61d-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4f61d-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="4f61d-127">Schema name</span></span>  <br/> |<span data-ttu-id="4f61d-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="4f61d-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="4f61d-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="4f61d-129">Validation file</span></span>  <br/> |<span data-ttu-id="4f61d-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4f61d-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4f61d-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="4f61d-131">Can be empty</span></span>  <br/> |<span data-ttu-id="4f61d-132">False</span><span class="sxs-lookup"><span data-stu-id="4f61d-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4f61d-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4f61d-133">See also</span></span>



- [<span data-ttu-id="4f61d-134">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="4f61d-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

