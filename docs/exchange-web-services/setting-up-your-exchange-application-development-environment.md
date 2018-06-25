---
title: 设置 Exchange 应用程序开发环境
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 91b86e93-bdde-41c3-9680-45cf61420592
description: 了解如何设置开发环境与 Exchange 中创建的 EWS 应用程序进行通信。
ms.openlocfilehash: 0c7d4c6d37b28b6797bdb638930b8582f31ffc5e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753009"
---
# <a name="setting-up-your-exchange-application-development-environment"></a>设置 Exchange 应用程序开发环境

了解如何设置开发环境与 Exchange 中创建的 EWS 应用程序进行通信。
  
在开始编写您的 Exchange Web Services (EWS) 应用程序之前，您需要确保您的开发环境满足以下最低要求。 您可以使用 EWS 托管 API，.NET Framework 应用程序的标准客户端访问 API 开发应用程序，或者您可以在其自己的与使用 EWS 我们不自动生成的代理。 一般情况下，我们建议您使用 EWS 托管 API;但是，您可以更详细地查找[浏览这两个选项之间的差异](ews-client-design-overview-for-exchange.md)出的一种适用于您。 
  
> [!NOTE]
>  [!注释]  EWS 托管 API 现在已经作为开放源项目在 [GitHub](https://github.com/officedev/ews-managed-api) 上可用。您可以使用开放源库执行以下操作： >  为 API 提供缺陷修复和增强功能。 >  在修补程序和增强功能在正式的版本中可用之前获取它们。 >  访问最全面且最新的 API 实现，将其用作参考或在新的平台上创建新库。 >  我们欢迎您通过 GitHub 做出 [贡献](https://github.com/OfficeDev/ews-managed-api/blob/master/CONTRIBUTING.md)。 
  
## <a name="development-environment-for-the-ews-managed-api"></a>EWS 托管 API 的开发环境
<a name="bk_EWSMA"> </a>

创建 EWS 托管 API 应用程序，您将需要以下访问：
  
- [EWS 托管 API](http://aka.ms/ews-managed-api-readme)。 
    
    您可以将您的计算机; 在任何位置 EWS 托管 API 文件存储默认情况下，它们安装程序 Files\Microsoft\Exchange\Web 服务在\\< 版本号\>文件夹。
    
- Exchange Online、 Exchange Online 作为 Office 365 的一部分或的 Exchange 版本运行 Exchange Server 2007 开头的 Exchange 服务器上邮箱。 
    
    您可以获取 Exchange Online 计划的业务需要，包括免费的试用版，从[Office 365 网站](http://office.microsoft.com/en-us/business/compare-office-365-for-business-plans-FX102918419.aspx#fbid=1tsGNIE7e3a)。 为了连接到的邮箱中，您必须具有用户名和帐户与邮箱关联的凭据。
    
- Visual Studio 开头 Visual Studio 2005 的版本。 如果当前没有 Visual Studio，您可以下载免费版本的[Visual Studio 2010 Express](http://www.microsoft.com/visualstudio/eng/products/visual-studio-2010-express)。
    
- 开头.NET Framework 3.5 的.NET framework 版本。 您可以从[Microsoft 下载中心](http://go.microsoft.com/fwlink/?LinkId=191777)下载.NET Framework 3.5。
    
此外，很有帮助您了解一些使用 C#。 尽管 Visual Studio 支持其他语言除了 C#，但是大部分可用于 EWS 托管 API 的代码示例是用 C# 编写的。
  
## <a name="development-environment-for-ews"></a>EWS 的开发环境
<a name="bk_EWS"> </a>

您可以使用 EWS 开发应用程序在两个不同的方式。 使用 EWS 的最简单方式是创建包含您 XML 的请求，文本文件并将其传输到 Exchange。 为此，下面是您的需要： 
  
- 简单的文本编辑器，如记事本来编辑 XML 请求。 任何文本编辑器中将执行操作，但您可能希望之一将帮助您 XML 语法验证 XMetal 类似。
    
- 工具或可以发送和接收才能进行通信与 Exchange 的 SOAP XML 请求和响应，应用程序中。
    
当您处理原始 XML，还是有的 XML 格式的基本的了解非常有用。
  
使用 EWS 第二种方法是创建一个自动生成的代理，使您能够通过使用 C# 类似的.NET 语言来处理操作。 下面是您需要使用的自动生成的代理：
  
- Visual Studio 开头 Visual Studio 2005 来创建的代理引用的版本。 您可以下载免费版本的[Visual Studio 2010 Express](http://www.microsoft.com/visualstudio/eng/products/visual-studio-2010-express)。
    
- 开头.NET Framework 2.0 的.NET framework 版本。 您可以从[Microsoft 下载中心](http://go.microsoft.com/fwlink/?LinkId=191777)下载.NET Framework 3.5。
    
如果您使用的自动生成的代理，您需要了解一些 C# 编程。
  
> [!NOTE]
> 如果您是.NET Framework 开发人员，我们建议您使用 EWS 托管 API 而不是自动生成代理针对 EWS。 自动生成代理对象模型比易于使用 EWS 托管 API 对象模型。 此外，EWS 托管 API 实现[自动发现](autodiscover-for-exchange.md)，包括客户端的逻辑。 
  
## <a name="see-also"></a>另请参阅


- [设置您的 Exchange 应用程序开发环境](setting-up-your-exchange-application-development-environment.md)
    
- [Exchange 的 EWS 客户端设计概述](ews-client-design-overview-for-exchange.md)
    
- [在 Exchange 控制对 EWS 的访问](how-to-control-access-to-ews-in-exchange.md)
    
- [EWS 生成 Exchange 对象模型](https://msdn.microsoft.com/en-us/library/jj190899)
    

