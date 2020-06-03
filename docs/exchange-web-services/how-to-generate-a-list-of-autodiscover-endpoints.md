---
title: 生成自动发现终结点列表
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 82394d3c-9fc7-4b3c-b48d-1fe983c198f7
description: 了解如何生成自动发现终结点的按优先级排序的列表。
localization_priority: Priority
ms.openlocfilehash: db888c8d562f57bd46edc251f4917e9e03d85d95
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528096"
---
# <a name="generate-a-list-of-autodiscover-endpoints"></a><span data-ttu-id="009ab-103">生成自动发现终结点列表</span><span class="sxs-lookup"><span data-stu-id="009ab-103">Generate a list of Autodiscover endpoints</span></span>

<span data-ttu-id="009ab-104">了解如何生成自动发现终结点的按优先级排序的列表。</span><span class="sxs-lookup"><span data-stu-id="009ab-104">Find out how to generate a prioritized list of Autodiscover endpoints.</span></span>
  
<span data-ttu-id="009ab-105">[自动发现过程](autodiscover-for-exchange.md)中的第一个任务是为您的应用程序生成要尝试的自动发现终结点的列表。</span><span class="sxs-lookup"><span data-stu-id="009ab-105">The first task in the [Autodiscover process](autodiscover-for-exchange.md) is to generate a list of Autodiscover endpoints for your application to try.</span></span> <span data-ttu-id="009ab-106">这些自动发现终结点可以来自[SCP 查找](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md)，也可以从用户的电子邮件地址派生。</span><span class="sxs-lookup"><span data-stu-id="009ab-106">These Autodiscover endpoints can come from an [SCP lookup](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md) or can be derived from the user's email address.</span></span> <span data-ttu-id="009ab-107">最后，您可以最终使用大量终结点。</span><span class="sxs-lookup"><span data-stu-id="009ab-107">In the end, you can end up with a large number of endpoints.</span></span> <span data-ttu-id="009ab-108">我们来看看如何按优先级对其进行组织。</span><span class="sxs-lookup"><span data-stu-id="009ab-108">Let's take a look at how you can organize them by priority.</span></span> 
  
## <a name="start-with-scp-lookup"></a><span data-ttu-id="009ab-109">从 SCP 查找开始</span><span class="sxs-lookup"><span data-stu-id="009ab-109">Start with SCP lookup</span></span>
<span data-ttu-id="009ab-110"><a name="bk_StartWithScp"> </a></span><span class="sxs-lookup"><span data-stu-id="009ab-110"><a name="bk_StartWithScp"> </a></span></span>

<span data-ttu-id="009ab-111">来自[SCP 查找](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md)的自动发现终结点应具有列表中的最高优先级。</span><span class="sxs-lookup"><span data-stu-id="009ab-111">Autodiscover endpoints that come from an [SCP lookup](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md) should have top priority in your list.</span></span> <span data-ttu-id="009ab-112">管理员可以将 SCP 对象配置为将客户端路由到最接近或最高效的自动发现终结点，因此最好从这些终结点开始。</span><span class="sxs-lookup"><span data-stu-id="009ab-112">Administrators can configure SCP objects to route your client to the closest or most efficient Autodiscover endpoint, so it is a good idea to start with these endpoints.</span></span> <span data-ttu-id="009ab-113">由于 SCP 查找过程具有其自己的优先顺序方案，因此 SCP 查找的结果已进行了优先级划分，如下所示：</span><span class="sxs-lookup"><span data-stu-id="009ab-113">Because the SCP lookup process has its own prioritization scheme, the results of an SCP lookup are already prioritized, as follows:</span></span> 
  
1. <span data-ttu-id="009ab-114">从作用域到客户端计算机所属的 Active Directory 站点的 SCP 对象的自动发现终结点。</span><span class="sxs-lookup"><span data-stu-id="009ab-114">Autodiscover endpoints from SCP objects scoped to the Active Directory site that the client computer belongs to.</span></span>
    
