---
title: CChkSGFiles.Delete 函数
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Delete
api_type:
- dllExport
ms.assetid: 869e927f-7df2-4247-88ef-b8b05b29a700
description: 上次修改时间： 2013 年 2 月 22 日
ms.openlocfilehash: 5c41007a797e5a256692b2c4bdcb3cfae82c12ab
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752688"
---
# <a name="cchksgfilesdelete-function"></a>CChkSGFiles.Delete 函数

**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013
  
销毁现有**CChkSGFiles**类的实例。 应用程序已完成使用指定的对象后，必须调用此函数。 
  
```cs
Static VOID __stdcall Delete 
(
        CCheckSGFiles  * pcchecksgfiles
);

```

## <a name="parameters"></a>参数

### <a name="pcchecksgfiles"></a>pcchecksgfiles 
  
输入的参数。 指向现有**CCheckSGFiles**对象的指针。 将然后释放与对象关联的内存。 
    
## <a name="return-value"></a>返回值

无。
  
## <a name="remarks"></a>注解

**删除**函数释放与**CCheckSGFiles**对象关联的内存。 您调用**删除**后，将无效*pcchecksgfiles*参数中传递的指针，可以对该对象执行任何其他操作。 
  
应用程序的应用程序使用**ErrCheckDbPages**函数，如果必须手动; 释放内存缓冲区**删除**函数不将其释放。 
  
如果您使用 CHKSGFILES 多线程应用程序中，必须**删除**函数调用的应用程序的单线程部分中，且您可以为每个**CCheckSGFiles**对象调用它仅执行一次。 
  
## <a name="requirements"></a>要求

Exchange 2013 只包括 CHKSGFILES API 的 64 位版本。
  
下运行该应用程序的帐户必须具有对要检查的数据库和日志文件的读取访问权限。
  

