---
title: PolicyTag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fa4b1447-dc7b-47ad-a677-78fcee443dc6
description: PolicyTag 元素指定项目或文件夹的保留标识符。
ms.openlocfilehash: d6cd5aab1145f6006912541c8f8c1d0a91d1e17e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826835"
---
# <a name="policytag"></a><span data-ttu-id="85735-103">PolicyTag</span><span class="sxs-lookup"><span data-stu-id="85735-103">PolicyTag</span></span>

<span data-ttu-id="85735-104">**PolicyTag**元素指定项目或文件夹的保留标识符。</span><span class="sxs-lookup"><span data-stu-id="85735-104">The **PolicyTag** element specifies the retention identifier on an item or folder.</span></span> 
  
```xml
<PolicyTag IsExplicit="true | false"></PolicyTag>
```

 <span data-ttu-id="85735-105">**RetentionTagType**</span><span class="sxs-lookup"><span data-stu-id="85735-105">**RetentionTagType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="85735-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="85735-106">Attributes and elements</span></span>

<span data-ttu-id="85735-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="85735-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="85735-108">属性</span><span class="sxs-lookup"><span data-stu-id="85735-108">Attributes</span></span>

|<span data-ttu-id="85735-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="85735-109">**Attribute**</span></span>|<span data-ttu-id="85735-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="85735-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="85735-111">IsExplicit</span><span class="sxs-lookup"><span data-stu-id="85735-111">IsExplicit</span></span>  <br/> |<span data-ttu-id="85735-112">指示是否策略标记显式设置项目或文件夹。</span><span class="sxs-lookup"><span data-stu-id="85735-112">Indicates whether a policy tag was explicitly set on an item or folder.</span></span>  <br/> <span data-ttu-id="85735-113">文本值为**true**的**IsExplicit**属性指示上的项目或文件夹的显式设置策略标记。</span><span class="sxs-lookup"><span data-stu-id="85735-113">A text value of **true** for the **IsExplicit** attribute indicates that the policy tag was explicitly set on the item or folder.</span></span> <span data-ttu-id="85735-114">文本值为**false**指示的隐式的项目或基于父文件夹策略标记文件夹上设置了策略标记。</span><span class="sxs-lookup"><span data-stu-id="85735-114">A text value of **false** indicates that the policy tag was implicitly set on the item or folder based on the parent folder policy tag.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="85735-115">子元素</span><span class="sxs-lookup"><span data-stu-id="85735-115">Child elements</span></span>

<span data-ttu-id="85735-116">无。</span><span class="sxs-lookup"><span data-stu-id="85735-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="85735-117">父元素</span><span class="sxs-lookup"><span data-stu-id="85735-117">Parent elements</span></span>

<span data-ttu-id="85735-118">[SearchPreviewItem](searchpreviewitem.md) | [项](item.md) | [联系人](contact.md) | [消息](message-ex15websvcsotherref.md) | [DistributionList](distributionlist.md) | [日历项目](calendaritem.md) | [PostItem](postitem.md) | [任务](task.md)</span><span class="sxs-lookup"><span data-stu-id="85735-118">[SearchPreviewItem](searchpreviewitem.md) | [Item](item.md) | [Contact](contact.md) | [Message](message-ex15websvcsotherref.md) | [DistributionList](distributionlist.md) | [CalendarItem](calendaritem.md) | [PostItem](postitem.md) | [Task](task.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="85735-119">文本值</span><span class="sxs-lookup"><span data-stu-id="85735-119">Text value</span></span>

<span data-ttu-id="85735-120">**PolicyTag**元素的文本值是策略标记标识符。</span><span class="sxs-lookup"><span data-stu-id="85735-120">The text value of the **PolicyTag** element is the policy tag identifier.</span></span> <span data-ttu-id="85735-121">策略标记标识符是一个 GUID。</span><span class="sxs-lookup"><span data-stu-id="85735-121">The policy tag identifier is a GUID.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="85735-122">备注</span><span class="sxs-lookup"><span data-stu-id="85735-122">Remarks</span></span>

<span data-ttu-id="85735-123">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="85735-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="85735-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="85735-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="85735-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="85735-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="85735-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="85735-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="85735-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="85735-127">Schema name</span></span>  <br/> |<span data-ttu-id="85735-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="85735-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="85735-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="85735-129">Validation file</span></span>  <br/> |<span data-ttu-id="85735-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="85735-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="85735-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="85735-131">Can be empty</span></span>  <br/> ||
   

