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
# <a name="get-started-with-ews-client-applications"></a><span data-ttu-id="b7d1b-103">EWS 客户端应用程序入门</span><span class="sxs-lookup"><span data-stu-id="b7d1b-103">Get started with EWS client applications</span></span>

<span data-ttu-id="b7d1b-104">使用 Exchange 中的 Exchange Web 服务（EWS），创建你的第一个应用程序。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-104">Create your first application by using Exchange Web Services (EWS) in Exchange.</span></span>
  
<span data-ttu-id="b7d1b-105">EWS 是一种全面的服务，应用程序可以使用 EWS 来访问几乎所有存储在 Exchange Online、作为 Office 365 一部分的 Exchange Online 或 Exchange 本地邮箱中的信息。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-105">EWS is a comprehensive service that your applications can use to access almost all the information stored in an Exchange Online, Exchange Online as part of Office 365, or Exchange on-premises mailbox.</span></span> <span data-ttu-id="b7d1b-106">EWS 使用标准 Web 协议，对 Exchange 服务器提供访问权限；诸如 [EWS 托管 API](get-started-with-ews-managed-api-client-applications.md) 等库会环绕 EWS 操作，提供面向对象的界面。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-106">EWS uses standard web protocols to provide access to an Exchange server; libraries like the [EWS Managed API](get-started-with-ews-managed-api-client-applications.md) wrap the EWS operations to provide an object-oriented interface.</span></span> <span data-ttu-id="b7d1b-107">运行本文中的示例后，你将基本了解可以使用 EWS 执行的操作。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-107">After you've run the examples in this article, you will have a basic understanding of what you can do with EWS.</span></span> 
  
<span data-ttu-id="b7d1b-108">可从任意操作系统或语言中调用 EWS 操作，因为 EWS 请求和响应使用 SOAP 协议。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-108">You can call EWS operations from any operating system or language, because the EWS requests and responses use the SOAP protocol.</span></span> <span data-ttu-id="b7d1b-109">本文中的示例编写自 C# ，并利用了 .NET Frameork [HttpWebRequest](https://msdn.microsoft.com/library/System.Net.HttpWebRequest.aspx) 和 [HttpWebResponse](https://msdn.microsoft.com/library/System.Net.HttpWebResponse.aspx) 对象；但是，代码的重要部分是用于构建 EWS 请求的 XML，以及从服务器返回的 XML 响应。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-109">The examples in this article are written using C# and make use of the .NET Framework [HttpWebRequest](https://msdn.microsoft.com/library/System.Net.HttpWebRequest.aspx) and [HttpWebResponse](https://msdn.microsoft.com/library/System.Net.HttpWebResponse.aspx) objects; however, the important part of the code is the XML used to make the EWS request and the XML response returned from the server.</span></span> <span data-ttu-id="b7d1b-110">代码示例强调 XML 事务，和不处理 XML。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-110">The code examples emphasize the XML transactions and not processing the XML.</span></span> 
  
## <a name="youll-need-an-exchange-server"></a><span data-ttu-id="b7d1b-111">你将需要 Exchange 服务器</span><span class="sxs-lookup"><span data-stu-id="b7d1b-111">You'll need an Exchange server</span></span>

<span data-ttu-id="b7d1b-112">如果你已经有一个 Exchange 邮箱帐户，则可以跳过此步骤。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-112">If you already have an Exchange mailbox account, you can skip this step.</span></span> <span data-ttu-id="b7d1b-113">否则，你必须具备以下选项来为密的首个 EWS 应用程序设置 Exchange 邮箱：</span><span class="sxs-lookup"><span data-stu-id="b7d1b-113">Otherwise, you have the following options for setting up an Exchange mailbox for your first EWS application:</span></span>
  
