---
title: Exchange 2013 Exchange编写器
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: ec126433-9f0a-46ec-a685-ff4af2f97bc1
description: 查找有关 Exchange 2013 Exchange备份和还原操作的信息。
ms.openlocfilehash: 7c50c2aa014308b05bdbc1acf0f2a91e33717ed6
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516235"
---
# <a name="exchange-writer-in-exchange-2013"></a>Exchange 2013 Exchange编写器

查找有关 Exchange 2013 Exchange备份和还原操作的信息。 
  
**适用于：Exchange Server** 2013 
  
Exchange编写器负责备份和还原活动 Exchange Server 2013 数据库。 该Exchange编写器还支持所选数据库的备份功能，其中卷影副本针对数据库和事务日志文件的复制实例进行。 
  
## <a name="overview-of-the-exchange-writer"></a>编写器Exchange概述
<a name="bk_Overview"> </a>

Exchange 2013 包括数据库移动功能，这些功能使数据库可以在不同的 Exchange 服务器之间复制，以提高数据库可用性和站点恢复能力。 数据库可用性组 (DAG) 中的其他数据库副本为 Exchange 备份提供了一个有价值的机会，以便使用副本位置可用的额外资源。 此外，由于备份的是副本而不是活动数据库主机，因此备份期间该副本在较长时间内可能不可用。 
  
