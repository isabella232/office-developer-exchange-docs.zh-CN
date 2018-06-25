---
title: CChkSGFiles.ErrCheckLogs 函数
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
description: 上次修改时间： 2013 年 2 月 22 日
ms.openlocfilehash: 5b1070de73bc23ae09ddb7835bd72c8e8a71a95f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752690"
---
# <a name="cchksgfileserrchecklogs-function"></a>CChkSGFiles.ErrCheckLogs 函数

**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013
  
验证已**ErrInit**函数中指定的所有数据库文件的日志文件。 验证的日志那些在位于路径，并具有三个字母基本日志文件名称传递给**ErrInit**。
  
```cs
Vitual ERRErrCheckLogs 
(
        BOOL  * const pfOnlyUnnecessaryLogsCorrup,
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a>参数

### <a name="pfonlyunnecessarylogscorrupt"></a>pfOnlyUnnecessaryLogsCorrupt 
  
输出参数。 **True**，此参数指示发现事务日志文件，但这些错误错误时已所有到，则不需要的日志文件中找到将数据库置于干净关闭状态丢失数据。 仅当**ErrCheckLogs**返回**errSuccess**时，此参数中返回一个**true**值是有效。 
    
### <a name="ulflags"></a>ulFlags
  
可选的输入的参数。 此值保留以供将来使用。 通过此参数传递的值应为 0 （零）。
    
## <a name="return-value"></a>返回值

从[ERR](cchksgfiles-err-enumeration.md)枚举错误代码。 
  
务必要记住甚至在日志文件中找到错误时，此函数可以返回**errSuccess** 。 因此，当**ErrCheckLogs**返回**errSuccess**，应用程序还应检查**pfOnlyUnnecessaryLogsCorrupt**返回参数。 如果**ErrCheckLogs**返回**errSuccess**时， **pfOnlyUnnecessaryLogsCorrupts**为**true** ，则表示的发现一个或多个错误，但仅在不需要以显示最新的数据库的日志文件。
  
## <a name="remarks"></a>注解

可以调用**ErrCheckLogs**函数之前，必须调用**ErrCheckDbHeaders**函数。 
  
当正在检查 Exchange 数据库事务日志文件时，日志文件的一些将需要存储组中将数据库置于干净关闭状态，而不会数据丢失，而可能不需要其他日志文件。 **ErrCheckLogs**函数确定最早和最新日志文件所需以显示最新的数据库。 
  
**ErrCheckLogs**函数验证传递给**ErrInit**函数还可以指定三个字母的基文件名指定路径中的所有日志文件。 
  
如果在日志文件中没有发现任何错误， **ErrCheckLogs**返回**errSuccess**。 
  
如果找到任何所需的日志文件可能已损坏， **ErrCheckLogs**将返回错误。 
  
如果仅在早于所需的最早那些的日志文件中没有发现错误，该函数将返回**errSuccess** ，并将返回参数**pfOnlyUnnecessaryLogCorrupt**设置为**true**。 应用程序应认识到，没有错误某些这些旧的日志文件，如果跟随，则它可能将通知用户。 在任何情况下，这些错误应该不会影响数据库的总体完整性，或影响是否播放日志向前将成功。
  
如果没有发现任何后的最早创建的日志文件中的错误日志**ErrCheckLogs**确定所需、 函数将返回错误。 偶数晚于什么生成的日志文件中找到的日志文件错误如果是，以使最新的数据库，将返回错误。 尽管就可以通过使用标识的日志文件将数据库置于干净关闭状态，更高版本损坏的日志文件中指定的事务将不会应用，从而导致数据丢失时还原数据库。 
  
**CChkSGFiles**对象确定是否实际检查了所有与**ErrInit**函数注册的日志文件。 如果不是所有日志未成功签， **ErrTerm**函数将返回错误。 
  
如果您使用 CHKSGFILES 多线程应用程序中，您可以将应用程序的多线程部分中调用**ErrCheckLogs**函数，但您可以为每个**CCheckSGFiles**对象调用它仅执行一次。 
  
## <a name="requirements"></a>要求

Exchange 2013 只包括 CHKSGFILES API 的 64 位版本。
  
下运行该应用程序的帐户必须具有对要检查的数据库和日志文件的读取访问权限。
  

