---
title: CChkSGFiles.CMaxDbPerSG 函数
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CMaxDbPerSG
api_type:
- dllExport
ms.assetid: 5871988b-a5d7-42cc-9b83-8fededb5072f
description: 上次修改时间： 2013 年 2 月 22 日
ms.openlocfilehash: bf09074bab6dee13e97e8a59a22ae1b19522a5e5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753650"
---
# <a name="cchksgfilescmaxdbpersg-function"></a>CChkSGFiles.CMaxDbPerSG 函数

**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013
  
返回数据库中一个 Exchange 服务器存储组允许的最大数目。
  
```cs
Static ULONG  __stdcall CMaxDbPerSG  ();

```

## <a name="parameters"></a>参数

无。
  
## <a name="return-value"></a>返回值

指定的 Exchange 服务器允许每个存储组的数据库的最大数目。 由于存储组不是 Exchange 2013 的一部分，此函数返回 1。
  
## <a name="remarks"></a>注解

您可以使用**CCheckSGFiles**对象，由**CMaxDbPerSG**函数返回的值还代表您可以通过使用检查的数据库的最大数目，以便只有一个存储组中，验证数据库 （和事务日志文件）**CCheckSGFiles**类的实例。 
  
请注意，默认情况下，Exchange Server 2003 和 Exchange Server 2007 允许每个存储组的五个数据库的最大值。
  
## <a name="requirements"></a>要求

Exchange 2013 只包括 CHKSGFILES API 的 64 位版本。
  
下运行该应用程序的帐户必须具有对要检查的数据库和日志文件的读取访问权限。
  

