---
title: RoomLists
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RoomLists
api_type:
- schema
ms.assetid: 2b190823-b11e-4635-97e4-3aba5865fd05
description: RoomLists 元素是一个或多个地址表示的会议室列表的列表。
ms.openlocfilehash: eb03c34aeb5d80c4a9c6c92471e4094c63f04c87
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827252"
---
# <a name="roomlists"></a><span data-ttu-id="f7bfa-103">RoomLists</span><span class="sxs-lookup"><span data-stu-id="f7bfa-103">RoomLists</span></span>

<span data-ttu-id="f7bfa-104">**RoomLists**元素是一个或多个地址表示的会议室列表的列表。</span><span class="sxs-lookup"><span data-stu-id="f7bfa-104">The **RoomLists** element is a list of one or more addresses that represent a list of meeting rooms.</span></span> 
  
[<span data-ttu-id="f7bfa-105">GetRoomListsResponse</span><span class="sxs-lookup"><span data-stu-id="f7bfa-105">GetRoomListsResponse</span></span>](getroomlistsresponse.md)
  
[<span data-ttu-id="f7bfa-106">RoomLists</span><span class="sxs-lookup"><span data-stu-id="f7bfa-106">RoomLists</span></span>](roomlists.md)
  
```xml
<RoomLists>   <Address/></RoomLists>
```

 <span data-ttu-id="f7bfa-107">**ArrayOfEmailAddressesType**</span><span class="sxs-lookup"><span data-stu-id="f7bfa-107">**ArrayOfEmailAddressesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f7bfa-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f7bfa-108">Attributes and elements</span></span>

<span data-ttu-id="f7bfa-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f7bfa-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f7bfa-110">属性</span><span class="sxs-lookup"><span data-stu-id="f7bfa-110">Attributes</span></span>

<span data-ttu-id="f7bfa-111">无。</span><span class="sxs-lookup"><span data-stu-id="f7bfa-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f7bfa-112">子元素</span><span class="sxs-lookup"><span data-stu-id="f7bfa-112">Child elements</span></span>

|<span data-ttu-id="f7bfa-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="f7bfa-113">**Element**</span></span>|<span data-ttu-id="f7bfa-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="f7bfa-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f7bfa-115">地址 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="f7bfa-115">Address (EmailAddressType)</span></span>](address-emailaddresstype.md) <br/> |<span data-ttu-id="f7bfa-116">定义电子邮件地址和表示聊天室列表的显示名称。</span><span class="sxs-lookup"><span data-stu-id="f7bfa-116">Defines the e-mail address and display name that represents the room list.</span></span> <span data-ttu-id="f7bfa-117">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="f7bfa-117">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f7bfa-118">父元素</span><span class="sxs-lookup"><span data-stu-id="f7bfa-118">Parent elements</span></span>

|<span data-ttu-id="f7bfa-119">**元素**</span><span class="sxs-lookup"><span data-stu-id="f7bfa-119">**Element**</span></span>|<span data-ttu-id="f7bfa-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="f7bfa-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f7bfa-121">GetRoomListsResponse</span><span class="sxs-lookup"><span data-stu-id="f7bfa-121">GetRoomListsResponse</span></span>](getroomlistsresponse.md) <br/> |<span data-ttu-id="f7bfa-122">包含状态和[GetRoomLists 操作](getroomlists-operation.md)请求的结果。</span><span class="sxs-lookup"><span data-stu-id="f7bfa-122">Contains the status and result of a [GetRoomLists operation](getroomlists-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f7bfa-123">备注</span><span class="sxs-lookup"><span data-stu-id="f7bfa-123">Remarks</span></span>

<span data-ttu-id="f7bfa-124">描述此元素的架构位于安装了客户端访问服务器角色与运行 Exchange Server 的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f7bfa-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f7bfa-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="f7bfa-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f7bfa-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="f7bfa-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f7bfa-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="f7bfa-127">Schema Name</span></span>  <br/> |<span data-ttu-id="f7bfa-128">消息架构</span><span class="sxs-lookup"><span data-stu-id="f7bfa-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f7bfa-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="f7bfa-129">Validation File</span></span>  <br/> |<span data-ttu-id="f7bfa-130">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f7bfa-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f7bfa-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="f7bfa-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="f7bfa-132">False</span><span class="sxs-lookup"><span data-stu-id="f7bfa-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f7bfa-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f7bfa-133">See also</span></span>



[<span data-ttu-id="f7bfa-134">GetRoomLists 操作</span><span class="sxs-lookup"><span data-stu-id="f7bfa-134">GetRoomLists operation</span></span>](getroomlists-operation.md)


- [<span data-ttu-id="f7bfa-135">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f7bfa-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

