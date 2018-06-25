---
title: AllowExternalOof
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AllowExternalOof
api_type:
- schema
ms.assetid: e5387172-5b92-4bb1-8394-180e9c7ff771
description: AllowExternalOof 元素包含一个值，该值标识向其发送外部外出 (OOF) 邮件。
ms.openlocfilehash: 1c87a51676bf6e44b2e650a4e973d0ab89a52e31
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753142"
---
# <a name="allowexternaloof"></a><span data-ttu-id="31fcb-103">AllowExternalOof</span><span class="sxs-lookup"><span data-stu-id="31fcb-103">AllowExternalOof</span></span>

<span data-ttu-id="31fcb-104">**AllowExternalOof**元素包含一个值，该值标识向其发送外部外出 (OOF) 邮件。</span><span class="sxs-lookup"><span data-stu-id="31fcb-104">The **AllowExternalOof** element contains a value that identifies to whom external Out of Office (OOF) messages are sent.</span></span> 
  
- [<span data-ttu-id="31fcb-105">GetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="31fcb-105">GetUserOofSettingsResponse</span></span>](getuseroofsettingsresponse.md)
  
- [<span data-ttu-id="31fcb-106">AllowExternalOof</span><span class="sxs-lookup"><span data-stu-id="31fcb-106">AllowExternalOof</span></span>](allowexternaloof.md)
  
```xml
<AllowExternalOof>None or Known or All</AllowExternalOof>
```

 <span data-ttu-id="31fcb-107">**ExternalAudience**</span><span class="sxs-lookup"><span data-stu-id="31fcb-107">**ExternalAudience**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="31fcb-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="31fcb-108">Attributes and elements</span></span>

<span data-ttu-id="31fcb-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="31fcb-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="31fcb-110">属性</span><span class="sxs-lookup"><span data-stu-id="31fcb-110">Attributes</span></span>

<span data-ttu-id="31fcb-111">无。</span><span class="sxs-lookup"><span data-stu-id="31fcb-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="31fcb-112">子元素</span><span class="sxs-lookup"><span data-stu-id="31fcb-112">Child elements</span></span>

<span data-ttu-id="31fcb-113">无。</span><span class="sxs-lookup"><span data-stu-id="31fcb-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="31fcb-114">父元素</span><span class="sxs-lookup"><span data-stu-id="31fcb-114">Parent elements</span></span>

|<span data-ttu-id="31fcb-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="31fcb-115">**Element**</span></span>|<span data-ttu-id="31fcb-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="31fcb-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="31fcb-117">GetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="31fcb-117">GetUserOofSettingsResponse</span></span>](getuseroofsettingsresponse.md) <br/> |<span data-ttu-id="31fcb-118">包含响应结果和用户的 OOF 设置。</span><span class="sxs-lookup"><span data-stu-id="31fcb-118">Contains the response results and the OOF settings for a user.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="31fcb-119">文本值</span><span class="sxs-lookup"><span data-stu-id="31fcb-119">Text value</span></span>

<span data-ttu-id="31fcb-120">需要为此元素的文本值。</span><span class="sxs-lookup"><span data-stu-id="31fcb-120">A text value is required for this element.</span></span> <span data-ttu-id="31fcb-121">下表列出了此元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="31fcb-121">The following table lists the possible values for this element.</span></span>
  
|<span data-ttu-id="31fcb-122">**值**</span><span class="sxs-lookup"><span data-stu-id="31fcb-122">**Value**</span></span>|<span data-ttu-id="31fcb-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="31fcb-123">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="31fcb-124">**None**</span><span class="sxs-lookup"><span data-stu-id="31fcb-124">**None**</span></span> <br/> |<span data-ttu-id="31fcb-125">邮箱用户的组织外部的电子邮件发件人将邮件发送到用户不会收到外部 OOF 消息响应。</span><span class="sxs-lookup"><span data-stu-id="31fcb-125">E-mail senders outside the mailbox user's organization who send messages to the user will not receive an external OOF message response.</span></span>  <br/> |
|<span data-ttu-id="31fcb-126">**已知**</span><span class="sxs-lookup"><span data-stu-id="31fcb-126">**Known**</span></span> <br/> |<span data-ttu-id="31fcb-127">邮箱用户的组织外部的电子邮件发件人发送给用户的消息将仅接收外部 OOF 消息响应如果发件人是用户的 Exchange 中存储的联系人列表。</span><span class="sxs-lookup"><span data-stu-id="31fcb-127">E-mail senders outside the mailbox user's organization who send messages to the user will only receive an external OOF message response if the sender is in the user's Exchange store contact list.</span></span>  <br/> |
|<span data-ttu-id="31fcb-128">**All**</span><span class="sxs-lookup"><span data-stu-id="31fcb-128">**All**</span></span> <br/> |<span data-ttu-id="31fcb-129">邮箱用户的组织外部的电子邮件发件人将邮件发送到用户将收到外部 OOF 消息响应。</span><span class="sxs-lookup"><span data-stu-id="31fcb-129">E-mail senders outside the mailbox user's organization who send messages to the user will receive an external OOF message response.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="31fcb-130">注解</span><span class="sxs-lookup"><span data-stu-id="31fcb-130">Remarks</span></span>

<span data-ttu-id="31fcb-131">此元素共享[ExternalAudience](externalaudience.md)元素类型相同。</span><span class="sxs-lookup"><span data-stu-id="31fcb-131">This element shares the same type as the [ExternalAudience](externalaudience.md) element.</span></span> 
  
<span data-ttu-id="31fcb-132">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="31fcb-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="31fcb-133">元素信息</span><span class="sxs-lookup"><span data-stu-id="31fcb-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="31fcb-134">命名空间</span><span class="sxs-lookup"><span data-stu-id="31fcb-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="31fcb-135">架构名称</span><span class="sxs-lookup"><span data-stu-id="31fcb-135">Schema Name</span></span>  <br/> |<span data-ttu-id="31fcb-136">消息架构</span><span class="sxs-lookup"><span data-stu-id="31fcb-136">Messages schema</span></span>  <br/> |
|<span data-ttu-id="31fcb-137">验证文件</span><span class="sxs-lookup"><span data-stu-id="31fcb-137">Validation File</span></span>  <br/> |<span data-ttu-id="31fcb-138">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="31fcb-138">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="31fcb-139">可以为空</span><span class="sxs-lookup"><span data-stu-id="31fcb-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="31fcb-140">False</span><span class="sxs-lookup"><span data-stu-id="31fcb-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="31fcb-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="31fcb-141">See also</span></span>

- [<span data-ttu-id="31fcb-142">GetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="31fcb-142">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md) 
- [<span data-ttu-id="31fcb-143">SetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="31fcb-143">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

