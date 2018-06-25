---
title: CChkSGFiles.ERR 枚举
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ERR
api_type:
- dllExport
ms.assetid: f0efe195-91c3-4f3a-8c7d-e5dba336465a
description: 上次修改时间： 2015 年 3 月 9 日
ms.openlocfilehash: 20f10c43e3b92604bb51e1aa5f896a8bd7c4b335
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753633"
---
# <a name="cchksgfileserr-enumeration"></a>CChkSGFiles.ERR 枚举 
  
**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013
  
指示被调用的函数的结果。 此枚举由**CCheckSGFiles**类的多个函数返回。 
  
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
|errSuccess  <br/> |0  <br/> |没有任何错误完成函数。  <br/> |
|errTaskDropped  <br/> |-106  <br/> |返回由**ErrTerm**函数，以指示已选中不是所有数据库页面和事务日志文件，或验证期间遇到了错误。  <br/> |
|errRequiredLogFilesMissing  <br/> |-543  <br/> |一个或多个日志文件所需数据库置于干净关闭状态找不到在日志文件路径，或没有指定三个字母的基名称。  <br/> |
|errInvalidParameter  <br/> |-1003  <br/> |一个或多个已传递给函数的参数无效。  <br/> |
|errOutOfMemory  <br/> |-1011  <br/> |内存不足时可用于完成请求的操作。  <br/> |
|errReadVerifyFailure  <br/> |-1018  <br/> |在数据库页上存储的校验和与其预期的校验和不匹配。  <br/> |
|errTooManyActiveUsers  <br/> |-1059  <br/> |仍使用该对象时调用了**ErrTerm**函数。 发生这种情况**ErrTerm**称为之前**ErrCheckDbPages**或返回**ErrCheckLogFiles**了。  <br/> |
   
## <a name="requirements"></a>要求

Exchange Server 2013 只包括 CHKSGFILES API 的 64 位版本。
  
下运行该应用程序的帐户必须具有对要检查的数据库和日志文件的读取访问权限。
  

