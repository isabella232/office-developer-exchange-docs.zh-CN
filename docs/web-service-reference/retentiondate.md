---
title: RetentionDate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0c1df5e2-b56a-4947-a047-2b73b32e5fb7
description: RetentionDate 元素指定必须保留项目的最后一个日期。
ms.openlocfilehash: 2e450a72081a31c805c74bffc3a446034d4f24e7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827217"
---
# <a name="retentiondate"></a><span data-ttu-id="d0b8e-103">RetentionDate</span><span class="sxs-lookup"><span data-stu-id="d0b8e-103">RetentionDate</span></span>

<span data-ttu-id="d0b8e-104">**RetentionDate**元素指定必须保留项目的最后一个日期。</span><span class="sxs-lookup"><span data-stu-id="d0b8e-104">The **RetentionDate** element specifies the last date that an item must be retained.</span></span> 
  
```XML
<RetentionDate></RetentionDate>
```

 <span data-ttu-id="d0b8e-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="d0b8e-105">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d0b8e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d0b8e-106">Attributes and elements</span></span>

<span data-ttu-id="d0b8e-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d0b8e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d0b8e-108">属性</span><span class="sxs-lookup"><span data-stu-id="d0b8e-108">Attributes</span></span>

<span data-ttu-id="d0b8e-109">无。</span><span class="sxs-lookup"><span data-stu-id="d0b8e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d0b8e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d0b8e-110">Child elements</span></span>

<span data-ttu-id="d0b8e-111">无。</span><span class="sxs-lookup"><span data-stu-id="d0b8e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d0b8e-112">父元素</span><span class="sxs-lookup"><span data-stu-id="d0b8e-112">Parent elements</span></span>

<span data-ttu-id="d0b8e-113">[SearchPreviewItem](searchpreviewitem.md) | [项](item.md) | [联系人](contact.md) | [消息](message-ex15websvcsotherref.md) | [DistributionList](distributionlist.md) | [日历项目](calendaritem.md) | [PostItem](postitem.md) | [任务](task.md)</span><span class="sxs-lookup"><span data-stu-id="d0b8e-113">[SearchPreviewItem](searchpreviewitem.md) | [Item](item.md) | [Contact](contact.md) | [Message](message-ex15websvcsotherref.md) | [DistributionList](distributionlist.md) | [CalendarItem](calendaritem.md) | [PostItem](postitem.md) | [Task](task.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="d0b8e-114">文本值</span><span class="sxs-lookup"><span data-stu-id="d0b8e-114">Text value</span></span>

<span data-ttu-id="d0b8e-115">**RetentionDate**元素的文本值表示时应不会保留项目的日期。</span><span class="sxs-lookup"><span data-stu-id="d0b8e-115">The text value of the **RetentionDate** element represents the date when an item should no longer be retained.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d0b8e-116">备注</span><span class="sxs-lookup"><span data-stu-id="d0b8e-116">Remarks</span></span>

<span data-ttu-id="d0b8e-117">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="d0b8e-117">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d0b8e-118">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d0b8e-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d0b8e-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="d0b8e-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d0b8e-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="d0b8e-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d0b8e-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="d0b8e-121">Schema name</span></span>  <br/> |<span data-ttu-id="d0b8e-122">类型架构</span><span class="sxs-lookup"><span data-stu-id="d0b8e-122">Types schema</span></span>  <br/> |
|<span data-ttu-id="d0b8e-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="d0b8e-123">Validation file</span></span>  <br/> |<span data-ttu-id="d0b8e-124">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d0b8e-124">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d0b8e-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="d0b8e-125">Can be empty</span></span>  <br/> ||
   
