---
title: Outlook 加载项和 Exchange 中的 EWS
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.assetid: 821c8eb9-bb58-42e8-9a3a-61ca635cba59
description: 查找有关 Outlook 外接程序及其如何与 Exchange 中的 EWS 配合使用的信息。
localization_priority: Priority
ms.openlocfilehash: 2b0cee2017c24d714fa444c094ab1797be1fbe99
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456274"
---
# <a name="outlook-add-ins-and-ews-in-exchange"></a>Outlook 加载项和 Exchange 中的 EWS

查找有关 Outlook 外接程序及其如何与 Exchange 中的 EWS 配合使用的信息。

Outlook 外接程序提供了单个接口和编程模型，该模型使用 web 标准使您能够为您的电子邮件用户创建自定义体验。 您可以创建在 Outlook 托管的 HTML5 框架中显示上下文或有用信息的邮件应用程序;例如，邮件应用程序可以显示电子邮件包含地址时突出显示的地址的 Bing 地图。 或者，当用户撰写邮件时，邮件应用程序可以显示有关收件人的其他信息，并在按钮中插入电子邮件中的标准问候语。

> [!NOTE]
> 除非另有说明，否则本文中提及“Outlook”的地方也适用于 Outlook 富客户端、Outlook Web App 和适用于设备的 OWA。

邮件应用程序接口是适用于 Office 的 JavaScript API 的一部分。 您可以使用 API 访问 Exchange 中的信息，以使您的邮件应用程序：

