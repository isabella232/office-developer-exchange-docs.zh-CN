---
title: CChkSGFiles 函数
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
description: 上次修改时间：2013年2月22日
ms.openlocfilehash: d18d3ef20890012a1d8c193ec87bdca10a1ed451
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455231"
---
# <a name="cchksgfilesnew-function"></a><span data-ttu-id="e69ce-103">CChkSGFiles 函数</span><span class="sxs-lookup"><span data-stu-id="e69ce-103">CChkSGFiles.New function</span></span>

<span data-ttu-id="e69ce-104">**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="e69ce-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="e69ce-105">创建**CChkSGFiles**类的新实例。</span><span class="sxs-lookup"><span data-stu-id="e69ce-105">Creates a new instance of the **CChkSGFiles** class.</span></span> <span data-ttu-id="e69ce-106">您必须先调用此函数，然后才能指定要检查的存储组和数据库。</span><span class="sxs-lookup"><span data-stu-id="e69ce-106">You must call this function before you can specify the storage group and databases to be checked.</span></span> 
  
```cs
Static CCheckSGFiles  * __stdcall New  ();

```

## <a name="parameters"></a><span data-ttu-id="e69ce-107">参数</span><span class="sxs-lookup"><span data-stu-id="e69ce-107">Parameters</span></span>

<span data-ttu-id="e69ce-108">无。</span><span class="sxs-lookup"><span data-stu-id="e69ce-108">None.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="e69ce-109">返回值</span><span class="sxs-lookup"><span data-stu-id="e69ce-109">Return value</span></span>

<span data-ttu-id="e69ce-110">对新创建的对象的引用（指针）。</span><span class="sxs-lookup"><span data-stu-id="e69ce-110">A reference (pointer) to the newly created object.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e69ce-111">备注</span><span class="sxs-lookup"><span data-stu-id="e69ce-111">Remarks</span></span>

<span data-ttu-id="e69ce-112">**新**函数创建一个**CCheckSGFiles**对象，并向调用方返回指向该对象的引用（指针）。</span><span class="sxs-lookup"><span data-stu-id="e69ce-112">The **New** function creates a **CCheckSGFiles** object and returns to the caller a reference (pointer) to that object.</span></span> <span data-ttu-id="e69ce-113">在调用**CCheckSGFiles**类中的任何其他函数之前，必须先调用此函数。</span><span class="sxs-lookup"><span data-stu-id="e69ce-113">You must call this function before it calls any of the other functions in the **CCheckSGFiles** class.</span></span> 
  
<span data-ttu-id="e69ce-114">如果要在多线程应用程序中使用 CHKSGFILES，则必须在应用程序的单线程部分调用新函数，并且只能为每个**CCheckSGFiles**对象调用一次**新**函数。</span><span class="sxs-lookup"><span data-stu-id="e69ce-114">If you're using CHKSGFILES in a multithreaded application, you must call the **New** function in the single-threaded portion of the application, and you can call it only once for each **CCheckSGFiles** object.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="e69ce-115">Requirements</span><span class="sxs-lookup"><span data-stu-id="e69ce-115">Requirements</span></span>

<span data-ttu-id="e69ce-116">Exchange 2013 仅包含64位版本的 CHKSGFILES API。</span><span class="sxs-lookup"><span data-stu-id="e69ce-116">Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="e69ce-117">运行应用程序所使用的帐户必须具有对要检查的数据库和日志文件的读取访问权限。</span><span class="sxs-lookup"><span data-stu-id="e69ce-117">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

