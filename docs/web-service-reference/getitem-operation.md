---
title: GetItem 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
api_name:
- GetItem
api_type:
- schema
ms.assetid: e3590b8b-c2a7-4dad-a014-6360197b68e4
description: 查找有关 GetItem EWS 操作的信息。
localization_priority: Priority
ms.openlocfilehash: 8871dde183974454fc27dbddda489e6b0a70f3aa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463326"
---
# <a name="getitem-operation"></a><span data-ttu-id="87beb-103">GetItem 操作</span><span class="sxs-lookup"><span data-stu-id="87beb-103">GetItem operation</span></span>

<span data-ttu-id="87beb-104">查找有关**GetItem** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="87beb-104">Find information about the **GetItem** EWS operation.</span></span> 
  
<span data-ttu-id="87beb-105">**GetItem**操作从 Exchange 存储中获取项目。</span><span class="sxs-lookup"><span data-stu-id="87beb-105">The **GetItem** operation gets items from the Exchange store.</span></span> 
  
## <a name="using-the-getitem-operation"></a><span data-ttu-id="87beb-106">使用 GetItem 操作</span><span class="sxs-lookup"><span data-stu-id="87beb-106">Using the GetItem operation</span></span>

<span data-ttu-id="87beb-107">**GetItem**操作返回许多项目属性。</span><span class="sxs-lookup"><span data-stu-id="87beb-107">The **GetItem** operation returns many item properties.</span></span> <span data-ttu-id="87beb-108">**GetItem**响应中返回的属性根据所请求的形状、请求的其他属性和返回的项目类型而有所不同。</span><span class="sxs-lookup"><span data-stu-id="87beb-108">The properties that are returned in a **GetItem** response vary based on the requested shape, requested additional properties, and the type of item returned.</span></span> 
  
<span data-ttu-id="87beb-109">[Message](message-ex15websvcsotherref.md)元素表示的电子邮件和所有其他不是由 Exchange Web 服务（EWS）架构强类型化的项目。</span><span class="sxs-lookup"><span data-stu-id="87beb-109">[Message](message-ex15websvcsotherref.md) elements represent email messages and all other items that are not strongly typed by the Exchange Web Services (EWS) schema.</span></span> <span data-ttu-id="87beb-110">项目，如 IPM。共享和 IPM. InfoPath 以[邮件](message-ex15websvcsotherref.md)元素的形式返回。</span><span class="sxs-lookup"><span data-stu-id="87beb-110">Items such as IPM.Sharing and IPM.InfoPath are returned as [Message](message-ex15websvcsotherref.md) elements.</span></span> <span data-ttu-id="87beb-111">Exchange 不会在响应中返回基本[项目](item.md)元素。</span><span class="sxs-lookup"><span data-stu-id="87beb-111">Exchange does not return the base [Item](item.md) element in responses.</span></span> 
  
<span data-ttu-id="87beb-112">**GetItem**操作不会返回附件。</span><span class="sxs-lookup"><span data-stu-id="87beb-112">The **GetItem** operation does not return attachments.</span></span> <span data-ttu-id="87beb-113">它会返回有关附加项或文件的元数据。</span><span class="sxs-lookup"><span data-stu-id="87beb-113">It does return metadata about an attached item or file.</span></span> <span data-ttu-id="87beb-114">若要返回附件，请使用[GetAttachment 操作](getattachment-operation.md)。</span><span class="sxs-lookup"><span data-stu-id="87beb-114">To return an attachment, use the [GetAttachment operation](getattachment-operation.md).</span></span>
  
## <a name="getitem-operation-soap-headers"></a><span data-ttu-id="87beb-115">GetItem 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="87beb-115">GetItem operation SOAP headers</span></span>

