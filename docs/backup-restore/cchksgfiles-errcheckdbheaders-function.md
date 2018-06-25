---
title: CChkSGFiles.ErrCheckDbHeaders 函数
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ErrCheckDbHeaders
api_type:
- dllExport
ms.assetid: 75289cd2-35b1-4f75-a651-dce01f1ddda1
description: 上次修改时间： 2013 年 2 月 22 日
ms.openlocfilehash: a407019063b34970e883a00ca4f4d730935d7cba
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752694"
---
# <a name="cchksgfileserrcheckdbheaders-function"></a>CChkSGFiles.ErrCheckDbHeaders 函数

**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013 
  
验证**ErrInit**函数由指定的数据库文件的标题。 此函数还返回每个指定的数据库中的页面大小和数量页面。 
  
```cs
Vitual ERRErrCheckDbHeaders  
(
        ULONG  * const pcbDbPageSize,
        ULONG  * const pcHeaderPagesPerDb,
        ULONG   const piDbErrorEncountered,
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a>参数

### <a name="pcbdbpagesize"></a>pcbDbPageSize 
  
输出参数。 每个指定的数据库，以字节为单位的页面大小。
    
### <a name="pcheaderpagesperdb"></a>pcHeaderPagesPerDb 
  
输出参数。 每个开头的页数指定保留供内部使用数据库引擎的数据库。 请注意，您应该*传递标题页用于验证**ErrCheckDbPages**函数*。 
    
### <a name="pidberrorencountered"></a>piDbErrorEncountered
  
输出参数。 如果该函数的返回值指示错误，此参数将传递给**ErrInit**函数**rgwszDb []** 数组的索引。 索引的数组元素表示遇到错误的数据库。 如果该函数不返回错误值，此参数值无效。 
    
### <a name="ulflags"></a>ulFlags 
  
可选的输入的参数。 此值保留以供将来使用。 传递的值应为 0 （零）。
    
## <a name="return-value"></a>返回值

此函数返回[CChkSGFiles.ERR 枚举](cchksgfiles-err-enumeration.md)中的错误代码。
  
## <a name="remarks"></a>注解

**ErrCheckDbHeaders**验证**ErrInit**注册的所有数据库都具有相同的日志签名和数据库页面大小。 您可以使用最低**genMin**参数值和最高**genMax**参数值来确定所需的所有已注册数据库置于干净关闭状态的日志文件的集合。 
  
**PiDbErrorEncountered**参数设置仅在检测到错误时，由非零**ErrCheckDbHeaders**返回值。 
  
在此函数中出现错误时发生，则 error 事件将添加到 Windows 错误事件日志。
  
您可以调用**ErrInit**后才, 调用**ErrCheckDbHeaders**和调用**ErrCheckDbPages**和**ErrCheckLogs**之前必须调用。
  
如果您使用 CHKSGFILES 多线程应用程序中，您必须**ErrCheckDbHeaders**函数调用中的单线程部分中，且您可以为每个**CCheckSGFiles**对象调用它仅执行一次。 
  
## <a name="requirements"></a>要求

Exchange 2013 只包括 CHKSGFILES API 的 64 位版本。
  
下运行该应用程序的帐户必须具有对要检查的数据库和日志文件的读取访问权限。
  

