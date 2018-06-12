---
title: EmailAddresses (ArrayOfEmailAddressesType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 95084659-aa5a-4bac-8977-00db3b87883e
description: EmailAddresses 元素指定数组的相关联的角色的所有电子邮件地址。
ms.openlocfilehash: 292d4c3f12b01f25fd094b2ab6d9c2d484d37694
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754060"
---
# <a name="emailaddresses-arrayofemailaddressestype"></a><span data-ttu-id="95793-103">EmailAddresses (ArrayOfEmailAddressesType)</span><span class="sxs-lookup"><span data-stu-id="95793-103">EmailAddresses (ArrayOfEmailAddressesType)</span></span>

<span data-ttu-id="95793-104">**EmailAddresses**元素指定数组的相关联的角色的所有电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="95793-104">The **EmailAddresses** element specifies an array of all email addresses of the associated persona.</span></span> 
  
```XML
<EmailAddresses>
    <Address></Address>
</EmailAddresses>
```

 <span data-ttu-id="95793-105">**ArrayOfEmailAddressesType**</span><span class="sxs-lookup"><span data-stu-id="95793-105">**ArrayOfEmailAddressesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="95793-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="95793-106">Attributes and elements</span></span>

<span data-ttu-id="95793-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="95793-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="95793-108">属性</span><span class="sxs-lookup"><span data-stu-id="95793-108">Attributes</span></span>

<span data-ttu-id="95793-109">无。</span><span class="sxs-lookup"><span data-stu-id="95793-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="95793-110">子元素</span><span class="sxs-lookup"><span data-stu-id="95793-110">Child elements</span></span>

|<span data-ttu-id="95793-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="95793-111">**Element**</span></span>|<span data-ttu-id="95793-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="95793-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="95793-113">地址 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="95793-113">Address (EmailAddressType)</span></span>](address-emailaddresstype.md) <br/> |<span data-ttu-id="95793-114">表示一个完全解析电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="95793-114">Represents a fully resolved e-mail address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="95793-115">父元素</span><span class="sxs-lookup"><span data-stu-id="95793-115">Parent elements</span></span>

|<span data-ttu-id="95793-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="95793-116">**Element**</span></span>|<span data-ttu-id="95793-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="95793-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="95793-118">角色</span><span class="sxs-lookup"><span data-stu-id="95793-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="95793-119">指定一组个人**GetPersona**请求返回的数据。</span><span class="sxs-lookup"><span data-stu-id="95793-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="95793-120">备注</span><span class="sxs-lookup"><span data-stu-id="95793-120">Remarks</span></span>

<span data-ttu-id="95793-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="95793-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="95793-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="95793-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="95793-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="95793-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="95793-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="95793-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="95793-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="95793-125">Schema Name</span></span>  <br/> |<span data-ttu-id="95793-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="95793-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="95793-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="95793-127">Validation File</span></span>  <br/> |<span data-ttu-id="95793-128">types.xsd</span><span class="sxs-lookup"><span data-stu-id="95793-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="95793-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="95793-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="95793-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="95793-130">See also</span></span>



- [<span data-ttu-id="95793-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="95793-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

