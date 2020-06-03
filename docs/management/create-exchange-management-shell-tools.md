---
title: 创建 Exchange 命令行管理程序工具
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 46e4812f-37a8-449f-bd37-bc4a94605db9
description: 查找有关开始为 Exchange 创建 Exchange 命令行管理程序工具的信息。
ms.openlocfilehash: c6e11fa5b55aa514b12f4f52bc9346ac213d3781
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463725"
---
# <a name="create-exchange-management-shell-tools"></a><span data-ttu-id="a8310-103">创建 Exchange 命令行管理程序工具</span><span class="sxs-lookup"><span data-stu-id="a8310-103">Create Exchange Management Shell tools</span></span>

<span data-ttu-id="a8310-104">查找有关开始为 Exchange 创建 Exchange 命令行管理程序工具的信息。</span><span class="sxs-lookup"><span data-stu-id="a8310-104">Find information to get started creating Exchange Management Shell tools for Exchange.</span></span>

<span data-ttu-id="a8310-105">**适用于：** Exchange Online |Exchange Server 2013 |Office 365</span><span class="sxs-lookup"><span data-stu-id="a8310-105">**Applies to:** Exchange Online | Exchange Server 2013 | Office 365</span></span>
  
<span data-ttu-id="a8310-106">Exchange 命令行管理程序基于 Windows PowerShell 平台提供了一组丰富的命令，用于管理 Exchange Online、作为 Office 365 的一部分的 Exchange Online 或从 Exchange 2013 开始的 Exchange 内部部署版本。</span><span class="sxs-lookup"><span data-stu-id="a8310-106">The Exchange Management Shell provides a rich set of commands, based on the Windows PowerShell platform, for managing Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange 2013.</span></span> <span data-ttu-id="a8310-107">您可以使用 Exchange 命令行管理程序命令，通过直接执行命令或使用命令脚本来自动管理服务器。</span><span class="sxs-lookup"><span data-stu-id="a8310-107">You can use Exchange Management Shell commands to automate the administration of a server by directly executing the commands, or by using command scripts.</span></span>
  
<span data-ttu-id="a8310-108">如果需要在承载应用程序（如在管理员桌面上运行的管理应用程序或基于 web 的应用程序）中使用 Exchange 命令行管理程序命令，则可以从 Visual Basic 或 c # 应用程序中调用 Exchange 命令行管理程序 cmdlet 以管理 Exchange 服务器。</span><span class="sxs-lookup"><span data-stu-id="a8310-108">If you need to use Exchange Management Shell commands from within a hosting application, such as an administrative application that is running on the administrator's desktop or through a web-based application, you can call Exchange Management Shell cmdlets from within your Visual Basic or C# application to manage an Exchange server.</span></span>
  
## <a name="get-started-with-exchange-management-shell-tools"></a><span data-ttu-id="a8310-109">开始使用 Exchange 命令行管理程序工具</span><span class="sxs-lookup"><span data-stu-id="a8310-109">Get started with Exchange Management Shell tools</span></span>
<span data-ttu-id="a8310-110"><a name="SP15GettingStartedTemplate_WhatDoYouNeed"> </a></span><span class="sxs-lookup"><span data-stu-id="a8310-110"><a name="SP15GettingStartedTemplate_WhatDoYouNeed"> </a></span></span>

<span data-ttu-id="a8310-111">如果您熟悉如何创建 Windows PowerShell 主机应用程序，并且想要查看演示如何从应用程序调用 Exchange 命令行管理程序 cmdlet 的示例，或者要查看您可以使用 Exchange 命令行管理程序 cmdlet 创建的应用程序类型的示例，请参阅[使用 Exchange 命令行管理程序获取邮件用户列表](how-to-get-a-list-of-mail-users-by-using-the-exchange-management-shell.md)。</span><span class="sxs-lookup"><span data-stu-id="a8310-111">If you are familiar with creating Windows PowerShell host applications and want to see an example that shows how to call the Exchange Management Shell cmdlets from an application, or to see an example of the types of applications that you can create by using the Exchange Management Shell cmdlets, see [Get a list of mail users by using the Exchange Management Shell](how-to-get-a-list-of-mail-users-by-using-the-exchange-management-shell.md).</span></span>
  
