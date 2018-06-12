---
title: Exchange 2013 的备份和还原概念
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9a1c4709-9313-4ccf-9f8a-673a51d51f23
description: 查找有关 Exchange 数据库将帮助您创建备份和还原 Exchange 2013 的应用程序的信息。
ms.openlocfilehash: 5fa62c3d34ffbe8f0bab852c6d41c49220e2883a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19752693"
---
# <a name="backup-and-restore-concepts-for-exchange-2013"></a>Exchange 2013 的备份和还原概念

查找有关 Exchange 数据库将帮助您创建备份和还原 Exchange 2013 的应用程序的信息。
  
创建备份和还原 Exchange Server 2013 的应用程序之前，您应熟悉的 Exchange 数据库文件结构。 通过使用 Exchange 存储数据库文件，可以在存储备份数据，并在以后根据需要对其进行还原。 如果您受到磁盘空间，管理员可能实现循环日志记录，并这会影响您如何能够备份数据库。 您还可以在 Exchange 2013 能够备份和还原 Exchange 数据充分利用数据库移动功能。 良好的灾难恢复的冗余措施数据库移动，与备份和还原应用程序结合使用。

<a name="bk_exchangedatabases"> </a>

## <a name="exchange-store-database-files"></a>Exchange 存储数据库文件

Exchange 2013 包括支持最多 100 个数据库。 每个 Exchange 2013 数据库包含下表中列出的文件。 
  
**表 1。Exchange 2013 数据库文件**

|文件类型|扩展名|说明|
|:-----|:-----|:-----|
|数据库文件  <br/> |\*.edb  <br/> |记录已提交到内存中数据库的所有更改。  <br/> |
|事务日志流  <br/> |\*.log  <br/> |记录操作，例如创建或修改一条消息，将提交到数据库。 有限的大小为 1 MB。  <br/> |
|检查点文件  <br/> |\*.chk  <br/> |具有已记录事务记录写入到磁盘上的数据库文件。  <br/> |
   
Exchange 2013 维护一组的每个数据库的事务日志文件。 事务日志很重要的备份和恢复操作。 当您创建的备份和还原应用程序使用卷影复制服务 (VSS) 时，您必须确保正确处理这些日志。 有关详细信息，请参阅[事务日志和备份和还原 Exchange 2013 中的检查点文件](transaction-logs-and-checkpoint-files-for-backup-and-restore-in-exchange.md)。 若要备份数据库和其日志流，您必须备份整个卷包含数据库和日志。 量或文件夹，其中包含 Exchange 数据库的完整备份成功完成后才会执行日志截断。
  
在每个 Exchange 服务器上，您可以一次装载只有一个恢复数据库。 您可以使用 Exchange 命令行管理程序 cmdlet，如**New-mailboxrestorerequest**访问恢复数据库。 有关 Exchange 恢复数据库的详细信息，请参阅 TechNet 上的[恢复数据库](http://technet.microsoft.com/en-us/library/dd876954%28v=exchg.150%29.aspx)。 有关 Exchange 命令行管理程序 cmdlet 的详细信息，请参阅 TechNet 上的[Exchange 2013 Cmdlets](http://technet.microsoft.com/en-us/library/bb124413.aspx) 。 
  
## <a name="circular-logging"></a>循环日志记录
<a name="bk_circularlogging"> </a>

如果存储容量问题，您的管理员可能启用循环日志记录。 Exchange 启用循环日志记录后，将编写事务日志，像往常一样，但时检查点文件高级，被截断事务日志的非活动部分。 您的管理员应配置 Exchange 2013 数据库能够使用循环日志记录如果还计划使用 VSS 启用自定义备份和还原操作。 循环日志记录将创建以下限制： 
  
- 如果启用在备份或恢复操作过程，您无法还原的各个数据库。
    
- 可能是仅时间点恢复操作。 启用循环日志记录后，您可以删除位于同一目录中的事务日志恢复数据库后，尽管这些日志可能是不同的 Exchange 2013 数据库的一部分。 
    
- 不能执行增量备份或差异备份操作。 有关这些类型的备份的详细信息，请参阅[Exchange 2013 的备份操作的类型](types-of-backup-operations-for-exchange-2013.md)。
    
如果启用循环日志记录，您的管理员应禁用尽快以确保 VSS 备份不会失败。 有关详细信息，查看[Exchange 循环日志记录和 VSS 备份](http://blogs.technet.com/b/exchange/archive/2010/08/18/3410672.aspx)的博客张贴内容。 
  
## <a name="exchange-database-mobility"></a>Exchange 数据库移动
<a name="bk_exchangedatabasemobility"> </a>

Exchange 2013 允许以提高邮箱可靠性和可用性的数据库移动。 数据库移动，可以创建 Exchange 存储数据库的副本，数据库断开服务器，并将其存储在另一台服务器上。 在 Exchange 2013 数据库可用性组 (DAG)，不同的计算机上存储数据库的多个副本。 当一个或多个副本的数据库的硬件或其他系统故障由于丢失，来自其他副本信息可以用于重新设定种子通过普通复制操作的数据库。
  
为备份操作，如果在 DAG 中配置 Exchange 2013 的数据库要备份的备份应用程序可以更好地阻止快照和活动服务器的性能之间的干扰处于非活动状态之一上按照快照数据库副本。 因为大多数情况下同步的数据库副本，备份应用程序可以执行从不同的数据库副本快照和更高版本重建它从片段。
  
DAG 数据库还原备份数据的唯一受支持的方法是数据库的使用相同的备份数据还原所有副本。 由于数据库日志文件可能会稍有不同的副本副本之间，还原单独的数据库副本使用不同的数据可能会变得不可安装的数据库。
  
## <a name="in-this-section"></a>本节内容
<a name="bk_inthissection"> </a>

- [事务日志和备份和还原 Exchange 2013 中的检查点文件](transaction-logs-and-checkpoint-files-for-backup-and-restore-in-exchange.md)
    
- [Exchange 2013 中的 Exchange 编写器](exchange-writer-in-exchange-2013.md)
    
## <a name="see-also"></a>另请参阅

- [Exchange Online 和 Exchange 开发](../exchange-server-development.md) 
- [Exchange 2013 的备份操作的类型](types-of-backup-operations-for-exchange-2013.md)
- [还原 Exchange 2013 数据库](restoring-exchange-2013-databases.md)
    

