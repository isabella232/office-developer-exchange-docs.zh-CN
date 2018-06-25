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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754068"
---
# <a name="emails3"></a><span data-ttu-id="f5b32-103">Emails3</span><span class="sxs-lookup"><span data-stu-id="f5b32-103">Emails3</span></span>

<span data-ttu-id="f5b32-104">**Emails3**元素指定的**EmailAddressAttributedValue**值的数组和为相关联的角色其源归属的标识符。</span><span class="sxs-lookup"><span data-stu-id="f5b32-104">The **Emails3** element specifies an array of **EmailAddressAttributedValue** values and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<Emails3>
    <EmailAddressAttributedValue></EmailAddressAttributedValue>
</Emails3>
```

 <span data-ttu-id="f5b32-105">**ArrayOfEmailAddressAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="f5b32-105">**ArrayOfEmailAddressAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f5b32-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f5b32-106">Attributes and elements</span></span>

<span data-ttu-id="f5b32-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f5b32-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f5b32-108">属性</span><span class="sxs-lookup"><span data-stu-id="f5b32-108">Attributes</span></span>

<span data-ttu-id="f5b32-109">无。</span><span class="sxs-lookup"><span data-stu-id="f5b32-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f5b32-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f5b32-110">Child elements</span></span>

|<span data-ttu-id="f5b32-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="f5b32-111">**Element**</span></span>|<span data-ttu-id="f5b32-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="f5b32-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f5b32-113">EmailAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="f5b32-113">EmailAddressAttributedValue</span></span>](emailaddressattributedvalue.md) <br/> |<span data-ttu-id="f5b32-114">指定一个电子邮件地址和其关联的归属的数组的实例。</span><span class="sxs-lookup"><span data-stu-id="f5b32-114">Specifies an instance of an array of email addresses and their associated attributions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f5b32-115">父元素</span><span class="sxs-lookup"><span data-stu-id="f5b32-115">Parent elements</span></span>

|<span data-ttu-id="f5b32-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="f5b32-116">**Element**</span></span>|<span data-ttu-id="f5b32-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="f5b32-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f5b32-118">角色</span><span class="sxs-lookup"><span data-stu-id="f5b32-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="f5b32-119">指定一组个人**GetPersona**请求返回的数据。</span><span class="sxs-lookup"><span data-stu-id="f5b32-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f5b32-120">备注</span><span class="sxs-lookup"><span data-stu-id="f5b32-120">Remarks</span></span>

<span data-ttu-id="f5b32-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="f5b32-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="f5b32-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f5b32-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f5b32-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="f5b32-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f5b32-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="f5b32-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f5b32-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="f5b32-125">Schema Name</span></span>  <br/> |<span data-ttu-id="f5b32-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="f5b32-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="f5b32-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="f5b32-127">Validation File</span></span>  <br/> |<span data-ttu-id="f5b32-128">types.xsd</span><span class="sxs-lookup"><span data-stu-id="f5b32-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="f5b32-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="f5b32-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="f5b32-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f5b32-130">See also</span></span>



- [<span data-ttu-id="f5b32-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f5b32-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

