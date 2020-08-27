---
title: EWS 客户端应用程序入门
manager: sethgros
ms.date: 8/26/2020
ms.audience: Developer
ms.assetid: e6fd5c23-0ba5-4a7b-bdde-4a553447069f
description: 使用 Exchange 中的 Exchange Web 服务（EWS），创建你的第一个应用程序。
localization_priority: Priority
ms.openlocfilehash: 81d4cb69d20f17945658ab4ad16c9fe3a47d4eec
ms.sourcegitcommit: 636c05a929279812c6ef87d75b01c166a4a05584
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/26/2020
ms.locfileid: "47254977"
---
# <a name="get-started-with-ews-client-applications"></a>EWS 客户端应用程序入门

使用 Exchange 中的 Exchange Web 服务（EWS），创建你的第一个应用程序。
  
EWS 是一种全面的服务，应用程序可以使用 EWS 来访问几乎所有存储在 Exchange Online、作为 Office 365 一部分的 Exchange Online 或 Exchange 本地邮箱中的信息。 EWS 使用标准 Web 协议，对 Exchange 服务器提供访问权限；诸如 [EWS 托管 API](get-started-with-ews-managed-api-client-applications.md) 等库会环绕 EWS 操作，提供面向对象的界面。 运行本文中的示例后，你将基本了解可以使用 EWS 执行的操作。 
  
可从任意操作系统或语言中调用 EWS 操作，因为 EWS 请求和响应使用 SOAP 协议。 本文中的示例编写自 C# ，并利用了 .NET Frameork [HttpWebRequest](https://msdn.microsoft.com/library/System.Net.HttpWebRequest.aspx) 和 [HttpWebResponse](https://msdn.microsoft.com/library/System.Net.HttpWebResponse.aspx) 对象；但是，代码的重要部分是用于构建 EWS 请求的 XML，以及从服务器返回的 XML 响应。 代码示例强调 XML 事务，和不处理 XML。 
  
## <a name="youll-need-an-exchange-server"></a>你将需要 Exchange 服务器

如果你已经有一个 Exchange 邮箱帐户，则可以跳过此步骤。 否则，你必须具备以下选项来为密的首个 EWS 应用程序设置 Exchange 邮箱：
  
