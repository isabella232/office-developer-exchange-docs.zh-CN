---
title: 还原 Exchange 2013 数据库
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e0804bb1-fd66-448a-b2cb-9ae2726ae888
description: 查找有关可还原 Exchange 2013 数据库的不同方法的信息。
ms.openlocfilehash: 9fe417bda5dc728af619da02d62ada6e920f731d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528670"
---
# <a name="restoring-exchange-2013-databases"></a>还原 Exchange 2013 数据库

查找有关可还原 Exchange 2013 数据库的不同方法的信息。 
  
**适用于：** Exchange Server 2013 
  
Exchange Server 2013 中包含的 Exchange 编写器可为您还原 Exchange 数据库的方式提供一些灵活性。 通过使用 Exchange 2013 中的 Exchange 编写器，可以将卷影副本备份还原到以下位置：
  
- 原始数据库，无论数据库或事务日志文件路径配置是否已修改。
    
- 恢复数据库。
    
- 任何生产数据库，而不管数据库显示名称是否与 VSS 备份集内的名称相匹配。
    
当还原应用程序将信息还原到原始数据库时，必须将日志文件还原到该数据库的 Active Directory 域服务（AD DS）中指定的目录路径。 如果应用程序将数据库还原到其他位置，则必须将日志文件还原到位于数据库日志文件目录内的名为 **_restoredLogs**的文件夹中。 
  
