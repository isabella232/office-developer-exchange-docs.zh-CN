---
title: 开始使用 EWS 客户端应用程序
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.assetid: e6fd5c23-0ba5-4a7b-bdde-4a553447069f
description: 使用 exchange 中的 Exchange Web 服务（EWS）创建您的第一个应用程序。
localization_priority: Priority
ms.openlocfilehash: fd02c46777dabd04b492ba3c4420a0737640c5eb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528396"
---
# <a name="get-started-with-ews-client-applications"></a>开始使用 EWS 客户端应用程序

使用 exchange 中的 Exchange Web 服务（EWS）创建您的第一个应用程序。
  
EWS 是一项全面的服务，您的应用程序可以使用它访问 Exchange Online 中存储的几乎所有信息、作为 Office 365 一部分的 Exchange Online 或 Exchange 内部部署邮箱。 EWS 使用标准 web 协议来提供对 Exchange 服务器的访问权限;像[Ews 托管 API](get-started-with-ews-managed-api-client-applications.md)这样的库可包装 ews 操作，以提供面向对象的接口。 在运行本文中的示例后，您将有基本的了解可以使用 EWS 执行的操作。 
  
您可以从任何操作系统或语言调用 EWS 操作，因为 EWS 请求和响应使用 SOAP 协议。 本文中的示例使用 c # 编写，并使用 .NET Framework [HttpWebRequest](https://msdn.microsoft.com/library/System.Net.HttpWebRequest.aspx)和[HttpWebResponse](https://msdn.microsoft.com/library/System.Net.HttpWebResponse.aspx)对象;但是，代码的重要部分是用于生成 EWS 请求和从服务器返回的 XML 响应的 XML。 代码示例强调 XML 事务，而不是处理 XML。 
  
## <a name="youll-need-an-exchange-server"></a>你将需要 Exchange 服务器

如果您已经有一个 Exchange 邮箱帐户，则可以跳过此步骤。 否则，您可以使用以下选项为第一个 EWS 应用程序设置 Exchange 邮箱：
  
