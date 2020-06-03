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
# <a name="reference-the-ews-managed-api-assembly"></a>引用 EWS 托管 API 集

查找有关如何引用 EWS 托管 API 程序集的信息。
  
EWS 托管 API 提供了一个简单且功能齐全的界面，用于开发和扩展使用 Exchange Web Services （EWS）的应用程序。 无论您是使用 Visual Studio 还是其他代码编辑器来开发 EWS 托管 API 应用程序，您都需要对 EWS 托管 API 程序集进行引用。 如果尚未安装 EWS 托管 API，请务必[下载该 api](https://aka.ms/ews-managed-api-readme)。
  
> [!NOTE]
> EWS 托管 API 现已作为 [GitHub](https://github.com/officedev/ews-managed-api) 上的开源项目推出。 你可以使用开源库进行以下操作： 
> - 为 API 提供缺陷修复和增强功能。 
> - 在修补程序和增强功能在正式的版本中可用之前获取它们。 
> - 访问最全面且最新的 API 实现，将其用作参考或在新的平台上创建新库。
> 
>  欢迎你通过 GitHub 做出[贡献](https://github.com/OfficeDev/ews-managed-api/blob/master/CONTRIBUTING.md)。 
  
## <a name="referencing-the-assembly"></a>引用程序集

添加引用的最常见方法是使用 Visual Studio。 我们知道，有些开发人员想要使用其他编辑器，因此我们提供了有关使用命令行编译器的说明以及使用 Visual Studio 的说明。 您可能会注意到后面的代码示例具有相同的**using**语句。 这两种方法的区别在于，命令行编译器需要程序集文件的位置。 Visual Studio 引用在幕后对此进行处理。 
  
### <a name="to-add-a-reference-by-using-visual-studio"></a>使用 Visual Studio 添加引用

1. 将 WebServices 文件和 WebServices 文件放到您选择的文件夹中，将其放入一个文件夹中。 默认情况下，这些文件安装在中 `C:\Program Files\Microsoft\Exchange\Web Services\2.0\` ，但您可以将文件存储在计算机上的任意位置。
    
2. 在 Visual Studio 中的 "解决方案资源管理器" 窗格中，选择 "**引用**"，然后选择 "**添加引用**"。 这将打开 "添加引用" 窗口。
    
3. 在 "添加引用" 窗口中，导航到 "**浏览**" 选项卡，浏览到 WebServices 文件的位置，选择该文件，然后选择 **"确定"**。 
    
4. 若要在应用程序中使用 EWS 托管 API，请为**WebServices**命名空间添加**using**语句。 
    
   ```cs
    using Microsoft.Exchange.WebServices.Data;
   ```

### <a name="to-add-a-reference-and-build-your-application-with-the-command-line-compiler"></a>使用命令行编译器添加引用并生成应用程序

1. 将 WebServices 文件放到您选择的文件夹中。 此文件夹将成为编译器的输出文件夹。
    
2. 在源代码编辑器中，将**using**语句添加到**WebServices**命名空间的源代码中。 
    
   ```cs
    using Microsoft.Exchange.WebServices.Data;
   ```

3. 运行命令行编译器以生成应用程序。 下面的命令使用 .NET Framework c # 编译器生成在源代码文件 "program.cs" 中定义的 Windows 应用程序。 它假定编译器位于默认安装目录中，并且 WebServices 文件位于名为 "build" 的当前目录的子目录中。
    
   ```cs
    c:\Windows\Microsoft.NET\Framework\3.5\csc /target: winexe /out: build\testApplication /reference: build\Microsoft.Exchange.WebServices.dll program.cs
   ```

## <a name="see-also"></a>另请参阅

- [EWS 托管 API 客户端应用程序入门](get-started-with-ews-managed-api-client-applications.md)    
- [设置 Exchange 应用程序开发环境](setting-up-your-exchange-application-development-environment.md)   
- [使用 EWS 托管 API 与 EWS 进行通信](how-to-communicate-with-ews-by-using-the-ews-managed-api.md)
    

