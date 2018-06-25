---
title: 聊天室
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
ms.openlocfilehash: e95112d3d565da29c309e45710ffc0ea9b4d5064
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827249"
---
# <a name="rooms"></a><span data-ttu-id="e4242-103">聊天室</span><span class="sxs-lookup"><span data-stu-id="e4242-103">Rooms</span></span>

<span data-ttu-id="e4242-104">**聊天室**元素是表示会议室的一个或多个元素的列表。</span><span class="sxs-lookup"><span data-stu-id="e4242-104">The **Rooms** element is a list of one or more elements that represent meeting rooms.</span></span> 
  
[<span data-ttu-id="e4242-105">GetRoomsResponse</span><span class="sxs-lookup"><span data-stu-id="e4242-105">GetRoomsResponse</span></span>](getroomsresponse.md)
  
[<span data-ttu-id="e4242-106">聊天室</span><span class="sxs-lookup"><span data-stu-id="e4242-106">Rooms</span></span>](rooms.md)
  
```xml
<Rooms>   <Room/></Rooms>
```

 <span data-ttu-id="e4242-107">**ArrayOfRoomsType**</span><span class="sxs-lookup"><span data-stu-id="e4242-107">**ArrayOfRoomsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e4242-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e4242-108">Attributes and elements</span></span>

<span data-ttu-id="e4242-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e4242-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e4242-110">属性</span><span class="sxs-lookup"><span data-stu-id="e4242-110">Attributes</span></span>

<span data-ttu-id="e4242-111">无。</span><span class="sxs-lookup"><span data-stu-id="e4242-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e4242-112">子元素</span><span class="sxs-lookup"><span data-stu-id="e4242-112">Child elements</span></span>

|<span data-ttu-id="e4242-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="e4242-113">**Element**</span></span>|<span data-ttu-id="e4242-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="e4242-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e4242-115">聊天室</span><span class="sxs-lookup"><span data-stu-id="e4242-115">Room</span></span>](room.md) <br/> |<span data-ttu-id="e4242-116">定义电子邮件地址和代表会议室的显示名称。</span><span class="sxs-lookup"><span data-stu-id="e4242-116">Defines an e-mail address and display name that represents a meeting room.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e4242-117">父元素</span><span class="sxs-lookup"><span data-stu-id="e4242-117">Parent elements</span></span>

|<span data-ttu-id="e4242-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="e4242-118">**Element**</span></span>|<span data-ttu-id="e4242-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="e4242-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e4242-120">GetRoomsResponse</span><span class="sxs-lookup"><span data-stu-id="e4242-120">GetRoomsResponse</span></span>](getroomsresponse.md) <br/> ||
   
## <a name="remarks"></a><span data-ttu-id="e4242-121">注解</span><span class="sxs-lookup"><span data-stu-id="e4242-121">Remarks</span></span>

<span data-ttu-id="e4242-122">描述此元素的架构位于运行 Microsoft Exchange Server 已安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e4242-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e4242-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="e4242-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e4242-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="e4242-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e4242-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="e4242-125">Schema Name</span></span>  <br/> |<span data-ttu-id="e4242-126">消息架构</span><span class="sxs-lookup"><span data-stu-id="e4242-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e4242-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="e4242-127">Validation File</span></span>  <br/> |<span data-ttu-id="e4242-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e4242-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e4242-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="e4242-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="e4242-130">False</span><span class="sxs-lookup"><span data-stu-id="e4242-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e4242-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e4242-131">See also</span></span>



[<span data-ttu-id="e4242-132">GetRooms 操作</span><span class="sxs-lookup"><span data-stu-id="e4242-132">GetRooms operation</span></span>](getrooms-operation.md)


- [<span data-ttu-id="e4242-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e4242-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

