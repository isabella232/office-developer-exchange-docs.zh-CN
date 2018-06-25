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
# <a name="types-of-backup-operations-for-exchange-2013"></a>Exchange 2013 的备份操作类型

您可以执行 Exchange 2013 有关备份的不同类型的查找信息存储数据库，包括完全、 复制、 增量和差异备份。
  
**适用于：** Exchange Server 2013 
  
本文提供了有关备份的不同类型的信息可以在 Exchange Server 2013 的数据库上执行以及这些备份如何影响数据库文件。 
  
使用卷影复制服务 (VSS) 和 Exchange 编写器的备份和还原应用程序可以执行下表中列出的备份类型。
  
**表 1。备份操作的类型**

|**备份类型**|**说明**|
|:-----|:-----|
|[完整备份](types-of-backup-operations-for-exchange-2013.md#bk_FullBackups) <br/> |备份数据库 (\*.edb)，事务日志 (\*.log)，检查点文件 (\*.chk)，，然后截断特定数据库的事务日志。  <br/> |
|[将备份复制](types-of-backup-operations-for-exchange-2013.md#bk_CopyBackups) <br/> |备份数据库、事务日志和检查点文件。副本备份不会截断数据库的事务日志。  <br/> |
|[增量备份](types-of-backup-operations-for-exchange-2013.md#bk_IncrementalBackups) <br/> |备份事务日志，记录自上次完整备份或增量备份以来的所有更改，然后再截断事务日志。  <br/> |
|[差异备份](types-of-backup-operations-for-exchange-2013.md#bk_DifferentialBackups) <br/> |备份事务日志，记录自上次完整备份或增量备份以来的所有更改，并且不截断事务日志。  <br/> |
   
组件或数据库文件，由 Exchange 编写器定义表示数据库文件和 Exchange 2013 数据库中的事务日志。 这样，备份和还原应用程序备份操作过程中显示的 Exchange 2013 数据库中的组件名称。 备份应用程序不能但是; 备份单个数据库组件它可以只备份整个数据库。 
  
Exchange 编写器标准化数据库组件的逻辑路径，该路径在 Exchange 编写器元数据中指定。Exchange 编写器会根据需要向备份和还原应用程序返回逻辑路径。
  
Exchange 作者提供了窗体中的逻辑路径： 
  
 `logicalPath = "Exchange Server\Microsoft Information Store\<Server name>"`
  
服务器和数据库组件是文件组的组件，但它们没有任何关联的文件。它们具有指定单个文件的子组件。数据库中仅包含一个名为 Logs 的日志组件。单个数据库组件的组件名称是显示为字符串的数据库的 Guid。 
  
Exchange 书写器仅列出了可以在基于 VSS 框架准则，备份的数据库。 为 Exchange 2013 恢复数据库，以及未装入的数据库装入的数据库无法进行备份，并因此中未列出 Exchange 编写器元数据。
  
下图显示了 Exchange 编写器备份过程。 
  
**图 1。备份过程的事件顺序**

![此图显示备份过程的事件序列。该序列从 Exchange 存储启动开始，然后继续经历 Exchange 编写器、VSS 和客户端应用程序之间的多个步骤。](media/VSS_StoreWriterBackup.gif)
  
## <a name="full-backups"></a>完整备份
<a name="bk_FullBackups"> </a>

Exchange 数据库的完整备份包括创建和存储的数据库文件、 事务日志和检查点文件的副本。 Exchange 2013 数据库有一组专用的事务日志文件。
  
已备份数据库之后，磁盘上的事务日志文件将被截断，以便仅保留发生在备份之后的数据库更改。在此过程中，基于对现已备份的数据库已处于包含多达最新检查点个数的所有更改的状态的假设，Exchange 编写器会删除多达检查点个数的所有日志条目。 
  
如果在备份操作过程中将卸除数据库备份，Exchange 2013 将不会截断事务日志，结果将备份复制操作，不是完整备份操作的等效项。 
  
完整备份完成后，当前备份信息中将更新活动安装的数据库的标头。在已复制的部署中，此信息将被提交到事务日志文件并复制到数据库的其他 DAG 副本。由于该事务日志文件已重播到数据库副本，因此数据库的标头副本将被更新。
  
为了运行增量或差异卷影副本备份，完整的卷影副本备份是必需的。完整备份可以来自任何副本，只要它是卷影副本备份即可。
  
在下列方案中使用完整备份：
  
- 数据库已损坏或丢失，但在磁盘上的事务日志文件保持不变。在此方案中，可以从完整备份还原受影响的数据库文件，并通过重播仍然在磁盘上的事务日志来进行恢复。 
    
- 事务日志文件和磁盘上的数据库文件都已丢失。在此方案中，在进行完整备份时备份的事务日志文件会与数据库一起还原。
    
在 Exchange 2013 中可以还原日志而无需还原完整备份集适用的数据库。 此选项可使可能为以前的完整备份来还原并将其与最新的完整备份滚的事务日志文件结合使用。
  
当的[VSS_BACKUP_TYPE](http://msdn.microsoft.com/en-us/library/windows/desktop/aa384679%28v=vs.85%29.aspx)枚举中 VSS 设置为**VSS_BT_FULL** Exchange 编写器执行备份时，备份中包括以下组件： 
  
- 数据库的逻辑路径 Exchange Server\Microsoft 信息存储\\< 服务器名称\>\\< 数据库 GUID\> 
    
- 使用的逻辑路径 Exchange Server\Microsoft 信息存储日志文件\\< 服务器名称\>\\< 数据库 GUID\> 
    
## <a name="copy-backups"></a>复制备份
<a name="bk_CopyBackups"> </a>

Exchange 数据库的副本备份涉及创建和存储与包含在完整备份中相同的元素。但是，与完整备份不同的是，备份结束时磁盘上的事务日志文件不会被截断。复制备份不是为了进行数据恢复。复制备份反而是提供数据图像，该图像可用于测试、问题诊断或为副本设定种子。
  
例如，遇到问题 Exchange 存储的 Exchange 2013 管理员可以创建副本备份用于测试环境中而不会影响生产系统。 复制备份不会影响常规备份时间表;但是，副本备份还将 Exchange 存储在备份正在进行中状态，因为它会阻止继续之前完成或已中止副本备份从其他计划的备份。 
  
当的[VSS_BACKUP_TYPE](http://msdn.microsoft.com/en-us/library/windows/desktop/aa384679%28v=vs.85%29.aspx)枚举中 VSS 设置为**VSS_BT_COPY**时，副本备份中包含以下组件： 
  
- 数据库的逻辑路径 Exchange Server\Microsoft 信息存储\\< 服务器名称\>\\< 数据库 GUID\> 
    
- 使用的逻辑路径 Exchange Server\Microsoft 信息存储日志文件组件\\< 服务器名称\>\\< 数据库 GUID\>
    
## <a name="incremental-backups"></a>增量备份
<a name="bk_IncrementalBackups"> </a>

Exchange 2013 数据库的增量备份将更改保存到发生自上次完整或增量备份的数据库。 在所有数据库文件和日志文件都还原到系统中时，就可恢复到所上次增量备份时的状态。 增量备份中存储的数据仅包含事务日志文件到当前时间为止。 
  
备份完成时，Exchange 服务器截断日志文件，并将备份时间标记在数据库标头中。使用增量备份恢复数据库要求至少要还原两个数据集：上次的完整备份，以及自上次完整备份后执行的每个增量备份。使用增量备份的优点是单独的备份会比完整备份小得多且单独的增量备份常常小于差异备份。 
  
使用增量备份的缺点是，如果在完整备份中间执行许多增量备份，恢复 Exchange 存储可能会涉及恢复许多增量备份。如果没有以前的完整备份去建立增量更改的起始点，Exchange 就不会允许进行增量备份。 
  
完整备份摘自 DAG 复制位置可以跟增量备份的活动的位置，反之亦然。 限制之一，需要注意的是最后一个备份状态维护活动的数据库的标头中，并向数据库头更改写入到事务日志，复制，并重播一样所有其他事务的复制数据库位置在 DAG 部署中的日志。 备份应用程序备份和还原互操作，因为可以提供的功能以独占方式在特定 DAG 节点上，无论节点是否是主动或被动，运行备份，以及以独占方式从被动节点运行备份或以独占方式从主动节点。
  
当的[VSS_BACKUP_TYPE](http://msdn.microsoft.com/en-us/library/windows/desktop/aa384679%28v=vs.85%29.aspx)枚举中 VSS 设置为**VSS_BT_INCREMENTAL**时，增量备份中包含以下组件： 
  
- 数据库的逻辑路径 Exchange Server\Microsoft 信息存储\\< 服务器名称\>\\< 数据库 GUID\> 
    
- 使用的逻辑路径 Exchange Server\Microsoft 信息存储日志文件\\< 服务器名称\>\\< 数据库 GUID\>
    
## <a name="differential-backups"></a>差异备份
<a name="bk_DifferentialBackups"> </a>

Exchange 2013 数据库的差异备份将更改保存到发生自上次完整或增量备份的数据库。 时由系统还原的数据库文件和日志文件，它们可以恢复到它们在差异备份所处的状态。 
  
差异备份中存储的数据仅包括多达当前检查点数量的事务日志文件。差异备份不删除或更改日志文件或更改数据库标头。若要使用差异备份恢复数据库，您只需要还原两个数据集：上次的完整备份，以及最新的差异备份。 
  
使用差异备份的缺点是，在执行完整备份之前，差异备份总是复制每个备份中的已备份数据。如果在完整备份中间执行许多差异备份，所需的存储空间可以超出相同数量的增量备份所需的存储空间。如果没有完整备份或增量备份来建立差异备份的起始点，Exchange 就不允许执行差异备份。
  
从副本位置执行的完整备份可以紧随从活动位置执行的差异备份，反之亦然。需要注意的限制之一是上次的备份状态保留在活动数据库的标头中，对数据库标头的更改被写入到事务日志中，并且和 DAG 部署中的所有其他事务日志一样被复制和重播在复制数据库位置中。因为备份和还原可进行互操作，所以备份应用程序可以以独占方式在特定的 DAG 节点提供运行所有备份的功能，而与该节点是主动或被动无关，可以是以独占方式从被动节点运行备份，也可以是以独占方式从主动节点运行备份。
  
当的[VSS_BACKUP_TYPE](http://msdn.microsoft.com/en-us/library/windows/desktop/aa384679%28v=vs.85%29.aspx)枚举中 VSS 设置为**VSS_BT_DIFFERENTIAL**时，差异备份中包含以下组件： 
  
- 数据库的逻辑路径 Exchange Server\Microsoft 信息存储\\< 服务器名称\>\\< 数据库 GUID\> 
    
- 使用的逻辑路径 Exchange Server\Microsoft 信息存储日志文件\\< 服务器名称\>\\< 数据库 GUID\>
    
## <a name="see-also"></a>另请参阅
<a name="bk_AdditionalResources"> </a>

- [构建备份和还原 Exchange 2013 的应用程序](build-backup-and-restore-applications-for-exchange-2013.md)
    
- [Exchange 2013 的备份和还原概念](backup-and-restore-concepts-for-exchange-2013.md)
    
- [还原 Exchange 2013 数据库](restoring-exchange-2013-databases.md)
    
- [使用 CHKSGFILES API 在 Exchange 2013 中验证备份完整性](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md)
    
- [通过使用 Eseutil 工具在 Exchange 2013 中验证备份完整性](how-to-validate-backup-integrity-by-using-the-eseutil-tool-in-exchange-2013.md)
    