当还原到与原始数据库不同的服务器或数据库时，还原应用程序必须确保提供给 VSS 的数据库目录路径与 AD DS 中的路径相匹配。 您可以使用[Set-mailboxdatabase](https://technet.microsoft.com/library/bb124924%28v=exchg.150%29.aspx)Exchange 命令行管理程序 cmdlet 来获取有关现有数据库的信息。 有关 Exchange 命令行管理程序的详细信息，请参阅[Exchange Server PowerShell （Exchange 命令行管理程序）](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)。 
  
下图显示了由卷影复制服务（VSS）管理的 Exchange 数据库的典型还原中的事件序列。
  
**图1。还原数据库的事件的顺序**

![此图显示恢复过程的事件序列。该序列从 Exchange 存储启动开始，然后是继续经历 Exchange 编写器、VSS 和客户端应用程序之间的多个步骤。](media/VSS_StoreWriterRestore.gif)
  
## <a name="restoring-exchange-databases-to-the-original-location"></a>将 Exchange 数据库还原到原始位置
<a name="bk_OriginalLocation"> </a>

Exchange 编写器使应用程序能够将数据库和事务日志文件还原到其在 Exchange 服务器上的原始位置。 默认情况下，在请求者确认在[OnPostRestore](https://msdn.microsoft.com/library/windows/desktop/aa381566%28v=vs.85%29.aspx)操作过程中完成还原后，Exchange 编写器将重播事务日志文件。 还原应用程序必须使用 VSS [SetAdditionalRestores](https://msdn.microsoft.com/library/windows/desktop/aa382829%28v=vs.85%29.aspx)方法来阻止重播日志文件。 以后，当 Exchange 管理员或应用程序 remounts 还原的数据库时，可以重播日志文件。 
  
将数据库还原回其原始数据库对象时（如果数据库中的目标 Guid 与备份集中的 Guid 相匹配），但对于不同的文件路径，应用程序必须确定当前文件路径，并将备份文件还原到数据库属性中指定的相应文件路径。 请求者必须调用[AddNewTarget](https://msdn.microsoft.com/library/windows/desktop/aa382648%28v=vs.85%29.aspx)方法以与 Exchange 编写器通信，以便在作者可以继续执行其余还原过程之前，还原文件的位置。 如果未调用**AddNewTarget** ，则 Exchange 编写器将假定将备份还原到备份元数据文档中指定的文件路径。 
  
通常情况下，您的应用程序不必为从数据库可用性组（DAG）副本执行的备份指定新路径。 Exchange 管理员通常不会更改数据库或日志文件路径。 但是，在 DAG 配置中，备份应用程序可能必须指定活动的数据库和日志路径，因为 DAG 复制路径始终不同于这些路径。
  
请注意，Exchange 2013 不支持还原非活动的 DAG 数据库副本。 仅当还原了主动数据库副本时，才能从备份数据还原 DAG 副本。 使用不同的备份数据集或尝试还原数据库副本的子集可能导致数据库变得无法装入。 在这种情况下，备份应用程序不必调用[SetRestoreOptions](https://msdn.microsoft.com/library/windows/desktop/aa382856%28v=vs.85%29.aspx)函数，因为备份会还原到创建它们的原始数据库对象。 但是，如果备份应用程序调用**SetRestoreOptions** ，并且 XML 元数据文档具有正确的参数，则结果不是错误。 
  
## <a name="restoring-exchange-databases-to-a-recovery-database"></a>将 Exchange 数据库还原到恢复数据库
<a name="bk_RecoveryDatabase"> </a>

Exchange 编写器使您能够将数据直接还原到恢复数据库。 将恢复的数据作为恢复数据库装载，可以使 Exchange 管理员能够还原单个邮箱甚至邮箱中的单个项目。
  
如果已存在恢复数据库，则应用程序可以卸除数据库，将数据还原到恢复数据库和日志文件，然后重新装入数据库。
  
每个 Exchange 2013 服务器允许一次仅装入一个恢复数据库。 服务器可以包含任意数量的已恢复数据库，因为磁盘空间允许，但只能将其中一个装载为恢复数据库。 装载为恢复数据库的数据库将被计算为可一次装入的最大数据库数。 作为服务器的恢复数据库挂载的恢复的数据库不会以任何方式与原始邮箱相关联。
  
若要恢复到恢复数据库，您的应用程序必须调用[SetRestoreOptions](https://msdn.microsoft.com/library/windows/desktop/aa382856%28v=vs.85%29.aspx)方法，并提供一个指示源和目标数据库 GUID 的 XML 文档。 源 Guid 必须与备份集中的 Guid 相匹配，且目标 Guid 必须与 AD DS 中的目标数据库条目相匹配。 备份应用程序还必须调用[AddNewTarget](https://msdn.microsoft.com/library/windows/desktop/aa382648%28v=vs.85%29.aspx)方法来指定将文件还原到的目录路径。 如果需要重命名数据库文件，Exchange 编写器将在[OnPostRestore](https://msdn.microsoft.com/library/windows/desktop/aa381566%28v=vs.85%29.aspx)操作过程中重命名数据库。 Exchange 要求将事务日志文件还原到当前事务日志文件路径下的子文件夹（ **_restoredLogs**）。 如果将日志文件还原到任何其他位置，则 Exchange 编写器将返回错误。 由于要作为恢复数据库而装载的数据库不会还原到其原始位置，因此需要将这些数据库置于干净关闭状态，然后才能装入它们。 默认情况下，在还原后，Exchange 编写器会将所有还原的数据库置于干净关闭状态。 如果备份应用程序调用[SetAdditionalRestores](https://msdn.microsoft.com/library/windows/desktop/aa382829%28v=vs.85%29.aspx)方法，则 Exchange 编写器将不会重播日志文件，管理员或备份应用程序需要在挂载数据库之前将数据库置于干净关闭状态。 
  
## <a name="restoring-exchange-databases-to-a-recovery-server"></a>将 Exchange 数据库还原到恢复服务器
<a name="bk_RecoveryServer"> </a>

在某些情况下，您可能需要将备份集恢复到另一台服务器上;例如，您可能需要将邮箱数据库迁移到同一 Exchange 组织中的另一台 Exchange 2013 服务器，或还原到生产环境外部的专用服务器以恢复邮箱和公用文件夹数据，从而从灾难性的服务器故障中恢复。 
  
在这些方案中，目标数据库的文件路径及其对象 Guid 与原始数据库的不同。 因此，您的应用程序必须使用 XML 文档调用[SetRestoreOptions](https://msdn.microsoft.com/library/windows/desktop/aa382856%28v=vs.85%29.aspx)方法，该文档指明源和目标数据库信息，并调用[AddNewTarget](https://msdn.microsoft.com/library/windows/desktop/aa382648%28v=vs.85%29.aspx)方法来指定要将备份文件还原到的目录路径。 对于 Exchange 编写器，此还原与还原到恢复数据库相同。 有关详细信息，请参阅本文前面的[将 Exchange 数据库还原到恢复数据库](restoring-exchange-2013-databases.md#bk_RecoveryDatabase)。 
  
## <a name="see-also"></a>另请参阅
<a name="bk_AdditionalResources"> </a>

- [Exchange 2013 的备份操作类型](types-of-backup-operations-for-exchange-2013.md)
    
- [为 Exchange 2013 生成备份和还原应用程序](build-backup-and-restore-applications-for-exchange-2013.md)
    
- [Exchange 2013 的备份和还原概念](backup-and-restore-concepts-for-exchange-2013.md)
    
- [CChkSGFiles 类参考](cchksgfiles-class-reference.md)
    

