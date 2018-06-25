---
title: EWS 托管 API 客户端应用程序入门
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: c2267733-6f4f-49e5-9614-1e4a24c3af1a
description: 使用 EWS 托管 API 针对 Exchange 开发一个简单的 Hello World 电子邮件客户端应用程序。
ms.openlocfilehash: dafc8cbbf172ad725ab83c93553464ba96ef33b8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752736"
---
# <a name="get-started-with-ews-managed-api-client-applications"></a>EWS 托管 API 客户端应用程序入门

本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 使用 EWS 托管 API 针对 Exchange 开发一个简单的 Hello World 电子邮件客户端应用程序。 
  
[EWS 托管 API](http://aka.ms/ews-managed-api-readme) 提供一个直观易用的对象模型，可用于发送和接收来自客户端应用程序、门户应用程序和服务应用程序的 Web 服务消息。您可以使用 EWS 托管 API 访问 Exchange Online、作为 Office 365 一部分的 Exchange Online 或 Exchange 服务器邮箱中存储的几乎所有信息。您可以使用本文中的信息以帮助您开发首个 EWS 托管 API 客户端应用程序。 
  
> [!NOTE]
> [!注释]  EWS 托管 API 现在已经作为开放源项目在 [GitHub](https://github.com/officedev/ews-managed-api) 上可用。您可以使用开放源库执行以下操作： >  为 API 提供缺陷修复和增强功能。 >  在修补程序和增强功能在正式的版本中可用之前获取它们。 >  访问最全面且最新的 API 实现，将其用作参考或在新的平台上创建新库。 >  我们欢迎您通过 GitHub 做出 [贡献](https://github.com/OfficeDev/ews-managed-api/blob/master/CONTRIBUTING.md)。 
  
## <a name="youll-need-an-exchange-server"></a>您将需要 Exchange 服务器
<a name="NeedExchange"> </a>

如果您已经有一个 Exchange 邮箱帐户，则可以跳过本节。否则，您必须具备以下选项来为您的首个 EWS 客户端应用程序设置 Exchange 邮箱：
  
- 获得 [Office 365 开发人员网站](http://msdn.microsoft.com/en-us/library/office/fp179924.aspx)（推荐）。这是您设置 Exchange 邮箱的最快方法。 
    
- 下载 [Exchange Server](http://office.microsoft.com/en-us/exchange/microsoft-exchange-try-or-buy-exchange-we-can-help-you-decide-FX103746846.aspx?WT%2Eintid1=ODC%5FENUS%5FFX103472230%5FXT103965589)。
    
确认您可以从 Exchange 发送和接收电子邮件后，您便可以设置您的开发环境了。您可以使用 Exchange Web 客户端 [Outlook Web App](http://technet.microsoft.com/en-us/library/jj657718%28v=exchg.150%29.aspx) 确认您是否可以发送电子邮件。 
  
## <a name="set-up-your-development-environment"></a>设置开发环境
<a name="Setup"> </a>

请确保您可访问以下项目：
  
- 支持.NET Framework 4 的任何版本的 [Visual Studio](http://www.visualstudio.com/en-us/downloads/download-visual-studio-vs.aspx)。尽管从技术上讲，您不需要 Visual Studio，因为您可以使用任何 C# 编译，但仍建议使用它。 
    
- [EWS 托管 API](http://aka.ms/ews-managed-api-readme)。您可以使用 32 位或 64 位版本，具体取决于您的系统。使用默认安装位置。 
    
## <a name="create-your-first-ews-managed-api-application"></a>创建第一个 EWS 托管 API 应用程序
<a name="Create"> </a>

这些步骤假定您设置 Office 365 开发人员网站。如果您已下载并安装 Exchange，您将需要在您的 Exchange 服务器上[安装有效的证书](http://technet.microsoft.com/en-us/library/bb310769%28v=exchg.141%29.aspx)或针对默认情况下提供的自签名证书[实现证书验证](how-to-validate-a-server-certificate-for-the-ews-managed-api.md)回调。另外，请注意以下步骤会稍有不同，具体取决于您正在使用的 Visual Studio 的版本。 
  
### <a name="step-1-create-a-project-in-visual-studio"></a>步骤 1：在 Visual Studio 中创建项目

1. 在 Visual Studio 中的 **文件** 菜单上，选择 **新建** ，然后选择 **项目** 。将打开 **新建项目** 对话框。 
    
2. 创建 **C# 控制台应用程序** 。从 **模板** 窗格中，选择 **Visual C#** ，然后选择 **控制台应用程序** 。 
    
3. 项目命名为 HelloWorld，，然后选择**确定**。
    
Visual Studio 创建该项目，并打开 Program.cs 代码文档窗口。

### <a name="step-2-add-a-reference-to-the-ews-managed-api"></a>步骤 2：向 EWS 托管 API 添加引用

1. 如果 **解决方案资源管理器** 窗口已经打开，请跳过此步骤并继续步骤 2。若要打开 **解决方案资源管理器** 窗口，请在 **视图** 菜单上，选择 **解决方案资源管理器** 。 
    
2. 在 **解决方案资源管理器** 和 **HelloWorld** 项目中，打开 **引用** 对应的快捷菜单（单击鼠标右键），然后从上下文菜单中选择 **添加引用** 。将打开用于管理项目引用的对话框。 
    
3. 选择**浏览**选项。 浏览到安装 EWS 托管 API DLL 的位置。 设置由安装程序的默认路径为以下： C:\Program Files\Microsoft\Exchange\Web 服务\<版本 >\. 根据您下载 32 或 64 位版本的 Microsoft.Exchange.WebServices.dll 变化路径。 **Microsoft.Exchange.WebServices.dll**并选择**确定**或**添加**。 这样会将添加到您的项目的 EWS 托管 API 引用。 
    
4. 如果使用 EWS 托管 API 2.0，请更改 HelloWorld 项目以锁定 .NET Framework 4。EWS 托管 API 的其他版本可能使用不同的 .NET Framework 目标版本。
    
5. 请确认您使用正确的 .NET Framework 目标版本。打开 **解决方案资源管理器** 中 **HelloWorld** 项目对应的快捷菜单，然后选择 **属性** 。请验证 **目标框架** 下拉列表框中是否已选择 **.NET Framework 4** 。 
    
现在，您已设置项目并创建对 EWS 托管 API 的引用，便可以创建第一个应用程序了。 为简便起见，请将代码添加到 Program.cs 文件中。 阅读有关引用 EWS 托管 API 的详细信息[引用的 EWS 托管 API 的程序集](how-to-reference-the-ews-managed-api-assembly.md)。 在下一个步骤中，您将开发基本代码来编写大多数 EWS 托管 API 客户端应用程序。 
### <a name="step-3-set-up-url-redirection-validation-for-autodiscover"></a>步骤 3：设置用于自动发现的 URL 重定向验证

- 在 **Main(string[] args)** 方法后添加以下重定向验证回调方法。这将验证重定向的 URL 是否由代表 HTTPS 终结点的 ["自动发现"](autodiscover-for-exchange.md) 表示。 
    
  ```cs
  private static bool RedirectionUrlValidationCallback(string redirectionUrl)
  {
     // The default for the validation callback is to reject the URL.
     bool result = false;
     Uri redirectionUri = new Uri(redirectionUrl);
     // Validate the contents of the redirection URL. In this simple validation
     // callback, the redirection URL is considered valid if it is using HTTPS
     // to encrypt the authentication credentials. 
     if (redirectionUri.Scheme == "https")
     {
        result = true;
     }
     return result;
  }
  ```

此验证回调将被传递到步骤 4 中的 **ExchangeService** 对象。您需要进行验证，以便应用程序将信任和遵循自动发现重定向 - 自动发现重定向的结果为我们的应用程序提供 EWS 终结点。 

### <a name="step-4-prepare-the-exchangeservice-object"></a>步骤 4：准备 ExchangeService 对象

1. 向 EWS 托管 API 添加 **using** 指令引用。在 Program.cs 顶部的最后一个 **using** 指令后添加以下代码。 
    
   ```cs
    using Microsoft.Exchange.WebServices.Data;
   ```

2. 在 **Main** 方法中，采用您打算使用的服务版本实例化 [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象。此示例将锁定 EWS 架构的最早版本。 
    
   ```cs
    ExchangeService service = new ExchangeService(ExchangeVersion.Exchange2007_SP1);
   ```

3. 如果锁定内部 Exchange 服务器，并且您的客户端加入域，请继续执行步骤 4。如果您的客户端锁定 Exchange Online 或 Office 365 开发人员网站邮箱，您必须传递显式凭据。在实例化 **ExchangeService** 对象后后添加以下代码并设置邮箱帐户的凭据。用户名应为用户主体名称。继续执行步骤 5。 
    
   ```cs
    service.Credentials = new WebCredentials("user1@contoso.com", "password");
   ```

4. 锁定内部 Exchange 服务器并加入域的客户端可以使用所登录用户的默认凭据，假定凭据与邮箱关联。实例化 **ExchangeService** 对象后添加以下代码。 
    
   ```cs
    service.UseDefaultCredentials = true;
   ```

   如果您的客户端锁定 Exchange Online 或 Office 365 开发人员网站的邮箱，请验证 [UseDefaultCredentials](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.usedefaultcredentials%28v=exchg.80%29.aspx) 是否设置为 **false**，该值为默认值。您的客户端已准备好进行自动发现服务的第一个调用以获得 EWS 服务调用的服务 URL。
    
5. **ExchangeService** 对象上的 **AutodiscoverUrl** 方法对自动发现服务执行一系列调用，以获取服务 URL。如果此方法调用成功， **ExchangeService** 对象上的 的 URL 属性将使用服务 URL 设置。将用户的电子邮件地址和 **RedirectionUrlValidationCallback** 传递到 **AutodiscoverUrl** 方法。在步骤 3 或 4 中指定凭据后，添加以下代码。将  `user1@contoso.com` 更改为您的电子邮件地址，以便自动发现服务查找您的 EWS 终结点。 
    
   ```cs
    service.AutodiscoverUrl("user1@contoso.com", RedirectionUrlValidationCallback);
   ```

此时，您的客户端设置为调用 EWS 以访问邮箱数据。 如果立即运行您的代码，则可以通过检查 **ExchangeService.Url** 属性的内容验证运行的 [AutodiscoverUrl](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) 方法调用。 如果此属性包含一个 URL，ze 您的调用成功！ 这意味着您的应用程序成功进行服务身份验证并发现您邮箱的 EWS 终结点。 现在，您便可以对 EWS 执行第一个调用了。 阅读有关设置 EWS URL 的详细信息的[设置使用 EWS 托管 API 的 EWS 服务 URL](how-to-set-the-ews-service-url-by-using-the-ews-managed-api.md) 。 

### <a name="step-6-create-your-first-hello-world-email-message"></a>步骤 6：创建第一个 Hello World 电子邮件

1. 在 **AutodiscoverUrl** 方法调用后，实例化一个新的 **EmailMessage** 对象并传递您创建的服务对象。 
    
   ```cs
    EmailMessage email = new EmailMessage(service);
   ```

   您现在有一封设置服务绑定的电子邮件。在 **EmailMessage** 对象上启动的任何调用都将在服务处被锁定。 
    
2. 现在设置收件人：电子邮件的行收件人。若要执行此操作，将  `user1@contoso.com` 更改为使用 SMTP 地址。 
    
   ```cs
    email.ToRecipients.Add("user1@contoso.com");
   ```

3. 设置电子邮件的主题和正文。
    
   ```cs
    email.Subject = "HelloWorld";
    email.Body = new MessageBody("This is the first email I've sent by using the EWS Managed API.");
   ```

4. 现在您便可以通过使用 EWS 托管 API 发送第一封电子邮件。 **Send** 方法将调用服务并提交电子邮件以便进行传送。 阅读[Communicate with EWS 使用 EWS 托管 API](how-to-communicate-with-ews-by-using-the-ews-managed-api.md)以了解您可以使用与 Exchange 进行通信的其他方法。 
    
   ```cs
    email.Send();
   ```

5. 现在您便可以运行 Hello World 应用程序了。在 Visual Studio 中，选择 **F5**。将会打开一个空白的控制台窗口。当应用程序进行身份验证时您将在控制台中看不到任何内容，遵循自动发现重定向，然后进行其第一次调用以创建向自己发送的电子邮件。如果您想要查看正在进行的调用，请在调用 **AutodiscoverUrl** 方法之前添加以下两行代码 。然后按 F5。这将 [追踪 EWS 请求和响应](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md)到控制台窗口。 
    
   ```cs
    service.TraceEnabled = true;
    service.TraceFlags = TraceFlags.All;
   ```

现在，您便拥有运行的 EWS 托管 API 客户端应用程序。为方便起见，下面的示例显示添加到 Program.cs 的所有代码以创建 Hello World 应用程序。

```cs
using System;
using Microsoft.Exchange.WebServices.Data;
namespace HelloWorld
{
  class Program
  {
    static void Main(string[] args)
    {
      ExchangeService service = new ExchangeService(ExchangeVersion.Exchange2007_SP1);
      service.Credentials = new WebCredentials("user1@contoso.com", "password");
      service.TraceEnabled = true;
      service.TraceFlags = TraceFlags.All;
      service.AutodiscoverUrl("user1@contoso.com", RedirectionUrlValidationCallback);
      EmailMessage email = new EmailMessage(service);
      email.ToRecipients.Add("user1@contoso.com");
      email.Subject = "HelloWorld";
      email.Body = new MessageBody("This is the first email I've sent by using the EWS Managed API");
      email.Send();
    }
    private static bool RedirectionUrlValidationCallback(string redirectionUrl)
    {
      // The default for the validation callback is to reject the URL.
      bool result = false;
      Uri redirectionUri = new Uri(redirectionUrl);
      // Validate the contents of the redirection URL. In this simple validation
      // callback, the redirection URL is considered valid if it is using HTTPS
      // to encrypt the authentication credentials. 
      if (redirectionUri.Scheme == "https")
      {
        result = true;
      }
      return result;
    }
  }
}
```

## <a name="next-steps"></a>后续步骤
<a name="Next"> </a>

如果您已经准备好使用您的第一个 EWS 托管 API 客户端应用程序执行更多操作，请浏览以下资源：
  
- [Exchange 2013：101 代码示例](http://code.msdn.microsoft.com/exchange/Exchange-2013-101-Code-3c38582c)
    
- [文件夹和项目](folders-and-items-in-ews-in-exchange.md)
    
- [EWSEditor](http://ewseditor.codeplex.com/)
    
如果您的应用程序遇到任何问题，[请尝试在论坛中发布问题或评论](http://social.technet.microsoft.com/Forums/exchange/en-US/home?forum=exchangesvrdevelopment)（别忘了阅读热门帖子）。 
  
## <a name="in-this-section"></a>本节中
<a name="Next"> </a>

- [EWS 托管 API 程序集参考](how-to-reference-the-ews-managed-api-assembly.md)
    
- [使用 EWS 托管 API 设置 EWS 服务 URL](how-to-set-the-ews-service-url-by-using-the-ews-managed-api.md)
    
- [使用 EWS 托管 API 与 EWS 通信](how-to-communicate-with-ews-by-using-the-ews-managed-api.md)
    
## <a name="see-also"></a>另请参阅

- [Start using web services in Exchange](start-using-web-services-in-exchange.md)    
- [Exchange 的 EWS 客户端设计概述](ews-client-design-overview-for-exchange.md)    
- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)   
- [跟踪请求和响应解决 EWS 托管 API 应用程序](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md)
    

