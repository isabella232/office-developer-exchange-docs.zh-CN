---
title: Exchange 2013 的备份和还原概念
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 9a1c4709-9313-4ccf-9f8a-673a51d51f23
description: 查找有关 Exchange 数据库的信息，这些数据库将帮助您创建 2013 Exchange应用程序。
ms.openlocfilehash: c0b2e0269c3668779f980bf6984d84aff76573f1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510517"
---
# <a name="backup-and-restore-concepts-for-exchange-2013"></a>Exchange 2013 的备份和还原概念

查找有关 Exchange 数据库的信息，这些数据库将帮助您创建 2013 Exchange应用程序。
  
在为 Exchange Server 2013 创建备份和还原应用程序之前，您应熟悉 Exchange 数据库文件结构。 通过使用 Exchange存储数据库文件，您可以备份存储中的数据，并稍后根据需要还原该数据。 如果磁盘空间有限，则管理员可能会实现循环日志记录，这将影响备份数据库的能力。 您还可以利用 Exchange 2013 中的数据库移动功能来备份和还原Exchange数据。 数据库移动性与备份和还原应用程序相结合是灾难恢复冗余的一个很好的度量。

<a name="bk_exchangedatabases"> </a>

## <a name="exchange-store-database-files"></a>Exchange存储数据库文件

Exchange 2013 包含最多 100 个数据库的支持。 每个 Exchange 2013 数据库都包含下表中列出的文件。 
  
**表 1.Exchange 2013 数据库文件**

|文件类型|扩展名|Description|
|:-----|:-----|:-----|
|数据库文件  <br/> |\*.edb  <br/> |记录已提交到内存中数据库的所有更改。  <br/> |
|事务日志流  <br/> |\*.log  <br/> |记录将提交到数据库的操作，例如创建或修改邮件。 大小限制为每个 1 MB。  <br/> |
|检查点文件  <br/> |\*.chk  <br/> |记录哪些记录的事务已写入磁盘上的数据库文件。  <br/> |
   
Exchange 2013 可维护每个数据库的一组事务日志文件。 事务日志对于备份和恢复操作非常重要。 创建使用 VSS 卷影复制服务 (备份和还原) 时，必须确保正确处理这些日志。 有关详细信息，请参阅[事务日志和检查点文件，以在 Exchange 2013 中备份和还原](transaction-logs-and-checkpoint-files-for-backup-and-restore-in-exchange.md)。 若要备份数据库及其日志流，必须备份包含数据库和日志的整个卷。 日志截断仅在包含数据库的卷或文件夹的完整备份成功完成Exchange发生。
  
在每台Exchange服务器上，一次只能装入一个恢复数据库。 您可以使用命令行管理程序 cmdlet（如 **New-MailboxRestoreRequest** Exchange命令行管理程序 cmdlet）访问恢复数据库。 有关恢复数据库Exchange，请参阅 TechNet[上的](https://technet.microsoft.com/library/dd876954%28v=exchg.150%29.aspx)恢复数据库。 有关命令行管理程序 cmdlet Exchange，请参阅 TechNet 上的 Exchange [2013 Cmdlet。](https://technet.microsoft.com/library/bb124413.aspx) 
  
## <a name="circular-logging"></a>循环日志记录
<a name="bk_circularlogging"> </a>

如果存储容量是问题，则管理员可能会启用循环日志记录。 启用循环日志记录后，Exchange像往常一样写入事务日志，但是当检查点文件处于高级状态时，事务日志的非活动部分将被截断。 如果您还计划使用 VSS 启用自定义备份和还原操作，则管理员不应将 Exchange 2013 数据库配置为使用循环日志记录。 循环日志记录会创建以下限制： 
  
- 如果在备份操作或恢复操作期间启用，则不能还原单个数据库。
    
- 只能执行时间点恢复操作。 启用循环日志记录后，可以在还原数据库时删除同一目录中的事务日志，尽管这些日志可能是 2013 年 2013 年Exchange的一部分。 
    
- 不能执行增量备份或差异备份操作。 有关这些备份类型的信息，请参阅[Types of backup operations for Exchange 2013](types-of-backup-operations-for-exchange-2013.md)。
    
如果启用循环日志记录，则管理员应尽快禁用它，以确保 VSS 备份不会失败。 有关详细信息，请查看博客文章Exchange[循环日志记录和 VSS 备份](https://blogs.technet.com/b/exchange/archive/2010/08/18/3410672.aspx)。 
  
## <a name="exchange-database-mobility"></a>Exchange数据库移动性
<a name="bk_exchangedatabasemobility"> </a>

Exchange 2013 允许数据库移动性，以提高邮箱可靠性和可用性。 利用数据库移动功能，您可以复制数据库Exchange数据库，断开该数据库与服务器的连接，然后将其存储在另一台服务器上。 在 Exchange 2013 数据库可用性 (DAG) 中，数据库的多个副本存储在不同的计算机上。 当数据库的一个或多个副本由于硬件或其他系统故障而丢失时，其他副本的信息可用于通过正常复制操作对数据库重新进行重新设置。
  
对于备份操作，如果要备份的 Exchange 2013 数据库在 DAG 中配置，则备份应用程序可以通过对非活动数据库副本之一拍摄快照来更好地防止快照与活动服务器的性能之间的干扰。 由于数据库副本大部分是同步的，因此备份应用程序可以从数据库的不同副本获取快照，然后从片段重新构造数据库。
  
从备份数据还原 DAG 数据库的唯一受支持的方法是使用相同的备份数据还原数据库的所有副本。 由于两个副本之间的数据库日志文件可能略有不同，因此使用不同的数据还原各个数据库副本可能会导致数据库无法装入。
  
## <a name="in-this-section"></a>本节内容
<a name="bk_inthissection"> </a>

- [Exchange 2013 中用于备份和还原的事务日志和检查点文件](transaction-logs-and-checkpoint-files-for-backup-and-restore-in-exchange.md)
    
- [Exchange 2013 Exchange编写器](exchange-writer-in-exchange-2013.md)
    
## <a name="see-also"></a>另请参阅

- [Exchange Online 和 Exchange 开发](../exchange-server-development.md) 
- [Exchange 2013 的备份操作类型](types-of-backup-operations-for-exchange-2013.md)
- [还原 Exchange 2013 数据库](restoring-exchange-2013-databases.md)
    

