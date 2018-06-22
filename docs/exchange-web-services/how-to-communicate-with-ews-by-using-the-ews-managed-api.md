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
# <a name="communicate-with-ews-by-using-the-ews-managed-api"></a><span data-ttu-id="56637-103">使用 EWS 托管 API 与 EWS 通信</span><span class="sxs-lookup"><span data-stu-id="56637-103">Communicate with EWS by using the EWS Managed API</span></span>

<span data-ttu-id="56637-104">查找有关如何使用 EWS 托管 API 在 Exchange 与 EWS 通信信息。</span><span class="sxs-lookup"><span data-stu-id="56637-104">Find information about how to use the EWS Managed API to communicate with EWS in Exchange.</span></span>
  
<span data-ttu-id="56637-105">EWS 托管 API 中的[ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)类包含的方法和属性，用于设置用户凭据、 确定 EWS 终结点、 发送和接收 SOAP 消息和使用 EWS 配置要进行通信的绑定。</span><span class="sxs-lookup"><span data-stu-id="56637-105">The [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) class in the EWS Managed API contains the methods and properties that you use to set user credentials, identify the EWS endpoint, send and receive SOAP messages, and configure the binding to communicate with EWS.</span></span> <span data-ttu-id="56637-106">您可以使用 EWS 托管 API 执行任何任务之前，您必须创建**ExchangeService**类的实例，并将其绑定到 EWS。</span><span class="sxs-lookup"><span data-stu-id="56637-106">Before you can use the EWS Managed API to perform any task, you have to create an instance of the **ExchangeService** class and bind it to EWS.</span></span> 
  
