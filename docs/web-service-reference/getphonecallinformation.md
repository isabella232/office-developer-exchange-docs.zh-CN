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
description: GetPhoneCallInformation 元素指定要获取电话呼叫的信息的请求。
ms.openlocfilehash: 2084a8b5e13b3fa03e0bf62439978bbe81d86ce9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754661"
---
# <a name="getphonecallinformation"></a><span data-ttu-id="faa8a-103">GetPhoneCallInformation</span><span class="sxs-lookup"><span data-stu-id="faa8a-103">GetPhoneCallInformation</span></span>

<span data-ttu-id="faa8a-104">**GetPhoneCallInformation**元素指定要获取电话呼叫的信息的请求。</span><span class="sxs-lookup"><span data-stu-id="faa8a-104">The **GetPhoneCallInformation** element specifies a request to get telephone call information.</span></span> 
  
```xml
<GetPhoneCallInformation>
   <PhoneCallId/>
</GetPhoneCallInformation>
```

 <span data-ttu-id="faa8a-105">**GetPhoneCallInformationType**</span><span class="sxs-lookup"><span data-stu-id="faa8a-105">**GetPhoneCallInformationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="faa8a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="faa8a-106">Attributes and elements</span></span>

<span data-ttu-id="faa8a-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="faa8a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="faa8a-108">属性</span><span class="sxs-lookup"><span data-stu-id="faa8a-108">Attributes</span></span>

<span data-ttu-id="faa8a-109">无。</span><span class="sxs-lookup"><span data-stu-id="faa8a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="faa8a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="faa8a-110">Child elements</span></span>

|<span data-ttu-id="faa8a-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="faa8a-111">**Element**</span></span>|<span data-ttu-id="faa8a-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="faa8a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="faa8a-113">PhoneCallId</span><span class="sxs-lookup"><span data-stu-id="faa8a-113">PhoneCallId</span></span>](phonecallid.md) <br/> |<span data-ttu-id="faa8a-114">指定的电话呼叫的标识符。</span><span class="sxs-lookup"><span data-stu-id="faa8a-114">Specifies the identifier of a phone call.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="faa8a-115">父元素</span><span class="sxs-lookup"><span data-stu-id="faa8a-115">Parent elements</span></span>

<span data-ttu-id="faa8a-116">无。</span><span class="sxs-lookup"><span data-stu-id="faa8a-116">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="faa8a-117">文本值</span><span class="sxs-lookup"><span data-stu-id="faa8a-117">Text value</span></span>

<span data-ttu-id="faa8a-118">无。</span><span class="sxs-lookup"><span data-stu-id="faa8a-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="faa8a-119">备注</span><span class="sxs-lookup"><span data-stu-id="faa8a-119">Remarks</span></span>

<span data-ttu-id="faa8a-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="faa8a-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="faa8a-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="faa8a-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="faa8a-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="faa8a-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="faa8a-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="faa8a-123">Schema Name</span></span>  <br/> |<span data-ttu-id="faa8a-124">消息架构</span><span class="sxs-lookup"><span data-stu-id="faa8a-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="faa8a-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="faa8a-125">Validation File</span></span>  <br/> |<span data-ttu-id="faa8a-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="faa8a-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="faa8a-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="faa8a-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="faa8a-128">False</span><span class="sxs-lookup"><span data-stu-id="faa8a-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="faa8a-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="faa8a-129">See also</span></span>



- [<span data-ttu-id="faa8a-130">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="faa8a-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

