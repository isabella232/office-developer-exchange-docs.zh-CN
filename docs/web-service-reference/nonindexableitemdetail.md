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
ms.openlocfilehash: ef1bd072a44b42b501a3016c394b89fe6ab25bf0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826543"
---
# <a name="nonindexableitemdetail"></a><span data-ttu-id="7f75a-103">NonIndexableItemDetail</span><span class="sxs-lookup"><span data-stu-id="7f75a-103">NonIndexableItemDetail</span></span>

<span data-ttu-id="7f75a-104">**NonIndexableItemDetail**元素指定有关无法编制索引的项目的详细信息。</span><span class="sxs-lookup"><span data-stu-id="7f75a-104">The **NonIndexableItemDetail** element specifies detail information about an item that cannot be indexed.</span></span> 
  
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

 <span data-ttu-id="7f75a-105">**NonIndexableItemDetailType**</span><span class="sxs-lookup"><span data-stu-id="7f75a-105">**NonIndexableItemDetailType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7f75a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7f75a-106">Attributes and elements</span></span>

<span data-ttu-id="7f75a-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7f75a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7f75a-108">属性</span><span class="sxs-lookup"><span data-stu-id="7f75a-108">Attributes</span></span>

<span data-ttu-id="7f75a-109">无。</span><span class="sxs-lookup"><span data-stu-id="7f75a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7f75a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="7f75a-110">Child elements</span></span>

<span data-ttu-id="7f75a-111">[ItemId](itemid.md) | [ErrorCode (ItemIndexErrorType)](errorcode-itemindexerrortype.md) | [ErrorDescription](errordescription.md) | [IsPartiallyIndexed](ispartiallyindexed.md) | [IsPermanentFailure](ispermanentfailure.md) | [SortValue](sortvalue.md) | [AttemptCount](attemptcount.md)  |  [LastAttemptTime](lastattempttime.md) | [AdditionalInfo](additionalinfo.md)</span><span class="sxs-lookup"><span data-stu-id="7f75a-111">[ItemId](itemid.md) | [ErrorCode (ItemIndexErrorType)](errorcode-itemindexerrortype.md) | [ErrorDescription](errordescription.md) | [IsPartiallyIndexed](ispartiallyindexed.md) | [IsPermanentFailure](ispermanentfailure.md) | [SortValue](sortvalue.md) | [AttemptCount](attemptcount.md) | [LastAttemptTime](lastattempttime.md) | [AdditionalInfo](additionalinfo.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7f75a-112">父元素</span><span class="sxs-lookup"><span data-stu-id="7f75a-112">Parent elements</span></span>

[<span data-ttu-id="7f75a-113">项目 (ArrayOfNonIndexableItemDetailsType)</span><span class="sxs-lookup"><span data-stu-id="7f75a-113">Items (ArrayOfNonIndexableItemDetailsType)</span></span>](items-arrayofnonindexableitemdetailstype.md)
  
## <a name="remarks"></a><span data-ttu-id="7f75a-114">备注</span><span class="sxs-lookup"><span data-stu-id="7f75a-114">Remarks</span></span>

<span data-ttu-id="7f75a-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="7f75a-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="7f75a-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7f75a-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7f75a-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="7f75a-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7f75a-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="7f75a-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7f75a-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="7f75a-119">Schema name</span></span>  <br/> |<span data-ttu-id="7f75a-120">类型架构</span><span class="sxs-lookup"><span data-stu-id="7f75a-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="7f75a-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="7f75a-121">Validation file</span></span>  <br/> |<span data-ttu-id="7f75a-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7f75a-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7f75a-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="7f75a-123">Can be empty</span></span>  <br/> ||
   