2. <span data-ttu-id="009ab-115">来自不限于任何 Active Directory 站点的 SCP 对象的自动发现终结点。</span><span class="sxs-lookup"><span data-stu-id="009ab-115">Autodiscover endpoints from SCP objects not scoped to any Active Directory site.</span></span>
    
3. <span data-ttu-id="009ab-116">来自 SCP 对象的自动发现终结点位于与客户端计算机所属的站点不同的 Active Directory 站点范围内。</span><span class="sxs-lookup"><span data-stu-id="009ab-116">Autodiscover endpoints from SCP objects scoped to a different Active Directory site than the site that the client computer belongs to.</span></span>
    
<span data-ttu-id="009ab-117">获得 SCP 查找过程的结果后，可以添加从用户的电子邮件地址派生的终结点。</span><span class="sxs-lookup"><span data-stu-id="009ab-117">After you have the results of the SCP lookup process, you can add endpoints that derive from the user's email address.</span></span> <span data-ttu-id="009ab-118">这些项可用作一组默认的终结点和回退，以防没有 SCP 结果或从 SCP 查找返回的终结点不足。</span><span class="sxs-lookup"><span data-stu-id="009ab-118">These can serve as a default set of endpoints and a fallback in case there are no SCP results or the endpoints returned from the SCP lookup are not sufficient.</span></span>
  
## <a name="add-endpoints-derived-from-the-users-email-address"></a><span data-ttu-id="009ab-119">添加从用户的电子邮件地址派生的终结点</span><span class="sxs-lookup"><span data-stu-id="009ab-119">Add endpoints derived from the user's email address</span></span>
<span data-ttu-id="009ab-120"><a name="bk_AddDerivedEndpoints"> </a></span><span class="sxs-lookup"><span data-stu-id="009ab-120"><a name="bk_AddDerivedEndpoints"> </a></span></span>

<span data-ttu-id="009ab-121">当 SCP 查找不起作用，或者 SCP 查找返回的终结点不返回成功响应时，可以从用户的电子邮件地址派生一组默认的自动发现终结点。</span><span class="sxs-lookup"><span data-stu-id="009ab-121">When SCP lookup doesn't work, or the endpoints returned by the SCP lookup don't return a successful response, you can derive a set of default Autodiscover endpoints from the user's email address.</span></span> <span data-ttu-id="009ab-122">这些终结点的优先级应低于来自 SCP 查找的优先级，但如果 SCP 查找不成功，则可能需要这些终结点。</span><span class="sxs-lookup"><span data-stu-id="009ab-122">These endpoints should be a lower priority than any that come from an SCP lookup, but you might need them if the SCP lookup was not successful.</span></span>
  
### <a name="to-derive-autodiscover-endpoints"></a><span data-ttu-id="009ab-123">派生自动发现终结点</span><span class="sxs-lookup"><span data-stu-id="009ab-123">To derive Autodiscover endpoints</span></span>

1. <span data-ttu-id="009ab-124">从用户的电子邮件地址中提取域名。</span><span class="sxs-lookup"><span data-stu-id="009ab-124">Extract the domain name from the user's email address.</span></span> <span data-ttu-id="009ab-125">例如，如果用户的电子邮件地址为 Sadie.Daniels@contoso.com，则域名将为 contoso.com。</span><span class="sxs-lookup"><span data-stu-id="009ab-125">For example, if the user's email address is Sadie.Daniels@contoso.com, the domain name would be contoso.com.</span></span>
    
2. <span data-ttu-id="009ab-126">构造不带文件扩展名的终结点 Url，格式如下：</span><span class="sxs-lookup"><span data-stu-id="009ab-126">Construct endpoint URLs without file extensions in the following formats:</span></span>
    
  - <span data-ttu-id="009ab-127">"https://" + domain + "/autodiscover/autodiscover"</span><span class="sxs-lookup"><span data-stu-id="009ab-127">"https://" + domain + "/autodiscover/autodiscover"</span></span>
    
  - <span data-ttu-id="009ab-128">"https://autodiscover."</span><span class="sxs-lookup"><span data-stu-id="009ab-128">"https://autodiscover."</span></span> <span data-ttu-id="009ab-129">+ domain + "/autodiscover/autodiscover"</span><span class="sxs-lookup"><span data-stu-id="009ab-129">+ domain + "/autodiscover/autodiscover"</span></span>
    
