---
title: 所属
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Rooms
api_type:
- schema
ms.assetid: 57b6079a-3d83-4429-861e-c551e9e1a991
description: 聊天室元素是表示会议室的一个或多个元素的列表。
ms.openlocfilehash: f8b60a9680f6abba459ebecc96613abfdd93766d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466183"
---
# <a name="rooms"></a><span data-ttu-id="8defe-103">所属</span><span class="sxs-lookup"><span data-stu-id="8defe-103">Rooms</span></span>

<span data-ttu-id="8defe-104">**聊天室**元素是表示会议室的一个或多个元素的列表。</span><span class="sxs-lookup"><span data-stu-id="8defe-104">The **Rooms** element is a list of one or more elements that represent meeting rooms.</span></span> 
  
[<span data-ttu-id="8defe-105">GetRoomsResponse</span><span class="sxs-lookup"><span data-stu-id="8defe-105">GetRoomsResponse</span></span>](getroomsresponse.md)
  
[<span data-ttu-id="8defe-106">所属</span><span class="sxs-lookup"><span data-stu-id="8defe-106">Rooms</span></span>](rooms.md)
  
```xml
<Rooms>   <Room/></Rooms>
```

 <span data-ttu-id="8defe-107">**ArrayOfRoomsType**</span><span class="sxs-lookup"><span data-stu-id="8defe-107">**ArrayOfRoomsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8defe-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8defe-108">Attributes and elements</span></span>

<span data-ttu-id="8defe-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8defe-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8defe-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="8defe-110">Attributes</span></span>

<span data-ttu-id="8defe-111">无。</span><span class="sxs-lookup"><span data-stu-id="8defe-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8defe-112">子元素</span><span class="sxs-lookup"><span data-stu-id="8defe-112">Child elements</span></span>

|<span data-ttu-id="8defe-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="8defe-113">**Element**</span></span>|<span data-ttu-id="8defe-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="8defe-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8defe-115">房间</span><span class="sxs-lookup"><span data-stu-id="8defe-115">Room</span></span>](room.md) <br/> |<span data-ttu-id="8defe-116">定义表示会议室的电子邮件地址和显示名称。</span><span class="sxs-lookup"><span data-stu-id="8defe-116">Defines an e-mail address and display name that represents a meeting room.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8defe-117">父元素</span><span class="sxs-lookup"><span data-stu-id="8defe-117">Parent elements</span></span>

|<span data-ttu-id="8defe-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="8defe-118">**Element**</span></span>|<span data-ttu-id="8defe-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="8defe-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8defe-120">GetRoomsResponse</span><span class="sxs-lookup"><span data-stu-id="8defe-120">GetRoomsResponse</span></span>](getroomsresponse.md) <br/> ||
   
## <a name="remarks"></a><span data-ttu-id="8defe-121">备注</span><span class="sxs-lookup"><span data-stu-id="8defe-121">Remarks</span></span>

<span data-ttu-id="8defe-122">描述此元素的架构位于运行 Microsoft Exchange Server 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8defe-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8defe-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="8defe-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8defe-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="8defe-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8defe-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="8defe-125">Schema Name</span></span>  <br/> |<span data-ttu-id="8defe-126">消息架构</span><span class="sxs-lookup"><span data-stu-id="8defe-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8defe-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="8defe-127">Validation File</span></span>  <br/> |<span data-ttu-id="8defe-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8defe-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8defe-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="8defe-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="8defe-130">False</span><span class="sxs-lookup"><span data-stu-id="8defe-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8defe-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8defe-131">See also</span></span>



[<span data-ttu-id="8defe-132">GetRooms 操作</span><span class="sxs-lookup"><span data-stu-id="8defe-132">GetRooms operation</span></span>](getrooms-operation.md)


- [<span data-ttu-id="8defe-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="8defe-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

