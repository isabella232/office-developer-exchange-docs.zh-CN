---
title: Exchange 2013 的备份操作类型
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 70510902-9583-4177-be3d-afbf757a1ec0
description: 您可以执行 Exchange 2013 有关备份的不同类型的查找信息存储数据库，包括完全、 复制、 增量和差异备份。
ms.openlocfilehash: 588bc0ffe896f286258006f7f123cf09d28b218c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752732"
---
# <a name="types-of-backup-operations-for-exchange-2013"></a><span data-ttu-id="13743-103">Exchange 2013 的备份操作类型</span><span class="sxs-lookup"><span data-stu-id="13743-103">Types of backup operations for Exchange 2013</span></span>

<span data-ttu-id="13743-104">您可以执行 Exchange 2013 有关备份的不同类型的查找信息存储数据库，包括完全、 复制、 增量和差异备份。</span><span class="sxs-lookup"><span data-stu-id="13743-104">Find information about the different types of backups you can perform on your Exchange 2013 store databases, including full, copy, incremental, and differential backups.</span></span>
  
<span data-ttu-id="13743-105">**适用于：** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="13743-105">**Applies to:** Exchange Server 2013</span></span> 
  
<span data-ttu-id="13743-106">本文提供了有关备份的不同类型的信息可以在 Exchange Server 2013 的数据库上执行以及这些备份如何影响数据库文件。</span><span class="sxs-lookup"><span data-stu-id="13743-106">This article provides information about the different types of backups you can perform on Exchange Server 2013 databases, and how those backups affect the database files.</span></span> 
  
<span data-ttu-id="13743-107">使用卷影复制服务 (VSS) 和 Exchange 编写器的备份和还原应用程序可以执行下表中列出的备份类型。</span><span class="sxs-lookup"><span data-stu-id="13743-107">Backup and restore applications that use the Volume Shadow Copy Service (VSS) and the Exchange writer can perform the types of backups listed in the following table.</span></span>
  
<span data-ttu-id="13743-108">**表 1。备份操作的类型**</span><span class="sxs-lookup"><span data-stu-id="13743-108">**Table 1. Types of backup operations**</span></span>

