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
description: AllowExternalOof 元素包含一个值，该值标识向其发送外部外出（OOF）邮件的人员。
ms.openlocfilehash: e4934bc4bc86e1f9f764279a13ecaeca073d9e5d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464810"
---
# <a name="allowexternaloof"></a><span data-ttu-id="1967a-103">AllowExternalOof</span><span class="sxs-lookup"><span data-stu-id="1967a-103">AllowExternalOof</span></span>

<span data-ttu-id="1967a-104">**AllowExternalOof**元素包含一个值，该值标识向其发送外部外出（OOF）邮件的人员。</span><span class="sxs-lookup"><span data-stu-id="1967a-104">The **AllowExternalOof** element contains a value that identifies to whom external Out of Office (OOF) messages are sent.</span></span> 
  
- [<span data-ttu-id="1967a-105">GetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="1967a-105">GetUserOofSettingsResponse</span></span>](getuseroofsettingsresponse.md)
  
- [<span data-ttu-id="1967a-106">AllowExternalOof</span><span class="sxs-lookup"><span data-stu-id="1967a-106">AllowExternalOof</span></span>](allowexternaloof.md)
  
```xml
<AllowExternalOof>None or Known or All</AllowExternalOof>
```

 <span data-ttu-id="1967a-107">**ExternalAudience**</span><span class="sxs-lookup"><span data-stu-id="1967a-107">**ExternalAudience**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1967a-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1967a-108">Attributes and elements</span></span>

<span data-ttu-id="1967a-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1967a-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1967a-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="1967a-110">Attributes</span></span>

<span data-ttu-id="1967a-111">无。</span><span class="sxs-lookup"><span data-stu-id="1967a-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1967a-112">子元素</span><span class="sxs-lookup"><span data-stu-id="1967a-112">Child elements</span></span>

<span data-ttu-id="1967a-113">无。</span><span class="sxs-lookup"><span data-stu-id="1967a-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1967a-114">父元素</span><span class="sxs-lookup"><span data-stu-id="1967a-114">Parent elements</span></span>

|<span data-ttu-id="1967a-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="1967a-115">**Element**</span></span>|<span data-ttu-id="1967a-116">**描述**</span><span class="sxs-lookup"><span data-stu-id="1967a-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1967a-117">GetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="1967a-117">GetUserOofSettingsResponse</span></span>](getuseroofsettingsresponse.md) <br/> |<span data-ttu-id="1967a-118">包含用户的响应结果和 OOF 设置。</span><span class="sxs-lookup"><span data-stu-id="1967a-118">Contains the response results and the OOF settings for a user.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1967a-119">文本值</span><span class="sxs-lookup"><span data-stu-id="1967a-119">Text value</span></span>

<span data-ttu-id="1967a-120">此元素需要一个文本值。</span><span class="sxs-lookup"><span data-stu-id="1967a-120">A text value is required for this element.</span></span> <span data-ttu-id="1967a-121">下表列出了此元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="1967a-121">The following table lists the possible values for this element.</span></span>
  
|<span data-ttu-id="1967a-122">**值**</span><span class="sxs-lookup"><span data-stu-id="1967a-122">**Value**</span></span>|<span data-ttu-id="1967a-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="1967a-123">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1967a-124">**无**</span><span class="sxs-lookup"><span data-stu-id="1967a-124">**None**</span></span> <br/> |<span data-ttu-id="1967a-125">向用户发送邮件的邮箱用户组织外部的电子邮件发件人将不会收到外部 OOF 邮件响应。</span><span class="sxs-lookup"><span data-stu-id="1967a-125">E-mail senders outside the mailbox user's organization who send messages to the user will not receive an external OOF message response.</span></span>  <br/> |
|<span data-ttu-id="1967a-126">**叫做**</span><span class="sxs-lookup"><span data-stu-id="1967a-126">**Known**</span></span> <br/> |<span data-ttu-id="1967a-127">如果邮箱用户的组织外部的电子邮件发件人向用户发送邮件，则仅会收到外部 OOF 邮件响应（如果发件人位于用户的 Exchange 存储联系人列表中）。</span><span class="sxs-lookup"><span data-stu-id="1967a-127">E-mail senders outside the mailbox user's organization who send messages to the user will only receive an external OOF message response if the sender is in the user's Exchange store contact list.</span></span>  <br/> |
|<span data-ttu-id="1967a-128">**All**</span><span class="sxs-lookup"><span data-stu-id="1967a-128">**All**</span></span> <br/> |<span data-ttu-id="1967a-129">将邮件发送给用户的邮箱用户的组织外部的电子邮件发件人将收到外部 OOF 邮件响应。</span><span class="sxs-lookup"><span data-stu-id="1967a-129">E-mail senders outside the mailbox user's organization who send messages to the user will receive an external OOF message response.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1967a-130">备注</span><span class="sxs-lookup"><span data-stu-id="1967a-130">Remarks</span></span>

<span data-ttu-id="1967a-131">此元素与[ExternalAudience](externalaudience.md)元素共享相同的类型。</span><span class="sxs-lookup"><span data-stu-id="1967a-131">This element shares the same type as the [ExternalAudience](externalaudience.md) element.</span></span> 
  
<span data-ttu-id="1967a-132">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1967a-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1967a-133">元素信息</span><span class="sxs-lookup"><span data-stu-id="1967a-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1967a-134">命名空间</span><span class="sxs-lookup"><span data-stu-id="1967a-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1967a-135">架构名称</span><span class="sxs-lookup"><span data-stu-id="1967a-135">Schema Name</span></span>  <br/> |<span data-ttu-id="1967a-136">消息架构</span><span class="sxs-lookup"><span data-stu-id="1967a-136">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1967a-137">验证文件</span><span class="sxs-lookup"><span data-stu-id="1967a-137">Validation File</span></span>  <br/> |<span data-ttu-id="1967a-138">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1967a-138">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1967a-139">可以为空</span><span class="sxs-lookup"><span data-stu-id="1967a-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="1967a-140">False</span><span class="sxs-lookup"><span data-stu-id="1967a-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1967a-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1967a-141">See also</span></span>

- [<span data-ttu-id="1967a-142">GetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="1967a-142">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md) 
- [<span data-ttu-id="1967a-143">SetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="1967a-143">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

