---
title: CChkSGFiles 函数
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ErrCheckLogs
api_type:
- dllExport
ms.assetid: cec0df4b-4679-4682-bacf-69b4f4aef343
description: 上次修改时间：2013年2月22日
ms.openlocfilehash: 71e21bb3a748a532f9e3167e0b36898acde71b02
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526716"
---
# <a name="cchksgfileserrchecklogs-function"></a>CChkSGFiles 函数

**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013
  
验证在**ErrInit**函数中指定的所有数据库文件的日志文件。 经过验证的日志是指路径中存在的日志，并将三个字母的基本日志文件名传递给**ErrInit**。
  
```cs
Vitual ERRErrCheckLogs 
(
        BOOL  * const pfOnlyUnnecessaryLogsCorrup,
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a>参数

### <a name="pfonlyunnecessarylogscorrupt"></a>pfOnlyUnnecessaryLogsCorrupt 
  
输出参数。 如果**为 true，则**此参数指示在事务日志文件中发现错误，但这些错误都在日志文件中，这些错误在不丢失数据的情况下，不需要将数据库置于干净关闭状态。 此参数中返回的**true**值仅在**ErrCheckLogs**返回**errSuccess**时有效。 
    
### <a name="ulflags"></a>ulFlags
  
可选的输入参数。 保留此值以供将来使用。 此参数传递的值应为0（零）。
    
## <a name="return-value"></a>返回值

[ERR](cchksgfiles-err-enumeration.md)枚举中的错误代码。 
  
请务必记住，即使在日志文件中发现错误，此函数也可以返回**errSuccess** 。 因此，当**ErrCheckLogs**返回**errSuccess**时，应用程序还应检查**pfOnlyUnnecessaryLogsCorrupt**返回参数。 如果**ErrCheckLogs**返回**errSuccess**时**pfOnlyUnnecessaryLogsCorrupts**为**true** ，则表示发现一个或多个错误，但仅在不需要将数据库更新为最新的日志文件中。
  
## <a name="remarks"></a>备注

必须先调用**ErrCheckDbHeaders**函数，然后才能调用**ErrCheckLogs**函数。 
  
检查 Exchange 数据库事务日志文件时，必须有一些日志文件将存储组中的数据库置于干净关闭状态，而不会丢失数据，而可能不需要其他日志文件。 **ErrCheckLogs**函数确定将数据库更新为最新所需的最旧和最新日志文件。 
  
**ErrCheckLogs**函数验证指定路径中的所有日志文件，这些日志文件也具有指定的三个字母的基本文件名（传递给**ErrInit**函数）。 
  
如果日志文件中未发现任何错误， **ErrCheckLogs**将返回**errSuccess**。 
  
如果发现任何所需的日志文件已损坏， **ErrCheckLogs**将返回错误。 
  
如果仅在日志文件中找到比所需的最早时间更早的错误，函数将返回**errSuccess** ，并将返回参数**pfOnlyUnnecessaryLogCorrupt**设置为**true**。 应用程序应识别某些旧日志文件中存在错误，如果是，则可能会提醒用户。 在任何情况下，这些错误都不会影响数据库的整体完整性，也不会影响播放日志是否将成功。
  
如果在需要**ErrCheckLogs**确定的最早日志之后创建的任何日志文件中都存在错误，则该函数将返回错误。 即使在生成的日志文件中发现的日志文件错误比将数据库更新为最新所需的日志文件中，也会返回该错误。 尽管可以使用已标识的日志文件将数据库置于干净关闭状态，但不会应用在以后损坏的日志文件中指定的事务，从而导致在还原数据库时丢失数据。 
  
**CChkSGFiles**对象确定是否实际检查了使用**ErrInit**函数注册的所有日志文件。 如果未成功检查所有日志， **ErrTerm**函数将返回一个错误。 
  
如果您在多线程应用程序中使用 CHKSGFILES，则可以在应用程序的多线程部分调用**ErrCheckLogs**函数，但只能为每个**CCheckSGFiles**对象调用一次该函数。 
  
## <a name="requirements"></a>Requirements

Exchange 2013 仅包含64位版本的 CHKSGFILES API。
  
运行应用程序所使用的帐户必须具有对要检查的数据库和日志文件的读取访问权限。
  

