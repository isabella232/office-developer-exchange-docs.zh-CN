---
title: GetMailTipsResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetMailTipsResponse
api_type:
- schema
ms.assetid: fe270e34-566e-4f9e-9e73-fbf38e06436d
description: GetMailTipsResponse 元素均表示 GetMailTips 操作的响应消息。
ms.openlocfilehash: e7a18e8818761af931d32b26aeaf58a2853fa684
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754613"
---
# <a name="getmailtipsresponse"></a><span data-ttu-id="baddc-103">GetMailTipsResponse</span><span class="sxs-lookup"><span data-stu-id="baddc-103">GetMailTipsResponse</span></span>

<span data-ttu-id="baddc-104">**GetMailTipsResponse**元素表示[GetMailTips 操作](getmailtips-operation.md)响应消息。</span><span class="sxs-lookup"><span data-stu-id="baddc-104">The **GetMailTipsResponse** element represents the response message for a [GetMailTips operation](getmailtips-operation.md).</span></span>
  
```XML
<GetMailTipsResponse>
   <ResponseMessages/>
</GetMailTipsResponse>
```

 <span data-ttu-id="baddc-105">**GetMailTipsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="baddc-105">**GetMailTipsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="baddc-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="baddc-106">Attributes and elements</span></span>

<span data-ttu-id="baddc-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="baddc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="baddc-108">属性</span><span class="sxs-lookup"><span data-stu-id="baddc-108">Attributes</span></span>

<span data-ttu-id="baddc-109">无。</span><span class="sxs-lookup"><span data-stu-id="baddc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="baddc-110">子元素</span><span class="sxs-lookup"><span data-stu-id="baddc-110">Child elements</span></span>

|<span data-ttu-id="baddc-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="baddc-111">**Element**</span></span>|<span data-ttu-id="baddc-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="baddc-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="baddc-113">ResponseMessages (ArrayOfMailTipsResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="baddc-113">ResponseMessages (ArrayOfMailTipsResponseMessageType)</span></span>](responsemessages-arrayofmailtipsresponsemessagetype.md) <br/> |<span data-ttu-id="baddc-114">代表一个邮件提示响应的列表。</span><span class="sxs-lookup"><span data-stu-id="baddc-114">Represents a list of mail tips response messages.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="baddc-115">父元素</span><span class="sxs-lookup"><span data-stu-id="baddc-115">Parent elements</span></span>

<span data-ttu-id="baddc-116">无。</span><span class="sxs-lookup"><span data-stu-id="baddc-116">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="baddc-117">文本值</span><span class="sxs-lookup"><span data-stu-id="baddc-117">Text value</span></span>

<span data-ttu-id="baddc-118">无。</span><span class="sxs-lookup"><span data-stu-id="baddc-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="baddc-119">备注</span><span class="sxs-lookup"><span data-stu-id="baddc-119">Remarks</span></span>

<span data-ttu-id="baddc-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="baddc-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="baddc-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="baddc-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="baddc-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="baddc-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="baddc-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="baddc-123">Schema Name</span></span>  <br/> |<span data-ttu-id="baddc-124">消息架构</span><span class="sxs-lookup"><span data-stu-id="baddc-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="baddc-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="baddc-125">Validation File</span></span>  <br/> |<span data-ttu-id="baddc-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="baddc-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="baddc-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="baddc-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="baddc-128">False</span><span class="sxs-lookup"><span data-stu-id="baddc-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="baddc-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="baddc-129">See also</span></span>



[<span data-ttu-id="baddc-130">GetMailTips 操作</span><span class="sxs-lookup"><span data-stu-id="baddc-130">GetMailTips operation</span></span>](getmailtips-operation.md)


- [<span data-ttu-id="baddc-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="baddc-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

