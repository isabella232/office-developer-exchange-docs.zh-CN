---
title: 房间
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Room
api_type:
- schema
ms.assetid: a2cde8b8-2d31-4ebf-8171-f4dfd650d079
description: 聊天室元素表示会议室。
ms.openlocfilehash: 3d5d587853e435016fdff6b9d268892a35fea825
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460531"
---
# <a name="room"></a><span data-ttu-id="35d55-103">房间</span><span class="sxs-lookup"><span data-stu-id="35d55-103">Room</span></span>

<span data-ttu-id="35d55-104">**聊天室**元素表示会议室。</span><span class="sxs-lookup"><span data-stu-id="35d55-104">The **Room** element represents a meeting room.</span></span> 
  
[<span data-ttu-id="35d55-105">所属</span><span class="sxs-lookup"><span data-stu-id="35d55-105">Rooms</span></span>](rooms.md)
  
[<span data-ttu-id="35d55-106">房间</span><span class="sxs-lookup"><span data-stu-id="35d55-106">Room</span></span>](room.md)
  
```XML
<Room>
   <Id/>
</Room>
```

 <span data-ttu-id="35d55-107">**RoomType**</span><span class="sxs-lookup"><span data-stu-id="35d55-107">**RoomType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="35d55-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="35d55-108">Attributes and elements</span></span>

<span data-ttu-id="35d55-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="35d55-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="35d55-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="35d55-110">Attributes</span></span>

<span data-ttu-id="35d55-111">无。</span><span class="sxs-lookup"><span data-stu-id="35d55-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="35d55-112">子元素</span><span class="sxs-lookup"><span data-stu-id="35d55-112">Child elements</span></span>

|<span data-ttu-id="35d55-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="35d55-113">**Element**</span></span>|<span data-ttu-id="35d55-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="35d55-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="35d55-115">Id （EmailAddressType）</span><span class="sxs-lookup"><span data-stu-id="35d55-115">Id (EmailAddressType)</span></span>](id-emailaddresstype.md) <br/> |<span data-ttu-id="35d55-116">包含表示会议室的电子邮件地址和显示名称的标识符。</span><span class="sxs-lookup"><span data-stu-id="35d55-116">An identifier that contains an email address and display name that represents the meeting room.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="35d55-117">父元素</span><span class="sxs-lookup"><span data-stu-id="35d55-117">Parent elements</span></span>

|<span data-ttu-id="35d55-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="35d55-118">**Element**</span></span>|<span data-ttu-id="35d55-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="35d55-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="35d55-120">所属</span><span class="sxs-lookup"><span data-stu-id="35d55-120">Rooms</span></span>](rooms.md) <br/> |<span data-ttu-id="35d55-121">定义与常见功能相关联的会议室的列表，如位于同一建筑物中。</span><span class="sxs-lookup"><span data-stu-id="35d55-121">Defines a list of meeting rooms associated with a common feature, such as being located in the same building.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="35d55-122">说明</span><span class="sxs-lookup"><span data-stu-id="35d55-122">Remarks</span></span>

<span data-ttu-id="35d55-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="35d55-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="35d55-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="35d55-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="35d55-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="35d55-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="35d55-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="35d55-126">Schema Name</span></span>  <br/> |<span data-ttu-id="35d55-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="35d55-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="35d55-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="35d55-128">Validation File</span></span>  <br/> |<span data-ttu-id="35d55-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="35d55-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="35d55-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="35d55-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="35d55-131">False</span><span class="sxs-lookup"><span data-stu-id="35d55-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="35d55-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="35d55-132">See also</span></span>



[<span data-ttu-id="35d55-133">GetRooms 操作</span><span class="sxs-lookup"><span data-stu-id="35d55-133">GetRooms operation</span></span>](getrooms-operation.md)


- [<span data-ttu-id="35d55-134">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="35d55-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

