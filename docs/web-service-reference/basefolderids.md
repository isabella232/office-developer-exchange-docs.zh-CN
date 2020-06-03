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
description: BaseFolderIds 元素表示将挖掘的文件夹集合，以确定搜索文件夹的内容。
ms.openlocfilehash: 97159ec1ded685e63aafedfaf90a06eff39adaab
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460265"
---
# <a name="basefolderids"></a><span data-ttu-id="01157-103">BaseFolderIds</span><span class="sxs-lookup"><span data-stu-id="01157-103">BaseFolderIds</span></span>

<span data-ttu-id="01157-104">**BaseFolderIds**元素表示将挖掘的文件夹集合，以确定搜索文件夹的内容。</span><span class="sxs-lookup"><span data-stu-id="01157-104">The **BaseFolderIds** element represents the collection of folders that will be mined to determine the contents of a search folder.</span></span> 
  
```xml
<BaseFolderIds>
   <FolderId/>
   <DistinguishedFolderId/>
</BaseFolderIds>
```

 <span data-ttu-id="01157-105">**NonEmptyArrayOfBaseFolderIdsType**</span><span class="sxs-lookup"><span data-stu-id="01157-105">**NonEmptyArrayOfBaseFolderIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="01157-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="01157-106">Attributes and elements</span></span>

<span data-ttu-id="01157-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="01157-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="01157-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="01157-108">Attributes</span></span>

<span data-ttu-id="01157-109">无。</span><span class="sxs-lookup"><span data-stu-id="01157-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="01157-110">子元素</span><span class="sxs-lookup"><span data-stu-id="01157-110">Child elements</span></span>

|<span data-ttu-id="01157-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="01157-111">**Element**</span></span>|<span data-ttu-id="01157-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="01157-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="01157-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="01157-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="01157-114">包含一个文件夹的标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="01157-114">Contains the identifier and change key of a folder.</span></span>  <br/> |
|[<span data-ttu-id="01157-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="01157-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="01157-116">标识可通过名称引用的 MicrosoftExchange Server 2007 文件夹。</span><span class="sxs-lookup"><span data-stu-id="01157-116">Identifies MicrosoftExchange Server 2007 folders that can be referenced by name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="01157-117">父元素</span><span class="sxs-lookup"><span data-stu-id="01157-117">Parent elements</span></span>

|<span data-ttu-id="01157-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="01157-118">**Element**</span></span>|<span data-ttu-id="01157-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="01157-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="01157-120">SearchParameters</span><span class="sxs-lookup"><span data-stu-id="01157-120">SearchParameters</span></span>](searchparameters.md) <br/> |<span data-ttu-id="01157-121">表示用于定义搜索文件夹的参数。</span><span class="sxs-lookup"><span data-stu-id="01157-121">Represents the parameters that define a search folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="01157-122">备注</span><span class="sxs-lookup"><span data-stu-id="01157-122">Remarks</span></span>

<span data-ttu-id="01157-123">**BaseFolderIds**元素必须包含至少一个[FolderId](folderid.md)或[DistinguishedFolderId](distinguishedfolderid.md)元素。</span><span class="sxs-lookup"><span data-stu-id="01157-123">The **BaseFolderIds** element must contain at least one [FolderId](folderid.md) or [DistinguishedFolderId](distinguishedfolderid.md) element.</span></span> 
  
<span data-ttu-id="01157-124">描述此元素的架构位于运行 Exchange Server 2007 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="01157-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="01157-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="01157-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="01157-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="01157-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="01157-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="01157-127">Schema name</span></span>  <br/> |<span data-ttu-id="01157-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="01157-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="01157-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="01157-129">Validation file</span></span>  <br/> |<span data-ttu-id="01157-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="01157-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="01157-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="01157-131">Can be empty</span></span>  <br/> |<span data-ttu-id="01157-132">False</span><span class="sxs-lookup"><span data-stu-id="01157-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="01157-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="01157-133">See also</span></span>



- [<span data-ttu-id="01157-134">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="01157-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

