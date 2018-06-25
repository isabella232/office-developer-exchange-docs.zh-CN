---
title: CChkSGFiles.ErrInit 函数
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ErrInit
api_type:
- dllExport
ms.assetid: 61bb3af1-8b51-4bae-8e25-90a4dc1226c5
description: 上次修改时间： 2013 年 3 月 3 日
ms.openlocfilehash: d4b76933a747fe4bf084061cf080bc68264132ed
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752686"
---
# <a name="cchksgfileserrinit-function"></a>CChkSGFiles.ErrInit 函数
  
**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013
  
初始化通过指定要检查的数据库的**CChkSGFiles**对象的路径和要检查的事务日志文件的基本名称。 应用程序应在成功调用**新建**函数后立即调用此函数。 
  
```cs
Vitual ERRErrInit  
(
    Const WCHAR  * const rgwszDb[],
    Const ULONGcDB,
    __in_z const WCHAR  * const wszLogPath,
    __in_z const WCHAR  * const wszBaseName,
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a>参数

### <a name="rgwszdb"></a>rgwszDb]
  
输入的参数。 数组，它指定要检查的数据库。 每个数组元素是 null 结尾的 Unicode 字符串，包含要检查的数据库的路径和文件名称。
    
### <a name="cdb"></a>cDB
  
输入的参数。 有效的数据库路径**rgwszDb**数组中的元素数。 
    
#### <a name="wszlogpath"></a>wszLogPath
  
输入的参数。 要检查的以 null 结尾的 Unicode 字符串形式的事务日志文件的完整路径。
    
### <a name="wszbasename"></a>wszBaseName
  
输入的参数。 Exchange 的事务日志文件，以 null 结尾的 Unicode 字符串形式三个字母基名称。
    
### <a name="ulflags"></a>ulFlags
  
可选的输入的参数。 此值保留以供将来使用。 通过此参数传递的值应为 0 （零）。
    
## <a name="return-value"></a>返回值

从[ERR](cchksgfiles-err-enumeration.md)枚举错误代码。 
  
## <a name="remarks"></a>注解

**ErrInit**函数注册的数据库和要检查的日志文件。 之后，**新建**函数将调用的函数调用任何其他**ChkSGFiles**之前，必须调用此函数。 
  
您必须以 null 结尾的 Unicode 字符串形式提供所有数据库名称、 日志文件路径，和的基名称。
  
您可以检查仅数据库文件，仅日志文件或数据库和日志文件。 但是时调用此函数，应用程序必须指定要检查的至少一个实体。 传递 0 （零） **cDB**和 NULL **wszLogPath**将返回错误。 
  
如果**cDB**的值为非 0 （零），为**rgwszDb**传递 NULL 将导致出错。 若要检查数据库文件，该应用程序必须提供数据库名称。 
  
如果为**wszBaseName**传递空值，但**wszLogPath**不为 NULL，则将返回错误。 始终在检查日志文件时所需日志文件的基名称。 
  
如果您使用 CHKSGFILES 多线程应用程序中，您必须将应用程序的单线程部分调用**ErrInit**函数，且您可以为每个**CCheckSGFiles**对象调用它仅执行一次。 
  
## <a name="requirements"></a>要求

Exchange 2013 只包括 CHKSGFILES API 的 64 位版本。
  
下运行该应用程序的帐户必须具有对要检查的数据库和日志文件的读取访问权限。
  

