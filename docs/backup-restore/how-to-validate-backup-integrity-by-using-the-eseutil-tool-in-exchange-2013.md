---
title: 通过使用 Eseutil 工具在 Exchange 2013 中验证备份完整性
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b0d325ba-4482-4ca2-9a69-c890f985b206
description: 了解如何使用 Eseutil 命令行工具来验证 Exchange 存储的备份。
ms.openlocfilehash: 03c4c23d433418911240bbe7c337308a989f3739
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752683"
---
#  <a name="validate-backup-integrity-by-using-the-eseutil-tool-in-exchange-2013"></a>通过使用 Eseutil 工具在 Exchange 2013 中验证备份完整性

了解如何使用 Eseutil 命令行工具来验证 Exchange 存储的备份。 
  
**适用于：** Exchange Server 2013 
  
卷影复制服务 (VSS) 可以创建备份 Exchange 继续写入数据库的同时，因为服务器不触摸所有页面，并执行所需的一致性检查。 因此，使用 VSS 任何备份和还原应用程序必须验证快照的一致性。 Exchange Server 2013 快照一致性检查支持以下两种方法： 
  
- CHKSGFILES API
    
- Eseutil 命令行工具
    
我们建议您使用 CHKSGFILES API，因为容易得多备份应用程序来检测、 诊断，并报告期间 CHKSGFILES 一致性找到的错误检查。 有关如何使用 CHKSGFILES API 的信息，请参阅[使用 CHKSGFILES API 在 Exchange 2013 验证备份完整性](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md)。
  
## <a name="running-the-eseutil-tool"></a>运行 Eseutil 工具

若要检查的快照一致性，请针对下表中标识的数据库和日志文件运行 eseutil 命令。 
  
**表 1。每种备份类型的 Eseutil.exe 命令**

|**文件类型/备份类型**|**完整备份**|**副本备份**|**增量备份**|**差异备份**|
|:-----|:-----|:-----|:-----|:-----|
|.edb  <br/> |"eseutil /k /i"  <br/> |"eseutil /k /i"  <br/> |不适用  <br/> |不适用  <br/> |
|.log  <br/> |"eseutil /k"(1)  <br/> |"eseutil /k"(1)  <br/> |"eseutil /k"(2)  <br/> |"eseutil /k"(2)  <br/> |
   
> [!NOTE]
> 不需要对.stm 和.chk 文件运行 eseutil 命令。 
  
等于或大于检查点日志文件的号码所需才能恢复快照数据库的生成，所有具有数字的日志文件生成的日志文件。 如果存在，也是必需的数据库恢复当前日志文件 (Enn.log)。 如果任何所需的日志文件的失败一致性检查，请求者必须确保调用[BackupComplete](http://msdn.microsoft.com/en-us/library/windows/desktop/aa382651%28v=vs.85%29.aspx)方法之前备份的组件的状态设置为 FALSE。 若要确定检查点日志文件，针对快照检查点文件运行 Eseutil.exe 和分析的输出"检查点:。" 下面的示例演示如何对检查点文件运行 Eseutil.exe。 
  
```cpp
c:\eseutil.exe /mk E01.chk
Checkpoint: (0x20, 9D, 187)
```

在示例中的第二行是返回的值，其中 0x20 是十六进制的日志生成编号的检查点日志文件。 本示例中，任何日志文件，包括 E01000020.log 和更高版本，必须无法损坏才能恢复的快照数据库，即使数据库本身已过物理一致性检查。
  
在增量备份或差异备份集中的所有日志文件都所需的数据库恢复。 您可以通过对日志文件前缀运行 Eseutil.exe 检查日志序列的一致性。 下面的示例演示如何在给定路径上针对所有文件的窗体 E01xxxxx.log 运行一致性检查。
  
```cpp
c:\eseutil /k E01
```

## <a name="checking-the-eseutilexe-output"></a>检查 Eseutil.exe 输出

请求者必须验证负退出错误级别错误的所有值返回。 有关错误级别值的信息，请参阅[参考 Eseutil 的常见错误](http://technet.microsoft.com/en-us/library/aa996759%28v=exchg.80%29.aspx)。 若要查看在命令行错误级别，请键入"回显 %错误级别 %"Eseutil.exe 完成运行后。 负错误级别指示一个或多个文件已损坏。
  
请求者调用**BackupComplete**方法之前，则必须确保备份的组件的状态反映一致性检查的结果。 如果发现任何损坏，状态将为 FALSE;如果找到没有损坏，状态将设为 TRUE。 
  
## <a name="see-also"></a>另请参阅

- [使用 CHKSGFILES API 在 Exchange 2013 中验证备份完整性](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md)
- [构建备份和还原 Exchange 2013 的应用程序](build-backup-and-restore-applications-for-exchange-2013.md)
- [CChkSGFiles 类参考 （英文）](cchksgfiles-class-reference.md)
- [Exchange 2013 的备份和还原概念](backup-and-restore-concepts-for-exchange-2013.md)
    

