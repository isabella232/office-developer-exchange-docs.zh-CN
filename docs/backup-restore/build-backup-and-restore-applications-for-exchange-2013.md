---
title: 构建备份和还原 Exchange 2013 的应用程序
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e5e952a5-add1-417c-a3c2-230f4dc99b00
description: 查找有关组件和 Exchange 2013 的备份和还原应用程序体系结构以及创建的备份的系统要求的信息和还原应用程序。
ms.openlocfilehash: e85a5364c40c472c9e1ea9d1d3b4e89329b1676f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752696"
---
# <a name="build-backup-and-restore-applications-for-exchange-2013"></a><span data-ttu-id="b3c9c-103">构建备份和还原 Exchange 2013 的应用程序</span><span class="sxs-lookup"><span data-stu-id="b3c9c-103">Build backup and restore applications for Exchange 2013</span></span>

<span data-ttu-id="b3c9c-104">查找有关组件和 Exchange 2013 的备份和还原应用程序体系结构以及创建的备份的系统要求的信息和还原应用程序。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-104">Find information about the components and architecture of backup and restore applications for Exchange 2013, and the system requirements for creating a backup and restore application.</span></span>
  
<span data-ttu-id="b3c9c-105">**适用于：** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="b3c9c-105">**Applies to:** Exchange Server 2013</span></span> 
  
