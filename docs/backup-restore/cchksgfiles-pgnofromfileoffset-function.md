---
title: CChkSGFiles.PgnoFromFileOffset 函数
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PgnoFromFileOffset
api_type:
- dllExport
ms.assetid: 3d69ca6d-5ed1-4038-859e-106e776eeec1
description: 上次修改时间： 2013 年 2 月 22 日
ms.openlocfilehash: d42ba7c8178c6fccdddec0b5da88a972f51184c6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752695"
---
# <a name="cchksgfilespgnofromfileoffset-function"></a>CChkSGFiles.PgnoFromFileOffset 函数

**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013
  
返回到物理数据库文件中指定的字节索引的逻辑数据库页码对应。 如果文件偏移量无效，或尚未**ErrCheckDbHeaders**函数调用的数据库，此函数将返回 0 （零）。 
  
```cs
Vitual ULONGPgnoFromFileOffset  
(
    Const ULONGLONGibFileOffset
);

```

## <a name="parameters"></a>参数

### <a name="ibfileoffset"></a>ibFileOffset
  
输入的参数。 偏移量数据库文件，以字节为单位。
    
## <a name="return-value"></a>返回值

数据库文件的逻辑页码，其中包含指定的偏移量。
  
## <a name="remarks"></a>注解

如果**ibFileOffset**参数无效，则**PgnoFromFileOffset**函数将返回 0 （零）。 
  
如果您尚未对**CCheckSGFiles**实例调用**ErrCheckDbHeaders**函数， **PgnoFromFileOffset**还返回 0 （零）。 您必须调用**ErrCheckDbHeaders**初始化数据库页面大小和分配到数据库标头的页数。 
  
您应使用**PgnoFromFileOffset**填充**页\_INFO**结构调用**ErrCheckDbPages**准备过程中的元素。 **ErrCheckDbPages** **rgPageInfo**参数要求数组中的每个元素的**PAGE_INFO**结构，用正确初始化**ulPgno**成员值。 
  
如果您使用 CHKSGFILES 多线程应用程序中，您可以在应用程序的多线程部分调用**PgnoFromFileOffset**函数。 请注意，您就可以通常调用此函数多次所检查每个数据库。 
  
## <a name="requirements"></a>要求

Exchange Server 2013 只包括 CHKSGFILES API 的 64 位版本。
  
下运行该应用程序的帐户必须具有读取权限要检查的数据库和日志文件。
  

