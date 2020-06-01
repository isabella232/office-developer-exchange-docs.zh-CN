---
title: SearchDumpster
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ddb62dce-c87a-4714-8023-a6b697a29699
description: SearchDumpster 元素指定是否在 Exchange 转储程序中进行搜索。
ms.openlocfilehash: 067bf8ea3e589aa392c6b8ba6d4dc10b430c1f28
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460489"
---
# <a name="searchdumpster"></a><span data-ttu-id="7a329-103">SearchDumpster</span><span class="sxs-lookup"><span data-stu-id="7a329-103">SearchDumpster</span></span>

<span data-ttu-id="7a329-104">**SearchDumpster**元素指定是否在 Exchange 转储程序中进行搜索。</span><span class="sxs-lookup"><span data-stu-id="7a329-104">The **SearchDumpster** element specifies whether to search in the Exchange Dumpster.</span></span> 
  
```XML
<SearchDumpster> true | false </SearchDumpster>
```

 ****
## <a name="attributes-and-elements"></a><span data-ttu-id="7a329-105">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7a329-105">Attributes and elements</span></span>

<span data-ttu-id="7a329-106">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7a329-106">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7a329-107">Attributes</span><span class="sxs-lookup"><span data-stu-id="7a329-107">Attributes</span></span>

<span data-ttu-id="7a329-108">无。</span><span class="sxs-lookup"><span data-stu-id="7a329-108">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7a329-109">子元素</span><span class="sxs-lookup"><span data-stu-id="7a329-109">Child elements</span></span>

<span data-ttu-id="7a329-110">无。</span><span class="sxs-lookup"><span data-stu-id="7a329-110">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7a329-111">父元素</span><span class="sxs-lookup"><span data-stu-id="7a329-111">Parent elements</span></span>

[<span data-ttu-id="7a329-112">FindMailboxStatisticsByKeywords</span><span class="sxs-lookup"><span data-stu-id="7a329-112">FindMailboxStatisticsByKeywords</span></span>](findmailboxstatisticsbykeywords.md)
  
## <a name="text-value"></a><span data-ttu-id="7a329-113">文本值</span><span class="sxs-lookup"><span data-stu-id="7a329-113">Text value</span></span>

<span data-ttu-id="7a329-114">如果**SearchDumpster**元素的文本值为**true** ，则表示邮箱统计信息搜索包括 Exchange 转储程序。</span><span class="sxs-lookup"><span data-stu-id="7a329-114">A text value of **true** for the **SearchDumpster** element indicates that the mailbox statistics search includes the Exchange Dumpster.</span></span> <span data-ttu-id="7a329-115">**如果值为 false** ，则表示不搜索 Exchange 转储程序。</span><span class="sxs-lookup"><span data-stu-id="7a329-115">A value of **false** indicates that the Exchange Dumpster is not searched.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7a329-116">备注</span><span class="sxs-lookup"><span data-stu-id="7a329-116">Remarks</span></span>

<span data-ttu-id="7a329-117">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="7a329-117">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="7a329-118">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7a329-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7a329-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="7a329-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7a329-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="7a329-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7a329-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="7a329-121">Schema name</span></span>  <br/> |<span data-ttu-id="7a329-122">类型架构</span><span class="sxs-lookup"><span data-stu-id="7a329-122">Types schema</span></span>  <br/> |
|<span data-ttu-id="7a329-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="7a329-123">Validation file</span></span>  <br/> |<span data-ttu-id="7a329-124">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7a329-124">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7a329-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="7a329-125">Can be empty</span></span>  <br/> ||
   

