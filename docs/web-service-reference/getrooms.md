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
description: GetRooms 元素是请求以获取特定的房间列表中的聊天室的列表中的根元素。
ms.openlocfilehash: a787097752cfeee9489e5f118549c2d939ba4c9a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754677"
---
# <a name="getrooms"></a><span data-ttu-id="0c844-103">GetRooms</span><span class="sxs-lookup"><span data-stu-id="0c844-103">GetRooms</span></span>

<span data-ttu-id="0c844-104">**GetRooms**元素是请求以获取特定的房间列表中的聊天室的列表中的根元素。</span><span class="sxs-lookup"><span data-stu-id="0c844-104">The **GetRooms** element is the root element in a request to get a list of rooms within a particular room list.</span></span> 
  
```XML
<GetRooms>
   <RoomList/>
</GetRooms>
```

 <span data-ttu-id="0c844-105">**GetRoomsType**</span><span class="sxs-lookup"><span data-stu-id="0c844-105">**GetRoomsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0c844-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0c844-106">Attributes and elements</span></span>

<span data-ttu-id="0c844-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0c844-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0c844-108">属性</span><span class="sxs-lookup"><span data-stu-id="0c844-108">Attributes</span></span>

<span data-ttu-id="0c844-109">无。</span><span class="sxs-lookup"><span data-stu-id="0c844-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0c844-110">子元素</span><span class="sxs-lookup"><span data-stu-id="0c844-110">Child elements</span></span>

|<span data-ttu-id="0c844-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="0c844-111">**Element**</span></span>|<span data-ttu-id="0c844-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="0c844-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0c844-113">RoomList</span><span class="sxs-lookup"><span data-stu-id="0c844-113">RoomList</span></span>](roomlist.md) <br/> |<span data-ttu-id="0c844-114">代表电子邮件地址的标识的会议室列表</span><span class="sxs-lookup"><span data-stu-id="0c844-114">Represents an e-mail address that identifies a list of meeting rooms</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0c844-115">父元素</span><span class="sxs-lookup"><span data-stu-id="0c844-115">Parent elements</span></span>

<span data-ttu-id="0c844-116">无。</span><span class="sxs-lookup"><span data-stu-id="0c844-116">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="0c844-117">文本值</span><span class="sxs-lookup"><span data-stu-id="0c844-117">Text value</span></span>

<span data-ttu-id="0c844-118">无。</span><span class="sxs-lookup"><span data-stu-id="0c844-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0c844-119">备注</span><span class="sxs-lookup"><span data-stu-id="0c844-119">Remarks</span></span>

<span data-ttu-id="0c844-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="0c844-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0c844-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="0c844-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0c844-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="0c844-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0c844-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="0c844-123">Schema Name</span></span>  <br/> |<span data-ttu-id="0c844-124">消息架构</span><span class="sxs-lookup"><span data-stu-id="0c844-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0c844-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="0c844-125">Validation File</span></span>  <br/> |<span data-ttu-id="0c844-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0c844-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0c844-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="0c844-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="0c844-128">False</span><span class="sxs-lookup"><span data-stu-id="0c844-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0c844-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0c844-129">See also</span></span>



- [<span data-ttu-id="0c844-130">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="0c844-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

