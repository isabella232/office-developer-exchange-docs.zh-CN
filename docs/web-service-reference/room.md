---
title: 聊天室
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
description: 会议室元素均表示会议室。
ms.openlocfilehash: e064a458b5a9265fc9dad63c87c641eaf47d7062
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827242"
---
# <a name="room"></a><span data-ttu-id="257bc-103">聊天室</span><span class="sxs-lookup"><span data-stu-id="257bc-103">Room</span></span>

<span data-ttu-id="257bc-104">**会议室**元素均表示会议室。</span><span class="sxs-lookup"><span data-stu-id="257bc-104">The **Room** element represents a meeting room.</span></span> 
  
[<span data-ttu-id="257bc-105">聊天室</span><span class="sxs-lookup"><span data-stu-id="257bc-105">Rooms</span></span>](rooms.md)
  
[<span data-ttu-id="257bc-106">聊天室</span><span class="sxs-lookup"><span data-stu-id="257bc-106">Room</span></span>](room.md)
  
```XML
<Room>
   <Id/>
</Room>
```

 <span data-ttu-id="257bc-107">**RoomType**</span><span class="sxs-lookup"><span data-stu-id="257bc-107">**RoomType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="257bc-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="257bc-108">Attributes and elements</span></span>

<span data-ttu-id="257bc-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="257bc-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="257bc-110">属性</span><span class="sxs-lookup"><span data-stu-id="257bc-110">Attributes</span></span>

<span data-ttu-id="257bc-111">无。</span><span class="sxs-lookup"><span data-stu-id="257bc-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="257bc-112">子元素</span><span class="sxs-lookup"><span data-stu-id="257bc-112">Child elements</span></span>

|<span data-ttu-id="257bc-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="257bc-113">**Element**</span></span>|<span data-ttu-id="257bc-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="257bc-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="257bc-115">Id (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="257bc-115">Id (EmailAddressType)</span></span>](id-emailaddresstype.md) <br/> |<span data-ttu-id="257bc-116">一个包含电子邮件地址的标识符和代表会议室的显示名称。</span><span class="sxs-lookup"><span data-stu-id="257bc-116">An identifier that contains an email address and display name that represents the meeting room.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="257bc-117">父元素</span><span class="sxs-lookup"><span data-stu-id="257bc-117">Parent elements</span></span>

|<span data-ttu-id="257bc-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="257bc-118">**Element**</span></span>|<span data-ttu-id="257bc-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="257bc-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="257bc-120">聊天室</span><span class="sxs-lookup"><span data-stu-id="257bc-120">Rooms</span></span>](rooms.md) <br/> |<span data-ttu-id="257bc-121">定义常见功能，如正在位于同一构建相关联的会议室的列表。</span><span class="sxs-lookup"><span data-stu-id="257bc-121">Defines a list of meeting rooms associated with a common feature, such as being located in the same building.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="257bc-122">备注</span><span class="sxs-lookup"><span data-stu-id="257bc-122">Remarks</span></span>

<span data-ttu-id="257bc-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="257bc-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="257bc-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="257bc-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="257bc-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="257bc-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="257bc-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="257bc-126">Schema Name</span></span>  <br/> |<span data-ttu-id="257bc-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="257bc-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="257bc-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="257bc-128">Validation File</span></span>  <br/> |<span data-ttu-id="257bc-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="257bc-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="257bc-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="257bc-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="257bc-131">False</span><span class="sxs-lookup"><span data-stu-id="257bc-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="257bc-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="257bc-132">See also</span></span>



[<span data-ttu-id="257bc-133">GetRooms 操作</span><span class="sxs-lookup"><span data-stu-id="257bc-133">GetRooms operation</span></span>](getrooms-operation.md)


- [<span data-ttu-id="257bc-134">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="257bc-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

