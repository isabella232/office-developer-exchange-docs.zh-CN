---
title: Exchange 的自动发现 web 服务参考
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a01124a8-a8cf-4b80-8625-d7ee05690bca
description: 在 Exchange 中查找自动发现 web 服务的引用内容。
ms.openlocfilehash: ce7f2bbd662a5e61959c7e3c6748f0cf40cc4fb3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466869"
---
# <a name="autodiscover-web-service-reference-for-exchange"></a><span data-ttu-id="e548b-103">Exchange 的自动发现 web 服务参考</span><span class="sxs-lookup"><span data-stu-id="e548b-103">Autodiscover web service reference for Exchange</span></span>

<span data-ttu-id="e548b-104">在 Exchange 中查找自动发现 web 服务的引用内容。</span><span class="sxs-lookup"><span data-stu-id="e548b-104">Find reference content for the Autodiscover web service in Exchange.</span></span>
  
<span data-ttu-id="e548b-105">自动发现 web 服务提供了您的应用程序用来创建与 Exchange 服务器的连接的配置信息。</span><span class="sxs-lookup"><span data-stu-id="e548b-105">The Autodiscover web service provides the configuration information that your application uses to create a connection to an Exchange server.</span></span> <span data-ttu-id="e548b-106">您可以使用下列选项之一连接到自动发现：</span><span class="sxs-lookup"><span data-stu-id="e548b-106">You can use one of the following options to connect to Autodiscover:</span></span>
  
- <span data-ttu-id="e548b-107">SOAP 自动发现服务—可用于连接到以 Exchange 2010 开头的 Exchange 版本的客户端，包括 Exchange Online。</span><span class="sxs-lookup"><span data-stu-id="e548b-107">SOAP Autodiscover service —Available to clients that connect to versions of Exchange starting with Exchange 2010, including Exchange Online.</span></span>
    
- <span data-ttu-id="e548b-108">"纯旧 XML" （POX）自动发现服务—可用于连接到以 Exchange 2007 开头的 Exchange 版本的客户端（包括 Exchange Online）。</span><span class="sxs-lookup"><span data-stu-id="e548b-108">"plain old XML" (POX) Autodiscover service — Available to clients that connect to versions of Exchange starting with Exchange 2007, including Exchange Online.</span></span> 
    
<span data-ttu-id="e548b-109">SOAP 和 POX 自动发现服务都可以提供您的客户端将用于创建与 Exchange 服务器的连接的配置信息。</span><span class="sxs-lookup"><span data-stu-id="e548b-109">Both the SOAP and the POX Autodiscover service can provide the configuration information that your client will use to create a connection to an Exchange server.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e548b-110">对于从 Exchange 2010 开始的 Exchange 版本，我们建议使用 SOAP 自动发现服务，而不是 POX 自动发现服务。</span><span class="sxs-lookup"><span data-stu-id="e548b-110">For versions of Exchange starting with Exchange 2010, we recommend that you use the SOAP Autodiscover service instead of the POX Autodiscover service.</span></span> <span data-ttu-id="e548b-111">SOAP 自动发现服务提供批量自动发现设置请求，并更精确地控制响应中返回的设置。</span><span class="sxs-lookup"><span data-stu-id="e548b-111">The SOAP Autodiscover service provides batched Autodiscover setting requests and more granular control over which settings are returned in the response.</span></span> 
  
<span data-ttu-id="e548b-112">本节包含有关 SOAP 自动发现服务和 POX 自动发现服务的参考信息。</span><span class="sxs-lookup"><span data-stu-id="e548b-112">This section contains reference information for the SOAP Autodiscover service and the POX Autodiscover service.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="e548b-113">本节内容</span><span class="sxs-lookup"><span data-stu-id="e548b-113">In this section</span></span>
<span data-ttu-id="e548b-114"><a name="bk_InThisSection"> </a></span><span class="sxs-lookup"><span data-stu-id="e548b-114"><a name="bk_InThisSection"> </a></span></span>

- [<span data-ttu-id="e548b-115">Exchange 的 SOAP 自动发现 web 服务参考</span><span class="sxs-lookup"><span data-stu-id="e548b-115">SOAP Autodiscover web service reference for Exchange</span></span>](soap-autodiscover-web-service-reference-for-exchange.md)
    
- [<span data-ttu-id="e548b-116">Exchange 的 POX 自动发现 web 服务参考</span><span class="sxs-lookup"><span data-stu-id="e548b-116">POX Autodiscover web service reference for Exchange</span></span>](pox-autodiscover-web-service-reference-for-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="e548b-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e548b-117">See also</span></span>

- [<span data-ttu-id="e548b-118">Exchange Web 服务应用</span><span class="sxs-lookup"><span data-stu-id="e548b-118">Web services reference for Exchange</span></span>](web-services-reference-for-exchange.md)
- [<span data-ttu-id="e548b-119">自动发现服务（SOAP）</span><span class="sxs-lookup"><span data-stu-id="e548b-119">Autodiscover Service (SOAP)</span></span>](https://msdn.microsoft.com/library/e24d1a1f-0d20-4bd9-ae4c-9112ecacea78%28Office.15%29.aspx)
- [<span data-ttu-id="e548b-120">自动发现服务（POX）</span><span class="sxs-lookup"><span data-stu-id="e548b-120">Autodiscover Service (POX)</span></span>](https://msdn.microsoft.com/library/13c54de3-a91c-4424-8732-99dd8f2162ec%28Office.15%29.aspx)
    

