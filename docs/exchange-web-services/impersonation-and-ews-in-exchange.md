---
title: 模拟和 Exchange 中的 EWS
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7e1ea63c-eb29-43d2-827f-2f2b1846483b
description: 了解如何以及何时在您的 Exchange 服务应用程序中使用模拟。
ms.openlocfilehash: f8a215874475034f0d147b80a05cae414e6438f9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19752899"
---
# <a name="impersonation-and-ews-in-exchange"></a>模拟和 Exchange 中的 EWS

了解如何以及何时在您的 Exchange[服务应用程序](ews-application-types.md)中使用模拟。
  
您可以让用户能够访问其他用户的邮箱的三种方式之一：
  
- 添加代理人，并指定每个代理人的权限。
    
- 通过直接修改文件夹权限。
    
- 使用模拟。
    
何时您应通过委派或文件夹的权限中选择模拟 以下指南将帮助您决定：
  
- 当您想要提供用户访问的文件夹，但不是希望用户具有"代表发送"权限，请使用文件夹权限。 
    
- 您想要赋予一个用户的权限以执行代表另一个用户工作时使用代理访问。 通常，这是一个一对一或一个到几权限-例如，管理日历的管理员或管理一组会议室的日历的单个会议室计划单个行政助理。
    
- 需要访问多个邮箱和"作为"邮箱所有者的服务应用程序后，请使用模拟。
    
模拟时您处理与多个邮箱因为您可以轻松地一个服务帐户授予访问权限的每个邮箱数据库中的最佳选择。 委派和文件夹权限是最佳时要仅对少数用户授权访问因为您需要为每个邮箱单独添加权限。 图 1 显示了一些每种类型的访问之间的差异。
  
**图 1。方式访问其他用户的邮箱**

![显示邮箱访问类型、邮箱所有者与每种类型的委派之间的关系以及权限类型的图表。代表委派权限和/或文件夹权限发送。用于模拟的发送身份权限。](media/Ex15_Delegate_Overview.png)
  
模拟非常适合于连接到 Exchange Online 中，Exchange Online 作为 Office 365 的一部分的应用程序和本地 Exchange 版本以及执行操作，如存档电子邮件、 设置 OOF 自动用户度假或任何其他任务需要应用程序用作邮箱的所有者的。 当应用程序使用模拟时发送一条消息时，显示从邮箱所有者发送电子邮件。 没有要了解的服务帐户已发送邮件的收件人方法。 委派，另一方面，使其他邮箱帐户权限，才能代表邮箱所有者操作。 当由代理发送一封电子邮件时，"从"值标识邮箱所有者，并且"发件人"值标识已发送邮件的代理人。 
  
## <a name="security-considerations-for-impersonation"></a>模拟的安全注意事项

模拟使呼叫者可以模拟的给定的用户帐户。 这样呼叫者使用模拟的帐户，而不是与呼叫者的帐户相关联的权限与关联的权限执行操作。 因此，您应了解以下安全注意事项：
  
- 已由 Exchange 服务器管理员授予**ApplicationImpersonation**角色的帐户可以使用模拟。 
    
- 您应创建一个管理作用域限制模拟至一组指定的帐户。 如果未创建管理作用域，则**ApplicationImpersonation**角色授予在组织中的所有帐户。 
    
- 通常，**通过 ApplicationImpersonation**角色授予专用于特定应用程序或应用程序的组的服务帐户，而不是用户帐户。 您可以根据需要您可以创建多个或尽可能少的服务帐户。 
    
您可以阅读更多有关[配置模拟](how-to-configure-impersonation.md)，但您应使用您的 Exchange 管理员以确保所需的服务帐户创建的[权限和访问](http://technet.microsoft.com/en-us/library/dd351175%28v=exchg.150%29.aspx)满足的安全要求与您组织。 
  
## <a name="in-this-section"></a>本节内容

- [配置模拟](how-to-configure-impersonation.md)
    
- [确定要模拟的帐户](how-to-identify-the-account-to-impersonate.md)
    
- [使用 Exchange 模拟添加约会](how-to-add-appointments-by-using-exchange-impersonation.md)
    
## <a name="see-also"></a>另请参阅


- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)
    
- [代理访问和 Exchange 中的 EWS](delegate-access-and-ews-in-exchange.md)
    
- [Exchange 2013 权限](http://technet.microsoft.com/en-us/library/dd351175%28v=exchg.150%29.aspx)
    

