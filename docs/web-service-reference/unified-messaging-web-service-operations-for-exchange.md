---
title: Exchange 的统一消息 web 服务操作
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
description: 查找 Exchange 中的统一消息 web 服务操作的参考信息。
ms.openlocfilehash: b13ca2fbc44846db0bc98b3961916ba5d0872310
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529712"
---
# <a name="unified-messaging-web-service-operations-for-exchange"></a><span data-ttu-id="e62dc-103">Exchange 的统一消息 web 服务操作</span><span class="sxs-lookup"><span data-stu-id="e62dc-103">Unified Messaging web service operations for Exchange</span></span>

<span data-ttu-id="e62dc-104">查找 Exchange 中的统一消息 web 服务操作的参考信息。</span><span class="sxs-lookup"><span data-stu-id="e62dc-104">Find reference information for the Unified Messaging web service operations in Exchange.</span></span>
  
<span data-ttu-id="e62dc-105">统一消息 web 服务提供了许多操作，使客户端应用程序能够读取和更改统一消息属性、播放语音邮件、录制问候语，并通过电话设备听写邮箱项目。</span><span class="sxs-lookup"><span data-stu-id="e62dc-105">The Unified Messaging web service provides many operations that enable client applications to read and change Unified Messaging properties, play voice mail messages, record greetings, and dictate mailbox items over telephony devices.</span></span> <span data-ttu-id="e62dc-106">本节中的文章提供有关操作的请求和响应消息的整体结构的信息。</span><span class="sxs-lookup"><span data-stu-id="e62dc-106">The articles in this section provide information about the overall structure of the request and response messages for the operations.</span></span> <span data-ttu-id="e62dc-107">这些文章提供了显示常见邮件结构的示例。</span><span class="sxs-lookup"><span data-stu-id="e62dc-107">These articles provide examples that show common message structures.</span></span> <span data-ttu-id="e62dc-108">您可以使用这些示例了解使用统一消息 web 服务请求可以执行的操作。</span><span class="sxs-lookup"><span data-stu-id="e62dc-108">You can use these examples to learn about what you can do with a Unified Messaging web service request.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e62dc-109">对于从 Exchange 2010 开始的 Exchange 版本，建议使用[Exchange Web 服务（EWS）](https://msdn.microsoft.com/library/60285497-0c4e-4e51-84e1-34dd6d89a5d8%28Office.15%29.aspx)而不是统一消息 Web 服务中提供的统一消息操作，原因如下：</span><span class="sxs-lookup"><span data-stu-id="e62dc-109">For versions of Exchange starting with Exchange 2010, we recommend that you use the Unified Messaging operations that are available in [Exchange Web Services (EWS)](https://msdn.microsoft.com/library/60285497-0c4e-4e51-84e1-34dd6d89a5d8%28Office.15%29.aspx) instead of the Unified Messaging web service, for the following reasons:</span></span> 
> - <span data-ttu-id="e62dc-110">基于 EWS 的统一消息功能在 EWS 托管 API 中具有第一类支持。</span><span class="sxs-lookup"><span data-stu-id="e62dc-110">The EWS-based Unified Messaging features have first-class support in the EWS Managed API.</span></span> 
> - <span data-ttu-id="e62dc-111">在从 Exchange 2010 开始的 Exchange 版本中，会将新的统一消息功能添加到 EWS，但不会添加到统一消息 web 服务中。</span><span class="sxs-lookup"><span data-stu-id="e62dc-111">In versions of Exchange starting with Exchange 2010, new Unified Messaging features are added to EWS but not to the Unified Messaging web service.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="e62dc-112">本节内容</span><span class="sxs-lookup"><span data-stu-id="e62dc-112">In this section</span></span>
<span data-ttu-id="e62dc-113"><a name="bk_InThisSection"> </a></span><span class="sxs-lookup"><span data-stu-id="e62dc-113"><a name="bk_InThisSection"> </a></span></span>

- [<span data-ttu-id="e62dc-114">断开连接操作（UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="e62dc-114">Disconnect operation (UM web service)</span></span>](disconnect-operation-um-web-service.md)    
- [<span data-ttu-id="e62dc-115">GetCallInfo 操作（UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="e62dc-115">GetCallInfo operation (UM web service)</span></span>](getcallinfo-operation-um-web-service.md)   
- [<span data-ttu-id="e62dc-116">GetUMProperties 操作（UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="e62dc-116">GetUMProperties operation (UM web service)</span></span>](getumproperties-operation-um-web-service.md)   
- [<span data-ttu-id="e62dc-117">IsUMEnabled 操作（UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="e62dc-117">IsUMEnabled operation (UM web service)</span></span>](isumenabled-operation-um-web-service.md)   
- [<span data-ttu-id="e62dc-118">PlayOnPhone 操作（UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="e62dc-118">PlayOnPhone operation (UM web service)</span></span>](playonphone-operation-um-web-service.md)   
- [<span data-ttu-id="e62dc-119">PlayOnPhoneGreeting 操作（UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="e62dc-119">PlayOnPhoneGreeting operation (UM web service)</span></span>](playonphonegreeting-operation-um-web-service.md)   
- [<span data-ttu-id="e62dc-120">ResetPIN 操作（UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="e62dc-120">ResetPIN operation (UM web service)</span></span>](resetpin-operation-um-web-service.md)   
- [<span data-ttu-id="e62dc-121">SetMissedCallNotificationEnabled 操作（UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="e62dc-121">SetMissedCallNotificationEnabled operation (UM web service)</span></span>](setmissedcallnotificationenabled-operation-um-web-service.md)  
- [<span data-ttu-id="e62dc-122">SetOofStatus 操作（UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="e62dc-122">SetOofStatus operation (UM web service)</span></span>](setoofstatus-operation-um-web-service.md)    
- [<span data-ttu-id="e62dc-123">SetPlayOnPhoneDialString 操作（UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="e62dc-123">SetPlayOnPhoneDialString operation (UM web service)</span></span>](setplayonphonedialstring-operation-um-web-service.md)   
- [<span data-ttu-id="e62dc-124">SetTelephoneAccessFolderEmail 操作（UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="e62dc-124">SetTelephoneAccessFolderEmail operation (UM web service)</span></span>](settelephoneaccessfolderemail-operation-um-web-service.md)
    
## <a name="see-also"></a><span data-ttu-id="e62dc-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e62dc-125">See also</span></span>

- [<span data-ttu-id="e62dc-126">Exchange 的统一消息 web 服务参考</span><span class="sxs-lookup"><span data-stu-id="e62dc-126">Unified Messaging web service reference for Exchange</span></span>](unified-messaging-web-service-reference-for-exchange.md)
- [<span data-ttu-id="e62dc-127">Exchange 自动发现</span><span class="sxs-lookup"><span data-stu-id="e62dc-127">Autodiscover for Exchange</span></span>](../exchange-web-services/autodiscover-for-exchange.md)
- [<span data-ttu-id="e62dc-128">Start using web services in Exchange</span><span class="sxs-lookup"><span data-stu-id="e62dc-128">Start using web services in Exchange</span></span>](../exchange-web-services/start-using-web-services-in-exchange.md)
    

