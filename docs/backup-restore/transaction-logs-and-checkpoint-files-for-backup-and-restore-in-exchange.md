---
title: 用于在 Exchange 中进行备份和还原的事务日志和检查点文件
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 80e04b9f-87c7-4acf-89b1-aa66ffaf7e53
description: 查找有关事务日志和检查点文件以及如何使用它们来备份和还原 Exchange 2013 数据的信息。
ms.openlocfilehash: 5b01fc6924f82e76943795df877ae84b1fde087b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456386"
---
# <a name="transaction-logs-and-checkpoint-files-for-backup-and-restore-in-exchange"></a><span data-ttu-id="f7a5c-103">用于在 Exchange 中进行备份和还原的事务日志和检查点文件</span><span class="sxs-lookup"><span data-stu-id="f7a5c-103">Transaction logs and checkpoint files for backup and restore in Exchange</span></span>

<span data-ttu-id="f7a5c-104">查找有关事务日志和检查点文件以及如何使用它们来备份和还原 Exchange 2013 数据的信息。</span><span class="sxs-lookup"><span data-stu-id="f7a5c-104">Find information about transaction logs and checkpoint files and how they are used to back up and restore Exchange 2013 data.</span></span>
  
<span data-ttu-id="f7a5c-105">**适用于：** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="f7a5c-105">**Applies to:** Exchange Server 2013</span></span> 
  
<span data-ttu-id="f7a5c-106">本文介绍 Exchange Server 2013 如何使用事务日志和检查点文件来帮助防止数据丢失。</span><span class="sxs-lookup"><span data-stu-id="f7a5c-106">This article describes how Exchange Server 2013 uses transaction logs and checkpoint files to help prevent data loss.</span></span> <span data-ttu-id="f7a5c-107">当您开发一些在 Windows Server 2008 以上的 Windows Server 版本中使用卷影复制服务 (VSS) 的备份和还原应用程序时，务必要注意此信息。</span><span class="sxs-lookup"><span data-stu-id="f7a5c-107">It is important to be aware of this information when you develop backup and restore applications that use the Volume Shadow Copy Service (VSS) in versions of Windows Server starting with Windows Server 2008.</span></span>
  
## <a name="transaction-logs-in-exchange-2013"></a><span data-ttu-id="f7a5c-108">Exchange 2013 中的事务日志</span><span class="sxs-lookup"><span data-stu-id="f7a5c-108">Transaction logs in Exchange 2013</span></span>

<span data-ttu-id="f7a5c-109">Exchange 2013 维护每个数据库的一组事务日志文件。</span><span class="sxs-lookup"><span data-stu-id="f7a5c-109">Exchange 2013 maintains a single set of transaction log files for each database.</span></span> <span data-ttu-id="f7a5c-110">事务被定义为更改数据库状态或内容的任何操作。</span><span class="sxs-lookup"><span data-stu-id="f7a5c-110">A transaction is defined as any operation that changes the state or contents of the database.</span></span> <span data-ttu-id="f7a5c-111">单个数据库的事务日志文件记录对该数据库执行的所有事务。</span><span class="sxs-lookup"><span data-stu-id="f7a5c-111">The transaction log files for an individual database record all the transactions performed on the database.</span></span> <span data-ttu-id="f7a5c-112">事务的记录将写入事务日志，然后成为数据库的一部分，这样可以确保在数据库出现故障时可恢复所有已提交的事务。</span><span class="sxs-lookup"><span data-stu-id="f7a5c-112">Records of the transactions are written to the transaction logs before they are made in the database itself, to ensure that all committed transactions can be recovered in the event of a database failure.</span></span> <span data-ttu-id="f7a5c-113">在将事务提交到数据库文件之前，Exchange 2013 数据库事务日志存储在磁盘上。</span><span class="sxs-lookup"><span data-stu-id="f7a5c-113">Exchange 2013 database transaction logs are stored on disk before the transactions are committed to the database file.</span></span> 
  