<span data-ttu-id="009ab-130">编译从 SCP 查找和用户的电子邮件地址派生的终结点的列表后，可能需要在这些 Url 中修改文件扩展名，具体取决于您使用的是[SOAP 自动发现 web 服务](https://msdn.microsoft.com/library/61c21ea9-7fea-4f56-8ada-bf80e1e6b074%28Office.15%29.aspx)还是[POX 自动发现 web 服务](https://msdn.microsoft.com/library/877152f0-f4b1-4f63-b2ce-924f4bdf2d20%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="009ab-130">After you compile the list of endpoint URLs that derive from both SCP lookup and the user's email address, you might need to revise file name extensions in those URLs, depending on whether you're using the [SOAP Autodiscover web service](https://msdn.microsoft.com/library/61c21ea9-7fea-4f56-8ada-bf80e1e6b074%28Office.15%29.aspx) or the [POX Autodiscover web service](https://msdn.microsoft.com/library/877152f0-f4b1-4f63-b2ce-924f4bdf2d20%28Office.15%29.aspx).</span></span>
  
## <a name="add-or-replace-file-name-extensions-in-endpoint-urls"></a><span data-ttu-id="009ab-131">在终结点 Url 中添加或替换文件扩展名</span><span class="sxs-lookup"><span data-stu-id="009ab-131">Add or replace file name extensions in endpoint URLs</span></span>
<span data-ttu-id="009ab-132"><a name="bk_FileExtensions"> </a></span><span class="sxs-lookup"><span data-stu-id="009ab-132"><a name="bk_FileExtensions"> </a></span></span>

<span data-ttu-id="009ab-133">您可以使用 SOAP 自动发现 web 服务或 POX 自动发现 web 服务来访问自动发现服务。</span><span class="sxs-lookup"><span data-stu-id="009ab-133">You can access the Autodiscover service by using either the SOAP Autodiscover web service or the POX Autodiscover web service.</span></span> <span data-ttu-id="009ab-134">每个服务使用类似的终结点 Url，唯一的区别是文件扩展名。</span><span class="sxs-lookup"><span data-stu-id="009ab-134">Each service uses similar endpoint URLs, with the only difference being the file name extension.</span></span> <span data-ttu-id="009ab-135">SOAP 自动发现 web 服务使用 ".svc" 文件扩展名，POX 自动发现 web 服务使用 ".xml" 文件扩展名。</span><span class="sxs-lookup"><span data-stu-id="009ab-135">The SOAP Autodiscover web service uses the ".svc" file name extension, and the POX Autodiscover web service uses the ".xml" file name extension.</span></span>
  
<span data-ttu-id="009ab-136">默认情况下，从 SCP 查找返回的自动发现终结点 Url 是 POX Url。</span><span class="sxs-lookup"><span data-stu-id="009ab-136">By default, the Autodiscover endpoint URLs returned from an SCP lookup are POX URLs.</span></span> <span data-ttu-id="009ab-137">但是，如果您使用的是 SOAP 自动发现，则只需将文件扩展名从 ".xml" 更改为 ".svc"，然后尝试 SOAP 请求即可。</span><span class="sxs-lookup"><span data-stu-id="009ab-137">However, if you are using SOAP Autodiscover, you can simply change the file name extension from ".xml" to ".svc" and try a SOAP request.</span></span>
  
<span data-ttu-id="009ab-138">对于派生的自动发现终结点 Url，将省略文件扩展名。</span><span class="sxs-lookup"><span data-stu-id="009ab-138">For the derived Autodiscover endpoint URLs, the file extension is omitted.</span></span> <span data-ttu-id="009ab-139">在尝试 URL 之前，为要使用的自动发现 web 服务添加适当的文件扩展名。</span><span class="sxs-lookup"><span data-stu-id="009ab-139">Add the appropriate file extension for the Autodiscover web service you are using prior to trying the URL.</span></span>
  
## <a name="example-generating-a-list-of-autodiscover-endpoints"></a><span data-ttu-id="009ab-140">示例：生成自动发现终结点列表</span><span class="sxs-lookup"><span data-stu-id="009ab-140">Example: Generating a list of Autodiscover endpoints</span></span>
<span data-ttu-id="009ab-141"><a name="bk_Example"> </a></span><span class="sxs-lookup"><span data-stu-id="009ab-141"><a name="bk_Example"> </a></span></span>

<span data-ttu-id="009ab-142">我们来看一个示例。</span><span class="sxs-lookup"><span data-stu-id="009ab-142">Let's take a look at an example.</span></span> <span data-ttu-id="009ab-143">Sadie Daniels （Sadie.Daniels@contoso.com）是首次使用 Exchange Web 服务（EWS）应用程序。</span><span class="sxs-lookup"><span data-stu-id="009ab-143">Sadie Daniels (Sadie.Daniels@contoso.com) is using an Exchange Web Services (EWS) application for the first time.</span></span> <span data-ttu-id="009ab-144">应用程序使用自动发现来配置自身。</span><span class="sxs-lookup"><span data-stu-id="009ab-144">The application uses Autodiscover to configure itself.</span></span> <span data-ttu-id="009ab-145">Sadie 的计算机已加入 contoso.com 域，位于 Redmond Active Directory 站点中。</span><span class="sxs-lookup"><span data-stu-id="009ab-145">Sadie's computer is joined to the contoso.com domain and is in the Redmond Active Directory site.</span></span> <span data-ttu-id="009ab-146">应用程序将生成图1中所示的自动发现终结点的列表。</span><span class="sxs-lookup"><span data-stu-id="009ab-146">The application generates the list of Autodiscover endpoints shown in Figure 1.</span></span>
  
<span data-ttu-id="009ab-147">**图1：自动发现终结点的示例列表**</span><span class="sxs-lookup"><span data-stu-id="009ab-147">**Figure 1: Sample list of Autodiscover endpoints**</span></span>

![自动发现终结点的示例列表，显示从 SCP 查找获得的终结点，具有比派生终结点更高的优先级。](media/Ex15_Autodiscover_GenerateList_Example.png)
  
<span data-ttu-id="009ab-149">此示例中的 EWS 应用程序优先于 SOAP 自动发现 web 服务，因此在向其发送 SOAP 请求之前，它会将 SCP 结果的文件扩展名更改为 ".svc"。</span><span class="sxs-lookup"><span data-stu-id="009ab-149">The EWS application in this example prefers the SOAP Autodiscover web service, so it changes the file name extension for the SCP results to ".svc" before sending SOAP requests to them.</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="009ab-150">后续步骤</span><span class="sxs-lookup"><span data-stu-id="009ab-150">Next steps</span></span>
<span data-ttu-id="009ab-151"><a name="bk_NextSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="009ab-151"><a name="bk_NextSteps"> </a></span></span>

<span data-ttu-id="009ab-152">生成自动发现终结点的列表后，通过[向这些终结点发送请求来](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)尝试这些终结点。</span><span class="sxs-lookup"><span data-stu-id="009ab-152">After you generate a list of Autodiscover endpoints, try them by [sending requests to those endpoints](how-to-get-user-settings-from-exchange-by-using-autodiscover.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="009ab-153">另请参阅</span><span class="sxs-lookup"><span data-stu-id="009ab-153">See also</span></span>


- [<span data-ttu-id="009ab-154">Exchange 自动发现</span><span class="sxs-lookup"><span data-stu-id="009ab-154">Autodiscover for Exchange</span></span>](autodiscover-for-exchange.md)
    
- [<span data-ttu-id="009ab-155">通过使用 Exchange 中的 SCP 查找来找到自动发现终结点</span><span class="sxs-lookup"><span data-stu-id="009ab-155">Find Autodiscover endpoints by using SCP lookup in Exchange</span></span>](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md)
    
- [<span data-ttu-id="009ab-156">处理自动发现错误消息</span><span class="sxs-lookup"><span data-stu-id="009ab-156">Handling Autodiscover error messages</span></span>](handling-autodiscover-error-messages.md)
    

