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
description: RoomLists 元素是表示会议室列表的一个或多个地址的列表。
ms.openlocfilehash: 8f6393b617331e5878e48113c94ca3546cba095e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459046"
---
# <a name="roomlists"></a><span data-ttu-id="15731-103">RoomLists</span><span class="sxs-lookup"><span data-stu-id="15731-103">RoomLists</span></span>

<span data-ttu-id="15731-104">**RoomLists**元素是表示会议室列表的一个或多个地址的列表。</span><span class="sxs-lookup"><span data-stu-id="15731-104">The **RoomLists** element is a list of one or more addresses that represent a list of meeting rooms.</span></span> 
  
[<span data-ttu-id="15731-105">GetRoomListsResponse</span><span class="sxs-lookup"><span data-stu-id="15731-105">GetRoomListsResponse</span></span>](getroomlistsresponse.md)
  
[<span data-ttu-id="15731-106">RoomLists</span><span class="sxs-lookup"><span data-stu-id="15731-106">RoomLists</span></span>](roomlists.md)
  
```xml
<RoomLists>   <Address/></RoomLists>
```

 <span data-ttu-id="15731-107">**ArrayOfEmailAddressesType**</span><span class="sxs-lookup"><span data-stu-id="15731-107">**ArrayOfEmailAddressesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="15731-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="15731-108">Attributes and elements</span></span>

<span data-ttu-id="15731-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="15731-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="15731-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="15731-110">Attributes</span></span>

<span data-ttu-id="15731-111">无。</span><span class="sxs-lookup"><span data-stu-id="15731-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="15731-112">子元素</span><span class="sxs-lookup"><span data-stu-id="15731-112">Child elements</span></span>

|<span data-ttu-id="15731-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="15731-113">**Element**</span></span>|<span data-ttu-id="15731-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="15731-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="15731-115">地址 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="15731-115">Address (EmailAddressType)</span></span>](address-emailaddresstype.md) <br/> |<span data-ttu-id="15731-116">定义表示会议室列表的电子邮件地址和显示名称。</span><span class="sxs-lookup"><span data-stu-id="15731-116">Defines the e-mail address and display name that represents the room list.</span></span> <span data-ttu-id="15731-117">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="15731-117">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="15731-118">父元素</span><span class="sxs-lookup"><span data-stu-id="15731-118">Parent elements</span></span>

|<span data-ttu-id="15731-119">**元素**</span><span class="sxs-lookup"><span data-stu-id="15731-119">**Element**</span></span>|<span data-ttu-id="15731-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="15731-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="15731-121">GetRoomListsResponse</span><span class="sxs-lookup"><span data-stu-id="15731-121">GetRoomListsResponse</span></span>](getroomlistsresponse.md) <br/> |<span data-ttu-id="15731-122">包含[GetRoomLists 操作](getroomlists-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="15731-122">Contains the status and result of a [GetRoomLists operation](getroomlists-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="15731-123">备注</span><span class="sxs-lookup"><span data-stu-id="15731-123">Remarks</span></span>

<span data-ttu-id="15731-124">描述此元素的架构位于运行 Exchange Server 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="15731-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="15731-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="15731-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="15731-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="15731-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="15731-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="15731-127">Schema Name</span></span>  <br/> |<span data-ttu-id="15731-128">消息架构</span><span class="sxs-lookup"><span data-stu-id="15731-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="15731-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="15731-129">Validation File</span></span>  <br/> |<span data-ttu-id="15731-130">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="15731-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="15731-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="15731-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="15731-132">False</span><span class="sxs-lookup"><span data-stu-id="15731-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="15731-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="15731-133">See also</span></span>



[<span data-ttu-id="15731-134">GetRoomLists 操作</span><span class="sxs-lookup"><span data-stu-id="15731-134">GetRoomLists operation</span></span>](getroomlists-operation.md)


- [<span data-ttu-id="15731-135">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="15731-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

