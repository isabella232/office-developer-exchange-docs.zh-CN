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
ms.openlocfilehash: b0ff9ab00f3e46351b5a2db9bc4b6282fa4385cd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825747"
---
# <a name="globalparentfolderids"></a><span data-ttu-id="88a49-103">GlobalParentFolderIds</span><span class="sxs-lookup"><span data-stu-id="88a49-103">GlobalParentFolderIds</span></span>

<span data-ttu-id="88a49-104">**GlobalParentFolderIds**元素指定全局父文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="88a49-104">The **GlobalParentFolderIds** element specifies the identifiers of the global parent folders.</span></span> 
  
```XML
<GlobalParentFolderIds>
    <FolderId/>
    <DistinguishedFolderId/>
</GlobalParentFolderIds>
```

 <span data-ttu-id="88a49-105">**NonEmptyArrayOfBaseFolderIdsType**</span><span class="sxs-lookup"><span data-stu-id="88a49-105">**NonEmptyArrayOfBaseFolderIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="88a49-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="88a49-106">Attributes and elements</span></span>

<span data-ttu-id="88a49-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="88a49-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="88a49-108">属性</span><span class="sxs-lookup"><span data-stu-id="88a49-108">Attributes</span></span>

<span data-ttu-id="88a49-109">无。</span><span class="sxs-lookup"><span data-stu-id="88a49-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="88a49-110">子元素</span><span class="sxs-lookup"><span data-stu-id="88a49-110">Child elements</span></span>

|<span data-ttu-id="88a49-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="88a49-111">**Element**</span></span>|<span data-ttu-id="88a49-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="88a49-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="88a49-113">文件夹 Id</span><span class="sxs-lookup"><span data-stu-id="88a49-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="88a49-114">包含一个文件夹的标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="88a49-114">Contains the identifier and change key of a folder.</span></span>  <br/> |
|[<span data-ttu-id="88a49-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="88a49-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="88a49-116">标识可以通过名称引用的文件夹。</span><span class="sxs-lookup"><span data-stu-id="88a49-116">Identifies folders that can be referenced by name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="88a49-117">父元素</span><span class="sxs-lookup"><span data-stu-id="88a49-117">Parent elements</span></span>

|<span data-ttu-id="88a49-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="88a49-118">**Element**</span></span>|<span data-ttu-id="88a49-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="88a49-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="88a49-120">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="88a49-120">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="88a49-121">表示单个对话。</span><span class="sxs-lookup"><span data-stu-id="88a49-121">Represents a single conversation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="88a49-122">备注</span><span class="sxs-lookup"><span data-stu-id="88a49-122">Remarks</span></span>

<span data-ttu-id="88a49-123">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="88a49-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="88a49-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="88a49-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="88a49-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="88a49-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="88a49-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="88a49-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="88a49-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="88a49-127">Schema Name</span></span>  <br/> |<span data-ttu-id="88a49-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="88a49-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="88a49-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="88a49-129">Validation File</span></span>  <br/> |<span data-ttu-id="88a49-130">types.xsd</span><span class="sxs-lookup"><span data-stu-id="88a49-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="88a49-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="88a49-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="88a49-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="88a49-132">See also</span></span>



- [<span data-ttu-id="88a49-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="88a49-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

