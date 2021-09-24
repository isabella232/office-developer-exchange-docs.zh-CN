---
title: 处理 EWS 中与委派相关的Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 631d364f-e324-4838-a92c-820286f771f8
description: 了解如何在应用程序中使用 EWS 托管 API 或 EWS 在应用程序中处理与委派Exchange。
ms.openlocfilehash: 17e4e7898f5cbed7a6dc524a84db6ba4080eab88
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512294"
---
# <a name="handling-delegation-related-errors-in-ews-in-exchange"></a>处理 EWS 中与委派相关的Exchange

了解如何在应用程序中使用 EWS 托管 API 或 EWS 在应用程序中处理与委派Exchange。
  
如果应用程序使用委派或添加或删除委派，您可能必须处理与委派相关的错误。 您可以处理这些错误在运行时，或者开发 EWS 应用程序时。 这些错误由 EWS 托管 API [ServiceError](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceerror%28v=exchg.80%29.aspx) 枚举和 EWS [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) 元素定义。 
  
## <a name="delegation-related-errors"></a>与委派相关的错误

|**错误**|**在尝试...**|**处理它的...**|
|:-----|:-----|:-----|
|ErrorItemNotFound  <br/> ErrorFolderNotFound  <br/> |对无法访问的邮箱、文件夹或项目执行操作。  <br/> |通过调用 [UpdateDelegates](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.updatedelegates%28v=exchg.80%29.aspx) EWS 托管 API 方法或 [UpdateDelegate](https://msdn.microsoft.com/library/03f618ac-ad1a-4772-9b81-c5bb0f12d6ab%28Office.15%29.aspx) EWS 操作，然后重试请求，更新代理的权限以允许他们访问文件夹或项目。  <br/> |
|ErrorAccessDenied  <br/> |修改您没有足够的权限修改的项。  <br/> |通过调用 **UpdateDelegate** EWS 托管 API 方法或 **UpdateDelegate** EWS 操作，然后重试请求来更新委派权限。  <br/> |
|ErrorDelegateCannotAddOwner  <br/> |尝试将邮箱所有者作为代理添加到其自己的邮箱。  <br/> |[将其他用户添加为代理，](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)而不是邮箱所有者。  <br/> |
|ErrorDelegateAlreadyExists  <br/> |在委托已存在时添加委托。  <br/> |不执行任何操作，因为邮箱所有者的代理已存在。 或者，如果要尝试更改现有代理的权限，请使用 **UpdateDelegates** 方法或 **UpdateDelegate** 操作。  <br/> |
|ErrorNotDelegate  <br/> |修改没有邮箱委派权限的用户的委派权限。  <br/> |[在尝试更新或删除其](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) 权限之前，将用户添加为邮箱的代理。  <br/> |
|ErrorDelegateNoUser  <br/> |修改不在 Active Directory 域服务中的用户的委派权限 (AD DS) 。  <br/> |在 AD DS 中创建用户，或更正请求中的委派信息。  <br/> |
|ErrorSubscriptionDelegateAccessNotSupported  <br/> |使用代理代表邮箱所有者订阅通知。  <br/> |作为邮箱所有者订阅通知。  <br/> |
|ErrorWrongServerVersionDelegate  <br/> |从服务器版本与主体邮箱服务器不同的代理提出请求。  <br/> |使用代理或添加其邮箱与邮箱所有者具有相同的服务器版本的代理。  <br/> |
|ErrorMissingEmailAddress  <br/> |使用没有邮箱的委派帐户提出请求。  <br/> |将邮箱添加到代理的帐户。  <br/> |
   
## <a name="see-also"></a>另请参阅


- [Exchange 中的代理访问和 EWS](delegate-access-and-ews-in-exchange.md)
    
- [工具和资源来解决 exchange 的 EWS 应用程序](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md)
    

