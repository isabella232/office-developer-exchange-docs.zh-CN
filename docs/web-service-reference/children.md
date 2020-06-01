---
title: 子代
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Children
api_type:
- schema
ms.assetid: ceaffddd-f9bc-43ea-b348-a20fdade738f
description: "\"子女\" 元素包含联系人子女的姓名。"
ms.openlocfilehash: de398c93590a4a9ae93b6aa46994c9295d051b84
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460223"
---
# <a name="children"></a><span data-ttu-id="3b0ee-103">子代</span><span class="sxs-lookup"><span data-stu-id="3b0ee-103">Children</span></span>

<span data-ttu-id="3b0ee-104">"**子女**" 元素包含联系人子女的姓名。</span><span class="sxs-lookup"><span data-stu-id="3b0ee-104">The **Children** element contains the names of a contact's children.</span></span> 
  
```xml
<Children>
   <String/>
</Children>
```

 <span data-ttu-id="3b0ee-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="3b0ee-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3b0ee-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="3b0ee-106">Attributes and elements</span></span>

<span data-ttu-id="3b0ee-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3b0ee-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3b0ee-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="3b0ee-108">Attributes</span></span>

<span data-ttu-id="3b0ee-109">无。</span><span class="sxs-lookup"><span data-stu-id="3b0ee-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3b0ee-110">子元素</span><span class="sxs-lookup"><span data-stu-id="3b0ee-110">Child elements</span></span>

|<span data-ttu-id="3b0ee-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="3b0ee-111">**Element**</span></span>|<span data-ttu-id="3b0ee-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="3b0ee-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3b0ee-113">字符串</span><span class="sxs-lookup"><span data-stu-id="3b0ee-113">String</span></span>](string.md) <br/> |<span data-ttu-id="3b0ee-114">包含联系人子女的姓名。</span><span class="sxs-lookup"><span data-stu-id="3b0ee-114">Contains the name of a contact's child.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3b0ee-115">父元素</span><span class="sxs-lookup"><span data-stu-id="3b0ee-115">Parent elements</span></span>

|<span data-ttu-id="3b0ee-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="3b0ee-116">**Element**</span></span>|<span data-ttu-id="3b0ee-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="3b0ee-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3b0ee-118">Contact</span><span class="sxs-lookup"><span data-stu-id="3b0ee-118">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="3b0ee-119">表示 Exchange 存储中的联系人。</span><span class="sxs-lookup"><span data-stu-id="3b0ee-119">Represents a contact in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3b0ee-120">说明</span><span class="sxs-lookup"><span data-stu-id="3b0ee-120">Remarks</span></span>

<span data-ttu-id="3b0ee-121">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="3b0ee-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3b0ee-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="3b0ee-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3b0ee-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="3b0ee-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3b0ee-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="3b0ee-124">Schema name</span></span>  <br/> |<span data-ttu-id="3b0ee-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="3b0ee-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="3b0ee-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="3b0ee-126">Validation file</span></span>  <br/> |<span data-ttu-id="3b0ee-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3b0ee-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3b0ee-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="3b0ee-128">Can be empty</span></span>  <br/> |<span data-ttu-id="3b0ee-129">False</span><span class="sxs-lookup"><span data-stu-id="3b0ee-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3b0ee-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3b0ee-130">See also</span></span>



- [<span data-ttu-id="3b0ee-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="3b0ee-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

