---
title: Exchange Management Shell
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cc0c4fa-9e13-45cb-88da-0486f2ac1bd0
description: 查找有关如何使用 Exchange 命令行管理程序来开发用于 Exchange server 管理工具的信息。
ms.openlocfilehash: 1cb0328bdb0eebda0ce4eda929e1bfb21be451f4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753022"
---
# <a name="exchange-management-shell"></a><span data-ttu-id="b71ca-103">Exchange Management Shell</span><span class="sxs-lookup"><span data-stu-id="b71ca-103">Exchange Management Shell</span></span>

<span data-ttu-id="b71ca-104">查找有关如何使用 Exchange 命令行管理程序来开发用于 Exchange server 管理工具的信息。</span><span class="sxs-lookup"><span data-stu-id="b71ca-104">Find information about how to use the Exchange Management Shell to develop tools for Exchange server administration.</span></span>
  
<span data-ttu-id="b71ca-105">**适用于：** Exchange Online |Exchange Server 2013 |Office 365</span><span class="sxs-lookup"><span data-stu-id="b71ca-105">**Applies to:** Exchange Online | Exchange Server 2013 | Office 365</span></span>
  
<span data-ttu-id="b71ca-106">Exchange 命令行管理程序提供了一组丰富的命令，基于 Windows PowerShell 平台，用于管理 Exchange Online、 Exchange Online 作为 Office 365 的一部分或 Exchange 的内部部署版本开头 Exchange 2013。</span><span class="sxs-lookup"><span data-stu-id="b71ca-106">The Exchange Management Shell provides a rich set of commands, based on the Windows PowerShell platform, for managing Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange 2013.</span></span> <span data-ttu-id="b71ca-107">您可以使用 Exchange 命令行管理程序创建两种工具： 在 Windows PowerShell 环境中内, 工作的命令行脚本和工具的托管接口通过使用 Exchange 命令行管理程序 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b71ca-107">You can use the Exchange Management Shell to create two kinds of tools: command-line scripts that work within the Windows PowerShell environment, and tools that use the Exchange Management Shell cmdlets through a managed interface.</span></span> <span data-ttu-id="b71ca-108">托管应用程序可用于创建标准的 Windows 或基于 web 的用户界面来管理 Exchange 服务器。</span><span class="sxs-lookup"><span data-stu-id="b71ca-108">You can use managed applications to create a standard Windows or web-based UI to administer an Exchange server.</span></span> 
  
## <a name="what-you-need-to-know-about-the-exchange-management-shell"></a><span data-ttu-id="b71ca-109">您需要了解的有关 Exchange 命令行管理程序</span><span class="sxs-lookup"><span data-stu-id="b71ca-109">What you need to know about the Exchange Management Shell</span></span>

