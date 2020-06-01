---
title: CChkSGFiles 函数
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
description: 上次修改时间：2013年3月3日
ms.openlocfilehash: c881691e7c1ba83a396e659f6aac0328625e49a5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457009"
---
# <a name="cchksgfileserrinit-function"></a>CChkSGFiles 函数
  
**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013
  
通过指定要检查的数据库以及要检查的事务日志文件的路径和基名称来初始化**CChkSGFiles**对象。 应用程序应在成功调用**新**函数后立即调用此函数。 
  
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
  
输入参数。 指定要检查的数据库的数组。 每个 array 元素都是一个以 null 结尾的 Unicode 字符串，其中包含要检查的数据库的路径和文件名。
    
### <a name="cdb"></a>cDB
  
输入参数。 **RgwszDb**数组中的有效数据库路径元素的数目。 
    
#### <a name="wszlogpath"></a>wszLogPath
  
输入参数。 要检查的事务日志文件的完整路径（以以 null 结尾的 Unicode 字符串的形式）。
    
### <a name="wszbasename"></a>wszBaseName
  
输入参数。 以 null 结尾的 Unicode 字符串形式的 Exchange 事务日志文件的三个字母的基本名称。
    
### <a name="ulflags"></a>ulFlags
  
可选的输入参数。 保留此值以供将来使用。 此参数传递的值应为0（零）。
    
## <a name="return-value"></a>返回值

[ERR](cchksgfiles-err-enumeration.md)枚举中的错误代码。 
  
## <a name="remarks"></a>备注

**ErrInit**函数注册要检查的数据库和日志文件。 调用**新**函数之后，但在调用任何其他**ChkSGFiles**函数之前，必须调用此函数。 
  
您必须提供所有数据库名称、日志文件路径和基名称，以以 null 结尾的 Unicode 字符串。
  
您可以只检查数据库文件、仅检查日志文件，还是同时检查数据库和日志文件。 但是，在调用此函数时，应用程序必须指定至少一个要检查的实体。 为**cDB**传递0（零）， **wszLogPath**的 NULL 值将返回一个错误。 
  
如果**cDB**的值不是0（零），则为**rgwszDb**传递 NULL 将导致错误。 若要检查数据库文件，应用程序必须提供数据库名称。 
  
如果为**wszBaseName**传递了 null，但**WSZLOGPATH**不为 null，则将返回错误。 检查日志文件时，总是需要使用日志文件基名称。 
  
如果要在多线程应用程序中使用 CHKSGFILES，则必须在应用程序的单线程部分调用**ErrInit**函数，并且只能为每个**CCheckSGFiles**对象调用一次该函数。 
  
## <a name="requirements"></a>Requirements

Exchange 2013 仅包含64位版本的 CHKSGFILES API。
  
运行应用程序所使用的帐户必须具有对要检查的数据库和日志文件的读取访问权限。
  

