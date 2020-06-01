---
title: 在 Exchange 中处理 EWS 中与委派相关的错误
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 631d364f-e324-4838-a92c-820286f771f8
description: 了解如何在使用 EWS 托管 API 或 Exchange 中的 EWS 开发的应用程序中处理与委派相关的错误。
ms.openlocfilehash: 145783c4e7f49ed6e2aa3a2dbe0d10909e06d7e8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455350"
---
# <a name="handling-delegation-related-errors-in-ews-in-exchange"></a>在 Exchange 中处理 EWS 中与委派相关的错误

了解如何在使用 EWS 托管 API 或 Exchange 中的 EWS 开发的应用程序中处理与委派相关的错误。
  
如果应用程序使用委派或添加或删除委派，则可能需要处理与委派相关的错误。 您可以处理这些错误在运行时，或者开发 EWS 应用程序时。 这些错误由 EWS 托管 API [ServiceError](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceerror%28v=exchg.80%29.aspx)枚举和 ews [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素定义。 
  
## <a name="delegation-related-errors"></a>与委派相关的错误

|**Error**|**当您尝试 .。。**|**处理它的...**|
|:-----|:-----|:-----|
|ErrorItemNotFound  <br/> ErrorFolderNotFound  <br/> |对邮箱、文件夹或不具有访问权限的项目执行操作。  <br/> |通过调用[UpdateDelegates](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.updatedelegates%28v=exchg.80%29.aspx) EWS 托管 API 方法或[UpdateDelegate](https://msdn.microsoft.com/library/03f618ac-ad1a-4772-9b81-c5bb0f12d6ab%28Office.15%29.aspx) EWS 操作更新代理的权限，以使其可以访问文件夹或项目，然后重试请求。  <br/> |
|ErrorAccessDenied  <br/> |修改您没有足够权限修改的项目。  <br/> |通过调用**UpdateDelegate** EWS 托管 API 方法或**UpdateDelegate** EWS 操作更新代理权限，然后重试请求。  <br/> |
|ErrorDelegateCannotAddOwner  <br/> |尝试将邮箱所有者添加为其自己的邮箱的代理。  <br/> |[将其他用户添加为代理](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)，而不是邮箱所有者。  <br/> |
|ErrorDelegateAlreadyExists  <br/> |委派已存在时添加委派。  <br/> |不执行任何操作，因为邮箱所有者已存在委派。 或者，如果您尝试更改现有代理的权限，则使用**UpdateDelegates**方法或**UpdateDelegate**操作。  <br/> |
|ErrorNotDelegate  <br/> |为对邮箱没有代理权限的用户修改委派权限。  <br/> |在尝试更新或删除用户权限之前，[将该用户添加为](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)邮箱的代理人。  <br/> |
|ErrorDelegateNoUser  <br/> |修改不在 Active Directory 域服务（AD DS）中的用户的委派权限。  <br/> |在 AD DS 中创建用户或更正请求中的代理信息。  <br/> |
|ErrorSubscriptionDelegateAccessNotSupported  <br/> |使用代理代表邮箱所有者订阅通知。  <br/> |以邮箱所有者的形式订阅通知。  <br/> |
|ErrorWrongServerVersionDelegate  <br/> |从具有与主体邮箱服务器不同的服务器版本的代理发出请求。  <br/> |使用代理或添加其邮箱与邮箱所有者具有相同的服务器版本的代理。  <br/> |
|ErrorMissingEmailAddress  <br/> |使用没有邮箱的代理帐户发出请求。  <br/> |将邮箱添加到代理的帐户。  <br/> |
   
## <a name="see-also"></a>另请参阅


- [代理访问和 Exchange 中的 EWS](delegate-access-and-ews-in-exchange.md)
    
- [工具和资源来解决 exchange 的 EWS 应用程序](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md)
    

