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
description: SendNotification 元素包含运行 Microsoft Exchange Server 2007 的计算机发送给客户端应用程序的推送通知。
ms.openlocfilehash: 49f2f6cb7f5c8e1171b54ff965ee1d22accc9bf2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462113"
---
# <a name="sendnotification"></a><span data-ttu-id="f5cf1-103">SendNotification</span><span class="sxs-lookup"><span data-stu-id="f5cf1-103">SendNotification</span></span>

<span data-ttu-id="f5cf1-104">**SendNotification**元素包含运行 Microsoft Exchange Server 2007 的计算机发送给客户端应用程序的推送通知。</span><span class="sxs-lookup"><span data-stu-id="f5cf1-104">The **SendNotification** element contains the push notifications that are sent by the computer that is running Microsoft Exchange Server 2007 to the client application.</span></span> 
  
```xml
<SendNotification>
   <ResponseMessages/>
</SendNotification>
```

 <span data-ttu-id="f5cf1-105">**SendNotificationResponseType**</span><span class="sxs-lookup"><span data-stu-id="f5cf1-105">**SendNotificationResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f5cf1-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f5cf1-106">Attributes and elements</span></span>

<span data-ttu-id="f5cf1-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f5cf1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f5cf1-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="f5cf1-108">Attributes</span></span>

<span data-ttu-id="f5cf1-109">无。</span><span class="sxs-lookup"><span data-stu-id="f5cf1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f5cf1-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f5cf1-110">Child elements</span></span>

|<span data-ttu-id="f5cf1-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="f5cf1-111">**Element**</span></span>|<span data-ttu-id="f5cf1-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="f5cf1-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f5cf1-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="f5cf1-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="f5cf1-114">包含客户端访问服务器发送的推送通知。</span><span class="sxs-lookup"><span data-stu-id="f5cf1-114">Contains the push notifications that are sent by the Client Access server.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f5cf1-115">父元素</span><span class="sxs-lookup"><span data-stu-id="f5cf1-115">Parent elements</span></span>

<span data-ttu-id="f5cf1-116">无。</span><span class="sxs-lookup"><span data-stu-id="f5cf1-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f5cf1-117">说明</span><span class="sxs-lookup"><span data-stu-id="f5cf1-117">Remarks</span></span>

<span data-ttu-id="f5cf1-118">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f5cf1-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f5cf1-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="f5cf1-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f5cf1-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="f5cf1-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f5cf1-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="f5cf1-121">Schema Name</span></span>  <br/> |<span data-ttu-id="f5cf1-122">消息架构</span><span class="sxs-lookup"><span data-stu-id="f5cf1-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f5cf1-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="f5cf1-123">Validation File</span></span>  <br/> |<span data-ttu-id="f5cf1-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f5cf1-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f5cf1-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="f5cf1-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="f5cf1-126">False</span><span class="sxs-lookup"><span data-stu-id="f5cf1-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f5cf1-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f5cf1-127">See also</span></span>



- [<span data-ttu-id="f5cf1-128">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f5cf1-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="f5cf1-129">EWS 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="f5cf1-129">Event notifications in EWS</span></span>](https://msdn.microsoft.com/library/4fd4b351-d35c-4ccc-9ed9-878932ab9d50%28Office.15%29.aspx)
  
[<span data-ttu-id="f5cf1-130">推送通知示例应用程序</span><span class="sxs-lookup"><span data-stu-id="f5cf1-130">Push Notification Sample Application</span></span>](https://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx)

