---
title: 还原 Exchange 2013 数据库
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: e0804bb1-fd66-448a-b2cb-9ae2726ae888
description: 查找有关可用于还原 2013 数据库Exchange的信息。
ms.openlocfilehash: 522128026bcbef893ce4909174d3fd9a95f1e8a9
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513274"
---
# <a name="restoring-exchange-2013-databases"></a>还原 Exchange 2013 数据库

查找有关可用于还原 2013 数据库Exchange的信息。 
  
**适用于：Exchange Server** 2013 
  
2013 Exchange中包含的 Exchange Server 编写器使还原数据库Exchange一些灵活性。 通过使用 Exchange 2013 中的Exchange编写器，可以将卷影副本备份还原到以下位置：
  
- 原始数据库，无论数据库或事务日志文件路径配置是否已修改。
    
- 恢复数据库。
    
- 任何生产数据库，无论数据库是否显示名称 VSS 备份集的名称匹配。
    
当还原应用程序将信息还原到原始数据库时，必须将日志文件还原到在 Active Directory 域服务 (AD DS) 中为该数据库指定的目录路径。 如果应用程序将数据库还原到其他位置，则必须将日志文件还原到名为 **_restoredLogs** 的文件夹，该文件夹位于数据库日志文件目录中。 
  
当还原到与原始数据库不同的服务器或数据库时，还原应用程序必须确保提供给 VSS 的数据库目录路径与 AD DS 中的数据库目录路径相匹配。 您可以使用[get-MailboxDatabase](https://technet.microsoft.com/library/bb124924%28v=exchg.150%29.aspx)Exchange命令行管理程序 cmdlet 获取有关现有数据库的信息。 有关 Exchange 命令行管理程序的详细信息，请参阅 [Exchange 服务器 PowerShell (Exchange 命令行管理程序)](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps) 
  
下图显示了由卷影复制服务 Exchange VSS 管理的数据库的典型还原中的 (事件) 。
  
**图 1.还原数据库的事件序列**

![此图显示恢复过程的事件序列。该序列从 Exchange 存储启动开始，然后是继续经历 Exchange 编写器、VSS 和客户端应用程序之间的多个步骤。](media/VSS_StoreWriterRestore.gif)
  
## <a name="restoring-exchange-databases-to-the-original-location"></a>将Exchange数据库还原到原始位置
<a name="bk_OriginalLocation"> </a>

利用Exchange编写器，应用程序能够将数据库和事务日志文件还原到其服务器上Exchange位置。 默认情况下，Exchange编写器在请求者在[OnPostRestore](https://msdn.microsoft.com/library/windows/desktop/aa381566%28v=vs.85%29.aspx)操作期间确认还原已完成后重播事务日志文件。 还原应用程序必须使用 VSS [SetAdditionalRestores](https://msdn.microsoft.com/library/windows/desktop/aa382829%28v=vs.85%29.aspx) 方法来防止重播日志文件。 稍后，当管理员或应用程序重新安装还原的数据库Exchange可以重播日志文件。 
  
将数据库还原回其原始数据库对象 (以便数据库中的目标 GUID 与备份集) 中的目标 GUID 相匹配，但还原到不同的文件路径时，应用程序必须确定当前文件路径，将备份文件还原到数据库属性中指定的相应文件路径。 请求程序必须调用[AddNewTarget](https://msdn.microsoft.com/library/windows/desktop/aa382648%28v=vs.85%29.aspx)方法，才能向 Exchange 编写器传达文件还原的位置，然后编写器才能继续执行还原过程的其余部分。 如果未 **调用 AddNewTarget，Exchange** 编写器将假定备份还原到备份元数据文档中指定的文件路径。 
  
通常，应用程序无需为从 DAG 数据库可用性组或 DAG (副本执行的备份) 路径。 Exchange管理员通常不会更改数据库或日志文件路径。 但在 DAG 配置中，备份应用程序可能必须指定活动数据库和日志路径，因为 DAG 副本路径始终不同于这些路径。
  
请注意，Exchange 2013 不支持还原非活动 DAG 数据库副本。 只有在还原主动数据库副本时，才能从备份数据还原 DAG 副本。 使用不同的备份数据集或尝试还原数据库副本的子集可能会导致数据库无法装入。 在这种情况下，备份应用程序不需要调用 [SetRestoreOptions](https://msdn.microsoft.com/library/windows/desktop/aa382856%28v=vs.85%29.aspx) 函数，因为备份将还原到从中创建它们的原始数据库对象。 但是，如果备份应用程序调用 **SetRestoreOptions** 并且 XML 元数据文档具有正确的参数，则结果不是错误。 
  
## <a name="restoring-exchange-databases-to-a-recovery-database"></a>将Exchange还原到恢复数据库
<a name="bk_RecoveryDatabase"> </a>

利用Exchange编写器，您可以直接将数据还原到恢复数据库。 装载恢复的数据作为恢复数据库，Exchange管理员还原单个邮箱，甚至是邮箱中的单个项目。
  
如果恢复数据库已存在，则应用程序可以卸除该数据库，将数据还原到恢复数据库和日志文件，然后重新装入该数据库。
  
每台 Exchange 2013 服务器都只允许一次装入一个恢复数据库。 服务器可以包含磁盘空间允许的已恢复数据库，但只有一个数据库可以装入恢复数据库。 作为恢复数据库装入的数据库将计入一次可装入的最大数据库数。 作为服务器的恢复数据库装入的已恢复数据库不会以任何方式与原始邮箱关联。
  
若要恢复到恢复数据库，您的应用程序必须调用 [SetRestoreOptions](https://msdn.microsoft.com/library/windows/desktop/aa382856%28v=vs.85%29.aspx) 方法并提供一个指示源和目标数据库 GUID 的 XML 文档。 源 GUID 必须与备份集的 GUID 相匹配，并且目标 GUID 必须与 AD DS 中的目标数据库条目相匹配。 备份应用程序还必须调用 [AddNewTarget](https://msdn.microsoft.com/library/windows/desktop/aa382648%28v=vs.85%29.aspx) 方法来指定文件还原到的目录路径。 如果需要重命名数据库文件，则Exchange编写器将在[OnPostRestore](https://msdn.microsoft.com/library/windows/desktop/aa381566%28v=vs.85%29.aspx)操作期间重命名数据库。 Exchange事务日志文件必须还原到子文件夹 **(_restoredLogs)** 当前事务日志文件文件夹。 如果日志文件还原到任何其他位置，则Exchange编写器将返回错误。 由于作为恢复数据库装入的数据库不会还原到其原始位置，因此需要先将其恢复到干净关闭状态，然后才能装入它们。 默认情况下，Exchange编写器将在还原后使所有还原的数据库进入干净关闭状态。 如果备份应用程序调用[SetAdditionalRestores](https://msdn.microsoft.com/library/windows/desktop/aa382829%28v=vs.85%29.aspx)方法，Exchange 编写器将不会重播日志文件，管理员或备份应用程序需要在装入数据库之前使数据库进入干净关闭状态。 
  
## <a name="restoring-exchange-databases-to-a-recovery-server"></a>将Exchange还原到恢复服务器
<a name="bk_RecoveryServer"> </a>

在某些情况下，您可能需要将备份集恢复到另一台服务器;例如，您可能需要将邮箱数据库移植到同一 Exchange 组织中另一个 Exchange 2013 服务器，以从灾难性服务器故障中恢复，或还原到生产环境之外的专用服务器以恢复邮箱和公用文件夹数据。 
  
在这些情况下，目标数据库的文件路径及其对象 GUID 不同于原始数据库的文件路径。 因此，您的应用程序必须调用带指示源和目标数据库信息的 XML 文档的 [SetRestoreOptions](https://msdn.microsoft.com/library/windows/desktop/aa382856%28v=vs.85%29.aspx) 方法，并调用 [AddNewTarget](https://msdn.microsoft.com/library/windows/desktop/aa382648%28v=vs.85%29.aspx) 方法以指定要还原到的备份文件的目录路径。 对于Exchange编写器，此还原与还原到恢复数据库相同。 有关详细信息，请参阅本文前面[Exchange将](restoring-exchange-2013-databases.md#bk_RecoveryDatabase)数据库还原到恢复数据库。 
  
## <a name="see-also"></a>另请参阅
<a name="bk_AdditionalResources"> </a>

- [Exchange 2013 的备份操作类型](types-of-backup-operations-for-exchange-2013.md)
    
- [构建适用于 Exchange 2013 的备份和还原应用程序](build-backup-and-restore-applications-for-exchange-2013.md)
    
- [Exchange 2013 的备份和还原概念](backup-and-restore-concepts-for-exchange-2013.md)
    
- [CChkSGFiles 类参考](cchksgfiles-class-reference.md)
    

