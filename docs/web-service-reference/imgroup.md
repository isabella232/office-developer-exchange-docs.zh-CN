---
title: ImGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ab7b884e-ecf1-4e58-86ec-856b13a95f2b
description: ImGroup 元素表示即时消息组。
ms.openlocfilehash: a0ff3fcb82e7f18837af5a6f5daa16e90043034d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460685"
---
# <a name="imgroup"></a><span data-ttu-id="5a5da-103">ImGroup</span><span class="sxs-lookup"><span data-stu-id="5a5da-103">ImGroup</span></span>

<span data-ttu-id="5a5da-104">**ImGroup**元素表示即时消息组。</span><span class="sxs-lookup"><span data-stu-id="5a5da-104">The **ImGroup** element represents an instant messaging group.</span></span> 
  
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

 <span data-ttu-id="5a5da-105">**ImGroupType**</span><span class="sxs-lookup"><span data-stu-id="5a5da-105">**ImGroupType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5a5da-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5a5da-106">Attributes and elements</span></span>

<span data-ttu-id="5a5da-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5a5da-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5a5da-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="5a5da-108">Attributes</span></span>

<span data-ttu-id="5a5da-109">无。</span><span class="sxs-lookup"><span data-stu-id="5a5da-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5a5da-110">子元素</span><span class="sxs-lookup"><span data-stu-id="5a5da-110">Child elements</span></span>

<span data-ttu-id="5a5da-111">[DisplayName （NonEmptyStringType）](displayname-nonemptystringtype.md)  | [GroupType](grouptype.md)  | [ExchangeStoreId](exchangestoreid.md)  | [MemberCorrelationKey](membercorrelationkey.md)  | [ExtendedProperties （NonEmptyArrayOfExtendedPropertyType）](extendedproperties-nonemptyarrayofextendedpropertytype.md)  | [SmtpAddress](smtpaddress.md)</span><span class="sxs-lookup"><span data-stu-id="5a5da-111">[DisplayName (NonEmptyStringType)](displayname-nonemptystringtype.md) | [GroupType](grouptype.md) | [ExchangeStoreId](exchangestoreid.md) | [MemberCorrelationKey](membercorrelationkey.md) | [ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)](extendedproperties-nonemptyarrayofextendedpropertytype.md) | [SmtpAddress](smtpaddress.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5a5da-112">父元素</span><span class="sxs-lookup"><span data-stu-id="5a5da-112">Parent elements</span></span>

<span data-ttu-id="5a5da-113">[组（ArrayOfImGroupType）](groups-arrayofimgrouptype.md)  | [AddDistributionGroupToImListResponse](adddistributiongrouptoimlistresponse.md)  | [AddImGroupResponse](addimgroupresponse.md)</span><span class="sxs-lookup"><span data-stu-id="5a5da-113">[Groups (ArrayOfImGroupType)](groups-arrayofimgrouptype.md) | [AddDistributionGroupToImListResponse](adddistributiongrouptoimlistresponse.md) | [AddImGroupResponse](addimgroupresponse.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5a5da-114">备注</span><span class="sxs-lookup"><span data-stu-id="5a5da-114">Remarks</span></span>

<span data-ttu-id="5a5da-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="5a5da-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="5a5da-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="5a5da-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5a5da-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="5a5da-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5a5da-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="5a5da-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5a5da-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="5a5da-119">Schema name</span></span>  <br/> |<span data-ttu-id="5a5da-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="5a5da-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="5a5da-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="5a5da-121">Validation file</span></span>  <br/> |<span data-ttu-id="5a5da-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="5a5da-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5a5da-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="5a5da-123">Can be empty</span></span>  <br/> ||
   

