---
title: CChkSGFiles 函数
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
description: 上次修改时间：2013年3月3日
ms.openlocfilehash: c881691e7c1ba83a396e659f6aac0328625e49a5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457009"
---
# <a name="cchksgfileserrinit-function"></a><span data-ttu-id="274f0-103">CChkSGFiles 函数</span><span class="sxs-lookup"><span data-stu-id="274f0-103">CChkSGFiles.ErrInit function</span></span>
  
<span data-ttu-id="274f0-104">**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="274f0-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="274f0-105">通过指定要检查的数据库以及要检查的事务日志文件的路径和基名称来初始化**CChkSGFiles**对象。</span><span class="sxs-lookup"><span data-stu-id="274f0-105">Initializes the **CChkSGFiles** object by specifying the databases to be checked and the path and base name of the transaction log files to be checked.</span></span> <span data-ttu-id="274f0-106">应用程序应在成功调用**新**函数后立即调用此函数。</span><span class="sxs-lookup"><span data-stu-id="274f0-106">Applications should call this function immediately after successfully calling the **New** function.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="274f0-107">参数</span><span class="sxs-lookup"><span data-stu-id="274f0-107">Parameters</span></span>

### <a name="rgwszdb"></a><span data-ttu-id="274f0-108">rgwszDb[]</span><span class="sxs-lookup"><span data-stu-id="274f0-108">rgwszDb[]</span></span>
  
<span data-ttu-id="274f0-109">输入参数。</span><span class="sxs-lookup"><span data-stu-id="274f0-109">Input parameter.</span></span> <span data-ttu-id="274f0-110">指定要检查的数据库的数组。</span><span class="sxs-lookup"><span data-stu-id="274f0-110">An array that specifies the databases to be checked.</span></span> <span data-ttu-id="274f0-111">每个 array 元素都是一个以 null 结尾的 Unicode 字符串，其中包含要检查的数据库的路径和文件名。</span><span class="sxs-lookup"><span data-stu-id="274f0-111">Each array element is a null-terminated Unicode string that contains the path and file name of a database to be checked.</span></span>
    
### <a name="cdb"></a><span data-ttu-id="274f0-112">cDB</span><span class="sxs-lookup"><span data-stu-id="274f0-112">cDB</span></span>
  
<span data-ttu-id="274f0-113">输入参数。</span><span class="sxs-lookup"><span data-stu-id="274f0-113">Input parameter.</span></span> <span data-ttu-id="274f0-114">**RgwszDb**数组中的有效数据库路径元素的数目。</span><span class="sxs-lookup"><span data-stu-id="274f0-114">The number of valid database path elements in the **rgwszDb** array.</span></span> 
    
#### <a name="wszlogpath"></a><span data-ttu-id="274f0-115">wszLogPath</span><span class="sxs-lookup"><span data-stu-id="274f0-115">wszLogPath</span></span>
  
<span data-ttu-id="274f0-116">输入参数。</span><span class="sxs-lookup"><span data-stu-id="274f0-116">Input parameter.</span></span> <span data-ttu-id="274f0-117">要检查的事务日志文件的完整路径（以以 null 结尾的 Unicode 字符串的形式）。</span><span class="sxs-lookup"><span data-stu-id="274f0-117">The full path of the transaction log files to be checked, in the form of a null-terminated Unicode string.</span></span>
    
### <a name="wszbasename"></a><span data-ttu-id="274f0-118">wszBaseName</span><span class="sxs-lookup"><span data-stu-id="274f0-118">wszBaseName</span></span>
  
<span data-ttu-id="274f0-119">输入参数。</span><span class="sxs-lookup"><span data-stu-id="274f0-119">Input parameter.</span></span> <span data-ttu-id="274f0-120">以 null 结尾的 Unicode 字符串形式的 Exchange 事务日志文件的三个字母的基本名称。</span><span class="sxs-lookup"><span data-stu-id="274f0-120">The three-letter base name of the Exchange transaction log files, in the form of a null-terminated Unicode string.</span></span>
    
### <a name="ulflags"></a><span data-ttu-id="274f0-121">ulFlags</span><span class="sxs-lookup"><span data-stu-id="274f0-121">ulFlags</span></span>
  
<span data-ttu-id="274f0-122">可选的输入参数。</span><span class="sxs-lookup"><span data-stu-id="274f0-122">Optional input parameter.</span></span> <span data-ttu-id="274f0-123">保留此值以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="274f0-123">This value is reserved for future use.</span></span> <span data-ttu-id="274f0-124">此参数传递的值应为0（零）。</span><span class="sxs-lookup"><span data-stu-id="274f0-124">The value passed by this parameter should be 0 (zero).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="274f0-125">返回值</span><span class="sxs-lookup"><span data-stu-id="274f0-125">Return value</span></span>

