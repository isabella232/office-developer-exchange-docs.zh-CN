---
title: 还原 Exchange 2013 数据库
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e0804bb1-fd66-448a-b2cb-9ae2726ae888
description: 查找有关您可以还原 Exchange 2013 数据库以不同方式的信息。
ms.openlocfilehash: d3ca3a884b0ad30f7d7968a9ed435b02aaf205e1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19752717"
---
# <a name="restoring-exchange-2013-databases"></a>还原 Exchange 2013 数据库

查找有关您可以还原 Exchange 2013 数据库以不同方式的信息。 
  
**适用于：** Exchange Server 2013 
  
是包含在 Exchange Server 2013 中如何还原 Exchange 数据库的一些灵活性允许 Exchange 编写器。 在 Exchange 2013 中使用 Exchange 编写器，您可以将卷影副本备份还原到以下位置：
  
- 原始数据库，而不管是否已修改的数据库或事务日志文件路径配置。
    
- 恢复数据库。
    
- 任何生产数据库，而不管是否数据库显示名称匹配中的 VSS 备份集的名称。
    
当您还原应用程序还原到原始数据库的信息时，日志文件必须将还原到 Active Directory 域服务 (AD DS) 中指定的目录路径该数据库。 如果您的应用程序将数据库还原到不同的位置，必须将日志文件还原到名为 **_restoredLogs**内数据库日志文件目录位于的文件夹中。 
  
