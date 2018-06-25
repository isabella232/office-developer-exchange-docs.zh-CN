---
title: CChkSGFiles.New 函数
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
description: 上次修改时间： 2013 年 2 月 22 日
ms.openlocfilehash: b40f8b1a95477715b29defb4addabfb333e92d04
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752682"
---
# <a name="cchksgfilesnew-function"></a>CChkSGFiles.New 函数

**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013
  
创建**CChkSGFiles**类的新实例。 您可以指定要检查的存储组和数据库之前，必须调用此函数。 
  
```cs
Static CCheckSGFiles  * __stdcall New  ();

```

## <a name="parameters"></a>参数

无。
  
## <a name="return-value"></a>返回值

对新创建的对象的引用 （指针）。
  
## <a name="remarks"></a>注解

**新建**函数创建**CCheckSGFiles**对象，并返回到呼叫者对该对象的引用 （指针）。 任何其他函数调用**CCheckSGFiles**类中之前，必须调用此函数。 
  
如果您使用 CHKSGFILES 多线程应用程序中，您必须将应用程序的单线程部分调用**新建**函数，且您可以为每个**CCheckSGFiles**对象调用它仅执行一次。 
  
## <a name="requirements"></a>要求

Exchange 2013 只包括 CHKSGFILES API 的 64 位版本。
  
下运行该应用程序的帐户必须具有对要检查的数据库和日志文件的读取访问权限。
  

