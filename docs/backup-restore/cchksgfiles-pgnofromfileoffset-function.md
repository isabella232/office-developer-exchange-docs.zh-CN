---
title: CChkSGFiles.PgnoFromFileOffset 函数
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PgnoFromFileOffset
api_type:
- dllExport
ms.assetid: 3d69ca6d-5ed1-4038-859e-106e776eeec1
description: 上次修改时间：2013 年 2 月 22 日
ms.openlocfilehash: 3e2845cc326520ad875dc8bda52bac3d7c2e2cfa
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516242"
---
# <a name="cchksgfilespgnofromfileoffset-function"></a>CChkSGFiles.PgnoFromFileOffset 函数

**适用于：Exchange Server** 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013 年
  
返回与物理数据库文件中指定的字节索引相对应的逻辑数据库页码。 如果文件偏移量无效，或者尚未为数据库调用 **ErrCheckDbHeaders** 函数，则此函数返回 0 (零) 。 
  
```cs
Vitual ULONGPgnoFromFileOffset  
(
    Const ULONGLONGibFileOffset
);

```

## <a name="parameters"></a>参数

### <a name="ibfileoffset"></a>ibmFileOffset
  
输入参数。 数据库文件偏移量（以字节为单位）。
    
## <a name="return-value"></a>返回值

包含指定偏移的数据库文件的逻辑页码。
  
## <a name="remarks"></a>注解

如果 **ibfileOffset** 参数无效， **则 PgnoFromFileOffset** 函数返回 0 (0) 。 
  
如果没有在 **CCheckSGFiles** 实例上调用 **ErrCheckDbHeaders** 函数) **PgnoFromFileOffset** 也会返回 0 (0。 必须调用 **ErrCheckDbHeaders** 以初始化数据库页面大小和分配给数据库标头的页数。 
  
您应该使用 **PgnoFromFileOffset** 填充 **PAGE \_ INFO** 结构元素，以准备调用 **ErrCheckDbPages**。 **ErrCheckDbPages** 的 **rgPageInfo** 参数要求数组中每个元素都是一个 PAGE_INFO 结构，并正确初始化 **ulPgno** 成员值。 
  
如果在多线程应用程序中使用 CHKSGFILES，可以在应用程序的多线程部分调用 **PgnoFromFileOffset** 函数。 请注意，您通常会针对所检查的每个数据库多次调用此函数。 
  
## <a name="requirements"></a>Requirements

Exchange Server 2013 仅包括 64 位版本的 CHKSGFILES API。
  
运行应用程序的帐户必须具有对要检查的数据库和日志文件的读取权限。
  

