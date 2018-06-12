---
title: ImGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ab7b884e-ecf1-4e58-86ec-856b13a95f2b
description: ImGroup 元素均表示一个即时消息的组。
ms.openlocfilehash: 2a444158dbc6a73b1aee7b306cc251d33d005c43
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825890"
---
# <a name="imgroup"></a><span data-ttu-id="042a1-103">ImGroup</span><span class="sxs-lookup"><span data-stu-id="042a1-103">ImGroup</span></span>

<span data-ttu-id="042a1-104">**ImGroup**元素均表示一个即时消息的组。</span><span class="sxs-lookup"><span data-stu-id="042a1-104">The **ImGroup** element represents an instant messaging group.</span></span> 
  
```XML
<ImGroup>
   <DisplayName/>
   <GroupType/>
   <ExchangeStoreId/>
   <MemberCorrelationKey/>
   <ExtendedProperties/>
   <SmtpAddress/>
</ImGroup>
```

 <span data-ttu-id="042a1-105">**ImGroupType**</span><span class="sxs-lookup"><span data-stu-id="042a1-105">**ImGroupType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="042a1-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="042a1-106">Attributes and elements</span></span>

<span data-ttu-id="042a1-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="042a1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="042a1-108">属性</span><span class="sxs-lookup"><span data-stu-id="042a1-108">Attributes</span></span>

<span data-ttu-id="042a1-109">无。</span><span class="sxs-lookup"><span data-stu-id="042a1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="042a1-110">子元素</span><span class="sxs-lookup"><span data-stu-id="042a1-110">Child elements</span></span>

<span data-ttu-id="042a1-111">[DisplayName (NonEmptyStringType)](displayname-nonemptystringtype.md) | [GroupType](grouptype.md) | [ExchangeStoreId](exchangestoreid.md) | [MemberCorrelationKey](membercorrelationkey.md) | [ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)](extendedproperties-nonemptyarrayofextendedpropertytype.md)  |  [SmtpAddress](smtpaddress.md)</span><span class="sxs-lookup"><span data-stu-id="042a1-111">[DisplayName (NonEmptyStringType)](displayname-nonemptystringtype.md) | [GroupType](grouptype.md) | [ExchangeStoreId](exchangestoreid.md) | [MemberCorrelationKey](membercorrelationkey.md) | [ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)](extendedproperties-nonemptyarrayofextendedpropertytype.md) | [SmtpAddress](smtpaddress.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="042a1-112">父元素</span><span class="sxs-lookup"><span data-stu-id="042a1-112">Parent elements</span></span>

<span data-ttu-id="042a1-113">[组 (ArrayOfImGroupType)](groups-arrayofimgrouptype.md) | [AddDistributionGroupToImListResponse](adddistributiongrouptoimlistresponse.md) | [AddImGroupResponse](addimgroupresponse.md)</span><span class="sxs-lookup"><span data-stu-id="042a1-113">[Groups (ArrayOfImGroupType)](groups-arrayofimgrouptype.md) | [AddDistributionGroupToImListResponse](adddistributiongrouptoimlistresponse.md) | [AddImGroupResponse](addimgroupresponse.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="042a1-114">备注</span><span class="sxs-lookup"><span data-stu-id="042a1-114">Remarks</span></span>

<span data-ttu-id="042a1-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="042a1-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="042a1-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="042a1-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="042a1-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="042a1-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="042a1-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="042a1-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="042a1-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="042a1-119">Schema name</span></span>  <br/> |<span data-ttu-id="042a1-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="042a1-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="042a1-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="042a1-121">Validation file</span></span>  <br/> |<span data-ttu-id="042a1-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="042a1-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="042a1-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="042a1-123">Can be empty</span></span>  <br/> ||
   

