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
description: UnknownEntry 元素表示单个无法针对 Active Directory 目录服务进行解析的未知权限条目。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: 452857690f719ba3ee9dffa29e576ca4f3b2b945
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459396"
---
# <a name="unknownentry"></a><span data-ttu-id="89c12-104">UnknownEntry</span><span class="sxs-lookup"><span data-stu-id="89c12-104">UnknownEntry</span></span>

<span data-ttu-id="89c12-105">**UnknownEntry**元素表示单个无法针对 Active Directory 目录服务进行解析的未知权限条目。</span><span class="sxs-lookup"><span data-stu-id="89c12-105">The **UnknownEntry** element represents a single unknown permission entry that cannot be resolved against the Active Directory directory service.</span></span> <span data-ttu-id="89c12-106">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="89c12-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<UnknownEntry/>
```

 <span data-ttu-id="89c12-107">**string**</span><span class="sxs-lookup"><span data-stu-id="89c12-107">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="89c12-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="89c12-108">Attributes and elements</span></span>

<span data-ttu-id="89c12-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="89c12-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="89c12-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="89c12-110">Attributes</span></span>

<span data-ttu-id="89c12-111">无。</span><span class="sxs-lookup"><span data-stu-id="89c12-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="89c12-112">子元素</span><span class="sxs-lookup"><span data-stu-id="89c12-112">Child elements</span></span>

<span data-ttu-id="89c12-113">无。</span><span class="sxs-lookup"><span data-stu-id="89c12-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="89c12-114">父元素</span><span class="sxs-lookup"><span data-stu-id="89c12-114">Parent elements</span></span>

|<span data-ttu-id="89c12-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="89c12-115">**Element**</span></span>|<span data-ttu-id="89c12-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="89c12-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="89c12-117">UnknownEntries</span><span class="sxs-lookup"><span data-stu-id="89c12-117">UnknownEntries</span></span>](unknownentries.md) <br/> |<span data-ttu-id="89c12-118">包含无法对 Active Directory 进行解析的未知权限项数组。</span><span class="sxs-lookup"><span data-stu-id="89c12-118">Contains an array of unknown permission entries that cannot be resolved against Active Directory.</span></span> <span data-ttu-id="89c12-119">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="89c12-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="89c12-120">文本值</span><span class="sxs-lookup"><span data-stu-id="89c12-120">Text value</span></span>

<span data-ttu-id="89c12-121">该文本值表示无法对 Active Directory 进行解析的权限条目。</span><span class="sxs-lookup"><span data-stu-id="89c12-121">The text value represents a permission entry that cannot be resolved against Active Directory.</span></span> <span data-ttu-id="89c12-122">文本值表示安全标识符（SID）。</span><span class="sxs-lookup"><span data-stu-id="89c12-122">The text value represents a security identifier (SID).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="89c12-123">说明</span><span class="sxs-lookup"><span data-stu-id="89c12-123">Remarks</span></span>

<span data-ttu-id="89c12-124">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="89c12-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="89c12-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="89c12-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="89c12-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="89c12-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="89c12-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="89c12-127">Schema Name</span></span>  <br/> |<span data-ttu-id="89c12-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="89c12-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="89c12-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="89c12-129">Validation File</span></span>  <br/> |<span data-ttu-id="89c12-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="89c12-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="89c12-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="89c12-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="89c12-132">False</span><span class="sxs-lookup"><span data-stu-id="89c12-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="89c12-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="89c12-133">See also</span></span>



- [<span data-ttu-id="89c12-134">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="89c12-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="89c12-135">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="89c12-135">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

