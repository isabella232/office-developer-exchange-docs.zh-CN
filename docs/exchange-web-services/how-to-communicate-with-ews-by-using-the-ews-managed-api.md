---
title: 使用 EWS 托管 API 与 EWS 通信
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d1b78293-da02-413a-875c-681e99146af3
description: 查找有关如何使用 EWS 托管 API 在 Exchange 与 EWS 通信信息。
ms.openlocfilehash: 773fcc3f7e95d25effb5a686d4b79ec22610df8c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19752763"
---
# <a name="communicate-with-ews-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 与 EWS 通信

查找有关如何使用 EWS 托管 API 在 Exchange 与 EWS 通信信息。
  
EWS 托管 API 中的[ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)类包含的方法和属性，用于设置用户凭据、 确定 EWS 终结点、 发送和接收 SOAP 消息和使用 EWS 配置要进行通信的绑定。 您可以使用 EWS 托管 API 执行任何任务之前，您必须创建**ExchangeService**类的实例，并将其绑定到 EWS。 
  
设置用户凭据[ExchangeService](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.aspx)对象和 EWS 终结点后，引用[ExchangeService](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.aspx)对象的任何邮箱对象可以使用以下方法类型与 EWS 通信： 
  
- ExchangeService 对象的方法 — **ExchangeService**对象上所有并非继承自基**对象**类型的方法进行 EWS 调用。 
    
- Exchange 邮箱项目和文件夹类型方法。
    
**表 1。邮箱项目和文件夹类型的方法与 EWS 通信**

|方法|功能|它将调用的操作|
|:-----|:-----|:-----|
|[加载](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.load%28v=exchg.80%29.aspx) <br/> |获取项目、 附件或用户配置对象上的属性。  <br/> |[GetItem 操作](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/><br/> [GetAttachment 操作](http://msdn.microsoft.com/library/24d10a15-b942-415e-9024-a6375708f326%28Office.15%29.aspx) <br/><br/> [GetUserConfiguration 操作](http://msdn.microsoft.com/library/71d50e3c-92bd-435f-8118-b28bb85f8138%28Office.15%29.aspx) <br/> |
|[绑定](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) <br/> |填充从现有项目的服务器上的信息与客户端上的新项。  <br/> |[GetItem 操作](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> |
|[Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.save%28v=exchg.80%29.aspx) <br/> |在服务器上保存项目副本的客户端。  <br/> |[UpdateItem 操作](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/><br/> [UpdateFolder Operation](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/><br/>[CreateItem 操作](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/><br/>[CreateFolder Operation](http://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> |
|[更新](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.update%28v=exchg.80%29.aspx) <br/> |将服务器更新与客户端上所做的更改。<br/><br/>为项目和文件夹， **Update**方法使用[UpdateItem 操作](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)和[UpdateFolder 操作](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx)。  <br/> |[UpdateItem 操作](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/><br/>[UpdateFolder Operation](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> |
|[删除](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx) <br/> |删除在服务器上的项。<br/><br/>为项目和文件夹， **Delete**方法使用和[DeleteFolder 操作](http://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx)。  <br/> |[删除项操作](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/><br/> [DeleteFolder 操作](http://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |
|[Copy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.copy%28v=exchg.80%29.aspx) <br/> |在服务器上创建的项目或文件夹的副本。  <br/> |[CopyItem 操作](http://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/><br/> [CopyFolder 操作](http://msdn.microsoft.com/library/c7ea0d68-9793-4144-b378-d99536776db9%28Office.15%29.aspx) <br/> |
|[移动](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.move%28v=exchg.80%29.aspx) <br/> |移动项目或服务器上的文件夹。  <br/> |[MoveItem 操作](http://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/><br/> [MoveFolder 操作](http://msdn.microsoft.com/library/c7233966-6c87-4a14-8156-b1610760176d%28Office.15%29.aspx) <br/> |
   
## <a name="to-use-the-ews-managed-api-to-communicate-with-ews"></a>若要使用 EWS 托管 API 与 EWS 进行通信

1. 实例化**ExchangeService**类。 
    
   ```csharp
    ExchangeService service = new ExchangeService();
   ```

   > [!NOTE]
   > 实例**ExchangeService**化使用空的构造函数将创建绑定到 Exchange 已知的最新版本的实例。 或者，可以通过作为参数指定版本目标特定的 Exchange 版本。 `ExchangeService service = new ExchangeService(ExchangeVersion.Exchange2007_SP1);`
  
2. 设置将请求发送到 Exchange server 的用户的凭据。 如果您想要连接到 EWS 登录到域的计算机中，使用的身份验证的用户凭据设置为**true**， **ExchangeService**在对象上**使用**属性。
    
   ```cs
    // Connect by using the default credentials of the authenticated user.
    service.UseDefaultCredentials = true;
   ```

   如果您不希望连接使用默认的用户凭据，在要显式指定不同的用户的凭据的**ExchangeService**对象上设置**凭据**属性。 如果使用 Exchange Online 或 Exchange Online 作为 Office 365 的一部分，您将使用基本身份验证，只有用户名和密码。 为 NTLM 身份验证所需的域名。 
    
   ```cs
    // Connect by using the credentials of user1 at contoso.com.
    service.Credentials = new WebCredentials("user1@contoso.com", "password");
   ```

   您还可以使用的域用户名和密码指定用户的凭据。
    
   ```cs
    // Connect by using the credentials of contoso/user1.
    service.Credentials = new WebCredentials("user1", "password", "contoso");
   ```

   > [!NOTE]
   > 如果**使用**属性设置为**true**，则忽略**凭据**属性的值。 
  
3. 设置 EWS 终结点 URL。 此 URL 中查找客户端访问服务器上的 exchange.asmx 文件。
    
   ```cs
    // Use Autodiscover to set the URL endpoint.
    service.AutodiscoverUrl("user1@contoso.com");
   ```

   > [!NOTE]
   >  尽管您可以为硬编码值来显式设置**ExchangeService**的**Url**属性，我们建议您改用自动发现服务，原因如下： > 自动发现确定给定用户的最佳终结点（终结点靠近用户的邮箱服务器）。 > 如果部署了新的客户端访问服务器，则可能更改 EWS URL。 在此方案中，使用[自动发现](autodiscover-for-exchange.md)意味着不必代码进行更改。 > 您应显式设置的 URL 或呼叫**AutodiscoverUrl**，但不是应执行两项操作。 
  
## <a name="see-also"></a>另请参阅

- [EWS 托管 API 客户端应用程序入门](get-started-with-ews-managed-api-client-applications.md) 
- [使用 Autodiscover 以查找连接点](how-to-use-autodiscover-to-find-connection-points.md)   
- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)
    

