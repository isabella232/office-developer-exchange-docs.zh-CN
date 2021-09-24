---
title: CChkSGFiles.ErrCheckLogs 函数
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ErrCheckLogs
api_type:
- dllExport
ms.assetid: cec0df4b-4679-4682-bacf-69b4f4aef343
description: 上次修改时间：2013 年 2 月 22 日
ms.openlocfilehash: 64484b32fdc566d6fee8631f80d078aca82b11d1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516382"
---
# <a name="cchksgfileserrchecklogs-function"></a>CChkSGFiles.ErrCheckLogs 函数

**适用于：Exchange Server** 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013 年
  
验证 **ErrInit** 函数中指定的所有数据库文件的日志文件。 经过验证的日志是路径中存在的日志，这些日志将三个字母的基本日志文件传递到 **ErrInit**。
  
```cs
Vitual ERRErrCheckLogs 
(
        BOOL  * const pfOnlyUnnecessaryLogsCorrup,
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a>参数

### <a name="pfonlyunnecessarylogscorrupt"></a>pfOnlyUnnecessaryLogsCorrupt 
  
输出参数。 如果 **为 true，** 则此参数指示在事务日志文件中发现了错误，但在日志文件中发现了所有这些错误，这些错误是在不丢失数据的情况下使数据库干净关闭状态所不需要的。 此 **参数** 中返回的 true 值仅在 **ErrCheckLogs** 返回 **errSuccess 时有效**。 
    
### <a name="ulflags"></a>ulFlags
  
可选输入参数。 保留此值以供将来使用。 此参数传递的值应为 0， (零) 。
    
## <a name="return-value"></a>返回值

ERR [枚举中的错误](cchksgfiles-err-enumeration.md) 代码。 
  
必须记住，即使日志文件中发现错误，此函数也可以返回 **errSuccess。** 因此， **当 ErrCheckLogs** 返回 **errSuccess** 时，应用程序还应检查  **pfOnlyUnnecessaryLogsCorrupt** 返回参数。 如果 **ErrCheckLogs** 返回 **errSuccess** 时 **pfOnlyUnnecessaryLogsCorrupts** 为 **true，** 则这表示已找到一个或多个错误，但仅在日志文件中发现错误，使数据库成为最新数据库不需要。
  
## <a name="remarks"></a>注解

必须先 **调用 ErrCheckDbHeaders** 函数，然后才能调用 **ErrCheckLogs** 函数。 
  
检查Exchange事务日志文件时，需要一些日志文件，才能将存储组的数据库保持干净关闭状态而不会丢失数据，而其他日志文件可能不需要。 **ErrCheckLogs** 函数确定使数据库更新所需的最旧日志文件和最新日志文件。 
  
**ErrCheckLogs** 函数验证传递给 **ErrInit** 函数的指定路径中也具有指定三个字母的基本文件名的所有日志文件。 
  
如果在日志文件中未找到任何错误， **则 ErrCheckLogs** 将返回 **errSuccess**。 
  
如果发现任何必需的日志文件已损坏 **，ErrCheckLogs** 将返回错误。 
  
如果仅在比所需最早时间早的日志文件中发现错误，该函数将返回 **errSuccess，** 并设置返回参数 **pfOnlyUnnecessaryLogCorrupt** 为 **true**。 应用程序应意识到某些旧日志文件中出现错误，如果是这样，它可能会警告用户。 在任何情况下，这些错误都不应影响数据库的整体完整性或影响能否成功播放日志。
  
如果在需要 **ErrCheckLogs** 确定日志文件日志之后创建的任何记录中发现错误，函数将返回错误。 即使在更新数据库所需的日志文件生成的日志文件，也会返回此错误。 尽管使用标识的日志文件可能会将数据库恢复到干净关闭状态，但将不会应用在以后损坏的日志文件中指定的事务，从而在还原数据库时导致数据丢失。 
  
**CChkSGFiles** 对象确定是否实际检查了通过 **ErrInit** 函数注册的所有日志文件。 如果未成功检查所有日志 **，ErrTerm** 函数将返回错误。 
  
如果在多线程应用程序中使用 CHKSGFILES，可以在应用程序的多线程部分调用 **ErrCheckLogs** 函数，但只能针对每个 **CCheckSGFiles** 对象调用它一次。 
  
## <a name="requirements"></a>Requirements

Exchange 2013 仅包括 64 位版本的 CHKSGFILES API。
  
运行应用程序的帐户必须具有对要检查的数据库和日志文件的读取访问权限。
  