- [获取 Office 365 开发人员网站](https://developer.microsoft.com/microsoft-365/dev-program)（推荐）。 这是你获取 Exchange 邮箱的最快方法。
    
- 下载 [Exchange Server](https://office.microsoft.com/exchange/microsoft-exchange-try-or-buy-exchange-we-can-help-you-decide-FX103746846.aspx?WT%2Eintid1=ODC%5FENUS%5FFX103472230%5FXT103965589)。

    
在你确认可以从 Exchange 服务器发送和接收电子邮件后，你便可以设置你的开发环境了。 可以使用 Outlook Web App 来验证你是否可以发送电子邮件。
  
你还需要了解服务器的 EWS 端点 URL。 在制作应用程序的过程中，你会使用 “[自动发现](autodiscover-for-exchange.md)” 来确定 EWS URL。 本文中的示例使用 Office 365 EWS 端点 URL，`https://outlook.office365.com/EWS/Exchange.asmx`。 等你准备好以后，“[后续步骤](#bk_next)” 部分中有更多关于“自动发现”详细信息的链接。 
  
如果使用具有默认自签名证书的 Exchange 服务器测试应用程序，则需要创建符合组织安全要求的 [证书验证方法](how-to-validate-a-server-certificate-for-the-ews-managed-api.md)。 
  
## <a name="set-up-your-development-environment"></a>设置开发环境

用于创建首个 EWS 应用程序的工具取决于所使用的操作系统和语言，这大多只是个人喜好问题。 如果你想跟着沿用本文中的 C# 示例，你将需要： 
  
- 支持 .NET Framework 4.0 的任何 Visual Studio 版本。 
    
- 可让开发计算机联系 Exchange 服务器的 Internet 连接。 如果你可以使用 Outlook Web App 和 DNS 名称，而不是 IP 地址来连接 Exchange 服务器的话，则代表你已经设置好了。
    
## <a name="create-your-first-ews-application"></a>创建你的第一个 EWS 应用程序

要创建的 EWS 应用程序会显示使用 EWS 的两种典型方案：
  
1. 从 Exchange 邮箱获取信息并向用户显示该信息。
    
2. 执行一个操作（如发送电子邮件），然后检查响应以查看操作是否成功。
    
让我们开始吧。
  
### <a name="set-up-the-solution"></a>设置解决方案

首先，使用 Visual Studio 创建一个新的控制台应用程序解决方案。 解决方案准备就绪后，创建名为 Tracing.cs 的新对象。 使用此对象向控制台和日志文件写入信息，这样你就可以在运行代码后查看结果。 将以下代码粘贴到 Tracing.cs 文件中。
  
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

接下来，打开 Program.cs 文件。 将此示例中代码的其余部分放入此文件中。
  
首先，设置程序的外壳。 程序将： 
  
1. 创建日志文件，以便可将请求和响应写入磁盘，供日后研究。
    
2. 获取你将访问的帐户的电子邮件地址和密码。
    
3. 调用示例方法。
    
将 Program.cs 中的 `Main` 方法替换成以下代码。 
  
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

最后要做的事就是添加  `GetPasswordFromConsole` 静态方法。 此方法会返回一个 [SecureString](https://msdn.microsoft.com/library/System.Security.SecureString.aspx) 对象，它包含在控制台中键入的密码。 
  
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

### <a name="get-the-number-of-new-messages-in-an-inbox"></a>获取“收件箱”中的新邮件数

EWS 应用程序中的常见操作是获取有关电子邮件、约会、会议和存储它们的文件夹的信息。 此示例会获取帐户“收件箱”中的邮件数量，并显示邮件总数和未读邮件数。 它演示了以下这些 EWS 应用程序的常见操作：
  
- 向 Exchange 服务器发出 EWS 请求。
    
- 为所请求的信息分析返回的 XML 响应。
    
- 处理常见异常和错误消息。
    
将下面的代码添加到  `ShowNumberOfMessagesInInbox` 方法中，该方法是主方法后的存根。 运行应用程序时，它将打印帐户“收件箱”中的邮件数和“收件箱”中的未读邮件数。 运行应用程序后，可以打开 GetStartedWithEWS.log 文件，查看发送到 Exchange 服务器的 XML 请求和服务器返回的响应。 
  
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

### <a name="send-an-email-message"></a>发送电子邮件消息

EWS 应用程序的另一个常见操作是发送电子邮件或会议请求。 此示例使用之前所输入的用户凭据，创建并发送电子邮件。 它演示了这些常见的 EWS 应用程序任务：
  
- 创建和发送电子邮件。
    
- 分析返回的 XML 响应，确定是否已正确发送电子邮件。
    
- 处理常见异常和错误消息。
    
将下面的代码添加到 SendTestEmail 方法中，该方法是主方法后的存根。 运行应用程序后，可以打开 GetStartedWithEWS.log 文件，查看发送到 Exchange 服务器的 XML 请求和服务器返回的响应。
  
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

现在你已编写了你的首个 EWS 应用程序，这就代表你已经准备好发现使用 EWS 的其他方法了。 以下是一些帮助你开始使用的思路：
  
- 在应用程序中实施“[自动发现](autodiscover-for-exchange.md)” ，以便应用程序可以根据用户的电子邮件地址连接到正确的 Exchange 服务器。 另请参阅 [Exchange 2013：通过“自动发现”获取用户设置](https://code.msdn.microsoft.com/Exchange-2013-Get-user-7e22c86e) 示例。 
    
- 有关更多关于 EWS 的详细信息，请参阅 [EWS 参考](https://msdn.microsoft.com/library/2a873474-1bb2-4cb1-a556-40e8c4159f4a%28Office.15%29.aspx)。 
    
- 有关可用操作的信息，请参阅 [EWS 操作](https://msdn.microsoft.com/library/cf6fd871-9a65-4f34-8557-c8c71dd7ce09%28Office.15%29.aspx)。 
    
- 使用 [EWS 编辑器](http://ewseditor.codeplex.com/)，查看发送到和发送自服务器的 SOAP 流量。 
    
如果你的应用程序遇到任何问题，[请尝试在论坛中发布问题或评论](https://social.technet.microsoft.com/Forums/exchange/home?forum=exchangesvrdevelopment)（别忘了阅读第一个帖子）。 
  
## <a name="see-also"></a>另请参阅

- [开始使用 Exchange 中的 Web 服务](start-using-web-services-in-exchange.md)   
- [在 Exchange 中浏览 EWS 托管 API、EWS 和 Web 服务](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) 
- [Exchange 的 EWS 客户端设计概述](ews-client-design-overview-for-exchange.md)   
- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)  
- [EWS 托管 API 客户端应用程序入门](get-started-with-ews-managed-api-client-applications.md)
    
