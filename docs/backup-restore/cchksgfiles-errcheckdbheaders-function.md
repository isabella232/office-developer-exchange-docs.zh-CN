---
title: CChkSGFiles.ErrCheckDbHeaders 函数
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ErrCheckDbHeaders
api_type:
- dllExport
ms.assetid: 75289cd2-35b1-4f75-a651-dce01f1ddda1
description: 上次修改时间：2013 年 2 月 22 日
ms.openlocfilehash: 215a0d1126fce48b7e3800016619b0c52915312b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510468"
---
# <a name="cchksgfileserrcheckdbheaders-function"></a>CChkSGFiles.ErrCheckDbHeaders 函数

**适用于：Exchange Server** 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013 年 
  
验证 **ErrInit** 函数指定的数据库文件的标题。 此函数还返回每个指定数据库中的页面大小和页数。 
  
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

### <a name="pcbdbpagesize"></a>该页面 
  
输出参数。 每个指定数据库的页面大小（以字节为单位）。
    
### <a name="pcheaderpagesperdb"></a>pcHeaderPagesPerDb 
  
输出参数。 数据库引擎为内部使用保留的每个指定数据库的开头的页数。 请注意，不应 *将页* 眉页传递给 **ErrCheckDbPages** 函数进行验证。 
    
### <a name="pidberrorencountered"></a>piDbErrorEncountered
  
输出参数。 如果函数的返回值指示错误，则此参数将是传递给 **ErrInit** 函数 **的 rgwszDb[]** 数组的索引。 索引数组元素表示遇到错误的数据库。 如果函数未返回错误值，则此参数值无效。 
    
### <a name="ulflags"></a>ulFlags 
  
可选输入参数。 保留此值以供将来使用。 传递的值应为 0， (0) 。
    
## <a name="return-value"></a>返回值

此函数从 [CChkSGFiles.ERR 枚举中返回错误代码](cchksgfiles-err-enumeration.md)。
  
## <a name="remarks"></a>注解

**ErrCheckDbHeaders** 验证向 **ErrInit** 注册的所有数据库是否具有相同的日志签名和数据库页面大小。 您还可以使用最低 **genMin** 参数值和最高 **genMax** 参数值来确定使所有注册的数据库进入干净关闭状态所需的日志文件集。 
  
**piDbErrorEncountered** 参数仅在检测到错误时设置，如非零 **ErrCheckDbHeaders** 返回值所指示。 
  
在此函数中发生错误时，错误事件将添加到错误Windows日志中。
  
只有在调用 **ErrInit** 之后，才能调用 **ErrCheckDbHeaders，** 并且必须先调用它，然后才能调用 **ErrCheckDbPages** 和 **ErrCheckLogs**。
  
如果在多线程应用程序中使用 CHKSGFILES，则必须在单线程部分调用 **ErrCheckDbHeaders** 函数，并且只能针对每个 **CCheckSGFiles** 对象调用它一次。 
  
## <a name="requirements"></a>Requirements

Exchange 2013 仅包括 64 位版本的 CHKSGFILES API。
  
运行应用程序的帐户必须具有对要检查的数据库和日志文件的读取访问权限。
  

