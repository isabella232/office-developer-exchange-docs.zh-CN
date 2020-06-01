---
title: TotalCount
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TotalCount
api_type:
- schema
ms.assetid: c48c6388-8449-4622-bc38-6f0e84293872
description: TotalCount 元素表示给定文件夹中项的总计数。
ms.openlocfilehash: 3d068b558cddf73265b6bbff9fb0760738e54cec
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467520"
---
# <a name="totalcount"></a><span data-ttu-id="606a6-103">TotalCount</span><span class="sxs-lookup"><span data-stu-id="606a6-103">TotalCount</span></span>

<span data-ttu-id="606a6-104">**TotalCount**元素表示给定文件夹中项的总计数。</span><span class="sxs-lookup"><span data-stu-id="606a6-104">The **TotalCount** element represents the total count of items within a given folder.</span></span> 
  
```xml
<TotalCount/>
```

 <span data-ttu-id="606a6-105">**int**</span><span class="sxs-lookup"><span data-stu-id="606a6-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="606a6-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="606a6-106">Attributes and elements</span></span>

<span data-ttu-id="606a6-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="606a6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="606a6-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="606a6-108">Attributes</span></span>

<span data-ttu-id="606a6-109">无。</span><span class="sxs-lookup"><span data-stu-id="606a6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="606a6-110">子元素</span><span class="sxs-lookup"><span data-stu-id="606a6-110">Child elements</span></span>

<span data-ttu-id="606a6-111">无。</span><span class="sxs-lookup"><span data-stu-id="606a6-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="606a6-112">父元素</span><span class="sxs-lookup"><span data-stu-id="606a6-112">Parent elements</span></span>

|<span data-ttu-id="606a6-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="606a6-113">**Element**</span></span>|<span data-ttu-id="606a6-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="606a6-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="606a6-115">Folder</span><span class="sxs-lookup"><span data-stu-id="606a6-115">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="606a6-116">表示邮箱中的文件夹。</span><span class="sxs-lookup"><span data-stu-id="606a6-116">Represents a folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="606a6-117">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="606a6-117">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="606a6-118">代表邮箱中的 "日历" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="606a6-118">Represents a calendar folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="606a6-119">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="606a6-119">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="606a6-120">表示邮箱中的 "联系人" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="606a6-120">Represents a contacts folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="606a6-121">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="606a6-121">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="606a6-122">表示邮箱中的搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="606a6-122">Represents a search folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="606a6-123">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="606a6-123">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="606a6-124">表示邮箱中的任务文件夹。</span><span class="sxs-lookup"><span data-stu-id="606a6-124">Represents a task folder in a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="606a6-125">文本值</span><span class="sxs-lookup"><span data-stu-id="606a6-125">Text value</span></span>

<span data-ttu-id="606a6-126">该文本值表示一个整数值。</span><span class="sxs-lookup"><span data-stu-id="606a6-126">The text value represents an integer value.</span></span> <span data-ttu-id="606a6-127">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="606a6-127">This property is read-only.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="606a6-128">说明</span><span class="sxs-lookup"><span data-stu-id="606a6-128">Remarks</span></span>

<span data-ttu-id="606a6-129">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="606a6-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="606a6-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="606a6-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="606a6-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="606a6-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="606a6-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="606a6-132">Schema Name</span></span>  <br/> |<span data-ttu-id="606a6-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="606a6-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="606a6-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="606a6-134">Validation File</span></span>  <br/> |<span data-ttu-id="606a6-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="606a6-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="606a6-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="606a6-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="606a6-137">False</span><span class="sxs-lookup"><span data-stu-id="606a6-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="606a6-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="606a6-138">See also</span></span>



- [<span data-ttu-id="606a6-139">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="606a6-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

