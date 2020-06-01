---
title: CChkSGFiles 枚举
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
description: 上次修改时间：2015 年 3 月 9 日
ms.openlocfilehash: dbc76601a808f79ce3ed5b5dc9fbe4cf92efb015
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455252"
---
# <a name="cchksgfileserr-enumeration"></a>CChkSGFiles 枚举 
  
**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013
  
指示被调用函数的结果。 **CCheckSGFiles**类的多个函数返回此枚举。 
  
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
|errTaskDropped  <br/> |-106  <br/> |由**ErrTerm**函数返回以指示并不检查所有数据库页和事务日志文件，或者在验证过程中遇到错误。  <br/> |
|errRequiredLogFilesMissing  <br/> |-543  <br/> |在日志文件路径中找不到将数据库引入干净关闭状态所需的一个或多个日志文件，或者没有指定的三个字母的基本名称。  <br/> |
|errInvalidParameter  <br/> |-1003  <br/> |传递给函数的一个或多个参数无效。  <br/> |
|errOutOfMemory  <br/> |-1011  <br/> |可用内存不足，无法完成所请求的操作。  <br/> |
|errReadVerifyFailure  <br/> |-1018  <br/> |存储在数据库页面上的校验和与它的预期校验和不匹配。  <br/> |
|errTooManyActiveUsers  <br/> |-1059  <br/> |当仍在使用对象时，调用**ErrTerm**函数。 如果在**ErrCheckDbPages**或**ErrCheckLogFiles**返回之前调用**ErrTerm** ，则可能会发生此情况。  <br/> |
   
## <a name="requirements"></a>Requirements

Exchange Server 2013 仅包含64位版本的 CHKSGFILES API。
  
运行应用程序所使用的帐户必须具有对要检查的数据库和日志文件的读取访问权限。
  

