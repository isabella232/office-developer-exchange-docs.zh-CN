---
title: 引用 EWS 托管 API 集
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 130990db-6297-42dc-9f5d-f68a2400872a
description: 查找有关如何引用 EWS 托管 API 程序集的信息。
localization_priority: Priority
ms.openlocfilehash: d49091781da279d87a1eab35608f19ece43a0333
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527759"
---
# <a name="reference-the-ews-managed-api-assembly"></a><span data-ttu-id="f8320-103">引用 EWS 托管 API 集</span><span class="sxs-lookup"><span data-stu-id="f8320-103">Reference the EWS Managed API assembly</span></span>

<span data-ttu-id="f8320-104">查找有关如何引用 EWS 托管 API 程序集的信息。</span><span class="sxs-lookup"><span data-stu-id="f8320-104">Find information about how to reference the EWS Managed API assembly.</span></span>
  
<span data-ttu-id="f8320-105">EWS 托管 API 提供了一个简单且功能齐全的界面，用于开发和扩展使用 Exchange Web Services （EWS）的应用程序。</span><span class="sxs-lookup"><span data-stu-id="f8320-105">The EWS Managed API provides a simple and full-featured interface for developing and extending applications that use Exchange Web Services (EWS).</span></span> <span data-ttu-id="f8320-106">无论您是使用 Visual Studio 还是其他代码编辑器来开发 EWS 托管 API 应用程序，您都需要对 EWS 托管 API 程序集进行引用。</span><span class="sxs-lookup"><span data-stu-id="f8320-106">Whether you are using Visual Studio or another code editor to develop your EWS Managed API application, you will need to make a reference to the EWS Managed API assembly.</span></span> <span data-ttu-id="f8320-107">如果尚未安装 EWS 托管 API，请务必[下载该 api](https://aka.ms/ews-managed-api-readme)。</span><span class="sxs-lookup"><span data-stu-id="f8320-107">If you haven't installed the EWS Managed API already, be sure to [download the API](https://aka.ms/ews-managed-api-readme).</span></span>
  
> [!NOTE]
> <span data-ttu-id="f8320-108">EWS 托管 API 现已作为 [GitHub](https://github.com/officedev/ews-managed-api) 上的开源项目推出。</span><span class="sxs-lookup"><span data-stu-id="f8320-108">The EWS Managed API is now available as an open source project on [GitHub](https://github.com/officedev/ews-managed-api).</span></span> <span data-ttu-id="f8320-109">你可以使用开源库进行以下操作：</span><span class="sxs-lookup"><span data-stu-id="f8320-109">You can use the open source library to:</span></span> 
> - <span data-ttu-id="f8320-110">为 API 提供缺陷修复和增强功能。</span><span class="sxs-lookup"><span data-stu-id="f8320-110">Contribute bug fixes and enhancements to the API.</span></span> 
> - <span data-ttu-id="f8320-111">在修补程序和增强功能在正式的版本中可用之前获取它们。</span><span class="sxs-lookup"><span data-stu-id="f8320-111">Get fixes and enhancements before they are available in an official release.</span></span> 
> - <span data-ttu-id="f8320-112">访问最全面且最新的 API 实现，将其用作参考或在新的平台上创建新库。</span><span class="sxs-lookup"><span data-stu-id="f8320-112">Access the most comprehensive and up-to-date implementation of the API, to use as a reference or to create new libraries on new platforms.</span></span>
> 
>  <span data-ttu-id="f8320-113">欢迎你通过 GitHub 做出[贡献](https://github.com/OfficeDev/ews-managed-api/blob/master/CONTRIBUTING.md)。</span><span class="sxs-lookup"><span data-stu-id="f8320-113">We welcome your [contributions](https://github.com/OfficeDev/ews-managed-api/blob/master/CONTRIBUTING.md) via GitHub.</span></span> 
  
## <a name="referencing-the-assembly"></a><span data-ttu-id="f8320-114">引用程序集</span><span class="sxs-lookup"><span data-stu-id="f8320-114">Referencing the assembly</span></span>

<span data-ttu-id="f8320-115">添加引用的最常见方法是使用 Visual Studio。</span><span class="sxs-lookup"><span data-stu-id="f8320-115">The most common way to add a reference is to use Visual Studio.</span></span> <span data-ttu-id="f8320-116">我们知道，有些开发人员想要使用其他编辑器，因此我们提供了有关使用命令行编译器的说明以及使用 Visual Studio 的说明。</span><span class="sxs-lookup"><span data-stu-id="f8320-116">We know that some developers out there like to use other editors, so we are including instructions for using the command-line compiler as well as instructions for using Visual Studio.</span></span> <span data-ttu-id="f8320-117">您可能会注意到后面的代码示例具有相同的**using**语句。</span><span class="sxs-lookup"><span data-stu-id="f8320-117">You might notice that the code examples that follow have the same **using** statements.</span></span> <span data-ttu-id="f8320-118">这两种方法的区别在于，命令行编译器需要程序集文件的位置。</span><span class="sxs-lookup"><span data-stu-id="f8320-118">The difference between the two methods is that the command-line compiler needs the location of the assembly file.</span></span> <span data-ttu-id="f8320-119">Visual Studio 引用在幕后对此进行处理。</span><span class="sxs-lookup"><span data-stu-id="f8320-119">The Visual Studio reference handles this for you behind the scenes.</span></span> 
  
### <a name="to-add-a-reference-by-using-visual-studio"></a><span data-ttu-id="f8320-120">使用 Visual Studio 添加引用</span><span class="sxs-lookup"><span data-stu-id="f8320-120">To add a reference by using Visual Studio</span></span>

1. <span data-ttu-id="f8320-121">将 WebServices 文件和 WebServices 文件放到您选择的文件夹中，将其放入一个文件夹中。</span><span class="sxs-lookup"><span data-stu-id="f8320-121">Put the Microsoft.Exchange.WebServices.dll file and the Microsoft.Exchange.WebServices.xml file into a folder of your choice.</span></span> <span data-ttu-id="f8320-122">默认情况下，这些文件安装在中 `C:\Program Files\Microsoft\Exchange\Web Services\2.0\` ，但您可以将文件存储在计算机上的任意位置。</span><span class="sxs-lookup"><span data-stu-id="f8320-122">By default, the files are installed in  `C:\Program Files\Microsoft\Exchange\Web Services\2.0\`, but you can store the files anywhere on your computer.</span></span>
    
2. <span data-ttu-id="f8320-123">在 Visual Studio 中的 "解决方案资源管理器" 窗格中，选择 "**引用**"，然后选择 "**添加引用**"。</span><span class="sxs-lookup"><span data-stu-id="f8320-123">In the Solution Explorer pane in Visual Studio, select **References**, and then choose **Add Reference**.</span></span> <span data-ttu-id="f8320-124">这将打开 "添加引用" 窗口。</span><span class="sxs-lookup"><span data-stu-id="f8320-124">This opens the Add Reference window.</span></span>
    
3. <span data-ttu-id="f8320-125">在 "添加引用" 窗口中，导航到 "**浏览**" 选项卡，浏览到 WebServices 文件的位置，选择该文件，然后选择 **"确定"**。</span><span class="sxs-lookup"><span data-stu-id="f8320-125">In the Add Reference window, navigate to the **Browse** tab, browse to the location of the Microsoft.Exchange.WebServices.dll file, select that file, and then select **OK**.</span></span> 
    
4. <span data-ttu-id="f8320-126">若要在应用程序中使用 EWS 托管 API，请为**WebServices**命名空间添加**using**语句。</span><span class="sxs-lookup"><span data-stu-id="f8320-126">To use the EWS Managed API in your application, add a **using** statement for the **Microsoft.Exchange.WebServices.Data** namespace.</span></span> 
    
   ```cs
    using Microsoft.Exchange.WebServices.Data;
   ```

### <a name="to-add-a-reference-and-build-your-application-with-the-command-line-compiler"></a><span data-ttu-id="f8320-127">使用命令行编译器添加引用并生成应用程序</span><span class="sxs-lookup"><span data-stu-id="f8320-127">To add a reference and build your application with the command-line compiler</span></span>

1. <span data-ttu-id="f8320-128">将 WebServices 文件放到您选择的文件夹中。</span><span class="sxs-lookup"><span data-stu-id="f8320-128">Put the Microsoft.Exchange.WebServices.dll file into a folder of your choice.</span></span> <span data-ttu-id="f8320-129">此文件夹将成为编译器的输出文件夹。</span><span class="sxs-lookup"><span data-stu-id="f8320-129">This folder will be the output folder for the compiler.</span></span>
    
2. <span data-ttu-id="f8320-130">在源代码编辑器中，将**using**语句添加到**WebServices**命名空间的源代码中。</span><span class="sxs-lookup"><span data-stu-id="f8320-130">In your source code editor, add a **using** statement to the source code for the **Microsoft.Exchange.WebServices.Data** namespace.</span></span> 
    
   ```cs
    using Microsoft.Exchange.WebServices.Data;
   ```

3. <span data-ttu-id="f8320-131">运行命令行编译器以生成应用程序。</span><span class="sxs-lookup"><span data-stu-id="f8320-131">Run the command-line compiler to build the application.</span></span> <span data-ttu-id="f8320-132">下面的命令使用 .NET Framework c # 编译器生成在源代码文件 "program.cs" 中定义的 Windows 应用程序。</span><span class="sxs-lookup"><span data-stu-id="f8320-132">The following command uses the .NET Framework C# compiler to build the Windows application defined in the source code file "program.cs".</span></span> <span data-ttu-id="f8320-133">它假定编译器位于默认安装目录中，并且 WebServices 文件位于名为 "build" 的当前目录的子目录中。</span><span class="sxs-lookup"><span data-stu-id="f8320-133">It assumes that the compiler is located in the default installation directory and that the Microsoft.Exchange.WebServices.dll file is in a subdirectory of the current directory named "build".</span></span>
    
   ```cs
    c:\Windows\Microsoft.NET\Framework\3.5\csc /target: winexe /out: build\testApplication /reference: build\Microsoft.Exchange.WebServices.dll program.cs
   ```

## <a name="see-also"></a><span data-ttu-id="f8320-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f8320-134">See also</span></span>

- [<span data-ttu-id="f8320-135">EWS 托管 API 客户端应用程序入门</span><span class="sxs-lookup"><span data-stu-id="f8320-135">Get started with EWS Managed API client applications</span></span>](get-started-with-ews-managed-api-client-applications.md)    
- [<span data-ttu-id="f8320-136">设置 Exchange 应用程序开发环境</span><span class="sxs-lookup"><span data-stu-id="f8320-136">Setting up your Exchange application development environment</span></span>](setting-up-your-exchange-application-development-environment.md)   
- [<span data-ttu-id="f8320-137">使用 EWS 托管 API 与 EWS 进行通信</span><span class="sxs-lookup"><span data-stu-id="f8320-137">Communicate with EWS by using the EWS Managed API</span></span>](how-to-communicate-with-ews-by-using-the-ews-managed-api.md)
    

