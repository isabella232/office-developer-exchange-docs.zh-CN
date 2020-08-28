---
title: 在 Exchange 中的模拟和 EWS
manager: sethgros
ms.date: 08/24/2020
ms.audience: Developer
ms.assetid: 7e1ea63c-eb29-43d2-827f-2f2b1846483b
description: 了解如何以及何时在 Exchange 服务应用程序中使用模拟。
localization_priority: Priority
ms.openlocfilehash: da35fb04f316c21a1c85c71b789b7f1485653466
ms.sourcegitcommit: 636c05a929279812c6ef87d75b01c166a4a05584
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/26/2020
ms.locfileid: "47254970"
---
# <a name="impersonation-and-ews-in-exchange"></a>在 Exchange 中的模拟和 EWS

了解如何以及何时在 Exchange [服务应用程序](ews-application-types.md)中使用模拟。
  
可通过以下三种方式之一使用户能够访问其他用户的邮箱：
  
- 为每个代理添加代理并指定权限。
    
- 直接修改文件夹权限。
    
- 使用模拟。
    
何时应选择模拟，而不是代理或者或文件夹权限呢？ 以下准则将帮助你确定：
  
- 如果想要为用户提供对文件夹的访问权限，但不希望用户拥有“代表某人发送”的权限，请使用文件夹权限。 
    
- 当你想给一个用户代表其他用户执行工作的权限时，请使用代理访问权限。 通常情况下，这是一对一或一对多的权限，例如，单一管理助手管理管理员的日历，或单一分组讨论室计划程序管理一组会议室的日历。
    
- 如果服务应用程序需要访问多个邮箱并“充当”邮箱的所有者，请使用模拟。
    
当你处理多个邮箱时，模拟是最佳选择，因为你可以轻松地对一个服务帐户授予对数据库中每个邮箱的访问权限。 代理和文件夹权限最适用于仅授予几个用户访问权限的情况，因为你必须对每个邮箱单独添加权限。 图 1 显示了每种类型的访问权限之间的一些差异。
  
**图 1。访问其他用户邮箱的方式**

![显示邮箱访问类型、邮箱所有者与每种类型的委派之间的关系以及权限类型的图表。代表委派权限和/或文件夹权限发送。用于模拟的发送身份权限。](media/Ex15_Delegate_Overview.png)
  
模拟非常适用于连接到 Exchange Online 的应用程序、作为 Office 365 一部分的 Exchange Online 和本地版本的 Exchange ，以及执行操作（例如，存档电子邮件、为休假的用户自动设置外出，或任何需要应用程序充当邮箱所有者的其他任务）。 如果应用程序使用模拟发送邮件，则电子邮件将看起来像是由邮箱所有者发送。 收件人无法知道该邮件是由服务帐户发送的。 另一方面，代理则可向另一个邮箱帐户授予代表邮箱所有者操作的权限。 当代理发送电子邮件时，“发件人”值将标识邮箱所有者，并且“发送者”值将标识发送邮件的代理。 
  
## <a name="security-considerations-for-impersonation"></a>模拟的安全注意事项

模拟使呼叫者能够模拟给定的用户帐户。 这使呼叫者能够使用与模拟帐户相关联的权限来执行操作，而不是与呼叫者帐户相关联的权限。 因此，应注意以下安全注意事项：
  
- 只有 Exchange 服务器管理员授予 **ApplicationImpersonation** 角色的帐户可以使用模拟。 
    
- 你应该创建管理范围，限制只有指定帐户组可以使用模拟。 如果未创建管理范围，则 **ApplicationImpersonation** 角色会被授予组织中的所有帐户。 
    
- 通常情况下， **ApplicationImpersonation** 角色会被授予专用于特定应用程序或应用程序组的服务帐户，而不是用户帐户。 你可以根据需要创建多个或少个服务帐户。 
    
你可以阅读有关 [配置模拟](how-to-configure-impersonation.md)的详细信息，但应与 Exchange 管理员合作，确保你使用 [权限和访问](https://technet.microsoft.com/library/dd351175%28v=exchg.150%29.aspx) 来创建需要的且能满足组织安全要求的服务账户。 
  
## <a name="in-this-section"></a>本节内容

- [配置模拟](how-to-configure-impersonation.md)
    
- [标识要模拟的帐户](how-to-identify-the-account-to-impersonate.md)
    
- [使用 Exchange 模拟添加约会](how-to-add-appointments-by-using-exchange-impersonation.md)

## <a name="performance-considerations-for-ews-impersonation"></a>EWS 模拟的性能注意事项

使用 EWS 模拟时，应始终正确设置 X-AnchorMailbox。  否则，可能会时不时收到错误消息 500 或 503。 这对于 Exchange Online/Exchange 2013 的性能和通知是至关重要的。  不设置的话可能会用上两倍或更长的时间来完成调用。 在某些情况下，你还可能会超时。 
    
## <a name="see-also"></a>另请参阅


- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)
    
- [Exchange 中的代理访问和 EWS](delegate-access-and-ews-in-exchange.md)
    
- [Exchange 2013 权限](https://technet.microsoft.com/library/dd351175%28v=exchg.150%29.aspx)
    