<span data-ttu-id="87beb-116">**GetItem**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="87beb-116">The **GetItem** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="87beb-117">标头 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="87beb-117">\*\*\*\*Header\*\*\*\*</span></span>|<span data-ttu-id="87beb-118">\*\*\*\*Element\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="87beb-118">\*\*\*\*Element\*\*\*\*</span></span>|<span data-ttu-id="87beb-119">\*\*\*\*说明\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="87beb-119">\*\*\*\*Description\*\*\*\*</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="87beb-120">**DateTimePrecision**</span><span class="sxs-lookup"><span data-stu-id="87beb-120">**DateTimePrecision**</span></span> <br/> |[<span data-ttu-id="87beb-121">DateTimePrecision</span><span class="sxs-lookup"><span data-stu-id="87beb-121">DateTimePrecision</span></span>](datetimeprecision.md) <br/> |<span data-ttu-id="87beb-122">指定对来自服务器的响应中的数据/时间值的解析（以秒或毫秒为单位）。</span><span class="sxs-lookup"><span data-stu-id="87beb-122">Specifies the resolution of data/time values in responses from the server, either in seconds or in milliseconds.</span></span>  <br/> |
|<span data-ttu-id="87beb-123">**模拟**</span><span class="sxs-lookup"><span data-stu-id="87beb-123">**Impersonation**</span></span> <br/> |[<span data-ttu-id="87beb-124">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="87beb-124">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="87beb-125">标识客户端应用程序模拟的用户。</span><span class="sxs-lookup"><span data-stu-id="87beb-125">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="87beb-126">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="87beb-126">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="87beb-127">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="87beb-127">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="87beb-128">确定用于访问邮箱的区域性（如 RFC 3066 中定义的用于标识语言的标记）。</span><span class="sxs-lookup"><span data-stu-id="87beb-128">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span>  <br/> |
|<span data-ttu-id="87beb-129">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="87beb-129">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="87beb-130">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="87beb-130">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="87beb-131">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="87beb-131">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="87beb-132">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="87beb-132">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="87beb-133">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="87beb-133">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="87beb-134">标识响应请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="87beb-134">Identifies the version of the server that responded to the request.</span></span>  <br/> |
|<span data-ttu-id="87beb-135">**TimeZoneContext**</span><span class="sxs-lookup"><span data-stu-id="87beb-135">**TimeZoneContext**</span></span> <br/> |[<span data-ttu-id="87beb-136">TimeZoneContext</span><span class="sxs-lookup"><span data-stu-id="87beb-136">TimeZoneContext</span></span>](timezonecontext.md) <br/> |<span data-ttu-id="87beb-137">标识要用于来自服务器的所有响应的时区。</span><span class="sxs-lookup"><span data-stu-id="87beb-137">Identifies the time zone to be used for all responses from the server.</span></span>  <br/> |
   
## <a name="in-this-section"></a><span data-ttu-id="87beb-138">本部分内容</span><span class="sxs-lookup"><span data-stu-id="87beb-138">In This Section</span></span>

[<span data-ttu-id="87beb-139">GetItem 操作（电子邮件）</span><span class="sxs-lookup"><span data-stu-id="87beb-139">GetItem operation (email message)</span></span>](getitem-operation-email-message.md)
  
[<span data-ttu-id="87beb-140">GetItem 操作（日历项目）</span><span class="sxs-lookup"><span data-stu-id="87beb-140">GetItem operation (calendar item)</span></span>](getitem-operation-calendar-item.md)
  
[<span data-ttu-id="87beb-141">GetItem 操作（任务）</span><span class="sxs-lookup"><span data-stu-id="87beb-141">GetItem operation (task)</span></span>](getitem-operation-task.md)
  
[<span data-ttu-id="87beb-142">GetItem 操作（联系人）</span><span class="sxs-lookup"><span data-stu-id="87beb-142">GetItem operation (contact)</span></span>](getitem-operation-contact.md)
  
## <a name="see-also"></a><span data-ttu-id="87beb-143">另请参阅</span><span class="sxs-lookup"><span data-stu-id="87beb-143">See also</span></span>



[<span data-ttu-id="87beb-144">Exchange 的 EWS 引用</span><span class="sxs-lookup"><span data-stu-id="87beb-144">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)

