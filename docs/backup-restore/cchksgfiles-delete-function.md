---
title: CChkSGFiles 函数
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
description: 上次修改时间：2013年2月22日
ms.openlocfilehash: 38cb72b42727855f652de607bb2a02ecdeaae16e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44447048"
---
# <a name="cchksgfilesdelete-function"></a>CChkSGFiles 函数

**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013
  
销毁**CChkSGFiles**类的现有实例。 在应用程序完成对指定对象的操作后，必须调用此函数。 
  
```cs
Static VOID __stdcall Delete 
(
        CCheckSGFiles  * pcchecksgfiles
);

```

## <a name="parameters"></a>参数

### <a name="pcchecksgfiles"></a>pcchecksgfiles 
  
输入参数。 指向现有**CCheckSGFiles**对象的指针。 然后，将释放与该对象关联的内存。 
    
## <a name="return-value"></a>返回值

无。
  
## <a name="remarks"></a>说明

**Delete**函数释放与**CCheckSGFiles**对象相关联的内存。 调用**Delete**后，在*pcchecksgfiles*参数中传递的指针将无效，并且无法对该对象执行其他操作。 
  
如果应用程序使用**ErrCheckDbPages**函数，应用程序必须手动释放内存缓冲区;**删除**函数将无法释放它。 
  
如果要在多线程应用程序中使用 CHKSGFILES，则必须在应用程序的单线程部分调用 Delete 函数，并且只能为每个**CCheckSGFiles**对象调用一次**Delete**函数。 
  
## <a name="requirements"></a>Requirements

Exchange 2013 仅包含64位版本的 CHKSGFILES API。
  
运行应用程序所使用的帐户必须具有对要检查的数据库和日志文件的读取访问权限。
  

