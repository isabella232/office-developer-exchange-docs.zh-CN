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
# <a name="communicate-with-ews-by-using-the-ews-managed-api"></a><span data-ttu-id="87cf9-103">使用 EWS 托管 API 与 EWS 进行通信</span><span class="sxs-lookup"><span data-stu-id="87cf9-103">Communicate with EWS by using the EWS Managed API</span></span>

<span data-ttu-id="87cf9-104">查找有关如何使用 EWS 托管 API 与 Exchange 中的 EWS 进行通信的信息。</span><span class="sxs-lookup"><span data-stu-id="87cf9-104">Find information about how to use the EWS Managed API to communicate with EWS in Exchange.</span></span>
  
<span data-ttu-id="87cf9-105">EWS 托管 API 中的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)类包含用于设置用户凭据、标识 EWS 终结点、发送和接收 SOAP 消息以及将绑定配置为与 EWS 通信的方法和属性。</span><span class="sxs-lookup"><span data-stu-id="87cf9-105">The [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) class in the EWS Managed API contains the methods and properties that you use to set user credentials, identify the EWS endpoint, send and receive SOAP messages, and configure the binding to communicate with EWS.</span></span> <span data-ttu-id="87cf9-106">您必须先创建**ExchangeService**类的实例并将其绑定到 EWS，然后才能使用 EWS 托管 API 执行任何任务。</span><span class="sxs-lookup"><span data-stu-id="87cf9-106">Before you can use the EWS Managed API to perform any task, you have to create an instance of the **ExchangeService** class and bind it to EWS.</span></span> 
  
<span data-ttu-id="87cf9-107">在使用用户凭据和 EWS 终结点设置[ExchangeService](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.aspx)对象之后，引用[ExchangeService](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.aspx)对象的任何邮箱对象都可以使用以下方法类型与 EWS 进行通信：</span><span class="sxs-lookup"><span data-stu-id="87cf9-107">After you set up an [ExchangeService](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.aspx) object with user credentials and the EWS endpoint, any mailbox object that references the [ExchangeService](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.aspx) object can use the following method types to communicate with EWS:</span></span> 
  
- <span data-ttu-id="87cf9-108">ExchangeService 对象方法- **ExchangeService**对象上不是从基本**对象**类型继承的所有方法都将调用 EWS。</span><span class="sxs-lookup"><span data-stu-id="87cf9-108">ExchangeService object methods — All the methods on the **ExchangeService** object that are not inherited from the base **Object** type make calls to EWS.</span></span> 
    
- <span data-ttu-id="87cf9-109">Exchange 邮箱项目和文件夹类型方法。</span><span class="sxs-lookup"><span data-stu-id="87cf9-109">Exchange mailbox item and folder type methods.</span></span>
    
<span data-ttu-id="87cf9-110">**表1。与 EWS 通信的邮箱项目和文件夹类型方法**</span><span class="sxs-lookup"><span data-stu-id="87cf9-110">**Table 1. Mailbox item and folder type methods that communicate with EWS**</span></span>