<span data-ttu-id="274f0-126">[ERR](cchksgfiles-err-enumeration.md)枚举中的错误代码。</span><span class="sxs-lookup"><span data-stu-id="274f0-126">An error code from the [ERR](cchksgfiles-err-enumeration.md) enumeration.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="274f0-127">备注</span><span class="sxs-lookup"><span data-stu-id="274f0-127">Remarks</span></span>

<span data-ttu-id="274f0-128">**ErrInit**函数注册要检查的数据库和日志文件。</span><span class="sxs-lookup"><span data-stu-id="274f0-128">The **ErrInit** function registers the databases and log files that are to be checked.</span></span> <span data-ttu-id="274f0-129">调用**新**函数之后，但在调用任何其他**ChkSGFiles**函数之前，必须调用此函数。</span><span class="sxs-lookup"><span data-stu-id="274f0-129">This function must be called after the **New** function is called but before any other **ChkSGFiles** function is called.</span></span> 
  
<span data-ttu-id="274f0-130">您必须提供所有数据库名称、日志文件路径和基名称，以以 null 结尾的 Unicode 字符串。</span><span class="sxs-lookup"><span data-stu-id="274f0-130">You must provide all the database names, the log file path, and the base name as null-terminated Unicode strings.</span></span>
  
<span data-ttu-id="274f0-131">您可以只检查数据库文件、仅检查日志文件，还是同时检查数据库和日志文件。</span><span class="sxs-lookup"><span data-stu-id="274f0-131">You can check only the database files, only the log files, or both the database and log files.</span></span> <span data-ttu-id="274f0-132">但是，在调用此函数时，应用程序必须指定至少一个要检查的实体。</span><span class="sxs-lookup"><span data-stu-id="274f0-132">However, when calling this function, the application must specify at least one entity to be checked.</span></span> <span data-ttu-id="274f0-133">为**cDB**传递0（零）， **wszLogPath**的 NULL 值将返回一个错误。</span><span class="sxs-lookup"><span data-stu-id="274f0-133">Passing 0 (zero) for  **cDB**  and NULL for  **wszLogPath**  will return an error.</span></span> 
  
<span data-ttu-id="274f0-134">如果**cDB**的值不是0（零），则为**rgwszDb**传递 NULL 将导致错误。</span><span class="sxs-lookup"><span data-stu-id="274f0-134">If the value of  **cDB**  is other than 0 (zero), passing NULL for  **rgwszDb**  will result in an error.</span></span> <span data-ttu-id="274f0-135">若要检查数据库文件，应用程序必须提供数据库名称。</span><span class="sxs-lookup"><span data-stu-id="274f0-135">To check the database files, the application must provide the database names.</span></span> 
  
<span data-ttu-id="274f0-136">如果为**wszBaseName**传递了 null，但**WSZLOGPATH**不为 null，则将返回错误。</span><span class="sxs-lookup"><span data-stu-id="274f0-136">If NULL is passed for  **wszBaseName**  but  **wszLogPath**  is not NULL, an error will be returned.</span></span> <span data-ttu-id="274f0-137">检查日志文件时，总是需要使用日志文件基名称。</span><span class="sxs-lookup"><span data-stu-id="274f0-137">A log file base name is always required when checking log files.</span></span> 
  
<span data-ttu-id="274f0-138">如果要在多线程应用程序中使用 CHKSGFILES，则必须在应用程序的单线程部分调用**ErrInit**函数，并且只能为每个**CCheckSGFiles**对象调用一次该函数。</span><span class="sxs-lookup"><span data-stu-id="274f0-138">If you're using CHKSGFILES in a multithreaded application, you must call the **ErrInit** function in the single-threaded portion of the application, and you can call it only once for each **CCheckSGFiles** object.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="274f0-139">Requirements</span><span class="sxs-lookup"><span data-stu-id="274f0-139">Requirements</span></span>

<span data-ttu-id="274f0-140">Exchange 2013 仅包含64位版本的 CHKSGFILES API。</span><span class="sxs-lookup"><span data-stu-id="274f0-140">Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="274f0-141">运行应用程序所使用的帐户必须具有对要检查的数据库和日志文件的读取访问权限。</span><span class="sxs-lookup"><span data-stu-id="274f0-141">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

