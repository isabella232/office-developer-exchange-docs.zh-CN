---
title: DraftItemIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c228f7e7-6dc8-476d-9b8c-99cd5b6f9f0c
description: DraftItemIds 元素包含项目标识符的数组，这些标识符指向对话中的草稿项目。
ms.openlocfilehash: 5e635e354c9d2d768bab5efaafafde272fe568d3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463571"
---
# <a name="draftitemids"></a><span data-ttu-id="c5bd7-103">DraftItemIds</span><span class="sxs-lookup"><span data-stu-id="c5bd7-103">DraftItemIds</span></span>

<span data-ttu-id="c5bd7-104">**DraftItemIds**元素包含项目标识符的数组，这些标识符指向对话中的草稿项目。</span><span class="sxs-lookup"><span data-stu-id="c5bd7-104">The **DraftItemIds** element contains an array of item identifiers to draft items in a conversation.</span></span> 
  
```XML
<DraftItemIds>
   <ItemId/>
   <OccirrenceItemId/>
   <RecurringMasterItemId/>
   <RecurringMasterItemIdRanges/>
</DraftItemIds>
```

 <span data-ttu-id="c5bd7-105">**NonEmptyArrayOfBaseItemIdsType**</span><span class="sxs-lookup"><span data-stu-id="c5bd7-105">**NonEmptyArrayOfBaseItemIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c5bd7-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c5bd7-106">Attributes and elements</span></span>

<span data-ttu-id="c5bd7-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c5bd7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c5bd7-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="c5bd7-108">Attributes</span></span>

<span data-ttu-id="c5bd7-109">无。</span><span class="sxs-lookup"><span data-stu-id="c5bd7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c5bd7-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c5bd7-110">Child elements</span></span>

<span data-ttu-id="c5bd7-111">[ItemId](itemid.md)  | [OccurrenceItemId](occurrenceitemid.md)  | [RecurringMasterItemId](recurringmasteritemid.md)  | [RecurringMasterItemIdRanges](recurringmasteritemidranges.md)</span><span class="sxs-lookup"><span data-stu-id="c5bd7-111">[ItemId](itemid.md) | [OccurrenceItemId](occurrenceitemid.md) | [RecurringMasterItemId](recurringmasteritemid.md) | [RecurringMasterItemIdRanges](recurringmasteritemidranges.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c5bd7-112">父元素</span><span class="sxs-lookup"><span data-stu-id="c5bd7-112">Parent elements</span></span>

[<span data-ttu-id="c5bd7-113">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="c5bd7-113">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
## <a name="remarks"></a><span data-ttu-id="c5bd7-114">备注</span><span class="sxs-lookup"><span data-stu-id="c5bd7-114">Remarks</span></span>

<span data-ttu-id="c5bd7-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="c5bd7-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c5bd7-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c5bd7-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c5bd7-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="c5bd7-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c5bd7-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="c5bd7-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c5bd7-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="c5bd7-119">Schema name</span></span>  <br/> |<span data-ttu-id="c5bd7-120">类型架构</span><span class="sxs-lookup"><span data-stu-id="c5bd7-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="c5bd7-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="c5bd7-121">Validation file</span></span>  <br/> |<span data-ttu-id="c5bd7-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c5bd7-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c5bd7-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="c5bd7-123">Can be empty</span></span>  <br/> ||
   