- [识别](https://msdn.microsoft.com/library/a6b0904b-afe9-4882-9136-3d8cfd57fcf8%28Office.15%29.aspx)电子邮件中的实体，如地址、电话号码、任务建议或会议建议。

- 在单独的视图中打开并显示现有[邮件](https://msdn.microsoft.com/library/d0bca550-70c3-457c-85f8-e19b39e3b892%28Office.15%29.aspx)和[约会](https://msdn.microsoft.com/library/6cfbc29d-8581-474e-9a8b-510471e4bf8b%28Office.15%29.aspx)，以便用户可以在一个或多个邮件中交叉引用信息。

- 对承载用户邮箱的 Exchange 服务器[发出 EWS 请求](https://msdn.microsoft.com/library/2ec380e0-4a67-4146-92a6-6a39f65dc6f2%28Office.15%29.aspx)。 例如，邮件应用程序可以获取文件夹列表，以便用户可以选择一个文件夹来存储邮件，或显示对话中的所有项目，或将电子邮件标记为垃圾邮件。

- [获取一个令牌](https://msdn.microsoft.com/library/c658518b-6867-41a0-99cf-810303e4c539%28Office.15%29.aspx)，以唯一标识电子邮件帐户，以便在第三方服务上启用单一登录。

- [获取一个令牌](https://msdn.microsoft.com/library/c658518b-6867-41a0-99cf-810303e4c539%28Office.15%29.aspx)，该令牌使第三方服务可以代表用户发出 EWS 请求，例如，从项目中提取附件，或从 Exchange 服务器获取项目以进行进一步处理。

您可以使用邮件应用程序为您的用户自定义 Outlook Web App 体验;但是，如果要自定义 Outlook Web App 的 "外观"，请参阅 TechNet 上的以下文章：

- [为 Outlook Web App 创建主题](https://technet.microsoft.com/library/bb201700%28v=exchg.150%29.aspx)

- [自定义 Outlook Web App 登录、语言选择和错误页](https://technet.microsoft.com/library/ee633483%28v=exchg.150%29.aspx)

您的组织可以在内部服务器上安装邮件应用程序，以限制对已授权用户的访问权限，或者您和其他邮件应用程序开发人员可以将邮件应用程序放在[Office 商店](https://office.microsoft.com/store/)以销售到一般大众。 运行 Outlook 的任何人都可以从 marketplace 下载、安装和使用邮件应用程序。

若要了解有关创建邮件应用程序的详细信息，请查看[Outlook 外接程序文档](/outlook/add-ins)或[生成 EWS 请求](https://code.msdn.microsoft.com/exchange/Mail-apps-for-Outlook-Make-770b2528)示例。

## <a name="ews-and-outlook-add-ins"></a>EWS 和 Outlook 外接程序

您可以在承载运行邮件应用程序的帐户的 Exchange 服务器上使用 EWS 部分的 EWS 操作。

[MakeEwsRequestAsync](https://msdn.microsoft.com/library/2ec380e0-4a67-4146-92a6-6a39f65dc6f2%28Office.15%29.aspx)函数使您能够将 EWS 请求从您的邮件应用程序发回承载用户邮箱的服务器。 创建 SOAP 信封和 XML 请求， **makeEwsRequestAsync**函数将使用标识发出请求的邮箱和邮件应用程序的身份验证令牌调用 EWS。 为了帮助保护用户邮箱的安全，Exchange 服务器将拒绝不来自邮件应用程序或未在服务器上托管的邮箱发出的任何请求。

与任何其他应用程序一样，邮件应用程序需要权限才能发挥作用。 您的管理员需要执行以下操作：

- 授予对邮件应用程序用户的[EWS 访问权限](controlling-client-application-access-to-ews-in-exchange.md)。

- 在客户端访问服务器 EWS 目录上[将 "OAuthAuthentication" 设置为 true](https://technet.microsoft.com/library/aa997233%28v=exchg.150%29.aspx) 。

您还需要确保您的应用程序在 Office 相关应用程序[权限模型](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md)中请求 "读/写邮箱" 权限。

完成这些步骤后，可使用邮件应用程序的文件夹和项目 EWS 操作的子集。

**表1。邮件应用程序可以使用的 EWS 文件夹和项目操作**

|**文件夹操作**|**项操作**|
|:-----|:-----|
|[CreateFolder 操作](https://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> [FindFolder 操作](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) <br/> [GetFolder 操作](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> [UpdateFolder 操作](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> |[CopyItem 操作](https://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> [CreateItem 操作](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/> [FindItem 操作](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) <br/> [FindConversation 操作](https://msdn.microsoft.com/library/2384908a-c203-45b6-98aa-efd6a4c23aac%28Office.15%29.aspx) <br/> [GetConversationItems 操作](https://msdn.microsoft.com/library/8ae00a99-b37b-4194-829c-fe300db6ab99%28Office.15%29.aspx) <br/> [GetItem 操作](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> [MarkAsJunk 操作](https://msdn.microsoft.com/library/1f71f04d-56a9-4fee-a4e7-d1034438329e%28Office.15%29.aspx) <br/> [MoveItem 操作](https://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/> [SendItem 操作](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) <br/> [UpdateItem 操作](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |

### <a name="service-callback-tokens"></a>服务回调令牌

服务回调令牌使邮件应用程序能够将访问令牌传递给第三方服务，以便该服务可以对承载邮箱的 Exchange 服务器发出 EWS 请求。 例如，邮件应用程序可以将服务回调令牌传递给第三方服务，以及附加到电子邮件的图片的附件 Id 列表。 然后，服务可以使用附件 Id 和回调令牌向用户的 Exchange 服务器发出 EWS 请求，以获取附加的图片。 邮件应用程序还可以使用具有项目 Id 列表的服务回调令牌来获取来自 Exchange 服务器的电子邮件和约会项目。

服务回调令牌是一个不透明令牌，第三方服务在持有者身份验证标头中附加到 EWS 请求。 令牌标识邮件应用程序和邮箱，以帮助保护 EWS 请求。 若要了解如何使用服务回调令牌，请参阅[Outlook 外接程序：从 Exchange Server 获取附件](https://code.msdn.microsoft.com/exchange/Mail-apps-for-Office-Get-38babdc9)示例。

## <a name="see-also"></a>另请参阅


- [控制对 Exchange 中的 EWS 的客户端应用程序访问](controlling-client-application-access-to-ews-in-exchange.md)

- [Mailbox.makeEwsRequestAsync 方法（适用于 Office 的 JavaScript API）](https://msdn.microsoft.com/library/2ec380e0-4a67-4146-92a6-6a39f65dc6f2%28Office.15%29.aspx)

- [Outlook 加载项](https://docs.microsoft.com/outlook/add-ins)

- [Mailbox.getUserIdentityTokenAsync 方法（适用于 Office 的 JavaScript API）](https://msdn.microsoft.com/library/c658518b-6867-41a0-99cf-810303e4c539%28Office.15%29.aspx)

- [使用 Exchange 标识令牌对 Outlook 外接程序进行身份验证](https://msdn.microsoft.com/library/c0520a1e-d9ba-495a-a99f-6816d7d2a23e%28Office.15%29.aspx)

- [了解 Outlook 外接程序权限](https://docs.microsoft.com/outlook/add-ins/understanding-outlook-add-in-permissions)

- [Set-webservicesvirtualdirectory](https://technet.microsoft.com/library/aa997233%28v=exchg.150%29.aspx)

- [Outlook 外接程序：生成 EWS 请求](https://code.msdn.microsoft.com/office/Mail-apps-for-Outlook-Make-770b2528)

- [Outlook 外接程序：使用客户端标识令牌](https://code.msdn.microsoft.com/Mail-apps-for-Outlook-Use-b20a66b6)

- [Outlook 外接程序：从 Exchange 服务器获取附件](https://code.msdn.microsoft.com/office/Mail-apps-for-Office-Get-38babdc9)
