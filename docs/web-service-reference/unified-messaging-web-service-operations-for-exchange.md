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
ms.openlocfilehash: bd86a4ab2de58e5f04a8d37f17196040bcf38b97
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354356"
---
# <a name="unified-messaging-web-service-operations-for-exchange"></a><span data-ttu-id="36711-103">Exchange 统一的消息 web 服务操作</span><span class="sxs-lookup"><span data-stu-id="36711-103">Unified Messaging web service operations for Exchange</span></span>

<span data-ttu-id="36711-104">在 Exchange 中查找的统一消息 web 服务操作的参考信息。</span><span class="sxs-lookup"><span data-stu-id="36711-104">Find reference information for the Unified Messaging web service operations in Exchange.</span></span>
  
<span data-ttu-id="36711-105">统一消息 web 服务提供了许多使客户端应用程序能够读取和更改统一消息属性、 播放语音邮件、 录制问候语，和通过电话设备规定的邮箱项目的操作。</span><span class="sxs-lookup"><span data-stu-id="36711-105">The Unified Messaging web service provides many operations that enable client applications to read and change Unified Messaging properties, play voice mail messages, record greetings, and dictate mailbox items over telephony devices.</span></span> <span data-ttu-id="36711-106">本节中的文章提供有关操作的请求和响应消息的总体结构的信息。</span><span class="sxs-lookup"><span data-stu-id="36711-106">The articles in this section provide information about the overall structure of the request and response messages for the operations.</span></span> <span data-ttu-id="36711-107">这些文章提供显示常见消息结构的示例。</span><span class="sxs-lookup"><span data-stu-id="36711-107">These articles provide examples that show common message structures.</span></span> <span data-ttu-id="36711-108">这些示例用于了解有关可以与统一消息 web 服务请求执行的操作。</span><span class="sxs-lookup"><span data-stu-id="36711-108">You can use these examples to learn about what you can do with a Unified Messaging web service request.</span></span>
  
> [!NOTE]
> <span data-ttu-id="36711-109">启动与 Exchange 2010 的 Exchange 版本，我们建议您使用统一消息操作所提供的[Exchange Web Services (EWS)](http://msdn.microsoft.com/library/60285497-0c4e-4e51-84e1-34dd6d89a5d8%28Office.15%29.aspx)而不是统一消息 web 服务，原因如下：</span><span class="sxs-lookup"><span data-stu-id="36711-109">For versions of Exchange starting with Exchange 2010, we recommend that you use the Unified Messaging operations that are available in [Exchange Web Services (EWS)](http://msdn.microsoft.com/library/60285497-0c4e-4e51-84e1-34dd6d89a5d8%28Office.15%29.aspx) instead of the Unified Messaging web service, for the following reasons:</span></span> 
> - <span data-ttu-id="36711-110">基于 EWS 的统一消息功能具有 EWS 托管 API 的一流支持。</span><span class="sxs-lookup"><span data-stu-id="36711-110">The EWS-based Unified Messaging features have first-class support in the EWS Managed API.</span></span> 
> - <span data-ttu-id="36711-111">在版本的 Exchange 启动与 Exchange 2010，EWS 但不是到统一消息 web 服务添加新的统一消息功能。</span><span class="sxs-lookup"><span data-stu-id="36711-111">In versions of Exchange starting with Exchange 2010, new Unified Messaging features are added to EWS but not to the Unified Messaging web service.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="36711-112">本节内容</span><span class="sxs-lookup"><span data-stu-id="36711-112">In this section</span></span>
<span data-ttu-id="36711-113"><a name="bk_InThisSection"> </a></span><span class="sxs-lookup"><span data-stu-id="36711-113"></span></span>

- [<span data-ttu-id="36711-114">Disconnect 操作（UM Web 服务）</span><span class="sxs-lookup"><span data-stu-id="36711-114">Disconnect operation (UM web service)</span></span>](disconnect-operation-um-web-service.md)    
- [<span data-ttu-id="36711-115">GetCallInfo 操作（UM Web 服务）</span><span class="sxs-lookup"><span data-stu-id="36711-115">GetCallInfo operation (UM web service)</span></span>](getcallinfo-operation-um-web-service.md)   
- [<span data-ttu-id="36711-116">GetUMProperties 操作（UM Web 服务）</span><span class="sxs-lookup"><span data-stu-id="36711-116">GetUMProperties operation (UM web service)</span></span>](getumproperties-operation-um-web-service.md)   
- [<span data-ttu-id="36711-117">IsUMEnabled 操作（UM Web 服务）</span><span class="sxs-lookup"><span data-stu-id="36711-117">IsUMEnabled operation (UM web service)</span></span>](isumenabled-operation-um-web-service.md)   
- [<span data-ttu-id="36711-118">PlayOnPhone 操作（UM Web 服务）</span><span class="sxs-lookup"><span data-stu-id="36711-118">PlayOnPhone operation (UM web service)</span></span>](playonphone-operation-um-web-service.md)   
- [<span data-ttu-id="36711-119">PlayOnPhoneGreeting 操作（UM Web 服务）</span><span class="sxs-lookup"><span data-stu-id="36711-119">PlayOnPhoneGreeting operation (UM web service)</span></span>](playonphonegreeting-operation-um-web-service.md)   
- [<span data-ttu-id="36711-120">ResetPIN 操作（UM Web 服务）</span><span class="sxs-lookup"><span data-stu-id="36711-120">ResetPIN operation (UM web service)</span></span>](resetpin-operation-um-web-service.md)   
- [<span data-ttu-id="36711-121">SetMissedCallNotificationEnabled 操作（UM Web 服务）</span><span class="sxs-lookup"><span data-stu-id="36711-121">SetMissedCallNotificationEnabled operation (UM web service)</span></span>](setmissedcallnotificationenabled-operation-um-web-service.md)  
- [<span data-ttu-id="36711-122">SetOofStatus 操作（UM Web 服务）</span><span class="sxs-lookup"><span data-stu-id="36711-122">SetOofStatus operation (UM web service)</span></span>](setoofstatus-operation-um-web-service.md)    
- [<span data-ttu-id="36711-123">SetPlayOnPhoneDialString 操作（UM Web 服务）</span><span class="sxs-lookup"><span data-stu-id="36711-123">SetPlayOnPhoneDialString operation (UM web service)</span></span>](setplayonphonedialstring-operation-um-web-service.md)   
- [<span data-ttu-id="36711-124">SetTelephoneAccessFolderEmail 操作（UM Web 服务）</span><span class="sxs-lookup"><span data-stu-id="36711-124">SetTelephoneAccessFolderEmail operation (UM web service)</span></span>](settelephoneaccessfolderemail-operation-um-web-service.md)
    
## <a name="see-also"></a><span data-ttu-id="36711-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="36711-125">See also</span></span>

- [<span data-ttu-id="36711-126">Exchange 统一的消息 web 服务引用</span><span class="sxs-lookup"><span data-stu-id="36711-126">Unified Messaging web service reference for Exchange</span></span>](unified-messaging-web-service-reference-for-exchange.md)
- [<span data-ttu-id="36711-127">Exchange 自动发现</span><span class="sxs-lookup"><span data-stu-id="36711-127">Autodiscover for Exchange</span></span>](../exchange-web-services/autodiscover-for-exchange.md)
- [<span data-ttu-id="36711-128">Start using web services in Exchange</span><span class="sxs-lookup"><span data-stu-id="36711-128">Start using web services in Exchange</span></span>](../exchange-web-services/start-using-web-services-in-exchange.md)
    

