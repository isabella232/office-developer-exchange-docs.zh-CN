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
description: DisconnectPhoneCall 元素表示一个断开呼叫的请求。
ms.openlocfilehash: 8d64ecb9dce1d8b7efcebc70686db8fcbf867217
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529705"
---
# <a name="disconnectphonecall"></a><span data-ttu-id="82ef9-103">DisconnectPhoneCall</span><span class="sxs-lookup"><span data-stu-id="82ef9-103">DisconnectPhoneCall</span></span>

<span data-ttu-id="82ef9-104">**DisconnectPhoneCall**元素表示一个断开呼叫的请求。</span><span class="sxs-lookup"><span data-stu-id="82ef9-104">The **DisconnectPhoneCall** element represents a request to disconnect a call.</span></span> 
  
```xml
<DisconnectPhoneCall>
   <PhoneCallId/>
</DisconnectPhoneCall>
```

 <span data-ttu-id="82ef9-105">**DisconnectPhoneCallType**</span><span class="sxs-lookup"><span data-stu-id="82ef9-105">**DisconnectPhoneCallType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="82ef9-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="82ef9-106">Attributes and elements</span></span>

<span data-ttu-id="82ef9-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="82ef9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="82ef9-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="82ef9-108">Attributes</span></span>

<span data-ttu-id="82ef9-109">无。</span><span class="sxs-lookup"><span data-stu-id="82ef9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="82ef9-110">子元素</span><span class="sxs-lookup"><span data-stu-id="82ef9-110">Child elements</span></span>

|<span data-ttu-id="82ef9-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="82ef9-111">**Element**</span></span>|<span data-ttu-id="82ef9-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="82ef9-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="82ef9-113">PhoneCallId</span><span class="sxs-lookup"><span data-stu-id="82ef9-113">PhoneCallId</span></span>](phonecallid.md) <br/> |<span data-ttu-id="82ef9-114">指定要断开连接的呼叫的标识符。</span><span class="sxs-lookup"><span data-stu-id="82ef9-114">Specifies the identifier of the call to disconnect.</span></span> <span data-ttu-id="82ef9-115">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="82ef9-115">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="82ef9-116">父元素</span><span class="sxs-lookup"><span data-stu-id="82ef9-116">Parent elements</span></span>

<span data-ttu-id="82ef9-117">无。</span><span class="sxs-lookup"><span data-stu-id="82ef9-117">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="82ef9-118">文本值</span><span class="sxs-lookup"><span data-stu-id="82ef9-118">Text value</span></span>

<span data-ttu-id="82ef9-119">无。</span><span class="sxs-lookup"><span data-stu-id="82ef9-119">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="82ef9-120">说明</span><span class="sxs-lookup"><span data-stu-id="82ef9-120">Remarks</span></span>

<span data-ttu-id="82ef9-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="82ef9-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="82ef9-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="82ef9-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="82ef9-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="82ef9-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="82ef9-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="82ef9-124">Schema Name</span></span>  <br/> |<span data-ttu-id="82ef9-125">消息架构</span><span class="sxs-lookup"><span data-stu-id="82ef9-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="82ef9-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="82ef9-126">Validation File</span></span>  <br/> |<span data-ttu-id="82ef9-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="82ef9-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="82ef9-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="82ef9-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="82ef9-129">False</span><span class="sxs-lookup"><span data-stu-id="82ef9-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="82ef9-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="82ef9-130">See also</span></span>

- [<span data-ttu-id="82ef9-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="82ef9-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

