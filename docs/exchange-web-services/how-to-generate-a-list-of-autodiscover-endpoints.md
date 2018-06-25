---
title: 生成自动发现终结点的列表
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 82394d3c-9fc7-4b3c-b48d-1fe983c198f7
description: 了解如何生成自动发现终结点的优先级的列表。
ms.openlocfilehash: ccecacc9c8beef464727efbc9d1fced7a81f9b7c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752784"
---
# <a name="generate-a-list-of-autodiscover-endpoints"></a><span data-ttu-id="67455-103">生成自动发现终结点的列表</span><span class="sxs-lookup"><span data-stu-id="67455-103">Generate a list of Autodiscover endpoints</span></span>

<span data-ttu-id="67455-104">了解如何生成自动发现终结点的优先级的列表。</span><span class="sxs-lookup"><span data-stu-id="67455-104">Find out how to generate a prioritized list of Autodiscover endpoints.</span></span>
  
<span data-ttu-id="67455-105">[自动发现过程](autodiscover-for-exchange.md)的第一个任务是生成的应用程序尝试自动发现终结点列表。</span><span class="sxs-lookup"><span data-stu-id="67455-105">The first task in the [Autodiscover process](autodiscover-for-exchange.md) is to generate a list of Autodiscover endpoints for your application to try.</span></span> <span data-ttu-id="67455-106">这些自动发现终结点可以来自[SCP 查找](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md)或可从用户的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="67455-106">These Autodiscover endpoints can come from an [SCP lookup](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md) or can be derived from the user's email address.</span></span> <span data-ttu-id="67455-107">最后，您可以结尾数量较大的终结点。</span><span class="sxs-lookup"><span data-stu-id="67455-107">In the end, you can end up with a large number of endpoints.</span></span> <span data-ttu-id="67455-108">我们来看一下如何按优先级组织它们。</span><span class="sxs-lookup"><span data-stu-id="67455-108">Let's take a look at how you can organize them by priority.</span></span> 
  
## <a name="start-with-scp-lookup"></a><span data-ttu-id="67455-109">启动 SCP 查找</span><span class="sxs-lookup"><span data-stu-id="67455-109">Start with SCP lookup</span></span>
<span data-ttu-id="67455-110"><a name="bk_StartWithScp"> </a></span><span class="sxs-lookup"><span data-stu-id="67455-110"></span></span>

<span data-ttu-id="67455-111">来自[SCP 查找](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md)的自动发现终结点列表中应有最高的优先级。</span><span class="sxs-lookup"><span data-stu-id="67455-111">Autodiscover endpoints that come from an [SCP lookup](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md) should have top priority in your list.</span></span> <span data-ttu-id="67455-112">管理员可以配置要路由到最接近或最适合您自动发现终结点，您的客户端，使其与这些终结点开始，最好的 SCP 对象。</span><span class="sxs-lookup"><span data-stu-id="67455-112">Administrators can configure SCP objects to route your client to the closest or most efficient Autodiscover endpoint, so it is a good idea to start with these endpoints.</span></span> <span data-ttu-id="67455-113">SCP 查找过程具有自己的优先顺序方案，因为 SCP 查找的结果是已确定优先级、，如下所示：</span><span class="sxs-lookup"><span data-stu-id="67455-113">Because the SCP lookup process has its own prioritization scheme, the results of an SCP lookup are already prioritized, as follows:</span></span> 
  
1. <span data-ttu-id="67455-114">从 SCP 对象范围内的客户端计算机所属的 Active Directory 站点的自动发现终结点。</span><span class="sxs-lookup"><span data-stu-id="67455-114">Autodiscover endpoints from SCP objects scoped to the Active Directory site that the client computer belongs to.</span></span>
    
2. <span data-ttu-id="67455-115">从 SCP 对象不到任何 Active Directory 站点范围的自动发现终结点。</span><span class="sxs-lookup"><span data-stu-id="67455-115">Autodiscover endpoints from SCP objects not scoped to any Active Directory site.</span></span>
    
