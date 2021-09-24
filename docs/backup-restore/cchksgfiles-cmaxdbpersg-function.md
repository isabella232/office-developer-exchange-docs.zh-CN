---
title: CChkSGFiles.CMaxDbPerSG 函数
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CMaxDbPerSG
api_type:
- dllExport
ms.assetid: 5871988b-a5d7-42cc-9b83-8fededb5072f
description: 上次修改时间：2013 年 2 月 22 日
ms.openlocfilehash: 1a82e71afde4766734d0875f68d7932a9fd9f26a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510523"
---
# <a name="cchksgfilescmaxdbpersg-function"></a>CChkSGFiles.CMaxDbPerSG 函数

**适用于：Exchange Server** 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013 年
  
返回单个数据库服务器存储组中允许的最大Exchange数。
  
```cs
Static ULONG  __stdcall CMaxDbPerSG  ();

```

## <a name="parameters"></a>参数

无。
  
## <a name="return-value"></a>返回值

指定的服务器允许每个存储Exchange的最大数据库数。 因为存储组不是 2013 Exchange的一部分，所以此函数返回 1。
  
## <a name="remarks"></a>注解

您可以使用 **CCheckSGFiles** 对象来验证数据库 (和事务日志文件) 在一个存储组中，因此 **CMaxDbPerSG** 函数返回的值还表示可以使用 **CCheckSGFiles** 类的实例检查的最大数据库数。 
  
请注意，默认情况下，Exchange Server 2003 Exchange Server 2007 允许每个存储组最多有五个数据库。
  
## <a name="requirements"></a>Requirements

Exchange 2013 仅包括 64 位版本的 CHKSGFILES API。
  
运行应用程序的帐户必须具有对要检查的数据库和日志文件的读取访问权限。
  

