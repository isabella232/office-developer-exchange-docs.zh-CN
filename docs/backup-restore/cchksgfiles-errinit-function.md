---
title: CChkSGFiles.ErrInit 函数
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ErrInit
api_type:
- dllExport
ms.assetid: 61bb3af1-8b51-4bae-8e25-90a4dc1226c5
description: 上次修改时间： 2013 年 3 月 3 日
ms.openlocfilehash: d4b76933a747fe4bf084061cf080bc68264132ed
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752686"
---
# <a name="cchksgfileserrinit-function"></a><span data-ttu-id="22a10-103">CChkSGFiles.ErrInit 函数</span><span class="sxs-lookup"><span data-stu-id="22a10-103">CChkSGFiles.ErrInit function</span></span>
  
<span data-ttu-id="22a10-104">**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="22a10-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="22a10-105">初始化通过指定要检查的数据库的**CChkSGFiles**对象的路径和要检查的事务日志文件的基本名称。</span><span class="sxs-lookup"><span data-stu-id="22a10-105">Initializes the **CChkSGFiles** object by specifying the databases to be checked and the path and base name of the transaction log files to be checked.</span></span> <span data-ttu-id="22a10-106">应用程序应在成功调用**新建**函数后立即调用此函数。</span><span class="sxs-lookup"><span data-stu-id="22a10-106">Applications should call this function immediately after successfully calling the **New** function.</span></span> 
  
