---
title: CChkSGFiles 函数
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
description: 上次修改时间：2013年2月25日
ms.openlocfilehash: 12b07fba69054d327c7250bbf83e4c77016e8b3f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466197"
---
# <a name="cchksgfileserrterm-function"></a>CChkSGFiles 函数
  
**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013
  
提供数据库和日志验证的总体状态，以指示是否已成功验证所有数据库页和日志。
  
> [!IMPORTANT]
> 存储组在 Exchange 2013 中不可用。 为了在 exchange Server 2010 之前的 Exchange 版本中与数据库和存储组保持向后兼容性，CHKSGFILES API 使您能够指定存储组。 当您针对 Exchange 2013 数据库运行 CHKSGFILES 时，应将指定存储组标识符的参数设置为空字符串。 
  
```cs
Vitual ERRErrTerm 
(
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a>参数

### <a name="ulflags"></a>ulFlags
  
可选的输入参数。 保留此值以供将来使用。 此参数传递的值应为0（零）。
    
## <a name="return-value"></a>返回值

[ERR](cchksgfiles-err-enumeration.md)枚举中的错误代码。 
  
## <a name="remarks"></a>备注

**CChkSGFiles**对象确定是否实际检查了使用**ErrInit**函数注册的所有数据库。 此对象使用**ErrCheckDbPages**函数验证是否实际验证了**ErrCheckDbHeaders**函数所标识的相同数量的数据库页。 如果未成功检查每个数据库中的正确数量的页面， **ErrTerm**函数将返回一个错误。 
  
如果使用**ErrCheckDbPages**选中的数据库页面的数量小于**ErrCheckDbHeaders**所指示的数目，则此函数会在 Windows 事件日志中创建一个错误， **ErrTerm**将返回错误。 
  
如果使用**ErrCheckDbPages**检查的数据库页面的数量大于**ErrCheckDbHeaders**所指示的数目，则此函数会在 Windows 事件日志中创建一个警告，以指示该应用程序可能不需要多次检查某些数据库页。 但在这种情况下， **ErrTerm**函数将成功。 
  
**CChkSGFiles**对象还确定是否实际检查了在**ErrInit**中注册的日志文件。 如果未成功检查所有日志， **ErrTerm**函数将返回一个错误。 
  
当**ErrTerm**返回错误时，它将是它找到的第一个错误，即使它检查所有注册到**ErrInit**的数据库的验证状态。
  
如果要在多线程应用程序中使用 CHKSGFILES，则必须在应用程序的单线程部分调用**ErrTerm**函数，并且对于每个**CCheckSGFiles**对象，您可以调用该函数，而不能超过一次。 
  
## <a name="requirements"></a>Requirements

Exchange 2013 仅包含64位版本的 CHKSGFILES。
  
运行应用程序所使用的帐户必须具有对要检查的数据库和日志文件的读取访问权限。
  

