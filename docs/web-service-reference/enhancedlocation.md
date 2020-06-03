---
title: EnhancedLocation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4fdfb74f-f33c-46ae-a7c7-451a5b0c6a59
description: EnhancedLocation 元素指定位置信息，如名称、地址和关于某个位置的可选注释。
ms.openlocfilehash: 06ec800b763ef61af51da03ca8a340f6ac4d2a8e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462955"
---
# <a name="enhancedlocation"></a><span data-ttu-id="65979-103">EnhancedLocation</span><span class="sxs-lookup"><span data-stu-id="65979-103">EnhancedLocation</span></span>

<span data-ttu-id="65979-104">**EnhancedLocation**元素指定位置信息，如名称、地址和关于某个位置的可选注释。</span><span class="sxs-lookup"><span data-stu-id="65979-104">The **EnhancedLocation** element specifies location information such as the name, address, and optional notes about a location.</span></span> 
  
```XML
<EnhancedLocation>
    <DisplayName/>
    <Annotation/>
    <PostalAddress/>
</EnhancedLocation>
```

 <span data-ttu-id="65979-105">**EnhancedLocationType**</span><span class="sxs-lookup"><span data-stu-id="65979-105">**EnhancedLocationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="65979-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="65979-106">Attributes and elements</span></span>

<span data-ttu-id="65979-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="65979-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="65979-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="65979-108">Attributes</span></span>

<span data-ttu-id="65979-109">无。</span><span class="sxs-lookup"><span data-stu-id="65979-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="65979-110">子元素</span><span class="sxs-lookup"><span data-stu-id="65979-110">Child elements</span></span>

|<span data-ttu-id="65979-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="65979-111">**Element**</span></span>|<span data-ttu-id="65979-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="65979-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="65979-113">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="65979-113">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="65979-114">定义文件夹、联系人、通讯组列表、代理用户、位置或规则的显示名称。</span><span class="sxs-lookup"><span data-stu-id="65979-114">Defines the display name of a folder, contact, distribution list, delegate user, location, or rule.</span></span>  <br/> |
|[<span data-ttu-id="65979-115">Annotation</span><span class="sxs-lookup"><span data-stu-id="65979-115">Annotation</span></span>](annotation.md) <br/> |<span data-ttu-id="65979-116">包含用户添加的可选注释。</span><span class="sxs-lookup"><span data-stu-id="65979-116">Contains optional notes added by a user.</span></span>  <br/> |
|[<span data-ttu-id="65979-117">省略（PersonaPostalAddressType）</span><span class="sxs-lookup"><span data-stu-id="65979-117">PostalAddress (PersonaPostalAddressType)</span></span>](postaladdress-personapostaladdresstype.md) <br/> |<span data-ttu-id="65979-118">指定角色的邮政地址。</span><span class="sxs-lookup"><span data-stu-id="65979-118">Specifies the postal address for a persona.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="65979-119">父元素</span><span class="sxs-lookup"><span data-stu-id="65979-119">Parent elements</span></span>

|<span data-ttu-id="65979-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="65979-120">**Element**</span></span>|<span data-ttu-id="65979-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="65979-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="65979-122">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="65979-122">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="65979-123">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="65979-123">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="65979-124">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="65979-124">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="65979-125">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="65979-125">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="65979-126">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="65979-126">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="65979-127">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="65979-127">Represents a meeting response in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="65979-128">备注</span><span class="sxs-lookup"><span data-stu-id="65979-128">Remarks</span></span>

<span data-ttu-id="65979-129">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="65979-129">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="65979-130">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="65979-130">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="65979-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="65979-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="65979-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="65979-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="65979-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="65979-133">Schema Name</span></span>  <br/> |<span data-ttu-id="65979-134">类型架构</span><span class="sxs-lookup"><span data-stu-id="65979-134">Type schema</span></span>  <br/> |
|<span data-ttu-id="65979-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="65979-135">Validation File</span></span>  <br/> |<span data-ttu-id="65979-136">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="65979-136">types.xsd</span></span>  <br/> |
|<span data-ttu-id="65979-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="65979-137">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="65979-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="65979-138">See also</span></span>



- [<span data-ttu-id="65979-139">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="65979-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

