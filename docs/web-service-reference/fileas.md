---
title: FileAs
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FileAs
api_type:
- schema
ms.assetid: df50524e-471c-49d2-89fe-b2d0f61a1365
description: FileAs 元素表示联系人或通讯组列表在 "联系人" 文件夹中的存档方式。
ms.openlocfilehash: be756d86d7608fcb758dd54f2ada9f03a04343e2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461196"
---
# <a name="fileas"></a><span data-ttu-id="c8c3d-103">FileAs</span><span class="sxs-lookup"><span data-stu-id="c8c3d-103">FileAs</span></span>

<span data-ttu-id="c8c3d-104">**FileAs**元素表示联系人或通讯组列表在 "联系人" 文件夹中的存档方式。</span><span class="sxs-lookup"><span data-stu-id="c8c3d-104">The **FileAs** element represents how a contact or distribution list is filed in the Contacts folder.</span></span> 
  
```xml
<FileAs/>
```

 <span data-ttu-id="c8c3d-105">**string**</span><span class="sxs-lookup"><span data-stu-id="c8c3d-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c8c3d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c8c3d-106">Attributes and elements</span></span>

<span data-ttu-id="c8c3d-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c8c3d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c8c3d-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="c8c3d-108">Attributes</span></span>

<span data-ttu-id="c8c3d-109">无。</span><span class="sxs-lookup"><span data-stu-id="c8c3d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c8c3d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c8c3d-110">Child elements</span></span>

<span data-ttu-id="c8c3d-111">无。</span><span class="sxs-lookup"><span data-stu-id="c8c3d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c8c3d-112">父元素</span><span class="sxs-lookup"><span data-stu-id="c8c3d-112">Parent elements</span></span>

|<span data-ttu-id="c8c3d-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="c8c3d-113">**Element**</span></span>|<span data-ttu-id="c8c3d-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="c8c3d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c8c3d-115">DistributionList</span><span class="sxs-lookup"><span data-stu-id="c8c3d-115">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="c8c3d-116">表示通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="c8c3d-116">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="c8c3d-117">Contact</span><span class="sxs-lookup"><span data-stu-id="c8c3d-117">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="c8c3d-118">表示 Exchange 联系人项目。</span><span class="sxs-lookup"><span data-stu-id="c8c3d-118">Represents an Exchange contact item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c8c3d-119">文本值</span><span class="sxs-lookup"><span data-stu-id="c8c3d-119">Text value</span></span>

<span data-ttu-id="c8c3d-120">如果使用此元素，则需要一个表示字符串的文本值。</span><span class="sxs-lookup"><span data-stu-id="c8c3d-120">A text value that represents a string is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c8c3d-121">备注</span><span class="sxs-lookup"><span data-stu-id="c8c3d-121">Remarks</span></span>

<span data-ttu-id="c8c3d-122">**FileAs**元素用于按姓名（而不是全名或公司名称）对联系人和通讯组列表进行排序。</span><span class="sxs-lookup"><span data-stu-id="c8c3d-122">The **FileAs** element is used to sort contacts and distribution lists by a name other than a full name or company name.</span></span> 
  
<span data-ttu-id="c8c3d-123">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c8c3d-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c8c3d-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="c8c3d-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c8c3d-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="c8c3d-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c8c3d-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="c8c3d-126">Schema name</span></span>  <br/> |<span data-ttu-id="c8c3d-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="c8c3d-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="c8c3d-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="c8c3d-128">Validation file</span></span>  <br/> |<span data-ttu-id="c8c3d-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c8c3d-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c8c3d-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="c8c3d-130">Can be empty</span></span>  <br/> |<span data-ttu-id="c8c3d-131">False</span><span class="sxs-lookup"><span data-stu-id="c8c3d-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c8c3d-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c8c3d-132">See also</span></span>



- [<span data-ttu-id="c8c3d-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c8c3d-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

