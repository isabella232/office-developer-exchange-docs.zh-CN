---
title: CChkSGFiles.ErrInit 函数
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ErrInit
api_type:
- dllExport
ms.assetid: 61bb3af1-8b51-4bae-8e25-90a4dc1226c5
description: 上次修改时间：2013 年 3 月 3 日
ms.openlocfilehash: ccb5293e35f20328181c4cf1cb5f0eddbb42e03f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516291"
---
# <a name="cchksgfileserrinit-function"></a>CChkSGFiles.ErrInit 函数
  
**适用于：Exchange Server** 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013 年
  
通过指定要检查的数据库以及要检查的事务日志文件的路径和基名称来初始化 **CChkSGFiles** 对象。 应用程序应在成功调用 New 函数后立即调用 **此** 函数。 
  
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

### <a name="rgwszdb"></a>rgwszDb[]
  
输入参数。 一个指定要检查的数据库的数组。 每个数组元素都是以 null 结尾的 Unicode 字符串，其中包含要检查的数据库的路径和文件名。
    
### <a name="cdb"></a>cDB
  
输入参数。 **rgwszDb** 数组中有效数据库路径元素的数量。 
    
#### <a name="wszlogpath"></a>wszLogPath
  
输入参数。 要检查的事务日志文件的完整路径，格式为以 null 结尾的 Unicode 字符串。
    
### <a name="wszbasename"></a>wszBaseName
  
输入参数。 事务日志文件的三个字母Exchange，格式为以 null 结尾的 Unicode 字符串。
    
### <a name="ulflags"></a>ulFlags
  
可选输入参数。 保留此值以供将来使用。 此参数传递的值应为 0， (0) 。
    
## <a name="return-value"></a>返回值

ERR [枚举中的错误](cchksgfiles-err-enumeration.md) 代码。 
  
## <a name="remarks"></a>注解

**ErrInit** 函数注册要检查的数据库和日志文件。 在调用 **New** 函数之后、调用任何其他 **ChkSGFiles** 函数之前，必须调用此函数。 
  
必须提供所有数据库名称、日志文件路径和基名称作为以 null 终止的 Unicode 字符串。
  
您可以只检查数据库文件、仅检查日志文件，也可以同时检查数据库和日志文件。 但是，在调用此函数时，应用程序必须指定至少一个要检查的实体。 如果为  **cDB**  (0) 零值，为  **wszLogPath**  传递 NULL 将返回错误。 
  
如果  **cDB**  的值不是 0， (0) ，则为  **rgwszDb**  传递 NULL 将导致错误。 若要检查数据库文件，应用程序必须提供数据库名称。 
  
如果为  **wszBaseName**  传递 NULL，但  **wszLogPath**  不为 NULL，则返回错误。 检查日志文件始终需要一个基本名称。 
  
如果在多线程应用程序中使用 CHKSGFILES，则必须在应用程序的单线程部分调用 **ErrInit** 函数，并且只能针对每个 **CCheckSGFiles** 对象调用它一次。 
  
## <a name="requirements"></a>Requirements

Exchange 2013 仅包括 64 位版本的 CHKSGFILES API。
  
运行应用程序的帐户必须具有对要检查的数据库和日志文件的读取访问权限。
  

