---
title: Emails3
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4f4dc589-4530-4a35-b2a6-0c83cac23637
description: Emails3 元素指定 EmailAddressAttributedValue 值的数组以及关联角色的源归属的标识符。
ms.openlocfilehash: 0505b0ea248a3ab2de7ec18a344fa57651f84cca
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460720"
---
# <a name="emails3"></a><span data-ttu-id="2d4b8-103">Emails3</span><span class="sxs-lookup"><span data-stu-id="2d4b8-103">Emails3</span></span>

<span data-ttu-id="2d4b8-104">**Emails3**元素指定**EmailAddressAttributedValue**值的数组以及关联角色的源归属的标识符。</span><span class="sxs-lookup"><span data-stu-id="2d4b8-104">The **Emails3** element specifies an array of **EmailAddressAttributedValue** values and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<Emails3>
    <EmailAddressAttributedValue></EmailAddressAttributedValue>
</Emails3>
```

 <span data-ttu-id="2d4b8-105">**ArrayOfEmailAddressAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="2d4b8-105">**ArrayOfEmailAddressAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2d4b8-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2d4b8-106">Attributes and elements</span></span>

<span data-ttu-id="2d4b8-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2d4b8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2d4b8-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="2d4b8-108">Attributes</span></span>

<span data-ttu-id="2d4b8-109">无。</span><span class="sxs-lookup"><span data-stu-id="2d4b8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2d4b8-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2d4b8-110">Child elements</span></span>

|<span data-ttu-id="2d4b8-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="2d4b8-111">**Element**</span></span>|<span data-ttu-id="2d4b8-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="2d4b8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2d4b8-113">EmailAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="2d4b8-113">EmailAddressAttributedValue</span></span>](emailaddressattributedvalue.md) <br/> |<span data-ttu-id="2d4b8-114">指定电子邮件地址数组的实例及其关联的归属。</span><span class="sxs-lookup"><span data-stu-id="2d4b8-114">Specifies an instance of an array of email addresses and their associated attributions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2d4b8-115">父元素</span><span class="sxs-lookup"><span data-stu-id="2d4b8-115">Parent elements</span></span>

|<span data-ttu-id="2d4b8-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="2d4b8-116">**Element**</span></span>|<span data-ttu-id="2d4b8-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="2d4b8-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2d4b8-118">角色</span><span class="sxs-lookup"><span data-stu-id="2d4b8-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="2d4b8-119">指定由**GetPersona**请求返回的一组角色数据。</span><span class="sxs-lookup"><span data-stu-id="2d4b8-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2d4b8-120">备注</span><span class="sxs-lookup"><span data-stu-id="2d4b8-120">Remarks</span></span>

<span data-ttu-id="2d4b8-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="2d4b8-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2d4b8-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2d4b8-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2d4b8-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="2d4b8-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2d4b8-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="2d4b8-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2d4b8-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="2d4b8-125">Schema Name</span></span>  <br/> |<span data-ttu-id="2d4b8-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="2d4b8-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="2d4b8-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="2d4b8-127">Validation File</span></span>  <br/> |<span data-ttu-id="2d4b8-128">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="2d4b8-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="2d4b8-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="2d4b8-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="2d4b8-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2d4b8-130">See also</span></span>



- [<span data-ttu-id="2d4b8-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2d4b8-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

