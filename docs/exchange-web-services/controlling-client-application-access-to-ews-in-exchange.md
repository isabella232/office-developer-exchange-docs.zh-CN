---
title: 在 Exchange 控制客户端应用程序访问 EWS
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 60ac3f7b-ba8a-4c93-99f7-c27002caff93
description: 了解用于管理客户端应用程序访问 EWS 的选项。
ms.openlocfilehash: e3a0e07b733b4ebc070ab6b3fc73c8aec4b62785
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353061"
---
# <a name="controlling-client-application-access-to-ews-in-exchange"></a>在 Exchange 控制客户端应用程序访问 EWS

了解用于管理客户端应用程序访问 EWS 的选项。
  
您创建任何 EWS 客户端应用程序必须授予访问 Exchange Online 中，为 Office 365 的一部分或 Exchange 版本的 Exchange Online 开头 Exchange 2013，才能调用 EWS 操作。 测试或生产服务器管理员可以使用 Exchange 命令行管理程序来限制对 EWS 的所有用户和应用程序，为各个用户，或单独的应用程序的访问。 EWS 的访问控制基于域帐户。 当使用通过本地安全机构进行身份验证的凭据进行连接时，服务器将返回一条错误，指示可以连接仅域帐户。 
  
## <a name="access-control-for-ews-clients-and-users"></a>EWS 客户端和用户的访问控制
<a name="bk_configure"> </a>

测试或生产服务器管理员可以配置为按以下方式连接到 EWS 的客户端访问控制： 
  
- 通过阻止连接的所有客户端应用程序。
    
- 通过允许特定客户端应用程序仅连接。
    
- 通过允许任何客户端应用程序连接除外明确阻止。
    
- 通过允许任何客户端应用程序连接。
    
由发送 HTTP web 请求中的用户代理字符串标识应用程序。
  
> [!IMPORTANT]
> 应用程序级阻止不是一项安全功能。 容易造假用户代理字符串。 如果 EWS 访问允许应用程序，则该应用程序必须仍提供凭据的服务器进行身份验证应用程序可以连接到 EWS 之前。 
  
管理员还可以配置为按以下方式连接到 EWS 的邮箱所有者的访问控制： 
  
- 通过阻止或允许整个组织。
    
- 通过阻止或允许一组用户标识的基于角色的身份验证的范围包含或排除是否有权访问 EWS 的邮箱所有者。
    
- 通过阻止或允许单个邮箱所有者。
    
特定的访问控制设置重写常规的访问控制设置。 例如，如果组织拒绝 EWS 访问，但允许应用程序访问各个邮箱所有者，单个设置生效，并允许访问。 
  
## <a name="delegation-and-ews-access-management"></a>委派和 EWS 访问管理
<a name="bk_delegation"> </a>

当委托用户不具有访问 EWS 使用客户端应用程序，它们将不能使用访问主体用户邮箱 EWS，即使主体用户具有 EWS 访问。 如果代理用户具有的 EWS 访问，代理将能够使用 EWS 客户端应用程序访问主体用户的邮箱，即使主体用户不具有 EWS 访问。 
  
## <a name="impersonation-and-ews-access-management"></a>模拟和 EWS 访问管理
<a name="bk_impersonation"> </a>

连接到 EWS 代表邮箱所有者的客户端应用程序可能无法使用 EWS 设置邮箱所有者。 例如，存档的应用程序电子邮件消息的公司已连接到 EWS 无论哪些邮箱用户的设置。 其他应用程序，如邮件客户端，不必要使用邮箱所有者的 EWS 设置。 
  
管理员应创建模拟帐户为每个应用程序或他们在其服务器使用的应用程序类。 这将使管理员能够配置没有 EWS 权限的所有用户的基于角色的访问控制范围。 
  
若要启用模拟帐户，测试或生产服务器管理员应执行以下任一操作： 
  
- 向之前 Win2K 兼容 Access 组添加 Authenticated Users 组。 
    
- 向 Windows 授权 Access 组添加 Exchange 服务器组。 
    
## <a name="exchange-management-shell-cmdlets-for-access-management"></a>用于访问管理 Exchange 命令行管理程序 cmdlet
<a name="bk_cmdlets"> </a>

管理员使用下面的 Exchange 命令行管理程序 cmdlet 配置 EWS 访问控制： 
  
- [Get-casmailbox](http://technet.microsoft.com/en-us/library/bb124754.aspx)   
- [设置 CASMailbox](http://technet.microsoft.com/en-us/library/bb125264.aspx)   
- [Get-organizationconfig](http://technet.microsoft.com/en-us/library/aa997571.aspx)   
- [Set-organizationconfig](http://technet.microsoft.com/en-us/library/aa997443.aspx)
    
## <a name="see-also"></a>另请参阅

- [Start using web services in Exchange](start-using-web-services-in-exchange.md)  
- [在 Exchange 控制对 EWS 的访问](how-to-control-access-to-ews-in-exchange.md)
- [Exchange Server PowerShell （Exchange 命令行管理程序）](https://docs.microsoft.com/en-us/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)
- [Windows PowerShell](http://msdn.microsoft.com/en-us/library/dd835506%28v=vs.85%29.aspx)
    

