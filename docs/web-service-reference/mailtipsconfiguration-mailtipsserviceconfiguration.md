---
title: MailTipsConfiguration (MailTipsServiceConfiguration)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailTipsConfiguration
api_type:
- schema
ms.assetid: 9a34515e-815b-4c61-b118-d5f66b80238f
description: MailTipsConfiguration 元素包含邮件提示服务的服务配置信息。
ms.openlocfilehash: 9128ee99545066899c3b27b624f10a9f1bd36c9d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467786"
---
# <a name="mailtipsconfiguration-mailtipsserviceconfiguration"></a><span data-ttu-id="cfd04-103">MailTipsConfiguration (MailTipsServiceConfiguration)</span><span class="sxs-lookup"><span data-stu-id="cfd04-103">MailTipsConfiguration (MailTipsServiceConfiguration)</span></span>

<span data-ttu-id="cfd04-104">**MailTipsConfiguration**元素包含邮件提示服务的服务配置信息。</span><span class="sxs-lookup"><span data-stu-id="cfd04-104">The **MailTipsConfiguration** element contains service configuration information for the mail tips service.</span></span> 
  
```XML
<MailTipsConfiguration>
   <MailTipsEnabled/>
   <MaxRecipientsPerGetMailTipsRequest/>
   <MaxMessageSize/>
   <LargeAudienceThreshold/>
   <ShowExternalRecipientCount/>
   <InternalDomains/>
</MailTipsConfiguration>
```

 <span data-ttu-id="cfd04-105">**MailTipsServiceConfiguration**</span><span class="sxs-lookup"><span data-stu-id="cfd04-105">**MailTipsServiceConfiguration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cfd04-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="cfd04-106">Attributes and elements</span></span>

<span data-ttu-id="cfd04-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="cfd04-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cfd04-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="cfd04-108">Attributes</span></span>

<span data-ttu-id="cfd04-109">无。</span><span class="sxs-lookup"><span data-stu-id="cfd04-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cfd04-110">子元素</span><span class="sxs-lookup"><span data-stu-id="cfd04-110">Child elements</span></span>

|<span data-ttu-id="cfd04-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="cfd04-111">**Element**</span></span>|<span data-ttu-id="cfd04-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="cfd04-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cfd04-113">MailTipsEnabled</span><span class="sxs-lookup"><span data-stu-id="cfd04-113">MailTipsEnabled</span></span>](mailtipsenabled.md) <br/> |<span data-ttu-id="cfd04-114">指示是否可以使用邮件提示服务。</span><span class="sxs-lookup"><span data-stu-id="cfd04-114">Indicates whether the mail tips service is available.</span></span> <span data-ttu-id="cfd04-115">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="cfd04-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="cfd04-116">MaxRecipientsPerGetMailTipsRequest</span><span class="sxs-lookup"><span data-stu-id="cfd04-116">MaxRecipientsPerGetMailTipsRequest</span></span>](maxrecipientspergetmailtipsrequest.md) <br/> |<span data-ttu-id="cfd04-117">指示可传递给[GetMailTips 操作](getmailtips-operation.md)的最大收件人数。</span><span class="sxs-lookup"><span data-stu-id="cfd04-117">Indicates the maximum number of recipients that can be passed to the [GetMailTips operation](getmailtips-operation.md).</span></span> <span data-ttu-id="cfd04-118">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="cfd04-118">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="cfd04-119">MaxMessageSize</span><span class="sxs-lookup"><span data-stu-id="cfd04-119">MaxMessageSize</span></span>](maxmessagesize.md) <br/> |<span data-ttu-id="cfd04-120">表示收件人可接受的最大邮件大小。</span><span class="sxs-lookup"><span data-stu-id="cfd04-120">Represents the maximum message size a recipient can accept.</span></span> <span data-ttu-id="cfd04-121">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="cfd04-121">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="cfd04-122">LargeAudienceThreshold</span><span class="sxs-lookup"><span data-stu-id="cfd04-122">LargeAudienceThreshold</span></span>](largeaudiencethreshold.md) <br/> |<span data-ttu-id="cfd04-123">表示客户端的大型访问群体阈值。</span><span class="sxs-lookup"><span data-stu-id="cfd04-123">Represents the large audience threshold for a client.</span></span> <span data-ttu-id="cfd04-124">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="cfd04-124">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="cfd04-125">ShowExternalRecipientCount</span><span class="sxs-lookup"><span data-stu-id="cfd04-125">ShowExternalRecipientCount</span></span>](showexternalrecipientcount.md) <br/> |<span data-ttu-id="cfd04-126">指示[GetMailTips 操作](getmailtips-operation.md)的使用者是否必须显示指示向其发送邮件的外部收件人数的邮件提示。</span><span class="sxs-lookup"><span data-stu-id="cfd04-126">Indicates whether consumers of the [GetMailTips operation](getmailtips-operation.md) have to show mail tips that indicate the number of external recipients to which a message is addressed.</span></span> <span data-ttu-id="cfd04-127">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="cfd04-127">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="cfd04-128">InternalDomains （SmtpDomainList）</span><span class="sxs-lookup"><span data-stu-id="cfd04-128">InternalDomains (SmtpDomainList)</span></span>](internaldomains-smtpdomainlist.md) <br/> |<span data-ttu-id="cfd04-129">标识组织的内部 SMTP 域的列表。</span><span class="sxs-lookup"><span data-stu-id="cfd04-129">Identifies the list of internal SMTP domains of the organization.</span></span> <span data-ttu-id="cfd04-130">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="cfd04-130">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cfd04-131">父元素</span><span class="sxs-lookup"><span data-stu-id="cfd04-131">Parent elements</span></span>

