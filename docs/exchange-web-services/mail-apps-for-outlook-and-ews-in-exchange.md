---
title: Outlook 和 Exchange 中的 EWS 的邮件应用程序
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 821c8eb9-bb58-42e8-9a3a-61ca635cba59
description: 查找有关邮件应用程序的 Outlook 和如何使用 EWS 在 Exchange 中的信息。
ms.openlocfilehash: 2f44045d80a74ed6a835604d516949ca3bc27379
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752914"
---
# <a name="mail-apps-for-outlook-and-ews-in-exchange"></a>Outlook 和 Exchange 中的 EWS 的邮件应用程序

查找有关邮件应用程序的 Outlook 和如何使用 EWS 在 Exchange 中的信息。
  
Outlook 邮件应用程序提供了单一界面和使用 web 标准来使您能够创建自定义电子邮件用户体验的编程模型。 您可以创建在 Outlook 中; 承载 HTML5 框架中显示上下文或有用信息的邮件应用程序例如，邮件应用程序可以使用突出显示时的电子邮件包含地址的地址显示必应 Bing 地图。 或者，当用户撰写邮件时，邮件应用程序可以显示收件人，有关其他信息，然后在按钮的触摸电子邮件中插入的标准的问候语。
  
> [!NOTE]
> 除非另有说明，否则本文中提及“Outlook”的地方也适用于 Outlook 富客户端、Outlook Web App 和适用于设备的 OWA。 
  
邮件应用程序界面属于 JavaScript API for Office。 您可以使用 API 访问 Exchange 中启用对邮件应用程序的信息：
  