|<span data-ttu-id="13743-109">**备份类型**</span><span class="sxs-lookup"><span data-stu-id="13743-109">**Backup type**</span></span>|<span data-ttu-id="13743-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="13743-110">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="13743-111">完整备份</span><span class="sxs-lookup"><span data-stu-id="13743-111">Full backups</span></span>](types-of-backup-operations-for-exchange-2013.md#bk_FullBackups) <br/> |<span data-ttu-id="13743-112">备份数据库 (\*.edb)，事务日志 (\*.log)，检查点文件 (\*.chk)，，然后截断特定数据库的事务日志。</span><span class="sxs-lookup"><span data-stu-id="13743-112">Backs up the databases (\*.edb), transaction logs (\*.log), checkpoint files (\*.chk), and then truncates the transaction logs for a specific database.</span></span>  <br/> |
|[<span data-ttu-id="13743-113">将备份复制</span><span class="sxs-lookup"><span data-stu-id="13743-113">Copy backups</span></span>](types-of-backup-operations-for-exchange-2013.md#bk_CopyBackups) <br/> |<span data-ttu-id="13743-p101">备份数据库、事务日志和检查点文件。副本备份不会截断数据库的事务日志。</span><span class="sxs-lookup"><span data-stu-id="13743-p101">Backs up the database, transaction logs, and checkpoint files. Copy backups do not truncate the transaction logs for the database.</span></span>  <br/> |
|[<span data-ttu-id="13743-116">增量备份</span><span class="sxs-lookup"><span data-stu-id="13743-116">Incremental backups</span></span>](types-of-backup-operations-for-exchange-2013.md#bk_IncrementalBackups) <br/> |<span data-ttu-id="13743-117">备份事务日志，记录自上次完整备份或增量备份以来的所有更改，然后再截断事务日志。</span><span class="sxs-lookup"><span data-stu-id="13743-117">Backs up the transaction logs to record changes since the last full or incremental backup, and then truncates the transaction logs.</span></span>  <br/> |
|[<span data-ttu-id="13743-118">差异备份</span><span class="sxs-lookup"><span data-stu-id="13743-118">Differential backups</span></span>](types-of-backup-operations-for-exchange-2013.md#bk_DifferentialBackups) <br/> |<span data-ttu-id="13743-119">备份事务日志，记录自上次完整备份或增量备份以来的所有更改，并且不截断事务日志。</span><span class="sxs-lookup"><span data-stu-id="13743-119">Backs up the transaction logs to record changes since the last full or incremental backup, and does not truncate the transaction logs.</span></span>  <br/> |
   
<span data-ttu-id="13743-120">组件或数据库文件，由 Exchange 编写器定义表示数据库文件和 Exchange 2013 数据库中的事务日志。</span><span class="sxs-lookup"><span data-stu-id="13743-120">The components, or database files, defined by the Exchange writer represent the database files and transaction logs within Exchange 2013 databases.</span></span> <span data-ttu-id="13743-121">这样，备份和还原应用程序备份操作过程中显示的 Exchange 2013 数据库中的组件名称。</span><span class="sxs-lookup"><span data-stu-id="13743-121">This allows your backup and restore application to display the names of the components within an Exchange 2013 database during backup operations.</span></span> <span data-ttu-id="13743-122">备份应用程序不能但是; 备份单个数据库组件它可以只备份整个数据库。</span><span class="sxs-lookup"><span data-stu-id="13743-122">Your backup application cannot back up individual database components, however; it can only back up whole databases.</span></span> 
  
<span data-ttu-id="13743-p103">Exchange 编写器标准化数据库组件的逻辑路径，该路径在 Exchange 编写器元数据中指定。Exchange 编写器会根据需要向备份和还原应用程序返回逻辑路径。</span><span class="sxs-lookup"><span data-stu-id="13743-p103">The Exchange writer standardizes the database component logical paths, which are specified in the Exchange writer metadata. The Exchange writer returns the logical paths to your backup and restore application as needed.</span></span>
  
<span data-ttu-id="13743-125">Exchange 作者提供了窗体中的逻辑路径：</span><span class="sxs-lookup"><span data-stu-id="13743-125">The Exchange writer provides logical paths in the form:</span></span> 
  
 `logicalPath = "Exchange Server\Microsoft Information Store\<Server name>"`
  
<span data-ttu-id="13743-p104">服务器和数据库组件是文件组的组件，但它们没有任何关联的文件。它们具有指定单个文件的子组件。数据库中仅包含一个名为 Logs 的日志组件。单个数据库组件的组件名称是显示为字符串的数据库的 Guid。</span><span class="sxs-lookup"><span data-stu-id="13743-p104">The server and database components are file group components, but they do not have any associated files. They have subcomponents that specify the individual files. A database contains only one log component, named Logs. The component names of the individual database components are the GUIDs of the databases, shown as strings.</span></span> 
  
<span data-ttu-id="13743-130">Exchange 书写器仅列出了可以在基于 VSS 框架准则，备份的数据库。</span><span class="sxs-lookup"><span data-stu-id="13743-130">The Exchange writer only lists databases that can be backed up, based on VSS framework guidelines.</span></span> <span data-ttu-id="13743-131">为 Exchange 2013 恢复数据库，以及未装入的数据库装入的数据库无法进行备份，并因此中未列出 Exchange 编写器元数据。</span><span class="sxs-lookup"><span data-stu-id="13743-131">Databases that are mounted as the Exchange 2013 recovery database, as well as databases that are not mounted, cannot be backed up, and therefore are not listed in the Exchange writer's metadata.</span></span>
  
<span data-ttu-id="13743-132">下图显示了 Exchange 编写器备份过程。</span><span class="sxs-lookup"><span data-stu-id="13743-132">The following figure shows the Exchange writer backup process.</span></span> 
  
<span data-ttu-id="13743-133">**图 1。备份过程的事件顺序**</span><span class="sxs-lookup"><span data-stu-id="13743-133">**Figure 1. Sequence of events for the backup process**</span></span>

![此图显示备份过程的事件序列。该序列从 Exchange 存储启动开始，然后继续经历 Exchange 编写器、VSS 和客户端应用程序之间的多个步骤。](media/VSS_StoreWriterBackup.gif)
  
## <a name="full-backups"></a><span data-ttu-id="13743-136">完整备份</span><span class="sxs-lookup"><span data-stu-id="13743-136">Full backups</span></span>
<span data-ttu-id="13743-137"><a name="bk_FullBackups"> </a></span><span class="sxs-lookup"><span data-stu-id="13743-137"></span></span>

<span data-ttu-id="13743-138">Exchange 数据库的完整备份包括创建和存储的数据库文件、 事务日志和检查点文件的副本。</span><span class="sxs-lookup"><span data-stu-id="13743-138">A full backup of an Exchange database involves creating and storing a copy of the database file, transaction logs, and checkpoint files.</span></span> <span data-ttu-id="13743-139">Exchange 2013 数据库有一组专用的事务日志文件。</span><span class="sxs-lookup"><span data-stu-id="13743-139">An Exchange 2013 database has one set of dedicated transaction log files.</span></span>
  
<span data-ttu-id="13743-p108">已备份数据库之后，磁盘上的事务日志文件将被截断，以便仅保留发生在备份之后的数据库更改。在此过程中，基于对现已备份的数据库已处于包含多达最新检查点个数的所有更改的状态的假设，Exchange 编写器会删除多达检查点个数的所有日志条目。</span><span class="sxs-lookup"><span data-stu-id="13743-p108">After the database has been backed up, the transaction log files on the disk are truncated so that only database changes that occurred after the backup was made will remain. During this process, the Exchange writer deletes all log entries up to the checkpoint, based on the assumption that the databases have now been backed up in a consistent state that contains all changes up to the most recent checkpoint.</span></span> 
  
<span data-ttu-id="13743-142">如果在备份操作过程中将卸除数据库备份，Exchange 2013 将不会截断事务日志，结果将备份复制操作，不是完整备份操作的等效项。</span><span class="sxs-lookup"><span data-stu-id="13743-142">If the database being backed up is dismounted during the backup operation, Exchange 2013 will not truncate the transaction logs and the result will be the equivalent of a copy backup operation, not a full backup operation.</span></span> 
  
<span data-ttu-id="13743-p109">完整备份完成后，当前备份信息中将更新活动安装的数据库的标头。在已复制的部署中，此信息将被提交到事务日志文件并复制到数据库的其他 DAG 副本。由于该事务日志文件已重播到数据库副本，因此数据库的标头副本将被更新。</span><span class="sxs-lookup"><span data-stu-id="13743-p109">When a full backup is completed, the headers of the active mounted database are updated with the current backup information. In replicated deployments, this information will be committed to a transaction log file and replicated to the other DAG copies of the database. Headers of the database copies are updated as this transaction log file is replayed into the database copy.</span></span>
  
<span data-ttu-id="13743-p110">为了运行增量或差异卷影副本备份，完整的卷影副本备份是必需的。完整备份可以来自任何副本，只要它是卷影副本备份即可。</span><span class="sxs-lookup"><span data-stu-id="13743-p110">A full shadow copy backup is required in order to run incremental or differential shadow copy backups. The full backups can be taken from any copy as long as it is a shadow copy backup.</span></span>
  
<span data-ttu-id="13743-148">在下列方案中使用完整备份：</span><span class="sxs-lookup"><span data-stu-id="13743-148">Full backups are used in the following scenarios:</span></span>
  
- <span data-ttu-id="13743-p111">数据库已损坏或丢失，但在磁盘上的事务日志文件保持不变。在此方案中，可以从完整备份还原受影响的数据库文件，并通过重播仍然在磁盘上的事务日志来进行恢复。</span><span class="sxs-lookup"><span data-stu-id="13743-p111">A database becomes corrupted or is lost, but the transaction log files on disk are intact. In this scenario, the affected database files can be restored from the full backup, and then recovered by replaying the transaction logs that are still on disk.</span></span> 
    
- <span data-ttu-id="13743-p112">事务日志文件和磁盘上的数据库文件都已丢失。在此方案中，在进行完整备份时备份的事务日志文件会与数据库一起还原。</span><span class="sxs-lookup"><span data-stu-id="13743-p112">Transaction log files, as well as the database file on disk, are lost. In this scenario, the transaction log files that were backed up at the time of the full backup are restored together with the database.</span></span>
    
<span data-ttu-id="13743-153">在 Exchange 2013 中可以还原日志而无需还原完整备份集适用的数据库。</span><span class="sxs-lookup"><span data-stu-id="13743-153">In Exchange 2013, logs can be restored without having to restore the applicable database from a full backup set.</span></span> <span data-ttu-id="13743-154">此选项可使可能为以前的完整备份来还原并将其与最新的完整备份滚的事务日志文件结合使用。</span><span class="sxs-lookup"><span data-stu-id="13743-154">This option makes it possible for a previous full backup to be restored and combined with the transaction log files from the most recent full backup to roll forward.</span></span>
  
<span data-ttu-id="13743-155">当的[VSS_BACKUP_TYPE](http://msdn.microsoft.com/zh-cn/library/windows/desktop/aa384679%28v=vs.85%29.aspx)枚举中 VSS 设置为**VSS_BT_FULL** Exchange 编写器执行备份时，备份中包括以下组件：</span><span class="sxs-lookup"><span data-stu-id="13743-155">When the [VSS_BACKUP_TYPE](http://msdn.microsoft.com/zh-cn/library/windows/desktop/aa384679%28v=vs.85%29.aspx) enumeration in VSS is set to **VSS_BT_FULL** when the Exchange writer performs a backup, the following components are included in the backup:</span></span> 
  
- <span data-ttu-id="13743-156">数据库的逻辑路径 Exchange Server\Microsoft 信息存储\\< 服务器名称\>\\< 数据库 GUID\></span><span class="sxs-lookup"><span data-stu-id="13743-156">A database with the logical path Exchange Server\Microsoft Information Store\\<Server Name\>\\<Database GUID\></span></span> 
    
- <span data-ttu-id="13743-157">使用的逻辑路径 Exchange Server\Microsoft 信息存储日志文件\\< 服务器名称\>\\< 数据库 GUID\></span><span class="sxs-lookup"><span data-stu-id="13743-157">A log file with the logical path Exchange Server\Microsoft Information Store\\<Server Name\>\\<Database GUID\></span></span> 
    
## <a name="copy-backups"></a><span data-ttu-id="13743-158">复制备份</span><span class="sxs-lookup"><span data-stu-id="13743-158">Copy backups</span></span>
<span data-ttu-id="13743-159"><a name="bk_CopyBackups"> </a></span><span class="sxs-lookup"><span data-stu-id="13743-159"></span></span>

<span data-ttu-id="13743-p114">Exchange 数据库的副本备份涉及创建和存储与包含在完整备份中相同的元素。但是，与完整备份不同的是，备份结束时磁盘上的事务日志文件不会被截断。复制备份不是为了进行数据恢复。复制备份反而是提供数据图像，该图像可用于测试、问题诊断或为副本设定种子。</span><span class="sxs-lookup"><span data-stu-id="13743-p114">A copy backup of an Exchange database involves creating and storing the same elements that are included in a full backup. However, unlike with a full backup, the transaction log files on disk are not truncated when the backup is complete. Copy backups are not intended for data recovery purposes. Instead, copy backups provide an image of the data for use in testing, problem diagnosis, or for seeding a replica.</span></span>
  
<span data-ttu-id="13743-164">例如，遇到问题 Exchange 存储的 Exchange 2013 管理员可以创建副本备份用于测试环境中而不会影响生产系统。</span><span class="sxs-lookup"><span data-stu-id="13743-164">For example, an Exchange 2013 administrator who is experiencing problems with the Exchange store can make a copy backup for use in a test environment without affecting the production system.</span></span> <span data-ttu-id="13743-165">复制备份不会影响常规备份时间表;但是，副本备份还将 Exchange 存储在备份正在进行中状态，因为它会阻止继续之前完成或已中止副本备份从其他计划的备份。</span><span class="sxs-lookup"><span data-stu-id="13743-165">Copy backups do not affect regular backup schedules; however, because a copy backup also puts the Exchange store in a backup-in-progress state, it blocks other scheduled backups from proceeding until the copy backup is completed or aborted.</span></span> 
  
<span data-ttu-id="13743-166">当的[VSS_BACKUP_TYPE](http://msdn.microsoft.com/zh-cn/library/windows/desktop/aa384679%28v=vs.85%29.aspx)枚举中 VSS 设置为**VSS_BT_COPY**时，副本备份中包含以下组件：</span><span class="sxs-lookup"><span data-stu-id="13743-166">When the [VSS_BACKUP_TYPE](http://msdn.microsoft.com/zh-cn/library/windows/desktop/aa384679%28v=vs.85%29.aspx) enumeration in VSS is set to **VSS_BT_COPY**, the following components are included in a copy backup:</span></span> 
  
- <span data-ttu-id="13743-167">数据库的逻辑路径 Exchange Server\Microsoft 信息存储\\< 服务器名称\>\\< 数据库 GUID\></span><span class="sxs-lookup"><span data-stu-id="13743-167">A database with the logical path Exchange Server\Microsoft Information Store\\<Server Name\>\\<Database GUID\></span></span> 
    
- <span data-ttu-id="13743-168">使用的逻辑路径 Exchange Server\Microsoft 信息存储日志文件组件\\< 服务器名称\>\\< 数据库 GUID\></span><span class="sxs-lookup"><span data-stu-id="13743-168">A log file component with the logical path Exchange Server\Microsoft Information Store\\<Server Name\>\\<Database GUID\></span></span>
    
## <a name="incremental-backups"></a><span data-ttu-id="13743-169">增量备份</span><span class="sxs-lookup"><span data-stu-id="13743-169">Incremental backups</span></span>
<span data-ttu-id="13743-170"><a name="bk_IncrementalBackups"> </a></span><span class="sxs-lookup"><span data-stu-id="13743-170"></span></span>

<span data-ttu-id="13743-171">Exchange 2013 数据库的增量备份将更改保存到发生自上次完整或增量备份的数据库。</span><span class="sxs-lookup"><span data-stu-id="13743-171">An incremental backup of an Exchange 2013 database saves changes to the database that have occurred since the last full or incremental backup.</span></span> <span data-ttu-id="13743-172">在所有数据库文件和日志文件都还原到系统中时，就可恢复到所上次增量备份时的状态。</span><span class="sxs-lookup"><span data-stu-id="13743-172">When all the database files and log files are restored to the system, they can be recovered to the state they were in at the time of the last incremental backup.</span></span> <span data-ttu-id="13743-173">增量备份中存储的数据仅包含事务日志文件到当前时间为止。</span><span class="sxs-lookup"><span data-stu-id="13743-173">The data stored in an incremental backup includes only the transaction log files up to the current time.</span></span> 
  
<span data-ttu-id="13743-p117">备份完成时，Exchange 服务器截断日志文件，并将备份时间标记在数据库标头中。使用增量备份恢复数据库要求至少要还原两个数据集：上次的完整备份，以及自上次完整备份后执行的每个增量备份。使用增量备份的优点是单独的备份会比完整备份小得多且单独的增量备份常常小于差异备份。</span><span class="sxs-lookup"><span data-stu-id="13743-p117">When the backup is complete, the Exchange server truncates the log files and marks the backup time in the database headers. Using an incremental backup to recover a database requires at least two data sets to be restored: the last full backup, and then every incremental backup taken after the last full backup. The advantage to using incremental backups is that the individual backups are much smaller than a full backup and individual incremental backups are frequently smaller than differential backups.</span></span> 
  
<span data-ttu-id="13743-p118">使用增量备份的缺点是，如果在完整备份中间执行许多增量备份，恢复 Exchange 存储可能会涉及恢复许多增量备份。如果没有以前的完整备份去建立增量更改的起始点，Exchange 就不会允许进行增量备份。</span><span class="sxs-lookup"><span data-stu-id="13743-p118">The disadvantage to using incremental backups is that if many incremental backups were made between full backups, recovering the Exchange store may involve recovering many incremental backups. Exchange does not allow an incremental backup to occur when no previous full backup exists to establish the starting point for the incremental changes.</span></span> 
  
<span data-ttu-id="13743-179">完整备份摘自 DAG 复制位置可以跟增量备份的活动的位置，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="13743-179">A full backup taken from a DAG copy location can be followed by an incremental backup from the active location and vice versa.</span></span> <span data-ttu-id="13743-180">限制之一，需要注意的是最后一个备份状态维护活动的数据库的标头中，并向数据库头更改写入到事务日志，复制，并重播一样所有其他事务的复制数据库位置在 DAG 部署中的日志。</span><span class="sxs-lookup"><span data-stu-id="13743-180">One restriction to keep in mind is that the last backup state is maintained in the active database's header, and the changes to the database header are written to transaction logs, replicated, and replayed at the copy database location just like all other transaction logs in DAG deployments.</span></span> <span data-ttu-id="13743-181">备份应用程序备份和还原互操作，因为可以提供的功能以独占方式在特定 DAG 节点上，无论节点是否是主动或被动，运行备份，以及以独占方式从被动节点运行备份或以独占方式从主动节点。</span><span class="sxs-lookup"><span data-stu-id="13743-181">Because backups and restores interoperate, backup applications can provide the functionality to run backups exclusively on a specific DAG node, regardless of whether the node is active or passive, as well as to run backups exclusively from the passive node or exclusively from the active node.</span></span>
  
<span data-ttu-id="13743-182">当的[VSS_BACKUP_TYPE](http://msdn.microsoft.com/zh-cn/library/windows/desktop/aa384679%28v=vs.85%29.aspx)枚举中 VSS 设置为**VSS_BT_INCREMENTAL**时，增量备份中包含以下组件：</span><span class="sxs-lookup"><span data-stu-id="13743-182">When the [VSS_BACKUP_TYPE](http://msdn.microsoft.com/zh-cn/library/windows/desktop/aa384679%28v=vs.85%29.aspx) enumeration in VSS is set to **VSS_BT_INCREMENTAL**, the following components are included in an incremental backup:</span></span> 
  
- <span data-ttu-id="13743-183">数据库的逻辑路径 Exchange Server\Microsoft 信息存储\\< 服务器名称\>\\< 数据库 GUID\></span><span class="sxs-lookup"><span data-stu-id="13743-183">A database with the logical path Exchange Server\Microsoft Information Store\\<Server Name\>\\<Database GUID\></span></span> 
    
- <span data-ttu-id="13743-184">使用的逻辑路径 Exchange Server\Microsoft 信息存储日志文件\\< 服务器名称\>\\< 数据库 GUID\></span><span class="sxs-lookup"><span data-stu-id="13743-184">A log file with the logical path Exchange Server\Microsoft Information Store\\<Server Name\>\\<Database GUID\></span></span>
    
## <a name="differential-backups"></a><span data-ttu-id="13743-185">差异备份</span><span class="sxs-lookup"><span data-stu-id="13743-185">Differential backups</span></span>
<span data-ttu-id="13743-186"><a name="bk_DifferentialBackups"> </a></span><span class="sxs-lookup"><span data-stu-id="13743-186"></span></span>

<span data-ttu-id="13743-187">Exchange 2013 数据库的差异备份将更改保存到发生自上次完整或增量备份的数据库。</span><span class="sxs-lookup"><span data-stu-id="13743-187">A differential backup of an Exchange 2013 database saves changes to the database that have occurred since the last full or incremental backup.</span></span> <span data-ttu-id="13743-188">时由系统还原的数据库文件和日志文件，它们可以恢复到它们在差异备份所处的状态。</span><span class="sxs-lookup"><span data-stu-id="13743-188">When the database files and log files are restored by the system, they can be recovered to the state they were in at the last differential backup.</span></span> 
  
<span data-ttu-id="13743-p121">差异备份中存储的数据仅包括多达当前检查点数量的事务日志文件。差异备份不删除或更改日志文件或更改数据库标头。若要使用差异备份恢复数据库，您只需要还原两个数据集：上次的完整备份，以及最新的差异备份。</span><span class="sxs-lookup"><span data-stu-id="13743-p121">The data stored in a differential backup includes only the transaction log files up to the current checkpoint. Differential backups do not delete or change the log files or change the database headers. To use a differential backup to recover a database, you only need to restore two data sets: the last full backup, and then the most recent differential backup.</span></span> 
  
<span data-ttu-id="13743-p122">使用差异备份的缺点是，在执行完整备份之前，差异备份总是复制每个备份中的已备份数据。如果在完整备份中间执行许多差异备份，所需的存储空间可以超出相同数量的增量备份所需的存储空间。如果没有完整备份或增量备份来建立差异备份的起始点，Exchange 就不允许执行差异备份。</span><span class="sxs-lookup"><span data-stu-id="13743-p122">The disadvantage to using differential backups is that the differential backups duplicate the backed up data in each backup until a full backup is performed. If many differential backups are taken between full backups, the storage space required can exceed that required by the same number of incremental backups. Exchange does not allow a differential backup to occur when there has not been a full or incremental backup to establish the starting point for differential backups.</span></span>
  
<span data-ttu-id="13743-p123">从副本位置执行的完整备份可以紧随从活动位置执行的差异备份，反之亦然。需要注意的限制之一是上次的备份状态保留在活动数据库的标头中，对数据库标头的更改被写入到事务日志中，并且和 DAG 部署中的所有其他事务日志一样被复制和重播在复制数据库位置中。因为备份和还原可进行互操作，所以备份应用程序可以以独占方式在特定的 DAG 节点提供运行所有备份的功能，而与该节点是主动或被动无关，可以是以独占方式从被动节点运行备份，也可以是以独占方式从主动节点运行备份。</span><span class="sxs-lookup"><span data-stu-id="13743-p123">A full backup taken from the copy location can be followed by a differential backup from the active location and vice versa. One restriction to keep in mind is that the last backup state is maintained in the active database's header, and the changes to the database header are written to transaction logs, replicated, and replayed at the copy database location just like all other transaction logs in DAG deployments. Because backups and restores interoperate, backup applications provide the functionality to run all backups exclusively on a specific DAG node, regardless of whether the node is active or passive, as well as to run backups exclusively from the passive node or exclusively from the active node.</span></span>
  
<span data-ttu-id="13743-198">当的[VSS_BACKUP_TYPE](http://msdn.microsoft.com/zh-cn/library/windows/desktop/aa384679%28v=vs.85%29.aspx)枚举中 VSS 设置为**VSS_BT_DIFFERENTIAL**时，差异备份中包含以下组件：</span><span class="sxs-lookup"><span data-stu-id="13743-198">When the [VSS_BACKUP_TYPE](http://msdn.microsoft.com/zh-cn/library/windows/desktop/aa384679%28v=vs.85%29.aspx) enumeration in VSS is set to **VSS_BT_DIFFERENTIAL**, the following components are included in a differential backup:</span></span> 
  
- <span data-ttu-id="13743-199">数据库的逻辑路径 Exchange Server\Microsoft 信息存储\\< 服务器名称\>\\< 数据库 GUID\></span><span class="sxs-lookup"><span data-stu-id="13743-199">A database with the logical path Exchange Server\Microsoft Information Store\\<Server Name\>\\<Database GUID\></span></span> 
    
- <span data-ttu-id="13743-200">使用的逻辑路径 Exchange Server\Microsoft 信息存储日志文件\\< 服务器名称\>\\< 数据库 GUID\></span><span class="sxs-lookup"><span data-stu-id="13743-200">A log file with the logical path Exchange Server\Microsoft Information Store\\<Server Name\>\\<Database GUID\></span></span>
    
## <a name="see-also"></a><span data-ttu-id="13743-201">另请参阅</span><span class="sxs-lookup"><span data-stu-id="13743-201">See also</span></span>
<span data-ttu-id="13743-202"><a name="bk_AdditionalResources"> </a></span><span class="sxs-lookup"><span data-stu-id="13743-202"></span></span>

- [<span data-ttu-id="13743-203">构建备份和还原 Exchange 2013 的应用程序</span><span class="sxs-lookup"><span data-stu-id="13743-203">Build backup and restore applications for Exchange 2013</span></span>](build-backup-and-restore-applications-for-exchange-2013.md)
    
- [<span data-ttu-id="13743-204">Exchange 2013 的备份和还原概念</span><span class="sxs-lookup"><span data-stu-id="13743-204">Backup and restore concepts for Exchange 2013</span></span>](backup-and-restore-concepts-for-exchange-2013.md)
    
- [<span data-ttu-id="13743-205">还原 Exchange 2013 数据库</span><span class="sxs-lookup"><span data-stu-id="13743-205">Restoring Exchange 2013 databases</span></span>](restoring-exchange-2013-databases.md)
    
- [<span data-ttu-id="13743-206">使用 CHKSGFILES API 在 Exchange 2013 中验证备份完整性</span><span class="sxs-lookup"><span data-stu-id="13743-206">Validate backup integrity by using the CHKSGFILES API in Exchange 2013</span></span>](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md)
    
- [<span data-ttu-id="13743-207">通过使用 Eseutil 工具在 Exchange 2013 中验证备份完整性</span><span class="sxs-lookup"><span data-stu-id="13743-207">Validate backup integrity by using the Eseutil tool in Exchange 2013</span></span>](how-to-validate-backup-integrity-by-using-the-eseutil-tool-in-exchange-2013.md)
    

