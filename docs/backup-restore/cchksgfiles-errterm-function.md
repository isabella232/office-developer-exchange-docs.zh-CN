---
title: CChkSGFiles.ErrTerm 函数
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ErrTerm
api_type:
- dllExport
ms.assetid: eea20a55-4a2a-4209-ae79-dc1ee1cd631b
description: 上次修改时间：2013 年 2 月 25 日
ms.openlocfilehash: 152fd613ef461d8c1ef69401237cfea09cd32b08
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516284"
---
# <a name="cchksgfileserrterm-function"></a>CChkSGFiles.ErrTerm 函数
  
**适用于：Exchange Server** 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013 年
  
提供数据库和日志验证的总体状态，指示是否已成功验证所有数据库页和日志。
  
> [!IMPORTANT]
> 存储 2013 年 10 月Exchange组。 为了与 Exchange 2010 Exchange Server版本中的数据库和存储组向后兼容，CHKSGFILES API 允许您指定存储组。 对 2013 Exchange CHKSGFILES 时，应该将指定存储组标识符的参数设置为空字符串。 
  
```cs
Vitual ERRErrTerm 
(
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a>参数

### <a name="ulflags"></a>ulFlags
  
可选输入参数。 保留此值以供将来使用。 此参数传递的值应为 0， (0) 。
    
## <a name="return-value"></a>返回值

ERR [枚举中的错误](cchksgfiles-err-enumeration.md) 代码。 
  
## <a name="remarks"></a>注解

**CChkSGFiles** 对象确定是否实际检查了使用 **ErrInit** 函数注册的所有数据库。 此对象使用 **ErrCheckDbPages** 函数验证是否实际验证 **了由 ErrCheckDbHeaders** 函数标识的相同数量的数据库页。 如果未成功检查每个数据库中的正确页数， **则 ErrTerm** 函数将返回错误。 
  
如果使用 **ErrCheckDbPages** 检查的数据库页数小于 **ErrCheckDbHeaders** 指示的数量，则此函数在 Windows 事件日志中创建一个错误，**并且 ErrTerm** 将返回错误。 
  
如果使用 **ErrCheckDbPages** 检查的数据库页数大于 **ErrCheckDbHeaders** 指示的数量，则此函数将在 Windows 事件日志中创建一条警告，以指示应用程序可能不必要地检查某些数据库页多次。 但在这种情况下 **，ErrTerm** 函数成功。 
  
**CChkSGFiles** 对象还确定是否实际检查了通过 **ErrInit** 注册的日志文件。 如果未成功检查所有日志 **，ErrTerm** 函数将返回错误。 
  
当 **ErrTerm** 返回错误时，它将是它找到的第一个错误，即使它会检查使用 **ErrInit** 注册的所有数据库的验证状态。
  
如果在多线程应用程序中使用 CHKSGFILES，则必须在应用程序的单线程部分调用 **ErrTerm** 函数，并且每个 **CCheckSGFiles** 对象只能调用一次。 
  
## <a name="requirements"></a>Requirements

Exchange 2013 仅包括 64 位版本的 CHKSGFILES。
  
运行应用程序的帐户必须具有对要检查的数据库和日志文件的读取访问权限。
  

