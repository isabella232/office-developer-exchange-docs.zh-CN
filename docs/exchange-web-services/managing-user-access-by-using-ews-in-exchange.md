---
title: 使用 Exchange 中的 EWS 管理用户访问
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 48f0170c-8786-405f-86cb-568b7314a425
description: 了解用于管理用户帐户对 Exchange 服务器的访问权限的选项。
ms.openlocfilehash: 476292d4db206f22cd84134ce2b46957e9fe85fc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456240"
---
# <a name="managing-user-access-by-using-ews-in-exchange"></a><span data-ttu-id="32530-103">使用 Exchange 中的 EWS 管理用户访问</span><span class="sxs-lookup"><span data-stu-id="32530-103">Managing user access by using EWS in Exchange</span></span>

<span data-ttu-id="32530-104">了解用于管理用户帐户对 Exchange 服务器的访问权限的选项。</span><span class="sxs-lookup"><span data-stu-id="32530-104">Find out what your options are for managing user account access to your Exchange server.</span></span>
  
<span data-ttu-id="32530-105">Exchange Web 服务（EWS）和 EWS 托管 API 提供有限数量的操作，可用于管理 Exchange Online 上的帐户、Exchange Online 作为 Office 365 的一部分或从 Exchange 2013 开始的 Exchange 版本。</span><span class="sxs-lookup"><span data-stu-id="32530-105">Exchange Web Services (EWS) and the EWS managed API provide a limited number of operations that you can use to manage accounts on Exchange Online, Exchange Online as part of Office 365, or a version of Exchange starting with Exchange 2013.</span></span> <span data-ttu-id="32530-106">您可以使用下图中所示的操作来管理委派和为其他帐户设置文件夹访问权限。</span><span class="sxs-lookup"><span data-stu-id="32530-106">You can use the operations shown in the following figure to manage delegates and to set folder access permissions for other accounts.</span></span> 
  
<span data-ttu-id="32530-107">**用于委派和文件夹访问的 EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="32530-107">**EWS operations for delegate and folder access**</span></span>

![EWS 用户管理选项。](media/Exchange_ManagingUserAccess_1.png)
  
<span data-ttu-id="32530-109">如果您的应用程序需要对 Exchange 服务器上的帐户进行更多控制，则可以使用 Exchange 命令行管理程序 cmdlet 来管理帐户。</span><span class="sxs-lookup"><span data-stu-id="32530-109">If your application needs additional control over the accounts on an Exchange server, you can use Exchange Management Shell cmdlets to manage the accounts.</span></span> <span data-ttu-id="32530-110">您可以通过执行以下操作之一来调用 Exchange 命令行管理程序 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="32530-110">You can call the Exchange Management Shell cmdlets by doing one of the following:</span></span>
  
- <span data-ttu-id="32530-111">使用 c # 或 Visual Basic 编写调用 Exchange 命令行管理程序 cmdlet 的应用程序。</span><span class="sxs-lookup"><span data-stu-id="32530-111">Writing an application using C# or Visual Basic that calls the Exchange Management Shell cmdlets.</span></span> <span data-ttu-id="32530-112">您可以查看[Exchange 命令行管理程序 API 文档](../management/exchange-management-shell.md)中的示例代码，以了解如何调用 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="32530-112">You can look at the sample code in the [Exchange Management Shell API documentation](../management/exchange-management-shell.md) to learn how to call a cmdlet.</span></span> 
    
- <span data-ttu-id="32530-113">使用 Windows PowerShell 和 Windows PowerShell 脚本调用 Exchange 命令行管理程序 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="32530-113">Using Windows PowerShell and Windows PowerShell scripts to call Exchange Management Shell cmdlets.</span></span> <span data-ttu-id="32530-114">您可以找到[Exchange Server PowerShell （Exchange 命令行管理程序）](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)的完整列表，以及演示如何使用它们的示例。</span><span class="sxs-lookup"><span data-stu-id="32530-114">You can find a complete list of the [Exchange Server PowerShell (Exchange Management Shell)](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps), along with examples that show how to use them.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="32530-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="32530-115">See also</span></span>

- [<span data-ttu-id="32530-116">设置 EWS 应用程序</span><span class="sxs-lookup"><span data-stu-id="32530-116">Setting up your EWS application</span></span>](setting-up-your-ews-application.md)   
- [<span data-ttu-id="32530-117">Exchange 2013 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="32530-117">Exchange 2013 Cmdlets</span></span>](https://docs.microsoft.com/powershell/exchange/?view=exchange-ps)  
    

