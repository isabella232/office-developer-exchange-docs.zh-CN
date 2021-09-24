---
title: CChkSGFiles.ERR 枚举
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ERR
api_type:
- dllExport
ms.assetid: f0efe195-91c3-4f3a-8c7d-e5dba336465a
description: 上次修改时间：2015 年 3 月 9 日
ms.openlocfilehash: 12cfff44a6dacbb07ee5518d0008092fbfb644d1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510461"
---
# <a name="cchksgfileserr-enumeration"></a>CChkSGFiles.ERR 枚举 
  
**适用于：Exchange Server** 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013 年
  
指示被调用的函数的结果。 此枚举由 **CCheckSGFiles** 类的许多函数返回。 
  
```cs
Enum ERR  
{
        errSuccess = 0,
        errTaskDropped = -106,
        errRequiredLogFilesMissing = -543,
        errInvalidParameter = -1003,
        errOutOfMemory = -1011,
        errReadVerifyFailure = -1018,
        errTooManyActiveUsers = -1059,
        errDatabaseCorrupted = -1206
}

```

## <a name="values"></a>值

|**成员名称**|**值**|**说明**|
|:-----|:-----|:-----|
|errSuccess  <br/> |0  <br/> |函数已完成，没有任何错误。  <br/> |
|errTaskDropped  <br/> |-106  <br/> |由 **ErrTerm** 函数返回，以指示并非所有数据库页和事务日志文件都经过检查，或者验证过程中遇到了错误。  <br/> |
|errRequiredLogFilesMissing  <br/> |-543  <br/> |在 日志文件 路径中找不到使数据库干净关闭状态所需的一个或多个日志文件，或者没有指定的三个字母的基本名称。  <br/> |
|errInvalidParameter  <br/> |-1003  <br/> |传递给函数的一个或多个参数无效。  <br/> |
|errOutOfMemory  <br/> |-1011  <br/> |内存不足，无法完成请求的操作。  <br/> |
|errReadVerifyFailure  <br/> |-1018  <br/> |存储在数据库页上的校验和与预期的校验和不匹配。  <br/> |
|errTooManyActiveUsers  <br/> |-1059  <br/> |在仍在使用对象时调用 **了 ErrTerm** 函数。 如果在 **ErrCheckDbPages** 或 **ErrCheckLogFiles** 返回之前调用 **ErrTerm，** 则可能发生此情况。  <br/> |
   
## <a name="requirements"></a>Requirements

Exchange Server 2013 仅包括 64 位版本的 CHKSGFILES API。
  
运行应用程序的帐户必须具有对要检查的数据库和日志文件的读取访问权限。
  

