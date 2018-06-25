---
title: MSExchangeCertificate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c514f22f-be3e-4cad-ac56-bdff6bafcee6
description: MSExchangeCertificate 元素包含一个值，它将编码的联系人的 Microsoft Exchange 证书。
ms.openlocfilehash: 8d07198012485b5c6d22e1fb4721890bf9a5eb39
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826498"
---
# <a name="msexchangecertificate"></a><span data-ttu-id="21e74-103">MSExchangeCertificate</span><span class="sxs-lookup"><span data-stu-id="21e74-103">MSExchangeCertificate</span></span>

<span data-ttu-id="21e74-104">**MSExchangeCertificate**元素包含一个值，它将编码的联系人的 Microsoft Exchange 证书。</span><span class="sxs-lookup"><span data-stu-id="21e74-104">The **MSExchangeCertificate** element contains a value that encodes the Microsoft Exchange certificate of a contact.</span></span> 
  
```XML
<MSExchangeCertificate/>
```

 <span data-ttu-id="21e74-105">**ArrayOfBinaryType**</span><span class="sxs-lookup"><span data-stu-id="21e74-105">**ArrayOfBinaryType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="21e74-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="21e74-106">Attributes and elements</span></span>

<span data-ttu-id="21e74-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="21e74-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="21e74-108">属性</span><span class="sxs-lookup"><span data-stu-id="21e74-108">Attributes</span></span>

<span data-ttu-id="21e74-109">无。</span><span class="sxs-lookup"><span data-stu-id="21e74-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="21e74-110">子元素</span><span class="sxs-lookup"><span data-stu-id="21e74-110">Child elements</span></span>

|<span data-ttu-id="21e74-111">**元素名**</span><span class="sxs-lookup"><span data-stu-id="21e74-111">**Element name**</span></span>|<span data-ttu-id="21e74-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="21e74-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="21e74-113">Base64Binary</span><span class="sxs-lookup"><span data-stu-id="21e74-113">Base64Binary</span></span>](base64binary.md) <br/> |<span data-ttu-id="21e74-114">包含一个 Base64 编码的值。</span><span class="sxs-lookup"><span data-stu-id="21e74-114">Contains a Base64-encoded value.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="21e74-115">父元素</span><span class="sxs-lookup"><span data-stu-id="21e74-115">Parent elements</span></span>

|<span data-ttu-id="21e74-116">**元素名**</span><span class="sxs-lookup"><span data-stu-id="21e74-116">**Element name**</span></span>|<span data-ttu-id="21e74-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="21e74-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="21e74-118">联系人</span><span class="sxs-lookup"><span data-stu-id="21e74-118">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="21e74-119">表示对 Exchange 存储中的联系人项目。</span><span class="sxs-lookup"><span data-stu-id="21e74-119">Represents a contact item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="21e74-120">文本值</span><span class="sxs-lookup"><span data-stu-id="21e74-120">Text value</span></span>

<span data-ttu-id="21e74-121">无。</span><span class="sxs-lookup"><span data-stu-id="21e74-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="21e74-122">备注</span><span class="sxs-lookup"><span data-stu-id="21e74-122">Remarks</span></span>

<span data-ttu-id="21e74-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="21e74-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="21e74-124">Exchange Server 2010 Service Pack 2 (SP2) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="21e74-124">This element was introduced in Exchange Server 2010 Service Pack 2 (SP2).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="21e74-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="21e74-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="21e74-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="21e74-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="21e74-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="21e74-127">Schema name</span></span>  <br/> |<span data-ttu-id="21e74-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="21e74-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="21e74-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="21e74-129">Validation file</span></span>  <br/> |<span data-ttu-id="21e74-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="21e74-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="21e74-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="21e74-131">Can be empty</span></span>  <br/> |<span data-ttu-id="21e74-132">False</span><span class="sxs-lookup"><span data-stu-id="21e74-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="21e74-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="21e74-133">See also</span></span>



- [<span data-ttu-id="21e74-134">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="21e74-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="21e74-135">Creating Contacts (Exchange Web Services)</span><span class="sxs-lookup"><span data-stu-id="21e74-135">Creating Contacts (Exchange Web Services)</span></span>](http://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)

