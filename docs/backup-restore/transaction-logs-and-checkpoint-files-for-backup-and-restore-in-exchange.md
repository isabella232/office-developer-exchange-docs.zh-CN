---
title: 事务日志和备份和还原 Exchange 中的检查点文件
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 80e04b9f-87c7-4acf-89b1-aa66ffaf7e53
description: 查找有关事务日志和检查点文件以及如何使用它们来备份和还原 Exchange 2013 数据的信息。
ms.openlocfilehash: 53f128348bb2e8895bc1eefaf62402fa348c81ea
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752714"
---
# <a name="transaction-logs-and-checkpoint-files-for-backup-and-restore-in-exchange"></a>事务日志和备份和还原 Exchange 中的检查点文件

查找有关事务日志和检查点文件以及如何使用它们来备份和还原 Exchange 2013 数据的信息。
  
**适用于：** Exchange Server 2013 
  
本文介绍 Exchange Server 2013 如何使用事务日志和检查点文件帮助防止数据丢失。 务必在制定备份和还原的开头 Windows Server 2008 的 Windows Server 版本中使用卷影复制服务 (VSS) 的应用程序时要注意的此信息。
  
## <a name="transaction-logs-in-exchange-2013"></a>Exchange 2013 中的事务日志

Exchange 2013 维护一组的每个数据库的事务日志文件。 事务被定义为更改的状态或内容数据库的任何操作。 对于单个数据库记录的所有事务数据库都执行事务日志文件。 事务记录写入事务日志之前他们所做数据库本身，以确保所有提交的事务，可以恢复如果数据库故障。 Exchange 2013 数据库事务日志存储在磁盘上的事务提交到数据库文件之前。 
  
记录之前更新的数据库的事务称为提前写入日志记录。 为了帮助确保数据库后正确将有正确的状态，Exchange 2013 将数据写入到数据库文件使用基于页面的写入和检查点。 常规操作期间 Exchange 存储首先事务日志中记录数据库的更改，并在内存中副本的数据库将这些更改。 事务日志记录的开头和结尾的每个事务。 这确保足够的信息可用于更高版本撤消或回滚操作数据库中。
  
当从磁盘上的数据库文件已损坏但事务日志完好的错误中恢复时，您的还原应用程序必须首先还原数据库文件的已知正确副本。
  
Exchange 存储将重播来自以前备份的事务日志的事务，然后重播磁盘上的事务日志文件中的所有剩余事务。请注意，如果在将事务记录在事务日志并实际将它们写入数据库文件的过程中系统出现故障，则有时可能会丢失事务。 
  
Exchange 存储会定期检查内存数据库图像，然后确定哪些页面已更改。Exchange 存储将组合挂起的更改，然后将这些页面写入到磁盘上的数据库文件中。
  
## <a name="checkpoint-files-in-exchange-2013"></a>Exchange 2013 中的检查点文件

检查点文件记录哪些记录的事务已被写入磁盘上的数据库文件。当被事务日志中的条目修改过的所有数据库页都已成功写入到磁盘中时，检查点数量会增加。由于检查点文件记录已存在于磁盘上的数据库映像中的交易记录，所以 Exchange 存储仅需要重播在检查点之后发生的事务。根据备份之间的时间段，如果系统发生故障，这样做会极大地降低必须重播到数据库中的事务数。
  
## <a name="see-also"></a>另请参阅

- [Exchange 2013 的备份和还原概念](backup-and-restore-concepts-for-exchange-2013.md)
- [Exchange 2013 的备份操作的类型](types-of-backup-operations-for-exchange-2013.md)
- [还原 Exchange 2013 数据库](restoring-exchange-2013-databases.md)
    

