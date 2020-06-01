---
title: Exchange 2013 中的 exchange 编写器
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ec126433-9f0a-46ec-a685-ff4af2f97bc1
description: 查找有关用于备份和还原操作的 Exchange 2013 中的 Exchange 编写器的信息。
ms.openlocfilehash: 44270a87c38b08d274d389fa6e46f3864da13ed2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44452886"
---
# <a name="exchange-writer-in-exchange-2013"></a>Exchange 2013 中的 exchange 编写器

查找有关用于备份和还原操作的 Exchange 2013 中的 Exchange 编写器的信息。 
  
**适用于：** Exchange Server 2013 
  
Exchange 编写器负责备份和还原活动 Exchange Server 2013 数据库。 Exchange 编写器还支持所选数据库的备份功能，其中卷影副本针对数据库和事务日志文件的复制实例进行。 
  
## <a name="overview-of-the-exchange-writer"></a>Exchange 编写器概述
<a name="bk_Overview"> </a>

Exchange 2013 包括数据库移动功能，这些功能使数据库能够在不同的 Exchange 服务器之间进行复制，以提高数据库可用性和站点恢复能力。 数据库可用性组（DAG）中的其他数据库副本为 Exchange 备份提供了可在副本位置使用的额外资源的有价值的机会。 此外，由于备份副本（而不是活动数据库主控形状），因此副本在备份期间可能会在更长时间内不可用。 
  
Exchange 编写器与 Exchange 服务协调（代表请求者进行操作）以准备用于备份的数据库文件，在备份数据库之前冻结 Exchange 事务产生的 IO 活动，然后在备份完成后取消冻结和截断日志文件。
  
在还原过程中，您的备份和还原应用程序指示 Exchange 编写器与 Exchange 存储区进行协调（代表请求者进行操作）以验证还原目标，如有必要，请重命名数据库文件，然后根据需要重放事务日志。 Exchange 编写器支持备份和还原。
  
Exchange 编写器在安装了邮箱服务器角色的任何 Exchange 服务器上均可用。 
  
## <a name="exchange-writer-configuration-settings"></a>Exchange 编写器配置设置
<a name="bk_ExchangeWriterConfig"> </a>

用于 VSS 的 Exchange 编写器使用在备份和还原操作过程中必须正确设置和保留的各种设置和值。 这些配置设置存储在 Exchange 编写器元数据文档中。 如果备份应用程序不保留这些设置，则在尝试备份 Exchange 数据库时可能会遇到意外错误。 
  
下表列出了公开有关数据库备份组件的元数据的 VSS 接口。 这些接口是获取用于执行 Exchange 存储备份的 Exchange 编写器元数据文档所必需的。
  
**表1。VSS 接口**

