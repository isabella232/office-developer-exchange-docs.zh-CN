---
title: Exchange 2013 中的 Exchange 编写器
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ec126433-9f0a-46ec-a685-ff4af2f97bc1
description: 查找有关 Exchange 书写器信息 Exchange 2013 中备份和还原操作。
ms.openlocfilehash: a4dc5963ab24a83969efc6e425b38a35276f3aa3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19752684"
---
# <a name="exchange-writer-in-exchange-2013"></a>Exchange 2013 中的 Exchange 编写器

查找有关 Exchange 书写器信息 Exchange 2013 中备份和还原操作。 
  
**适用于：** Exchange Server 2013 
  
Exchange 作者负责备份和还原 Exchange Server 2013 中的活动数据库。 Exchange 书写器还支持其中卷影副本针对采取复制实例的数据库和事务日志文件的所选的数据库的备份功能。 
  
## <a name="overview-of-the-exchange-writer"></a>Exchange 书写器的概述
<a name="bk_Overview"> </a>

Exchange 2013 包括数据库移动功能，以便在不同的 Exchange 服务器，以提高数据库可用性和站点恢复之间复制的数据库。 其他数据库副本的数据库可用性组 (DAG) 提供 Exchange 备份使用额外的资源的副本位置提供的重要机会。 此外，而不是活动数据库主控形状副本备份，因为副本的不会备份期间长的时间段。 
  
Exchange 书写器配合 （代表申请者操作系统） 的 Exchange 服务来准备备份的数据库文件、 冻结 IO 活动生成 Exchange 事务之前备份数据库，然后取消冻结和截断备份完成后，则日志文件。
  
在还原期间，您的备份和还原应用程序指示要与 Exchange 存储 （代表申请者操作系统） 协调，以验证还原目标，重命名数据库文件，如有必要，然后重播事务的 Exchange 编写器根据需要日志。 Exchange 编写器支持的备份和恢复。
  
Exchange 编写器任何安装了邮箱服务器角色的 Exchange 服务器上可用。 
  
## <a name="exchange-writer-configuration-settings"></a>Exchange 编写器配置设置
<a name="bk_ExchangeWriterConfig"> </a>

Exchange writer for VSS 使用各种设置和必须正确设置和备份和还原操作过程中保留的值。 这些配置设置存储在 Exchange 编写器元数据文档。 如果备份应用程序不会保留这些设置，您可能会遇到意外的错误，当您尝试备份 Exchange 数据库时。 
  
下表列出了公开有关数据库备份的组件的元数据的 VSS 接口。 这些接口所需获取 Exchange 编写器元数据文档用于执行 Exchange 存储的备份。
  
**表 1。VSS 接口**

