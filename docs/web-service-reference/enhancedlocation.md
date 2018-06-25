---
title: EnhancedLocation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4fdfb74f-f33c-46ae-a7c7-451a5b0c6a59
description: EnhancedLocation 元素指定如姓名、 地址和可选注释有关位置的位置信息。
ms.openlocfilehash: 90397cfc622fed40c561d30c13d6617eb979a68a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754129"
---
# <a name="enhancedlocation"></a><span data-ttu-id="62f53-103">EnhancedLocation</span><span class="sxs-lookup"><span data-stu-id="62f53-103">EnhancedLocation</span></span>

<span data-ttu-id="62f53-104">**EnhancedLocation**元素指定如姓名、 地址和可选注释有关位置的位置信息。</span><span class="sxs-lookup"><span data-stu-id="62f53-104">The **EnhancedLocation** element specifies location information such as the name, address, and optional notes about a location.</span></span> 
  
```XML
<EnhancedLocation>
    <DisplayName/>
    <Annotation/>
    <PostalAddress/>
</EnhancedLocation>
```

 <span data-ttu-id="62f53-105">**EnhancedLocationType**</span><span class="sxs-lookup"><span data-stu-id="62f53-105">**EnhancedLocationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="62f53-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="62f53-106">Attributes and elements</span></span>

<span data-ttu-id="62f53-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="62f53-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="62f53-108">属性</span><span class="sxs-lookup"><span data-stu-id="62f53-108">Attributes</span></span>

<span data-ttu-id="62f53-109">无。</span><span class="sxs-lookup"><span data-stu-id="62f53-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="62f53-110">子元素</span><span class="sxs-lookup"><span data-stu-id="62f53-110">Child elements</span></span>

|<span data-ttu-id="62f53-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="62f53-111">**Element**</span></span>|<span data-ttu-id="62f53-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="62f53-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="62f53-113">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="62f53-113">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="62f53-114">定义文件夹、 联系人、 通讯组列表、 代理用户、 位置或规则的显示名称。</span><span class="sxs-lookup"><span data-stu-id="62f53-114">Defines the display name of a folder, contact, distribution list, delegate user, location, or rule.</span></span>  <br/> |
|[<span data-ttu-id="62f53-115">批注</span><span class="sxs-lookup"><span data-stu-id="62f53-115">Annotation</span></span>](annotation.md) <br/> |<span data-ttu-id="62f53-116">包含由用户添加的可选说明。</span><span class="sxs-lookup"><span data-stu-id="62f53-116">Contains optional notes added by a user.</span></span>  <br/> |
|[<span data-ttu-id="62f53-117">PostalAddress (PersonaPostalAddressType)</span><span class="sxs-lookup"><span data-stu-id="62f53-117">PostalAddress (PersonaPostalAddressType)</span></span>](postaladdress-personapostaladdresstype.md) <br/> |<span data-ttu-id="62f53-118">指定个人的邮政地址。</span><span class="sxs-lookup"><span data-stu-id="62f53-118">Specifies the postal address for a persona.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="62f53-119">父元素</span><span class="sxs-lookup"><span data-stu-id="62f53-119">Parent elements</span></span>

|<span data-ttu-id="62f53-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="62f53-120">**Element**</span></span>|<span data-ttu-id="62f53-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="62f53-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="62f53-122">日历项目</span><span class="sxs-lookup"><span data-stu-id="62f53-122">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="62f53-123">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="62f53-123">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="62f53-124">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="62f53-124">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="62f53-125">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="62f53-125">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="62f53-126">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="62f53-126">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="62f53-127">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="62f53-127">Represents a meeting response in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="62f53-128">备注</span><span class="sxs-lookup"><span data-stu-id="62f53-128">Remarks</span></span>

<span data-ttu-id="62f53-129">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="62f53-129">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="62f53-130">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="62f53-130">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="62f53-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="62f53-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="62f53-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="62f53-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="62f53-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="62f53-133">Schema Name</span></span>  <br/> |<span data-ttu-id="62f53-134">类型架构</span><span class="sxs-lookup"><span data-stu-id="62f53-134">Type schema</span></span>  <br/> |
|<span data-ttu-id="62f53-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="62f53-135">Validation File</span></span>  <br/> |<span data-ttu-id="62f53-136">types.xsd</span><span class="sxs-lookup"><span data-stu-id="62f53-136">types.xsd</span></span>  <br/> |
|<span data-ttu-id="62f53-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="62f53-137">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="62f53-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="62f53-138">See also</span></span>



- [<span data-ttu-id="62f53-139">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="62f53-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