3. <span data-ttu-id="67455-116">从 SCP 对象范围内的客户端计算机所属的网站与不同的 Active Directory 站点的自动发现终结点。</span><span class="sxs-lookup"><span data-stu-id="67455-116">Autodiscover endpoints from SCP objects scoped to a different Active Directory site than the site that the client computer belongs to.</span></span>
    
<span data-ttu-id="67455-117">SCP 查找过程的结果后，您可以添加用户的电子邮件地址派生的终结点。</span><span class="sxs-lookup"><span data-stu-id="67455-117">After you have the results of the SCP lookup process, you can add endpoints that derive from the user's email address.</span></span> <span data-ttu-id="67455-118">这些可以作为没有 SCP 结果或从 SCP 查找返回的终结点没有足够的情况下，默认设置的终结点和后备。</span><span class="sxs-lookup"><span data-stu-id="67455-118">These can serve as a default set of endpoints and a fallback in case there are no SCP results or the endpoints returned from the SCP lookup are not sufficient.</span></span>
  
## <a name="add-endpoints-derived-from-the-users-email-address"></a><span data-ttu-id="67455-119">添加源自用户的电子邮件地址的终结点</span><span class="sxs-lookup"><span data-stu-id="67455-119">Add endpoints derived from the user's email address</span></span>
<span data-ttu-id="67455-120"><a name="bk_AddDerivedEndpoints"> </a></span><span class="sxs-lookup"><span data-stu-id="67455-120"></span></span>

<span data-ttu-id="67455-121">当 SCP 查找操作不起作用，或在 SCP 查找返回的终结点不返回成功响应时，您可以从用户的电子邮件地址派生一默认自动发现终结点。</span><span class="sxs-lookup"><span data-stu-id="67455-121">When SCP lookup doesn't work, or the endpoints returned by the SCP lookup don't return a successful response, you can derive a set of default Autodiscover endpoints from the user's email address.</span></span> <span data-ttu-id="67455-122">这些终结点应为较低的优先级高于任何来自 SCP 查找，但您可能需要如果 SCP 查找未成功完成。</span><span class="sxs-lookup"><span data-stu-id="67455-122">These endpoints should be a lower priority than any that come from an SCP lookup, but you might need them if the SCP lookup was not successful.</span></span>
  
### <a name="to-derive-autodiscover-endpoints"></a><span data-ttu-id="67455-123">派生自动发现终结点</span><span class="sxs-lookup"><span data-stu-id="67455-123">To derive Autodiscover endpoints</span></span>

1. <span data-ttu-id="67455-124">从用户的电子邮件地址中提取的域名。</span><span class="sxs-lookup"><span data-stu-id="67455-124">Extract the domain name from the user's email address.</span></span> <span data-ttu-id="67455-125">例如，如果用户的电子邮件地址，Sadie.Daniels@contoso.com 域名称将为 contoso.com。</span><span class="sxs-lookup"><span data-stu-id="67455-125">For example, if the user's email address is Sadie.Daniels@contoso.com, the domain name would be contoso.com.</span></span>
    
2. <span data-ttu-id="67455-126">构造无采用以下格式的文件扩展名的终结点 Url:</span><span class="sxs-lookup"><span data-stu-id="67455-126">Construct endpoint URLs without file extensions in the following formats:</span></span>
    
  - <span data-ttu-id="67455-127">"https://"+ 域 +"/ 自动发现/自动发现"</span><span class="sxs-lookup"><span data-stu-id="67455-127">"https://" + domain + "/autodiscover/autodiscover"</span></span>
    
  - <span data-ttu-id="67455-128">"https://autodiscover."</span><span class="sxs-lookup"><span data-stu-id="67455-128"></span></span> <span data-ttu-id="67455-129">域 +"/ 自动发现/自动发现"</span><span class="sxs-lookup"><span data-stu-id="67455-129">+ domain + "/autodiscover/autodiscover"</span></span>
    
