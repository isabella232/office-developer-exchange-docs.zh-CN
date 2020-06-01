---
title: GlobalParentFolderIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8f5fcbcb-05ed-462a-99cf-a6b112a4aef6
description: GlobalParentFolderIds 元素指定全局父文件夹的标识符。
ms.openlocfilehash: 11c520fa0f4a1ed6d6c9d694b407e39cd036b9cd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459095"
---
# <a name="globalparentfolderids"></a><span data-ttu-id="a178e-103">GlobalParentFolderIds</span><span class="sxs-lookup"><span data-stu-id="a178e-103">GlobalParentFolderIds</span></span>

<span data-ttu-id="a178e-104">**GlobalParentFolderIds**元素指定全局父文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="a178e-104">The **GlobalParentFolderIds** element specifies the identifiers of the global parent folders.</span></span> 
  
```XML
<GlobalParentFolderIds>
    <FolderId/>
    <DistinguishedFolderId/>
</GlobalParentFolderIds>
```

 <span data-ttu-id="a178e-105">**NonEmptyArrayOfBaseFolderIdsType**</span><span class="sxs-lookup"><span data-stu-id="a178e-105">**NonEmptyArrayOfBaseFolderIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a178e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a178e-106">Attributes and elements</span></span>

<span data-ttu-id="a178e-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a178e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a178e-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="a178e-108">Attributes</span></span>

<span data-ttu-id="a178e-109">无。</span><span class="sxs-lookup"><span data-stu-id="a178e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a178e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a178e-110">Child elements</span></span>

|<span data-ttu-id="a178e-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="a178e-111">**Element**</span></span>|<span data-ttu-id="a178e-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="a178e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a178e-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="a178e-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="a178e-114">包含一个文件夹的标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="a178e-114">Contains the identifier and change key of a folder.</span></span>  <br/> |
|[<span data-ttu-id="a178e-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="a178e-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="a178e-116">标识可通过名称引用的文件夹。</span><span class="sxs-lookup"><span data-stu-id="a178e-116">Identifies folders that can be referenced by name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a178e-117">父元素</span><span class="sxs-lookup"><span data-stu-id="a178e-117">Parent elements</span></span>

|<span data-ttu-id="a178e-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="a178e-118">**Element**</span></span>|<span data-ttu-id="a178e-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="a178e-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a178e-120">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="a178e-120">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="a178e-121">表示单个对话。</span><span class="sxs-lookup"><span data-stu-id="a178e-121">Represents a single conversation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a178e-122">备注</span><span class="sxs-lookup"><span data-stu-id="a178e-122">Remarks</span></span>

<span data-ttu-id="a178e-123">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="a178e-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a178e-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a178e-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a178e-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="a178e-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a178e-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="a178e-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a178e-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="a178e-127">Schema Name</span></span>  <br/> |<span data-ttu-id="a178e-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="a178e-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="a178e-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="a178e-129">Validation File</span></span>  <br/> |<span data-ttu-id="a178e-130">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="a178e-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="a178e-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="a178e-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="a178e-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a178e-132">See also</span></span>



- [<span data-ttu-id="a178e-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a178e-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

