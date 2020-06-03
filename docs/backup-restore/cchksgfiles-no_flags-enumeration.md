---
title: NO_FLAGS CChkSGFiles 枚举
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
description: 上次修改时间：2013年2月22日
ms.openlocfilehash: a55bcf2c845b6896105d446a14a70cc45fbc3de2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455357"
---
# <a name="cchksgfilesno_flags-enumeration"></a><span data-ttu-id="91dd4-103">NO_FLAGS CChkSGFiles 枚举</span><span class="sxs-lookup"><span data-stu-id="91dd4-103">CChkSGFiles.NO_FLAGS enumeration</span></span>

<span data-ttu-id="91dd4-104">**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="91dd4-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="91dd4-105">充当大多数**CCheckSGFiles**类函数接受的**ulFlags**参数的占位符值。</span><span class="sxs-lookup"><span data-stu-id="91dd4-105">Serves as a placeholder value for the **ulFlags** parameters that are accepted by most **CCheckSGFiles** class functions.</span></span> 
  
```cs
Enum { NO_FLAGS = 0 }

```

## <a name="requirements"></a><span data-ttu-id="91dd4-106">Requirements</span><span class="sxs-lookup"><span data-stu-id="91dd4-106">Requirements</span></span>

<span data-ttu-id="91dd4-107">Exchange Server 2013 仅包含64位版本的 CHKSGFILES API。</span><span class="sxs-lookup"><span data-stu-id="91dd4-107">Exchange Server 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="91dd4-108">运行应用程序所使用的帐户必须具有对要检查的数据库和日志文件的读取访问权限。</span><span class="sxs-lookup"><span data-stu-id="91dd4-108">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