<span data-ttu-id="67455-130">编译从 SCP 查找和用户的电子邮件地址中获得的终结点 Url 的列表后，您可能需要修改这些 Url，具体取决于是否正在使用[SOAP 自动发现 web 服务](http://msdn.microsoft.com/library/61c21ea9-7fea-4f56-8ada-bf80e1e6b074%28Office.15%29.aspx)或[POX 中的文件扩展名自动发现 web 服务](http://msdn.microsoft.com/library/877152f0-f4b1-4f63-b2ce-924f4bdf2d20%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="67455-130">After you compile the list of endpoint URLs that derive from both SCP lookup and the user's email address, you might need to revise file name extensions in those URLs, depending on whether you're using the [SOAP Autodiscover web service](http://msdn.microsoft.com/library/61c21ea9-7fea-4f56-8ada-bf80e1e6b074%28Office.15%29.aspx) or the [POX Autodiscover web service](http://msdn.microsoft.com/library/877152f0-f4b1-4f63-b2ce-924f4bdf2d20%28Office.15%29.aspx).</span></span>
  
## <a name="add-or-replace-file-name-extensions-in-endpoint-urls"></a><span data-ttu-id="67455-131">添加或替换终结点 Url 中的文件扩展名</span><span class="sxs-lookup"><span data-stu-id="67455-131">Add or replace file name extensions in endpoint URLs</span></span>
<span data-ttu-id="67455-132"><a name="bk_FileExtensions"> </a></span><span class="sxs-lookup"><span data-stu-id="67455-132"></span></span>

<span data-ttu-id="67455-133">您可以使用 SOAP 自动发现 web 服务或 POX 自动发现 web 服务访问的自动发现服务。</span><span class="sxs-lookup"><span data-stu-id="67455-133">You can access the Autodiscover service by using either the SOAP Autodiscover web service or the POX Autodiscover web service.</span></span> <span data-ttu-id="67455-134">每个服务将类似的终结点 Url，使用唯一的区别在于文件扩展名。</span><span class="sxs-lookup"><span data-stu-id="67455-134">Each service uses similar endpoint URLs, with the only difference being the file name extension.</span></span> <span data-ttu-id="67455-135">SOAP 自动发现 web 服务使用".svc"文件扩展名和 POX 自动发现 web 服务使用".xml"文件扩展名。</span><span class="sxs-lookup"><span data-stu-id="67455-135">The SOAP Autodiscover web service uses the ".svc" file name extension, and the POX Autodiscover web service uses the ".xml" file name extension.</span></span>
  
<span data-ttu-id="67455-136">默认情况下，自动发现终结点 Url 返回从 SCP 查找是 POX Url。</span><span class="sxs-lookup"><span data-stu-id="67455-136">By default, the Autodiscover endpoint URLs returned from an SCP lookup are POX URLs.</span></span> <span data-ttu-id="67455-137">但是，如果您使用 SOAP 自动发现，可以只需更改文件扩展名从".xml"为".svc"，并尝试 SOAP 请求。</span><span class="sxs-lookup"><span data-stu-id="67455-137">However, if you are using SOAP Autodiscover, you can simply change the file name extension from ".xml" to ".svc" and try a SOAP request.</span></span>
  
<span data-ttu-id="67455-138">派生的自动发现终结点 url，省略的文件扩展名。</span><span class="sxs-lookup"><span data-stu-id="67455-138">For the derived Autodiscover endpoint URLs, the file extension is omitted.</span></span> <span data-ttu-id="67455-139">添加适当的文件扩展名之前尝试 URL 使用自动发现 web 服务。</span><span class="sxs-lookup"><span data-stu-id="67455-139">Add the appropriate file extension for the Autodiscover web service you are using prior to trying the URL.</span></span>
  
## <a name="example-generating-a-list-of-autodiscover-endpoints"></a><span data-ttu-id="67455-140">示例： 生成自动发现终结点的列表</span><span class="sxs-lookup"><span data-stu-id="67455-140">Example: Generating a list of Autodiscover endpoints</span></span>
<span data-ttu-id="67455-141"><a name="bk_Example"> </a></span><span class="sxs-lookup"><span data-stu-id="67455-141"></span></span>

<span data-ttu-id="67455-142">我们来看看一个示例。</span><span class="sxs-lookup"><span data-stu-id="67455-142">Let's take a look at an example.</span></span> <span data-ttu-id="67455-143">Sadie Daniels (Sadie.Daniels@contoso.com) 首次使用 Exchange Web Services (EWS) 应用程序。</span><span class="sxs-lookup"><span data-stu-id="67455-143">Sadie Daniels (Sadie.Daniels@contoso.com) is using an Exchange Web Services (EWS) application for the first time.</span></span> <span data-ttu-id="67455-144">应用程序使用自动发现配置本身。</span><span class="sxs-lookup"><span data-stu-id="67455-144">The application uses Autodiscover to configure itself.</span></span> <span data-ttu-id="67455-145">Sadie 的计算机加入到 contoso.com 域和雷德蒙德 Active Directory 站点中。</span><span class="sxs-lookup"><span data-stu-id="67455-145">Sadie's computer is joined to the contoso.com domain and is in the Redmond Active Directory site.</span></span> <span data-ttu-id="67455-146">应用程序生成图 1 中显示的自动发现终结点的列表。</span><span class="sxs-lookup"><span data-stu-id="67455-146">The application generates the list of Autodiscover endpoints shown in Figure 1.</span></span>
  
<span data-ttu-id="67455-147">**图 1： 的自动发现终结点的示例列表**</span><span class="sxs-lookup"><span data-stu-id="67455-147">**Figure 1: Sample list of Autodiscover endpoints**</span></span>

![自动发现终结点的示例列表，显示从 SCP 查找获得的终结点，具有比派生终结点更高的优先级。](media/Ex15_Autodiscover_GenerateList_Example.png)
  
<span data-ttu-id="67455-149">此示例中的 EWS 应用喜欢 SOAP 自动发现 web 服务，因此它将更改 SCP 结果的文件扩展名为".svc"发送给他们的 SOAP 请求之前。</span><span class="sxs-lookup"><span data-stu-id="67455-149">The EWS application in this example prefers the SOAP Autodiscover web service, so it changes the file name extension for the SCP results to ".svc" before sending SOAP requests to them.</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="67455-150">后续步骤</span><span class="sxs-lookup"><span data-stu-id="67455-150">Next steps</span></span>
<span data-ttu-id="67455-151"><a name="bk_NextSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="67455-151"></span></span>

<span data-ttu-id="67455-152">生成的自动发现终结点列表后，尝试它们通过[发送到这些终结点的请求](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)。</span><span class="sxs-lookup"><span data-stu-id="67455-152">After you generate a list of Autodiscover endpoints, try them by [sending requests to those endpoints](how-to-get-user-settings-from-exchange-by-using-autodiscover.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="67455-153">另请参阅</span><span class="sxs-lookup"><span data-stu-id="67455-153">See also</span></span>


- [<span data-ttu-id="67455-154">Exchange 自动发现</span><span class="sxs-lookup"><span data-stu-id="67455-154">Autodiscover for Exchange</span></span>](autodiscover-for-exchange.md)
    
- [<span data-ttu-id="67455-155">在 Exchange 使用 SCP 查找来查找自动发现终结点</span><span class="sxs-lookup"><span data-stu-id="67455-155">Find Autodiscover endpoints by using SCP lookup in Exchange</span></span>](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md)
    
- [<span data-ttu-id="67455-156">处理自动发现错误消息</span><span class="sxs-lookup"><span data-stu-id="67455-156">Handling Autodiscover error messages</span></span>](handling-autodiscover-error-messages.md)
    

