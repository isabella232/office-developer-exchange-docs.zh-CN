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
description: GetMailTipsResponse 元素表示 GetMailTips 操作的响应消息。
ms.openlocfilehash: 2c0dcfe4e2deddcf9a6f4bb9d68d59115c171796
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458605"
---
# <a name="getmailtipsresponse"></a><span data-ttu-id="a293b-103">GetMailTipsResponse</span><span class="sxs-lookup"><span data-stu-id="a293b-103">GetMailTipsResponse</span></span>

<span data-ttu-id="a293b-104">**GetMailTipsResponse**元素表示[GetMailTips 操作](getmailtips-operation.md)的响应消息。</span><span class="sxs-lookup"><span data-stu-id="a293b-104">The **GetMailTipsResponse** element represents the response message for a [GetMailTips operation](getmailtips-operation.md).</span></span>
  
```XML
<GetMailTipsResponse>
   <ResponseMessages/>
</GetMailTipsResponse>
```

 <span data-ttu-id="a293b-105">**GetMailTipsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="a293b-105">**GetMailTipsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a293b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a293b-106">Attributes and elements</span></span>

<span data-ttu-id="a293b-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a293b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a293b-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="a293b-108">Attributes</span></span>

<span data-ttu-id="a293b-109">无。</span><span class="sxs-lookup"><span data-stu-id="a293b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a293b-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a293b-110">Child elements</span></span>

|<span data-ttu-id="a293b-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="a293b-111">**Element**</span></span>|<span data-ttu-id="a293b-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="a293b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a293b-113">ResponseMessages (ArrayOfMailTipsResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="a293b-113">ResponseMessages (ArrayOfMailTipsResponseMessageType)</span></span>](responsemessages-arrayofmailtipsresponsemessagetype.md) <br/> |<span data-ttu-id="a293b-114">表示邮件提示响应邮件的列表。</span><span class="sxs-lookup"><span data-stu-id="a293b-114">Represents a list of mail tips response messages.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a293b-115">父元素</span><span class="sxs-lookup"><span data-stu-id="a293b-115">Parent elements</span></span>

<span data-ttu-id="a293b-116">无。</span><span class="sxs-lookup"><span data-stu-id="a293b-116">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="a293b-117">文本值</span><span class="sxs-lookup"><span data-stu-id="a293b-117">Text value</span></span>

<span data-ttu-id="a293b-118">无。</span><span class="sxs-lookup"><span data-stu-id="a293b-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a293b-119">说明</span><span class="sxs-lookup"><span data-stu-id="a293b-119">Remarks</span></span>

<span data-ttu-id="a293b-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a293b-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a293b-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="a293b-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a293b-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="a293b-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a293b-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="a293b-123">Schema Name</span></span>  <br/> |<span data-ttu-id="a293b-124">消息架构</span><span class="sxs-lookup"><span data-stu-id="a293b-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a293b-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="a293b-125">Validation File</span></span>  <br/> |<span data-ttu-id="a293b-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a293b-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a293b-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="a293b-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="a293b-128">False</span><span class="sxs-lookup"><span data-stu-id="a293b-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a293b-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a293b-129">See also</span></span>



[<span data-ttu-id="a293b-130">GetMailTips 操作</span><span class="sxs-lookup"><span data-stu-id="a293b-130">GetMailTips operation</span></span>](getmailtips-operation.md)


- [<span data-ttu-id="a293b-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a293b-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

