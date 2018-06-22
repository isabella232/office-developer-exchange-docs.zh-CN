---
title: 创建 Exchange 命令行管理程序工具
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 46e4812f-37a8-449f-bd37-bc4a94605db9
description: 查找开始创建针对 Exchange 的 Exchange 命令行管理工具的信息。
ms.openlocfilehash: e8414460007f333e50c9d596bf977792977b1e4e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753016"
---
# <a name="create-exchange-management-shell-tools"></a><span data-ttu-id="7ca38-103">创建 Exchange 命令行管理程序工具</span><span class="sxs-lookup"><span data-stu-id="7ca38-103">Create Exchange Management Shell tools</span></span>

<span data-ttu-id="7ca38-104">查找开始创建针对 Exchange 的 Exchange 命令行管理工具的信息。</span><span class="sxs-lookup"><span data-stu-id="7ca38-104">Find information to get started creating Exchange Management Shell tools for Exchange.</span></span>

<span data-ttu-id="7ca38-105">**适用于：** Exchange Online |Exchange Server 2013 |Office 365</span><span class="sxs-lookup"><span data-stu-id="7ca38-105">**Applies to:** Exchange Online | Exchange Server 2013 | Office 365</span></span>
  
<span data-ttu-id="7ca38-106">Exchange 命令行管理程序提供了一组丰富的命令，基于 Windows PowerShell 平台，用于管理 Exchange Online、 Exchange Online 作为 Office 365 的一部分或 Exchange 的内部部署版本开头 Exchange 2013。</span><span class="sxs-lookup"><span data-stu-id="7ca38-106">The Exchange Management Shell provides a rich set of commands, based on the Windows PowerShell platform, for managing Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange 2013.</span></span> <span data-ttu-id="7ca38-107">您可以使用 Exchange 命令行管理程序命令以直接执行命令，或使用命令脚本自动执行服务器的管理。</span><span class="sxs-lookup"><span data-stu-id="7ca38-107">You can use Exchange Management Shell commands to automate the administration of a server by directly executing the commands, or by using command scripts.</span></span>
  
<span data-ttu-id="7ca38-108">如果您需要使用 Exchange 命令行管理程序命令从中承载的应用程序，如管理运行应用程序管理员的桌面或通过基于 web 的应用程序，您可以调用从 Exchange 命令行管理程序 cmdletVisual Basic 或 C# 应用程序内管理 Exchange 服务器。</span><span class="sxs-lookup"><span data-stu-id="7ca38-108">If you need to use Exchange Management Shell commands from within a hosting application, such as an administrative application that is running on the administrator's desktop or through a web-based application, you can call Exchange Management Shell cmdlets from within your Visual Basic or C# application to manage an Exchange server.</span></span>
  
## <a name="get-started-with-exchange-management-shell-tools"></a><span data-ttu-id="7ca38-109">开始使用 Exchange 命令行管理程序工具</span><span class="sxs-lookup"><span data-stu-id="7ca38-109">Get started with Exchange Management Shell tools</span></span>
<span data-ttu-id="7ca38-110"><a name="SP15GettingStartedTemplate_WhatDoYouNeed"> </a></span><span class="sxs-lookup"><span data-stu-id="7ca38-110"></span></span>

<span data-ttu-id="7ca38-111">如果您熟悉创建 Windows PowerShell 主机应用程序，并且想要查看的示例，演示如何调用的 Exchange 命令行管理程序 cmdlet 从应用程序，或查看您可以使用 Exchange 中创建的应用程序类型的示例管理命令行管理程序 cmdlet，请参阅[获取使用 Exchange 命令行管理程序的邮件用户的列表](how-to-get-a-list-of-mail-users-by-using-the-exchange-management-shell.md)。</span><span class="sxs-lookup"><span data-stu-id="7ca38-111">If you are familiar with creating Windows PowerShell host applications and want to see an example that shows how to call the Exchange Management Shell cmdlets from an application, or to see an example of the types of applications that you can create by using the Exchange Management Shell cmdlets, see [Get a list of mail users by using the Exchange Management Shell](how-to-get-a-list-of-mail-users-by-using-the-exchange-management-shell.md).</span></span>
  
