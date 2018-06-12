---
title: GetItem Operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetItem
api_type:
- schema
ms.assetid: e3590b8b-c2a7-4dad-a014-6360197b68e4
description: 查找信息执行 GetItem EWS 操作。
ms.openlocfilehash: 9b63032b2eaa3bf26027a42e38bfa06bedcbac86
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754602"
---
# <a name="getitem-operation"></a><span data-ttu-id="40489-103">GetItem Operation</span><span class="sxs-lookup"><span data-stu-id="40489-103">GetItem operation</span></span>

<span data-ttu-id="40489-104">查找有关**GetItem** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="40489-104">Find information about the **GetItem** EWS operation.</span></span> 
  
<span data-ttu-id="40489-105">**GetItem**操作获取从 Exchange 存储的项。</span><span class="sxs-lookup"><span data-stu-id="40489-105">The **GetItem** operation gets items from the Exchange store.</span></span> 
  
## <a name="using-the-getitem-operation"></a><span data-ttu-id="40489-106">使用 GetItem 操作</span><span class="sxs-lookup"><span data-stu-id="40489-106">Using the GetItem operation</span></span>

<span data-ttu-id="40489-107">**GetItem**操作返回许多项属性。</span><span class="sxs-lookup"><span data-stu-id="40489-107">The **GetItem** operation returns many item properties.</span></span> <span data-ttu-id="40489-108">**GetItem**响应中返回的属性有所不同，根据该请求的形状，返回请求的其他属性，和项目类型。</span><span class="sxs-lookup"><span data-stu-id="40489-108">The properties that are returned in a **GetItem** response vary based on the requested shape, requested additional properties, and the type of item returned.</span></span> 
  
<span data-ttu-id="40489-109">[消息](message-ex15websvcsotherref.md)元素表示电子邮件和非 Exchange Web Services (EWS) 架构的强类型的所有其他项目。</span><span class="sxs-lookup"><span data-stu-id="40489-109">[Message](message-ex15websvcsotherref.md) elements represent email messages and all other items that are not strongly typed by the Exchange Web Services (EWS) schema.</span></span> <span data-ttu-id="40489-110">如 IPM 的项目。共享和[消息](message-ex15websvcsotherref.md)元素以返回 IPM.InfoPath。</span><span class="sxs-lookup"><span data-stu-id="40489-110">Items such as IPM.Sharing and IPM.InfoPath are returned as [Message](message-ex15websvcsotherref.md) elements.</span></span> <span data-ttu-id="40489-111">Exchange 不在响应中返回基本的[Item](item.md)元素。</span><span class="sxs-lookup"><span data-stu-id="40489-111">Exchange does not return the base [Item](item.md) element in responses.</span></span> 
  
<span data-ttu-id="40489-112">**GetItem**操作不会返回附件。</span><span class="sxs-lookup"><span data-stu-id="40489-112">The **GetItem** operation does not return attachments.</span></span> <span data-ttu-id="40489-113">它确实返回有关的附加的项或文件的元数据。</span><span class="sxs-lookup"><span data-stu-id="40489-113">It does return metadata about an attached item or file.</span></span> <span data-ttu-id="40489-114">若要返回附件，请使用[GetAttachment 操作](getattachment-operation.md)。</span><span class="sxs-lookup"><span data-stu-id="40489-114">To return an attachment, use the [GetAttachment operation](getattachment-operation.md).</span></span>
  
## <a name="getitem-operation-soap-headers"></a><span data-ttu-id="40489-115">GetItem 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="40489-115">GetItem operation SOAP headers</span></span>

