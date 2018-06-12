---
title: ServerReplyWithMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ServerReplyWithMessage
api_type:
- schema
ms.assetid: 113c6ff2-9592-44f0-b542-54e4d5122ccb
description: ServerReplyWithMessage 元素指示是将作为答复传入邮件发送的模板邮件 ID。
ms.openlocfilehash: f2d927ae18ac68523d4cdd173f0474fbbeb36c98
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827390"
---
# <a name="serverreplywithmessage"></a><span data-ttu-id="3dd2c-103">ServerReplyWithMessage</span><span class="sxs-lookup"><span data-stu-id="3dd2c-103">ServerReplyWithMessage</span></span>

<span data-ttu-id="3dd2c-104">**ServerReplyWithMessage**元素指示是将作为答复传入邮件发送的模板邮件 ID。</span><span class="sxs-lookup"><span data-stu-id="3dd2c-104">The **ServerReplyWithMessage** element indicates the ID of the template message that is to be sent as a reply to incoming messages.</span></span> 
  
```XML
<ServerReplyWithMessage>
    <ItemId>
</ServerReplyWithMessage>
```

 <span data-ttu-id="3dd2c-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="3dd2c-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3dd2c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="3dd2c-106">Attributes and elements</span></span>

<span data-ttu-id="3dd2c-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3dd2c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3dd2c-108">属性</span><span class="sxs-lookup"><span data-stu-id="3dd2c-108">Attributes</span></span>

<span data-ttu-id="3dd2c-109">无。</span><span class="sxs-lookup"><span data-stu-id="3dd2c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3dd2c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="3dd2c-110">Child elements</span></span>

|<span data-ttu-id="3dd2c-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="3dd2c-111">**Element**</span></span>|<span data-ttu-id="3dd2c-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="3dd2c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3dd2c-113">ItemId</span><span class="sxs-lookup"><span data-stu-id="3dd2c-113">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="3dd2c-114">代表 Exchange 存储中的项的唯一标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="3dd2c-114">Represents the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3dd2c-115">父元素</span><span class="sxs-lookup"><span data-stu-id="3dd2c-115">Parent elements</span></span>

|<span data-ttu-id="3dd2c-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="3dd2c-116">**Element**</span></span>|<span data-ttu-id="3dd2c-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="3dd2c-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3dd2c-118">操作</span><span class="sxs-lookup"><span data-stu-id="3dd2c-118">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="3dd2c-119">表示可在满足条件时要采取对邮件的操作的集合。</span><span class="sxs-lookup"><span data-stu-id="3dd2c-119">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3dd2c-120">文本值</span><span class="sxs-lookup"><span data-stu-id="3dd2c-120">Text value</span></span>

<span data-ttu-id="3dd2c-121">无。</span><span class="sxs-lookup"><span data-stu-id="3dd2c-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3dd2c-122">备注</span><span class="sxs-lookup"><span data-stu-id="3dd2c-122">Remarks</span></span>

<span data-ttu-id="3dd2c-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="3dd2c-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3dd2c-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="3dd2c-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3dd2c-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="3dd2c-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3dd2c-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="3dd2c-126">Schema Name</span></span>  <br/> |<span data-ttu-id="3dd2c-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="3dd2c-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3dd2c-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="3dd2c-128">Validation File</span></span>  <br/> |<span data-ttu-id="3dd2c-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3dd2c-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3dd2c-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="3dd2c-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="3dd2c-131">True</span><span class="sxs-lookup"><span data-stu-id="3dd2c-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3dd2c-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3dd2c-132">See also</span></span>



- [<span data-ttu-id="3dd2c-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="3dd2c-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

