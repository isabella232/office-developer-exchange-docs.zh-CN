---
title: GetPhoneCallInformation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetPhoneCallInformation
api_type:
- schema
ms.assetid: 5f4ee71c-bde0-4b0d-b426-0c24dfe67585
description: GetPhoneCallInformation 元素指定获取电话呼叫信息的请求。
ms.openlocfilehash: b835cd301b1c243e88034d1057026ef1305b9038
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530195"
---
# <a name="getphonecallinformation"></a><span data-ttu-id="52be4-103">GetPhoneCallInformation</span><span class="sxs-lookup"><span data-stu-id="52be4-103">GetPhoneCallInformation</span></span>

<span data-ttu-id="52be4-104">**GetPhoneCallInformation**元素指定获取电话呼叫信息的请求。</span><span class="sxs-lookup"><span data-stu-id="52be4-104">The **GetPhoneCallInformation** element specifies a request to get telephone call information.</span></span> 
  
```xml
<GetPhoneCallInformation>
   <PhoneCallId/>
</GetPhoneCallInformation>
```

 <span data-ttu-id="52be4-105">**GetPhoneCallInformationType**</span><span class="sxs-lookup"><span data-stu-id="52be4-105">**GetPhoneCallInformationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="52be4-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="52be4-106">Attributes and elements</span></span>

<span data-ttu-id="52be4-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="52be4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="52be4-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="52be4-108">Attributes</span></span>

<span data-ttu-id="52be4-109">无。</span><span class="sxs-lookup"><span data-stu-id="52be4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="52be4-110">子元素</span><span class="sxs-lookup"><span data-stu-id="52be4-110">Child elements</span></span>

|<span data-ttu-id="52be4-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="52be4-111">**Element**</span></span>|<span data-ttu-id="52be4-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="52be4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="52be4-113">PhoneCallId</span><span class="sxs-lookup"><span data-stu-id="52be4-113">PhoneCallId</span></span>](phonecallid.md) <br/> |<span data-ttu-id="52be4-114">指定电话呼叫的标识符。</span><span class="sxs-lookup"><span data-stu-id="52be4-114">Specifies the identifier of a phone call.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="52be4-115">父元素</span><span class="sxs-lookup"><span data-stu-id="52be4-115">Parent elements</span></span>

<span data-ttu-id="52be4-116">无。</span><span class="sxs-lookup"><span data-stu-id="52be4-116">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="52be4-117">文本值</span><span class="sxs-lookup"><span data-stu-id="52be4-117">Text value</span></span>

<span data-ttu-id="52be4-118">无。</span><span class="sxs-lookup"><span data-stu-id="52be4-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="52be4-119">说明</span><span class="sxs-lookup"><span data-stu-id="52be4-119">Remarks</span></span>

<span data-ttu-id="52be4-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="52be4-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="52be4-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="52be4-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="52be4-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="52be4-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="52be4-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="52be4-123">Schema Name</span></span>  <br/> |<span data-ttu-id="52be4-124">消息架构</span><span class="sxs-lookup"><span data-stu-id="52be4-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="52be4-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="52be4-125">Validation File</span></span>  <br/> |<span data-ttu-id="52be4-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="52be4-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="52be4-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="52be4-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="52be4-128">False</span><span class="sxs-lookup"><span data-stu-id="52be4-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="52be4-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="52be4-129">See also</span></span>



- [<span data-ttu-id="52be4-130">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="52be4-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

