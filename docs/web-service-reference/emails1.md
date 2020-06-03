---
title: Emails1
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cc02bd86-c618-446a-92f0-749423cbc4ee
description: Emails1 元素指定 EmailAddressAttributedValue 值的数组以及关联角色的源归属的标识符。
ms.openlocfilehash: 916f87038cfe959045c93dba749f1dc3b85296e2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456169"
---
# <a name="emails1"></a><span data-ttu-id="2f72d-103">Emails1</span><span class="sxs-lookup"><span data-stu-id="2f72d-103">Emails1</span></span>

<span data-ttu-id="2f72d-104">**Emails1**元素指定**EmailAddressAttributedValue**值的数组以及关联角色的源归属的标识符。</span><span class="sxs-lookup"><span data-stu-id="2f72d-104">The **Emails1** element specifies an array of **EmailAddressAttributedValue** values and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<Emails1>
    <EmailAddressAttributedValue></EmailAddressAttributedValue>
</Emails1>
```

 <span data-ttu-id="2f72d-105">**ArrayOfEmailAddressAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="2f72d-105">**ArrayOfEmailAddressAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2f72d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2f72d-106">Attributes and elements</span></span>

<span data-ttu-id="2f72d-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2f72d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2f72d-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="2f72d-108">Attributes</span></span>

<span data-ttu-id="2f72d-109">无。</span><span class="sxs-lookup"><span data-stu-id="2f72d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2f72d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2f72d-110">Child elements</span></span>

|<span data-ttu-id="2f72d-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="2f72d-111">**Element**</span></span>|<span data-ttu-id="2f72d-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="2f72d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2f72d-113">EmailAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="2f72d-113">EmailAddressAttributedValue</span></span>](emailaddressattributedvalue.md) <br/> |<span data-ttu-id="2f72d-114">指定电子邮件地址数组的实例及其关联的归属。</span><span class="sxs-lookup"><span data-stu-id="2f72d-114">Specifies an instance of an array of email addresses and their associated attributions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2f72d-115">父元素</span><span class="sxs-lookup"><span data-stu-id="2f72d-115">Parent elements</span></span>

|<span data-ttu-id="2f72d-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="2f72d-116">**Element**</span></span>|<span data-ttu-id="2f72d-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="2f72d-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2f72d-118">角色</span><span class="sxs-lookup"><span data-stu-id="2f72d-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="2f72d-119">指定由**GetPersona**请求返回的一组角色数据。</span><span class="sxs-lookup"><span data-stu-id="2f72d-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2f72d-120">备注</span><span class="sxs-lookup"><span data-stu-id="2f72d-120">Remarks</span></span>

<span data-ttu-id="2f72d-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="2f72d-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2f72d-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2f72d-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2f72d-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="2f72d-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2f72d-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="2f72d-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2f72d-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="2f72d-125">Schema Name</span></span>  <br/> |<span data-ttu-id="2f72d-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="2f72d-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="2f72d-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="2f72d-127">Validation File</span></span>  <br/> |<span data-ttu-id="2f72d-128">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="2f72d-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="2f72d-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="2f72d-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="2f72d-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2f72d-130">See also</span></span>



- [<span data-ttu-id="2f72d-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2f72d-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

