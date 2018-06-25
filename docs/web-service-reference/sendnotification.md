---
title: SendNotification
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SendNotification
api_type:
- schema
ms.assetid: e45c4451-a286-4aec-a691-119ec41c58e0
description: SendNotification 元素包含由客户端应用程序运行 Microsoft Exchange Server 2007 的计算机发送推送通知。
ms.openlocfilehash: 2288dbb5cf97b57a64b3c645eb72836342f4c178
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827345"
---
# <a name="sendnotification"></a><span data-ttu-id="82f81-103">SendNotification</span><span class="sxs-lookup"><span data-stu-id="82f81-103">SendNotification</span></span>

<span data-ttu-id="82f81-104">**SendNotification**元素包含由客户端应用程序运行 Microsoft Exchange Server 2007 的计算机发送推送通知。</span><span class="sxs-lookup"><span data-stu-id="82f81-104">The **SendNotification** element contains the push notifications that are sent by the computer that is running Microsoft Exchange Server 2007 to the client application.</span></span> 
  
```xml
<SendNotification>
   <ResponseMessages/>
</SendNotification>
```

 <span data-ttu-id="82f81-105">**SendNotificationResponseType**</span><span class="sxs-lookup"><span data-stu-id="82f81-105">**SendNotificationResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="82f81-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="82f81-106">Attributes and elements</span></span>

<span data-ttu-id="82f81-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="82f81-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="82f81-108">属性</span><span class="sxs-lookup"><span data-stu-id="82f81-108">Attributes</span></span>

<span data-ttu-id="82f81-109">无。</span><span class="sxs-lookup"><span data-stu-id="82f81-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="82f81-110">子元素</span><span class="sxs-lookup"><span data-stu-id="82f81-110">Child elements</span></span>

|<span data-ttu-id="82f81-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="82f81-111">**Element**</span></span>|<span data-ttu-id="82f81-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="82f81-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="82f81-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="82f81-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="82f81-114">包含由客户端访问服务器发送的推送通知。</span><span class="sxs-lookup"><span data-stu-id="82f81-114">Contains the push notifications that are sent by the Client Access server.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="82f81-115">父元素</span><span class="sxs-lookup"><span data-stu-id="82f81-115">Parent elements</span></span>

<span data-ttu-id="82f81-116">无。</span><span class="sxs-lookup"><span data-stu-id="82f81-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="82f81-117">备注</span><span class="sxs-lookup"><span data-stu-id="82f81-117">Remarks</span></span>

<span data-ttu-id="82f81-118">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="82f81-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="82f81-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="82f81-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="82f81-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="82f81-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="82f81-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="82f81-121">Schema Name</span></span>  <br/> |<span data-ttu-id="82f81-122">消息架构</span><span class="sxs-lookup"><span data-stu-id="82f81-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="82f81-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="82f81-123">Validation File</span></span>  <br/> |<span data-ttu-id="82f81-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="82f81-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="82f81-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="82f81-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="82f81-126">False</span><span class="sxs-lookup"><span data-stu-id="82f81-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="82f81-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="82f81-127">See also</span></span>



- [<span data-ttu-id="82f81-128">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="82f81-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="82f81-129">EWS 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="82f81-129">Event notifications in EWS</span></span>](http://msdn.microsoft.com/library/4fd4b351-d35c-4ccc-9ed9-878932ab9d50%28Office.15%29.aspx)
  
[<span data-ttu-id="82f81-130">推送通知示例应用程序</span><span class="sxs-lookup"><span data-stu-id="82f81-130">Push Notification Sample Application</span></span>](http://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx)

