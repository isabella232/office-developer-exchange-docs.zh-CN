---
title: NonIndexableItemDetail
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a26d4c02-f1bd-40c4-9257-5db45e839f17
description: NonIndexableItemDetail 元素指定有关无法编制索引的项目的详细信息。
ms.openlocfilehash: 4fc4324501570402d22aa303d6af2a60b50b3cc6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466736"
---
# <a name="nonindexableitemdetail"></a><span data-ttu-id="1b495-103">NonIndexableItemDetail</span><span class="sxs-lookup"><span data-stu-id="1b495-103">NonIndexableItemDetail</span></span>

<span data-ttu-id="1b495-104">**NonIndexableItemDetail**元素指定有关无法编制索引的项目的详细信息。</span><span class="sxs-lookup"><span data-stu-id="1b495-104">The **NonIndexableItemDetail** element specifies detail information about an item that cannot be indexed.</span></span> 
  
```XML
<NonIndexableItemDetail>
   <ItemId/>
   <ErrorCode/>
   <ErrorDescription/>
   <IsPartiallyIndexed/>
   <IsPermanentFailure/>
   <SortValue/>
   <AttemptCount/>
   <LastAttemptTime/>
   <AdditionalInfo/>
</NonIndexableItemDetail>
```

 <span data-ttu-id="1b495-105">**NonIndexableItemDetailType**</span><span class="sxs-lookup"><span data-stu-id="1b495-105">**NonIndexableItemDetailType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1b495-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1b495-106">Attributes and elements</span></span>

<span data-ttu-id="1b495-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1b495-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1b495-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="1b495-108">Attributes</span></span>

<span data-ttu-id="1b495-109">无。</span><span class="sxs-lookup"><span data-stu-id="1b495-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1b495-110">子元素</span><span class="sxs-lookup"><span data-stu-id="1b495-110">Child elements</span></span>

<span data-ttu-id="1b495-111">[ItemId](itemid.md)  | [ErrorCode （ItemIndexErrorType）](errorcode-itemindexerrortype.md)  | [ErrorDescription](errordescription.md)  | [IsPartiallyIndexed](ispartiallyindexed.md)  | [IsPermanentFailure](ispermanentfailure.md)  | [SortValue](sortvalue.md)  | [AttemptCount](attemptcount.md)  | [LastAttemptTime](lastattempttime.md)  | [AdditionalInfo](additionalinfo.md)</span><span class="sxs-lookup"><span data-stu-id="1b495-111">[ItemId](itemid.md) | [ErrorCode (ItemIndexErrorType)](errorcode-itemindexerrortype.md) | [ErrorDescription](errordescription.md) | [IsPartiallyIndexed](ispartiallyindexed.md) | [IsPermanentFailure](ispermanentfailure.md) | [SortValue](sortvalue.md) | [AttemptCount](attemptcount.md) | [LastAttemptTime](lastattempttime.md) | [AdditionalInfo](additionalinfo.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1b495-112">父元素</span><span class="sxs-lookup"><span data-stu-id="1b495-112">Parent elements</span></span>

[<span data-ttu-id="1b495-113">项目（ArrayOfNonIndexableItemDetailsType）</span><span class="sxs-lookup"><span data-stu-id="1b495-113">Items (ArrayOfNonIndexableItemDetailsType)</span></span>](items-arrayofnonindexableitemdetailstype.md)
  
## <a name="remarks"></a><span data-ttu-id="1b495-114">备注</span><span class="sxs-lookup"><span data-stu-id="1b495-114">Remarks</span></span>

<span data-ttu-id="1b495-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="1b495-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="1b495-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1b495-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1b495-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="1b495-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1b495-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="1b495-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1b495-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="1b495-119">Schema name</span></span>  <br/> |<span data-ttu-id="1b495-120">类型架构</span><span class="sxs-lookup"><span data-stu-id="1b495-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="1b495-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="1b495-121">Validation file</span></span>  <br/> |<span data-ttu-id="1b495-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1b495-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1b495-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="1b495-123">Can be empty</span></span>  <br/> ||
   

