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
# <a name="cchksgfilesnew-function"></a><span data-ttu-id="7b3c4-103">CChkSGFiles.New 函数</span><span class="sxs-lookup"><span data-stu-id="7b3c4-103">CChkSGFiles.New function</span></span>

<span data-ttu-id="7b3c4-104">**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="7b3c4-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="7b3c4-105">创建**CChkSGFiles**类的新实例。</span><span class="sxs-lookup"><span data-stu-id="7b3c4-105">Creates a new instance of the **CChkSGFiles** class.</span></span> <span data-ttu-id="7b3c4-106">您可以指定要检查的存储组和数据库之前，必须调用此函数。</span><span class="sxs-lookup"><span data-stu-id="7b3c4-106">You must call this function before you can specify the storage group and databases to be checked.</span></span> 
  
```cs
Static CCheckSGFiles  * __stdcall New  ();

```

## <a name="parameters"></a><span data-ttu-id="7b3c4-107">参数</span><span class="sxs-lookup"><span data-stu-id="7b3c4-107">Parameters</span></span>

<span data-ttu-id="7b3c4-108">无。</span><span class="sxs-lookup"><span data-stu-id="7b3c4-108">None.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="7b3c4-109">返回值</span><span class="sxs-lookup"><span data-stu-id="7b3c4-109">Return value</span></span>

<span data-ttu-id="7b3c4-110">对新创建的对象的引用 （指针）。</span><span class="sxs-lookup"><span data-stu-id="7b3c4-110">A reference (pointer) to the newly created object.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7b3c4-111">注解</span><span class="sxs-lookup"><span data-stu-id="7b3c4-111">Remarks</span></span>

<span data-ttu-id="7b3c4-112">**新建**函数创建**CCheckSGFiles**对象，并返回到呼叫者对该对象的引用 （指针）。</span><span class="sxs-lookup"><span data-stu-id="7b3c4-112">The **New** function creates a **CCheckSGFiles** object and returns to the caller a reference (pointer) to that object.</span></span> <span data-ttu-id="7b3c4-113">任何其他函数调用**CCheckSGFiles**类中之前，必须调用此函数。</span><span class="sxs-lookup"><span data-stu-id="7b3c4-113">You must call this function before it calls any of the other functions in the **CCheckSGFiles** class.</span></span> 
  
<span data-ttu-id="7b3c4-114">如果您使用 CHKSGFILES 多线程应用程序中，您必须将应用程序的单线程部分调用**新建**函数，且您可以为每个**CCheckSGFiles**对象调用它仅执行一次。</span><span class="sxs-lookup"><span data-stu-id="7b3c4-114">If you're using CHKSGFILES in a multithreaded application, you must call the **New** function in the single-threaded portion of the application, and you can call it only once for each **CCheckSGFiles** object.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="7b3c4-115">要求</span><span class="sxs-lookup"><span data-stu-id="7b3c4-115">Requirements</span></span>

<span data-ttu-id="7b3c4-116">Exchange 2013 只包括 CHKSGFILES API 的 64 位版本。</span><span class="sxs-lookup"><span data-stu-id="7b3c4-116">Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="7b3c4-117">下运行该应用程序的帐户必须具有对要检查的数据库和日志文件的读取访问权限。</span><span class="sxs-lookup"><span data-stu-id="7b3c4-117">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