```cs
Vitual ERRErrInit  
(
    Const WCHAR  * const rgwszDb[],
    Const ULONGcDB,
    __in_z const WCHAR  * const wszLogPath,
    __in_z const WCHAR  * const wszBaseName,
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a><span data-ttu-id="22a10-107">参数</span><span class="sxs-lookup"><span data-stu-id="22a10-107">Parameters</span></span>

### <a name="rgwszdb"></a><span data-ttu-id="22a10-108">rgwszDb]</span><span class="sxs-lookup"><span data-stu-id="22a10-108">rgwszDb[]</span></span>
  
<span data-ttu-id="22a10-109">输入的参数。</span><span class="sxs-lookup"><span data-stu-id="22a10-109">Input parameter.</span></span> <span data-ttu-id="22a10-110">数组，它指定要检查的数据库。</span><span class="sxs-lookup"><span data-stu-id="22a10-110">An array that specifies the databases to be checked.</span></span> <span data-ttu-id="22a10-111">每个数组元素是 null 结尾的 Unicode 字符串，包含要检查的数据库的路径和文件名称。</span><span class="sxs-lookup"><span data-stu-id="22a10-111">Each array element is a null-terminated Unicode string that contains the path and file name of a database to be checked.</span></span>
    
### <a name="cdb"></a><span data-ttu-id="22a10-112">cDB</span><span class="sxs-lookup"><span data-stu-id="22a10-112">cDB</span></span>
  
<span data-ttu-id="22a10-113">输入的参数。</span><span class="sxs-lookup"><span data-stu-id="22a10-113">Input parameter.</span></span> <span data-ttu-id="22a10-114">有效的数据库路径**rgwszDb**数组中的元素数。</span><span class="sxs-lookup"><span data-stu-id="22a10-114">The number of valid database path elements in the **rgwszDb** array.</span></span> 
    
#### <a name="wszlogpath"></a><span data-ttu-id="22a10-115">wszLogPath</span><span class="sxs-lookup"><span data-stu-id="22a10-115">wszLogPath</span></span>
  
<span data-ttu-id="22a10-116">输入的参数。</span><span class="sxs-lookup"><span data-stu-id="22a10-116">Input parameter.</span></span> <span data-ttu-id="22a10-117">要检查的以 null 结尾的 Unicode 字符串形式的事务日志文件的完整路径。</span><span class="sxs-lookup"><span data-stu-id="22a10-117">The full path of the transaction log files to be checked, in the form of a null-terminated Unicode string.</span></span>
    
### <a name="wszbasename"></a><span data-ttu-id="22a10-118">wszBaseName</span><span class="sxs-lookup"><span data-stu-id="22a10-118">wszBaseName</span></span>
  
<span data-ttu-id="22a10-119">输入的参数。</span><span class="sxs-lookup"><span data-stu-id="22a10-119">Input parameter.</span></span> <span data-ttu-id="22a10-120">Exchange 的事务日志文件，以 null 结尾的 Unicode 字符串形式三个字母基名称。</span><span class="sxs-lookup"><span data-stu-id="22a10-120">The three-letter base name of the Exchange transaction log files, in the form of a null-terminated Unicode string.</span></span>
    
### <a name="ulflags"></a><span data-ttu-id="22a10-121">ulFlags</span><span class="sxs-lookup"><span data-stu-id="22a10-121">ulFlags</span></span>
  
<span data-ttu-id="22a10-122">可选的输入的参数。</span><span class="sxs-lookup"><span data-stu-id="22a10-122">Optional input parameter.</span></span> <span data-ttu-id="22a10-123">此值保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="22a10-123">This value is reserved for future use.</span></span> <span data-ttu-id="22a10-124">通过此参数传递的值应为 0 （零）。</span><span class="sxs-lookup"><span data-stu-id="22a10-124">The value passed by this parameter should be 0 (zero).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="22a10-125">返回值</span><span class="sxs-lookup"><span data-stu-id="22a10-125">Return value</span></span>

<span data-ttu-id="22a10-126">从[ERR](cchksgfiles-err-enumeration.md)枚举错误代码。</span><span class="sxs-lookup"><span data-stu-id="22a10-126">An error code from the [ERR](cchksgfiles-err-enumeration.md) enumeration.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="22a10-127">注解</span><span class="sxs-lookup"><span data-stu-id="22a10-127">Remarks</span></span>

<span data-ttu-id="22a10-128">**ErrInit**函数注册的数据库和要检查的日志文件。</span><span class="sxs-lookup"><span data-stu-id="22a10-128">The **ErrInit** function registers the databases and log files that are to be checked.</span></span> <span data-ttu-id="22a10-129">之后，**新建**函数将调用的函数调用任何其他**ChkSGFiles**之前，必须调用此函数。</span><span class="sxs-lookup"><span data-stu-id="22a10-129">This function must be called after the **New** function is called but before any other **ChkSGFiles** function is called.</span></span> 
  
<span data-ttu-id="22a10-130">您必须以 null 结尾的 Unicode 字符串形式提供所有数据库名称、 日志文件路径，和的基名称。</span><span class="sxs-lookup"><span data-stu-id="22a10-130">You must provide all the database names, the log file path, and the base name as null-terminated Unicode strings.</span></span>
  
<span data-ttu-id="22a10-131">您可以检查仅数据库文件，仅日志文件或数据库和日志文件。</span><span class="sxs-lookup"><span data-stu-id="22a10-131">You can check only the database files, only the log files, or both the database and log files.</span></span> <span data-ttu-id="22a10-132">但是时调用此函数，应用程序必须指定要检查的至少一个实体。</span><span class="sxs-lookup"><span data-stu-id="22a10-132">However, when calling this function, the application must specify at least one entity to be checked.</span></span> <span data-ttu-id="22a10-133">传递 0 （零） **cDB**和 NULL **wszLogPath**将返回错误。</span><span class="sxs-lookup"><span data-stu-id="22a10-133">Passing 0 (zero) for  **cDB**  and NULL for  **wszLogPath**  will return an error.</span></span> 
  
<span data-ttu-id="22a10-134">如果**cDB**的值为非 0 （零），为**rgwszDb**传递 NULL 将导致出错。</span><span class="sxs-lookup"><span data-stu-id="22a10-134">If the value of  **cDB**  is other than 0 (zero), passing NULL for  **rgwszDb**  will result in an error.</span></span> <span data-ttu-id="22a10-135">若要检查数据库文件，该应用程序必须提供数据库名称。</span><span class="sxs-lookup"><span data-stu-id="22a10-135">To check the database files, the application must provide the database names.</span></span> 
  
<span data-ttu-id="22a10-136">如果为**wszBaseName**传递空值，但**wszLogPath**不为 NULL，则将返回错误。</span><span class="sxs-lookup"><span data-stu-id="22a10-136">If NULL is passed for  **wszBaseName**  but  **wszLogPath**  is not NULL, an error will be returned.</span></span> <span data-ttu-id="22a10-137">始终在检查日志文件时所需日志文件的基名称。</span><span class="sxs-lookup"><span data-stu-id="22a10-137">A log file base name is always required when checking log files.</span></span> 
  
<span data-ttu-id="22a10-138">如果您使用 CHKSGFILES 多线程应用程序中，您必须将应用程序的单线程部分调用**ErrInit**函数，且您可以为每个**CCheckSGFiles**对象调用它仅执行一次。</span><span class="sxs-lookup"><span data-stu-id="22a10-138">If you're using CHKSGFILES in a multithreaded application, you must call the **ErrInit** function in the single-threaded portion of the application, and you can call it only once for each **CCheckSGFiles** object.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="22a10-139">要求</span><span class="sxs-lookup"><span data-stu-id="22a10-139">Requirements</span></span>

<span data-ttu-id="22a10-140">Exchange 2013 只包括 CHKSGFILES API 的 64 位版本。</span><span class="sxs-lookup"><span data-stu-id="22a10-140">Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="22a10-141">下运行该应用程序的帐户必须具有对要检查的数据库和日志文件的读取访问权限。</span><span class="sxs-lookup"><span data-stu-id="22a10-141">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