<span data-ttu-id="56637-107">设置用户凭据[ExchangeService](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.aspx)对象和 EWS 终结点后，引用[ExchangeService](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.aspx)对象的任何邮箱对象可以使用以下方法类型与 EWS 通信：</span><span class="sxs-lookup"><span data-stu-id="56637-107">After you set up an [ExchangeService](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.aspx) object with user credentials and the EWS endpoint, any mailbox object that references the [ExchangeService](https://msdn.microsoft.com/library/Microsoft.Exchange.WebServices.Data.ExchangeService.aspx) object can use the following method types to communicate with EWS:</span></span> 
  
- <span data-ttu-id="56637-108">ExchangeService 对象的方法 — **ExchangeService**对象上所有并非继承自基**对象**类型的方法进行 EWS 调用。</span><span class="sxs-lookup"><span data-stu-id="56637-108">ExchangeService object methods — All the methods on the **ExchangeService** object that are not inherited from the base **Object** type make calls to EWS.</span></span> 
    
- <span data-ttu-id="56637-109">Exchange 邮箱项目和文件夹类型方法。</span><span class="sxs-lookup"><span data-stu-id="56637-109">Exchange mailbox item and folder type methods.</span></span>
    
<span data-ttu-id="56637-110">**表 1。邮箱项目和文件夹类型的方法与 EWS 通信**</span><span class="sxs-lookup"><span data-stu-id="56637-110">**Table 1. Mailbox item and folder type methods that communicate with EWS**</span></span>

|<span data-ttu-id="56637-111">方法</span><span class="sxs-lookup"><span data-stu-id="56637-111">Method</span></span>|<span data-ttu-id="56637-112">功能</span><span class="sxs-lookup"><span data-stu-id="56637-112">What it does</span></span>|<span data-ttu-id="56637-113">它将调用的操作</span><span class="sxs-lookup"><span data-stu-id="56637-113">Operations that it calls</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="56637-114">加载</span><span class="sxs-lookup"><span data-stu-id="56637-114">Load</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.load%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="56637-115">获取项目、 附件或用户配置对象上的属性。</span><span class="sxs-lookup"><span data-stu-id="56637-115">Gets properties on an item, attachment, or user configuration object.</span></span>  <br/> |[<span data-ttu-id="56637-116">GetItem 操作</span><span class="sxs-lookup"><span data-stu-id="56637-116">GetItem operation</span></span>](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/><br/> [<span data-ttu-id="56637-117">GetAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="56637-117">GetAttachment operation</span></span>](http://msdn.microsoft.com/library/24d10a15-b942-415e-9024-a6375708f326%28Office.15%29.aspx) <br/><br/> [<span data-ttu-id="56637-118">GetUserConfiguration 操作</span><span class="sxs-lookup"><span data-stu-id="56637-118">GetUserConfiguration operation</span></span>](http://msdn.microsoft.com/library/71d50e3c-92bd-435f-8118-b28bb85f8138%28Office.15%29.aspx) <br/> |
|[<span data-ttu-id="56637-119">绑定</span><span class="sxs-lookup"><span data-stu-id="56637-119">Bind</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="56637-120">填充从现有项目的服务器上的信息与客户端上的新项。</span><span class="sxs-lookup"><span data-stu-id="56637-120">Populates a new item on the client with information from an existing item on the server.</span></span>  <br/> |[<span data-ttu-id="56637-121">GetItem 操作</span><span class="sxs-lookup"><span data-stu-id="56637-121">GetItem operation</span></span>](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> |
|[<span data-ttu-id="56637-122">Save</span><span class="sxs-lookup"><span data-stu-id="56637-122">Save</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.save%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="56637-123">在服务器上保存项目副本的客户端。</span><span class="sxs-lookup"><span data-stu-id="56637-123">Saves the copy of the client item on the server.</span></span>  <br/> |[<span data-ttu-id="56637-124">UpdateItem 操作</span><span class="sxs-lookup"><span data-stu-id="56637-124">UpdateItem operation</span></span>](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/><br/> [<span data-ttu-id="56637-125">UpdateFolder Operation</span><span class="sxs-lookup"><span data-stu-id="56637-125">UpdateFolder operation</span></span>](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/><br/>[<span data-ttu-id="56637-126">CreateItem 操作</span><span class="sxs-lookup"><span data-stu-id="56637-126">CreateItem operation</span></span>](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/><br/>[<span data-ttu-id="56637-127">CreateFolder Operation</span><span class="sxs-lookup"><span data-stu-id="56637-127">CreateFolder operation</span></span>](http://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> |
|[<span data-ttu-id="56637-128">更新</span><span class="sxs-lookup"><span data-stu-id="56637-128">Update</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.update%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="56637-129">将服务器更新与客户端上所做的更改。</span><span class="sxs-lookup"><span data-stu-id="56637-129">Updates the server with the changes made on the client.</span></span><br/><br/><span data-ttu-id="56637-130">为项目和文件夹， **Update**方法使用[UpdateItem 操作](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)和[UpdateFolder 操作](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="56637-130">For items and folders, the **Update** method uses the [UpdateItem operation](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) and the [UpdateFolder operation](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx).</span></span>  <br/> |[<span data-ttu-id="56637-131">UpdateItem 操作</span><span class="sxs-lookup"><span data-stu-id="56637-131">UpdateItem operation</span></span>](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/><br/>[<span data-ttu-id="56637-132">UpdateFolder Operation</span><span class="sxs-lookup"><span data-stu-id="56637-132">UpdateFolder operation</span></span>](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> |
|[<span data-ttu-id="56637-133">删除</span><span class="sxs-lookup"><span data-stu-id="56637-133">Delete</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="56637-134">删除在服务器上的项。</span><span class="sxs-lookup"><span data-stu-id="56637-134">Deletes an item on the server.</span></span><br/><br/><span data-ttu-id="56637-135">为项目和文件夹， **Delete**方法使用和[DeleteFolder 操作](http://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="56637-135">For items and folders, the **Delete** method uses the and the [DeleteFolder operation](http://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx).</span></span>  <br/> |[<span data-ttu-id="56637-136">删除项操作</span><span class="sxs-lookup"><span data-stu-id="56637-136">DeleteItem operation</span></span>](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/><br/> [<span data-ttu-id="56637-137">DeleteFolder 操作</span><span class="sxs-lookup"><span data-stu-id="56637-137">DeleteFolder operation</span></span>](http://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |
|[<span data-ttu-id="56637-138">Copy</span><span class="sxs-lookup"><span data-stu-id="56637-138">Copy</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.copy%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="56637-139">在服务器上创建的项目或文件夹的副本。</span><span class="sxs-lookup"><span data-stu-id="56637-139">Creates a copy of the item or folders on the server.</span></span>  <br/> |[<span data-ttu-id="56637-140">CopyItem 操作</span><span class="sxs-lookup"><span data-stu-id="56637-140">CopyItem operation</span></span>](http://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/><br/> [<span data-ttu-id="56637-141">CopyFolder 操作</span><span class="sxs-lookup"><span data-stu-id="56637-141">CopyFolder operation</span></span>](http://msdn.microsoft.com/library/c7ea0d68-9793-4144-b378-d99536776db9%28Office.15%29.aspx) <br/> |
|[<span data-ttu-id="56637-142">移动</span><span class="sxs-lookup"><span data-stu-id="56637-142">Move</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.move%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="56637-143">移动项目或服务器上的文件夹。</span><span class="sxs-lookup"><span data-stu-id="56637-143">Moves items or folders on the server.</span></span>  <br/> |[<span data-ttu-id="56637-144">MoveItem 操作</span><span class="sxs-lookup"><span data-stu-id="56637-144">MoveItem operation</span></span>](http://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/><br/> [<span data-ttu-id="56637-145">MoveFolder 操作</span><span class="sxs-lookup"><span data-stu-id="56637-145">MoveFolder operation</span></span>](http://msdn.microsoft.com/library/c7233966-6c87-4a14-8156-b1610760176d%28Office.15%29.aspx) <br/> |
   
## <a name="to-use-the-ews-managed-api-to-communicate-with-ews"></a><span data-ttu-id="56637-146">若要使用 EWS 托管 API 与 EWS 进行通信</span><span class="sxs-lookup"><span data-stu-id="56637-146">To use the EWS Managed API to communicate with EWS</span></span>

1. <span data-ttu-id="56637-147">实例化**ExchangeService**类。</span><span class="sxs-lookup"><span data-stu-id="56637-147">Instantiate the **ExchangeService** class.</span></span> 
    
   ```csharp
    ExchangeService service = new ExchangeService();
   ```

   > [!NOTE]
   > <span data-ttu-id="56637-148">实例**ExchangeService**化使用空的构造函数将创建绑定到 Exchange 已知的最新版本的实例。</span><span class="sxs-lookup"><span data-stu-id="56637-148">Instantiating **ExchangeService** with an empty constructor will create an instance that is bound to the latest known version of Exchange.</span></span> <span data-ttu-id="56637-149">或者，可以通过作为参数指定版本目标特定的 Exchange 版本。</span><span class="sxs-lookup"><span data-stu-id="56637-149">Alternatively, you can target a specific version of Exchange by specifying version as a parameter.</span></span> `ExchangeService service = new ExchangeService(ExchangeVersion.Exchange2007_SP1);`
  
2. <span data-ttu-id="56637-150">设置将请求发送到 Exchange server 的用户的凭据。</span><span class="sxs-lookup"><span data-stu-id="56637-150">Set the credentials of the user who sends requests to the Exchange server.</span></span> <span data-ttu-id="56637-151">如果您想要连接到 EWS 登录到域的计算机中，使用的身份验证的用户凭据设置为**true**， **ExchangeService**在对象上**使用**属性。</span><span class="sxs-lookup"><span data-stu-id="56637-151">If you want to connect to EWS from a computer that is logged on to the domain, using the credentials of the authenticated user, set the **UseDefaultCredentials** property on the **ExchangeService** object to **true**.</span></span>
    
   ```cs
    // Connect by using the default credentials of the authenticated user.
    service.UseDefaultCredentials = true;
   ```

   <span data-ttu-id="56637-152">如果您不希望连接使用默认的用户凭据，在要显式指定不同的用户的凭据的**ExchangeService**对象上设置**凭据**属性。</span><span class="sxs-lookup"><span data-stu-id="56637-152">If you do not want to connect by using the default user credentials, set the **Credentials** property on the **ExchangeService** object to explicitly specify the credentials of a different user.</span></span> <span data-ttu-id="56637-153">如果使用 Exchange Online 或 Exchange Online 作为 Office 365 的一部分，您将使用基本身份验证，只有用户名和密码。</span><span class="sxs-lookup"><span data-stu-id="56637-153">If you are using Exchange Online or Exchange Online as part of Office 365, you'll use basic authentication, with just a user name and password.</span></span> <span data-ttu-id="56637-154">为 NTLM 身份验证所需的域名。</span><span class="sxs-lookup"><span data-stu-id="56637-154">A domain name is required for NTLM authentication.</span></span> 
    
   ```cs
    // Connect by using the credentials of user1 at contoso.com.
    service.Credentials = new WebCredentials("user1@contoso.com", "password");
   ```

   <span data-ttu-id="56637-155">您还可以使用的域用户名和密码指定用户的凭据。</span><span class="sxs-lookup"><span data-stu-id="56637-155">You can also specify the credentials of the user by using the user's domain name and password.</span></span>
    
   ```cs
    // Connect by using the credentials of contoso/user1.
    service.Credentials = new WebCredentials("user1", "password", "contoso");
   ```

   > [!NOTE]
   > <span data-ttu-id="56637-156">如果**使用**属性设置为**true**，则忽略**凭据**属性的值。</span><span class="sxs-lookup"><span data-stu-id="56637-156">If the **UseDefaultCredentials** property is set to **true**, the value of the **Credentials** property is ignored.</span></span> 
  
3. <span data-ttu-id="56637-157">设置 EWS 终结点 URL。</span><span class="sxs-lookup"><span data-stu-id="56637-157">Set the URL of the EWS endpoint.</span></span> <span data-ttu-id="56637-158">此 URL 中查找客户端访问服务器上的 exchange.asmx 文件。</span><span class="sxs-lookup"><span data-stu-id="56637-158">This URL locates the exchange.asmx file on Client Access server.</span></span>
    
   ```cs
    // Use Autodiscover to set the URL endpoint.
    service.AutodiscoverUrl("user1@contoso.com");
   ```

   > [!NOTE]
   >  <span data-ttu-id="56637-159">尽管您可以为硬编码值来显式设置**ExchangeService**的**Url**属性，我们建议您改用自动发现服务，原因如下： > 自动发现确定给定用户的最佳终结点（终结点靠近用户的邮箱服务器）。</span><span class="sxs-lookup"><span data-stu-id="56637-159">Although you can explicitly set the **Url** property of the **ExchangeService** to a hardcoded value, we recommend that you use the Autodiscover service instead, for the following reasons: >  Autodiscover determines the best endpoint for a given user (the endpoint that is closest to the user's Mailbox server).</span></span> <span data-ttu-id="56637-160">> 如果部署了新的客户端访问服务器，则可能更改 EWS URL。</span><span class="sxs-lookup"><span data-stu-id="56637-160">>  The EWS URL might change if new Client Access servers are deployed.</span></span> <span data-ttu-id="56637-161">在此方案中，使用[自动发现](autodiscover-for-exchange.md)意味着不必代码进行更改。</span><span class="sxs-lookup"><span data-stu-id="56637-161">In this scenario, using [Autodiscover](autodiscover-for-exchange.md) means no code changes are necessary.</span></span> <span data-ttu-id="56637-162">> 您应显式设置的 URL 或呼叫**AutodiscoverUrl**，但不是应执行两项操作。</span><span class="sxs-lookup"><span data-stu-id="56637-162">>  You should either set the URL explicitly or call **AutodiscoverUrl**, but you should not do both.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="56637-163">另请参阅</span><span class="sxs-lookup"><span data-stu-id="56637-163">See also</span></span>

- [<span data-ttu-id="56637-164">EWS 托管 API 客户端应用程序入门</span><span class="sxs-lookup"><span data-stu-id="56637-164">Get started with EWS Managed API client applications</span></span>](get-started-with-ews-managed-api-client-applications.md) 
- [<span data-ttu-id="56637-165">使用 Autodiscover 以查找连接点</span><span class="sxs-lookup"><span data-stu-id="56637-165">Use Autodiscover to find connection points</span></span>](how-to-use-autodiscover-to-find-connection-points.md)   
- [<span data-ttu-id="56637-166">开发 Exchange Web 服务客户端</span><span class="sxs-lookup"><span data-stu-id="56637-166">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    

