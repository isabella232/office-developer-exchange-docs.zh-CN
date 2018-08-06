---
title: EWS 托管 API 客户端应用程序入门
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: c2267733-6f4f-49e5-9614-1e4a24c3af1a
description: 使用 EWS 托管 API 针对 Exchange 开发一个简单的 Hello World 电子邮件客户端应用程序。
ms.openlocfilehash: b4254ab80b4dfc2c8fadf90c79d57517c3a0bb16
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353985"
---
# <a name="get-started-with-ews-managed-api-client-applications"></a><span data-ttu-id="39503-103">EWS 托管 API 客户端应用程序入门</span><span class="sxs-lookup"><span data-stu-id="39503-103">Get started with EWS Managed API client applications</span></span>

<span data-ttu-id="39503-104">使用 EWS 托管 API 针对 Exchange 开发一个简单的 Hello World 电子邮件客户端应用程序。</span><span class="sxs-lookup"><span data-stu-id="39503-104">Develop a simple Hello World email client application for Exchange by using the EWS Managed API.</span></span> 
  
<span data-ttu-id="39503-p101">[EWS 托管 API](http://aka.ms/ews-managed-api-readme) 提供一个直观易用的对象模型，可用于发送和接收来自客户端应用程序、门户应用程序和服务应用程序的 Web 服务消息。您可以使用 EWS 托管 API 访问 Exchange Online、作为 Office 365 一部分的 Exchange Online 或 Exchange 服务器邮箱中存储的几乎所有信息。您可以使用本文中的信息以帮助您开发首个 EWS 托管 API 客户端应用程序。</span><span class="sxs-lookup"><span data-stu-id="39503-p101">The [EWS Managed API](http://aka.ms/ews-managed-api-readme) provides an intuitive, easy-to-use object model for sending and receiving web service messages from client applications, portal applications, and service applications. You can access almost all the information stored in an Exchange Online, Exchange Online as part of Office 365, or an Exchange server mailbox by using the EWS Managed API. You can use the information in this article to help you develop your first EWS Managed API client application.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="39503-108">EWS 托管 API 现已作为 [GitHub](https://github.com/officedev/ews-managed-api) 上的开源项目推出。</span><span class="sxs-lookup"><span data-stu-id="39503-108">The EWS Managed API is now available as an open source project on [GitHub](https://github.com/officedev/ews-managed-api).</span></span> <span data-ttu-id="39503-109">你可以使用开源库进行以下操作：</span><span class="sxs-lookup"><span data-stu-id="39503-109">You can use the open source library to: >  Contribute bug fixes and enhancements to the API.</span></span> 
> - <span data-ttu-id="39503-110">为 API 提供缺陷修复和增强功能。</span><span class="sxs-lookup"><span data-stu-id="39503-110">Contribute bug fixes and enhancements to the API.</span></span> 
> - <span data-ttu-id="39503-111">在修补程序和增强功能在正式的版本中可用之前获取它们。</span><span class="sxs-lookup"><span data-stu-id="39503-111">Get fixes and enhancements before they are available in an official release.</span></span> 
> - <span data-ttu-id="39503-112">访问最全面且最新的 API 实现，将其用作参考或在新的平台上创建新库。</span><span class="sxs-lookup"><span data-stu-id="39503-112">Access the most comprehensive and up-to-date implementation of the API, to use as a reference or to create new libraries on new platforms.</span></span> 
>
>  <span data-ttu-id="39503-113">欢迎你通过 GitHub 做出[贡献](https://github.com/OfficeDev/ews-managed-api/blob/master/CONTRIBUTING.md)。</span><span class="sxs-lookup"><span data-stu-id="39503-113">>  We welcome your [contributions](https://github.com/OfficeDev/ews-managed-api/blob/master/CONTRIBUTING.md) via GitHub.</span></span> 
  
## <a name="youll-need-an-exchange-server"></a><span data-ttu-id="39503-114">你将需要 Exchange 服务器</span><span class="sxs-lookup"><span data-stu-id="39503-114">You'll need an Exchange server</span></span>
<span data-ttu-id="39503-115"><a name="NeedExchange"> </a></span><span class="sxs-lookup"><span data-stu-id="39503-115"></span></span>

<span data-ttu-id="39503-p103">如果您已经有一个 Exchange 邮箱帐户，则可以跳过本节。否则，您必须具备以下选项来为您的首个 EWS 客户端应用程序设置 Exchange 邮箱：</span><span class="sxs-lookup"><span data-stu-id="39503-p103">If you already have an Exchange mailbox account, you can skip this section. Otherwise, you have the following options for setting up an Exchange mailbox for your first EWS client application:</span></span>
  
- <span data-ttu-id="39503-p104">获得 [Office 365 开发人员网站](http://msdn.microsoft.com/zh-CN/library/office/fp179924.aspx)（推荐）。这是您设置 Exchange 邮箱的最快方法。</span><span class="sxs-lookup"><span data-stu-id="39503-p104">Get an [Office 365 Developer Site](http://msdn.microsoft.com/zh-CN/library/office/fp179924.aspx) (recommended). This is the quickest way for you to set up an Exchange mailbox.</span></span> 
    
- <span data-ttu-id="39503-120">下载 [Exchange Server](http://office.microsoft.com/en-us/exchange/microsoft-exchange-try-or-buy-exchange-we-can-help-you-decide-FX103746846.aspx?WT%2Eintid1=ODC%5FENUS%5FFX103472230%5FXT103965589)。</span><span class="sxs-lookup"><span data-stu-id="39503-120">Download [Exchange Server](http://office.microsoft.com/en-us/exchange/microsoft-exchange-try-or-buy-exchange-we-can-help-you-decide-FX103746846.aspx?WT%2Eintid1=ODC%5FENUS%5FFX103472230%5FXT103965589).</span></span>
    
<span data-ttu-id="39503-p105">确认您可以从 Exchange 发送和接收电子邮件后，您便可以设置您的开发环境了。您可以使用 Exchange Web 客户端 [Outlook Web App](http://technet.microsoft.com/zh-CN/library/jj657718%28v=exchg.150%29.aspx) 确认您是否可以发送电子邮件。</span><span class="sxs-lookup"><span data-stu-id="39503-p105">After you have verified that you can send and receive email from Exchange, you are ready to set up your development environment. You can use the Exchange web client [Outlook Web App](http://technet.microsoft.com/zh-CN/library/jj657718%28v=exchg.150%29.aspx) to verify that you can send email.</span></span> 
  
## <a name="set-up-your-development-environment"></a><span data-ttu-id="39503-123">设置开发环境</span><span class="sxs-lookup"><span data-stu-id="39503-123">Set up your development environment</span></span>
<span data-ttu-id="39503-124"><a name="Setup"> </a></span><span class="sxs-lookup"><span data-stu-id="39503-124"></span></span>

<span data-ttu-id="39503-125">请确保您可访问以下项目：</span><span class="sxs-lookup"><span data-stu-id="39503-125">Make sure that you have access to the following:</span></span>
  
- <span data-ttu-id="39503-p106">支持.NET Framework 4 的任何版本的 [Visual Studio](http://www.visualstudio.com/zh-CN/downloads/download-visual-studio-vs.aspx)。尽管从技术上讲，您不需要 Visual Studio，因为您可以使用任何 C# 编译，但仍建议使用它。</span><span class="sxs-lookup"><span data-stu-id="39503-p106">Any version of [Visual Studio](http://www.visualstudio.com/zh-CN/downloads/download-visual-studio-vs.aspx) that supports the .NET Framework 4. Although technically, you don't need Visual Studio because you can use any C# compiler, we recommend that you use it.</span></span> 
    
- <span data-ttu-id="39503-p107">[EWS 托管 API](http://aka.ms/ews-managed-api-readme)。您可以使用 32 位或 64 位版本，具体取决于您的系统。使用默认安装位置。</span><span class="sxs-lookup"><span data-stu-id="39503-p107">The [EWS Managed API](http://aka.ms/ews-managed-api-readme). You can use either the 64-bit or 32-bit version, depending on your system. Use the default installation location.</span></span> 
    
## <a name="create-your-first-ews-managed-api-application"></a><span data-ttu-id="39503-131">创建第一个 EWS 托管 API 应用程序</span><span class="sxs-lookup"><span data-stu-id="39503-131">Create your first EWS Managed API application</span></span>
<span data-ttu-id="39503-132"><a name="Create"> </a></span><span class="sxs-lookup"><span data-stu-id="39503-132"></span></span>

<span data-ttu-id="39503-p108">这些步骤假定您设置 Office 365 开发人员网站。如果您已下载并安装 Exchange，您将需要在您的 Exchange 服务器上[安装有效的证书](http://technet.microsoft.com/zh-CN/library/bb310769%28v=exchg.141%29.aspx)或针对默认情况下提供的自签名证书[实现证书验证](how-to-validate-a-server-certificate-for-the-ews-managed-api.md)回调。另外，请注意以下步骤会稍有不同，具体取决于您正在使用的 Visual Studio 的版本。</span><span class="sxs-lookup"><span data-stu-id="39503-p108">These steps assume that you set up an Office 365 Developer Site. If you downloaded and installed Exchange, you will need to [install a valid certificate](http://technet.microsoft.com/zh-CN/library/bb310769%28v=exchg.141%29.aspx) on your Exchange server or [implement a certificate validation](how-to-validate-a-server-certificate-for-the-ews-managed-api.md) callback for a self-signed certificate that is provided by default. Also note that these steps might vary slightly depending on the version of Visual Studio that you are using.</span></span> 
  
### <a name="step-1-create-a-project-in-visual-studio"></a><span data-ttu-id="39503-136">步骤 1：在 Visual Studio 中创建项目</span><span class="sxs-lookup"><span data-stu-id="39503-136">Step 1: Create a project in Visual Studio</span></span>

1. <span data-ttu-id="39503-p109">在 Visual Studio 中的 **文件** 菜单上，选择 **新建** ，然后选择 **项目** 。将打开 **新建项目** 对话框。</span><span class="sxs-lookup"><span data-stu-id="39503-p109">In Visual Studio, on the **File** menu, choose **New**, and then choose **Project**. The **New Project** dialog box opens.</span></span> 
    
2. <span data-ttu-id="39503-p110">创建 **C# 控制台应用程序** 。从 **模板** 窗格中，选择 **Visual C#** ，然后选择 **控制台应用程序** 。</span><span class="sxs-lookup"><span data-stu-id="39503-p110">Create a **C# Console Application**. From the **Templates** pane, choose **Visual C#**, and then choose **Console Application**.</span></span> 
    
3. <span data-ttu-id="39503-141">将项目命名为 HelloWorld，然后选择“**确定**”。</span><span class="sxs-lookup"><span data-stu-id="39503-141">Name the project HelloWorld, and then choose **OK**.</span></span>
    
<span data-ttu-id="39503-142">Visual Studio 创建该项目，并打开 Program.cs 代码文档窗口。</span><span class="sxs-lookup"><span data-stu-id="39503-142">Visual Studio creates the project and opens the Program.cs code document window.</span></span>

### <a name="step-2-add-a-reference-to-the-ews-managed-api"></a><span data-ttu-id="39503-143">步骤 2：向 EWS 托管 API 添加引用</span><span class="sxs-lookup"><span data-stu-id="39503-143">Step 2: Add a reference to the EWS Managed API</span></span>

1. <span data-ttu-id="39503-p111">如果 **解决方案资源管理器** 窗口已经打开，请跳过此步骤并继续步骤 2。若要打开 **解决方案资源管理器** 窗口，请在 **视图** 菜单上，选择 **解决方案资源管理器** 。</span><span class="sxs-lookup"><span data-stu-id="39503-p111">If the **Solution Explorer** window is already open, skip this step and proceed to step 2. To open the **Solution Explorer** window, on the **View** menu, choose **Solution Explorer**.</span></span> 
    
2. <span data-ttu-id="39503-p112">在 **解决方案资源管理器** 和 **HelloWorld** 项目中，打开 **引用** 对应的快捷菜单（单击鼠标右键），然后从上下文菜单中选择 **添加引用** 。将打开用于管理项目引用的对话框。</span><span class="sxs-lookup"><span data-stu-id="39503-p112">In the **Solution Explorer** and the **HelloWorld** project, open the shortcut menu (right-click) for **References** and choose **Add Reference** from the context menu. A dialog box for managing project references will open.</span></span> 
    
3. <span data-ttu-id="39503-148">选择“**浏览**”选项。</span><span class="sxs-lookup"><span data-stu-id="39503-148">Choose the **Browse** option.</span></span> <span data-ttu-id="39503-149">浏览到安装 EWS 托管 API DLL 的位置。</span><span class="sxs-lookup"><span data-stu-id="39503-149">Browse to the location where you installed the EWS Managed API DLL.</span></span> <span data-ttu-id="39503-150">安装程序设置的默认路径为：C:\Program Files\Microsoft\Exchange\Web Services\<version>\.</span><span class="sxs-lookup"><span data-stu-id="39503-150">The default path set by the installer is the following: C:\Program Files\Microsoft\Exchange\Web Services\<version>\.</span></span> <span data-ttu-id="39503-151">根据是下载 32 位还是 64 位版本的 Microsoft.Exchange.WebServices.dll，路径会有所变化。</span><span class="sxs-lookup"><span data-stu-id="39503-151">The path can vary based on whether you download the 32 or 64 bit version of the Microsoft.Exchange.WebServices.dll.</span></span> <span data-ttu-id="39503-152">选择 **Microsoft.Exchange.WebServices.dll**，然后选择“**确定**”或“**添加**”。</span><span class="sxs-lookup"><span data-stu-id="39503-152">Choose **Microsoft.Exchange.WebServices.dll** and select **OK** or **Add**.</span></span> <span data-ttu-id="39503-153">这将向项目添加 EWS 托管 API 引用。</span><span class="sxs-lookup"><span data-stu-id="39503-153">This adds the EWS Managed API reference to your project.</span></span> 
    
4. <span data-ttu-id="39503-p114">如果使用 EWS 托管 API 2.0，请更改 HelloWorld 项目以锁定 .NET Framework 4。EWS 托管 API 的其他版本可能使用不同的 .NET Framework 目标版本。</span><span class="sxs-lookup"><span data-stu-id="39503-p114">If you are using EWS Managed API 2.0, change the HelloWorld project to target the .NET Framework 4. Other versions of the EWS Managed API might use a different target version of the .NET Framework.</span></span>
    
5. <span data-ttu-id="39503-p115">请确认您使用正确的 .NET Framework 目标版本。打开 **解决方案资源管理器** 中 **HelloWorld** 项目对应的快捷菜单，然后选择 **属性** 。请验证 **目标框架** 下拉列表框中是否已选择 **.NET Framework 4** 。</span><span class="sxs-lookup"><span data-stu-id="39503-p115">Confirm that you are using the correct target version of the .NET Framework. Open the shortcut menu (right-click) for your **HelloWorld** project in the **Solution Explorer**, and choose **Properties**. Verify that the **.NET Framework 4** is selected in the **Target framework** drop-down box.</span></span> 
    
<span data-ttu-id="39503-159">现在，您已设置项目并创建对 EWS 托管 API 的引用，便可以创建第一个应用程序了。</span><span class="sxs-lookup"><span data-stu-id="39503-159">Now that you have your project set up and you created a reference to the EWS Managed API, you are ready to create your first application.</span></span> <span data-ttu-id="39503-160">为简便起见，请将代码添加到 Program.cs 文件中。</span><span class="sxs-lookup"><span data-stu-id="39503-160">To keep things simple, add your code to the Program.cs file.</span></span> <span data-ttu-id="39503-161">请参阅[引用 EWS 托管 API 集](how-to-reference-the-ews-managed-api-assembly.md)，了解有关引用 EWS 托管 API 的详细信息。</span><span class="sxs-lookup"><span data-stu-id="39503-161">Read [How to: Reference the EWS Managed API assembly](how-to-reference-the-ews-managed-api-assembly.md) for more information about referencing the EWS Managed API.</span></span> <span data-ttu-id="39503-162">在下一个步骤中，您将开发大多数 EWS 托管 API 客户端应用程序时都会用到的基本代码。</span><span class="sxs-lookup"><span data-stu-id="39503-162">In the next step, you will develop the basic code to write most EWS Managed API client applications.</span></span> 
### <a name="step-3-set-up-url-redirection-validation-for-autodiscover"></a><span data-ttu-id="39503-163">步骤 3：设置用于自动发现的 URL 重定向验证</span><span class="sxs-lookup"><span data-stu-id="39503-163">Step 3: Set up URL redirection validation for Autodiscover</span></span>

- <span data-ttu-id="39503-p117">在 **Main(string[] args)** 方法后添加以下重定向验证回调方法。这将验证重定向的 URL 是否由代表 HTTPS 终结点的 ["自动发现"](autodiscover-for-exchange.md) 表示。</span><span class="sxs-lookup"><span data-stu-id="39503-p117">Add the following redirection validation callback method after the **Main(string[] args)** method. This validates whether redirected URLs returned by [Autodiscover](autodiscover-for-exchange.md) represent an HTTPS endpoint.</span></span> 
    
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

<span data-ttu-id="39503-p118">此验证回调将被传递到步骤 4 中的 **ExchangeService** 对象。您需要进行验证，以便应用程序将信任和遵循自动发现重定向 - 自动发现重定向的结果为我们的应用程序提供 EWS 终结点。</span><span class="sxs-lookup"><span data-stu-id="39503-p118">This validation callback will be passed to the **ExchangeService** object in step 4. You need this so that your application will trust and follow Autodiscover redirects - the results of the Autodiscover redirect provides the EWS endpoint for our application.</span></span> 

### <a name="step-4-prepare-the-exchangeservice-object"></a><span data-ttu-id="39503-168">步骤 4：准备 ExchangeService 对象</span><span class="sxs-lookup"><span data-stu-id="39503-168">Step 4: Prepare the ExchangeService object</span></span>

1. <span data-ttu-id="39503-p119">向 EWS 托管 API 添加 **using** 指令引用。在 Program.cs 顶部的最后一个 **using** 指令后添加以下代码。</span><span class="sxs-lookup"><span data-stu-id="39503-p119">Add a **using** directive reference to the EWS Managed API. Add the following code after the last **using** directive at the top of Program.cs.</span></span> 
    
   ```cs
    using Microsoft.Exchange.WebServices.Data;
   ```

2. <span data-ttu-id="39503-p120">在 **Main** 方法中，采用您打算使用的服务版本实例化 [ExchangeService](http://msdn.microsoft.com/zh-CN/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象。此示例将锁定 EWS 架构的最早版本。</span><span class="sxs-lookup"><span data-stu-id="39503-p120">In the **Main** method, instantiate the [ExchangeService](http://msdn.microsoft.com/zh-CN/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object with the service version you intend to target. This example targets the earliest version of the EWS schema.</span></span> 
    
   ```cs
    ExchangeService service = new ExchangeService(ExchangeVersion.Exchange2007_SP1);
   ```

3. <span data-ttu-id="39503-p121">如果锁定内部 Exchange 服务器，并且您的客户端加入域，请继续执行步骤 4。如果您的客户端锁定 Exchange Online 或 Office 365 开发人员网站邮箱，您必须传递显式凭据。在实例化 **ExchangeService** 对象后后添加以下代码并设置邮箱帐户的凭据。用户名应为用户主体名称。继续执行步骤 5。</span><span class="sxs-lookup"><span data-stu-id="39503-p121">If you are targeting an on-premises Exchange server and your client is domain joined, proceed to step 4. If you client is targeting an Exchange Online or Office 365 Developer Site mailbox, you have to pass explicit credentials. Add the following code after the instantiation of the **ExchangeService** object and set the credentials for your mailbox account. The user name should be the user principal name. Proceed to step 5.</span></span> 
    
   ```cs
    service.Credentials = new WebCredentials("user1@contoso.com", "password");
   ```

4. <span data-ttu-id="39503-p122">锁定内部 Exchange 服务器并加入域的客户端可以使用所登录用户的默认凭据，假定凭据与邮箱关联。实例化 **ExchangeService** 对象后添加以下代码。</span><span class="sxs-lookup"><span data-stu-id="39503-p122">Domain-joined clients that target an on-premises Exchange server can use the default credentials of the user who is logged on, assuming the credentials are associated with a mailbox. Add the following code after the instantiation of the **ExchangeService** object.</span></span> 
    
   ```cs
    service.UseDefaultCredentials = true;
   ```

   <span data-ttu-id="39503-p123">如果您的客户端锁定 Exchange Online 或 Office 365 开发人员网站的邮箱，请验证 [UseDefaultCredentials](http://msdn.microsoft.com/zh-CN/library/microsoft.exchange.webservices.data.exchangeservicebase.usedefaultcredentials%28v=exchg.80%29.aspx) 是否设置为 **false**，该值为默认值。您的客户端已准备好进行自动发现服务的第一个调用以获得 EWS 服务调用的服务 URL。</span><span class="sxs-lookup"><span data-stu-id="39503-p123">If your client targets an Exchange Online or Office 365 Developer Site mailbox, verify that [UseDefaultCredentials](http://msdn.microsoft.com/zh-CN/library/microsoft.exchange.webservices.data.exchangeservicebase.usedefaultcredentials%28v=exchg.80%29.aspx) is set to **false**, which is the default value. Your client is ready to make the first call to the Autodiscover service to get the service URL for calls to the EWS service.</span></span>
    
5. <span data-ttu-id="39503-p124">**ExchangeService** 对象上的 **AutodiscoverUrl** 方法对自动发现服务执行一系列调用，以获取服务 URL。如果此方法调用成功， **ExchangeService** 对象上的 的 URL 属性将使用服务 URL 设置。将用户的电子邮件地址和 **RedirectionUrlValidationCallback** 传递到 **AutodiscoverUrl** 方法。在步骤 3 或 4 中指定凭据后，添加以下代码。将  `user1@contoso.com` 更改为您的电子邮件地址，以便自动发现服务查找您的 EWS 终结点。</span><span class="sxs-lookup"><span data-stu-id="39503-p124">The **AutodiscoverUrl** method on the **ExchangeService** object performs a series of calls to the Autodiscover service to get the service URL. If this method call is successful, the URL property on the **ExchangeService** object will be set with the service URL. Pass the user's email address and the **RedirectionUrlValidationCallback** to the **AutodiscoverUrl** method. Add the following code after the credentials have been specified in step 3 or 4. Change  `user1@contoso.com` to your email address so that the Autodiscover service finds your EWS endpoint.</span></span> 
    
   ```cs
    service.AutodiscoverUrl("user1@contoso.com", RedirectionUrlValidationCallback);
   ```

<span data-ttu-id="39503-187">此时，客户端设置为调用 EWS 以访问邮箱数据。</span><span class="sxs-lookup"><span data-stu-id="39503-187">At this point, your client is set up to make calls to EWS to access mailbox data.</span></span> <span data-ttu-id="39503-188">如果立即运行您的代码，则可以通过检查 **ExchangeService.Url** 属性的内容验证运行的 [AutodiscoverUrl](http://msdn.microsoft.com/zh-CN/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) 方法调用。</span><span class="sxs-lookup"><span data-stu-id="39503-188">If you run your code now, you can verify that the **AutodiscoverUrl** method call worked by examining the contents of the [ExchangeService.Url](http://msdn.microsoft.com/zh-CN/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) property.</span></span> <span data-ttu-id="39503-189">如果此属性包含一个 URL，ze 您的调用成功！</span><span class="sxs-lookup"><span data-stu-id="39503-189">If this property contains a URL, your call was a success!</span></span> <span data-ttu-id="39503-190">这意味着您的应用程序成功进行服务身份验证并发现您邮箱的 EWS 终结点。</span><span class="sxs-lookup"><span data-stu-id="39503-190">This means that your application successfully authenticated with the service and discovered the EWS endpoint for your mailbox.</span></span> <span data-ttu-id="39503-191">现在，你就可以对 EWS 执行第一个调用了。</span><span class="sxs-lookup"><span data-stu-id="39503-191">Now you are ready to make your first calls to EWS.</span></span> <span data-ttu-id="39503-192">请参阅[使用 EWS 托管 API 设置 EWS 服务 URL](how-to-set-the-ews-service-url-by-using-the-ews-managed-api.md)，了解有关设置 EWS URL 的详细信息。</span><span class="sxs-lookup"><span data-stu-id="39503-192">Read [How to: Set the EWS service URL by using the EWS Managed API](how-to-set-the-ews-service-url-by-using-the-ews-managed-api.md) for more information about setting the EWS URL.</span></span> 

### <a name="step-6-create-your-first-hello-world-email-message"></a><span data-ttu-id="39503-193">步骤 6：创建第一封 Hello World 电子邮件</span><span class="sxs-lookup"><span data-stu-id="39503-193">Step 6: Create your first Hello World email message</span></span>

1. <span data-ttu-id="39503-194">在 **AutodiscoverUrl** 方法调用后，实例化一个新的 **EmailMessage** 对象并传递您创建的服务对象。</span><span class="sxs-lookup"><span data-stu-id="39503-194">After the **AutodiscoverUrl** method call, instantiate a new **EmailMessage** object and pass in the service object you created.</span></span> 
    
   ```cs
    EmailMessage email = new EmailMessage(service);
   ```

   <span data-ttu-id="39503-p126">您现在有一封设置服务绑定的电子邮件。在 **EmailMessage** 对象上启动的任何调用都将在服务处被锁定。</span><span class="sxs-lookup"><span data-stu-id="39503-p126">You now have an email message on which the service binding is set. Any calls initiated on the **EmailMessage** object will be targeted at the service.</span></span> 
    
2. <span data-ttu-id="39503-p127">现在设置收件人：电子邮件的行收件人。若要执行此操作，将  `user1@contoso.com` 更改为使用 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="39503-p127">Now set the To: line recipient of the email message. To do this, change  `user1@contoso.com` to use your SMTP address.</span></span> 
    
   ```cs
    email.ToRecipients.Add("user1@contoso.com");
   ```

3. <span data-ttu-id="39503-199">设置电子邮件的主题和正文。</span><span class="sxs-lookup"><span data-stu-id="39503-199">Set the subject and the body of the email message.</span></span>
    
   ```cs
    email.Subject = "HelloWorld";
    email.Body = new MessageBody("This is the first email I've sent by using the EWS Managed API.");
   ```

4. <span data-ttu-id="39503-200">现在您便可以通过使用 EWS 托管 API 发送第一封电子邮件。</span><span class="sxs-lookup"><span data-stu-id="39503-200">You are now ready to send your first email message by using the EWS Managed API.</span></span> <span data-ttu-id="39503-201">**Send** 方法将调用服务并提交电子邮件以便进行发送。</span><span class="sxs-lookup"><span data-stu-id="39503-201">The **Send** method will call the service and submit the email message for delivery.</span></span> <span data-ttu-id="39503-202">请参阅[使用 EWS 托管 API 与 EWS 进行通信](how-to-communicate-with-ews-by-using-the-ews-managed-api.md)，了解可用于与 Exchange 进行通信的其他方法。</span><span class="sxs-lookup"><span data-stu-id="39503-202">Read [How to: Communicate with EWS by using the EWS Managed API](how-to-communicate-with-ews-by-using-the-ews-managed-api.md) to learn about other methods you can use to communicate with Exchange.</span></span> 
    
   ```cs
    email.Send();
   ```

5. <span data-ttu-id="39503-p129">现在您便可以运行 Hello World 应用程序了。在 Visual Studio 中，选择 **F5**。将会打开一个空白的控制台窗口。当应用程序进行身份验证时您将在控制台中看不到任何内容，遵循自动发现重定向，然后进行其第一次调用以创建向自己发送的电子邮件。如果您想要查看正在进行的调用，请在调用 **AutodiscoverUrl** 方法之前添加以下两行代码 。然后按 F5。这将 [追踪 EWS 请求和响应](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md)到控制台窗口。</span><span class="sxs-lookup"><span data-stu-id="39503-p129">You are ready to run your Hello World application. In Visual Studio, select **F5**. A blank console window will open. You will not see anything in the console window while your application authenticates, follows Autodiscover redirections, and then makes its first call to create an email message that you send to yourself. If you want to see the calls being made, add the following two lines of code before the **AutodiscoverUrl** method is called. Then press F5. This will [trace out the EWS requests and responses](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md) to the console window.</span></span> 
    
   ```cs
    service.TraceEnabled = true;
    service.TraceFlags = TraceFlags.All;
   ```

<span data-ttu-id="39503-p130">现在，您便拥有运行的 EWS 托管 API 客户端应用程序。为方便起见，下面的示例显示添加到 Program.cs 的所有代码以创建 Hello World 应用程序。</span><span class="sxs-lookup"><span data-stu-id="39503-p130">You now have a working EWS Managed API client application. For your convenience, the following example shows all the code that you added to Program.cs to create your Hello World application.</span></span>

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

## <a name="next-steps"></a><span data-ttu-id="39503-212">后续步骤</span><span class="sxs-lookup"><span data-stu-id="39503-212">Next steps</span></span>
<span data-ttu-id="39503-213"><a name="Next"> </a></span><span class="sxs-lookup"><span data-stu-id="39503-213"></span></span>

<span data-ttu-id="39503-214">如果您已经准备好使用您的第一个 EWS 托管 API 客户端应用程序执行更多操作，请浏览以下资源：</span><span class="sxs-lookup"><span data-stu-id="39503-214">If you're ready to do more with your first EWS Managed API client application, explore the following resources:</span></span>
  
- [<span data-ttu-id="39503-215">Exchange 2013：101 代码示例</span><span class="sxs-lookup"><span data-stu-id="39503-215">Exchange 2013: 101 code samples</span></span>](http://code.msdn.microsoft.com/exchange/Exchange-2013-101-Code-3c38582c)   
- [<span data-ttu-id="39503-216">文件夹和项目</span><span class="sxs-lookup"><span data-stu-id="39503-216">Folders and items</span></span>](folders-and-items-in-ews-in-exchange.md)    
- [<span data-ttu-id="39503-217">EWSEditor</span><span class="sxs-lookup"><span data-stu-id="39503-217">EWSEditor</span></span>](http://ewseditor.codeplex.com/)
    
<span data-ttu-id="39503-218">如果您的应用程序遇到任何问题，[请尝试在论坛中发布问题或评论](http://social.technet.microsoft.com/Forums/exchange/en-US/home?forum=exchangesvrdevelopment)（别忘了阅读热门帖子）。</span><span class="sxs-lookup"><span data-stu-id="39503-218">If you run into any issues with your application, [try posting a question or comment in the forum](http://social.technet.microsoft.com/Forums/exchange/en-US/home?forum=exchangesvrdevelopment) (and don't forget to read the top post).</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="39503-219">本节内容</span><span class="sxs-lookup"><span data-stu-id="39503-219">In this section</span></span>
<span data-ttu-id="39503-220"><a name="Next"> </a></span><span class="sxs-lookup"><span data-stu-id="39503-220"></span></span>

- [<span data-ttu-id="39503-221">引用 EWS 托管 API 集</span><span class="sxs-lookup"><span data-stu-id="39503-221">How to: Reference the EWS Managed API assembly</span></span>](how-to-reference-the-ews-managed-api-assembly.md)   
- [<span data-ttu-id="39503-222">使用 EWS 托管 API 设置 EWS 服务 URL</span><span class="sxs-lookup"><span data-stu-id="39503-222">How to: Set the EWS service URL by using the EWS Managed API</span></span>](how-to-set-the-ews-service-url-by-using-the-ews-managed-api.md)   
- [<span data-ttu-id="39503-223">使用 EWS 托管 API 与 EWS 进行通信</span><span class="sxs-lookup"><span data-stu-id="39503-223">How to: Communicate with EWS by using the EWS Managed API</span></span>](how-to-communicate-with-ews-by-using-the-ews-managed-api.md)
    
## <a name="see-also"></a><span data-ttu-id="39503-224">另请参阅</span><span class="sxs-lookup"><span data-stu-id="39503-224">See also</span></span>

- [<span data-ttu-id="39503-225">开始使用 Exchange 中的 Web 服务</span><span class="sxs-lookup"><span data-stu-id="39503-225">Start using web services in Exchange</span></span>](start-using-web-services-in-exchange.md)    
- [<span data-ttu-id="39503-226">Exchange 的 EWS 客户端设计概述</span><span class="sxs-lookup"><span data-stu-id="39503-226">EWS client design overview for Exchange</span></span>](ews-client-design-overview-for-exchange.md)    
- [<span data-ttu-id="39503-227">开发 Exchange Web 服务客户端</span><span class="sxs-lookup"><span data-stu-id="39503-227">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)   
- [<span data-ttu-id="39503-228">跟踪请求和响应以便解决 EWS 托管 API 应用程序的故障</span><span class="sxs-lookup"><span data-stu-id="39503-228">How to: Trace requests and responses to troubleshoot EWS Managed API applications</span></span>](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md)
    

