---
title: 设置 Exchange 应用程序开发环境
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 91b86e93-bdde-41c3-9680-45cf61420592
description: 了解如何设置开发环境以创建与 Exchange 进行通信的 EWS 应用程序。
localization_priority: Priority
ms.openlocfilehash: 01a106817f29bd696991b8a0c5d7d9b7dd420b94
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463760"
---
# <a name="setting-up-your-exchange-application-development-environment"></a>设置 Exchange 应用程序开发环境

了解如何设置开发环境以创建与 Exchange 进行通信的 EWS 应用程序。
  
在开始编写 Exchange Web Services （EWS）应用程序之前，您需要确保您的开发环境满足最低要求。 您可以使用 EWS 托管 API （用于 .NET Framework 应用程序的标准客户端访问 API）来开发应用程序，也可以使用 EWS，因为我们没有自动生成的代理。 通常情况下，我们建议使用 EWS 托管 API;但是，可以更详细地了解这[两个选项之间的差异](ews-client-design-overview-for-exchange.md)，以找出哪一项适合您。 
  
> [!NOTE]
> EWS 托管 API 现已作为 [GitHub](https://github.com/officedev/ews-managed-api) 上的开源项目推出。 你可以使用开源库进行以下操作： 
> - 为 API 提供缺陷修复和增强功能。 
> - 在修补程序和增强功能在正式的版本中可用之前获取它们。 
> - 访问最全面且最新的 API 实现，将其用作参考或在新的平台上创建新库。
> 
>  欢迎你通过 GitHub 做出[贡献](https://github.com/OfficeDev/ews-managed-api/blob/master/CONTRIBUTING.md)。 
  
## <a name="development-environment-for-the-ews-managed-api"></a>EWS 托管 API 的开发环境
<a name="bk_EWSMA"> </a>

若要创建 EWS 托管 API 应用程序，您需要具有以下权限：
  
- [EWS 托管 API](https://aka.ms/ews-managed-api-readme)。 
    
    可以在计算机上的任意位置存储 EWS 托管 API 文件;默认情况下，它们安装在 Program Files\Microsoft\Exchange\Web Services \\<版本号文件夹中 \> 。
    
- Exchange server 上运行 Exchange Online 的邮箱、作为 Office 365 的一部分的 Exchange Online 或从 Exchange Server 2007 开始的 Exchange 版本。 
    
    您可以从[Office 365 网站](https://office.microsoft.com/business/compare-office-365-for-business-plans-FX102918419.aspx#fbid=1tsGNIE7e3a)获取 Exchange Online 计划（包括免费试用版）。 若要连接到邮箱，您必须具有与邮箱关联的帐户的用户名和凭据。

    
- 以 Visual Studio 2005 开头的 Visual Studio 版本。 如果当前没有 Visual Studio，则可以下载[免费版本](https://visualstudio.microsoft.com/)。
    
- 从 .NET Framework 3.5 开始的 .NET Framework 版本。 您可以从[Microsoft 下载中心](https://go.microsoft.com/fwlink/?LinkId=191777)下载 .net Framework 3.5。
    
此外，如果您熟悉 c #，它会有所帮助。 尽管除 c # 之外，Visual Studio 还支持其他语言，但大多数可用于 EWS 托管 API 的示例代码都是用 c # 编写的。
  
## <a name="development-environment-for-ews"></a>EWS 的开发环境
<a name="bk_EWS"> </a>

您可以使用 EWS 以几种不同的方式开发您的应用程序。 使用 EWS 最简单的方法是创建包含 XML 请求的文本文件，并将这些文件传输到 Exchange。 为此，您需要具备以下条件： 
  
- 简单的文本编辑器（如记事本）来编辑您的 XML 请求。 任何文本编辑器都将执行此操作，但您可能希望能够帮助您的 XML 语法验证（如 XMetal）。
    
- 可以发送和接收 SOAP XML 请求和响应的工具或应用程序，以便与 Exchange 进行通信。
    
使用原始 XML 时，对 XML 格式有一个基本的了解也很有帮助。
  
使用 EWS 的第二种方法是创建自动生成的代理，使您能够使用 .NET 语言（如 c #）处理这些操作。 以下是您需要使用自动生成的代理的内容：
  
- Visual studio 的一个版本，从 Visual Studio 2005 开始，以创建代理引用。 您可以下载[免费版本](https://visualstudio.microsoft.com/)。
    
- 从 .NET Framework 2.0 开始的 .NET Framework 版本。 您可以从[Microsoft 下载中心](https://go.microsoft.com/fwlink/?LinkId=191777)下载 .net Framework 3.5。
    
如果使用自动生成的代理，您需要了解一些 c # 编程。
  
> [!NOTE]
> 如果您是 .NET Framework 开发人员，我们鼓励您使用 EWS 托管 API 而不是自动生成的代理来针对 EWS 进行开发。 EWS 托管 API 对象模型比自动生成的代理对象模型更易于使用。 此外，EWS 托管 API 还实现[自动发现](autodiscover-for-exchange.md)并包括客户端逻辑。 
  
## <a name="see-also"></a>另请参阅

- [设置 Exchange 应用程序开发环境](setting-up-your-exchange-application-development-environment.md)   
- [Exchange 的 EWS 客户端设计概述](ews-client-design-overview-for-exchange.md)  
- [在 Exchange 中控制对 EWS 的访问](how-to-control-access-to-ews-in-exchange.md)  
- [EWS 生成的 Exchange 对象模型](https://msdn.microsoft.com/library/jj190899)
    