<span data-ttu-id="a8310-112">Exchange 命令行管理程序 cmdlet 是 Windows PowerShell 的扩展，它是一种专门为系统管理设计的基于任务的命令行命令行命令行管理程序和脚本语言。</span><span class="sxs-lookup"><span data-stu-id="a8310-112">The Exchange Management Shell cmdlets are extensions to Windows PowerShell, a task-based command-line shell and scripting language that is designed specifically for system administration.</span></span> <span data-ttu-id="a8310-113">Windows PowerShell 构建在 .NET Framework 之上，为 cmdlet、提供程序和主机应用程序开发人员提供了面向对象的 API。</span><span class="sxs-lookup"><span data-stu-id="a8310-113">Windows PowerShell is built on the .NET Framework, and provides an object-oriented API for cmdlet, provider, and host application developers.</span></span> <span data-ttu-id="a8310-114">若要了解 Windows PowerShell 编程，请参阅[Windows POWERSHELL SDK](https://msdn.microsoft.com/library/dd835506%28VS.85%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="a8310-114">To learn about Windows PowerShell programming, see the [Windows PowerShell SDK](https://msdn.microsoft.com/library/dd835506%28VS.85%29.aspx).</span></span>
  
<span data-ttu-id="a8310-115">Exchange 命令行管理程序 cmdlet 接受并返回对象。</span><span class="sxs-lookup"><span data-stu-id="a8310-115">The Exchange Management Shell cmdlets accept and return objects.</span></span> <span data-ttu-id="a8310-116">有关 Exchange 命令行管理程序 cmdlet 及其输入和输出类型的列表，请参阅[Exchange 命令行管理程序 cmdlet 的输入和输出类型](exchange-management-shell-cmdlet-input-and-output-types.md)。</span><span class="sxs-lookup"><span data-stu-id="a8310-116">For a list of Exchange management shell cmdlets and their input and output types, see [Exchange Management Shell cmdlet input and output types](exchange-management-shell-cmdlet-input-and-output-types.md).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="a8310-117">本节内容</span><span class="sxs-lookup"><span data-stu-id="a8310-117">In this section</span></span>

- [<span data-ttu-id="a8310-118">新的和更新的 Exchange 命令行管理程序 cmdlet</span><span class="sxs-lookup"><span data-stu-id="a8310-118">New and updated Exchange Management Shell cmdlets</span></span>](new-and-updated-exchange-management-shell-cmdlets.md)  
- [<span data-ttu-id="a8310-119">Exchange 命令行管理程序 cmdlet 的输入和输出类型</span><span class="sxs-lookup"><span data-stu-id="a8310-119">Exchange Management Shell cmdlet input and output types</span></span>](exchange-management-shell-cmdlet-input-and-output-types.md)
- [<span data-ttu-id="a8310-120">使用 Exchange 命令行管理程序获取邮件用户列表</span><span class="sxs-lookup"><span data-stu-id="a8310-120">Get a list of mail users by using the Exchange Management Shell</span></span>](how-to-get-a-list-of-mail-users-by-using-the-exchange-management-shell.md)
- [<span data-ttu-id="a8310-121">使用 Exchange 命令行管理程序 cmdlet 响应</span><span class="sxs-lookup"><span data-stu-id="a8310-121">Use the Exchange Management Shell cmdlet response</span></span>](how-to-use-the-exchange-management-shell-cmdlet-response.md)


## <a name="see-also"></a><span data-ttu-id="a8310-122">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a8310-122">See also</span></span>

- [<span data-ttu-id="a8310-123">Exchange 命令行管理程序命名空间</span><span class="sxs-lookup"><span data-stu-id="a8310-123">Exchange Management Shell namespaces</span></span>](exchange-management-shell-namespaces.md)  
- [<span data-ttu-id="a8310-124">Exchange Server PowerShell （Exchange 命令行管理程序）</span><span class="sxs-lookup"><span data-stu-id="a8310-124">Exchange Server PowerShell (Exchange Management Shell)</span></span>](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)  
- [<span data-ttu-id="a8310-125">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="a8310-125">Windows PowerShell</span></span>](https://msdn.microsoft.com/library/dd835506%28v=vs.85%29.aspx)
    

