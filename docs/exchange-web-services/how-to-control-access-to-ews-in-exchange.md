---
title: 在 Exchange 控制对 EWS 的访问
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 61e29e54-e3e5-404a-84c0-93b61a25ca58
description: 找出如何控制对 EWS 的用户、 应用程序或整个组织的访问。
ms.openlocfilehash: 956c28faba105ecf2a6b1452abe629ea2fc930e1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19752754"
---
# <a name="control-access-to-ews-in-exchange"></a>在 Exchange 控制对 EWS 的访问

找出如何控制对 EWS 的用户、 应用程序或整个组织的访问。
  
无论您使用 EWS 托管 API 或 EWS 直接在您的应用程序，您可以控制访问到 Exchange Web Services (EWS)。 如果您有到 Exchange 服务器的管理员访问权限，您可以使用 Exchange 命令行管理程序来控制访问全局，每个用户，以及每个应用程序管理对 EWS 访问。
  
## <a name="exchange-management-shell-cmdlets-for-configuring-access-control"></a>Exchange 命令行管理程序 cmdlet 配置的访问控制
<a name="bk_Cmdlets"> </a>

可以使用下面的 Exchange 命令行管理程序 cmdlet 查看当前的访问配置和设置 EWS 访问控制：
  
- [Get-casmailbox](http://technet.microsoft.com/en-us/library/bb124754.aspx) -显示哪些参数设置为特定邮箱。   
- [设置 CASMailbox](http://technet.microsoft.com/en-us/library/bb125264.aspx) -特定邮箱的设置参数。    
- [Get-organizationconfig](http://technet.microsoft.com/en-us/library/aa997571.aspx) -显示整个组织的参数。    
- [Set-organizationconfig](http://technet.microsoft.com/en-us/library/aa997443.aspx) -设置为整个组织的参数。 

<a name="bk_Examples"> </a>

## <a name="examples-controlling-access-to-ews"></a>示例： 控制对 EWS 的访问

让我们看看几个方案演示如何可以控制对您的应用程序的访问。
  
**表 1。用于控制访问 EWS 的命令**

|如果您要 |使用此命令|
|:-----|:-----|
|阻止通过 EWS 中的所有客户端应用程序。 | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceAllowList`<br/><br/>这样 AllowList 中列出的应用程序连接。 本示例中，没有应用程序中都包含 AllowList，因此没有应用程序可以使用 EWS。 |
|允许列表的客户端应用程序使用 EWS。 | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceAllowList -EwsAllowList:"OWA/*"`<br/><br/>这允许使用 EWS 特定应用程序。 本示例中，任何应用程序具有用户代理字符串的开头"OWA /"允许访问。 |
|允许所有客户端应用程序使用 EWS 除外明确阻止。 | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceBlockList -EwsBlockList:"OWA/*"`<br/> <br/>本示例仅阻止使用具有开头的用户代理字符串的 EWS 的应用程序"OWA /"。 |
|允许所有客户端应用程序使用 EWS。 | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceBlockList` <br/><br/> 由于指定没有 BlockList，则所有应用程序可以使用 EWS。 |
|阻止整个组织使用 EWS。 | `Set-OrganizationConfig -EwsEnabled:$false` |
|使整个组织使用 EWS。 | `Set-OrganizationConfig -EwsEnabled:$true`|
|阻止使用 EWS 单个邮箱。 | `Set-CASMailbox -Identity adam@contoso.com -EwsEnabled:$false`|
|允许使用 EWS 单个邮箱。 | `Set-CASMailbox -Identity adam@contoso.com -EwsEnabled:$true`|
   
## <a name="see-also"></a>另请参阅

- [EWS 应用程序设置](setting-up-your-ews-application.md)    
- [在 Exchange 控制客户端应用程序访问 EWS](controlling-client-application-access-to-ews-in-exchange.md)   
- [Exchange Server PowerShell （Exchange 命令行管理程序）](https://docs.microsoft.com/en-us/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps) 
- [Windows PowerShell](http://msdn.microsoft.com/en-us/library/dd835506%28v=vs.85%29.aspx)
    

