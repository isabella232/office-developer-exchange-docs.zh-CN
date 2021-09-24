---
title: 使用 2013 年 10 月中的 Eseutil 工具Exchange完整性
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: b0d325ba-4482-4ca2-9a69-c890f985b206
description: 了解如何使用 Eseutil 命令行工具验证数据库存储Exchange备份。
ms.openlocfilehash: 0ac994201d1f6c711e5d4d0a3d5835f9bac6e041
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516221"
---
#  <a name="validate-backup-integrity-by-using-the-eseutil-tool-in-exchange-2013"></a>使用 2013 年 10 月中的 Eseutil 工具Exchange完整性

了解如何使用 Eseutil 命令行工具验证数据库存储Exchange备份。 
  
**适用于：Exchange Server** 2013 
  
由于卷影复制服务 (VSS) 可以在 Exchange 继续写入数据库时创建备份，因此服务器不会接触所有页面并执行必要的一致性检查。 因此，使用 VSS 的任何备份和还原应用程序都必须验证快照一致性。 Exchange Server 2013 支持以下两种检查快照一致性的方法： 
  
- The CHKSGFILES API
    
- Eseutil 命令行工具
    
建议您使用 CHKSGFILES API，因为备份应用程序可以更轻松地检测、诊断并报告在 CHKSGFILES 一致性检查过程中发现的错误。 有关如何使用 CHKSGFILES API 的信息，请参阅 Exchange [2013 中的使用 CHKSGFILES API](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md)验证备份完整性。
  
## <a name="running-the-eseutil-tool"></a>运行 Eseutil 工具

若要检查快照一致性，请对下表中标识的数据库和日志文件运行 eseutil 命令。 
  
**表 1.Eseutil.exe备份类型的命令**

|**文件类型/备份类型**|**完整备份**|**复制备份**|**增量备份**|**差异备份**|
|:-----|:-----|:-----|:-----|:-----|
|.edb  <br/> |"eseutil /k /i"  <br/> |"eseutil /k /i"  <br/> |不适用  <br/> |不适用  <br/> |
|.log  <br/> |"eseutil /k" (1)   <br/> |"eseutil /k" (1)   <br/> |"eseutil /k" (2)   <br/> |"eseutil /k" (2)   <br/> |
   
> [!NOTE]
> 无需对 .stm 和 .chk 文件运行 eseutil 命令。 
  
恢复快照数据库日志文件生成号等于或大于检查点生成号的所有日志文件日志文件这些日志文件是必需的。 如果存在，则数据库恢复日志文件 (当前) Enn.log 数据库。 如果任何必需的日志文件未能通过一致性检查，则请求者必须确保备份组件的状态设置为 FALSE，然后再调用 [BackupComplete](https://msdn.microsoft.com/library/windows/desktop/aa382651%28v=vs.85%29.aspx) 方法。 若要标识检查点日志文件，请Eseutil.exe快照检查点文件运行检查点，然后分析"Checkpoint："的输出。 以下示例演示如何针对检查点Eseutil.exe运行安全检查。 
  
```cpp
c:\eseutil.exe /mk E01.chk
Checkpoint: (0x20, 9D, 187)
```

示例中的第二行是返回值，其中 0x20 是检查点日志的十六进制日志生成日志文件。 本示例中，任何日志文件（包括 E01000020.log 和更大的日志文件）都不得损坏，以便恢复快照数据库，即使数据库本身已经通过了物理一致性检查。
  
数据库恢复需要增量或差异备份集内的所有日志文件。 可以通过对前缀 Eseutil.exe来检查日志序列日志文件一致性。 下面的示例演示如何对给定路径上 E01xxxxx.log 形式的所有文件运行一致性检查。
  
```cpp
c:\eseutil /k E01
```

## <a name="checking-the-eseutilexe-output"></a>检查Eseutil.exe输出

请求者必须验证返回的所有退出 ERRORLEVEL 错误值都是非negative的。 有关 ERRORLEVEL 值的信息，请参阅 [Reference for Common Eseutil Errors](https://technet.microsoft.com/library/aa996759%28v=exchg.80%29.aspx)。 若要在命令行中查看 ERRORLEVEL，请键入"echo %errorlevel%"，Eseutil.exe运行。 负 ERRORLEVEL 表示一个或多个文件已损坏。
  
在请求者调用 **BackupComplete** 方法之前，它必须确保备份组件的状态反映一致性检查的结果。 如果发现任何损坏，则状态将为 FALSE;如果未找到损坏，则状态将为 TRUE。 
  
## <a name="see-also"></a>另请参阅

- [在 2013 年 6 月使用 CHKSGFILES API Exchange完整性](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md)
- [构建适用于 Exchange 2013 的备份和还原应用程序](build-backup-and-restore-applications-for-exchange-2013.md)
- [CChkSGFiles 类参考](cchksgfiles-class-reference.md)
- [Exchange 2013 的备份和还原概念](backup-and-restore-concepts-for-exchange-2013.md)
    

