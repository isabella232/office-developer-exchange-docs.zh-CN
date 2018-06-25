---
title: 在 Exchange 处理委派相关 EWS 中的错误
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 631d364f-e324-4838-a92c-820286f771f8
description: 了解如何处理您通过使用 EWS 的 EWS 托管 API 在 Exchange 开发的应用程序中委派相关的错误。
ms.openlocfilehash: 3851709888e3a1087df02eea5d4d58888ad168e3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752716"
---
# <a name="handling-delegation-related-errors-in-ews-in-exchange"></a>在 Exchange 处理委派相关 EWS 中的错误

了解如何处理您通过使用 EWS 的 EWS 托管 API 在 Exchange 开发的应用程序中委派相关的错误。
  
如果您的应用程序使用委派或添加或删除代理人，您可能需要处理委派相关的错误。 您可以处理这些错误在运行时，或者开发 EWS 应用程序时。 EWS 托管 API[服务错误](http://msdn.microsoft.com/EN-US/library/microsoft.exchange.webservices.data.serviceerror%28v=exchg.80%29.aspx)枚举和 EWS [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素来定义这些错误。 
  
## <a name="delegation-related-errors"></a>委派相关错误

|**Error**|**您尝试对时发生...**|**处理它的...**|
|:-----|:-----|:-----|
|ErrorItemNotFound  <br/> ErrorFolderNotFound  <br/> |执行操作邮箱、 文件夹或您有权访问的项目。  <br/> |更新代理人的权限，使其能够通过调用[UpdateDelegates](http://msdn.microsoft.com/EN-US/library/microsoft.exchange.webservices.data.exchangeservice.updatedelegates%28v=exchg.80%29.aspx) EWS 托管 API 方法或[UpdateDelegate](http://msdn.microsoft.com/library/03f618ac-ad1a-4772-9b81-c5bb0f12d6ab%28Office.15%29.aspx) EWS 操作，然后重试请求访问文件夹或项目。  <br/> |
|ErrorAccessDenied  <br/> |修改您没有足够的权限修改的项目。  <br/> |通过调用**UpdateDelegate** EWS 托管 API 方法或**UpdateDelegate** EWS 操作，然后重试请求更新委派权限。  <br/> |
|ErrorDelegateCannotAddOwner  <br/> |尝试将邮箱所有者作为代理人添加到其自己的邮箱。  <br/> |[添加其他用户作为代理人](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)，不是邮箱所有者。  <br/> |
|ErrorDelegateAlreadyExists  <br/> |该委托已存在时，请添加代理。  <br/> |执行任何操作，因为该委托已存在邮箱所有者。 或者，如果您正在尝试更改一个现有的代理人的权限，然后使用**UpdateDelegates**方法或**UpdateDelegate**操作。  <br/> |
|ErrorNotDelegate  <br/> |修改委派权限的邮箱没有委派权限的用户。  <br/> |[作为代理人将用户添加](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)邮箱之前尝试更新或删除其权限。  <br/> |
|ErrorDelegateNoUser  <br/> |修改未在 Active Directory 域服务 (AD DS) 的用户的委派权限。  <br/> |更正请求中的委托信息或在 AD DS 中创建用户。  <br/> |
|ErrorSubscriptionDelegateAccessNotSupported  <br/> |使用代理人订阅代表邮箱所有者的通知。  <br/> |订阅通知作为邮箱所有者。  <br/> |
|ErrorWrongServerVersionDelegate  <br/> |从具有不同的服务器版本比的主体的邮箱服务器的代理人发出请求。  <br/> |使用委托，或添加的委托其邮箱已作为邮箱所有者的相同服务器版本。  <br/> |
|ErrorMissingEmailAddress  <br/> |发出请求使用委托帐户不具有邮箱。  <br/> |将邮箱添加到代理的帐户。  <br/> |
   
## <a name="see-also"></a>另请参阅


- [代理访问和 Exchange 中的 EWS](delegate-access-and-ews-in-exchange.md)
    
- [工具和资源来解决 exchange 的 EWS 应用程序](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md)
    