<span data-ttu-id="40489-116">**GetItem**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="40489-116">The **GetItem** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="40489-117">标头 \*\*\*</span><span class="sxs-lookup"><span data-stu-id="40489-117">****Header****</span></span>|<span data-ttu-id="40489-118">****Element****</span><span class="sxs-lookup"><span data-stu-id="40489-118">****Element****</span></span>|<span data-ttu-id="40489-119">****说明****</span><span class="sxs-lookup"><span data-stu-id="40489-119">****Description****</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="40489-120">**DateTimePrecision**</span><span class="sxs-lookup"><span data-stu-id="40489-120">**DateTimePrecision**</span></span> <br/> |[<span data-ttu-id="40489-121">DateTimePrecision</span><span class="sxs-lookup"><span data-stu-id="40489-121">DateTimePrecision</span></span>](datetimeprecision.md) <br/> |<span data-ttu-id="40489-122">指定在从服务器中，以秒为单位，或以毫秒为单位的响应中的数据/时间值的分辨率。</span><span class="sxs-lookup"><span data-stu-id="40489-122">Specifies the resolution of data/time values in responses from the server, either in seconds or in milliseconds.</span></span>  <br/> |
|<span data-ttu-id="40489-123">**模拟**</span><span class="sxs-lookup"><span data-stu-id="40489-123">**Impersonation**</span></span> <br/> |[<span data-ttu-id="40489-124">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="40489-124">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="40489-125">标识模拟客户端应用程序的用户。</span><span class="sxs-lookup"><span data-stu-id="40489-125">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="40489-126">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="40489-126">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="40489-127">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="40489-127">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="40489-128">定义 RFC 3066 中，"标记的标识的语言"，以用于访问邮箱标识与的区域性。</span><span class="sxs-lookup"><span data-stu-id="40489-128">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span>  <br/> |
|<span data-ttu-id="40489-129">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="40489-129">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="40489-130">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="40489-130">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="40489-131">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="40489-131">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="40489-132">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="40489-132">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="40489-133">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="40489-133">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="40489-134">标识响应该请求的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="40489-134">Identifies the version of the server that responded to the request.</span></span>  <br/> |
|<span data-ttu-id="40489-135">**TimeZoneContext**</span><span class="sxs-lookup"><span data-stu-id="40489-135">**TimeZoneContext**</span></span> <br/> |[<span data-ttu-id="40489-136">TimeZoneContext</span><span class="sxs-lookup"><span data-stu-id="40489-136">TimeZoneContext</span></span>](timezonecontext.md) <br/> |<span data-ttu-id="40489-137">确定要用于来自服务器的所有响应的时区。</span><span class="sxs-lookup"><span data-stu-id="40489-137">Identifies the time zone to be used for all responses from the server.</span></span>  <br/> |
   
## <a name="in-this-section"></a><span data-ttu-id="40489-138">本部分内容</span><span class="sxs-lookup"><span data-stu-id="40489-138">In This Section</span></span>

[<span data-ttu-id="40489-139">GetItem 操作 （电子邮件）</span><span class="sxs-lookup"><span data-stu-id="40489-139">GetItem operation (email message)</span></span>](getitem-operation-email-message.md)
  
[<span data-ttu-id="40489-140">GetItem 操作 （日历项）</span><span class="sxs-lookup"><span data-stu-id="40489-140">GetItem operation (calendar item)</span></span>](getitem-operation-calendar-item.md)
  
[<span data-ttu-id="40489-141">GetItem 操作 （任务）</span><span class="sxs-lookup"><span data-stu-id="40489-141">GetItem operation (task)</span></span>](getitem-operation-task.md)
  
[<span data-ttu-id="40489-142">GetItem 操作 （联系人）</span><span class="sxs-lookup"><span data-stu-id="40489-142">GetItem operation (contact)</span></span>](getitem-operation-contact.md)
  
## <a name="see-also"></a><span data-ttu-id="40489-143">另请参阅</span><span class="sxs-lookup"><span data-stu-id="40489-143">See also</span></span>



[<span data-ttu-id="40489-144">Exchange 的 EWS 引用</span><span class="sxs-lookup"><span data-stu-id="40489-144">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)

