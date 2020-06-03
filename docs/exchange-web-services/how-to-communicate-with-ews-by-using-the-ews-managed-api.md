---
title: 使用 EWS 托管 API 与 EWS 进行通信
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: d1b78293-da02-413a-875c-681e99146af3
description: 查找有关如何使用 EWS 托管 API 与 Exchange 中的 EWS 进行通信的信息。
localization_priority: Priority
ms.openlocfilehash: be807f2d936bf79d181476ec8eb12f20fca7950f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528242"
---
# <a name="communicate-with-ews-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 与 EWS 进行通信

查找有关如何使用 EWS 托管 API 与 Exchange 中的 EWS 进行通信的信息。
  
EWS 托管 API 中的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)类包含用于设置用户凭据、标识 EWS 终结点、发送和接收 SOAP 消息以及将绑定配置为与 EWS 通信的方法和属性。 您必须先创建**ExchangeService**类的实例并将其绑定到 EWS，然后才能使用 EWS 托管 API 执行任何任务。 
  
在使用用户凭据和 EWS 终结点设置[ExchangeService](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.aspx)对象之后，引用[ExchangeService](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.aspx)对象的任何邮箱对象都可以使用以下方法类型与 EWS 进行通信： 
  
- ExchangeService 对象方法- **ExchangeService**对象上不是从基本**对象**类型继承的所有方法都将调用 EWS。 
    
- Exchange 邮箱项目和文件夹类型方法。
    
**表1。与 EWS 通信的邮箱项目和文件夹类型方法**

|Method|功能|它调用的操作|
|:-----|:-----|:-----|
|[Load](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.load%28v=exchg.80%29.aspx) <br/> |获取项、附件或用户配置对象的属性。  <br/> |[GetItem 操作](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/><br/> [GetAttachment 操作](https://msdn.microsoft.com/library/24d10a15-b942-415e-9024-a6375708f326%28Office.15%29.aspx) <br/><br/> [GetUserConfiguration 操作](https://msdn.microsoft.com/library/71d50e3c-92bd-435f-8118-b28bb85f8138%28Office.15%29.aspx) <br/> |
|[绑定](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) <br/> |使用服务器上的现有项目中的信息填充客户端上的新项目。  <br/> |[GetItem 操作](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> |
|[Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.save%28v=exchg.80%29.aspx) <br/> |在服务器上保存客户端项目的副本。  <br/> |[UpdateItem 操作](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/><br/> [UpdateFolder 操作](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/><br/>[CreateItem 操作](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/><br/>[CreateFolder 操作](https://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> |
|[更新](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.update%28v=exchg.80%29.aspx) <br/> |使用在客户端上所做的更改更新服务器。<br/><br/>对于项目和文件夹， **Update**方法使用[UpdateItem 操作](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)和[UpdateFolder 操作](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx)。  <br/> |[UpdateItem 操作](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/><br/>[UpdateFolder 操作](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> |
|[删除](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx) <br/> |删除服务器上的项目。<br/><br/>对于项目和文件夹， **Delete**方法使用和[DeleteFolder 操作](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx)。  <br/> |[DeleteItem 操作](https://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/><br/> [DeleteFolder 操作](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |
|[Copy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.copy%28v=exchg.80%29.aspx) <br/> |在服务器上创建一个或多个文件夹的副本。  <br/> |[CopyItem 操作](https://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/><br/> [CopyFolder 操作](https://msdn.microsoft.com/library/c7ea0d68-9793-4144-b378-d99536776db9%28Office.15%29.aspx) <br/> |
|[Move](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.move%28v=exchg.80%29.aspx) <br/> |移动服务器上的项目或文件夹。  <br/> |[MoveItem 操作](https://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/><br/> [MoveFolder 操作](https://msdn.microsoft.com/library/c7233966-6c87-4a14-8156-b1610760176d%28Office.15%29.aspx) <br/> |
   
## <a name="to-use-the-ews-managed-api-to-communicate-with-ews"></a>使用 EWS 托管 API 与 EWS 进行通信

1. 实例化**ExchangeService**类。 
    
   ```csharp
    ExchangeService service = new ExchangeService();
   ```

   > [!NOTE]
   > 使用空构造函数实例化**ExchangeService**将创建一个绑定到最新已知版本的 Exchange 的实例。 或者，可以通过指定 version 作为参数来设定特定版本的 Exchange。 `ExchangeService service = new ExchangeService(ExchangeVersion.Exchange2007_SP1);`
  
2. 设置向 Exchange 服务器发送请求的用户的凭据。 如果要使用已通过身份验证的用户的凭据从登录到域的计算机连接到 EWS，请将**ExchangeService**对象的**UseDefaultCredentials**属性设置为**true**。
    
   ```cs
    // Connect by using the default credentials of the authenticated user.
    service.UseDefaultCredentials = true;
   ```

   如果不想使用默认用户凭据进行连接，请设置**ExchangeService**对象的**凭据**属性以明确指定不同用户的凭据。 如果您使用的是 Exchange Online 或 Exchange Online 作为 Office 365 的一部分，您将使用基本身份验证，仅使用用户名和密码。 若要进行 NTLM 身份验证，域名是必需的。 
    
   ```cs
    // Connect by using the credentials of user1 at contoso.com.
    service.Credentials = new WebCredentials("user1@contoso.com", "password");
   ```

   您还可以使用用户的域名和密码指定用户的凭据。
    
   ```cs
    // Connect by using the credentials of contoso/user1.
    service.Credentials = new WebCredentials("user1", "password", "contoso");
   ```

   > [!NOTE]
   > 如果将**UseDefaultCredentials**属性设置为**true**，则将忽略**凭据**属性的值。 
  
3. 设置 EWS 终结点的 URL。 此 URL 定位客户端访问服务器上的 exchange .asmx 文件。
    
   ```cs
    // Use Autodiscover to set the URL endpoint.
    service.AutodiscoverUrl("user1@contoso.com");
   ```

   > [!NOTE]
   >  虽然您可以显式地将**ExchangeService**的**Url**属性设置为硬编码的值，但我们建议您改为使用自动发现服务，原因如下： > 自动发现将确定给定用户的最佳终结点（最接近用户邮箱服务器的终结点）。 如果部署了新的客户端访问服务器，则 > EWS URL 可能会更改。 在这种情况下，使用[自动发现](autodiscover-for-exchange.md)不需要更改代码。 > 应显式设置 URL 或调用**AutodiscoverUrl**，但不应同时进行这两个操作。 
  
## <a name="see-also"></a>另请参阅

- [EWS 托管 API 客户端应用程序入门](get-started-with-ews-managed-api-client-applications.md) 
- [使用自动发现查找连接点](how-to-use-autodiscover-to-find-connection-points.md)   
- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)
    

