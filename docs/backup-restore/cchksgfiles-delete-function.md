---
title: CChkSGFiles.Delete 函数
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Delete
api_type:
- dllExport
ms.assetid: 869e927f-7df2-4247-88ef-b8b05b29a700
description: 上次修改时间：2013 年 2 月 22 日
ms.openlocfilehash: cf1c23dd75442d73dfea49e0831d0859da321a40
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510538"
---
# <a name="cchksgfilesdelete-function"></a>CChkSGFiles.Delete 函数

**适用于：Exchange Server** 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013 年
  
销毁 **CChkSGFiles 类** 的现有实例。 您必须在应用程序完成对指定对象的处理后调用此函数。 
  
```cs
Static VOID __stdcall Delete 
(
        CCheckSGFiles  * pcchecksgfiles
);

```

## <a name="parameters"></a>参数

### <a name="pcchecksgfiles"></a>pcchecksgfiles 
  
输入参数。 指向现有 **CCheckSGFiles 对象的** 指针。 然后，将释放与对象关联的内存。 
    
## <a name="return-value"></a>返回值

无。
  
## <a name="remarks"></a>注解

**Delete** 函数释放与 **CCheckSGFiles** 对象关联的内存。 调用 **Delete 后***，pcchecksgfiles* 参数中传递的指针将无效，并且无法对该对象执行任何其他操作。 
  
如果应用程序使用 **ErrCheckDbPages** 函数，则应用程序必须手动释放内存缓冲区; **Delete** 函数不会释放它。 
  
如果在多线程应用程序中使用 CHKSGFILES，则必须在应用程序的单线程部分调用 **Delete** 函数，并且只能针对每个 **CCheckSGFiles** 对象调用它一次。 
  
## <a name="requirements"></a>Requirements

Exchange 2013 仅包括 64 位版本的 CHKSGFILES API。
  
运行应用程序的帐户必须具有对要检查的数据库和日志文件的读取访问权限。
  

