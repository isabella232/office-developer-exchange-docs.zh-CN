---
title: CChkSGFiles 函数
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
description: 上次修改时间：2013年2月22日
ms.openlocfilehash: a62c5940322d3d7a71f2db93214f1e970fc6859b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455245"
---
# <a name="cchksgfileserrcheckdbheaders-function"></a>CChkSGFiles 函数

**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013 
  
验证由**ErrInit**函数指定的数据库文件的标头。 此函数还返回每个指定数据库中的页面大小和页面数目。 
  
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
  
输出参数。 每个指定数据库的页面大小（以字节为单位）。
    
### <a name="pcheaderpagesperdb"></a>pcHeaderPagesPerDb 
  
输出参数。 在每个指定数据库的开头，由数据库引擎保留以供内部使用的页面数。 请注意，*不*应将标头页传递给**ErrCheckDbPages**函数以进行验证。 
    
### <a name="pidberrorencountered"></a>piDbErrorEncountered
  
输出参数。 如果函数的返回值指示错误，则此参数将是传递给**ErrInit**函数的**rgwszDb []** 数组的索引。 已编制索引的数组元素表示遇到错误的数据库。 如果函数不返回错误值，则此参数值无效。 
    
### <a name="ulflags"></a>ulFlags 
  
可选的输入参数。 保留此值以供将来使用。 传递的值应为0（零）。
    
## <a name="return-value"></a>返回值

此函数返回[CChkSGFiles 枚举](cchksgfiles-err-enumeration.md)中的错误代码。
  
## <a name="remarks"></a>备注

**ErrCheckDbHeaders**验证使用**ErrInit**注册的所有数据库是否具有相同的日志签名和数据库页面大小。 您还可以使用最低的**genMin**参数值和最高的**genMax**参数值来确定将所有已注册的数据库置于干净关闭状态所需的一组日志文件。 
  
仅当检测到错误（由非零**ErrCheckDbHeaders**返回值所指示）时，才会设置**piDbErrorEncountered**参数。 
  
当此函数中出现错误时，将向 Windows 错误事件日志中添加一个错误事件。
  
只能在调用**ErrInit**后调用**ErrCheckDbHeaders** ，并且必须先调用它，然后才能调用**ErrCheckDbPages**和**ErrCheckLogs**。
  
如果要在多线程应用程序中使用 CHKSGFILES，则必须在单线程部分调用**ErrCheckDbHeaders**函数，并且只能为每个**CCheckSGFiles**对象调用一次该函数。 
  
## <a name="requirements"></a>Requirements

Exchange 2013 仅包含64位版本的 CHKSGFILES API。
  
运行应用程序所使用的帐户必须具有对要检查的数据库和日志文件的读取访问权限。
  

