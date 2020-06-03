---
title: PolicyTag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fa4b1447-dc7b-47ad-a677-78fcee443dc6
description: PolicyTag 元素指定项目或文件夹中的保留标识符。
ms.openlocfilehash: ddc4d890d1e514586ba5ea7f6a8b541b2e4786c7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460895"
---
# <a name="policytag"></a><span data-ttu-id="c1920-103">PolicyTag</span><span class="sxs-lookup"><span data-stu-id="c1920-103">PolicyTag</span></span>

<span data-ttu-id="c1920-104">**PolicyTag**元素指定项目或文件夹中的保留标识符。</span><span class="sxs-lookup"><span data-stu-id="c1920-104">The **PolicyTag** element specifies the retention identifier on an item or folder.</span></span> 
  
```xml
<PolicyTag IsExplicit="true | false"></PolicyTag>
```

 <span data-ttu-id="c1920-105">**RetentionTagType**</span><span class="sxs-lookup"><span data-stu-id="c1920-105">**RetentionTagType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c1920-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c1920-106">Attributes and elements</span></span>

<span data-ttu-id="c1920-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c1920-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c1920-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="c1920-108">Attributes</span></span>

|<span data-ttu-id="c1920-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="c1920-109">**Attribute**</span></span>|<span data-ttu-id="c1920-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="c1920-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c1920-111">IsExplicit</span><span class="sxs-lookup"><span data-stu-id="c1920-111">IsExplicit</span></span>  <br/> |<span data-ttu-id="c1920-112">指示是否对项目或文件夹显式设置了策略标记。</span><span class="sxs-lookup"><span data-stu-id="c1920-112">Indicates whether a policy tag was explicitly set on an item or folder.</span></span>  <br/> <span data-ttu-id="c1920-113">**IsExplicit**属性的文本值为**true**表示已在项或文件夹上显式设置了策略标记。</span><span class="sxs-lookup"><span data-stu-id="c1920-113">A text value of **true** for the **IsExplicit** attribute indicates that the policy tag was explicitly set on the item or folder.</span></span> <span data-ttu-id="c1920-114">如果文本值为**false** ，则表示已基于父文件夹策略标记对项目或文件夹隐式设置了策略标记。</span><span class="sxs-lookup"><span data-stu-id="c1920-114">A text value of **false** indicates that the policy tag was implicitly set on the item or folder based on the parent folder policy tag.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c1920-115">子元素</span><span class="sxs-lookup"><span data-stu-id="c1920-115">Child elements</span></span>

<span data-ttu-id="c1920-116">无。</span><span class="sxs-lookup"><span data-stu-id="c1920-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c1920-117">父元素</span><span class="sxs-lookup"><span data-stu-id="c1920-117">Parent elements</span></span>

<span data-ttu-id="c1920-118">[SearchPreviewItem](searchpreviewitem.md)  | [项](item.md)  | [联系人](contact.md)  | [邮件](message-ex15websvcsotherref.md)  | [DistributionList](distributionlist.md)  | [CalendarItem](calendaritem.md)  | [PostItem](postitem.md)  | [任务](task.md)</span><span class="sxs-lookup"><span data-stu-id="c1920-118">[SearchPreviewItem](searchpreviewitem.md) | [Item](item.md) | [Contact](contact.md) | [Message](message-ex15websvcsotherref.md) | [DistributionList](distributionlist.md) | [CalendarItem](calendaritem.md) | [PostItem](postitem.md) | [Task](task.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="c1920-119">文本值</span><span class="sxs-lookup"><span data-stu-id="c1920-119">Text value</span></span>

<span data-ttu-id="c1920-120">**PolicyTag**元素的文本值是策略标记标识符。</span><span class="sxs-lookup"><span data-stu-id="c1920-120">The text value of the **PolicyTag** element is the policy tag identifier.</span></span> <span data-ttu-id="c1920-121">策略标记标识符是一个 GUID。</span><span class="sxs-lookup"><span data-stu-id="c1920-121">The policy tag identifier is a GUID.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c1920-122">备注</span><span class="sxs-lookup"><span data-stu-id="c1920-122">Remarks</span></span>

<span data-ttu-id="c1920-123">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="c1920-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c1920-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c1920-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c1920-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="c1920-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c1920-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="c1920-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c1920-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="c1920-127">Schema name</span></span>  <br/> |<span data-ttu-id="c1920-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="c1920-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="c1920-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="c1920-129">Validation file</span></span>  <br/> |<span data-ttu-id="c1920-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c1920-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c1920-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="c1920-131">Can be empty</span></span>  <br/> ||
   

