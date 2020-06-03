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
description: PhoneCallInformation 元素指定电话呼叫的状态信息。
ms.openlocfilehash: 75370bccb841818a8302bdd055ad96fd16b2e8df
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468843"
---
# <a name="phonecallinformation"></a><span data-ttu-id="0a230-103">PhoneCallInformation</span><span class="sxs-lookup"><span data-stu-id="0a230-103">PhoneCallInformation</span></span>

<span data-ttu-id="0a230-104">**PhoneCallInformation**元素指定电话呼叫的状态信息。</span><span class="sxs-lookup"><span data-stu-id="0a230-104">The **PhoneCallInformation** element specifies the state information for a phone call.</span></span> 
  
```XML
<PhoneCallInformation>
   <PhoneCallState/>
   <ConnectionFailureCause/>
   <SIPResponseText/>
   <SIPResponseCode/>
</PhoneCallInformation>
```

 <span data-ttu-id="0a230-105">**PhoneCallInformationType**</span><span class="sxs-lookup"><span data-stu-id="0a230-105">**PhoneCallInformationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0a230-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0a230-106">Attributes and elements</span></span>

<span data-ttu-id="0a230-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0a230-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0a230-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="0a230-108">Attributes</span></span>

<span data-ttu-id="0a230-109">无。</span><span class="sxs-lookup"><span data-stu-id="0a230-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0a230-110">子元素</span><span class="sxs-lookup"><span data-stu-id="0a230-110">Child elements</span></span>

|<span data-ttu-id="0a230-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="0a230-111">**Element**</span></span>|<span data-ttu-id="0a230-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="0a230-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0a230-113">PhoneCallState</span><span class="sxs-lookup"><span data-stu-id="0a230-113">PhoneCallState</span></span>](phonecallstate.md) <br/> |<span data-ttu-id="0a230-114">指定电话呼叫的状态。</span><span class="sxs-lookup"><span data-stu-id="0a230-114">Specifies the state for a phone call.</span></span> <span data-ttu-id="0a230-115">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="0a230-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="0a230-116">ConnectionFailureCause</span><span class="sxs-lookup"><span data-stu-id="0a230-116">ConnectionFailureCause</span></span>](connectionfailurecause.md) <br/> |<span data-ttu-id="0a230-117">指定连接失败的原因。</span><span class="sxs-lookup"><span data-stu-id="0a230-117">Specifies the cause of a connection failure.</span></span> <span data-ttu-id="0a230-118">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="0a230-118">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="0a230-119">SIPResponseText</span><span class="sxs-lookup"><span data-stu-id="0a230-119">SIPResponseText</span></span>](sipresponsetext.md) <br/> |<span data-ttu-id="0a230-120">指定 SIP 响应文本。</span><span class="sxs-lookup"><span data-stu-id="0a230-120">Specifies the SIP response text.</span></span> <span data-ttu-id="0a230-121">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="0a230-121">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="0a230-122">SIPResponseCode</span><span class="sxs-lookup"><span data-stu-id="0a230-122">SIPResponseCode</span></span>](sipresponsecode.md) <br/> |<span data-ttu-id="0a230-123">指定 SIP 响应代码。</span><span class="sxs-lookup"><span data-stu-id="0a230-123">Specifies the SIP response code.</span></span> <span data-ttu-id="0a230-124">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="0a230-124">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0a230-125">父元素</span><span class="sxs-lookup"><span data-stu-id="0a230-125">Parent elements</span></span>

|<span data-ttu-id="0a230-126">**元素**</span><span class="sxs-lookup"><span data-stu-id="0a230-126">**Element**</span></span>|<span data-ttu-id="0a230-127">**说明**</span><span class="sxs-lookup"><span data-stu-id="0a230-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0a230-128">GetPhoneCallInformationResponse</span><span class="sxs-lookup"><span data-stu-id="0a230-128">GetPhoneCallInformationResponse</span></span>](getphonecallinformationresponse.md) <br/> |<span data-ttu-id="0a230-129">定义对[GetPhoneCallInformation 操作](getphonecallinformation-operation.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="0a230-129">Defines a response to a [GetPhoneCallInformation operation](getphonecallinformation-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0a230-130">说明</span><span class="sxs-lookup"><span data-stu-id="0a230-130">Remarks</span></span>

<span data-ttu-id="0a230-131">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="0a230-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0a230-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="0a230-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0a230-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="0a230-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0a230-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="0a230-134">Schema Name</span></span>  <br/> |<span data-ttu-id="0a230-135">消息架构</span><span class="sxs-lookup"><span data-stu-id="0a230-135">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0a230-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="0a230-136">Validation File</span></span>  <br/> |<span data-ttu-id="0a230-137">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0a230-137">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0a230-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="0a230-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="0a230-139">False</span><span class="sxs-lookup"><span data-stu-id="0a230-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0a230-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0a230-140">See also</span></span>



- [<span data-ttu-id="0a230-141">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="0a230-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

