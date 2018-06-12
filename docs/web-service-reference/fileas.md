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
description: FileAs 元素均表示一个联系人或通讯组列表联系人文件夹中的字段如何。
ms.openlocfilehash: dab9142eebf7691862e7970a7d1e8f5874393b94
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754307"
---
# <a name="fileas"></a><span data-ttu-id="a471a-103">FileAs</span><span class="sxs-lookup"><span data-stu-id="a471a-103">FileAs</span></span>

<span data-ttu-id="a471a-104">**FileAs**元素均表示一个联系人或通讯组列表联系人文件夹中的字段如何。</span><span class="sxs-lookup"><span data-stu-id="a471a-104">The **FileAs** element represents how a contact or distribution list is filed in the Contacts folder.</span></span> 
  
```xml
<FileAs/>
```

 <span data-ttu-id="a471a-105">**string**</span><span class="sxs-lookup"><span data-stu-id="a471a-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a471a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a471a-106">Attributes and elements</span></span>

<span data-ttu-id="a471a-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a471a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a471a-108">属性</span><span class="sxs-lookup"><span data-stu-id="a471a-108">Attributes</span></span>

<span data-ttu-id="a471a-109">无。</span><span class="sxs-lookup"><span data-stu-id="a471a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a471a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a471a-110">Child elements</span></span>

<span data-ttu-id="a471a-111">无。</span><span class="sxs-lookup"><span data-stu-id="a471a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a471a-112">父元素</span><span class="sxs-lookup"><span data-stu-id="a471a-112">Parent elements</span></span>

|<span data-ttu-id="a471a-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="a471a-113">**Element**</span></span>|<span data-ttu-id="a471a-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="a471a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a471a-115">DistributionList</span><span class="sxs-lookup"><span data-stu-id="a471a-115">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="a471a-116">表示通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="a471a-116">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="a471a-117">联系人</span><span class="sxs-lookup"><span data-stu-id="a471a-117">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="a471a-118">表示 Exchange 联系人项目。</span><span class="sxs-lookup"><span data-stu-id="a471a-118">Represents an Exchange contact item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a471a-119">文本值</span><span class="sxs-lookup"><span data-stu-id="a471a-119">Text value</span></span>

<span data-ttu-id="a471a-120">如果使用此元素，则需要用于表示字符串的文本值。</span><span class="sxs-lookup"><span data-stu-id="a471a-120">A text value that represents a string is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a471a-121">备注</span><span class="sxs-lookup"><span data-stu-id="a471a-121">Remarks</span></span>

<span data-ttu-id="a471a-122">**FileAs**元素用于不同的完整名称或公司名称的名称对联系人和通讯组列表进行排序。</span><span class="sxs-lookup"><span data-stu-id="a471a-122">The **FileAs** element is used to sort contacts and distribution lists by a name other than a full name or company name.</span></span> 
  
<span data-ttu-id="a471a-123">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a471a-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a471a-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="a471a-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a471a-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="a471a-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a471a-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="a471a-126">Schema name</span></span>  <br/> |<span data-ttu-id="a471a-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="a471a-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="a471a-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="a471a-128">Validation file</span></span>  <br/> |<span data-ttu-id="a471a-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a471a-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a471a-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="a471a-130">Can be empty</span></span>  <br/> |<span data-ttu-id="a471a-131">False</span><span class="sxs-lookup"><span data-stu-id="a471a-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a471a-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a471a-132">See also</span></span>



- [<span data-ttu-id="a471a-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a471a-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

