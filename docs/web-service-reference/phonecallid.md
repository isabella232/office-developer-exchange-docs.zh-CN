---
title: PhoneCallId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PhoneCallId
api_type:
- schema
ms.assetid: 79e31a4c-fc84-4802-8761-470df8d63694
description: PhoneCallId 元素指定的电话呼叫的标识符。 此元素是必需的。
ms.openlocfilehash: 1886d9510fe254c016779166efccc9882fd77d2c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826757"
---
# <a name="phonecallid"></a><span data-ttu-id="a98cf-104">PhoneCallId</span><span class="sxs-lookup"><span data-stu-id="a98cf-104">PhoneCallId</span></span>

<span data-ttu-id="a98cf-105">**PhoneCallId**元素指定的电话呼叫的标识符。</span><span class="sxs-lookup"><span data-stu-id="a98cf-105">The **PhoneCallId** element specifies the identifier of a phone call.</span></span> <span data-ttu-id="a98cf-106">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="a98cf-106">This element is required.</span></span> 
  
```xml
<PhoneCallId Id="" />
```

 <span data-ttu-id="a98cf-107">**PhoneCallIdType**</span><span class="sxs-lookup"><span data-stu-id="a98cf-107">**PhoneCallIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a98cf-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a98cf-108">Attributes and elements</span></span>

<span data-ttu-id="a98cf-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a98cf-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a98cf-110">属性</span><span class="sxs-lookup"><span data-stu-id="a98cf-110">Attributes</span></span>

|<span data-ttu-id="a98cf-111">**属性**</span><span class="sxs-lookup"><span data-stu-id="a98cf-111">**Attribute**</span></span>|<span data-ttu-id="a98cf-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="a98cf-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a98cf-113">Id</span><span class="sxs-lookup"><span data-stu-id="a98cf-113">Id</span></span>  <br/> |<span data-ttu-id="a98cf-114">标识要断开电话呼叫。</span><span class="sxs-lookup"><span data-stu-id="a98cf-114">Identifies the phone call to disconnect.</span></span> <span data-ttu-id="a98cf-115">此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="a98cf-115">This attribute is required.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a98cf-116">子元素</span><span class="sxs-lookup"><span data-stu-id="a98cf-116">Child elements</span></span>

<span data-ttu-id="a98cf-117">无。</span><span class="sxs-lookup"><span data-stu-id="a98cf-117">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a98cf-118">父元素</span><span class="sxs-lookup"><span data-stu-id="a98cf-118">Parent elements</span></span>

|<span data-ttu-id="a98cf-119">**元素**</span><span class="sxs-lookup"><span data-stu-id="a98cf-119">**Element**</span></span>|<span data-ttu-id="a98cf-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="a98cf-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a98cf-121">DisconnectPhoneCall</span><span class="sxs-lookup"><span data-stu-id="a98cf-121">DisconnectPhoneCall</span></span>](disconnectphonecall.md) <br/> |<span data-ttu-id="a98cf-122">表示要断开呼叫的请求。</span><span class="sxs-lookup"><span data-stu-id="a98cf-122">Represents a request to disconnect a call.</span></span>  <br/> |
|[<span data-ttu-id="a98cf-123">GetPhoneCallInformation</span><span class="sxs-lookup"><span data-stu-id="a98cf-123">GetPhoneCallInformation</span></span>](getphonecallinformation.md) <br/> |<span data-ttu-id="a98cf-124">表示要获取电话呼叫的信息的请求。</span><span class="sxs-lookup"><span data-stu-id="a98cf-124">Represents a request to get telephone call information.</span></span>  <br/> |
|[<span data-ttu-id="a98cf-125">PlayOnPhoneResponse （Exchange Web 服务）</span><span class="sxs-lookup"><span data-stu-id="a98cf-125">PlayOnPhoneResponse (Exchange Web Services)</span></span>](playonphoneresponse-exchange-web-services.md) <br/> |<span data-ttu-id="a98cf-126">定义 PlayOnPhone 请求的响应。</span><span class="sxs-lookup"><span data-stu-id="a98cf-126">Defines a response to a PlayOnPhone request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a98cf-127">注解</span><span class="sxs-lookup"><span data-stu-id="a98cf-127">Remarks</span></span>

<span data-ttu-id="a98cf-128">描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a98cf-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a98cf-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="a98cf-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a98cf-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="a98cf-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a98cf-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="a98cf-131">Schema Name</span></span>  <br/> |<span data-ttu-id="a98cf-132">消息架构</span><span class="sxs-lookup"><span data-stu-id="a98cf-132">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a98cf-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="a98cf-133">Validation File</span></span>  <br/> |<span data-ttu-id="a98cf-134">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a98cf-134">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a98cf-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="a98cf-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="a98cf-136">False</span><span class="sxs-lookup"><span data-stu-id="a98cf-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a98cf-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a98cf-137">See also</span></span>



- [<span data-ttu-id="a98cf-138">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a98cf-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

