---
title: CChkSGFiles.NO_FLAGS 枚举
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- NO_FLAGS
api_type:
- dllExport
ms.assetid: 6b18b645-fec4-429a-9900-62ad0f19bf96
description: 上次修改时间： 2013 年 2 月 22 日
ms.openlocfilehash: dbe4cedf2011a1607a6db55dc064bd42dc229123
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753636"
---
# <a name="cchksgfilesnoflags-enumeration"></a><span data-ttu-id="50e72-103">CChkSGFiles.NO_FLAGS 枚举</span><span class="sxs-lookup"><span data-stu-id="50e72-103">CChkSGFiles.NO_FLAGS enumeration</span></span>

<span data-ttu-id="50e72-104">**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="50e72-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="50e72-105">充当大多数**CCheckSGFiles**类函数接受**ulFlags**参数的占位符值。</span><span class="sxs-lookup"><span data-stu-id="50e72-105">Serves as a placeholder value for the **ulFlags** parameters that are accepted by most **CCheckSGFiles** class functions.</span></span> 
  
```cs
Enum { NO_FLAGS = 0 }

```

## <a name="requirements"></a><span data-ttu-id="50e72-106">要求</span><span class="sxs-lookup"><span data-stu-id="50e72-106">Requirements</span></span>

<span data-ttu-id="50e72-107">Exchange Server 2013 只包括 CHKSGFILES API 的 64 位版本。</span><span class="sxs-lookup"><span data-stu-id="50e72-107">Exchange Server 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="50e72-108">下运行该应用程序的帐户必须具有对要检查的数据库和日志文件的读取访问权限。</span><span class="sxs-lookup"><span data-stu-id="50e72-108">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

