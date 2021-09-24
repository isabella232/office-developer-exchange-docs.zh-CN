---
title: 用于备份和还原的事务日志和检查点Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 80e04b9f-87c7-4acf-89b1-aa66ffaf7e53
description: 查找有关事务日志和检查点文件以及如何使用它们备份和还原 2013 Exchange的信息。
ms.openlocfilehash: ae47c7757a1001f28c467ea58ec87b4ddbc5a5c4
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513260"
---
# <a name="transaction-logs-and-checkpoint-files-for-backup-and-restore-in-exchange"></a>用于备份和还原的事务日志和检查点Exchange

查找有关事务日志和检查点文件以及如何使用它们备份和还原 2013 Exchange的信息。
  
**适用于：Exchange Server** 2013 
  
本文介绍了 2013 Exchange Server如何使用事务日志和检查点文件来帮助防止数据丢失。 当您开发一些在 Windows Server 2008 以上的 Windows Server 版本中使用卷影复制服务 (VSS) 的备份和还原应用程序时，务必要注意此信息。
  
## <a name="transaction-logs-in-exchange-2013"></a>Exchange 2013 中的事务日志

Exchange 2013 可维护每个数据库的一组事务日志文件。 事务被定义为更改数据库状态或内容的任何操作。 单个数据库的事务日志文件记录对该数据库执行的所有事务。 事务的记录将写入事务日志，然后成为数据库的一部分，这样可以确保在数据库出现故障时可恢复所有已提交的事务。 Exchange 2013 数据库事务日志存储在磁盘上，然后再将事务提交到数据库文件。 
  
在更新数据库之前记录事务称为“预写日志记录”。 为了帮助确保数据库正确返回正确的状态，Exchange 2013 使用基于页面的写入和检查点将数据写入数据库文件。 在正常操作过程中，Exchange 存储首先将数据库更改记录在事务日志中，然后将这些更改存储在数据库的内存副本中。 事务日志记录每个事务的开头和结尾。 这样可以确保有足够的信息可提供给将来在数据库中执行的撤消或回滚操作。
  
当从磁盘上的数据库文件已损坏但事务日志完好的错误中恢复时，您的还原应用程序必须首先还原数据库文件的已知正确副本。
  
Exchange 存储将重播来自以前备份的事务日志的事务，然后重播磁盘上的事务日志文件中的所有剩余事务。请注意，如果在将事务记录在事务日志并实际将它们写入数据库文件的过程中系统出现故障，则有时可能会丢失事务。 
  
Exchange 存储会定期检查内存数据库图像，然后确定哪些页面已更改。Exchange 存储将组合挂起的更改，然后将这些页面写入到磁盘上的数据库文件中。
  
## <a name="checkpoint-files-in-exchange-2013"></a>Exchange 2013 中的检查点文件

检查点文件记录哪些记录的事务已被写入磁盘上的数据库文件。当被事务日志中的条目修改过的所有数据库页都已成功写入到磁盘中时，检查点数量会增加。由于检查点文件记录已存在于磁盘上的数据库映像中的交易记录，所以 Exchange 存储仅需要重播在检查点之后发生的事务。根据备份之间的时间段，如果系统发生故障，这样做会极大地降低必须重播到数据库中的事务数。
  
## <a name="see-also"></a>另请参阅

- [Exchange 2013 的备份和还原概念](backup-and-restore-concepts-for-exchange-2013.md)
- [Exchange 2013 的备份操作类型](types-of-backup-operations-for-exchange-2013.md)
- [还原 Exchange 2013 数据库](restoring-exchange-2013-databases.md)
    