- <span data-ttu-id="b7d1b-114">[获取 Office 365 开发人员网站](https://developer.microsoft.com/microsoft-365/dev-program)（推荐）。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-114">[Get an Office 365 Developer Site ](https://developer.microsoft.com/microsoft-365/dev-program)(recommended).</span></span> <span data-ttu-id="b7d1b-115">这是你获取 Exchange 邮箱的最快方法。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-115">This is the quickest way for you to get an Exchange mailbox.</span></span>
    
- <span data-ttu-id="b7d1b-116">下载 [Exchange Server](https://office.microsoft.com/exchange/microsoft-exchange-try-or-buy-exchange-we-can-help-you-decide-FX103746846.aspx?WT%2Eintid1=ODC%5FENUS%5FFX103472230%5FXT103965589)。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-116">Download [Exchange Server](https://office.microsoft.com/exchange/microsoft-exchange-try-or-buy-exchange-we-can-help-you-decide-FX103746846.aspx?WT%2Eintid1=ODC%5FENUS%5FFX103472230%5FXT103965589).</span></span>

    
<span data-ttu-id="b7d1b-117">在你确认可以从 Exchange 服务器发送和接收电子邮件后，你便可以设置你的开发环境了。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-117">After you've verified that you can send and receive email from your Exchange server you are ready to set up your development environment.</span></span> <span data-ttu-id="b7d1b-118">可以使用 Outlook Web App 来验证你是否可以发送电子邮件。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-118">You can use Outlook Web App to verify that you can send email.</span></span>
  
<span data-ttu-id="b7d1b-119">你还需要了解服务器的 EWS 端点 URL。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-119">You'll also need to know the URL of the EWS endpoint for your server.</span></span> <span data-ttu-id="b7d1b-120">在制作应用程序的过程中，你会使用 “[自动发现](autodiscover-for-exchange.md)” 来确定 EWS URL。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-120">In a production application, you'd use [Autodiscover](autodiscover-for-exchange.md) to determine the EWS URL.</span></span> <span data-ttu-id="b7d1b-121">本文中的示例使用 Office 365 EWS 端点 URL，`https://outlook.office365.com/EWS/Exchange.asmx`。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-121">The examples in this article use the Office 365 EWS endpoint URL, `https://outlook.office365.com/EWS/Exchange.asmx`.</span></span> <span data-ttu-id="b7d1b-122">等你准备好以后，“[后续步骤](#bk_next)” 部分中有更多关于“自动发现”详细信息的链接。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-122">The [Next steps](#bk_next) section has links to more information about Autodiscover when you're ready.</span></span> 
  
<span data-ttu-id="b7d1b-123">如果使用具有默认自签名证书的 Exchange 服务器测试应用程序，则需要创建符合组织安全要求的 [证书验证方法](how-to-validate-a-server-certificate-for-the-ews-managed-api.md)。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-123">If you are testing your application using an Exchange server that has the default self-signed certificate, you'll need to create a [certificate validation method](how-to-validate-a-server-certificate-for-the-ews-managed-api.md) that meets the security requirements of your organization.</span></span> 
  
## <a name="set-up-your-development-environment"></a><span data-ttu-id="b7d1b-124">设置开发环境</span><span class="sxs-lookup"><span data-stu-id="b7d1b-124">Set up your development environment</span></span>

<span data-ttu-id="b7d1b-125">用于创建首个 EWS 应用程序的工具取决于所使用的操作系统和语言，这大多只是个人喜好问题。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-125">The tools that you use to create your first EWS application depend on the operating system and language that you use, and are mostly a matter of taste.</span></span> <span data-ttu-id="b7d1b-126">如果你想跟着沿用本文中的 C# 示例，你将需要：</span><span class="sxs-lookup"><span data-stu-id="b7d1b-126">If you want to follow along with the C# examples in this article, you'll need:</span></span> 
  
- <span data-ttu-id="b7d1b-127">支持 .NET Framework 4.0 的任何 Visual Studio 版本。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-127">Any version of Visual Studio that supports the .NET Framework 4.0.</span></span> 
    
- <span data-ttu-id="b7d1b-128">可让开发计算机联系 Exchange 服务器的 Internet 连接。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-128">An Internet connection that your development machine can use to contact your Exchange server.</span></span> <span data-ttu-id="b7d1b-129">如果你可以使用 Outlook Web App 和 DNS 名称，而不是 IP 地址来连接 Exchange 服务器的话，则代表你已经设置好了。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-129">If you can use Outlook Web App with a DNS name rather than an IP address to connect to your Exchange server, you are set up.</span></span>
    
## <a name="create-your-first-ews-application"></a><span data-ttu-id="b7d1b-130">创建你的第一个 EWS 应用程序</span><span class="sxs-lookup"><span data-stu-id="b7d1b-130">Create your first EWS application</span></span>

<span data-ttu-id="b7d1b-131">要创建的 EWS 应用程序会显示使用 EWS 的两种典型方案：</span><span class="sxs-lookup"><span data-stu-id="b7d1b-131">The EWS application that you will create shows two typical scenarios for using EWS:</span></span>
  
1. <span data-ttu-id="b7d1b-132">从 Exchange 邮箱获取信息并向用户显示该信息。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-132">Get information from an Exchange mailbox and display that information to the user.</span></span>
    
2. <span data-ttu-id="b7d1b-133">执行一个操作（如发送电子邮件），然后检查响应以查看操作是否成功。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-133">Perform an action, such as sending an email, and check the response to see if the action succeeded.</span></span>
    
<span data-ttu-id="b7d1b-134">让我们开始吧。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-134">Let's get started.</span></span>
  
### <a name="set-up-the-solution"></a><span data-ttu-id="b7d1b-135">设置解决方案</span><span class="sxs-lookup"><span data-stu-id="b7d1b-135">Set up the solution</span></span>

<span data-ttu-id="b7d1b-136">首先，使用 Visual Studio 创建一个新的控制台应用程序解决方案。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-136">First, create a new console application solution using Visual Studio.</span></span> <span data-ttu-id="b7d1b-137">解决方案准备就绪后，创建名为 Tracing.cs 的新对象。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-137">When the solution is ready, create a new object called Tracing.cs.</span></span> <span data-ttu-id="b7d1b-138">使用此对象向控制台和日志文件写入信息，这样你就可以在运行代码后查看结果。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-138">Use this object to write information to both the console and a log file so that you can review the results after you run your code.</span></span> <span data-ttu-id="b7d1b-139">将以下代码粘贴到 Tracing.cs 文件中。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-139">Paste the following code into the Tracing.cs file.</span></span>
  
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

<span data-ttu-id="b7d1b-140">接下来，打开 Program.cs 文件。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-140">Next, open the Program.cs file.</span></span> <span data-ttu-id="b7d1b-141">将此示例中代码的其余部分放入此文件中。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-141">You will put the rest of the code for the example in this file.</span></span>
  
<span data-ttu-id="b7d1b-142">首先，设置程序的外壳。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-142">First, set up the shell of the program.</span></span> <span data-ttu-id="b7d1b-143">程序将：</span><span class="sxs-lookup"><span data-stu-id="b7d1b-143">The program will:</span></span> 
  
1. <span data-ttu-id="b7d1b-144">创建日志文件，以便可将请求和响应写入磁盘，供日后研究。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-144">Create a log file so that the request and response can be written to disk for later study.</span></span>
    
2. <span data-ttu-id="b7d1b-145">获取你将访问的帐户的电子邮件地址和密码。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-145">Get the email address and password of the account that you'll access.</span></span>
    
3. <span data-ttu-id="b7d1b-146">调用示例方法。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-146">Call the sample methods.</span></span>
    
<span data-ttu-id="b7d1b-147">将 Program.cs 中的 `Main` 方法替换成以下代码。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-147">Replace the  `Main` method in the Program.cs with the following code.</span></span> 
  
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

<span data-ttu-id="b7d1b-148">最后要做的事就是添加  `GetPasswordFromConsole` 静态方法。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-148">The last thing that you need to do is add the  `GetPasswordFromConsole` static method.</span></span> <span data-ttu-id="b7d1b-149">此方法会返回一个 [SecureString](https://msdn.microsoft.com/library/System.Security.SecureString.aspx) 对象，它包含在控制台中键入的密码。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-149">This method returns a [SecureString](https://msdn.microsoft.com/library/System.Security.SecureString.aspx) object that contains a password typed at the console.</span></span> 
  
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

### <a name="get-the-number-of-new-messages-in-an-inbox"></a><span data-ttu-id="b7d1b-150">获取“收件箱”中的新邮件数</span><span class="sxs-lookup"><span data-stu-id="b7d1b-150">Get the number of new messages in an Inbox</span></span>

<span data-ttu-id="b7d1b-151">EWS 应用程序中的常见操作是获取有关电子邮件、约会、会议和存储它们的文件夹的信息。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-151">A common operation in an EWS application is to get information about email messages, appointments, meetings, and the folders that store them.</span></span> <span data-ttu-id="b7d1b-152">此示例会获取帐户“收件箱”中的邮件数量，并显示邮件总数和未读邮件数。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-152">This example gets the number of messages in an account's Inbox and displays the total number of messages and the number of unread messages.</span></span> <span data-ttu-id="b7d1b-153">它演示了以下这些 EWS 应用程序的常见操作：</span><span class="sxs-lookup"><span data-stu-id="b7d1b-153">It demonstrates the following common actions for EWS applications:</span></span>
  
- <span data-ttu-id="b7d1b-154">向 Exchange 服务器发出 EWS 请求。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-154">Making an EWS request to the Exchange server.</span></span>
    
- <span data-ttu-id="b7d1b-155">为所请求的信息分析返回的 XML 响应。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-155">Parsing the returned XML response for the requested information.</span></span>
    
- <span data-ttu-id="b7d1b-156">处理常见异常和错误消息。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-156">Handling common exceptions and error messages.</span></span>
    
<span data-ttu-id="b7d1b-157">将下面的代码添加到  `ShowNumberOfMessagesInInbox` 方法中，该方法是主方法后的存根。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-157">Add the following code to the  `ShowNumberOfMessagesInInbox` method that was stubbed out after the main method.</span></span> <span data-ttu-id="b7d1b-158">运行应用程序时，它将打印帐户“收件箱”中的邮件数和“收件箱”中的未读邮件数。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-158">When you run the application, it will print the number of messages in the account's Inbox and the number of unread messages in the Inbox.</span></span> <span data-ttu-id="b7d1b-159">运行应用程序后，可以打开 GetStartedWithEWS.log 文件，查看发送到 Exchange 服务器的 XML 请求和服务器返回的响应。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-159">After you run the application, you can open the GetStartedWithEWS.log file to see the XML request that was sent to the Exchange server and the response that the server returned.</span></span> 
  
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

### <a name="send-an-email-message"></a><span data-ttu-id="b7d1b-160">发送电子邮件消息</span><span class="sxs-lookup"><span data-stu-id="b7d1b-160">Send an email message</span></span>

<span data-ttu-id="b7d1b-161">EWS 应用程序的另一个常见操作是发送电子邮件或会议请求。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-161">Another common operation for an EWS application is to send email messages or meeting requests.</span></span> <span data-ttu-id="b7d1b-162">此示例使用之前所输入的用户凭据，创建并发送电子邮件。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-162">This example creates and sends an email message using the user credentials that were entered earlier.</span></span> <span data-ttu-id="b7d1b-163">它演示了这些常见的 EWS 应用程序任务：</span><span class="sxs-lookup"><span data-stu-id="b7d1b-163">It demonstrates these common EWS application tasks:</span></span>
  
- <span data-ttu-id="b7d1b-164">创建和发送电子邮件。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-164">Creating and sending an email.</span></span>
    
- <span data-ttu-id="b7d1b-165">分析返回的 XML 响应，确定是否已正确发送电子邮件。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-165">Parsing the returned XML response to determine if the email was correctly sent.</span></span>
    
- <span data-ttu-id="b7d1b-166">处理常见异常和错误消息。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-166">Handling common exceptions and error messages.</span></span>
    
<span data-ttu-id="b7d1b-167">将下面的代码添加到 SendTestEmail 方法中，该方法是主方法后的存根。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-167">Add the following code to the SendTestEmail method that was stubbed out after the main method.</span></span> <span data-ttu-id="b7d1b-168">运行应用程序后，可以打开 GetStartedWithEWS.log 文件，查看发送到 Exchange 服务器的 XML 请求和服务器返回的响应。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-168">After you run the application, you can open the GetStartedWithEWS.log file to see the XML request that was sent to the Exchange server and the response that the server returned.</span></span>
  
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

## <a name="next-steps"></a><span data-ttu-id="b7d1b-169">后续步骤</span><span class="sxs-lookup"><span data-stu-id="b7d1b-169">Next steps</span></span>

<span data-ttu-id="b7d1b-170">现在你已编写了你的首个 EWS 应用程序，这就代表你已经准备好发现使用 EWS 的其他方法了。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-170">Now that you've written your first EWS application, you're ready to discover other ways to use EWS.</span></span> <span data-ttu-id="b7d1b-171">以下是一些帮助你开始使用的思路：</span><span class="sxs-lookup"><span data-stu-id="b7d1b-171">Here are some ideas to get you started:</span></span>
  
- <span data-ttu-id="b7d1b-172">在应用程序中实施“[自动发现](autodiscover-for-exchange.md)” ，以便应用程序可以根据用户的电子邮件地址连接到正确的 Exchange 服务器。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-172">Implement [Autodiscover](autodiscover-for-exchange.md) in your application so that your application will connect to the correct Exchange server based on the user's email address.</span></span> <span data-ttu-id="b7d1b-173">另请参阅 [Exchange 2013：通过“自动发现”获取用户设置](https://code.msdn.microsoft.com/Exchange-2013-Get-user-7e22c86e) 示例。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-173">See also the [Exchange 2013: Get user settings with Autodiscover](https://code.msdn.microsoft.com/Exchange-2013-Get-user-7e22c86e) sample.</span></span> 
    
- <span data-ttu-id="b7d1b-174">有关更多关于 EWS 的详细信息，请参阅 [EWS 参考](https://msdn.microsoft.com/library/2a873474-1bb2-4cb1-a556-40e8c4159f4a%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-174">Look at the [EWS reference](https://msdn.microsoft.com/library/2a873474-1bb2-4cb1-a556-40e8c4159f4a%28Office.15%29.aspx) for more information about EWS.</span></span> 
    
- <span data-ttu-id="b7d1b-175">有关可用操作的信息，请参阅 [EWS 操作](https://msdn.microsoft.com/library/cf6fd871-9a65-4f34-8557-c8c71dd7ce09%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-175">See the [EWS operations](https://msdn.microsoft.com/library/cf6fd871-9a65-4f34-8557-c8c71dd7ce09%28Office.15%29.aspx) for information about the operations that are available.</span></span> 
    
- <span data-ttu-id="b7d1b-176">使用 [EWS 编辑器](http://ewseditor.codeplex.com/)，查看发送到和发送自服务器的 SOAP 流量。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-176">Use [EWS Editor](http://ewseditor.codeplex.com/) to see the SOAP traffic sent to and from the server.</span></span> 
    
<span data-ttu-id="b7d1b-177">如果你的应用程序遇到任何问题，[请尝试在论坛中发布问题或评论](https://social.technet.microsoft.com/Forums/exchange/home?forum=exchangesvrdevelopment)（别忘了阅读第一个帖子）。</span><span class="sxs-lookup"><span data-stu-id="b7d1b-177">If you run into any issues with your application, [try posting a question or comment in the forum](https://social.technet.microsoft.com/Forums/exchange/home?forum=exchangesvrdevelopment) (and don't forget to read the first post).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b7d1b-178">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b7d1b-178">See also</span></span>

- [<span data-ttu-id="b7d1b-179">开始使用 Exchange 中的 Web 服务</span><span class="sxs-lookup"><span data-stu-id="b7d1b-179">Start using web services in Exchange</span></span>](start-using-web-services-in-exchange.md)   
- [<span data-ttu-id="b7d1b-180">在 Exchange 中浏览 EWS 托管 API、EWS 和 Web 服务</span><span class="sxs-lookup"><span data-stu-id="b7d1b-180">Explore the EWS Managed API, EWS, and web services in Exchange</span></span>](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) 
- [<span data-ttu-id="b7d1b-181">Exchange 的 EWS 客户端设计概述</span><span class="sxs-lookup"><span data-stu-id="b7d1b-181">EWS client design overview for Exchange</span></span>](ews-client-design-overview-for-exchange.md)   
- [<span data-ttu-id="b7d1b-182">开发 Exchange Web 服务客户端</span><span class="sxs-lookup"><span data-stu-id="b7d1b-182">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)  
- [<span data-ttu-id="b7d1b-183">EWS 托管 API 客户端应用程序入门</span><span class="sxs-lookup"><span data-stu-id="b7d1b-183">Get started with EWS Managed API client applications</span></span>](get-started-with-ews-managed-api-client-applications.md)
    
