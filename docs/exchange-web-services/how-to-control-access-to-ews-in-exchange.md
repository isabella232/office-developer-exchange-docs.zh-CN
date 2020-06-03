---
title: 在 Exchange 中控制对 EWS 的访问
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 61e29e54-e3e5-404a-84c0-93b61a25ca58
description: 了解如何控制用户、应用程序或整个组织对 EWS 的访问。
localization_priority: Priority
ms.openlocfilehash: bd65b099ab15c1514945d8a1cfa4e9b1428a4755
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456876"
---
# <a name="control-access-to-ews-in-exchange"></a>在 Exchange 中控制对 EWS 的访问

了解如何控制用户、应用程序或整个组织对 EWS 的访问。
  
无论您是在应用程序中直接使用 EWS 托管 API （或 EWS），您都可以控制对 Exchange Web 服务（EWS）的访问。 如果您具有对 Exchange 服务器的管理员访问权限，则可以通过使用 Exchange 命令行管理程序来控制对 EWS 的访问权限，对每个用户和每个应用程序进行全局访问。
  
## <a name="exchange-management-shell-cmdlets-for-configuring-access-control"></a>用于配置访问控制的 Exchange 命令行管理程序 cmdlet
<a name="bk_Cmdlets"> </a>

您可以使用以下 Exchange 命令行管理程序 cmdlet 查看当前的访问配置和设置 EWS 访问控制：
  
- [Set-casmailbox](https://technet.microsoft.com/library/bb124754.aspx) -显示为特定邮箱设置的参数。   
- [Set-set-casmailbox](https://technet.microsoft.com/library/bb125264.aspx) -设置特定邮箱的参数。    
- [Set-organizationconfig](https://technet.microsoft.com/library/aa997571.aspx) -显示整个组织的参数。    
- [Set-set-organizationconfig](https://technet.microsoft.com/library/aa997443.aspx) -设置整个组织的参数。 

<a name="bk_Examples"> </a>

## <a name="examples-controlling-access-to-ews"></a>示例：控制对 EWS 的访问

我们来看看几个方案，向您介绍如何控制对应用程序的访问。
  
**表1。用于控制对 EWS 的访问的命令**

|如果您想要 |使用此命令|
|:-----|:-----|
|阻止所有客户端应用程序使用 EWS。 | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceAllowList`<br/><br/>这将允许 AllowList 中列出的应用程序进行连接。 在此示例中，AllowList 中不包含任何应用程序，因此任何应用程序都不能使用 EWS。 |
|允许客户端应用程序列表使用 EWS。 | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceAllowList -EwsAllowList:"OWA/*"`<br/><br/>这将允许特定应用程序使用 EWS。 在此示例中，允许具有以 "OWA/" 开头的用户代理字符串的任何应用程序访问权限。 |
|允许所有客户端应用程序使用 EWS，但特别被阻止的应用程序除外。 | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceBlockList -EwsBlockList:"OWA/*"`<br/> <br/>本示例仅阻止应用程序使用具有以 "OWA/" 开头的用户代理字符串的 EWS。 |
|允许所有客户端应用程序使用 EWS。 | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceBlockList` <br/><br/> 由于未指定阻止列表，所有应用程序都可以使用 EWS。 |
|阻止整个组织使用 EWS。 | `Set-OrganizationConfig -EwsEnabled:$false` |
|允许整个组织使用 EWS。 | `Set-OrganizationConfig -EwsEnabled:$true`|
|阻止单个邮箱使用 EWS。 | `Set-CASMailbox -Identity adam@contoso.com -EwsEnabled:$false`|
|允许单个邮箱使用 EWS。 | `Set-CASMailbox -Identity adam@contoso.com -EwsEnabled:$true`|
   
## <a name="see-also"></a>另请参阅

- [设置 EWS 应用程序](setting-up-your-ews-application.md)    
- [控制对 Exchange 中的 EWS 的客户端应用程序访问](controlling-client-application-access-to-ews-in-exchange.md)   
- [Exchange Server PowerShell （Exchange 命令行管理程序）](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps) 
- [Windows PowerShell](https://msdn.microsoft.com/library/dd835506%28v=vs.85%29.aspx)
    

