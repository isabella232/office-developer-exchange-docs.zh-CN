---
title: Exchange 2013 的备份和还原概念
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9a1c4709-9313-4ccf-9f8a-673a51d51f23
description: 查找可帮助您为 Exchange 2013 创建备份和还原应用程序的 Exchange 数据库的相关信息。
ms.openlocfilehash: fd35699839af105dd3fe285776b071c1d03d58dd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44437982"
---
# <a name="backup-and-restore-concepts-for-exchange-2013"></a>Exchange 2013 的备份和还原概念

查找可帮助您为 Exchange 2013 创建备份和还原应用程序的 Exchange 数据库的相关信息。
  
在为 Exchange Server 2013 创建备份和还原应用程序之前，您应熟悉 Exchange 数据库文件结构。 通过使用 Exchange 存储数据库文件，可以备份存储中的数据，并在以后需要时将其还原。 如果您的磁盘空间有限，管理员可能会实施循环日志记录，这将影响您备份数据库的能力。 您还可以利用 Exchange 2013 中的数据库移动功能来备份和还原 Exchange 数据。 与备份和还原应用程序结合使用的数据库移动性是用于灾难恢复的冗余的最佳度量。

<a name="bk_exchangedatabases"> </a>

## <a name="exchange-store-database-files"></a>Exchange 存储数据库文件

Exchange 2013 包括最高为100个数据库的支持。 每个 Exchange 2013 数据库都包含下表中列出的文件。 
  
**表1。Exchange 2013 数据库文件**

|文件类型|扩展名|说明|
|:-----|:-----|:-----|
|数据库文件  <br/> |\*.edb  <br/> |记录已提交到内存中数据库的所有更改。  <br/> |
|事务日志流  <br/> |\*.log  <br/> |记录将提交到数据库的操作，例如创建或修改邮件。 限制为每个大小的 1 MB。  <br/> |
|检查点文件  <br/> |\*.chk  <br/> |记录记录的事务已写入磁盘上的数据库文件。  <br/> |
   
Exchange 2013 维护每个数据库的一组事务日志文件。 事务日志对于备份和恢复操作非常重要。 创建使用卷影复制服务（VSS）的备份和还原应用程序时，必须确保正确处理这些日志。 有关详细信息，请参阅[Exchange 2013 中的备份和还原的事务日志和检查点文件](transaction-logs-and-checkpoint-files-for-backup-and-restore-in-exchange.md)。 若要备份数据库及其日志流，必须备份包含数据库和日志的整个卷。 仅在成功完成包含 Exchange 数据库的卷或文件夹的完整备份之后，才会发生日志截断。
  
在每个 Exchange 服务器上，一次只能装入一个恢复数据库。 您可以使用 Exchange 命令行管理程序 cmdlet （如**new-mailboxrestorerequest**）访问恢复数据库。 有关 Exchange 恢复数据库的详细信息，请参阅 TechNet 上的[恢复数据库](https://technet.microsoft.com/library/dd876954%28v=exchg.150%29.aspx)。 有关 Exchange 命令行管理程序 cmdlet 的详细信息，请参阅 TechNet 上的[exchange 2013 cmdlet](https://technet.microsoft.com/library/bb124413.aspx) 。 
  
## <a name="circular-logging"></a>循环日志记录
<a name="bk_circularlogging"> </a>

如果存储容量是一个问题，则管理员可能会启用循环日志记录。 启用循环日志记录时，Exchange 会照常写入事务日志，但如果检查点文件是高级的，事务日志的非活动部分将被截断。 如果您还计划使用 VSS 启用您的自定义备份和还原操作，则管理员不应将 Exchange 2013 数据库配置为使用循环日志记录。 循环日志记录将创建以下限制： 
  
- 如果在备份操作或恢复操作过程中启用此功能，则无法还原单个数据库。
    
- 仅可以执行时间点恢复操作。 启用循环日志记录时，您可以在还原数据库时删除同一目录中的事务日志，尽管这些日志可能是不同 Exchange 2013 数据库的一部分。 
    
- 您不能执行增量或差异备份操作。 有关这些类型的备份的详细信息，请参阅[Exchange 2013 的备份操作类型](types-of-backup-operations-for-exchange-2013.md)。
    
如果启用了循环日志记录，则管理员应尽快禁用它，以确保 VSS 备份不会失败。 有关详细信息，请查看博客文章[Exchange 循环日志记录和 VSS 备份](https://blogs.technet.com/b/exchange/archive/2010/08/18/3410672.aspx)。 
  
## <a name="exchange-database-mobility"></a>Exchange 数据库移动性
<a name="bk_exchangedatabasemobility"> </a>

Exchange 2013 允许数据库移动性提高邮箱的可靠性和可用性。 利用数据库移动功能，您可以制作 Exchange 存储数据库的副本，断开数据库与服务器的连接，并将其存储在另一台服务器上。 在 Exchange 2013 数据库可用性组（DAG）中，数据库的多个副本存储在不同的计算机上。 当由于硬件或其他系统故障而丢失数据库的一个或多个副本时，可使用来自其他副本的信息通过正常的复制操作对数据库进行种子设定。
  
对于备份操作，如果要备份的 Exchange 2013 数据库是在 DAG 中配置的，则备份应用程序可以通过在其中一个非活动数据库副本上拍摄快照来更好地阻止快照和活动服务器的性能之间的干扰。 由于数据库副本的大部分同步，因此备份应用程序可以从数据库的不同副本获取快照，稍后再从这些部分重建快照。
  
从备份数据中还原 DAG 数据库的唯一受支持方法是使用相同的备份数据还原数据库的所有副本。 由于副本之间的数据库日志文件可能稍有不同，因此使用不同数据还原单个数据库副本可能会导致数据库变得无法装入。
  
## <a name="in-this-section"></a>本节内容
<a name="bk_inthissection"> </a>

- [Exchange 2013 中用于备份和还原的事务日志和检查点文件](transaction-logs-and-checkpoint-files-for-backup-and-restore-in-exchange.md)
    
- [Exchange 2013 中的 exchange 编写器](exchange-writer-in-exchange-2013.md)
    
## <a name="see-also"></a>另请参阅

- [Exchange Online 和 Exchange 开发](../exchange-server-development.md) 
- [Exchange 2013 的备份操作类型](types-of-backup-operations-for-exchange-2013.md)
- [还原 Exchange 2013 数据库](restoring-exchange-2013-databases.md)
    