<span data-ttu-id="f7a5c-114">在更新数据库之前记录事务称为“预写日志记录”。</span><span class="sxs-lookup"><span data-stu-id="f7a5c-114">The recording of the transactions before the database is updated is called write-ahead logging.</span></span> <span data-ttu-id="f7a5c-115">为了帮助确保数据库正确恢复到正确状态，Exchange 2013 使用基于页面的写入和检查点将数据写入数据库文件中。</span><span class="sxs-lookup"><span data-stu-id="f7a5c-115">To help ensure that the database is correctly brought back to the proper state, Exchange 2013 writes data into the database files by using page-based writes and checkpoints.</span></span> <span data-ttu-id="f7a5c-116">在正常操作过程中，Exchange 存储首先将数据库更改记录在事务日志中，然后将这些更改存储在数据库的内存副本中。</span><span class="sxs-lookup"><span data-stu-id="f7a5c-116">During regular operations, the Exchange store first records database changes in the transaction logs, and then makes those changes on an in-memory copy of the database.</span></span> <span data-ttu-id="f7a5c-117">事务日志记录每个事务的开头和结尾。</span><span class="sxs-lookup"><span data-stu-id="f7a5c-117">The transaction logs record the beginning and end of each transaction.</span></span> <span data-ttu-id="f7a5c-118">这样可以确保有足够的信息可提供给将来在数据库中执行的撤消或回滚操作。</span><span class="sxs-lookup"><span data-stu-id="f7a5c-118">This ensures that sufficient information is available to later undo or roll back operations in the database.</span></span>
  
<span data-ttu-id="f7a5c-119">当从磁盘上的数据库文件已损坏但事务日志完好的错误中恢复时，您的还原应用程序必须首先还原数据库文件的已知正确副本。</span><span class="sxs-lookup"><span data-stu-id="f7a5c-119">When recovering from errors in which the database file on disk is damaged, but the transaction logs are intact, your restore application must first restore a known good copy of the database file.</span></span>
  
<span data-ttu-id="f7a5c-p104">Exchange 存储将重播来自以前备份的事务日志的事务，然后重播磁盘上的事务日志文件中的所有剩余事务。请注意，如果在将事务记录在事务日志并实际将它们写入数据库文件的过程中系统出现故障，则有时可能会丢失事务。</span><span class="sxs-lookup"><span data-stu-id="f7a5c-p104">The Exchange store replays the transactions from the previously backed up transaction logs, and then replays any remaining transactions from the on-disk transaction log files. Note that sometimes transactions can be lost if the system fails between when the transactions are recorded in the transaction logs, and when they are actually written to the database files.</span></span> 
  
<span data-ttu-id="f7a5c-p105">Exchange 存储会定期检查内存数据库图像，然后确定哪些页面已更改。Exchange 存储将组合挂起的更改，然后将这些页面写入到磁盘上的数据库文件中。</span><span class="sxs-lookup"><span data-stu-id="f7a5c-p105">Periodically, the Exchange store checks the in-memory database image, and then determines which pages have changed. The Exchange store combines the pending changes, and then writes those pages to the database file on disk.</span></span>
  
## <a name="checkpoint-files-in-exchange-2013"></a><span data-ttu-id="f7a5c-124">Exchange 2013 中的检查点文件</span><span class="sxs-lookup"><span data-stu-id="f7a5c-124">Checkpoint files in Exchange 2013</span></span>

<span data-ttu-id="f7a5c-p106">检查点文件记录哪些记录的事务已被写入磁盘上的数据库文件。当被事务日志中的条目修改过的所有数据库页都已成功写入到磁盘中时，检查点数量会增加。由于检查点文件记录已存在于磁盘上的数据库映像中的交易记录，所以 Exchange 存储仅需要重播在检查点之后发生的事务。根据备份之间的时间段，如果系统发生故障，这样做会极大地降低必须重播到数据库中的事务数。</span><span class="sxs-lookup"><span data-stu-id="f7a5c-p106">A checkpoint file records which logged transactions have been written to the on-disk database files. The checkpoint is advanced when all the database pages that have been modified by entries in the transaction logs are successfully written to disk. Because the checkpoint file records which transactions are already in the on-disk database image, the Exchange store only needs to replay transactions that occurred after the checkpoint. Depending on the time period between backups, this can greatly decrease the number of transactions that must be replayed into the database if a system failure occurs.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f7a5c-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f7a5c-129">See also</span></span>

- [<span data-ttu-id="f7a5c-130">Exchange 2013 的备份和还原概念</span><span class="sxs-lookup"><span data-stu-id="f7a5c-130">Backup and restore concepts for Exchange 2013</span></span>](backup-and-restore-concepts-for-exchange-2013.md)
- [<span data-ttu-id="f7a5c-131">Exchange 2013 的备份操作类型</span><span class="sxs-lookup"><span data-stu-id="f7a5c-131">Types of backup operations for Exchange 2013</span></span>](types-of-backup-operations-for-exchange-2013.md)
- [<span data-ttu-id="f7a5c-132">还原 Exchange 2013 数据库</span><span class="sxs-lookup"><span data-stu-id="f7a5c-132">Restoring Exchange 2013 databases</span></span>](restoring-exchange-2013-databases.md)
    

