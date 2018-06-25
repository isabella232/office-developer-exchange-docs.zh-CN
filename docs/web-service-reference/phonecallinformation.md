---
title: PhoneCallInformation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PhoneCallInformation
api_type:
- schema
ms.assetid: a0363c42-6d35-4074-bc17-946eb12736ff
description: PhoneCallInformation 元素指定的电话呼叫的状态信息。
ms.openlocfilehash: e64e7b38b3801c60df8a966e95d980746533d3a4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826758"
---
# <a name="phonecallinformation"></a><span data-ttu-id="65aab-103">PhoneCallInformation</span><span class="sxs-lookup"><span data-stu-id="65aab-103">PhoneCallInformation</span></span>

<span data-ttu-id="65aab-104">**PhoneCallInformation**元素指定的电话呼叫的状态信息。</span><span class="sxs-lookup"><span data-stu-id="65aab-104">The **PhoneCallInformation** element specifies the state information for a phone call.</span></span> 
  
```XML
<PhoneCallInformation>
   <PhoneCallState/>
   <ConnectionFailureCause/>
   <SIPResponseText/>
   <SIPResponseCode/>
</PhoneCallInformation>
```

 <span data-ttu-id="65aab-105">**PhoneCallInformationType**</span><span class="sxs-lookup"><span data-stu-id="65aab-105">**PhoneCallInformationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="65aab-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="65aab-106">Attributes and elements</span></span>

<span data-ttu-id="65aab-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="65aab-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="65aab-108">属性</span><span class="sxs-lookup"><span data-stu-id="65aab-108">Attributes</span></span>

<span data-ttu-id="65aab-109">无。</span><span class="sxs-lookup"><span data-stu-id="65aab-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="65aab-110">子元素</span><span class="sxs-lookup"><span data-stu-id="65aab-110">Child elements</span></span>

|<span data-ttu-id="65aab-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="65aab-111">**Element**</span></span>|<span data-ttu-id="65aab-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="65aab-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="65aab-113">PhoneCallState</span><span class="sxs-lookup"><span data-stu-id="65aab-113">PhoneCallState</span></span>](phonecallstate.md) <br/> |<span data-ttu-id="65aab-114">指定的电话的状态。</span><span class="sxs-lookup"><span data-stu-id="65aab-114">Specifies the state for a phone call.</span></span> <span data-ttu-id="65aab-115">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="65aab-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="65aab-116">ConnectionFailureCause</span><span class="sxs-lookup"><span data-stu-id="65aab-116">ConnectionFailureCause</span></span>](connectionfailurecause.md) <br/> |<span data-ttu-id="65aab-117">指定连接失败的原因。</span><span class="sxs-lookup"><span data-stu-id="65aab-117">Specifies the cause of a connection failure.</span></span> <span data-ttu-id="65aab-118">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="65aab-118">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="65aab-119">SIPResponseText</span><span class="sxs-lookup"><span data-stu-id="65aab-119">SIPResponseText</span></span>](sipresponsetext.md) <br/> |<span data-ttu-id="65aab-120">指定的 SIP 响应文本。</span><span class="sxs-lookup"><span data-stu-id="65aab-120">Specifies the SIP response text.</span></span> <span data-ttu-id="65aab-121">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="65aab-121">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="65aab-122">SIPResponseCode</span><span class="sxs-lookup"><span data-stu-id="65aab-122">SIPResponseCode</span></span>](sipresponsecode.md) <br/> |<span data-ttu-id="65aab-123">指定的 SIP 响应代码。</span><span class="sxs-lookup"><span data-stu-id="65aab-123">Specifies the SIP response code.</span></span> <span data-ttu-id="65aab-124">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="65aab-124">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="65aab-125">父元素</span><span class="sxs-lookup"><span data-stu-id="65aab-125">Parent elements</span></span>

|<span data-ttu-id="65aab-126">**元素**</span><span class="sxs-lookup"><span data-stu-id="65aab-126">**Element**</span></span>|<span data-ttu-id="65aab-127">**说明**</span><span class="sxs-lookup"><span data-stu-id="65aab-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="65aab-128">GetPhoneCallInformationResponse</span><span class="sxs-lookup"><span data-stu-id="65aab-128">GetPhoneCallInformationResponse</span></span>](getphonecallinformationresponse.md) <br/> |<span data-ttu-id="65aab-129">定义[GetPhoneCallInformation 操作](getphonecallinformation-operation.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="65aab-129">Defines a response to a [GetPhoneCallInformation operation](getphonecallinformation-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="65aab-130">备注</span><span class="sxs-lookup"><span data-stu-id="65aab-130">Remarks</span></span>

<span data-ttu-id="65aab-131">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="65aab-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="65aab-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="65aab-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="65aab-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="65aab-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="65aab-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="65aab-134">Schema Name</span></span>  <br/> |<span data-ttu-id="65aab-135">消息架构</span><span class="sxs-lookup"><span data-stu-id="65aab-135">Messages schema</span></span>  <br/> |
|<span data-ttu-id="65aab-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="65aab-136">Validation File</span></span>  <br/> |<span data-ttu-id="65aab-137">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="65aab-137">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="65aab-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="65aab-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="65aab-139">False</span><span class="sxs-lookup"><span data-stu-id="65aab-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="65aab-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="65aab-140">See also</span></span>



- [<span data-ttu-id="65aab-141">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="65aab-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

