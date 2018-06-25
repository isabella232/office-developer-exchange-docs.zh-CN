---
title: DisconnectPhoneCall
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DisconnectPhoneCall
api_type:
- schema
ms.assetid: f9252536-9852-4dd9-9ebc-91f5cf281171
description: DisconnectPhoneCall 元素均表示一个要断开呼叫的请求。
ms.openlocfilehash: 56947ea9ba56c76bb02d6a425ff43b3b846a2f60
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753905"
---
# <a name="disconnectphonecall"></a><span data-ttu-id="5fda6-103">DisconnectPhoneCall</span><span class="sxs-lookup"><span data-stu-id="5fda6-103">DisconnectPhoneCall</span></span>

<span data-ttu-id="5fda6-104">**DisconnectPhoneCall**元素均表示一个要断开呼叫的请求。</span><span class="sxs-lookup"><span data-stu-id="5fda6-104">The **DisconnectPhoneCall** element represents a request to disconnect a call.</span></span> 
  
```xml
<DisconnectPhoneCall>
   <PhoneCallId/>
</DisconnectPhoneCall>
```

 <span data-ttu-id="5fda6-105">**DisconnectPhoneCallType**</span><span class="sxs-lookup"><span data-stu-id="5fda6-105">**DisconnectPhoneCallType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5fda6-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5fda6-106">Attributes and elements</span></span>

<span data-ttu-id="5fda6-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5fda6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5fda6-108">属性</span><span class="sxs-lookup"><span data-stu-id="5fda6-108">Attributes</span></span>

<span data-ttu-id="5fda6-109">无。</span><span class="sxs-lookup"><span data-stu-id="5fda6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5fda6-110">子元素</span><span class="sxs-lookup"><span data-stu-id="5fda6-110">Child elements</span></span>

|<span data-ttu-id="5fda6-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="5fda6-111">**Element**</span></span>|<span data-ttu-id="5fda6-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="5fda6-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5fda6-113">PhoneCallId</span><span class="sxs-lookup"><span data-stu-id="5fda6-113">PhoneCallId</span></span>](phonecallid.md) <br/> |<span data-ttu-id="5fda6-114">指定呼叫断开连接的标识符。</span><span class="sxs-lookup"><span data-stu-id="5fda6-114">Specifies the identifier of the call to disconnect.</span></span> <span data-ttu-id="5fda6-115">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="5fda6-115">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5fda6-116">父元素</span><span class="sxs-lookup"><span data-stu-id="5fda6-116">Parent elements</span></span>

<span data-ttu-id="5fda6-117">无。</span><span class="sxs-lookup"><span data-stu-id="5fda6-117">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="5fda6-118">文本值</span><span class="sxs-lookup"><span data-stu-id="5fda6-118">Text value</span></span>

<span data-ttu-id="5fda6-119">无。</span><span class="sxs-lookup"><span data-stu-id="5fda6-119">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5fda6-120">备注</span><span class="sxs-lookup"><span data-stu-id="5fda6-120">Remarks</span></span>

<span data-ttu-id="5fda6-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="5fda6-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5fda6-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="5fda6-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5fda6-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="5fda6-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5fda6-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="5fda6-124">Schema Name</span></span>  <br/> |<span data-ttu-id="5fda6-125">消息架构</span><span class="sxs-lookup"><span data-stu-id="5fda6-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="5fda6-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="5fda6-126">Validation File</span></span>  <br/> |<span data-ttu-id="5fda6-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="5fda6-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5fda6-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="5fda6-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="5fda6-129">False</span><span class="sxs-lookup"><span data-stu-id="5fda6-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5fda6-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5fda6-130">See also</span></span>

- [<span data-ttu-id="5fda6-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="5fda6-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

