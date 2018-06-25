---
title: Exchange 统一的消息 web 服务操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- Unified
api_type:
- schema
ms.assetid: d92455bd-24e8-4255-9f93-2bdeff00d42d
description: 在 Exchange 中查找的统一消息 web 服务操作的参考信息。
ms.openlocfilehash: 21d3469d752ff6cdca4ed4ea9151daca52d51e9f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838311"
---
# <a name="unified-messaging-web-service-operations-for-exchange"></a><span data-ttu-id="afeee-103">Exchange 统一的消息 web 服务操作</span><span class="sxs-lookup"><span data-stu-id="afeee-103">Unified Messaging web service operations for Exchange</span></span>

<span data-ttu-id="afeee-104">在 Exchange 中查找的统一消息 web 服务操作的参考信息。</span><span class="sxs-lookup"><span data-stu-id="afeee-104">Find reference information for the Unified Messaging web service operations in Exchange.</span></span>
  
<span data-ttu-id="afeee-105">统一消息 web 服务提供了许多使客户端应用程序能够读取和更改统一消息属性、 播放语音邮件、 录制问候语，和通过电话设备规定的邮箱项目的操作。</span><span class="sxs-lookup"><span data-stu-id="afeee-105">The Unified Messaging web service provides many operations that enable client applications to read and change Unified Messaging properties, play voice mail messages, record greetings, and dictate mailbox items over telephony devices.</span></span> <span data-ttu-id="afeee-106">本节中的文章提供有关操作的请求和响应消息的总体结构的信息。</span><span class="sxs-lookup"><span data-stu-id="afeee-106">The articles in this section provide information about the overall structure of the request and response messages for the operations.</span></span> <span data-ttu-id="afeee-107">这些文章提供显示常见消息结构的示例。</span><span class="sxs-lookup"><span data-stu-id="afeee-107">These articles provide examples that show common message structures.</span></span> <span data-ttu-id="afeee-108">这些示例用于了解有关可以与统一消息 web 服务请求执行的操作。</span><span class="sxs-lookup"><span data-stu-id="afeee-108">You can use these examples to learn about what you can do with a Unified Messaging web service request.</span></span>
  
> [!NOTE]
>  <span data-ttu-id="afeee-109">启动与 Exchange 2010 的 Exchange 版本，我们建议您使用统一消息操作所提供的[Exchange Web Services (EWS)](http://msdn.microsoft.com/library/60285497-0c4e-4e51-84e1-34dd6d89a5d8%28Office.15%29.aspx)而不是统一消息 web 服务，原因如下： > 基于 EWS统一的消息功能具有 EWS 托管 API 中的第一类的支持。</span><span class="sxs-lookup"><span data-stu-id="afeee-109">For versions of Exchange starting with Exchange 2010, we recommend that you use the Unified Messaging operations that are available in [Exchange Web Services (EWS)](http://msdn.microsoft.com/library/60285497-0c4e-4e51-84e1-34dd6d89a5d8%28Office.15%29.aspx) instead of the Unified Messaging web service, for the following reasons: >  The EWS-based Unified Messaging features have first-class support in the EWS Managed API.</span></span> <span data-ttu-id="afeee-110">> 在版本的 Exchange 与 Exchange 2010 开始，到 EWS 但不是到统一消息 web 服务添加新的统一消息功能。</span><span class="sxs-lookup"><span data-stu-id="afeee-110">>  In versions of Exchange starting with Exchange 2010, new Unified Messaging features are added to EWS but not to the Unified Messaging web service.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="afeee-111">本节内容</span><span class="sxs-lookup"><span data-stu-id="afeee-111">In this section</span></span>
<span data-ttu-id="afeee-112"><a name="bk_InThisSection"> </a></span><span class="sxs-lookup"><span data-stu-id="afeee-112"></span></span>

- [<span data-ttu-id="afeee-113">断开连接操作 （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="afeee-113">Disconnect operation (UM web service)</span></span>](disconnect-operation-um-web-service.md)
    
- [<span data-ttu-id="afeee-114">GetCallInfo 操作 （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="afeee-114">GetCallInfo operation (UM web service)</span></span>](getcallinfo-operation-um-web-service.md)
    
- [<span data-ttu-id="afeee-115">GetUMProperties 操作 （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="afeee-115">GetUMProperties operation (UM web service)</span></span>](getumproperties-operation-um-web-service.md)
    
- [<span data-ttu-id="afeee-116">IsUMEnabled 操作 （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="afeee-116">IsUMEnabled operation (UM web service)</span></span>](isumenabled-operation-um-web-service.md)
    
- [<span data-ttu-id="afeee-117">PlayOnPhone 操作 （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="afeee-117">PlayOnPhone operation (UM web service)</span></span>](playonphone-operation-um-web-service.md)
    
- [<span data-ttu-id="afeee-118">PlayOnPhoneGreeting 操作 （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="afeee-118">PlayOnPhoneGreeting operation (UM web service)</span></span>](playonphonegreeting-operation-um-web-service.md)
    
- [<span data-ttu-id="afeee-119">ResetPIN 操作 （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="afeee-119">ResetPIN operation (UM web service)</span></span>](resetpin-operation-um-web-service.md)
    
- [<span data-ttu-id="afeee-120">SetMissedCallNotificationEnabled 操作 （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="afeee-120">SetMissedCallNotificationEnabled operation (UM web service)</span></span>](setmissedcallnotificationenabled-operation-um-web-service.md)
    
- [<span data-ttu-id="afeee-121">SetOofStatus 操作 （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="afeee-121">SetOofStatus operation (UM web service)</span></span>](setoofstatus-operation-um-web-service.md)
    
- [<span data-ttu-id="afeee-122">SetPlayOnPhoneDialString 操作 （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="afeee-122">SetPlayOnPhoneDialString operation (UM web service)</span></span>](setplayonphonedialstring-operation-um-web-service.md)
    
- [<span data-ttu-id="afeee-123">SetTelephoneAccessFolderEmail 操作 （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="afeee-123">SetTelephoneAccessFolderEmail operation (UM web service)</span></span>](settelephoneaccessfolderemail-operation-um-web-service.md)
    
## <a name="see-also"></a><span data-ttu-id="afeee-124">另请参阅</span><span class="sxs-lookup"><span data-stu-id="afeee-124">See also</span></span>

- [<span data-ttu-id="afeee-125">Exchange 统一的消息 web 服务引用</span><span class="sxs-lookup"><span data-stu-id="afeee-125">Unified Messaging web service reference for Exchange</span></span>](unified-messaging-web-service-reference-for-exchange.md)
- [<span data-ttu-id="afeee-126">Exchange 自动发现</span><span class="sxs-lookup"><span data-stu-id="afeee-126">Autodiscover for Exchange</span></span>](../exchange-web-services/autodiscover-for-exchange.md)
- [<span data-ttu-id="afeee-127">Start using web services in Exchange</span><span class="sxs-lookup"><span data-stu-id="afeee-127">Start using web services in Exchange</span></span>](../exchange-web-services/start-using-web-services-in-exchange.md)
    