- [识别实体](http://msdn.microsoft.com/library/a6b0904b-afe9-4882-9136-3d8cfd57fcf8%28Office.15%29.aspx)，如地址、 电话号码、 任务建议或电子邮件中的会议建议。 
    
- 在打开并显示现有[邮件](http://msdn.microsoft.com/library/d0bca550-70c3-457c-85f8-e19b39e3b892%28Office.15%29.aspx)和[约会](http://msdn.microsoft.com/library/6cfbc29d-8581-474e-9a8b-510471e4bf8b%28Office.15%29.aspx)单独的视图，以便用户可以交叉引用中一个或多个邮件的信息。 
    
- 向承载用户邮箱的 Exchange 服务器[发出 EWS 请求](http://msdn.microsoft.com/library/2ec380e0-4a67-4146-92a6-6a39f65dc6f2%28Office.15%29.aspx)。 例如，邮件应用程序可以文件夹的列表，以便用户可以选择一个要存储该邮件，或在对话中，显示所有项或标记为垃圾邮件的电子邮件中。 
    
- [获取令牌](http://msdn.microsoft.com/library/c658518b-6867-41a0-99cf-810303e4c539%28Office.15%29.aspx)来唯一标识的电子邮件帐户，若要启用单一登录第三方服务。 
    
- [获取令牌](http://msdn.microsoft.com/library/c658518b-6867-41a0-99cf-810303e4c539%28Office.15%29.aspx)，例如发出 EWS 请求代表用户，以提取附件从项目，或进一步处理从 Exchange 服务器获取项目的第三方服务。 
    
您可以使用邮件应用程序用户; 自定义的 Outlook Web App 体验如果，但是，您想要自定义"外观"Outlook Web app，请参阅 TechNet 上的以下文章：
  
- [为 Outlook Web App 中创建主题](http://technet.microsoft.com/en-us/library/bb201700%28v=exchg.150%29.aspx)
    
- [自定义 Outlook Web App 登录、 语言选择和错误页](http://technet.microsoft.com/en-us/library/ee633483%28v=exchg.150%29.aspx)
    
您的组织可以在要限制对授权用户访问的内部服务器上安装邮件应用程序或您和其他邮件应用程序开发人员可以将邮件应用程序置于[Office 商店](http://office.microsoft.com/store/)出售向公众。 运行 Outlook 的任何人都可以下载、 安装和使用市场中的邮件应用程序。 
  
如果您想要了解有关创建邮件应用程序详细信息，签出[的 Outlook 文档的邮件应用程序](http://msdn.microsoft.com/library/71e64bc9-e347-4f5d-8948-0a47b5dd93e6%28Office.15%29.aspx)或[发出 EWS 请求](http://code.msdn.microsoft.com/exchange/Mail-apps-for-Outlook-Make-770b2528)示例。 
  
## <a name="ews-and-mail-apps-for-outlook"></a>用于 Outlook 的 EWS 和邮件应用程序

您可以使用承载运行邮件应用程序的帐户的 Exchange 服务器上的 EWS 操作的一个子集。
  
[Mailbox.makeEwsRequestAsync](http://msdn.microsoft.com/library/2ec380e0-4a67-4146-92a6-6a39f65dc6f2%28Office.15%29.aspx)函数使您能够从邮件应用程序回服务器承载用户邮箱的 EWS 请求。 创建用于标识邮箱身份验证令牌 SOAP 信封 XML 请求和**makeEwsRequestAsync**函数调用 EWS 和邮件应用程序发出请求。 若要帮助保护用户的邮箱，Exchange 服务器将拒绝并非从邮件应用程序或未承载邮箱服务器的任何请求。 
  
任何其他应用程序，如邮件应用程序需要使用权限。 管理员需要为：
  
- 邮件应用程序用户[授予 EWS 访问](controlling-client-application-access-to-ews-in-exchange.md)。 
    
- 在客户端访问服务器 EWS 目录上[设置为 true 的"OAuthAuthentication"](http://technet.microsoft.com/en-us/library/aa997233%28v=exchg.150%29.aspx) 。 
    
您还需要以确保您的应用程序请求读/写邮箱权限 for Office[权限模型](http://msdn.microsoft.com/library/5bca69f2-b287-4e19-8f0f-78d896b2a3d3%28Office.15%29.aspx)应用程序中。
  
完成这些步骤后，为邮件应用程序使用提供了文件夹和项目 EWS 操作的子集。 
  
**表 1。可以使用邮件应用程序的 EWS 文件夹和项目操作**

|**文件夹操作**|**项目操作**|
|:-----|:-----|
|[CreateFolder Operation](http://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> [FindFolder Operation](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) <br/> [GetFolder Operation](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> [UpdateFolder Operation](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> |[CopyItem 操作](http://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> [CreateItem 操作](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/> [FindItem 操作](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) <br/> [FindConversation Operation](http://msdn.microsoft.com/library/2384908a-c203-45b6-98aa-efd6a4c23aac%28Office.15%29.aspx) <br/> [GetConversationItems 操作](http://msdn.microsoft.com/library/8ae00a99-b37b-4194-829c-fe300db6ab99%28Office.15%29.aspx) <br/> [GetItem 操作](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> [MarkAsJunk 操作](http://msdn.microsoft.com/library/1f71f04d-56a9-4fee-a4e7-d1034438329e%28Office.15%29.aspx) <br/> [MoveItem 操作](http://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/> [SendItem 操作](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) <br/> [UpdateItem 操作](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
   
### <a name="service-callback-tokens"></a>服务回调令牌

服务回调令牌启用邮件应用程序将传递给第三方服务的访问令牌，以便服务可以到承载邮箱的 Exchange 服务器发出 EWS 请求。 例如，邮件应用程序可以将服务回调令牌传递给第三方服务以及附加到电子邮件的图片的附件 Id 的列表。 该服务然后可以使用附件 Id 和回调令牌以向用户的 Exchange 服务器获取附加的图片发出 EWS 请求。 邮件应用程序也可以用于服务回调令牌一组项目 Id 从 Exchange 服务器获取电子邮件和约会项。
  
服务回调令牌是不透明令牌的第三方服务将附加到持有者 authentication 标头中的 EWS 请求。 标记标识邮件应用程序和要帮助保护 EWS 请求的邮箱。 若要了解如何使用服务回调令牌，请参阅[Outlook 邮件应用程序： 从 Exchange 服务器获取附件](http://code.msdn.microsoft.com/exchange/Mail-apps-for-Office-Get-38babdc9)示例。 
  
## <a name="see-also"></a>另请参阅


- [在 Exchange 控制客户端应用程序访问 EWS](controlling-client-application-access-to-ews-in-exchange.md)
    
- [Mailbox.makeEwsRequestAsync 方法 (Office 的 JavaScript API)](http://msdn.microsoft.com/library/2ec380e0-4a67-4146-92a6-6a39f65dc6f2%28Office.15%29.aspx)
    
- [Outlook 外接程序](http://msdn.microsoft.com/library/71e64bc9-e347-4f5d-8948-0a47b5dd93e6%28Office.15%29.aspx)
    
- [Mailbox.getUserIdentityTokenAsync 方法 (Office 的 JavaScript API)](http://msdn.microsoft.com/library/c658518b-6867-41a0-99cf-810303e4c539%28Office.15%29.aspx)
    
- [使用 Exchange 标识令牌对 Outlook 外接程序进行身份验证](http://msdn.microsoft.com/library/c0520a1e-d9ba-495a-a99f-6816d7d2a23e%28Office.15%29.aspx)
    
- [指定 Outlook 外接程序对用户邮箱的访问权限](http://msdn.microsoft.com/library/5bca69f2-b287-4e19-8f0f-78d896b2a3d3%28Office.15%29.aspx)
    
- [Set-webservicesvirtualdirectory](http://technet.microsoft.com/en-us/library/aa997233%28v=exchg.150%29.aspx)
    
- [Outlook 邮件应用程序： 发出 EWS 请求](http://code.msdn.microsoft.com/office/Mail-apps-for-Outlook-Make-770b2528)
    
- [Outlook 邮件应用程序： 使用客户端身份令牌](http://code.msdn.microsoft.com/Mail-apps-for-Outlook-Use-b20a66b6)
    
- [Outlook 邮件应用程序： 从 Exchange 服务器获取附件](http://code.msdn.microsoft.com/office/Mail-apps-for-Office-Get-38babdc9)
    

