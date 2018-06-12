---
title: GetMailTips
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetMailTips
api_type:
- schema
ms.assetid: 4a24ff79-f1ae-43a1-9ac2-49baf3eaa173
description: GetMailTips 元素均表示要检索的收件人和类型的邮件提示。
ms.openlocfilehash: aad3b3d9dd578d0c92bf7d48ee8b78b58c63e23d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754611"
---
# <a name="getmailtips"></a><span data-ttu-id="d26fc-103">GetMailTips</span><span class="sxs-lookup"><span data-stu-id="d26fc-103">GetMailTips</span></span>

<span data-ttu-id="d26fc-104">**GetMailTips**元素均表示要检索的收件人和类型的邮件提示。</span><span class="sxs-lookup"><span data-stu-id="d26fc-104">The **GetMailTips** element represents the recipients and types of mail tips to retrieve.</span></span> 
  
```XML
<GetMailTips>
   <SendingAs/>
   <Recipients/>
   <MailTipsRequested/>
</GetMailTips>
```

 <span data-ttu-id="d26fc-105">**GetMailTipsType**</span><span class="sxs-lookup"><span data-stu-id="d26fc-105">**GetMailTipsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d26fc-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d26fc-106">Attributes and elements</span></span>

<span data-ttu-id="d26fc-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d26fc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d26fc-108">属性</span><span class="sxs-lookup"><span data-stu-id="d26fc-108">Attributes</span></span>

<span data-ttu-id="d26fc-109">无。</span><span class="sxs-lookup"><span data-stu-id="d26fc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d26fc-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d26fc-110">Child elements</span></span>

|<span data-ttu-id="d26fc-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="d26fc-111">**Element**</span></span>|<span data-ttu-id="d26fc-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="d26fc-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d26fc-113">SendingAs</span><span class="sxs-lookup"><span data-stu-id="d26fc-113">SendingAs</span></span>](sendingas.md) <br/> |<span data-ttu-id="d26fc-114">包含用户试图将作为发送电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="d26fc-114">Contains an e-mail address that a user is trying to send as.</span></span>  <br/> |
|[<span data-ttu-id="d26fc-115">收件人 (ArrayOfRecipientsType)</span><span class="sxs-lookup"><span data-stu-id="d26fc-115">Recipients (ArrayOfRecipientsType)</span></span>](recipients-arrayofrecipientstype.md) <br/> |<span data-ttu-id="d26fc-116">包含要检查邮件提示的收件人列表。</span><span class="sxs-lookup"><span data-stu-id="d26fc-116">Contains a list of recipients to check for mail tips.</span></span>  <br/> |
|[<span data-ttu-id="d26fc-117">MailTipsRequested</span><span class="sxs-lookup"><span data-stu-id="d26fc-117">MailTipsRequested</span></span>](mailtipsrequested.md) <br/> |<span data-ttu-id="d26fc-118">包含邮件提示从的服务请求的类型。</span><span class="sxs-lookup"><span data-stu-id="d26fc-118">Contains the types of mail tips requested from the service.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d26fc-119">父元素</span><span class="sxs-lookup"><span data-stu-id="d26fc-119">Parent elements</span></span>

<span data-ttu-id="d26fc-120">无。</span><span class="sxs-lookup"><span data-stu-id="d26fc-120">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="d26fc-121">文本值</span><span class="sxs-lookup"><span data-stu-id="d26fc-121">Text value</span></span>

<span data-ttu-id="d26fc-122">无。</span><span class="sxs-lookup"><span data-stu-id="d26fc-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d26fc-123">备注</span><span class="sxs-lookup"><span data-stu-id="d26fc-123">Remarks</span></span>

<span data-ttu-id="d26fc-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d26fc-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d26fc-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="d26fc-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d26fc-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="d26fc-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d26fc-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="d26fc-127">Schema Name</span></span>  <br/> |<span data-ttu-id="d26fc-128">消息架构</span><span class="sxs-lookup"><span data-stu-id="d26fc-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d26fc-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="d26fc-129">Validation File</span></span>  <br/> |<span data-ttu-id="d26fc-130">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d26fc-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d26fc-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="d26fc-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="d26fc-132">False</span><span class="sxs-lookup"><span data-stu-id="d26fc-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d26fc-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d26fc-133">See also</span></span>



- [<span data-ttu-id="d26fc-134">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d26fc-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

