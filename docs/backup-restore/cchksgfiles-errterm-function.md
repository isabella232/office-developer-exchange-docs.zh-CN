---
title: CChkSGFiles.ErrTerm 函数
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ErrTerm
api_type:
- dllExport
ms.assetid: eea20a55-4a2a-4209-ae79-dc1ee1cd631b
description: 上次修改时间： 2013 年 2 月 25 日
ms.openlocfilehash: 099ec33663baa2414a0c28b90364523b6191c697
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752692"
---
# <a name="cchksgfileserrterm-function"></a>CChkSGFiles.ErrTerm 函数
  
**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013
  
提供数据库和日志验证，这表明已成功验证是否所有数据库页和日志的总体状态。
  
> [!IMPORTANT]
> 存储组不可用在 Exchange 2013。 与数据库和存储组的 Exchange 版本早于 Exchange Server 2010 中的向后兼容性，CHKSGFILES API 可以指定存储组。 针对 Exchange 2013 数据库运行 CHKSGFILES 时，您应设置为空字符串的存储组标识符指定的参数。 
  
```cs
Vitual ERRErrTerm 
(
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a>参数

### <a name="ulflags"></a>ulFlags
  
可选的输入的参数。 此值保留以供将来使用。 通过此参数传递的值应为 0 （零）。
    
## <a name="return-value"></a>返回值

从[ERR](cchksgfiles-err-enumeration.md)枚举错误代码。 
  
## <a name="remarks"></a>注解

**CChkSGFiles**对象确定是否已实际签**ErrInit**函数注册的所有数据库。 此对象使用**ErrCheckDbPages**函数以验证相同数量的页面由**ErrCheckDbHeaders**函数实际上已验证的数据库。 如果正确的每个数据库中的页面数不成功进行检查，则**ErrTerm**函数将返回错误。 
  
如果数据库网页保持为签与**ErrCheckDbPages**数少于的由**ErrCheckDbHeaders**，此函数在 Windows 事件日志中，创建一条错误，并**ErrTerm**返回错误。 
  
此函数使用**ErrCheckDbPages**检查数据库页面的数量大于**ErrCheckDbHeaders**所指示的如果在 Windows 事件日志，以指示的应用程序可能不必要地检查某些中创建一条警告数据库页多次。 在这种情况下，但是， **ErrTerm**函数成功。 
  
**CChkSGFiles**对象还决定是否已实际签注册**ErrInit**的日志文件。 如果未成功签所有日志， **ErrTerm**函数将返回错误。 
  
当**ErrTerm**返回错误时，它将发现的第一个错误，即使它检查**ErrInit**注册的所有数据库的验证状态。
  
如果您使用 CHKSGFILES 多线程应用程序中，您必须将应用程序的单线程部分调用**ErrTerm**函数且您可以调用它不能超过一次为每个**CCheckSGFiles**对象。 
  
## <a name="requirements"></a>要求

Exchange 2013 只包括 CHKSGFILES 的 64 位版本。
  
下运行该应用程序的帐户必须具有对要检查的数据库和日志文件的读取访问权限。
  

