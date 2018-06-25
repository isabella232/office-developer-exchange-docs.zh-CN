---
title: UnknownEntry
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UnknownEntry
api_type:
- schema
ms.assetid: 3cb4c62e-052a-4326-8639-8c41dfd047b2
description: UnknownEntry 元素均表示无法解析针对 Active Directory 目录服务的单个未知的权限条目。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。
ms.openlocfilehash: 11939ad39c83ac2d15ec7fface6f530d3f60e12a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838346"
---
# <a name="unknownentry"></a><span data-ttu-id="244fe-104">UnknownEntry</span><span class="sxs-lookup"><span data-stu-id="244fe-104">UnknownEntry</span></span>

<span data-ttu-id="244fe-105">**UnknownEntry**元素均表示无法解析针对 Active Directory 目录服务的单个未知的权限条目。</span><span class="sxs-lookup"><span data-stu-id="244fe-105">The **UnknownEntry** element represents a single unknown permission entry that cannot be resolved against the Active Directory directory service.</span></span> <span data-ttu-id="244fe-106">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="244fe-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<UnknownEntry/>
```

 <span data-ttu-id="244fe-107">**string**</span><span class="sxs-lookup"><span data-stu-id="244fe-107">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="244fe-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="244fe-108">Attributes and elements</span></span>

<span data-ttu-id="244fe-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="244fe-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="244fe-110">属性</span><span class="sxs-lookup"><span data-stu-id="244fe-110">Attributes</span></span>

<span data-ttu-id="244fe-111">无。</span><span class="sxs-lookup"><span data-stu-id="244fe-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="244fe-112">子元素</span><span class="sxs-lookup"><span data-stu-id="244fe-112">Child elements</span></span>

<span data-ttu-id="244fe-113">无。</span><span class="sxs-lookup"><span data-stu-id="244fe-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="244fe-114">父元素</span><span class="sxs-lookup"><span data-stu-id="244fe-114">Parent elements</span></span>

|<span data-ttu-id="244fe-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="244fe-115">**Element**</span></span>|<span data-ttu-id="244fe-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="244fe-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="244fe-117">UnknownEntries</span><span class="sxs-lookup"><span data-stu-id="244fe-117">UnknownEntries</span></span>](unknownentries.md) <br/> |<span data-ttu-id="244fe-118">包含数组无法解析的 Active directory 的未知的权限条目。</span><span class="sxs-lookup"><span data-stu-id="244fe-118">Contains an array of unknown permission entries that cannot be resolved against Active Directory.</span></span> <span data-ttu-id="244fe-119">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="244fe-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="244fe-120">文本值</span><span class="sxs-lookup"><span data-stu-id="244fe-120">Text value</span></span>

<span data-ttu-id="244fe-121">文本值表示无法解析的 Active directory 的权限条目。</span><span class="sxs-lookup"><span data-stu-id="244fe-121">The text value represents a permission entry that cannot be resolved against Active Directory.</span></span> <span data-ttu-id="244fe-122">文本值表示的安全标识符 (SID)。</span><span class="sxs-lookup"><span data-stu-id="244fe-122">The text value represents a security identifier (SID).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="244fe-123">备注</span><span class="sxs-lookup"><span data-stu-id="244fe-123">Remarks</span></span>

<span data-ttu-id="244fe-124">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="244fe-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="244fe-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="244fe-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="244fe-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="244fe-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="244fe-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="244fe-127">Schema Name</span></span>  <br/> |<span data-ttu-id="244fe-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="244fe-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="244fe-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="244fe-129">Validation File</span></span>  <br/> |<span data-ttu-id="244fe-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="244fe-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="244fe-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="244fe-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="244fe-132">False</span><span class="sxs-lookup"><span data-stu-id="244fe-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="244fe-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="244fe-133">See also</span></span>



- [<span data-ttu-id="244fe-134">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="244fe-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="244fe-135">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="244fe-135">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

