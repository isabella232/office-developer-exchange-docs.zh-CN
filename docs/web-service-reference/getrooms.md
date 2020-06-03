---
title: GetRooms
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetRooms
api_type:
- schema
ms.assetid: 82a737c7-da41-4777-8ad8-89851a0b602b
description: GetRooms 元素是请求中的根元素，用于获取特定会议室列表中的聊天室列表。
ms.openlocfilehash: 77fde5980a03d4c0509344933b0901cb21ab7197
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458591"
---
# <a name="getrooms"></a><span data-ttu-id="d04d0-103">GetRooms</span><span class="sxs-lookup"><span data-stu-id="d04d0-103">GetRooms</span></span>

<span data-ttu-id="d04d0-104">**GetRooms**元素是请求中的根元素，用于获取特定会议室列表中的聊天室列表。</span><span class="sxs-lookup"><span data-stu-id="d04d0-104">The **GetRooms** element is the root element in a request to get a list of rooms within a particular room list.</span></span> 
  
```XML
<GetRooms>
   <RoomList/>
</GetRooms>
```

 <span data-ttu-id="d04d0-105">**GetRoomsType**</span><span class="sxs-lookup"><span data-stu-id="d04d0-105">**GetRoomsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d04d0-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d04d0-106">Attributes and elements</span></span>

<span data-ttu-id="d04d0-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d04d0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d04d0-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="d04d0-108">Attributes</span></span>

<span data-ttu-id="d04d0-109">无。</span><span class="sxs-lookup"><span data-stu-id="d04d0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d04d0-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d04d0-110">Child elements</span></span>

|<span data-ttu-id="d04d0-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="d04d0-111">**Element**</span></span>|<span data-ttu-id="d04d0-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="d04d0-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d04d0-113">RoomList</span><span class="sxs-lookup"><span data-stu-id="d04d0-113">RoomList</span></span>](roomlist.md) <br/> |<span data-ttu-id="d04d0-114">代表标识会议室列表的电子邮件地址</span><span class="sxs-lookup"><span data-stu-id="d04d0-114">Represents an e-mail address that identifies a list of meeting rooms</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d04d0-115">父元素</span><span class="sxs-lookup"><span data-stu-id="d04d0-115">Parent elements</span></span>

<span data-ttu-id="d04d0-116">无。</span><span class="sxs-lookup"><span data-stu-id="d04d0-116">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="d04d0-117">文本值</span><span class="sxs-lookup"><span data-stu-id="d04d0-117">Text value</span></span>

<span data-ttu-id="d04d0-118">无。</span><span class="sxs-lookup"><span data-stu-id="d04d0-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d04d0-119">说明</span><span class="sxs-lookup"><span data-stu-id="d04d0-119">Remarks</span></span>

<span data-ttu-id="d04d0-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d04d0-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d04d0-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="d04d0-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d04d0-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="d04d0-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d04d0-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="d04d0-123">Schema Name</span></span>  <br/> |<span data-ttu-id="d04d0-124">消息架构</span><span class="sxs-lookup"><span data-stu-id="d04d0-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d04d0-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="d04d0-125">Validation File</span></span>  <br/> |<span data-ttu-id="d04d0-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d04d0-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d04d0-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="d04d0-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="d04d0-128">False</span><span class="sxs-lookup"><span data-stu-id="d04d0-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d04d0-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d04d0-129">See also</span></span>



- [<span data-ttu-id="d04d0-130">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d04d0-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

