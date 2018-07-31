---
title: EWS 托管 API 程序集参考
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 130990db-6297-42dc-9f5d-f68a2400872a
description: 查找有关如何引用 EWS 托管 API 程序集信息。
ms.openlocfilehash: a08ce43d139440186f611049fa1e457ea44f0362
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353684"
---
# <a name="reference-the-ews-managed-api-assembly"></a><span data-ttu-id="1b974-103">EWS 托管 API 程序集参考</span><span class="sxs-lookup"><span data-stu-id="1b974-103">Reference the EWS Managed API assembly</span></span>

<span data-ttu-id="1b974-104">查找有关如何引用 EWS 托管 API 程序集信息。</span><span class="sxs-lookup"><span data-stu-id="1b974-104">Find information about how to reference the EWS Managed API assembly.</span></span>
  
<span data-ttu-id="1b974-105">EWS 托管 API 提供了简单和全功能的接口，以开发和扩展的应用程序使用 Exchange Web Services (EWS)。</span><span class="sxs-lookup"><span data-stu-id="1b974-105">The EWS Managed API provides a simple and full-featured interface for developing and extending applications that use Exchange Web Services (EWS).</span></span> <span data-ttu-id="1b974-106">无论您使用 Visual Studio 或其他代码编辑器开发 EWS 托管 API 应用程序，您需要做出的 EWS 托管 API 集的引用。</span><span class="sxs-lookup"><span data-stu-id="1b974-106">Whether you are using Visual Studio or another code editor to develop your EWS Managed API application, you will need to make a reference to the EWS Managed API assembly.</span></span> <span data-ttu-id="1b974-107">如果您尚未已安装 EWS 托管 API，请确保[下载 API](http://aka.ms/ews-managed-api-readme)。</span><span class="sxs-lookup"><span data-stu-id="1b974-107">If you haven't installed the EWS Managed API already, be sure to [download the API](http://aka.ms/ews-managed-api-readme).</span></span>
  
> [!NOTE]
> <span data-ttu-id="1b974-108">[!注释] EWS 托管 API 现在已经作为开放源项目在 [GitHub](https://github.com/officedev/ews-managed-api) 上可用。</span><span class="sxs-lookup"><span data-stu-id="1b974-108">The EWS Managed API is now available as an open source project on [GitHub](https://github.com/officedev/ews-managed-api).</span></span> <span data-ttu-id="1b974-109">您可以使用开放源代码库到：</span><span class="sxs-lookup"><span data-stu-id="1b974-109">You can use the open source library to:</span></span> 
> - <span data-ttu-id="1b974-110">为 API 提供缺陷修复和增强功能。</span><span class="sxs-lookup"><span data-stu-id="1b974-110">Contribute bug fixes and enhancements to the API.</span></span> 
> - <span data-ttu-id="1b974-111">在修补程序和增强功能在正式的版本中可用之前获取它们。</span><span class="sxs-lookup"><span data-stu-id="1b974-111">Get fixes and enhancements before they are available in an official release.</span></span> 
> - <span data-ttu-id="1b974-112">访问最全面且最新的 API 实现，将其用作参考或在新的平台上创建新库。</span><span class="sxs-lookup"><span data-stu-id="1b974-112">Access the most comprehensive and up-to-date implementation of the API, to use as a reference or to create new libraries on new platforms.</span></span>
> 
>  <span data-ttu-id="1b974-113">我们欢迎 GitHub 通过您[的贡献](https://github.com/OfficeDev/ews-managed-api/blob/master/CONTRIBUTING.md)。</span><span class="sxs-lookup"><span data-stu-id="1b974-113">We welcome your [contributions](https://github.com/OfficeDev/ews-managed-api/blob/master/CONTRIBUTING.md) via GitHub.</span></span> 
  
## <a name="referencing-the-assembly"></a><span data-ttu-id="1b974-114">引用该程序集</span><span class="sxs-lookup"><span data-stu-id="1b974-114">Referencing the assembly</span></span>

<span data-ttu-id="1b974-115">添加引用的常用方式是使用 Visual Studio。</span><span class="sxs-lookup"><span data-stu-id="1b974-115">The most common way to add a reference is to use Visual Studio.</span></span> <span data-ttu-id="1b974-116">我们知道一些开发人员签出有要使用其他编辑器中，因此我们都包括有关使用 Visual Studio 中使用的命令行编译器以及说明的说明。</span><span class="sxs-lookup"><span data-stu-id="1b974-116">We know that some developers out there like to use other editors, so we are including instructions for using the command-line compiler as well as instructions for using Visual Studio.</span></span> <span data-ttu-id="1b974-117">您还可能注意下面的代码示例具有相同的**using**语句。</span><span class="sxs-lookup"><span data-stu-id="1b974-117">You might notice that the code examples that follow have the same **using** statements.</span></span> <span data-ttu-id="1b974-118">两种方法之间的区别是命令行编译器需要的程序集文件的位置。</span><span class="sxs-lookup"><span data-stu-id="1b974-118">The difference between the two methods is that the command-line compiler needs the location of the assembly file.</span></span> <span data-ttu-id="1b974-119">Visual Studio 参考为您处理此在后台。</span><span class="sxs-lookup"><span data-stu-id="1b974-119">The Visual Studio reference handles this for you behind the scenes.</span></span> 
  
### <a name="to-add-a-reference-by-using-visual-studio"></a><span data-ttu-id="1b974-120">使用 Visual Studio 中添加引用</span><span class="sxs-lookup"><span data-stu-id="1b974-120">To add a reference by using Visual Studio</span></span>

1. <span data-ttu-id="1b974-121">Microsoft.Exchange.WebServices.dll 文件和 Microsoft.Exchange.WebServices.xml 文件置于您选择的文件夹。</span><span class="sxs-lookup"><span data-stu-id="1b974-121">Put the Microsoft.Exchange.WebServices.dll file and the Microsoft.Exchange.WebServices.xml file into a folder of your choice.</span></span> <span data-ttu-id="1b974-122">默认情况下，将文件安装在`C:\Program Files\Microsoft\Exchange\Web Services\2.0\`，但您可以在计算机上的任意位置将文件存储。</span><span class="sxs-lookup"><span data-stu-id="1b974-122">By default, the files are installed in  `C:\Program Files\Microsoft\Exchange\Web Services\2.0\`, but you can store the files anywhere on your computer.</span></span>
    
2. <span data-ttu-id="1b974-123">在 Visual Studio 中的解决方案资源管理器窗格中，选择**引用**，然后选择**添加引用**。</span><span class="sxs-lookup"><span data-stu-id="1b974-123">In the Solution Explorer pane in Visual Studio, select **References**, and then choose **Add Reference**.</span></span> <span data-ttu-id="1b974-124">这将打开添加引用窗口。</span><span class="sxs-lookup"><span data-stu-id="1b974-124">This opens the Add Reference window.</span></span>
    
3. <span data-ttu-id="1b974-125">在添加引用窗口中，导航到**浏览**选项卡，浏览到 Microsoft.Exchange.WebServices.dll 文件的位置，选择该文件，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="1b974-125">In the Add Reference window, navigate to the **Browse** tab, browse to the location of the Microsoft.Exchange.WebServices.dll file, select that file, and then select **OK**.</span></span> 
    
4. <span data-ttu-id="1b974-126">若要在您的应用程序中使用 EWS 托管 API，添加**Microsoft.Exchange.WebServices.Data**命名空间的**using**语句。</span><span class="sxs-lookup"><span data-stu-id="1b974-126">To use the EWS Managed API in your application, add a **using** statement for the **Microsoft.Exchange.WebServices.Data** namespace.</span></span> 
    
   ```cs
    using Microsoft.Exchange.WebServices.Data;
   ```

### <a name="to-add-a-reference-and-build-your-application-with-the-command-line-compiler"></a><span data-ttu-id="1b974-127">若要添加的引用并生成与命令行编译器应用程序</span><span class="sxs-lookup"><span data-stu-id="1b974-127">To add a reference and build your application with the command-line compiler</span></span>

1. <span data-ttu-id="1b974-128">Microsoft.Exchange.WebServices.dll 文件置于您选择的文件夹。</span><span class="sxs-lookup"><span data-stu-id="1b974-128">Put the Microsoft.Exchange.WebServices.dll file into a folder of your choice.</span></span> <span data-ttu-id="1b974-129">此文件夹将编译器的输出文件夹。</span><span class="sxs-lookup"><span data-stu-id="1b974-129">This folder will be the output folder for the compiler.</span></span>
    
2. <span data-ttu-id="1b974-130">在源代码编辑器中，将添加到源代码**Microsoft.Exchange.WebServices.Data**命名空间的**using**语句。</span><span class="sxs-lookup"><span data-stu-id="1b974-130">In your source code editor, add a **using** statement to the source code for the **Microsoft.Exchange.WebServices.Data** namespace.</span></span> 
    
   ```cs
    using Microsoft.Exchange.WebServices.Data;
   ```

3. <span data-ttu-id="1b974-131">运行命令行编译器构建应用程序。</span><span class="sxs-lookup"><span data-stu-id="1b974-131">Run the command-line compiler to build the application.</span></span> <span data-ttu-id="1b974-132">以下命令使用.NET Framework C# 编译器构建 Windows 应用程序中的源代码文件"program.cs"定义。</span><span class="sxs-lookup"><span data-stu-id="1b974-132">The following command uses the .NET Framework C# compiler to build the Windows application defined in the source code file "program.cs".</span></span> <span data-ttu-id="1b974-133">它假定编译器位于默认安装目录并 Microsoft.Exchange.WebServices.dll 文件位于名为"生成"当前目录的子目录。</span><span class="sxs-lookup"><span data-stu-id="1b974-133">It assumes that the compiler is located in the default installation directory and that the Microsoft.Exchange.WebServices.dll file is in a subdirectory of the current directory named "build".</span></span>
    
   ```cs
    c:\Windows\Microsoft.NET\Framework\3.5\csc /target: winexe /out: build\testApplication /reference: build\Microsoft.Exchange.WebServices.dll program.cs
   ```

## <a name="see-also"></a><span data-ttu-id="1b974-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1b974-134">See also</span></span>

- [<span data-ttu-id="1b974-135">EWS 托管 API 客户端应用程序入门</span><span class="sxs-lookup"><span data-stu-id="1b974-135">Get started with EWS Managed API client applications</span></span>](get-started-with-ews-managed-api-client-applications.md)    
- [<span data-ttu-id="1b974-136">设置您的 Exchange 应用程序开发环境</span><span class="sxs-lookup"><span data-stu-id="1b974-136">Setting up your Exchange application development environment</span></span>](setting-up-your-exchange-application-development-environment.md)   
- [<span data-ttu-id="1b974-137">使用 EWS 托管 API 与 EWS 通信</span><span class="sxs-lookup"><span data-stu-id="1b974-137">Communicate with EWS by using the EWS Managed API</span></span>](how-to-communicate-with-ews-by-using-the-ews-managed-api.md)
    

