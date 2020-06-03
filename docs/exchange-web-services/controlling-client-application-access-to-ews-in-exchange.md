---
title: 控制对 Exchange 中的 EWS 的客户端应用程序访问
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 60ac3f7b-ba8a-4c93-99f7-c27002caff93
description: 了解用于管理对 EWS 的客户端应用程序访问的选项。
localization_priority: Priority
ms.openlocfilehash: b887b8167e3d38946b1d6caffe12655ded89569f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528459"
---
# <a name="controlling-client-application-access-to-ews-in-exchange"></a>控制对 Exchange 中的 EWS 的客户端应用程序访问

了解用于管理对 EWS 的客户端应用程序访问的选项。
  
您创建的任何 EWS 客户端应用程序都必须被授予对 Exchange Online、Exchange Online 作为 Office 365 的一部分的访问权限，或从 Exchange 2013 开始的 exchange 版本，然后才能调用 EWS 操作。 测试或生产服务器管理员可以使用 Exchange 命令行管理程序来限制所有用户和应用程序、单个用户或单个应用程序对 EWS 的访问权限。 EWS 的访问控制基于域帐户。 当使用由本地安全机构进行身份验证的凭据建立连接时，服务器将返回一个错误，指示只有域帐户可以连接。 
  
## <a name="access-control-for-ews-clients-and-users"></a>EWS 客户端和用户的访问控制
<a name="bk_configure"> </a>

您的测试或生产服务器管理员可以通过以下方式为连接到 EWS 的客户端配置访问控制： 
  
- 通过阻止所有客户端应用程序进行连接。
    
- 通过仅允许特定客户端应用程序进行连接。
    
- 允许任何客户端应用程序连接，但特别阻止的任何客户端应用程序除外。
    
- 允许任何客户端应用程序进行连接。
    
应用程序由其在 HTTP web 请求中发送的用户代理字符串进行标识。
  
> [!IMPORTANT]
> 应用程序级别的阻止不是一项安全功能。 用户代理字符串很容易被欺骗。 如果允许应用程序访问 EWS，则应用程序必须仍然存在服务器在应用程序可以连接到 EWS 之前进行身份验证的凭据。 
  
管理员还可以通过以下方式为连接到 EWS 的邮箱所有者配置访问控制： 
  
- 通过阻止或允许整个组织。
    
- 通过阻止或允许由基于角色的身份验证作用域标识的一组用户，其中包括或排除不具有 EWS 访问权限的邮箱所有者。
    
- 通过阻止或允许单个邮箱所有者。
    
特定访问控制设置将覆盖常规访问控制设置。 例如，如果组织拒绝 EWS 访问，但单个邮箱所有者允许应用程序访问，则允许单个设置 prevails 和访问。 
  
## <a name="delegation-and-ews-access-management"></a>委派和 EWS 访问管理
<a name="bk_delegation"> </a>

如果委派对 EWS 不具有访问权限的用户使用客户端应用程序，则即使主体用户具有 EWS 访问权限，也无法通过使用 EWS 访问主体用户的邮箱。 如果代理用户具有 EWS 访问权限，则该代理将能够使用您的 EWS 客户端应用程序访问主体用户的邮箱，即使主体用户不具有 EWS 访问权限也是如此。 
  
## <a name="impersonation-and-ews-access-management"></a>模拟和 EWS 访问管理
<a name="bk_impersonation"> </a>

代表邮箱所有者连接到 EWS 的客户端应用程序可能无法使用邮箱所有者的 EWS 设置。 例如，对公司的电子邮件进行存档的应用程序必须连接到 EWS，而不考虑邮箱用户的设置。 其他应用程序（如邮件客户端）必须使用邮箱所有者的 EWS 设置。 
  
管理员应为他们在其服务器上使用的每个应用程序或应用程序类创建一个模拟帐户。 这将使管理员能够为没有 EWS 权限的所有用户配置基于角色的访问控制作用域。 
  
若要启用模拟帐户，测试或生产服务器管理员应执行下列操作之一： 
  
- 将 "已通过身份验证的用户" 组添加到 "之前的 Win2K" 兼容访问组。 
    
- 将 "Exchange 服务器" 组添加到 "Windows 授权访问" 组。 
    
## <a name="exchange-management-shell-cmdlets-for-access-management"></a>用于 access management 的 Exchange 命令行管理程序 cmdlet
<a name="bk_cmdlets"> </a>

管理员使用以下 Exchange 命令行管理程序 cmdlet 来配置 EWS 访问控制： 
  
- [Get-CASMailbox](https://technet.microsoft.com/library/bb124754.aspx)   
- [Set-CASMailbox](https://technet.microsoft.com/library/bb125264.aspx)   
- [Set-organizationconfig](https://technet.microsoft.com/library/aa997571.aspx)   
- [Set-organizationconfig](https://technet.microsoft.com/library/aa997443.aspx)
    
## <a name="see-also"></a>另请参阅

- [开始使用 Exchange 中的 Web 服务](start-using-web-services-in-exchange.md)  
- [在 Exchange 中控制对 EWS 的访问](how-to-control-access-to-ews-in-exchange.md)
- [Exchange Server PowerShell （Exchange 命令行管理程序）](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)
- [Windows PowerShell](https://msdn.microsoft.com/library/dd835506%28v=vs.85%29.aspx)
    

