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
description: PhoneCallId 元素指定电话呼叫的标识符。 此元素是必需的。
ms.openlocfilehash: 3e4b9dba5e8be6e45a0c16508531fbc6cf91c170
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459698"
---
# <a name="phonecallid"></a><span data-ttu-id="561a4-104">PhoneCallId</span><span class="sxs-lookup"><span data-stu-id="561a4-104">PhoneCallId</span></span>

<span data-ttu-id="561a4-105">**PhoneCallId**元素指定电话呼叫的标识符。</span><span class="sxs-lookup"><span data-stu-id="561a4-105">The **PhoneCallId** element specifies the identifier of a phone call.</span></span> <span data-ttu-id="561a4-106">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="561a4-106">This element is required.</span></span> 
  
```xml
<PhoneCallId Id="" />
```

 <span data-ttu-id="561a4-107">**PhoneCallIdType**</span><span class="sxs-lookup"><span data-stu-id="561a4-107">**PhoneCallIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="561a4-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="561a4-108">Attributes and elements</span></span>

<span data-ttu-id="561a4-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="561a4-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="561a4-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="561a4-110">Attributes</span></span>

|<span data-ttu-id="561a4-111">**属性**</span><span class="sxs-lookup"><span data-stu-id="561a4-111">**Attribute**</span></span>|<span data-ttu-id="561a4-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="561a4-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="561a4-113">Id</span><span class="sxs-lookup"><span data-stu-id="561a4-113">Id</span></span>  <br/> |<span data-ttu-id="561a4-114">标识要断开连接的电话呼叫。</span><span class="sxs-lookup"><span data-stu-id="561a4-114">Identifies the phone call to disconnect.</span></span> <span data-ttu-id="561a4-115">此特性是必需的。</span><span class="sxs-lookup"><span data-stu-id="561a4-115">This attribute is required.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="561a4-116">子元素</span><span class="sxs-lookup"><span data-stu-id="561a4-116">Child elements</span></span>

<span data-ttu-id="561a4-117">无。</span><span class="sxs-lookup"><span data-stu-id="561a4-117">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="561a4-118">父元素</span><span class="sxs-lookup"><span data-stu-id="561a4-118">Parent elements</span></span>

|<span data-ttu-id="561a4-119">**元素**</span><span class="sxs-lookup"><span data-stu-id="561a4-119">**Element**</span></span>|<span data-ttu-id="561a4-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="561a4-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="561a4-121">DisconnectPhoneCall</span><span class="sxs-lookup"><span data-stu-id="561a4-121">DisconnectPhoneCall</span></span>](disconnectphonecall.md) <br/> |<span data-ttu-id="561a4-122">表示一个断开呼叫的请求。</span><span class="sxs-lookup"><span data-stu-id="561a4-122">Represents a request to disconnect a call.</span></span>  <br/> |
|[<span data-ttu-id="561a4-123">GetPhoneCallInformation</span><span class="sxs-lookup"><span data-stu-id="561a4-123">GetPhoneCallInformation</span></span>](getphonecallinformation.md) <br/> |<span data-ttu-id="561a4-124">表示获取电话呼叫信息的请求。</span><span class="sxs-lookup"><span data-stu-id="561a4-124">Represents a request to get telephone call information.</span></span>  <br/> |
|[<span data-ttu-id="561a4-125">PlayOnPhoneResponse （Exchange Web 服务）</span><span class="sxs-lookup"><span data-stu-id="561a4-125">PlayOnPhoneResponse (Exchange Web Services)</span></span>](playonphoneresponse-exchange-web-services.md) <br/> |<span data-ttu-id="561a4-126">定义对 PlayOnPhone 请求的响应。</span><span class="sxs-lookup"><span data-stu-id="561a4-126">Defines a response to a PlayOnPhone request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="561a4-127">备注</span><span class="sxs-lookup"><span data-stu-id="561a4-127">Remarks</span></span>

<span data-ttu-id="561a4-128">描述此元素的架构位于运行 Microsoft Exchange Server 2010 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="561a4-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="561a4-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="561a4-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="561a4-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="561a4-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="561a4-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="561a4-131">Schema Name</span></span>  <br/> |<span data-ttu-id="561a4-132">消息架构</span><span class="sxs-lookup"><span data-stu-id="561a4-132">Messages schema</span></span>  <br/> |
|<span data-ttu-id="561a4-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="561a4-133">Validation File</span></span>  <br/> |<span data-ttu-id="561a4-134">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="561a4-134">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="561a4-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="561a4-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="561a4-136">False</span><span class="sxs-lookup"><span data-stu-id="561a4-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="561a4-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="561a4-137">See also</span></span>



- [<span data-ttu-id="561a4-138">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="561a4-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

