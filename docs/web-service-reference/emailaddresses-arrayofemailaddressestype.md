---
title: EmailAddresses （ArrayOfEmailAddressesType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 95084659-aa5a-4bac-8977-00db3b87883e
description: EmailAddresses 元素指定关联角色的所有电子邮件地址的数组。
ms.openlocfilehash: e6132e9ef4ed13ea2546783f65d184fafeed5530
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463417"
---
# <a name="emailaddresses-arrayofemailaddressestype"></a><span data-ttu-id="e5199-103">EmailAddresses （ArrayOfEmailAddressesType）</span><span class="sxs-lookup"><span data-stu-id="e5199-103">EmailAddresses (ArrayOfEmailAddressesType)</span></span>

<span data-ttu-id="e5199-104">**EmailAddresses**元素指定关联角色的所有电子邮件地址的数组。</span><span class="sxs-lookup"><span data-stu-id="e5199-104">The **EmailAddresses** element specifies an array of all email addresses of the associated persona.</span></span> 
  
```XML
<EmailAddresses>
    <Address></Address>
</EmailAddresses>
```

 <span data-ttu-id="e5199-105">**ArrayOfEmailAddressesType**</span><span class="sxs-lookup"><span data-stu-id="e5199-105">**ArrayOfEmailAddressesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e5199-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e5199-106">Attributes and elements</span></span>

<span data-ttu-id="e5199-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e5199-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e5199-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="e5199-108">Attributes</span></span>

<span data-ttu-id="e5199-109">无。</span><span class="sxs-lookup"><span data-stu-id="e5199-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e5199-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e5199-110">Child elements</span></span>

|<span data-ttu-id="e5199-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="e5199-111">**Element**</span></span>|<span data-ttu-id="e5199-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="e5199-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e5199-113">地址 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="e5199-113">Address (EmailAddressType)</span></span>](address-emailaddresstype.md) <br/> |<span data-ttu-id="e5199-114">表示一个完全解析电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="e5199-114">Represents a fully resolved e-mail address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e5199-115">父元素</span><span class="sxs-lookup"><span data-stu-id="e5199-115">Parent elements</span></span>

|<span data-ttu-id="e5199-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="e5199-116">**Element**</span></span>|<span data-ttu-id="e5199-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="e5199-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e5199-118">角色</span><span class="sxs-lookup"><span data-stu-id="e5199-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="e5199-119">指定由**GetPersona**请求返回的一组角色数据。</span><span class="sxs-lookup"><span data-stu-id="e5199-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e5199-120">备注</span><span class="sxs-lookup"><span data-stu-id="e5199-120">Remarks</span></span>

<span data-ttu-id="e5199-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="e5199-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e5199-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e5199-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e5199-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="e5199-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e5199-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="e5199-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e5199-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="e5199-125">Schema Name</span></span>  <br/> |<span data-ttu-id="e5199-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="e5199-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="e5199-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="e5199-127">Validation File</span></span>  <br/> |<span data-ttu-id="e5199-128">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="e5199-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="e5199-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="e5199-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="e5199-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e5199-130">See also</span></span>



- [<span data-ttu-id="e5199-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e5199-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