|<span data-ttu-id="b71ca-110">如果您想知道有关</span><span class="sxs-lookup"><span data-stu-id="b71ca-110">If you're wondering about</span></span>|<span data-ttu-id="b71ca-111">请参阅这个</span><span class="sxs-lookup"><span data-stu-id="b71ca-111">Read this</span></span>|
|:-----|:-----|
|<span data-ttu-id="b71ca-112">可用性</span><span class="sxs-lookup"><span data-stu-id="b71ca-112">Availability</span></span>  <br/> |<span data-ttu-id="b71ca-113">Exchange 命令行管理程序命令安装在运行 Exchange 启动与 Exchange 2007 版本的所有服务器上。</span><span class="sxs-lookup"><span data-stu-id="b71ca-113">Exchange Management Shell commands are installed on all servers running versions of Exchange starting with Exchange 2007.</span></span><br/><span data-ttu-id="b71ca-114">可以在运行 Windows PowerShell 2.0 的任何计算机上部署客户端应用程序。</span><span class="sxs-lookup"><span data-stu-id="b71ca-114">Client applications can be deployed on any computer running Windows PowerShell 2.0.</span></span><br/> <span data-ttu-id="b71ca-115">有关访问命令行管理程序的信息，请参阅[Exchange Server PowerShell (Exchange Management Shell)](https://docs.microsoft.com/en-us/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)。</span><span class="sxs-lookup"><span data-stu-id="b71ca-115">For information about accessing the shell, see [Exchange Server PowerShell (Exchange Management Shell)](https://docs.microsoft.com/en-us/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps).</span></span>  <br/> |
|<span data-ttu-id="b71ca-116">语言和工具</span><span class="sxs-lookup"><span data-stu-id="b71ca-116">Languages and tools</span></span>  <br/> |<span data-ttu-id="b71ca-117">您可以在任何文本编辑器创建 Exchange 命令行管理程序脚本。</span><span class="sxs-lookup"><span data-stu-id="b71ca-117">You can create Exchange Management Shell scripts in any text editor.</span></span><br/><span data-ttu-id="b71ca-118">您可以使用许多第三方工具之一创建可与 Exchange 命令行管理程序的 Windows PowerShell 脚本。</span><span class="sxs-lookup"><span data-stu-id="b71ca-118">You can use one of many third-party tools for creating Windows PowerShell scripts that can be used with the Exchange Management Shell.</span></span>  <br/> <span data-ttu-id="b71ca-119">[Exchange 命令行管理程序对象模型](exchange-management-shell-namespaces.md)基于.NET Framework。</span><span class="sxs-lookup"><span data-stu-id="b71ca-119">The [Exchange Management Shell object model](exchange-management-shell-namespaces.md) is based on the .NET Framework.</span></span><br/><span data-ttu-id="b71ca-120">您可以使用任何.NET 语言开发 Exchange 命令行管理程序应用程序。</span><span class="sxs-lookup"><span data-stu-id="b71ca-120">You can use any .NET language to develop Exchange Management Shell applications.</span></span>  <br/> |
|<span data-ttu-id="b71ca-121">可用测试和调试工具</span><span class="sxs-lookup"><span data-stu-id="b71ca-121">Available test and debug tools</span></span>  <br/> |<span data-ttu-id="b71ca-122">您可以使用许多第三方应用程序之一测试和调试 Exchange 命令行管理程序脚本。</span><span class="sxs-lookup"><span data-stu-id="b71ca-122">You can use one of many third-party applications to test and debug Exchange Management Shell scripts.</span></span>  <br/> <span data-ttu-id="b71ca-123">您可以使用 Visual Studio 和第三方工具进行测试和调试托管 Exchange 命令行管理程序应用程序。</span><span class="sxs-lookup"><span data-stu-id="b71ca-123">You can use Visual Studio and third-party tools to test and debug managed Exchange Management Shell applications.</span></span>  <br/> |
|<span data-ttu-id="b71ca-124">服务器平台要求</span><span class="sxs-lookup"><span data-stu-id="b71ca-124">Server platform requirements</span></span>  <br/> |<span data-ttu-id="b71ca-125">您可以使用 Exchange 命令行管理程序上已安装的 Windows PowerShell 2.0 任何 Exchange 服务器。</span><span class="sxs-lookup"><span data-stu-id="b71ca-125">You can use the Exchange Management Shell on any Exchange server that has Windows PowerShell 2.0 installed.</span></span>  <br/> |
|<span data-ttu-id="b71ca-126">客户端平台要求</span><span class="sxs-lookup"><span data-stu-id="b71ca-126">Client platform requirements</span></span>  <br/> |<span data-ttu-id="b71ca-127">Exchange 命令行管理程序客户端应用程序需要 Windows PowerShell 2.0。</span><span class="sxs-lookup"><span data-stu-id="b71ca-127">Exchange Management Shell client applications require Windows PowerShell 2.0.</span></span>  <br/> |
|<span data-ttu-id="b71ca-128">权限</span><span class="sxs-lookup"><span data-stu-id="b71ca-128">Permissions</span></span>  <br/> |<span data-ttu-id="b71ca-129">运行 Exchange 命令行管理程序应用程序要求用户在 Exchange 存储上具有对受影响的数据的基于角色的访问控制权限。</span><span class="sxs-lookup"><span data-stu-id="b71ca-129">Running an Exchange Management Shell application requires that the user have role-based access control rights to the affected data on the Exchange store.</span></span><br/><span data-ttu-id="b71ca-130">有关基于角色的访问控制的详细信息，请参阅[Understanding Role Based Access Control](http://technet.microsoft.com/en-us/library/dd298183.aspx)。</span><span class="sxs-lookup"><span data-stu-id="b71ca-130">For more information about role-based access control, see [Understanding Role Based Access Control](http://technet.microsoft.com/en-us/library/dd298183.aspx).</span></span>  <br/> |
   
<span data-ttu-id="b71ca-131">本节中的文章介绍了用于创建 Exchange 管理工具重要的 Exchange 命令行管理程序功能。</span><span class="sxs-lookup"><span data-stu-id="b71ca-131">The articles in this section describe Exchange Management Shell features that are important for creating Exchange management tools.</span></span> <span data-ttu-id="b71ca-132">有关规划、 配置或维护 Exchange 的信息，请参阅[Exchange](https://docs.microsoft.com/en-us/exchange/)站点。</span><span class="sxs-lookup"><span data-stu-id="b71ca-132">For information about planning, configuring, or maintaining Exchange, see the [Exchange](https://docs.microsoft.com/en-us/exchange/) site.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="b71ca-133">本节内容</span><span class="sxs-lookup"><span data-stu-id="b71ca-133">In this section</span></span>

- [<span data-ttu-id="b71ca-134">创建 Exchange 命令行管理程序工具</span><span class="sxs-lookup"><span data-stu-id="b71ca-134">Create Exchange Management Shell tools</span></span>](create-exchange-management-shell-tools.md)
    
- [<span data-ttu-id="b71ca-135">Exchange 命令行管理程序命名空间</span><span class="sxs-lookup"><span data-stu-id="b71ca-135">Exchange Management Shell namespaces</span></span>](exchange-management-shell-namespaces.md)
    
## <a name="see-also"></a><span data-ttu-id="b71ca-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b71ca-136">See also</span></span>
  
- [<span data-ttu-id="b71ca-137">Windows PowerShell 文档</span><span class="sxs-lookup"><span data-stu-id="b71ca-137">Windows PowerShell documentation</span></span>](https://docs.microsoft.com/en-us/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-6)
- [<span data-ttu-id="b71ca-138">PowerShell 脚本</span><span class="sxs-lookup"><span data-stu-id="b71ca-138">PowerShell scripting</span></span>](https://docs.microsoft.com/en-us/powershell/scripting/powershell-scripting?view=powershell-6)
    

