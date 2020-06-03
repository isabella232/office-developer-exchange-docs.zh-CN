---
title: CChkSGFiles 函数
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- New
api_type:
- dllExport
ms.assetid: 588d8c74-c9ce-4d5e-8a79-a2a68676e858
description: 上次修改时间：2013年2月22日
ms.openlocfilehash: d18d3ef20890012a1d8c193ec87bdca10a1ed451
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455231"
---
# <a name="cchksgfilesnew-function"></a>CChkSGFiles 函数

**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013
  
创建**CChkSGFiles**类的新实例。 您必须先调用此函数，然后才能指定要检查的存储组和数据库。 
  
```cs
Static CCheckSGFiles  * __stdcall New  ();

```

## <a name="parameters"></a>参数

无。
  
## <a name="return-value"></a>返回值

对新创建的对象的引用（指针）。
  
## <a name="remarks"></a>备注

**新**函数创建一个**CCheckSGFiles**对象，并向调用方返回指向该对象的引用（指针）。 在调用**CCheckSGFiles**类中的任何其他函数之前，必须先调用此函数。 
  
如果要在多线程应用程序中使用 CHKSGFILES，则必须在应用程序的单线程部分调用新函数，并且只能为每个**CCheckSGFiles**对象调用一次**新**函数。 
  
## <a name="requirements"></a>Requirements

Exchange 2013 仅包含64位版本的 CHKSGFILES API。
  
运行应用程序所使用的帐户必须具有对要检查的数据库和日志文件的读取访问权限。
  