|**VSS 接口**|**说明**|
|:-----|:-----|
|IVssWMComponent  <br/> |允许访问存储在 Exchange 书写器的组件信息。  <br/> |
|IVssExamineWriterMetadata  <br/> |允许请求的备份和还原应用程序检查 Exchange 编写器元数据。 Exchange 编写器元数据文档包含特定于 Exchange 2013 的值和请求的备份和还原应用程序需要，以便它可以正确指定相应的组件备份的参数。  <br/> |
|IVssComponent  <br/> |包含用于检查和修改有关请求者的备份的组件文档中包含的组件的信息的方法。 仅获取对象已明确添加到此文档[IVssBackupComponents::AddComponent](http://msdn.microsoft.com/en-us/library/windows/desktop/aa382646%28v=vs.85%29.aspx)方法这些组件。  <br/> |
|IVssBackupComponents  <br/> |用于请求的备份和还原应用程序轮询 Exchange 作者有关文件状态和运行备份和还原操作。 [IVssBackupComponents::SetBackupState](http://msdn.microsoft.com/en-us/library/windows/desktop/aa382833%28v=vs.85%29.aspx)方法定义的备份操作是否是完整，复制，增量备份或差异备份。 [IVssBackupComponents::AddRestoreSubcomponent](http://msdn.microsoft.com/en-us/library/windows/desktop/aa382649%28v=vs.85%29.aspx)方法定义可选择用于还原操作的 Exchange 2013 数据库的子组件。  <br/> |
   
在 Windows Server 文件系统中，Exchange 2013 数据库存储为单个数据库文件扩展名 *.edb。Exchange 编写器公开 *.edb 作为数据库组件，同时事务日志 (*.log) 和检查点文件 (*.chk) 合并为单个组件，称为日志组件。 有关 Exchange 数据库文件的详细信息，请参阅[Exchange 2013 的备份和还原概念](backup-and-restore-concepts-for-exchange-2013.md)。
  
## <a name="interactions-between-the-exchange-writer-vss-and-vss-requesters"></a>Exchange 编写器、 VSS 和 VSS 之间的交互请求者
<a name="bk_interactions"> </a>

Exchange 作者，VSS 之间的高级交互期间备份操作的 Exchange 2013，如下所示，：
  
1. 备份程序（或代理）运行一项计划作业。 
    
2. 备份和还原应用程序中的 VSS 请求者向所选的 Exchange 2013 数据库卷影副本的 VSS 发送命令。 
    
3. VSS 与要准备快照备份的 Exchange 编写器进行通信。 Exchange 2013 禁止针对数据库的管理操作和检查卷依赖项，同时允许在只读访问挂起到所选实例的数据库和事务日志文件的所有写操作。 
    
4. VSS 与适当的存储提供程序创建包含 Exchange 2013 数据库的存储卷的卷影副本进行通信。 
    
5. VSS 发布 Exchange 2013，以恢复普通操作。 
    
6. VSS 请求者验证物理信号备份已成功之前设置的备份的一致性。 Exchange 2013 截断事务日志 （如果数据库是 DAG 的一部分，日志截断复制所有副本之间），并记录数据库的上次备份的时间。
    
VSS 序列化与 Exchange 书写器[OnPrepareBackup](http://msdn.microsoft.com/en-us/library/windows/desktop/aa381571%28v=vs.85%29.aspx)方法使用起始和结束与[OnPostSnapshot](http://msdn.microsoft.com/en-us/library/windows/desktop/aa381568%28v=vs.85%29.aspx)方法的请求者的交互。 通常情况下，Exchange 书写器等待使用卷影副本的时间的大部分时发生**OnPostSnapshot**方法之后, 的卷影副本一致性验证之前完成的备份。 Exchange 书写器支持并行**OnPostSnapshot**和[OnBackupComplete](http://msdn.microsoft.com/en-us/library/windows/desktop/aa381557%28v=vs.85%29.aspx)之间的备份。
  
Exchange 2013 不允许并发的同一个数据库的备份。 只有一个备份作业可以针对给定数据库运行一次。 当运行备份时，在 Exchange 存储会将数据库置于备份正在进行中状态。 在完成的备份过程或重新启动该服务，此内存中状态为清除状态。 承载的 Exchange 编写器服务重新启动后，重新启动操作系统后，或进行故障转移群集时，内存中备份正在进行中状态和其关联的数据将丢失。 任何这些事件将导致失败的备份作业。
  
备份启动事务日志文件截断触发根据要执行备份的类型。 在非 DAG 配置 Exchange 作者将截断事务日志文件的完整或增量备份成功完成。 在 DAG 复制配置，将复制服务延迟日志截断，直到所有必要的日志文件被重播到所有其他副本。 复制服务备份日志文件从活动和复制日志文件路径，日志文件已成功应用到复制数据库和两个活动数据库和数据库副本检查点已通过验证后将删除备份要删除的日志文件。
  
## <a name="see-also"></a>另请参阅

- [事务日志和备份和还原 Exchange 2013 中的检查点文件](transaction-logs-and-checkpoint-files-for-backup-and-restore-in-exchange.md)
    
- [Exchange 2013 的备份和还原概念](backup-and-restore-concepts-for-exchange-2013.md)
    

