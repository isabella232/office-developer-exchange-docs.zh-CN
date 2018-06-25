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
description: MailTipsConfiguration 元素包含的邮件提示服务的服务配置信息。
ms.openlocfilehash: ea92af3ebb2d2f720e5823c5317d09d5bcdb3978
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826321"
---
# <a name="mailtipsconfiguration-mailtipsserviceconfiguration"></a><span data-ttu-id="22ae5-103">MailTipsConfiguration (MailTipsServiceConfiguration)</span><span class="sxs-lookup"><span data-stu-id="22ae5-103">MailTipsConfiguration (MailTipsServiceConfiguration)</span></span>

<span data-ttu-id="22ae5-104">**MailTipsConfiguration**元素包含的邮件提示服务的服务配置信息。</span><span class="sxs-lookup"><span data-stu-id="22ae5-104">The **MailTipsConfiguration** element contains service configuration information for the mail tips service.</span></span> 
  
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

 <span data-ttu-id="22ae5-105">**MailTipsServiceConfiguration**</span><span class="sxs-lookup"><span data-stu-id="22ae5-105">**MailTipsServiceConfiguration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="22ae5-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="22ae5-106">Attributes and elements</span></span>

<span data-ttu-id="22ae5-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="22ae5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="22ae5-108">属性</span><span class="sxs-lookup"><span data-stu-id="22ae5-108">Attributes</span></span>

<span data-ttu-id="22ae5-109">无。</span><span class="sxs-lookup"><span data-stu-id="22ae5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="22ae5-110">子元素</span><span class="sxs-lookup"><span data-stu-id="22ae5-110">Child elements</span></span>

|<span data-ttu-id="22ae5-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="22ae5-111">**Element**</span></span>|<span data-ttu-id="22ae5-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="22ae5-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="22ae5-113">MailTipsEnabled</span><span class="sxs-lookup"><span data-stu-id="22ae5-113">MailTipsEnabled</span></span>](mailtipsenabled.md) <br/> |<span data-ttu-id="22ae5-114">指示邮件提示服务是否可用。</span><span class="sxs-lookup"><span data-stu-id="22ae5-114">Indicates whether the mail tips service is available.</span></span> <span data-ttu-id="22ae5-115">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="22ae5-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="22ae5-116">MaxRecipientsPerGetMailTipsRequest</span><span class="sxs-lookup"><span data-stu-id="22ae5-116">MaxRecipientsPerGetMailTipsRequest</span></span>](maxrecipientspergetmailtipsrequest.md) <br/> |<span data-ttu-id="22ae5-117">指示可以传递到[GetMailTips 操作](getmailtips-operation.md)的收件人的最大数量。</span><span class="sxs-lookup"><span data-stu-id="22ae5-117">Indicates the maximum number of recipients that can be passed to the [GetMailTips operation](getmailtips-operation.md).</span></span> <span data-ttu-id="22ae5-118">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="22ae5-118">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="22ae5-119">MaxMessageSize</span><span class="sxs-lookup"><span data-stu-id="22ae5-119">MaxMessageSize</span></span>](maxmessagesize.md) <br/> |<span data-ttu-id="22ae5-120">表示收件人可以接受的最大邮件大小。</span><span class="sxs-lookup"><span data-stu-id="22ae5-120">Represents the maximum message size a recipient can accept.</span></span> <span data-ttu-id="22ae5-121">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="22ae5-121">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="22ae5-122">LargeAudienceThreshold</span><span class="sxs-lookup"><span data-stu-id="22ae5-122">LargeAudienceThreshold</span></span>](largeaudiencethreshold.md) <br/> |<span data-ttu-id="22ae5-123">表示用于客户端的大型受众阈值。</span><span class="sxs-lookup"><span data-stu-id="22ae5-123">Represents the large audience threshold for a client.</span></span> <span data-ttu-id="22ae5-124">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="22ae5-124">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="22ae5-125">ShowExternalRecipientCount</span><span class="sxs-lookup"><span data-stu-id="22ae5-125">ShowExternalRecipientCount</span></span>](showexternalrecipientcount.md) <br/> |<span data-ttu-id="22ae5-126">指示是否[GetMailTips 操作](getmailtips-operation.md)的使用者具有显示邮件提示指示邮件要发送到外部收件人的数量。</span><span class="sxs-lookup"><span data-stu-id="22ae5-126">Indicates whether consumers of the [GetMailTips operation](getmailtips-operation.md) have to show mail tips that indicate the number of external recipients to which a message is addressed.</span></span> <span data-ttu-id="22ae5-127">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="22ae5-127">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="22ae5-128">InternalDomains (SmtpDomainList)</span><span class="sxs-lookup"><span data-stu-id="22ae5-128">InternalDomains (SmtpDomainList)</span></span>](internaldomains-smtpdomainlist.md) <br/> |<span data-ttu-id="22ae5-129">标识组织的内部 SMTP 域的列表。</span><span class="sxs-lookup"><span data-stu-id="22ae5-129">Identifies the list of internal SMTP domains of the organization.</span></span> <span data-ttu-id="22ae5-130">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="22ae5-130">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="22ae5-131">父元素</span><span class="sxs-lookup"><span data-stu-id="22ae5-131">Parent elements</span></span>

|<span data-ttu-id="22ae5-132">**元素**</span><span class="sxs-lookup"><span data-stu-id="22ae5-132">**Element**</span></span>|<span data-ttu-id="22ae5-133">**说明**</span><span class="sxs-lookup"><span data-stu-id="22ae5-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="22ae5-134">ServiceConfigurationResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="22ae5-134">ServiceConfigurationResponseMessageType</span></span>](serviceconfigurationresponsemessagetype.md) <br/> |<span data-ttu-id="22ae5-135">包含服务配置设置。</span><span class="sxs-lookup"><span data-stu-id="22ae5-135">Contains service configuration settings.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="22ae5-136">文本值</span><span class="sxs-lookup"><span data-stu-id="22ae5-136">Text value</span></span>

<span data-ttu-id="22ae5-137">无。</span><span class="sxs-lookup"><span data-stu-id="22ae5-137">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="22ae5-138">备注</span><span class="sxs-lookup"><span data-stu-id="22ae5-138">Remarks</span></span>

<span data-ttu-id="22ae5-139">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="22ae5-139">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="22ae5-140">元素信息</span><span class="sxs-lookup"><span data-stu-id="22ae5-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="22ae5-141">命名空间</span><span class="sxs-lookup"><span data-stu-id="22ae5-141">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="22ae5-142">架构名称</span><span class="sxs-lookup"><span data-stu-id="22ae5-142">Schema Name</span></span>  <br/> |<span data-ttu-id="22ae5-143">消息架构</span><span class="sxs-lookup"><span data-stu-id="22ae5-143">Messages schema</span></span>  <br/> |
|<span data-ttu-id="22ae5-144">验证文件</span><span class="sxs-lookup"><span data-stu-id="22ae5-144">Validation File</span></span>  <br/> |<span data-ttu-id="22ae5-145">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="22ae5-145">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="22ae5-146">可以为空</span><span class="sxs-lookup"><span data-stu-id="22ae5-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="22ae5-147">False</span><span class="sxs-lookup"><span data-stu-id="22ae5-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="22ae5-148">另请参阅</span><span class="sxs-lookup"><span data-stu-id="22ae5-148">See also</span></span>



- [<span data-ttu-id="22ae5-149">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="22ae5-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

