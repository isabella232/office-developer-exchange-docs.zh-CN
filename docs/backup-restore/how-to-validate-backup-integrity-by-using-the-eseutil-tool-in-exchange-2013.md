---
title: 使用 Exchange 2013 中的 Eseutil 工具验证备份完整性
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b0d325ba-4482-4ca2-9a69-c890f985b206
description: 了解如何使用 Eseutil 命令行工具验证 Exchange 存储的备份。
ms.openlocfilehash: e8f1a46e2d94729ae5586861317312e277216d63
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44452795"
---
#  <a name="validate-backup-integrity-by-using-the-eseutil-tool-in-exchange-2013"></a>使用 Exchange 2013 中的 Eseutil 工具验证备份完整性

了解如何使用 Eseutil 命令行工具验证 Exchange 存储的备份。 
  
**适用于：** Exchange Server 2013 
  
由于卷影复制服务（VSS）可以在 Exchange 继续写入数据库时创建备份，因此服务器不会接触所有页面并执行必要的一致性检查。 因此，使用 VSS 的任何备份和还原应用程序都必须验证快照一致性。 Exchange Server 2013 支持以下两种检查快照一致性的方法： 
  
- CHKSGFILES API
    
- Eseutil 命令行工具
    
建议使用 CHKSGFILES API，因为备份应用程序可以更轻松地检测、诊断和报告 CHKSGFILES 一致性检查过程中发现的错误。 有关如何使用 CHKSGFILES API 的信息，请参阅[使用 Exchange 2013 中的 CHKSGFILES API 验证备份完整性](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md)。
  
## <a name="running-the-eseutil-tool"></a>运行 Eseutil 工具

若要检查快照一致性，请对下表中标识的数据库和日志文件运行 eseutil 命令。 
  
**表1。每种备份类型的 Eseutil 命令**

|**文件类型/备份类型**|**完整备份**|**副本备份**|**增量备份**|**差异备份**|
|:-----|:-----|:-----|:-----|:-----|
|.edb  <br/> |"eseutil/k/i"  <br/> |"eseutil/k/i"  <br/> |不适用  <br/> |不适用  <br/> |
|.log  <br/> |"eseutil/k" （1）  <br/> |"eseutil/k" （1）  <br/> |"eseutil/k" （2）  <br/> |"eseutil/k" （2）  <br/> |
   
> [!NOTE]
> 您无需对 .stm 和 .chk 文件运行 eseutil 命令。 
  
必须有日志文件生成号等于或大于检查点日志文件世代号的所有日志文件，才能恢复快照数据库。 如果存在，则数据库恢复也需要当前日志文件（Enn）。 如果任何必需的日志文件未通过一致性检查，请求者必须确保在调用[BackupComplete](https://msdn.microsoft.com/library/windows/desktop/aa382651%28v=vs.85%29.aspx)方法之前将备份组件的状态设置为 FALSE。 若要确定检查点日志文件，请针对快照检查点文件运行 Eseutil，并分析 "检查点：" 的输出。 下面的示例演示如何对检查点文件运行 Eseutil。 
  
```cpp
c:\eseutil.exe /mk E01.chk
Checkpoint: (0x20, 9D, 187)
```

该示例中的第二行是返回值，其中0x20 是检查点日志文件的十六进制日志生成编号。 在此示例中，任何日志文件（包括 E01000020 和更高版本）都必须损坏才能恢复快照数据库，即使数据库本身已经通过了物理一致性检查也是如此。
  
数据库恢复需要增量备份或差异备份集中的所有日志文件。 您可以通过对日志文件前缀运行 Eseutil 来检查日志序列的一致性。 下面的示例演示如何对给定路径上 E01xxxxx 形式的所有文件运行一致性检查。
  
```cpp
c:\eseutil /k E01
```

## <a name="checking-the-eseutilexe-output"></a>检查 Eseutil.exe 输出

请求者必须验证返回的所有退出 ERRORLEVEL 错误值是否为非负。 有关 ERRORLEVEL 值的信息，请参阅[常见 Eseutil 错误的参考](https://technet.microsoft.com/library/aa996759%28v=exchg.80%29.aspx)。 若要在命令行中查看 ERRORLEVEL，请在运行 Eseutil 后键入 "echo% ERRORLEVEL%"。 负 ERRORLEVEL 表示一个或多个文件已损坏。
  
在请求者调用**BackupComplete**方法之前，必须确保备份组件的状态反映了一致性检查的结果。 如果发现任何损坏，则状态将为 FALSE;如果未发现损坏，状态将为 TRUE。 
  
## <a name="see-also"></a>另请参阅

- [使用 Exchange 2013 中的 CHKSGFILES API 验证备份完整性](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md)
- [为 Exchange 2013 生成备份和还原应用程序](build-backup-and-restore-applications-for-exchange-2013.md)
- [CChkSGFiles 类参考](cchksgfiles-class-reference.md)
- [Exchange 2013 的备份和还原概念](backup-and-restore-concepts-for-exchange-2013.md)
    

