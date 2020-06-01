---
title: Exchange 中的传输代理
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 36d63aa6-1b72-4670-b5c3-da685f3017cb
description: 查找有关 Exchange 2013 中的传输代理的信息。
ms.openlocfilehash: 62fb259672c47242a57b939deb4887e1e5519e2a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461756"
---
# <a name="transport-agents-in-exchange"></a><span data-ttu-id="49740-103">Exchange 中的传输代理</span><span class="sxs-lookup"><span data-stu-id="49740-103">Transport agents in Exchange</span></span>
  
<span data-ttu-id="49740-104">Exchange 2013 提供了一个类库，其中支持 Exchange 传输行为的扩展并启用内容类型的读取、写入和转换。</span><span class="sxs-lookup"><span data-stu-id="49740-104">Exchange 2013 provides a library of classes that support the extension of the Exchange transport behavior and enable the reading, writing, and converting of content types.</span></span> <span data-ttu-id="49740-105">您可以使用这些类创建在传输管道中读取、写入和处理邮件的 Exchange 传输应用程序。</span><span class="sxs-lookup"><span data-stu-id="49740-105">You can use these classes to create Exchange transport applications that read, write, and process messages in the transport pipeline.</span></span>
  
## <a name="what-you-need-to-know-about-transport-agents"></a><span data-ttu-id="49740-106">您需要了解的有关传输代理的信息</span><span class="sxs-lookup"><span data-stu-id="49740-106">What you need to know about transport agents</span></span>

|<span data-ttu-id="49740-107">如果你想要了解 .。。</span><span class="sxs-lookup"><span data-stu-id="49740-107">If you're wondering about…</span></span>|<span data-ttu-id="49740-108">请参阅这个</span><span class="sxs-lookup"><span data-stu-id="49740-108">Read this</span></span>|
|:-----|:-----|
|<span data-ttu-id="49740-109">供应情况</span><span class="sxs-lookup"><span data-stu-id="49740-109">Availability</span></span>  <br/> |<span data-ttu-id="49740-110">传输代理在从 Exchange 2007 开始的 Exchange 版本中可用。</span><span class="sxs-lookup"><span data-stu-id="49740-110">Transport agents are available in versions of Exchange starting with Exchange 2007.</span></span> <span data-ttu-id="49740-111">Office 365 或 Exchange Online 不支持传输代理。</span><span class="sxs-lookup"><span data-stu-id="49740-111">Transport agents are not supported in Office 365 or Exchange Online.</span></span>  <br/> |
|<span data-ttu-id="49740-112">远程使用情况</span><span class="sxs-lookup"><span data-stu-id="49740-112">Remote usage</span></span>  <br/> |<span data-ttu-id="49740-113">传输代理在 Exchange 服务器上运行，但不支持远程使用。</span><span class="sxs-lookup"><span data-stu-id="49740-113">Transport agents run on the Exchange server and do not support remote usage.</span></span>  <br/> |
|<span data-ttu-id="49740-114">支持的语言</span><span class="sxs-lookup"><span data-stu-id="49740-114">Languages supported</span></span>  <br/> |<span data-ttu-id="49740-115">可以使用任何 .NET Framework 语言来处理传输代理。</span><span class="sxs-lookup"><span data-stu-id="49740-115">You can use any .NET Framework language to work with transport agents.</span></span>  <br/> |
|<span data-ttu-id="49740-116">可用测试和调试工具</span><span class="sxs-lookup"><span data-stu-id="49740-116">Available test and debug tools</span></span>  <br/> |<span data-ttu-id="49740-117">使用 Visual studio 的版本从 Visual Studio 2012 开始，以调试传输代理。</span><span class="sxs-lookup"><span data-stu-id="49740-117">Use versions of Visual Studio starting with Visual Studio 2012 to debug transport agents.</span></span>  <br/> |
|<span data-ttu-id="49740-118">部署方法</span><span class="sxs-lookup"><span data-stu-id="49740-118">Deployment methods</span></span>  <br/> |<span data-ttu-id="49740-119">您可以使用[Exchange 命令行管理](../management/exchange-management-shell.md)程序脚本安装传输代理应用程序。</span><span class="sxs-lookup"><span data-stu-id="49740-119">You can install transport agent applications by using an [Exchange Management Shell](../management/exchange-management-shell.md) script.</span></span>  <br/> |
   
## <a name="in-this-section"></a><span data-ttu-id="49740-120">本节内容</span><span class="sxs-lookup"><span data-stu-id="49740-120">In this section</span></span>

- [<span data-ttu-id="49740-121">Exchange 2013 中的新的和更新的传输代理 Api</span><span class="sxs-lookup"><span data-stu-id="49740-121">New and updated transport agent APIs in Exchange 2013</span></span>](new-and-updated-transport-agent-apis-in-exchange-2013.md)
    
- [<span data-ttu-id="49740-122">Exchange 2013 的传输代理代码示例</span><span class="sxs-lookup"><span data-stu-id="49740-122">Transport agent code samples for Exchange 2013</span></span>](transport-agent-code-samples-for-exchange-2013.md)
    
- [<span data-ttu-id="49740-123">Exchange 2013 中的传输代理概念</span><span class="sxs-lookup"><span data-stu-id="49740-123">Transport agent concepts in Exchange 2013</span></span>](transport-agent-concepts-in-exchange-2013.md)
    
- [<span data-ttu-id="49740-124">读取和修改 Exchange 2013 传输管道中的邮件</span><span class="sxs-lookup"><span data-stu-id="49740-124">Reading and modifying messages in the Exchange 2013 transport pipeline</span></span>](reading-and-modifying-messages-in-the-exchange-2013-transport-pipeline.md)
    
- [<span data-ttu-id="49740-125">创建 Exchange 2013 的传输代理</span><span class="sxs-lookup"><span data-stu-id="49740-125">Creating transport agents for Exchange 2013</span></span>](creating-transport-agents-for-exchange-2013.md)
    
- [<span data-ttu-id="49740-126">Exchange 2013 的传输代理参考</span><span class="sxs-lookup"><span data-stu-id="49740-126">Transport agent reference for Exchange 2013</span></span>](transport-agent-reference-for-exchange-2013.md)
    
## <a name="see-also"></a><span data-ttu-id="49740-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="49740-127">See also</span></span>

- [<span data-ttu-id="49740-128">Exchange Online 和 Exchange 开发</span><span class="sxs-lookup"><span data-stu-id="49740-128">Exchange Online and Exchange development</span></span>](../exchange-server-development.md)    
- [<span data-ttu-id="49740-129">在 Exchange 中浏览 EWS 托管 API、EWS 和 Web 服务</span><span class="sxs-lookup"><span data-stu-id="49740-129">Explore the EWS Managed API, EWS, and web services in Exchange</span></span>](../exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)   
- [<span data-ttu-id="49740-130">Exchange 备份和还原</span><span class="sxs-lookup"><span data-stu-id="49740-130">Backup and restore for Exchange</span></span>](../backup-restore/backup-and-restore-for-exchange-2013.md) 
    

