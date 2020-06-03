---
title: Exchange 2013 的备份操作类型
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 70510902-9583-4177-be3d-afbf757a1ec0
description: 查找可以在 Exchange 2013 存储数据库上执行的不同类型的备份信息，包括完整备份、副本备份、增量备份和差异备份。
ms.openlocfilehash: dd07226acb3a3bb055e98f861a5c01375ee50dda
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456283"
---
# <a name="types-of-backup-operations-for-exchange-2013"></a>Exchange 2013 的备份操作类型

查找可以在 Exchange 2013 存储数据库上执行的不同类型的备份信息，包括完整备份、副本备份、增量备份和差异备份。
  
**适用于：** Exchange Server 2013 
  
本文提供了可在 Exchange Server 2013 数据库上执行的不同类型的备份的相关信息，以及这些备份对数据库文件的影响。 
  
使用卷影复制服务 (VSS) 和 Exchange 编写器的备份和还原应用程序可以执行下表中列出的备份类型。
  
**表 1. 备份操作的类型**

|**备份类型**|**说明**|
|:-----|:-----|
|[完整备份](types-of-backup-operations-for-exchange-2013.md#bk_FullBackups) <br/> |备份数据库（ \* .edb）、事务日志（ \* .log）、检查点文件（ \* .chk），然后截断特定数据库的事务日志。  <br/> |
|[复制备份](types-of-backup-operations-for-exchange-2013.md#bk_CopyBackups) <br/> |备份数据库、事务日志和检查点文件。 副本备份不会截断数据库的事务日志。  <br/> |
|[增量备份](types-of-backup-operations-for-exchange-2013.md#bk_IncrementalBackups) <br/> |备份事务日志，记录自上次完整备份或增量备份以来的所有更改，然后再截断事务日志。  <br/> |
|[差异备份](types-of-backup-operations-for-exchange-2013.md#bk_DifferentialBackups) <br/> |备份事务日志，记录自上次完整备份或增量备份以来的所有更改，并且不截断事务日志。  <br/> |
   
由 Exchange 编写器定义的组件或数据库文件表示的是 Exchange 2013 数据库中的数据库文件和事务日志。 这使您的备份和还原应用程序能够在备份操作过程中显示 Exchange 2013 数据库内组件的名称。 但是备份应用程序不能备份单个数据库组件；它只能备份整个数据库。 
  
Exchange 编写器标准化数据库组件的逻辑路径，该路径在 Exchange 编写器元数据中指定。Exchange 编写器会根据需要向备份和还原应用程序返回逻辑路径。
  
Exchange 编写器提供了以下形式的逻辑路径： 
  
 `logicalPath = "Exchange Server\Microsoft Information Store\<Server name>"`
  
服务器和数据库组件是文件组的组件，但它们没有任何关联的文件。它们具有指定单个文件的子组件。数据库中仅包含一个名为 Logs 的日志组件。单个数据库组件的组件名称是显示为字符串的数据库的 Guid。 
  
Exchange 编写器基于 VSS 框架准则仅列出了可以进行备份的数据库。 装载为 Exchange 2013 恢复数据库的数据库以及未装入的数据库都不能备份，因此不会在 Exchange 编写器的元数据中列出。
  
下图显示了 Exchange 编写器备份过程。 
  
**图 1. 备份过程的事件序列**

![此图显示备份过程的事件序列。该序列从 Exchange 存储启动开始，然后继续经历 Exchange 编写器、VSS 和客户端应用程序之间的多个步骤。](media/VSS_StoreWriterBackup.gif)
  
## <a name="full-backups"></a>完整备份
<a name="bk_FullBackups"> </a>

Exchange 数据库的完整备份涉及创建和存储数据库文件、事务日志和检查点文件的副本。 Exchange 2013 数据库包含一组专用的事务日志文件。
  
已备份数据库之后，磁盘上的事务日志文件将被截断，以便仅保留发生在备份之后的数据库更改。在此过程中，基于对现已备份的数据库已处于包含多达最新检查点个数的所有更改的状态的假设，Exchange 编写器会删除多达检查点个数的所有日志条目。 
  
如果在备份操作过程中卸除要备份的数据库，则 Exchange 2013 将不会截断事务日志，并且结果将与复制备份操作（而不是完整备份操作）等效。 
  
完整备份完成后，当前备份信息中将更新活动安装的数据库的标头。在已复制的部署中，此信息将被提交到事务日志文件并复制到数据库的其他 DAG 副本。由于该事务日志文件已重播到数据库副本，因此数据库的标头副本将被更新。
  
为了运行增量或差异卷影副本备份，完整的卷影副本备份是必需的。完整备份可以来自任何副本，只要它是卷影副本备份即可。
  
在下列方案中使用完整备份：
  
- 数据库已损坏或丢失，但在磁盘上的事务日志文件保持不变。在此方案中，可以从完整备份还原受影响的数据库文件，并通过重播仍然在磁盘上的事务日志来进行恢复。 
    
- 事务日志文件和磁盘上的数据库文件都已丢失。在此方案中，在进行完整备份时备份的事务日志文件会与数据库一起还原。
    
在 Exchange 2013 中，可以还原日志，而无需从完整备份集还原适用的数据库。 此选项对以前的完整备份进行还原以及与事务日志文件一起从最新的完整备份向前回滚。
  
当在 Exchange 编写器执行备份时，将 VSS 中的[VSS_BACKUP_TYPE](https://msdn.microsoft.com/library/windows/desktop/aa384679%28v=vs.85%29.aspx)枚举设置为**VSS_BT_FULL**时，备份中将包含以下组件： 
  
- 具有逻辑路径 Exchange Server\microsoft information store\ 信息存储 \\<服务器名称的数据库 \> \\<数据库 GUID\> 
    
- 包含逻辑路径 Exchange Server\microsoft information store\ 信息存储 \\<服务器名称的日志文件 \> \\<数据库 GUID\> 
    
## <a name="copy-backups"></a>复制备份
<a name="bk_CopyBackups"> </a>

Exchange 数据库的副本备份涉及创建和存储与包含在完整备份中相同的元素。但是，与完整备份不同的是，备份结束时磁盘上的事务日志文件不会被截断。复制备份不是为了进行数据恢复。复制备份反而是提供数据图像，该图像可用于测试、问题诊断或为副本设定种子。
  
例如，在 Exchange 存储中遇到问题的 Exchange 2013 管理员可以制作副本备份以在测试环境中使用，而不会影响生产系统。 复制备份不会影响常规备份计划；但是，因为副本备份也可将 Exchange 存储置于备份正在进行的状态，所以它会阻止其他计划的备份继续进行，直到完成或中止副本备份为止。 
  
当 VSS 中的[VSS_BACKUP_TYPE](https://msdn.microsoft.com/library/windows/desktop/aa384679%28v=vs.85%29.aspx)枚举设置为**VSS_BT_COPY**时，副本备份中包含以下组件： 
  
- 具有逻辑路径 Exchange Server\microsoft information store\ 信息存储 \\<服务器名称的数据库 \> \\<数据库 GUID\> 
    
- 包含逻辑路径 Exchange Server\microsoft information store\ 信息存储<服务器名称的日志文件组件 \\ \> \\<数据库 GUID\>
    
## <a name="incremental-backups"></a>增量备份
<a name="bk_IncrementalBackups"> </a>

Exchange 2013 数据库的增量备份会保存自上次完整备份或增量备份以来发生的对数据库所做的更改。 当所有的数据库文件和日志文件被还原到系统中时，就可恢复到上次增量备份发生时所处的状态。 增量备份中存储的数据仅包含截至当前时间的事务日志文件。 
  
备份完成时，Exchange 服务器截断日志文件，并将备份时间标记在数据库标头中。使用增量备份恢复数据库要求至少要还原两个数据集：上次的完整备份，以及自上次完整备份后执行的每个增量备份。使用增量备份的优点是单独的备份会比完整备份小得多且单独的增量备份常常小于差异备份。 
  
使用增量备份的缺点是，如果在完整备份中间执行许多增量备份，恢复 Exchange 存储可能会涉及恢复许多增量备份。如果没有以前的完整备份去建立增量更改的起始点，Exchange 就不会允许进行增量备份。 
  
从 DAG 副本位置执行的完整备份可以紧随从活动位置执行的增量备份，反之亦然。 需要注意的限制之一是上次的备份状态保留在活动数据库的标头中，对数据库标头的更改被写入到事务日志中，并且和 DAG 部署中的所有其他事务日志一样被复制和重播在复制数据库位置中。 因为备份和还原可进行互操作，所以备份应用程序可以以独占方式在特定的 DAG 节点提供运行备份的功能，而与该节点是主动或被动无关，可以是以独占方式从被动节点运行备份，也可以是以独占方式从主动节点运行备份。
  
当 VSS 中的[VSS_BACKUP_TYPE](https://msdn.microsoft.com/library/windows/desktop/aa384679%28v=vs.85%29.aspx)枚举设置为**VSS_BT_INCREMENTAL**时，增量备份中将包含以下组件： 
  
- 具有逻辑路径 Exchange Server\microsoft information store\ 信息存储 \\<服务器名称的数据库 \> \\<数据库 GUID\> 
    
- 包含逻辑路径 Exchange Server\microsoft information store\ 信息存储 \\<服务器名称的日志文件 \> \\<数据库 GUID\>
    
## <a name="differential-backups"></a>差异备份
<a name="bk_DifferentialBackups"> </a>

Exchange 2013 数据库的差异备份会保存自上次完整备份或增量备份以来发生的对数据库所做的更改。 数据库文件和日志文件一经系统还原，即可恢复到它们在上次差异备份时所处的状态。 
  
差异备份中存储的数据仅包括多达当前检查点数量的事务日志文件。差异备份不删除或更改日志文件或更改数据库标头。若要使用差异备份恢复数据库，您只需要还原两个数据集：上次的完整备份，以及最新的差异备份。 
  
使用差异备份的缺点是，在执行完整备份之前，差异备份总是复制每个备份中的已备份数据。如果在完整备份中间执行许多差异备份，所需的存储空间可以超出相同数量的增量备份所需的存储空间。如果没有完整备份或增量备份来建立差异备份的起始点，Exchange 就不允许执行差异备份。
  
从副本位置执行的完整备份可以紧随从活动位置执行的差异备份，反之亦然。需要注意的限制之一是上次的备份状态保留在活动数据库的标头中，对数据库标头的更改被写入到事务日志中，并且和 DAG 部署中的所有其他事务日志一样被复制和重播在复制数据库位置中。因为备份和还原可进行互操作，所以备份应用程序可以以独占方式在特定的 DAG 节点提供运行所有备份的功能，而与该节点是主动或被动无关，可以是以独占方式从被动节点运行备份，也可以是以独占方式从主动节点运行备份。
  
当 VSS 中的[VSS_BACKUP_TYPE](https://msdn.microsoft.com/library/windows/desktop/aa384679%28v=vs.85%29.aspx)枚举设置为**VSS_BT_DIFFERENTIAL**时，差异备份中包含以下组件： 
  
- 具有逻辑路径 Exchange Server\microsoft information store\ 信息存储 \\<服务器名称的数据库 \> \\<数据库 GUID\> 
    
- 包含逻辑路径 Exchange Server\microsoft information store\ 信息存储 \\<服务器名称的日志文件 \> \\<数据库 GUID\>
    
## <a name="see-also"></a>另请参阅
<a name="bk_AdditionalResources"> </a>

- [为 Exchange 2013 生成备份和还原应用程序](build-backup-and-restore-applications-for-exchange-2013.md)
    
- [Exchange 2013 的备份和还原概念](backup-and-restore-concepts-for-exchange-2013.md)
    
- [还原 Exchange 2013 数据库](restoring-exchange-2013-databases.md)
    
- [使用 Exchange 2013 中的 CHKSGFILES API 验证备份完整性](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md)
    
- [使用 Exchange 2013 中的 Eseutil 工具验证备份完整性](how-to-validate-backup-integrity-by-using-the-eseutil-tool-in-exchange-2013.md)
    

