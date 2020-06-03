---
title: Impersonation and EWS in Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.assetid: 7e1ea63c-eb29-43d2-827f-2f2b1846483b
description: 了解如何以及何时在 Exchange 服务应用程序中使用模拟。
localization_priority: Priority
ms.openlocfilehash: 8151b3d83421786d99ee0c82eaf4f7a5c0721f25
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466610"
---
# <a name="impersonation-and-ews-in-exchange"></a>Impersonation and EWS in Exchange

了解如何以及何时在 Exchange[服务应用程序](ews-application-types.md)中使用模拟。
  
您可以通过以下三种方式之一使用户能够访问其他用户的邮箱：
  
- 通过添加委派并为每个代理指定权限。
    
- 通过直接修改文件夹权限。
    
- 通过使用模拟。
    
何时应选择模拟而不是委派或文件夹权限？ 以下指南将帮助您做出决定：
  
- 当您希望提供用户对文件夹的访问权限但不希望用户具有 "代表发送" 权限时，可使用文件夹权限。 
    
- 如果要授予一个用户代表另一个用户执行工作的权限，请使用委派访问权限。 通常情况下，这是一对一或一对一的权限，例如，管理管理员日历的单个管理助理，或者是管理一组会议室的日历的单一聊天室计划程序。
    
- 当您有需要访问多个邮箱并 "充当" 邮箱所有者的服务应用程序时，请使用模拟。
    
当您处理多个邮箱时，模拟是最佳选择，因为您可以轻松授予一个服务帐户对数据库中每个邮箱的访问权限。 委派和文件夹权限最适用于仅授予几个用户的访问权限，因为您必须将权限单独添加到每个邮箱。 图1显示了每种类型的访问权限之间的一些差异。
  
**图1。访问其他用户的邮箱的方法**

![显示邮箱访问类型、邮箱所有者与每种类型的委派之间的关系以及权限类型的图表。代表委派权限和/或文件夹权限发送。用于模拟的发送身份权限。](media/Ex15_Delegate_Overview.png)
  
模拟非常适合于连接到 Exchange Online 的应用程序、Exchange Online 作为 Office 365 的一部分以及 Exchange 的本地版本，以及执行操作（如存档电子邮件、在假期中自动为用户设置 OOF）或任何其他需要该应用程序充当邮箱所有者的任务。 当应用程序使用模拟发送邮件时，电子邮件似乎将从邮箱所有者发送。 收件人无法知道该邮件是由服务帐户发送的。 另一方面，委派将授予另一个邮箱帐户代表邮箱所有者执行操作的权限。 当代理发送电子邮件时，"发件人" 值标识邮箱所有者，"发件人" 值标识发送邮件的代理。 
  
## <a name="security-considerations-for-impersonation"></a>模拟的安全注意事项

模拟使呼叫者能够模拟给定的用户帐户。 这样，调用方可以使用与模拟帐户关联的权限（而不是与呼叫者帐户关联的权限）执行操作。 出于此原因，应注意以下安全注意事项：
  
- 只有已通过 Exchange server 管理员授予**ApplicationImpersonation**角色的帐户才能使用模拟。 
    
- 应创建将模拟限制为指定帐户组的管理作用域。 如果不创建管理作用域，则会向组织中的所有帐户授予**ApplicationImpersonation**角色。 
    
- 通常情况下， **ApplicationImpersonation**角色被授予专用于特定应用程序或应用程序组的服务帐户，而不是用户帐户。 您可以根据需要创建任意多个服务帐户。 
    
您可以阅读有关[配置模拟](how-to-configure-impersonation.md)的详细信息，但应与 Exchange 管理员合作，以确保使用符合组织的安全要求的[权限和访问权限](https://technet.microsoft.com/library/dd351175%28v=exchg.150%29.aspx)创建所需的服务帐户。 
  
## <a name="in-this-section"></a>本节内容

- [配置模拟](how-to-configure-impersonation.md)
    
- [确定要模拟的帐户](how-to-identify-the-account-to-impersonate.md)
    
- [使用 Exchange 模拟添加约会](how-to-add-appointments-by-using-exchange-impersonation.md)
    
## <a name="see-also"></a>另请参阅


- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)
    
- [代理访问和 Exchange 中的 EWS](delegate-access-and-ews-in-exchange.md)
    
- [Exchange 2013 权限](https://technet.microsoft.com/library/dd351175%28v=exchg.150%29.aspx)
    

