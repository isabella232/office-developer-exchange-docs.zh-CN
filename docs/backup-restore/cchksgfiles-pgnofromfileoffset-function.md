---
title: CChkSGFiles 函数
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
description: 上次修改时间：2013年2月22日
ms.openlocfilehash: 3c8f749a03b4aa251bf9312eba5d7e2d46c91fae
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44452893"
---
# <a name="cchksgfilespgnofromfileoffset-function"></a>CChkSGFiles 函数

**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013
  
返回与物理数据库文件中指定的字节索引相对应的逻辑数据库页面编号。 如果文件偏移量无效，或者尚未为数据库调用**ErrCheckDbHeaders**函数，则此函数返回0（零）。 
  
```cs
Vitual ULONGPgnoFromFileOffset  
(
    Const ULONGLONGibFileOffset
);

```

## <a name="parameters"></a>参数

### <a name="ibfileoffset"></a>ibFileOffset
  
输入参数。 数据库文件中的偏移量（以字节为单位）。
    
## <a name="return-value"></a>返回值

包含指定偏移量的数据库文件的逻辑页面编号。
  
## <a name="remarks"></a>备注

如果**ibFileOffset**参数无效，则**PgnoFromFileOffset**函数将返回0（零）。 
  
如果您未在**CCheckSGFiles**实例上调用**ErrCheckDbHeaders**函数，则**PgnoFromFileOffset**也返回0（零）。 必须调用**ErrCheckDbHeaders**以初始化数据库页面大小和分配给数据库标头的页面数。 
  
应使用**PgnoFromFileOffset**在准备调用**ErrCheckDbPages**的过程中填写**页面 \_ 信息**结构元素。 **ErrCheckDbPages**的**rgPageInfo**参数要求数组中的每个元素都是一个**PAGE_INFO**结构，其中**ulPgno**成员的值已正确初始化。 
  
如果要在多线程应用程序中使用 CHKSGFILES，则可以在应用程序的多线程部分调用**PgnoFromFileOffset**函数。 请注意，对于所检查的每个数据库，通常需要多次调用此函数。 
  
## <a name="requirements"></a>Requirements

Exchange Server 2013 仅包含64位版本的 CHKSGFILES API。
  
运行应用程序所使用的帐户必须具有对要检查的数据库和日志文件的读取权限。
  