当还原到服务器或不同于原始数据库的数据库，您还原应用程序必须确保提供给 VSS 的数据库目录路径与匹配那些 AD DS 中。 可以使用[Get-mailboxdatabase](http://technet.microsoft.com/en-us/library/bb124924%28v=exchg.150%29.aspx)Exchange Management Shell cmdlet 以获取有关现有数据库的信息。 有关 Exchange 命令行管理程序的详细信息，请参阅[Exchange Server PowerShell (Exchange Management Shell)](https://docs.microsoft.com/en-us/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)。 
  
下图显示典型 Exchange 数据库管理的卷影复制服务 (VSS) 还原中的事件顺序。
  
**图 1。还原数据库的事件顺序**

![此图显示恢复过程的事件序列。该序列从 Exchange 存储启动开始，然后是继续经历 Exchange 编写器、VSS 和客户端应用程序之间的多个步骤。](media/VSS_StoreWriterRestore.gif)
  
## <a name="restoring-exchange-databases-to-the-original-location"></a>Exchange 数据库还原到原始位置
<a name="bk_OriginalLocation"> </a>

Exchange 书写器使应用程序还原到其原始位置的 Exchange 服务器上的数据库和事务日志文件。 默认情况下，Exchange 书写器重播事务日志文件后申请者确认[OnPostRestore](http://msdn.microsoft.com/en-us/library/windows/desktop/aa381566%28v=vs.85%29.aspx)操作期间已完成还原。 还原应用程序必须使用 VSS [SetAdditionalRestores](http://msdn.microsoft.com/en-us/library/windows/desktop/aa382829%28v=vs.85%29.aspx)方法以避免在重播日志文件。 可以在以后当 Exchange 管理员或您的应用程序重新载入还原的数据库重播日志文件。 
  
当还原回其原始数据库的数据库对象 （例如，在数据库中的目标 Guid 匹配备份集中） 但的应用程序必须确定当前的文件路径和到将备份文件还原到不同的文件路径在数据库属性中指定相应的文件路径。 请求者必须调用[AddNewTarget](http://msdn.microsoft.com/en-us/library/windows/desktop/aa382648%28v=vs.85%29.aspx)方法进行通信到 Exchange 编写器之前作者可以继续还原过程的其余部分，其中还原文件的位置。 如果未调用**AddNewTarget** ，Exchange 书写器假定，将备份还原到备份元数据文档中指定的文件路径。 
  
通常情况下，您的应用程序不必指定从数据库可用性组 (DAG) 复制执行的备份的新路径。 Exchange 管理员通常不会更改数据库或日志文件路径。 在 DAG 配置中，但是，备份应用程序可能需要指定活动数据库和日志路径，因为始终这些路径不同 DAG 的复制路径。
  
请注意，Exchange 2013 不支持还原非活动 DAG 数据库副本。 仅当还原主动数据库副本时，可以从备份数据还原 DAG 副本。 使用不同的备份数据集或尝试还原的数据库副本的子集可能会导致要成为均不可装入的数据库。 备份应用程序无需调用[SetRestoreOptions](http://msdn.microsoft.com/en-us/library/windows/desktop/aa382856%28v=vs.85%29.aspx)函数在这种情况下，因为备份还原到原始数据库对象从创建它们。 但是，如果在备份应用程序调用**SetRestoreOptions**和 XML 元数据文档具有正确的参数，结果不是错误。 
  
## <a name="restoring-exchange-databases-to-a-recovery-database"></a>Exchange 数据库还原到恢复数据库
<a name="bk_RecoveryDatabase"> </a>

Exchange 书写器，您可以直接向恢复数据库还原数据。 为恢复数据库恢复的数据装载允许 Exchange 管理员还原单个邮箱和邮箱中的甚至是单个项目。
  
如果恢复数据库已存在，您的应用程序可以卸除数据库还原到恢复的数据库和日志文件的数据，然后重新装入数据库。
  
每个 Exchange 2013 服务器允许装入一次只有一个恢复数据库。 服务器可以包含多个已恢复的数据库磁盘空间允许，但可以作为恢复数据库装载只有一个。 为恢复数据库装入的数据库计数中可以一次装入的数据库的最大数目。 恢复的数据库装入，服务器恢复数据库不与任何方式中的原始邮箱相关联。
  
若要恢复的数据库恢复，您的应用程序必须调用[SetRestoreOptions](http://msdn.microsoft.com/en-us/library/windows/desktop/aa382856%28v=vs.85%29.aspx)方法并提供 XML 文档指示源和目标数据库的 Guid。 源 Guid 必须匹配从备份集，并且目标 Guid 必须匹配 AD DS 中的目标数据库条目。 备份应用程序还必须调用[AddNewTarget](http://msdn.microsoft.com/en-us/library/windows/desktop/aa382648%28v=vs.85%29.aspx)方法可指定将文件还原到其中的目录路径。 如果需要重命名的数据库文件，因此 Exchange 书写器[OnPostRestore](http://msdn.microsoft.com/en-us/library/windows/desktop/aa381566%28v=vs.85%29.aspx)操作过程中将重命名数据库。 Exchange 需要当前的事务日志文件路径下的事务日志文件还原到的子文件夹 ( **_restoredLogs**)。 如果日志文件还原到其他任何位置，Exchange 作者将返回错误。 正在为恢复数据库装入的数据库不还原到其原始位置中，因为他们需要之前可以装载放入干净关闭状态。 默认情况下，Exchange 作者将所有还原的数据库置于干净关闭状态期间还原后。 如果备份应用程序调用[SetAdditionalRestores](http://msdn.microsoft.com/en-us/library/windows/desktop/aa382829%28v=vs.85%29.aspx)方法，Exchange 编写器将不会重播日志文件，并且管理员或备份应用程序需要数据库置于干净关闭状态之前安装数据库。 
  
## <a name="restoring-exchange-databases-to-a-recovery-server"></a>Exchange 数据库还原到恢复服务器
<a name="bk_RecoveryServer"> </a>

在某些情况下，您可能需要将设置为另一台服务器; 备份恢复例如，您可能需要迁移到另一个 Exchange 2013 服务器，在同一 Exchange 组织的邮箱数据库恢复灾难性服务器故障或还原到生产环境，要恢复的邮箱外的专用服务器和公用文件夹数据。 
  
在这些情况下，是不同于原始数据库的目标数据库，以及其对象 Guid 的文件路径。 因此，您的应用程序必须调用具有指示的源和目标数据库信息和呼叫[AddNewTarget](http://msdn.microsoft.com/en-us/library/windows/desktop/aa382648%28v=vs.85%29.aspx)方法可以指定的目录路径还原到备份文件的 XML 文档的[SetRestoreOptions](http://msdn.microsoft.com/en-us/library/windows/desktop/aa382856%28v=vs.85%29.aspx)方法. Exchange writer，此还原将还原到恢复数据库相同。 有关详细信息，请参阅上文中的[恢复数据库还原 Exchange 数据库](restoring-exchange-2013-databases.md#bk_RecoveryDatabase)。 
  
## <a name="see-also"></a>另请参阅
<a name="bk_AdditionalResources"> </a>

- [Exchange 2013 的备份操作的类型](types-of-backup-operations-for-exchange-2013.md)
    
- [构建备份和还原 Exchange 2013 的应用程序](build-backup-and-restore-applications-for-exchange-2013.md)
    
- [Exchange 2013 的备份和还原概念](backup-and-restore-concepts-for-exchange-2013.md)
    
- [CChkSGFiles 类参考 （英文）](cchksgfiles-class-reference.md)
    

