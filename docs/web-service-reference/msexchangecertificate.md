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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826498"
---
# <a name="msexchangecertificate"></a><span data-ttu-id="f86ad-103">MSExchangeCertificate</span><span class="sxs-lookup"><span data-stu-id="f86ad-103">MSExchangeCertificate</span></span>

<span data-ttu-id="f86ad-104">**MSExchangeCertificate**元素包含一个值，它将编码的联系人的 Microsoft Exchange 证书。</span><span class="sxs-lookup"><span data-stu-id="f86ad-104">The **MSExchangeCertificate** element contains a value that encodes the Microsoft Exchange certificate of a contact.</span></span> 
  
```XML
<MSExchangeCertificate/>
```

 <span data-ttu-id="f86ad-105">**ArrayOfBinaryType**</span><span class="sxs-lookup"><span data-stu-id="f86ad-105">**ArrayOfBinaryType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f86ad-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f86ad-106">Attributes and elements</span></span>

<span data-ttu-id="f86ad-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f86ad-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f86ad-108">属性</span><span class="sxs-lookup"><span data-stu-id="f86ad-108">Attributes</span></span>

<span data-ttu-id="f86ad-109">无。</span><span class="sxs-lookup"><span data-stu-id="f86ad-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f86ad-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f86ad-110">Child elements</span></span>

|<span data-ttu-id="f86ad-111">**元素名**</span><span class="sxs-lookup"><span data-stu-id="f86ad-111">**Element name**</span></span>|<span data-ttu-id="f86ad-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="f86ad-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f86ad-113">Base64Binary</span><span class="sxs-lookup"><span data-stu-id="f86ad-113">Base64Binary</span></span>](base64binary.md) <br/> |<span data-ttu-id="f86ad-114">包含一个 Base64 编码的值。</span><span class="sxs-lookup"><span data-stu-id="f86ad-114">Contains a Base64-encoded value.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f86ad-115">父元素</span><span class="sxs-lookup"><span data-stu-id="f86ad-115">Parent elements</span></span>

|<span data-ttu-id="f86ad-116">**元素名**</span><span class="sxs-lookup"><span data-stu-id="f86ad-116">**Element name**</span></span>|<span data-ttu-id="f86ad-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="f86ad-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f86ad-118">联系人</span><span class="sxs-lookup"><span data-stu-id="f86ad-118">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="f86ad-119">表示对 Exchange 存储中的联系人项目。</span><span class="sxs-lookup"><span data-stu-id="f86ad-119">Represents a contact item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f86ad-120">文本值</span><span class="sxs-lookup"><span data-stu-id="f86ad-120">Text value</span></span>

<span data-ttu-id="f86ad-121">无。</span><span class="sxs-lookup"><span data-stu-id="f86ad-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f86ad-122">备注</span><span class="sxs-lookup"><span data-stu-id="f86ad-122">Remarks</span></span>

<span data-ttu-id="f86ad-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f86ad-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="f86ad-124">Exchange Server 2010 Service Pack 2 (SP2) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="f86ad-124">This element was introduced in Exchange Server 2010 Service Pack 2 (SP2).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f86ad-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="f86ad-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f86ad-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="f86ad-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f86ad-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="f86ad-127">Schema name</span></span>  <br/> |<span data-ttu-id="f86ad-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="f86ad-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="f86ad-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="f86ad-129">Validation file</span></span>  <br/> |<span data-ttu-id="f86ad-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f86ad-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f86ad-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="f86ad-131">Can be empty</span></span>  <br/> |<span data-ttu-id="f86ad-132">False</span><span class="sxs-lookup"><span data-stu-id="f86ad-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f86ad-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f86ad-133">See also</span></span>



- [<span data-ttu-id="f86ad-134">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f86ad-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="f86ad-135">Creating Contacts (Exchange Web Services)</span><span class="sxs-lookup"><span data-stu-id="f86ad-135">Creating Contacts (Exchange Web Services)</span></span>](http://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)

