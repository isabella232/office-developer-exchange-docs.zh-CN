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
# <a name="reference-the-ews-managed-api-assembly"></a>EWS 托管 API 程序集参考

查找有关如何引用 EWS 托管 API 程序集信息。
  
EWS 托管 API 提供了简单和全功能的接口，以开发和扩展的应用程序使用 Exchange Web Services (EWS)。 无论您使用 Visual Studio 或其他代码编辑器开发 EWS 托管 API 应用程序，您需要做出的 EWS 托管 API 集的引用。 如果您尚未已安装 EWS 托管 API，请确保[下载 API](http://aka.ms/ews-managed-api-readme)。
  
> [!NOTE]
> [!注释] EWS 托管 API 现在已经作为开放源项目在 [GitHub](https://github.com/officedev/ews-managed-api) 上可用。 您可以使用开放源代码库到： 
> - 为 API 提供缺陷修复和增强功能。 
> - 在修补程序和增强功能在正式的版本中可用之前获取它们。 
> - 访问最全面且最新的 API 实现，将其用作参考或在新的平台上创建新库。
> 
>  我们欢迎 GitHub 通过您[的贡献](https://github.com/OfficeDev/ews-managed-api/blob/master/CONTRIBUTING.md)。 
  
## <a name="referencing-the-assembly"></a>引用该程序集

添加引用的常用方式是使用 Visual Studio。 我们知道一些开发人员签出有要使用其他编辑器中，因此我们都包括有关使用 Visual Studio 中使用的命令行编译器以及说明的说明。 您还可能注意下面的代码示例具有相同的**using**语句。 两种方法之间的区别是命令行编译器需要的程序集文件的位置。 Visual Studio 参考为您处理此在后台。 
  
### <a name="to-add-a-reference-by-using-visual-studio"></a>使用 Visual Studio 中添加引用

1. Microsoft.Exchange.WebServices.dll 文件和 Microsoft.Exchange.WebServices.xml 文件置于您选择的文件夹。 默认情况下，将文件安装在`C:\Program Files\Microsoft\Exchange\Web Services\2.0\`，但您可以在计算机上的任意位置将文件存储。
    
2. 在 Visual Studio 中的解决方案资源管理器窗格中，选择**引用**，然后选择**添加引用**。 这将打开添加引用窗口。
    
3. 在添加引用窗口中，导航到**浏览**选项卡，浏览到 Microsoft.Exchange.WebServices.dll 文件的位置，选择该文件，然后选择**确定**。 
    
4. 若要在您的应用程序中使用 EWS 托管 API，添加**Microsoft.Exchange.WebServices.Data**命名空间的**using**语句。 
    
   ```cs
    using Microsoft.Exchange.WebServices.Data;
   ```

### <a name="to-add-a-reference-and-build-your-application-with-the-command-line-compiler"></a>若要添加的引用并生成与命令行编译器应用程序

1. Microsoft.Exchange.WebServices.dll 文件置于您选择的文件夹。 此文件夹将编译器的输出文件夹。
    
2. 在源代码编辑器中，将添加到源代码**Microsoft.Exchange.WebServices.Data**命名空间的**using**语句。 
    
   ```cs
    using Microsoft.Exchange.WebServices.Data;
   ```

3. 运行命令行编译器构建应用程序。 以下命令使用.NET Framework C# 编译器构建 Windows 应用程序中的源代码文件"program.cs"定义。 它假定编译器位于默认安装目录并 Microsoft.Exchange.WebServices.dll 文件位于名为"生成"当前目录的子目录。
    
   ```cs
    c:\Windows\Microsoft.NET\Framework\3.5\csc /target: winexe /out: build\testApplication /reference: build\Microsoft.Exchange.WebServices.dll program.cs
   ```

## <a name="see-also"></a>另请参阅

- [EWS 托管 API 客户端应用程序入门](get-started-with-ews-managed-api-client-applications.md)    
- [设置您的 Exchange 应用程序开发环境](setting-up-your-exchange-application-development-environment.md)   
- [使用 EWS 托管 API 与 EWS 通信](how-to-communicate-with-ews-by-using-the-ews-managed-api.md)
    