- [获取 Office 365 开发人员网站](https://msdn.microsoft.com/library/office/fp179924.aspx)（推荐）。 这是获取 Exchange 邮箱的最快方法。
    
- 下载 [Exchange Server](https://office.microsoft.com/exchange/microsoft-exchange-try-or-buy-exchange-we-can-help-you-decide-FX103746846.aspx?WT%2Eintid1=ODC%5FENUS%5FFX103472230%5FXT103965589)。

    
确认您可以从 Exchange 服务器发送和接收电子邮件后，即可设置您的开发环境。 您可以使用 Outlook Web App 验证您是否可以发送电子邮件。
  
您还需要知道您的服务器的 EWS 终结点的 URL。 在生产应用程序中，您可以使用[自动发现](autodiscover-for-exchange.md)来确定 EWS URL。 本文中的示例使用 Office 365 EWS 终结点 URL `https://outlook.office365.com/EWS/Exchange.asmx` 。 "[后续步骤](#bk_next)" 部分包含有关 "准备就绪时自动发现" 的详细信息的链接。 
  
如果使用具有默认自签名证书的 Exchange 服务器测试应用程序，则需要创建符合组织的安全要求的[证书验证方法](how-to-validate-a-server-certificate-for-the-ews-managed-api.md)。 
  
## <a name="set-up-your-development-environment"></a>设置开发环境

用于创建第一台 EWS 应用程序的工具取决于所使用的操作系统和语言，并且主要是一项口味的考虑事项。 如果您希望按照本文中的 c # 示例操作，您将需要： 
  
- 支持 .NET Framework 4.0 的任何版本的 Visual Studio。 
    
- 您的开发计算机可用于联系您的 Exchange 服务器的 Internet 连接。 如果您可以使用具有 DNS 名称的 Outlook Web App （而不是 IP 地址）连接到您的 Exchange 服务器，则会进行设置。
    
## <a name="create-your-first-ews-application"></a>创建您的第一个 EWS 应用程序

您将创建的 EWS 应用程序显示了使用 EWS 的两种典型方案：
  
1. 从 Exchange 邮箱中获取信息，并向用户显示该信息。
    
2. 执行操作（如发送电子邮件），并检查响应以查看操作是否成功。
    
让我们开始吧。
  
### <a name="set-up-the-solution"></a>设置解决方案

首先，使用 Visual Studio 创建一个新的控制台应用程序解决方案。 在解决方案准备就绪后，创建一个名为 Tracing.cs 的新对象。 使用此对象可将信息写入控制台和日志文件中，以便您可以在运行代码后查看结果。 将以下代码粘贴到 Tracing.cs 文件中。
  
```cs
using System;
using System.IO;
namespace Microsoft.Exchange.Samples.EWS
{
  class Tracing
  {
    private static TextWriter logFileWriter = null;
    public static void OpenLog(string fileName)
    {
      logFileWriter = new StreamWriter(fileName);
    }
    public static void Write(string format, params object[] args)
    {
      Console.Write(format, args);
      if (logFileWriter != null)
      {
        logFileWriter.Write(format, args);
      }
    }
    public static void WriteLine(string format, params object[] args)
    {
      Console.WriteLine(format, args);
      if (logFileWriter != null)
      {
        logFileWriter.WriteLine(format, args);
      }
    }
    public static void CloseLog()
    {
      logFileWriter.Flush();
      logFileWriter.Close();
    }
  }
}
```

接下来，打开 Program.cs 文件。 将示例代码的其余部分放在此文件中。
  
首先，设置程序的命令行管理程序。 程序将： 
  
1. 创建一个日志文件，以便可以将该请求和响应写入磁盘，以供后续研究使用。
    
2. 获取你将访问的帐户的电子邮件地址和密码。
    
3. 调用示例方法。
    
`Main`将 Program.cs 中的方法替换为以下代码。 
  
```cs
    static void Main(string[] args)
    {
      // Start tracing to console and a log file.
      Tracing.OpenLog("./GetStartedWithEWS.log");
      Tracing.WriteLine("EWS sample application started.");
      var isValidEmailAddress = false;
      Console.Write("Enter an email address: ");
      var emailAddress = Console.ReadLine();
      
        isValidEmailAddress = (emailAddress.Contains("@") &amp;&amp; emailAddress.Contains("."));
      if (!isValidEmailAddress)
      {
        Tracing.WriteLine("Email address " + emailAddress + " is not a valid SMTP address. Closing program.");
        return;
      }
      SecureString password = GetPasswordFromConsole();
      if (password.Length == 0)
      {
        Tracing.WriteLine("Password empty, closing program.");
      }
      NetworkCredential userCredentials = new NetworkCredential(emailAddress, password);
      // These are the sample methods that demonstrate using EWS.
      // ShowNumberOfMessagesInInbox(userCredentials);
      // SendTestEmail(userCredentials);
     
      Tracing.WriteLine("EWS sample application ends.");
      Tracing.CloseLog();
      Console.WriteLine("Press enter to exit: ");
      Console.ReadLine();
    }
    // These method stubs will be filled in later.
    private static void ShowNumberOfMessagesInInbox(NetworkCredential userCredentials)
    {
    }
    private static void SendTestEmail(NetworkCredential userCredentials)
    {
    }
```

您需要做的最后一件事是添加 `GetPasswordFromConsole` 静态方法。 此方法返回一个[SecureString](https://msdn.microsoft.com/library/System.Security.SecureString.aspx)对象，该对象包含在控制台中键入的密码。 
  
```cs
    private static SecureString GetPasswordFromConsole()
    {
      SecureString password = new SecureString();
      bool readingPassword = true;
      Console.Write("Enter password: ");
      while (readingPassword)
      {
        ConsoleKeyInfo userInput = Console.ReadKey(true);
        switch (userInput.Key)
        {
          case (ConsoleKey.Enter):
            readingPassword = false;
            break;
          case (ConsoleKey.Escape):
            password.Clear();
            readingPassword = false;
            break;
          case (ConsoleKey.Backspace):
            if (password.Length > 0)
            {
              password.RemoveAt(password.Length - 1);
              Console.SetCursorPosition(Console.CursorLeft - 1, Console.CursorTop);
              Console.Write(" ");
              Console.SetCursorPosition(Console.CursorLeft - 1, Console.CursorTop);
            }
            break;
          default:
            if (userInput.KeyChar != 0)
            {
              password.AppendChar(userInput.KeyChar);
              Console.Write("*");
            }
            break;
        }
      }
      Console.WriteLine();
      password.MakeReadOnly();
      return password;
    }
```

### <a name="get-the-number-of-new-messages-in-an-inbox"></a>获取收件箱中的新邮件数

EWS 应用程序中的常见操作是获取有关电子邮件、约会、会议和存储它们的文件夹的信息。 本示例获取帐户收件箱中的邮件数，并显示邮件总数和未读邮件数。 它演示了对 EWS 应用程序的以下常见操作：
  
- 向 Exchange 服务器发出 EWS 请求。
    
- 分析所请求的信息的返回 XML 响应。
    
- 处理常见异常和错误消息。
    
将下面的代码添加到在 `ShowNumberOfMessagesInInbox` main 方法后无存根的方法中。 运行应用程序时，它将打印帐户收件箱中的邮件数以及收件箱中未读邮件的数量。 运行应用程序后，可以打开 GetStartedWithEWS 文件，以查看发送到 Exchange 服务器的 XML 请求以及服务器返回的响应。 
  
```cs
      /// This is the XML request that is sent to the Exchange server.
      var getFolderSOAPRequest =
"<?xml version=\"1.0\" encoding=\"utf-8\"?>\n" +
"<soap:Envelope xmlns:soap=\"https://schemas.xmlsoap.org/soap/envelope/\"\n" +
"   xmlns:t=\"https://schemas.microsoft.com/exchange/services/2006/types\">\n" +
"<soap:Header>\n" +
"    <t:RequestServerVersion Version=\"Exchange2007_SP1\" />\n" +
"  </soap:Header>\n" +
"  <soap:Body>\n" +
"    <GetFolder xmlns=\"https://schemas.microsoft.com/exchange/services/2006/messages\"\n" +
"               xmlns:t=\"https://schemas.microsoft.com/exchange/services/2006/types\">\n" +
"      <FolderShape>\n" +
"        <t:BaseShape>Default</t:BaseShape>\n" +
"      </FolderShape>\n" +
"      <FolderIds>\n" +
"        <t:DistinguishedFolderId Id=\"inbox\"/>\n" +
"      </FolderIds>\n" +
"    </GetFolder>\n" +
"  </soap:Body>\n" +
"</soap:Envelope>\n";
      // Write the get folder operation request to the console and log file.
      Tracing.WriteLine("Get folder operation request:");
      Tracing.WriteLine(getFolderSOAPRequest);
      var getFolderRequest = WebRequest.CreateHttp(Office365WebServicesURL);
      getFolderRequest.AllowAutoRedirect = false;
      getFolderRequest.Credentials = userCredentials;
      getFolderRequest.Method = "POST";
      getFolderRequest.ContentType = "text/xml";
      var requestWriter = new StreamWriter(getFolderRequest.GetRequestStream());
      requestWriter.Write(getFolderSOAPRequest);
      requestWriter.Close();
      try
      {
        var getFolderResponse = (HttpWebResponse)(getFolderRequest.GetResponse());
        if (getFolderResponse.StatusCode == HttpStatusCode.OK)
        {
          var responseStream = getFolderResponse.GetResponseStream();
          XElement responseEnvelope = XElement.Load(responseStream);
          if (responseEnvelope != null)
          {
            // Write the response to the console and log file.
            Tracing.WriteLine("Response:");
            StringBuilder stringBuilder = new StringBuilder();
            XmlWriterSettings settings = new XmlWriterSettings();
            settings.Indent = true;
            XmlWriter writer = XmlWriter.Create(stringBuilder, settings);
            responseEnvelope.Save(writer);
            writer.Close();
            Tracing.WriteLine(stringBuilder.ToString());
            // Check the response for error codes. If there is an error, throw an application exception.
            IEnumerable<XElement> errorCodes = from errorCode in responseEnvelope.Descendants
                                               ("{https://schemas.microsoft.com/exchange/services/2006/messages}ResponseCode")
                                               select errorCode;
            foreach (var errorCode in errorCodes)
            {
              if (errorCode.Value != "NoError")
              {
                switch (errorCode.Parent.Name.LocalName.ToString())
                {
                  case "Response":
                    string responseError = "Response-level error getting inbox information:\n" + errorCode.Value;
                    throw new ApplicationException(responseError);
                  case "UserResponse":
                    string userError = "User-level error getting inbox information:\n" + errorCode.Value;
                    throw new ApplicationException(userError);
                }
              }
            }
            // Process the response.
            IEnumerable<XElement> folders = from folderElement in
                                              responseEnvelope.Descendants
                                              ("{https://schemas.microsoft.com/exchange/services/2006/messages}Folders")
                                            select folderElement;
            foreach (var folder in folders)
            {
              Tracing.Write("Folder name:     ");
              var folderName = from folderElement in
                                 folder.Descendants
                                 ("{https://schemas.microsoft.com/exchange/services/2006/types}DisplayName")
                               select folderElement.Value;
              Tracing.WriteLine(folderName.ElementAt(0));
              Tracing.Write("Total messages:  ");
              var totalCount = from folderElement in
                                 folder.Descendants
                                   ("{https://schemas.microsoft.com/exchange/services/2006/types}TotalCount")
                               select folderElement.Value;
              Tracing.WriteLine(totalCount.ElementAt(0));
              Tracing.Write("Unread messages: ");
              var unreadCount = from folderElement in
                                 folder.Descendants
                                   ("{https://schemas.microsoft.com/exchange/services/2006/types}UnreadCount")
                               select folderElement.Value;
              Tracing.WriteLine(unreadCount.ElementAt(0));
            }
          }
        }
      }
      catch (WebException ex)
      {
        Tracing.WriteLine("Caught Web exception:");
        Tracing.WriteLine(ex.Message);
      }
      catch (ApplicationException ex)
      {
        Tracing.WriteLine("Caught application exception:");
        Tracing.WriteLine(ex.Message);
      }

```

### <a name="send-an-email-message"></a>发送电子邮件

EWS 应用程序的另一个常见操作是发送电子邮件或会议请求。 本示例使用之前输入的用户凭据创建并发送一封电子邮件。 它演示了这些常见的 EWS 应用程序任务：
  
- 创建和发送电子邮件。
    
- 分析返回的 XML 响应以确定是否已正确发送电子邮件。
    
- 处理常见异常和错误消息。
    
将以下代码添加到 SendTestEmail 方法，该方法在 main 方法之后无存根。 运行应用程序后，可以打开 GetStartedWithEWS 文件，以查看发送到 Exchange 服务器的 XML 请求以及服务器返回的响应。
  
```cs
var createItemSOAPRequest =
      "<?xml version=\"1.0\" encoding=\"utf-8\"?>\n" +
      "<soap:Envelope xmlns:xsi=\"http://www.w3.org/2001/XMLSchema-instance\" \n" +
      "               xmlns:m=\"https://schemas.microsoft.com/exchange/services/2006/messages\" \n" +
      "               xmlns:t=\"https://schemas.microsoft.com/exchange/services/2006/types\" \n" +
      "               xmlns:soap=\"https://schemas.xmlsoap.org/soap/envelope/\">\n" +
      "  <soap:Header>\n" +
      "    <t:RequestServerVersion Version=\"Exchange2007_SP1\" />\n" +
      "  </soap:Header>\n" +
      "  <soap:Body>\n" +
      "    <m:CreateItem MessageDisposition=\"SendAndSaveCopy\">\n" +
      "      <m:SavedItemFolderId>\n" +
      "        <t:DistinguishedFolderId Id=\"sentitems\" />\n" +
      "      </m:SavedItemFolderId>\n" +
      "      <m:Items>\n" +
      "        <t:Message>\n" +
      "          <t:Subject>Company Soccer Team</t:Subject>\n" +
      "          <t:Body BodyType=\"HTML\">Are you interested in joining?</t:Body>\n" +
      "          <t:ToRecipients>\n" +
      "            <t:Mailbox>\n" +
      "              <t:EmailAddress>sadie@contoso.com</t:EmailAddress>\n" +
      "              </t:Mailbox>\n" +
      "          </t:ToRecipients>\n" +
      "        </t:Message>\n" +
      "      </m:Items>\n" +
      "    </m:CreateItem>\n" +
      "  </soap:Body>\n" +
      "</soap:Envelope>\n";
      // Write the create item operation request to the console and log file.
      Tracing.WriteLine("Get folder operation request:");
      Tracing.WriteLine(createItemSOAPRequest);
      var getFolderRequest = WebRequest.CreateHttp(Office365WebServicesURL);
      getFolderRequest.AllowAutoRedirect = false;
      getFolderRequest.Credentials = userCredentials;
      getFolderRequest.Method = "POST";
      getFolderRequest.ContentType = "text/xml";
      var requestWriter = new StreamWriter(getFolderRequest.GetRequestStream());
      requestWriter.Write(createItemSOAPRequest);
      requestWriter.Close();
      try
      {
        var getFolderResponse = (HttpWebResponse)(getFolderRequest.GetResponse());
        if (getFolderResponse.StatusCode == HttpStatusCode.OK)
        {
          var responseStream = getFolderResponse.GetResponseStream();
          XElement responseEnvelope = XElement.Load(responseStream);
          if (responseEnvelope != null)
          {
            // Write the response to the console and log file.
            Tracing.WriteLine("Response:");
            StringBuilder stringBuilder = new StringBuilder();
            XmlWriterSettings settings = new XmlWriterSettings();
            settings.Indent = true;
            XmlWriter writer = XmlWriter.Create(stringBuilder, settings);
            responseEnvelope.Save(writer);
            writer.Close();
            Tracing.WriteLine(stringBuilder.ToString());
            // Check the response for error codes. If there is an error, throw an application exception.
            IEnumerable<XElement> errorCodes = from errorCode in responseEnvelope.Descendants
                                               ("{https://schemas.microsoft.com/exchange/services/2006/messages}ResponseCode")
                                               select errorCode;
            foreach (var errorCode in errorCodes)
            {
              if (errorCode.Value != "NoError")
              {
                switch (errorCode.Parent.Name.LocalName.ToString())
                {
                  case "Response":
                    string responseError = "Response-level error getting inbox information:\n" + errorCode.Value;
                    throw new ApplicationException(responseError);
                  case "UserResponse":
                    string userError = "User-level error getting inbox information:\n" + errorCode.Value;
                    throw new ApplicationException(userError);
                }
              }
            }
            Tracing.WriteLine("Message sent successfully.");
          }
        }
      }
      catch (WebException ex)
      {
        Tracing.WriteLine("Caught Web exception:");
        Tracing.WriteLine(ex.Message);
      }
      catch (ApplicationException ex)
      {
        Tracing.WriteLine("Caught application exception:");
        Tracing.WriteLine(ex.Message);
      }
```

<a name="bk_next"></a>

## <a name="next-steps"></a>后续步骤

现在，您已编写了第一个 EWS 应用程序，您就可以发现其他使用 EWS 的方法了。 下面是一些可让你入门的建议：
  
- 在应用程序中实现[自动发现](autodiscover-for-exchange.md)，以便应用程序将根据用户的电子邮件地址连接到正确的 Exchange 服务器。 另请参阅[Exchange 2013：使用自动发现示例获取用户设置](https://code.msdn.microsoft.com/Exchange-2013-Get-user-7e22c86e)。 
    
- 有关 EWS 的详细信息，请参阅[ews 参考](https://msdn.microsoft.com/library/2a873474-1bb2-4cb1-a556-40e8c4159f4a%28Office.15%29.aspx)。 
    
- 有关可用操作的信息，请参阅[EWS 操作](https://msdn.microsoft.com/library/cf6fd871-9a65-4f34-8557-c8c71dd7ce09%28Office.15%29.aspx)。 
    
- 使用[EWS 编辑器](http://ewseditor.codeplex.com/)查看发送到服务器和从服务器发送的 SOAP 流量。 
    
如果你的应用程序遇到任何问题，请[尝试在论坛中发布问题或评论](https://social.technet.microsoft.com/Forums/exchange/home?forum=exchangesvrdevelopment)（不要忘记阅读第一篇文章）。 
  
## <a name="see-also"></a>另请参阅

- [开始使用 Exchange 中的 Web 服务](start-using-web-services-in-exchange.md)   
- [在 Exchange 中浏览 EWS 托管 API、EWS 和 Web 服务](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) 
- [Exchange 的 EWS 客户端设计概述](ews-client-design-overview-for-exchange.md)   
- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)  
- [EWS 托管 API 客户端应用程序入门](get-started-with-ews-managed-api-client-applications.md)
    