<span data-ttu-id="7ca38-112">Exchange 命令行管理程序 cmdlet 的 Windows PowerShell、 基于任务的命令行管理程序和脚本语言，专门用于系统管理扩展。</span><span class="sxs-lookup"><span data-stu-id="7ca38-112">The Exchange Management Shell cmdlets are extensions to Windows PowerShell, a task-based command-line shell and scripting language that is designed specifically for system administration.</span></span> <span data-ttu-id="7ca38-113">Windows PowerShell 基于.NET Framework，并为 cmdlet、 提供商和主机应用程序开发人员提供面向对象的 API。</span><span class="sxs-lookup"><span data-stu-id="7ca38-113">Windows PowerShell is built on the .NET Framework, and provides an object-oriented API for cmdlet, provider, and host application developers.</span></span> <span data-ttu-id="7ca38-114">若要了解有关 Windows PowerShell 进行编程，请参阅[Windows PowerShell SDK](http://msdn.microsoft.com/en-us/library/dd835506%28VS.85%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="7ca38-114">To learn about Windows PowerShell programming, see the [Windows PowerShell SDK](http://msdn.microsoft.com/en-us/library/dd835506%28VS.85%29.aspx).</span></span>
  
<span data-ttu-id="7ca38-115">Exchange 命令行管理程序 cmdlet 接受并返回对象。</span><span class="sxs-lookup"><span data-stu-id="7ca38-115">The Exchange Management Shell cmdlets accept and return objects.</span></span> <span data-ttu-id="7ca38-116">Exchange 管理命令行管理程序 cmdlet 和其输入和输出的类型的列表，请参阅[Exchange Management Shell cmdlet 输入和输出类型](exchange-management-shell-cmdlet-input-and-output-types.md)。</span><span class="sxs-lookup"><span data-stu-id="7ca38-116">For a list of Exchange management shell cmdlets and their input and output types, see [Exchange Management Shell cmdlet input and output types](exchange-management-shell-cmdlet-input-and-output-types.md).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="7ca38-117">本节内容</span><span class="sxs-lookup"><span data-stu-id="7ca38-117">In this section</span></span>

- [<span data-ttu-id="7ca38-118">新增和经过更新的 Exchange 命令行管理程序 cmdlet</span><span class="sxs-lookup"><span data-stu-id="7ca38-118">New and updated Exchange Management Shell cmdlets</span></span>](new-and-updated-exchange-management-shell-cmdlets.md)  
- [<span data-ttu-id="7ca38-119">Exchange 命令行管理程序 cmdlet 输入和输出类型</span><span class="sxs-lookup"><span data-stu-id="7ca38-119">Exchange Management Shell cmdlet input and output types</span></span>](exchange-management-shell-cmdlet-input-and-output-types.md)
- [<span data-ttu-id="7ca38-120">使用 Exchange 命令行管理程序中获取邮件用户的列表</span><span class="sxs-lookup"><span data-stu-id="7ca38-120">Get a list of mail users by using the Exchange Management Shell</span></span>](how-to-get-a-list-of-mail-users-by-using-the-exchange-management-shell.md)
- [<span data-ttu-id="7ca38-121">使用 Exchange 命令行管理程序 cmdlet 响应</span><span class="sxs-lookup"><span data-stu-id="7ca38-121">Use the Exchange Management Shell cmdlet response</span></span>](how-to-use-the-exchange-management-shell-cmdlet-response.md)


## <a name="see-also"></a><span data-ttu-id="7ca38-122">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7ca38-122">See also</span></span>

- [<span data-ttu-id="7ca38-123">Exchange 命令行管理程序命名空间</span><span class="sxs-lookup"><span data-stu-id="7ca38-123">Exchange Management Shell namespaces</span></span>](exchange-management-shell-namespaces.md)  
- [<span data-ttu-id="7ca38-124">Exchange Server PowerShell （Exchange 命令行管理程序）</span><span class="sxs-lookup"><span data-stu-id="7ca38-124">Exchange Server PowerShell (Exchange Management Shell)</span></span>](https://docs.microsoft.com/en-us/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)  
- [<span data-ttu-id="7ca38-125">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="7ca38-125">Windows PowerShell</span></span>](http://msdn.microsoft.com/en-us/library/dd835506%28v=vs.85%29.aspx)
    