Exchange 编写器代表请求程序) 与 Exchange 服务 (进行协调以准备数据库文件进行备份，在备份数据库之前冻结由 Exchange 事务导致的 IO 活动，然后在备份完成后解除冻结和截断日志文件。
  
在还原过程中，备份和还原应用程序会指示 Exchange 编写器代表请求程序) 与 Exchange 存储 (进行协调，以验证还原目标、重命名数据库文件（如有必要）然后根据需要重播事务日志。 该Exchange编写器支持备份和还原。
  
在Exchange邮箱服务器角色的任何 Exchange 服务器上，都可用该编写器。 
  
## <a name="exchange-writer-configuration-settings"></a>Exchange编写器配置设置
<a name="bk_ExchangeWriterConfig"> </a>

VSS Exchange编写器使用各种设置和值，在备份和还原操作过程中必须正确设置和保留这些设置和值。 这些配置设置存储在Exchange元数据文档中。 如果备份应用程序不保留这些设置，则当您尝试备份数据库时，可能会遇到意外Exchange错误。 
  
下表列出了公开有关数据库备份组件的元数据的 VSS 接口。 若要获取用于执行Exchange存储备份的编写器元数据文档，需要这些接口Exchange文档。
  
**表 1.VSS 接口**

|**VSS 接口**|**说明**|
|:-----|:-----|
|IVssWMComponent  <br/> |允许访问存储在编写器中的组件Exchange信息。  <br/> |
|IVssExwriterWriterMetadata  <br/> |允许请求备份和还原应用程序检查数据库编写器Exchange元数据。 Exchange编写器元数据文档包含Exchange备份和还原应用程序所需的特定于 2013 的值和参数，以便它可以正确指定相应的备份组件。  <br/> |
|IVssComponent  <br/> |包含用于检查和修改有关请求者备份组件文档中包含的组件的信息的方法。 只能为已经由 [IVssBackupComponents：：AddComponent](https://msdn.microsoft.com/library/windows/desktop/aa382646%28v=vs.85%29.aspx) 方法显式添加到此文档中的组件获取对象。  <br/> |
|IVssBackupComponents  <br/> |由请求备份和还原应用程序用于轮询Exchange文件状态的信息以及运行备份和还原操作。 [IVssBackupComponents：：SetBackupState](https://msdn.microsoft.com/library/windows/desktop/aa382833%28v=vs.85%29.aspx)方法定义备份操作是完整备份、复制备份、增量备份还是差异备份。 [IVssBackupComponents：：AddRestoreSubcomponent](https://msdn.microsoft.com/library/windows/desktop/aa382649%28v=vs.85%29.aspx)方法定义可针对还原操作选择的 Exchange 2013 数据库的子组件。  <br/> |
   
在 Windows Server 文件系统中，Exchange 2013 数据库存储为扩展名 *.edb 的单个数据库文件。Exchange 编写器将 *.edb** 公开为数据库组件，而事务日志 (.log) 和检查点文件 (.chk) 将组合到一个组件中，称为日志组件。 有关数据库文件Exchange，请参阅 Backup and [restore concepts for Exchange 2013。](backup-and-restore-concepts-for-exchange-2013.md)
  
## <a name="interactions-between-the-exchange-writer-vss-and-vss-requesters"></a>编写器Exchange VSS 和 VSS 请求程序之间的交互
<a name="bk_interactions"> </a>

在备份操作期间，VSS、Exchange编写器与 Exchange 2013 之间的高级交互如下所示：
  
1. 备份程序（或代理）运行一项计划作业。 
    
2. 备份和还原应用程序中的 VSS 请求程序向 VSS 发送命令，以拍摄所选 Exchange 2013 数据库的卷影副本。 
    
3. VSS 与 Exchange 编写器进行通信，以准备快照备份。 Exchange 2013 禁止对数据库执行管理操作，检查卷相关性，并暂停对所选数据库实例和事务日志文件的所有写入操作，同时允许只读访问。 
    
4. VSS 与相应的存储提供程序通信，以创建存储卷的卷影副本，其中包含 Exchange 2013 数据库。 
    
5. VSS 2013 Exchange 2013 版恢复普通操作。 
    
6. VSS 请求程序在发出备份成功信号之前验证备份集的物理一致性。 Exchange 2013 年 10 月会截断事务日志 (如果数据库是 DAG 的一部分，日志截断将在) 所有副本之间复制，并记录数据库上次备份的时间。
    
VSS 序列化请求者与 Exchange 编写器之间的交互，从[OnPrepareBackup](https://msdn.microsoft.com/library/windows/desktop/aa381571%28v=vs.85%29.aspx)方法开始，以[OnPostSnapshot](https://msdn.microsoft.com/library/windows/desktop/aa381568%28v=vs.85%29.aspx)方法结束。 通常，Exchange编写器使用卷影副本所花的大多数时间发生在 **OnPostSnapshot** 方法之后，在备份完成之前验证卷影副本的一致性。 该Exchange编写器支持 **OnPostSnapshot** 和 [OnBackupComplete 之间的并行备份](https://msdn.microsoft.com/library/windows/desktop/aa381557%28v=vs.85%29.aspx)。
  
Exchange 2013 不允许对同一数据库进行并发备份。 一次只能对给定数据库运行一个备份作业。 当备份运行时，Exchange存储会将数据库置于备份正在进行状态。 在完成备份过程或重新启动服务时，将清除此内存中状态。 当承载 Exchange 编写器的服务重新启动、重新启动操作系统或发生群集故障转移时，内存中的正在进行备份的状态及其关联数据将丢失。 任何这些事件都将导致备份作业失败。
  
基于要执行的日志文件，触发由备份启动的事务处理和截断。 在非 DAG 配置中，Exchange编写器将在完整备份或增量备份完成时截断事务日志文件。 在 DAG 复制配置中，日志截断将被复制服务延迟，直到所有必要的日志文件重播到所有其他副本中。 在确认日志文件已成功应用于复制数据库，并且活动数据库和数据库副本检查点已传递要删除的日志文件后，复制服务将从活动路径和复制 日志文件 路径中删除备份的日志文件。
  
## <a name="see-also"></a>另请参阅

- [Exchange 2013 中用于备份和还原的事务日志和检查点文件](transaction-logs-and-checkpoint-files-for-backup-and-restore-in-exchange.md)
    
- [Exchange 2013 的备份和还原概念](backup-and-restore-concepts-for-exchange-2013.md)
    