|<span data-ttu-id="87cf9-111">Method</span><span class="sxs-lookup"><span data-stu-id="87cf9-111">Method</span></span>|<span data-ttu-id="87cf9-112">功能</span><span class="sxs-lookup"><span data-stu-id="87cf9-112">What it does</span></span>|<span data-ttu-id="87cf9-113">它调用的操作</span><span class="sxs-lookup"><span data-stu-id="87cf9-113">Operations that it calls</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="87cf9-114">Load</span><span class="sxs-lookup"><span data-stu-id="87cf9-114">Load</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.load%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="87cf9-115">获取项、附件或用户配置对象的属性。</span><span class="sxs-lookup"><span data-stu-id="87cf9-115">Gets properties on an item, attachment, or user configuration object.</span></span>  <br/> |[<span data-ttu-id="87cf9-116">GetItem 操作</span><span class="sxs-lookup"><span data-stu-id="87cf9-116">GetItem operation</span></span>](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/><br/> [<span data-ttu-id="87cf9-117">GetAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="87cf9-117">GetAttachment operation</span></span>](https://msdn.microsoft.com/library/24d10a15-b942-415e-9024-a6375708f326%28Office.15%29.aspx) <br/><br/> [<span data-ttu-id="87cf9-118">GetUserConfiguration 操作</span><span class="sxs-lookup"><span data-stu-id="87cf9-118">GetUserConfiguration operation</span></span>](https://msdn.microsoft.com/library/71d50e3c-92bd-435f-8118-b28bb85f8138%28Office.15%29.aspx) <br/> |
|[<span data-ttu-id="87cf9-119">绑定</span><span class="sxs-lookup"><span data-stu-id="87cf9-119">Bind</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="87cf9-120">使用服务器上的现有项目中的信息填充客户端上的新项目。</span><span class="sxs-lookup"><span data-stu-id="87cf9-120">Populates a new item on the client with information from an existing item on the server.</span></span>  <br/> |[<span data-ttu-id="87cf9-121">GetItem 操作</span><span class="sxs-lookup"><span data-stu-id="87cf9-121">GetItem operation</span></span>](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> |
|[<span data-ttu-id="87cf9-122">Save</span><span class="sxs-lookup"><span data-stu-id="87cf9-122">Save</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.save%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="87cf9-123">在服务器上保存客户端项目的副本。</span><span class="sxs-lookup"><span data-stu-id="87cf9-123">Saves the copy of the client item on the server.</span></span>  <br/> |[<span data-ttu-id="87cf9-124">UpdateItem 操作</span><span class="sxs-lookup"><span data-stu-id="87cf9-124">UpdateItem operation</span></span>](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/><br/> [<span data-ttu-id="87cf9-125">UpdateFolder 操作</span><span class="sxs-lookup"><span data-stu-id="87cf9-125">UpdateFolder operation</span></span>](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/><br/>[<span data-ttu-id="87cf9-126">CreateItem 操作</span><span class="sxs-lookup"><span data-stu-id="87cf9-126">CreateItem operation</span></span>](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/><br/>[<span data-ttu-id="87cf9-127">CreateFolder 操作</span><span class="sxs-lookup"><span data-stu-id="87cf9-127">CreateFolder operation</span></span>](https://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> |
|[<span data-ttu-id="87cf9-128">更新</span><span class="sxs-lookup"><span data-stu-id="87cf9-128">Update</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.update%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="87cf9-129">使用在客户端上所做的更改更新服务器。</span><span class="sxs-lookup"><span data-stu-id="87cf9-129">Updates the server with the changes made on the client.</span></span><br/><br/><span data-ttu-id="87cf9-130">对于项目和文件夹， **Update**方法使用[UpdateItem 操作](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)和[UpdateFolder 操作](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="87cf9-130">For items and folders, the **Update** method uses the [UpdateItem operation](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) and the [UpdateFolder operation](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx).</span></span>  <br/> |[<span data-ttu-id="87cf9-131">UpdateItem 操作</span><span class="sxs-lookup"><span data-stu-id="87cf9-131">UpdateItem operation</span></span>](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/><br/>[<span data-ttu-id="87cf9-132">UpdateFolder 操作</span><span class="sxs-lookup"><span data-stu-id="87cf9-132">UpdateFolder operation</span></span>](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> |
|[<span data-ttu-id="87cf9-133">删除</span><span class="sxs-lookup"><span data-stu-id="87cf9-133">Delete</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="87cf9-134">删除服务器上的项目。</span><span class="sxs-lookup"><span data-stu-id="87cf9-134">Deletes an item on the server.</span></span><br/><br/><span data-ttu-id="87cf9-135">对于项目和文件夹， **Delete**方法使用和[DeleteFolder 操作](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="87cf9-135">For items and folders, the **Delete** method uses the and the [DeleteFolder operation](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx).</span></span>  <br/> |[<span data-ttu-id="87cf9-136">DeleteItem 操作</span><span class="sxs-lookup"><span data-stu-id="87cf9-136">DeleteItem operation</span></span>](https://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/><br/> [<span data-ttu-id="87cf9-137">DeleteFolder 操作</span><span class="sxs-lookup"><span data-stu-id="87cf9-137">DeleteFolder operation</span></span>](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |
|[<span data-ttu-id="87cf9-138">Copy</span><span class="sxs-lookup"><span data-stu-id="87cf9-138">Copy</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.copy%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="87cf9-139">在服务器上创建一个或多个文件夹的副本。</span><span class="sxs-lookup"><span data-stu-id="87cf9-139">Creates a copy of the item or folders on the server.</span></span>  <br/> |[<span data-ttu-id="87cf9-140">CopyItem 操作</span><span class="sxs-lookup"><span data-stu-id="87cf9-140">CopyItem operation</span></span>](https://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/><br/> [<span data-ttu-id="87cf9-141">CopyFolder 操作</span><span class="sxs-lookup"><span data-stu-id="87cf9-141">CopyFolder operation</span></span>](https://msdn.microsoft.com/library/c7ea0d68-9793-4144-b378-d99536776db9%28Office.15%29.aspx) <br/> |
|[<span data-ttu-id="87cf9-142">Move</span><span class="sxs-lookup"><span data-stu-id="87cf9-142">Move</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.move%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="87cf9-143">移动服务器上的项目或文件夹。</span><span class="sxs-lookup"><span data-stu-id="87cf9-143">Moves items or folders on the server.</span></span>  <br/> |[<span data-ttu-id="87cf9-144">MoveItem 操作</span><span class="sxs-lookup"><span data-stu-id="87cf9-144">MoveItem operation</span></span>](https://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/><br/> [<span data-ttu-id="87cf9-145">MoveFolder 操作</span><span class="sxs-lookup"><span data-stu-id="87cf9-145">MoveFolder operation</span></span>](https://msdn.microsoft.com/library/c7233966-6c87-4a14-8156-b1610760176d%28Office.15%29.aspx) <br/> |
   
## <a name="to-use-the-ews-managed-api-to-communicate-with-ews"></a><span data-ttu-id="87cf9-146">使用 EWS 托管 API 与 EWS 进行通信</span><span class="sxs-lookup"><span data-stu-id="87cf9-146">To use the EWS Managed API to communicate with EWS</span></span>

1. <span data-ttu-id="87cf9-147">实例化**ExchangeService**类。</span><span class="sxs-lookup"><span data-stu-id="87cf9-147">Instantiate the **ExchangeService** class.</span></span> 
    
   ```csharp
    ExchangeService service = new ExchangeService();
   ```

   > [!NOTE]
   > <span data-ttu-id="87cf9-148">使用空构造函数实例化**ExchangeService**将创建一个绑定到最新已知版本的 Exchange 的实例。</span><span class="sxs-lookup"><span data-stu-id="87cf9-148">Instantiating **ExchangeService** with an empty constructor will create an instance that is bound to the latest known version of Exchange.</span></span> <span data-ttu-id="87cf9-149">或者，可以通过指定 version 作为参数来设定特定版本的 Exchange。</span><span class="sxs-lookup"><span data-stu-id="87cf9-149">Alternatively, you can target a specific version of Exchange by specifying version as a parameter.</span></span> `ExchangeService service = new ExchangeService(ExchangeVersion.Exchange2007_SP1);`
  
2. <span data-ttu-id="87cf9-150">设置向 Exchange 服务器发送请求的用户的凭据。</span><span class="sxs-lookup"><span data-stu-id="87cf9-150">Set the credentials of the user who sends requests to the Exchange server.</span></span> <span data-ttu-id="87cf9-151">如果要使用已通过身份验证的用户的凭据从登录到域的计算机连接到 EWS，请将**ExchangeService**对象的**UseDefaultCredentials**属性设置为**true**。</span><span class="sxs-lookup"><span data-stu-id="87cf9-151">If you want to connect to EWS from a computer that is logged on to the domain, using the credentials of the authenticated user, set the **UseDefaultCredentials** property on the **ExchangeService** object to **true**.</span></span>
    
   ```cs
    // Connect by using the default credentials of the authenticated user.
    service.UseDefaultCredentials = true;
   ```

   <span data-ttu-id="87cf9-152">如果不想使用默认用户凭据进行连接，请设置**ExchangeService**对象的**凭据**属性以明确指定不同用户的凭据。</span><span class="sxs-lookup"><span data-stu-id="87cf9-152">If you do not want to connect by using the default user credentials, set the **Credentials** property on the **ExchangeService** object to explicitly specify the credentials of a different user.</span></span> <span data-ttu-id="87cf9-153">如果您使用的是 Exchange Online 或 Exchange Online 作为 Office 365 的一部分，您将使用基本身份验证，仅使用用户名和密码。</span><span class="sxs-lookup"><span data-stu-id="87cf9-153">If you are using Exchange Online or Exchange Online as part of Office 365, you'll use basic authentication, with just a user name and password.</span></span> <span data-ttu-id="87cf9-154">若要进行 NTLM 身份验证，域名是必需的。</span><span class="sxs-lookup"><span data-stu-id="87cf9-154">A domain name is required for NTLM authentication.</span></span> 
    
   ```cs
    // Connect by using the credentials of user1 at contoso.com.
    service.Credentials = new WebCredentials("user1@contoso.com", "password");
   ```

   <span data-ttu-id="87cf9-155">您还可以使用用户的域名和密码指定用户的凭据。</span><span class="sxs-lookup"><span data-stu-id="87cf9-155">You can also specify the credentials of the user by using the user's domain name and password.</span></span>
    
   ```cs
    // Connect by using the credentials of contoso/user1.
    service.Credentials = new WebCredentials("user1", "password", "contoso");
   ```

   > [!NOTE]
   > <span data-ttu-id="87cf9-156">如果将**UseDefaultCredentials**属性设置为**true**，则将忽略**凭据**属性的值。</span><span class="sxs-lookup"><span data-stu-id="87cf9-156">If the **UseDefaultCredentials** property is set to **true**, the value of the **Credentials** property is ignored.</span></span> 
  
3. <span data-ttu-id="87cf9-157">设置 EWS 终结点的 URL。</span><span class="sxs-lookup"><span data-stu-id="87cf9-157">Set the URL of the EWS endpoint.</span></span> <span data-ttu-id="87cf9-158">此 URL 定位客户端访问服务器上的 exchange .asmx 文件。</span><span class="sxs-lookup"><span data-stu-id="87cf9-158">This URL locates the exchange.asmx file on Client Access server.</span></span>
    
   ```cs
    // Use Autodiscover to set the URL endpoint.
    service.AutodiscoverUrl("user1@contoso.com");
   ```

   > [!NOTE]
   >  <span data-ttu-id="87cf9-159">虽然您可以显式地将**ExchangeService**的**Url**属性设置为硬编码的值，但我们建议您改为使用自动发现服务，原因如下： > 自动发现将确定给定用户的最佳终结点（最接近用户邮箱服务器的终结点）。</span><span class="sxs-lookup"><span data-stu-id="87cf9-159">Although you can explicitly set the **Url** property of the **ExchangeService** to a hardcoded value, we recommend that you use the Autodiscover service instead, for the following reasons: >  Autodiscover determines the best endpoint for a given user (the endpoint that is closest to the user's Mailbox server).</span></span> <span data-ttu-id="87cf9-160">如果部署了新的客户端访问服务器，则 > EWS URL 可能会更改。</span><span class="sxs-lookup"><span data-stu-id="87cf9-160">>  The EWS URL might change if new Client Access servers are deployed.</span></span> <span data-ttu-id="87cf9-161">在这种情况下，使用[自动发现](autodiscover-for-exchange.md)不需要更改代码。</span><span class="sxs-lookup"><span data-stu-id="87cf9-161">In this scenario, using [Autodiscover](autodiscover-for-exchange.md) means no code changes are necessary.</span></span> <span data-ttu-id="87cf9-162">> 应显式设置 URL 或调用**AutodiscoverUrl**，但不应同时进行这两个操作。</span><span class="sxs-lookup"><span data-stu-id="87cf9-162">>  You should either set the URL explicitly or call **AutodiscoverUrl**, but you should not do both.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="87cf9-163">另请参阅</span><span class="sxs-lookup"><span data-stu-id="87cf9-163">See also</span></span>

- [<span data-ttu-id="87cf9-164">EWS 托管 API 客户端应用程序入门</span><span class="sxs-lookup"><span data-stu-id="87cf9-164">Get started with EWS Managed API client applications</span></span>](get-started-with-ews-managed-api-client-applications.md) 
- [<span data-ttu-id="87cf9-165">使用自动发现查找连接点</span><span class="sxs-lookup"><span data-stu-id="87cf9-165">Use Autodiscover to find connection points</span></span>](how-to-use-autodiscover-to-find-connection-points.md)   
- [<span data-ttu-id="87cf9-166">开发 Exchange Web 服务客户端</span><span class="sxs-lookup"><span data-stu-id="87cf9-166">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    

