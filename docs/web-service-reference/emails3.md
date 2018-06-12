---
title: Emails3
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4f4dc589-4530-4a35-b2a6-0c83cac23637
description: Emails3 元素指定的 EmailAddressAttributedValue 值的数组和为相关联的角色其源归属的标识符。
ms.openlocfilehash: 1d174000d59883446bb7f61af90278d197ef5ed9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754068"
---
# <a name="emails3"></a><span data-ttu-id="9b91a-103">Emails3</span><span class="sxs-lookup"><span data-stu-id="9b91a-103">Emails3</span></span>

<span data-ttu-id="9b91a-104">**Emails3**元素指定的**EmailAddressAttributedValue**值的数组和为相关联的角色其源归属的标识符。</span><span class="sxs-lookup"><span data-stu-id="9b91a-104">The **Emails3** element specifies an array of **EmailAddressAttributedValue** values and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<Emails3>
    <EmailAddressAttributedValue></EmailAddressAttributedValue>
</Emails3>
```

 <span data-ttu-id="9b91a-105">**ArrayOfEmailAddressAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="9b91a-105">**ArrayOfEmailAddressAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9b91a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9b91a-106">Attributes and elements</span></span>

<span data-ttu-id="9b91a-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9b91a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9b91a-108">属性</span><span class="sxs-lookup"><span data-stu-id="9b91a-108">Attributes</span></span>

<span data-ttu-id="9b91a-109">无。</span><span class="sxs-lookup"><span data-stu-id="9b91a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9b91a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="9b91a-110">Child elements</span></span>

|<span data-ttu-id="9b91a-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="9b91a-111">**Element**</span></span>|<span data-ttu-id="9b91a-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="9b91a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9b91a-113">EmailAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="9b91a-113">EmailAddressAttributedValue</span></span>](emailaddressattributedvalue.md) <br/> |<span data-ttu-id="9b91a-114">指定一个电子邮件地址和其关联的归属的数组的实例。</span><span class="sxs-lookup"><span data-stu-id="9b91a-114">Specifies an instance of an array of email addresses and their associated attributions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9b91a-115">父元素</span><span class="sxs-lookup"><span data-stu-id="9b91a-115">Parent elements</span></span>

|<span data-ttu-id="9b91a-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="9b91a-116">**Element**</span></span>|<span data-ttu-id="9b91a-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="9b91a-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9b91a-118">角色</span><span class="sxs-lookup"><span data-stu-id="9b91a-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="9b91a-119">指定一组个人**GetPersona**请求返回的数据。</span><span class="sxs-lookup"><span data-stu-id="9b91a-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9b91a-120">备注</span><span class="sxs-lookup"><span data-stu-id="9b91a-120">Remarks</span></span>

<span data-ttu-id="9b91a-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="9b91a-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="9b91a-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9b91a-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9b91a-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="9b91a-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9b91a-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="9b91a-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9b91a-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="9b91a-125">Schema Name</span></span>  <br/> |<span data-ttu-id="9b91a-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="9b91a-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="9b91a-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="9b91a-127">Validation File</span></span>  <br/> |<span data-ttu-id="9b91a-128">types.xsd</span><span class="sxs-lookup"><span data-stu-id="9b91a-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="9b91a-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="9b91a-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="9b91a-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9b91a-130">See also</span></span>



- [<span data-ttu-id="9b91a-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="9b91a-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

