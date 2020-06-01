---
title: UserSMIMECertificate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 66e6b4ba-368d-4469-bd47-e59441b7d64d
description: UserSMIMECertificate 元素包含对联系人的 SMIME 证书进行编码的值。
ms.openlocfilehash: 7e2dbc6a9c8b04758ba99db036e237d8837850aa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467653"
---
# <a name="usersmimecertificate"></a><span data-ttu-id="87ae5-103">UserSMIMECertificate</span><span class="sxs-lookup"><span data-stu-id="87ae5-103">UserSMIMECertificate</span></span>

<span data-ttu-id="87ae5-104">**UserSMIMECertificate**元素包含对联系人的 SMIME 证书进行编码的值。</span><span class="sxs-lookup"><span data-stu-id="87ae5-104">The **UserSMIMECertificate** element contains a value that encodes a contact's SMIME certificate.</span></span> 
  
```XML
<UserSMIMECertificate/>
```

 <span data-ttu-id="87ae5-105">**ArrayOfBinaryType**</span><span class="sxs-lookup"><span data-stu-id="87ae5-105">**ArrayOfBinaryType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="87ae5-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="87ae5-106">Attributes and elements</span></span>

<span data-ttu-id="87ae5-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="87ae5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="87ae5-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="87ae5-108">Attributes</span></span>

<span data-ttu-id="87ae5-109">无。</span><span class="sxs-lookup"><span data-stu-id="87ae5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="87ae5-110">子元素</span><span class="sxs-lookup"><span data-stu-id="87ae5-110">Child elements</span></span>

|<span data-ttu-id="87ae5-111">**元素名**</span><span class="sxs-lookup"><span data-stu-id="87ae5-111">**Element name**</span></span>|<span data-ttu-id="87ae5-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="87ae5-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="87ae5-113">Base64Binary</span><span class="sxs-lookup"><span data-stu-id="87ae5-113">Base64Binary</span></span>](base64binary.md) <br/> |<span data-ttu-id="87ae5-114">包含 Base64 编码的值。</span><span class="sxs-lookup"><span data-stu-id="87ae5-114">Contains a Base64-encoded value.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="87ae5-115">父元素</span><span class="sxs-lookup"><span data-stu-id="87ae5-115">Parent elements</span></span>

|<span data-ttu-id="87ae5-116">**元素名**</span><span class="sxs-lookup"><span data-stu-id="87ae5-116">**Element name**</span></span>|<span data-ttu-id="87ae5-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="87ae5-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="87ae5-118">联系人</span><span class="sxs-lookup"><span data-stu-id="87ae5-118">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="87ae5-119">表示对 Exchange 存储中的联系人项目。</span><span class="sxs-lookup"><span data-stu-id="87ae5-119">Represents a contact item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="87ae5-120">文本值</span><span class="sxs-lookup"><span data-stu-id="87ae5-120">Text value</span></span>

<span data-ttu-id="87ae5-121">无。</span><span class="sxs-lookup"><span data-stu-id="87ae5-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="87ae5-122">说明</span><span class="sxs-lookup"><span data-stu-id="87ae5-122">Remarks</span></span>

<span data-ttu-id="87ae5-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="87ae5-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="87ae5-124">Exchange Server 2010 Service Pack 2 (SP2) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="87ae5-124">This element was introduced in Exchange Server 2010 Service Pack 2 (SP2).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="87ae5-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="87ae5-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="87ae5-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="87ae5-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="87ae5-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="87ae5-127">Schema name</span></span>  <br/> |<span data-ttu-id="87ae5-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="87ae5-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="87ae5-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="87ae5-129">Validation file</span></span>  <br/> |<span data-ttu-id="87ae5-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="87ae5-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="87ae5-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="87ae5-131">Can be empty</span></span>  <br/> |<span data-ttu-id="87ae5-132">False</span><span class="sxs-lookup"><span data-stu-id="87ae5-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="87ae5-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="87ae5-133">See also</span></span>



- [<span data-ttu-id="87ae5-134">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="87ae5-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="87ae5-135">创建联系人（Exchange Web 服务）</span><span class="sxs-lookup"><span data-stu-id="87ae5-135">Creating Contacts (Exchange Web Services)</span></span>](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)