<span data-ttu-id="b3c9c-106">您可以使用[卷影复制服务 (VSS)](http://msdn.microsoft.com/en-us/library/bb968832%28VS.85%29.aspx)版本的 Windows Server 开头 Windows Server 2008 中创建的备份和还原 Exchange Server 2013 数据应用程序。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-106">You can use the [Volume Shadow Copy Service (VSS)](http://msdn.microsoft.com/en-us/library/bb968832%28VS.85%29.aspx) in versions of Windows Server starting with Windows Server 2008 to create applications that back up and restore Exchange Server 2013 data.</span></span> <span data-ttu-id="b3c9c-107">VSS 提供一个基础结构，使您能够创建和管理跨第三方存储管理系统、 业务应用程序和硬件的卷影副本。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-107">VSS provides an infrastructure that enables you to create and manage shadow copies across third-party storage management systems, business applications, and hardware.</span></span> <span data-ttu-id="b3c9c-108">您可以创建基于 VSS 基础结构使用卷影副本备份和还原一个或多个 Exchange 2013 数据库的解决方案。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-108">You can create solutions based on the VSS infrastructure that use shadow copies to back up and restore one or more Exchange 2013 databases.</span></span> 
  
## <a name="backup-and-restore-application-prerequisites"></a><span data-ttu-id="b3c9c-109">备份和还原应用程序的先决条件</span><span class="sxs-lookup"><span data-stu-id="b3c9c-109">Backup and restore application prerequisites</span></span>
<span data-ttu-id="b3c9c-110"><a name="bk_systemrequirements"> </a></span><span class="sxs-lookup"><span data-stu-id="b3c9c-110"></span></span>

<span data-ttu-id="b3c9c-111">使您的自定义备份和还原应用程序和 VSS 备份和还原 Exchange 2013 数据库，您的环境必须包括：</span><span class="sxs-lookup"><span data-stu-id="b3c9c-111">In order for your custom backup and restore application and VSS to back up and restore Exchange 2013 databases, your environment must include the following:</span></span>
  
- <span data-ttu-id="b3c9c-112">开始使用 Windows Server 2008 的 Windows Server 的版本</span><span class="sxs-lookup"><span data-stu-id="b3c9c-112">A version of Windows Server starting with Windows Server 2008</span></span> 
    
- <span data-ttu-id="b3c9c-113">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="b3c9c-113">Exchange 2013</span></span>
    
<span data-ttu-id="b3c9c-114">此外，如果您要创建的备份和还原应用程序，您应了解的开发环境的以下限制：</span><span class="sxs-lookup"><span data-stu-id="b3c9c-114">In addition, if you are creating a backup and restore application, you should be aware of the following restrictions on the development environment:</span></span>
  
- <span data-ttu-id="b3c9c-115">VSS 是可通过 COM 互操作程序集的.NET Framework 托管代码从非托管的 COM API。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-115">VSS is an unmanaged COM API that can be accessed from .NET Framework managed code via a COM Interop Assembly.</span></span>
    
- <span data-ttu-id="b3c9c-116">Exchange 命令行管理程序的托管的应用程序访问通过.NET Framework 托管代码。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-116">The Exchange Management Shell is a managed application that is accessed via .NET Framework managed code.</span></span>
    
- <span data-ttu-id="b3c9c-117">与 Exchange 2013 提供 CHKSGFILES API 为本机代码 64-bit DLL。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-117">The CHKSGFILES API that is supplied with Exchange 2013 is a native-code 64-bit DLL.</span></span> <span data-ttu-id="b3c9c-118">不支持与 Exchange 2013 数据库的 Exchange 2007 32年位 CHKSGFILES dll 的使用。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-118">Use of the Exchange 2007 32-bit CHKSGFILES DLL with Exchange 2013 databases is not supported.</span></span>
    
## <a name="backup-and-restore-application-overview"></a><span data-ttu-id="b3c9c-119">备份和还原应用程序概述</span><span class="sxs-lookup"><span data-stu-id="b3c9c-119">Backup and restore application overview</span></span>
<span data-ttu-id="b3c9c-120"><a name="bk_components"> </a></span><span class="sxs-lookup"><span data-stu-id="b3c9c-120"></span></span>

<span data-ttu-id="b3c9c-121">VSS 协调以下组件之间的通信：</span><span class="sxs-lookup"><span data-stu-id="b3c9c-121">VSS coordinates communication between the following components:</span></span> 
  
- <span data-ttu-id="b3c9c-122">VSS 请求者，即备份应用程序</span><span class="sxs-lookup"><span data-stu-id="b3c9c-122">The VSS requester, which is your backup application</span></span>
    
- <span data-ttu-id="b3c9c-123">VSS 编写器</span><span class="sxs-lookup"><span data-stu-id="b3c9c-123">The VSS writer</span></span>
    
- <span data-ttu-id="b3c9c-124">VSS 提供程序，即创建卷影副本的系统、 软件或硬件组件</span><span class="sxs-lookup"><span data-stu-id="b3c9c-124">The VSS provider, which is the system, software, or hardware components that create the shadow copies</span></span>
    
<span data-ttu-id="b3c9c-125">若要使用 VSS 备份 Exchange 2013 数据，备份应用程序必须了解 Exchange 2013 VSS 申请者。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-125">To use VSS to back up Exchange 2013 data, your backup application must be an Exchange 2013-aware VSS requester.</span></span> <span data-ttu-id="b3c9c-126">Exchange 2013 包括 VSS 编写器，Microsoft Exchange Writer，调用的 Windows 服务器备份程序;但是，Exchange 书写器仅备份整个卷。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-126">Exchange 2013 includes a VSS writer, called the Microsoft Exchange Writer, for the Windows Server backup program; however, the Exchange writer only backs up whole volumes.</span></span> <span data-ttu-id="b3c9c-127">它不会备份单个 Exchange 2013 的数据库。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-127">It does not back up individual Exchange 2013 databases.</span></span> <span data-ttu-id="b3c9c-128">如果您需要更大的灵活性，您可以使用的第三方备份应用程序具有 Exchange 感知 VSS 编写器可以使用 Exchange 的各个数据库，也可以创建自定义的 VSS 请求。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-128">If you need more flexibility, you can use a third-party backup application that has an Exchange-aware VSS writer that can work with individual Exchange databases, or you can create a custom VSS requester.</span></span>
  
<span data-ttu-id="b3c9c-129">您的应用程序调用 VSS 启动备份之前，它必须获取有关备份 Exchange 2013 系统的存储配置信息。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-129">Before your application calls VSS to initiate a backup, it must obtain information about the storage configuration for the Exchange 2013 system that it is backing up.</span></span> <span data-ttu-id="b3c9c-130">该信息存储在 Active Directory 域服务 (AD DS) 中。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-130">That information is stored in Active Directory Domain Services (AD DS).</span></span> <span data-ttu-id="b3c9c-131">备份应用程序可以通过使用 Exchange 命令行管理程序命令来获取 Exchange 存储配置数据。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-131">Your backup application can get Exchange storage configuration data by using Exchange Management Shell commands.</span></span> <span data-ttu-id="b3c9c-132">有关详细信息，请参阅[Exchange Server PowerShell (Exchange Management Shell)](https://docs.microsoft.com/en-us/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-132">For more information, see [Exchange Server PowerShell (Exchange Management Shell)](https://docs.microsoft.com/en-us/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps).</span></span> 
  
<span data-ttu-id="b3c9c-133">Exchange 2013 备份应用程序调用 VSS COM Api 创建完整，副本、 差异备份和增量备份的 Exchange 数据库;他们不直接与 VSS 编写器交互。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-133">Exchange 2013 backup applications call the VSS COM APIs to create full, copy, differential and incremental backups of Exchange databases; they do not interact directly with the VSS writer.</span></span> <span data-ttu-id="b3c9c-134">Exchange 中的数据库可用性组 (DAG) 功能还允许您的应用程序创建完全一致的备份，即使初始完整备份和增量备份更高版本来自不同 DAG 中的服务器。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-134">The Database Availability Group (DAG) functionality in Exchange also enables your application to create a fully consistent backup, even if the initial full backup and later incremental backups come from different servers in the DAG.</span></span> <span data-ttu-id="b3c9c-135">VSS 创建 Exchange 数据的副本后，您备份应用程序存储到预期媒体。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-135">After VSS creates the copy of the Exchange data, your backup application stores the data onto the intended media.</span></span>
  
<span data-ttu-id="b3c9c-136">若要还原的 Exchange 2013 数据库，您还原应用程序检索的数据库和日志文件从备份媒体，，并将其存储在活动的磁盘存储的 Exchange server 上。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-136">To restore an Exchange 2013 database, your restore application retrieves the database and log files from the backup media, and stores them on the active disk storage of an Exchange server.</span></span> <span data-ttu-id="b3c9c-137">单个数据库不与特定 Exchange 服务器相关联。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-137">Individual databases are not associated with a particular Exchange server.</span></span> 
  
<span data-ttu-id="b3c9c-138">备份和还原应用程序必须指定多个特定于 Exchange 2013 的参数正确控制和管理针对 Exchange 2013 数据库运行 VSS 的操作。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-138">Backup and restore applications must specify a number of Exchange 2013-specific parameters to correctly control and manage operations run by VSS against Exchange 2013 databases.</span></span> <span data-ttu-id="b3c9c-139">例如，由于 Exchange 2013 支持同时处于活动状态的最多 100 个数据库，备份应用程序必须正确指定并处理数据库文件、 事务日志文件和检查点文件数据库组件。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-139">For example, because Exchange 2013 supports up to 100 simultaneously active databases, the backup application must correctly specify and process the database file, transaction log files, and checkpoint file database components.</span></span>
  
<span data-ttu-id="b3c9c-140">若要重新构造自上次完整备份以来已更改的数据库，您还原应用程序需要从不同的备份的数据库和日志文件。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-140">To reconstruct a database that had changes since the last full back, your restore application requires database and log files from different backups.</span></span> <span data-ttu-id="b3c9c-141">例如，它可能需要每周的完整备份和一个或多个每日的增量备份。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-141">For example, it might require a weekly full backup and one or more daily incremental backups.</span></span> <span data-ttu-id="b3c9c-142">在 Exchange 2013 使用 Dag 的系统，还原应用程序可以重建数据库在同一个 DAG 中的不同服务器上使用从不同的数据库副本的备份。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-142">In Exchange 2013 systems that use DAGs, your restore application can rebuild a database by using backups from different database copies on different servers in the same DAG.</span></span> <span data-ttu-id="b3c9c-143">但是，从备份还原 DAG 数据库支持的唯一方法是数据库的使用相同的数据还原的所有活动和被动副本。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-143">However, the only supported way to restore a DAG database from backup is to restore all active and passive copies of the database by using the same data.</span></span>
  
<span data-ttu-id="b3c9c-144">所有数据后，您还原应用程序发出信号 Exchange 检查数据库和日志文件的完整性。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-144">After all the data is in place, your restore application signals Exchange to check the integrity of the database and log files.</span></span> <span data-ttu-id="b3c9c-145">如果已正确还原的数据库和日志文件，Exchange 服务器可然后播放数据库日志文件，以使最新数据库并将其装载。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-145">If the database and log files have been restored correctly, the Exchange server can then replay the database log files to bring the database up to date and mount it.</span></span> <span data-ttu-id="b3c9c-146">如果具有已将数据库恢复到已有的数据库装入主动副本的服务器，数据库将被视为恢复数据库。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-146">If the database has been recovered to a server that already has an active copy of the database mounted, the database is treated as a recover database.</span></span> <span data-ttu-id="b3c9c-147">如果已进行了数据库恢复到另一台服务器，也可以独立装入的数据库，或该副本然后可被添加到 DAG。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-147">If the database has been recovered onto a different server, the database can either be independently mounted, or that replica can then be added into the DAG.</span></span>
  
## <a name="backup-and-restore-system-architecture"></a><span data-ttu-id="b3c9c-148">备份和还原系统体系结构</span><span class="sxs-lookup"><span data-stu-id="b3c9c-148">Backup and restore system architecture</span></span>
<span data-ttu-id="b3c9c-149"><a name="bk_ExchangeVSS"> </a></span><span class="sxs-lookup"><span data-stu-id="b3c9c-149"></span></span>

<span data-ttu-id="b3c9c-150">与 Windows Server 文件系统和通过第三方 （或自定义） 提供商的大容量存储设备驱动程序，VSS 进行通信。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-150">VSS communicates with the Windows Server file system and with the mass storage device driver through a third-party (or custom) provider.</span></span> <span data-ttu-id="b3c9c-151">硬件提供商决定将在其中创建卷影副本。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-151">The hardware provider determines where the shadow copy will be created.</span></span> <span data-ttu-id="b3c9c-152">VSS 抽象化特定于硬件的卷影副本，以便备份和还原应用程序可以访问卷影副本不包含有关硬件的实现详细信息的信息。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-152">VSS abstracts the hardware-specific shadow copy so that your backup and restore application can access the shadow copy without information about the hardware implementation details.</span></span> <span data-ttu-id="b3c9c-153">下图显示了与 Exchange 2013 和 Windows Server 备份和还原应用程序的交互方式。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-153">The following figure shows how your backup and restore application interacts with Exchange 2013 and Windows Server.</span></span>
  
<span data-ttu-id="b3c9c-154">**图 1。备份和还原系统体系结构**</span><span class="sxs-lookup"><span data-stu-id="b3c9c-154">**Figure 1. Backup and restore system architecture**</span></span>

![此图显示备份和恢复应用程序如何进行交互。在 Exchange、Windows Server 和客户端应用程序之间存在双向通信。Windows Server 还会与大容量存储设备或备份媒体交互。](media/VSS_architecture_E2k7.gif)
  
<span data-ttu-id="b3c9c-158">备份和还原应用程序作为 VSS 请求者。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-158">The backup and restore application functions as the VSS requester.</span></span> <span data-ttu-id="b3c9c-159">请求者与 VSS 获取有关 Exchange 2013，若要启动的卷影副本创建和访问用于备份数据的信息进行通信。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-159">The requester communicates with VSS to obtain information about Exchange 2013, to initiate the creation of shadow copies, and to gain access to the data for backup.</span></span> 
  
<span data-ttu-id="b3c9c-160">在 Exchange 存储是 Exchange 2013 的一个组件，通过 Windows Server 文件系统访问 Exchange 2013 数据库。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-160">The Exchange store is a component of Exchange 2013 and accesses Exchange 2013 databases through the Windows Server file system.</span></span> <span data-ttu-id="b3c9c-161">在文件系统中，每个 Exchange 服务器可同时装入达 100 个数据库与其相应的数据库 (.edb) 文件和事务日志文件，检查点文件。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-161">Within the file system, each Exchange server can simultaneously mount up to 100 databases with their accompanying database (.edb) files, transaction log files, and a checkpoint file.</span></span>
  
<span data-ttu-id="b3c9c-162">若要支持 VSS，Exchange 2013 包括 Exchange 存储中内置的 Exchange 编写器。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-162">To support VSS, Exchange 2013 includes an Exchange writer that is built in to the Exchange store.</span></span> <span data-ttu-id="b3c9c-163">与 Exchange 存储 （代表申请者操作系统） Exchange 书写器协调冻结和 backing up 之前, 卸除数据库，然后解除冻结和装入数据库备份后已完成。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-163">The Exchange writer coordinates with the Exchange store (operating on behalf of the requester) to freeze and dismount the database before backing it up, and then to unfreeze and mount the database after the backup is complete.</span></span> <span data-ttu-id="b3c9c-164">在还原期间，您的备份和还原应用程序指示 Exchange 编写器来协调与 Exchange 存储卸除数据库、 替换数据库文件、 装入数据库，并然后重播事务日志 （根据需要）。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-164">During a restore, your backup and restore application instructs the Exchange writer to coordinate with the Exchange store to dismount the database, replace the database files, mount the database, and then replay the transaction logs (as needed).</span></span>
  
<span data-ttu-id="b3c9c-165">在还原期间，请求者还可与 VSS 系统准备还原，通信，然后将数据重新拖到大容量存储设备。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-165">During a restore, the requester also communicates with VSS to prepare the system for the restore, and then to put the data back onto the mass storage device.</span></span> <span data-ttu-id="b3c9c-166">备份和还原应用程序也是负责处理要读取和写入数据的备份存储媒体、 是否磁带存档、 存储区域网络或其他备份媒体的 Windows 服务器。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-166">Your backup and restore application is also responsible for working with Windows Server to read data from and write data to the backup storage media, whether a tape archive, a storage area network, or other backup medium.</span></span>
  
<span data-ttu-id="b3c9c-167">还原的数据库可装入，作为常规、 活动数据库，或 Exchange 2013 恢复数据库。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-167">The restored database can be mounted either as a regular, active database, or as the Exchange 2013 recovery database.</span></span> <span data-ttu-id="b3c9c-168">可以将只能有一个装入的数据库指定为每个 Exchange 服务器上的恢复数据库。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-168">Only one mounted database can be designated as a recovery database on each Exchange server.</span></span>
  
<span data-ttu-id="b3c9c-169">信息才能成功完成备份和还原操作之间 Exchange 2013 VSS 和备份和还原应用程序将作为 Exchange 编写器元数据的一部分进行传输。</span><span class="sxs-lookup"><span data-stu-id="b3c9c-169">Information required to successfully complete backup and restore operations among Exchange 2013, VSS, and your backup and restore application is transferred as part of the Exchange writer metadata.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="b3c9c-170">本节内容</span><span class="sxs-lookup"><span data-stu-id="b3c9c-170">In this section</span></span>
<span data-ttu-id="b3c9c-171"><a name="bk_inthissection"> </a></span><span class="sxs-lookup"><span data-stu-id="b3c9c-171"></span></span>

- [<span data-ttu-id="b3c9c-172">Exchange 2013 的备份操作的类型</span><span class="sxs-lookup"><span data-stu-id="b3c9c-172">Types of backup operations for Exchange 2013</span></span>](types-of-backup-operations-for-exchange-2013.md)
    
- [<span data-ttu-id="b3c9c-173">还原 Exchange 2013 数据库</span><span class="sxs-lookup"><span data-stu-id="b3c9c-173">Restoring Exchange 2013 databases</span></span>](restoring-exchange-2013-databases.md)
    
- [<span data-ttu-id="b3c9c-174">使用 CHKSGFILES API 在 Exchange 2013 中验证备份完整性</span><span class="sxs-lookup"><span data-stu-id="b3c9c-174">Validate backup integrity by using the CHKSGFILES API in Exchange 2013</span></span>](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md)
    
- [<span data-ttu-id="b3c9c-175">通过使用 Eseutil 工具在 Exchange 2013 中验证备份完整性</span><span class="sxs-lookup"><span data-stu-id="b3c9c-175">Validate backup integrity by using the Eseutil tool in Exchange 2013</span></span>](how-to-validate-backup-integrity-by-using-the-eseutil-tool-in-exchange-2013.md)
    
## <a name="see-also"></a><span data-ttu-id="b3c9c-176">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b3c9c-176">See also</span></span>

- [<span data-ttu-id="b3c9c-177">备份和还原 exchange</span><span class="sxs-lookup"><span data-stu-id="b3c9c-177">Backup and restore for Exchange</span></span>](backup-and-restore-for-exchange-2013.md) 
- [<span data-ttu-id="b3c9c-178">CChkSGFiles 类参考 （英文）</span><span class="sxs-lookup"><span data-stu-id="b3c9c-178">CChkSGFiles class reference</span></span>](cchksgfiles-class-reference.md) 
- [<span data-ttu-id="b3c9c-179">卷影复制服务</span><span class="sxs-lookup"><span data-stu-id="b3c9c-179">Volume Shadow Copy Service</span></span>](http://msdn.microsoft.com/en-us/library/bb968832%28VS.85%29.aspx) 
- [<span data-ttu-id="b3c9c-180">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="b3c9c-180">Windows PowerShell</span></span>](http://msdn.microsoft.com/en-us/library/dd835506%28v=vs.85%29.aspx)
    

