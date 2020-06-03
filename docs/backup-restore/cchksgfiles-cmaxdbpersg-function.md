---
title: CChkSGFiles 函数
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
description: 上次修改时间：2013年2月22日
ms.openlocfilehash: b7c3517779eb07ef053c1dd4fa25544310fb3343
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455259"
---
# <a name="cchksgfilescmaxdbpersg-function"></a>CChkSGFiles 函数

**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013
  
返回单个 Exchange server 存储组中允许的最大数据库数。
  
```cs
Static ULONG  __stdcall CMaxDbPerSG  ();

```

## <a name="parameters"></a>参数

无。
  
## <a name="return-value"></a>返回值

指定的 Exchange 服务器允许每个存储组的最大数据库数。 因为存储组不是 Exchange 2013 的一部分，所以此函数返回1。
  
## <a name="remarks"></a>备注

您可以使用**CCheckSGFiles**对象来验证仅在一个存储组中的数据库（和事务日志文件），因此**CMaxDbPerSG**函数返回的值还表示您可以使用**CCheckSGFiles**类的实例进行检查的数据库的最大数量。 
  
请注意，默认情况下，Exchange Server 2003 和 Exchange Server 2007 允许每个存储组最多5个数据库。
  
## <a name="requirements"></a>Requirements

Exchange 2013 仅包含64位版本的 CHKSGFILES API。
  
运行应用程序所使用的帐户必须具有对要检查的数据库和日志文件的读取访问权限。
  