|**VSS 接口**|**说明**|
|:-----|:-----|
|IVssWMComponent  <br/> |允许访问存储在 Exchange 编写器中的组件信息。  <br/> |
|IVssExamineWriterMetadata  <br/> |允许请求的备份和还原应用程序检查 Exchange 编写器的元数据。 Exchange 编写器元数据文档包含请求的备份和还原应用程序所需的 Exchange 2013 特定的值和参数，以便可以正确指定用于备份的相应组件。  <br/> |
|IVssComponent  <br/> |包含检查和修改有关请求者的备份组件文档中包含的组件的信息的方法。 仅可为已通过[IVssBackupComponents：： AddComponent](https://msdn.microsoft.com/library/windows/desktop/aa382646%28v=vs.85%29.aspx)方法显式添加到此文档中的组件获取对象。  <br/> |
|IVssBackupComponents  <br/> |由请求的备份和还原应用程序用来轮询 Exchange 编写器，以轮询文件状态和运行备份和还原操作。 [IVssBackupComponents：： SetBackupState](https://msdn.microsoft.com/library/windows/desktop/aa382833%28v=vs.85%29.aspx)方法定义备份操作是完整备份、副本备份、增量备份还是差异备份。 [IVssBackupComponents：： AddRestoreSubcomponent](https://msdn.microsoft.com/library/windows/desktop/aa382649%28v=vs.85%29.aspx)方法定义可为还原操作选择的 Exchange 2013 数据库的子组件。  <br/> |
   
在 Windows Server 文件系统中，Exchange 2013 数据库存储为带有扩展名 .edb 的单个数据库文件 *。Exchange 编写器将 *.edb 公开为数据库组件，而事务日志（*.log）和检查点文件（*.chk）合并到一个组件（称为 "日志组件"）中。 有关 Exchange 数据库文件的详细信息，请参阅[exchange 2013 的备份和还原概念](backup-and-restore-concepts-for-exchange-2013.md)。
  
## <a name="interactions-between-the-exchange-writer-vss-and-vss-requesters"></a>Exchange 编写器、VSS 和 VSS 请求程序之间的交互
<a name="bk_interactions"> </a>

在备份操作过程中，VSS、Exchange 编写器和 Exchange 2013 之间的高级交互如下所示：
  
1. 备份程序（或代理）运行一项计划作业。 
    
2. 备份和还原应用程序中的 VSS 请求者将命令发送到 VSS，以拍摄选定的 Exchange 2013 数据库的卷影副本。 
    
3. VSS 与 Exchange 编写器进行通信以准备快照备份。 Exchange 2013 禁止对数据库执行管理操作，检查卷依赖项，并挂起对数据库和事务日志文件的选定实例的所有写入操作，同时允许只读访问。 
    
4. VSS 与相应的存储提供程序通信，以创建包含 Exchange 2013 数据库的存储卷的卷影副本。 
    
5. VSS 发布 Exchange 2013 以恢复普通操作。 
    
6. VSS 请求者在发出备份成功的信号之前验证备份集的物理一致性。 Exchange 2013 截断事务日志（如果数据库是 DAG 的一部分，则在所有副本中复制日志截断，并记录数据库的最后备份时间。
    
VSS 将请求者与 Exchange 编写器的交互序列化从[OnPrepareBackup](https://msdn.microsoft.com/library/windows/desktop/aa381571%28v=vs.85%29.aspx)方法开始，并以[OnPostSnapshot](https://msdn.microsoft.com/library/windows/desktop/aa381568%28v=vs.85%29.aspx)方法结束。 通常情况下，在完成备份之前，如果卷影副本的一致性被确认，则 Exchange 编写器在使用卷影副本时所花的时间将在**OnPostSnapshot**方法之后发生。 Exchange 编写器支持**OnPostSnapshot**和[OnBackupComplete](https://msdn.microsoft.com/library/windows/desktop/aa381557%28v=vs.85%29.aspx)之间的并行备份。
  
Exchange 2013 不允许对同一个数据库进行并发备份。 一次仅可对给定数据库运行一个备份作业。 在备份运行时，Exchange 存储会将数据库置于正在进行的备份状态。 此内存中的状态在备份过程完成或服务重新启动时清除。 当重新启动承载 Exchange 编写器的服务、重新启动操作系统或发生群集故障转移时，内存中的正在进行的备份状态及其关联的数据将会丢失。 这些事件中的任何一种都将导致备份作业失败。
  
根据要执行的备份类型触发备份启动的事务日志文件截断。 在非 DAG 配置中，Exchange 编写器将在完成成功的完整备份或增量备份时截断事务日志文件。 在 DAG 复制配置中，复制服务将延迟日志截断，直到将所有必要的日志文件重播到其他所有副本。 复制服务在验证日志文件是否已成功应用于复制数据库，并且两个活动数据库和数据库副本检查点都已传递要删除的日志文件后，将从主动和副本日志文件路径中删除备份的日志文件。
  
## <a name="see-also"></a>另请参阅

- [Exchange 2013 中用于备份和还原的事务日志和检查点文件](transaction-logs-and-checkpoint-files-for-backup-and-restore-in-exchange.md)
    
- [Exchange 2013 的备份和还原概念](backup-and-restore-concepts-for-exchange-2013.md)
    