|<span data-ttu-id="cfd04-132">**元素**</span><span class="sxs-lookup"><span data-stu-id="cfd04-132">**Element**</span></span>|<span data-ttu-id="cfd04-133">**说明**</span><span class="sxs-lookup"><span data-stu-id="cfd04-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cfd04-134">ServiceConfigurationResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="cfd04-134">ServiceConfigurationResponseMessageType</span></span>](serviceconfigurationresponsemessagetype.md) <br/> |<span data-ttu-id="cfd04-135">包含服务配置设置。</span><span class="sxs-lookup"><span data-stu-id="cfd04-135">Contains service configuration settings.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cfd04-136">文本值</span><span class="sxs-lookup"><span data-stu-id="cfd04-136">Text value</span></span>

<span data-ttu-id="cfd04-137">无。</span><span class="sxs-lookup"><span data-stu-id="cfd04-137">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cfd04-138">说明</span><span class="sxs-lookup"><span data-stu-id="cfd04-138">Remarks</span></span>

<span data-ttu-id="cfd04-139">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="cfd04-139">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cfd04-140">元素信息</span><span class="sxs-lookup"><span data-stu-id="cfd04-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cfd04-141">命名空间</span><span class="sxs-lookup"><span data-stu-id="cfd04-141">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cfd04-142">架构名称</span><span class="sxs-lookup"><span data-stu-id="cfd04-142">Schema Name</span></span>  <br/> |<span data-ttu-id="cfd04-143">消息架构</span><span class="sxs-lookup"><span data-stu-id="cfd04-143">Messages schema</span></span>  <br/> |
|<span data-ttu-id="cfd04-144">验证文件</span><span class="sxs-lookup"><span data-stu-id="cfd04-144">Validation File</span></span>  <br/> |<span data-ttu-id="cfd04-145">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="cfd04-145">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cfd04-146">可以为空</span><span class="sxs-lookup"><span data-stu-id="cfd04-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="cfd04-147">False</span><span class="sxs-lookup"><span data-stu-id="cfd04-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cfd04-148">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cfd04-148">See also</span></span>



- [<span data-ttu-id="cfd04-149">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="cfd04-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

