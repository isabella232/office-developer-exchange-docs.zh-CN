---
title: CChkSGFiles.New 函数
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- New
api_type:
- dllExport
ms.assetid: 588d8c74-c9ce-4d5e-8a79-a2a68676e858
description: 上次修改时间：2013 年 2 月 22 日
ms.openlocfilehash: e50b41e761b8e46d778011b6bac3db4dbb624809
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516270"
---
# <a name="cchksgfilesnew-function"></a>CChkSGFiles.New 函数

**适用于：Exchange Server** 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013 年
  
创建 **CChkSGFiles** 类的新实例。 必须先调用此函数，然后才能指定要检查的存储组和数据库。 
  
```cs
Static CCheckSGFiles  * __stdcall New  ();

```

## <a name="parameters"></a>参数

无。
  
## <a name="return-value"></a>返回值

指向 (对象的) 引用。
  
## <a name="remarks"></a>注解

**New** 函数创建一个 **CCheckSGFiles** 对象，并返回对该对象 (指针) 调用方。 在调用 **CCheckSGFiles** 类中的其他任何函数之前，必须调用此函数。 
  
如果在多线程应用程序中使用 CHKSGFILES，则必须在应用程序的单线程部分调用 **New** 函数，并且只能针对每个 **CCheckSGFiles** 对象调用它一次。 
  
## <a name="requirements"></a>Requirements

Exchange 2013 仅包括 64 位版本的 CHKSGFILES API。
  
运行应用程序的帐户必须具有对要检查的数据库和日志文件的读取访问权限。
  

