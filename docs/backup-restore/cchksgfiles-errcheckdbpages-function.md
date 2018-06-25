---
title: CChkSGFiles.ErrCheckDbPages 函数
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ErrCheckDbPages
api_type:
- dllExport
ms.assetid: 5e981a7c-28cd-470c-b7eb-606463e9dd05
description: 上次修改时间： 2013 年 2 月 22 日
ms.openlocfilehash: f1588b1dbc4bd7e83683fa4432a175405ad17903
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752687"
---
# <a name="cchksgfileserrcheckdbpages-function"></a><span data-ttu-id="5e17c-103">CChkSGFiles.ErrCheckDbPages 函数</span><span class="sxs-lookup"><span data-stu-id="5e17c-103">CChkSGFiles.ErrCheckDbPages function</span></span>

<span data-ttu-id="5e17c-104">**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="5e17c-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="5e17c-105">验证指定的数据库中的页面范围。</span><span class="sxs-lookup"><span data-stu-id="5e17c-105">Validates a range of pages in a specified database.</span></span> 
  
```cs
Vitual ERRErrCheckDbPages  
(
    Const ULONGiDb,
    Const VOID  * const pvPageBuffer,
    Const ULONGcbPageBuffer,
    PAGE_INFOrgPageInfo[],
    Const ULONGcPageInfo,
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a><span data-ttu-id="5e17c-106">参数</span><span class="sxs-lookup"><span data-stu-id="5e17c-106">Parameters</span></span>

### <a name="idb"></a><span data-ttu-id="5e17c-107">iDb</span><span class="sxs-lookup"><span data-stu-id="5e17c-107">iDb</span></span>
  
<span data-ttu-id="5e17c-108">输入的参数。</span><span class="sxs-lookup"><span data-stu-id="5e17c-108">Input parameter.</span></span> <span data-ttu-id="5e17c-109">**ErrInit**函数**rgwszDb []** 参数中指定的数据库的数组中的索引。</span><span class="sxs-lookup"><span data-stu-id="5e17c-109">An index into the array of databases specified in the **rgwszDb[]** parameter to the **ErrInit** function.</span></span> <span data-ttu-id="5e17c-110">此参数所编制索引的数据库将被选中。</span><span class="sxs-lookup"><span data-stu-id="5e17c-110">The database indexed by this parameter will be checked.</span></span> 
    
### <a name="pvpagebuffer"></a><span data-ttu-id="5e17c-111">pvPageBuffer</span><span class="sxs-lookup"><span data-stu-id="5e17c-111">pvPageBuffer</span></span> 
  
<span data-ttu-id="5e17c-112">输入的参数。</span><span class="sxs-lookup"><span data-stu-id="5e17c-112">Input parameter.</span></span> <span data-ttu-id="5e17c-113">指向包含要检查的一个或多个数据库页的缓冲区的指针。</span><span class="sxs-lookup"><span data-stu-id="5e17c-113">A pointer to a buffer containing one or more database pages to be checked.</span></span> <span data-ttu-id="5e17c-114">缓冲区的大小必须是数据库页面大小的倍数，如**ErrCheckDbHeaders**函数返回**pcbDbPageSize**参数中。</span><span class="sxs-lookup"><span data-stu-id="5e17c-114">The size of the buffer must be a multiple of the database page size, as returned in the **pcbDbPageSize** parameter by the **ErrCheckDbHeaders** function.</span></span> <span data-ttu-id="5e17c-115">调用应用程序必须调用**ErrCheckDbPages**之前填充数据库页面内容的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="5e17c-115">The calling application must fill the buffer with the database page contents before calling **ErrCheckDbPages**.</span></span>
    
### <a name="cbpagebuffer"></a><span data-ttu-id="5e17c-116">cbPageBuffer</span><span class="sxs-lookup"><span data-stu-id="5e17c-116">cbPageBuffer</span></span>
  
<span data-ttu-id="5e17c-117">输入的参数。</span><span class="sxs-lookup"><span data-stu-id="5e17c-117">Input parameter.</span></span> <span data-ttu-id="5e17c-118">**PvPageBuffer**参数，以字节为单位的大小。</span><span class="sxs-lookup"><span data-stu-id="5e17c-118">The size of the **pvPageBuffer** parameter, in bytes.</span></span> <span data-ttu-id="5e17c-119">由**ErrCheckDbHeaders**函数返回**pcbDbPageSize**参数中，此值必须是数据库页面大小的倍数。</span><span class="sxs-lookup"><span data-stu-id="5e17c-119">This value must be a multiple of the database page size, as returned in the **pcbDbPageSize** parameter by the **ErrCheckDbHeaders** function.</span></span> 
    
### <a name="rgpageinfo"></a><span data-ttu-id="5e17c-120">rgPageInfo]</span><span class="sxs-lookup"><span data-stu-id="5e17c-120">rgPageInfo[]</span></span> 
  
<span data-ttu-id="5e17c-121">输入/输出参数。</span><span class="sxs-lookup"><span data-stu-id="5e17c-121">Input/output parameter.</span></span> <span data-ttu-id="5e17c-122">数组**页\_INFO** **ErrCheckDbPages**填入的结构详细进行检查每个数据库页的结果。</span><span class="sxs-lookup"><span data-stu-id="5e17c-122">An array of **PAGE\_INFO** structures that **ErrCheckDbPages** fills with detailed results of each database page that is checked.</span></span> <span data-ttu-id="5e17c-123">该数组必须具有一个元素传递**pvPageBuffer**参数和中每**ulPgno**字段中每个数据库页**页\_INFO**结构必须设置为逻辑页码对应于数据库页。</span><span class="sxs-lookup"><span data-stu-id="5e17c-123">The array must have one element for each database page passed in the **pvPageBuffer** parameter, and the **ulPgno** field in each **PAGE\_INFO** structure must be set to the logical page number that corresponds to the database page.</span></span> <span data-ttu-id="5e17c-124">有关详细信息，请参阅本主题后面的"备注"。</span><span class="sxs-lookup"><span data-stu-id="5e17c-124">For more information, see "Remarks" later in this topic.</span></span> 
    
### <a name="cpageinfo"></a><span data-ttu-id="5e17c-125">cPageInfo</span><span class="sxs-lookup"><span data-stu-id="5e17c-125">cPageInfo</span></span>
  
<span data-ttu-id="5e17c-126">输入的参数。</span><span class="sxs-lookup"><span data-stu-id="5e17c-126">Input parameter.</span></span> <span data-ttu-id="5e17c-127">**RgPageInfo []** 数组中的条目数。</span><span class="sxs-lookup"><span data-stu-id="5e17c-127">The number of entries in the **rgPageInfo[]** array.</span></span> <span data-ttu-id="5e17c-128">该值必须等于**pvPageBuffer**参数中传递的数据库页面的数量。</span><span class="sxs-lookup"><span data-stu-id="5e17c-128">This value must be equal to the number of database pages passed in the **pvPageBuffer** parameter.</span></span> 
    
### <a name="ulflags"></a><span data-ttu-id="5e17c-129">ulFlags</span><span class="sxs-lookup"><span data-stu-id="5e17c-129">ulFlags</span></span> 
  
<span data-ttu-id="5e17c-130">可选的输入的参数。</span><span class="sxs-lookup"><span data-stu-id="5e17c-130">Optional input parameter.</span></span> <span data-ttu-id="5e17c-131">此值保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="5e17c-131">This value is reserved for future use.</span></span> <span data-ttu-id="5e17c-132">此参数中传递的值应为 0 （零）。</span><span class="sxs-lookup"><span data-stu-id="5e17c-132">The value passed in this parameter should be 0 (zero).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5e17c-133">返回值</span><span class="sxs-lookup"><span data-stu-id="5e17c-133">Return value</span></span>

<span data-ttu-id="5e17c-134">从[ERR](cchksgfiles-err-enumeration.md)枚举错误代码。</span><span class="sxs-lookup"><span data-stu-id="5e17c-134">An error code from the [ERR](cchksgfiles-err-enumeration.md) enumeration.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5e17c-135">注解</span><span class="sxs-lookup"><span data-stu-id="5e17c-135">Remarks</span></span>

<span data-ttu-id="5e17c-136">请注意，您需要指定数据库的数据库传递给**ErrInit**函数数组中。</span><span class="sxs-lookup"><span data-stu-id="5e17c-136">Note that you need to have specified the database in the array of databases passed to the **ErrInit** function.</span></span> <span data-ttu-id="5e17c-137">此外，必须在**ErrCheckDbPages**之前调用**ErrCheckDbHeaders** 。</span><span class="sxs-lookup"><span data-stu-id="5e17c-137">Also, **ErrCheckDbHeaders** must be called before **ErrCheckDbPages**.</span></span>
  
<span data-ttu-id="5e17c-138">调用应用程序必须分配内存缓冲区的足以容纳要检查的数据库页面。</span><span class="sxs-lookup"><span data-stu-id="5e17c-138">The calling application must allocate a memory buffer that is large enough to hold the database pages to be checked.</span></span> <span data-ttu-id="5e17c-139">应用程序负责为一个或多个此类数据库页的内容填充缓冲区。</span><span class="sxs-lookup"><span data-stu-id="5e17c-139">The application is responsible for filling the buffer with the contents of one or more such database pages.</span></span> 
  
<span data-ttu-id="5e17c-140">调用应用程序必须调用**ErrCheckDbPages**之前调用**ErrCheckDbHeaders** 。</span><span class="sxs-lookup"><span data-stu-id="5e17c-140">The calling application must call **ErrCheckDbHeaders** before calling **ErrCheckDbPages**.</span></span> <span data-ttu-id="5e17c-141">可以根据需要以覆盖要检查的所有数据库文件中的所有页面多次调用此函数。</span><span class="sxs-lookup"><span data-stu-id="5e17c-141">This function can be called as many times as necessary to cover all the pages in all database files that are to be checked.</span></span>
  
<span data-ttu-id="5e17c-142">在**rgPageInfo []** 参数中，返回每个元素包含有关在数据库页的信息**页\_INFO**结构。</span><span class="sxs-lookup"><span data-stu-id="5e17c-142">In the **rgPageInfo[]** parameter, each element returned contains information about the database page in a **PAGE\_INFO** structure.</span></span> <span data-ttu-id="5e17c-143">如果**ErrCheckDbPages**函数将返回错误，应用程序应检查每个**页\_INFO**结构以确定哪一页上找到错误。</span><span class="sxs-lookup"><span data-stu-id="5e17c-143">If the **ErrCheckDbPages** function returns an error, the application should check each **PAGE\_INFO** structure to determine on which page the error was found.</span></span> <span data-ttu-id="5e17c-144">例如，比较**checksumActual**和**checksumExpected**值将指示是否已在该数据库页上检测到的校验和错误。</span><span class="sxs-lookup"><span data-stu-id="5e17c-144">For example, comparing the **checksumActual** and **checksumExpected** values will indicate whether a checksum error was detected on that database page.</span></span> 
  
<span data-ttu-id="5e17c-145">如果**ErrCheckDbPages**检测到数据库内容中的任何错误，其将创建一个 Windows 错误事件日志条目。</span><span class="sxs-lookup"><span data-stu-id="5e17c-145">If **ErrCheckDbPages** detects any errors in the database content, it will create a Windows Error event log entry.</span></span> 
  
<span data-ttu-id="5e17c-146">**CChkSGFiles**对象确定是否已实际签**ErrInit**函数注册的所有数据库。</span><span class="sxs-lookup"><span data-stu-id="5e17c-146">The **CChkSGFiles** object determines whether all the databases registered with the **ErrInit** function were actually checked.</span></span> <span data-ttu-id="5e17c-147">具体而言， **CChkSGFiles**使用**ErrCheckDbPages**函数来确定是否相同数量的数据库页由**ErrCheckDbHeaders**实际已验证。</span><span class="sxs-lookup"><span data-stu-id="5e17c-147">Specifically, **CChkSGFiles** uses the **ErrCheckDbPages** function to determine whether the same number of database pages indicated by **ErrCheckDbHeaders** were actually verified.</span></span> <span data-ttu-id="5e17c-148">如果未成功签正确的每个数据库中的页面数，则**ErrTerm**函数将返回错误。</span><span class="sxs-lookup"><span data-stu-id="5e17c-148">If the correct number of pages in each database were not successfully checked, the **ErrTerm** function returns an error.</span></span> 
  
<span data-ttu-id="5e17c-149">如果您使用 CHKSGFILES 多线程应用程序中，您可以在应用程序的多线程部分调用**ErrCheckDbPages**函数。</span><span class="sxs-lookup"><span data-stu-id="5e17c-149">If you're using CHKSGFILES in a multithreaded application, you can call the **ErrCheckDbPages** function in the multithreaded portion of the application.</span></span> <span data-ttu-id="5e17c-150">请注意**ErrCheckDbPages**通常会调用多次进行检查的每个数据库。</span><span class="sxs-lookup"><span data-stu-id="5e17c-150">Note that **ErrCheckDbPages** is typically called multiple times for each database that is checked.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="5e17c-151">要求</span><span class="sxs-lookup"><span data-stu-id="5e17c-151">Requirements</span></span>

<span data-ttu-id="5e17c-152">Exchange 2013 只包括 CHKSGFILES API 的 64 位版本。</span><span class="sxs-lookup"><span data-stu-id="5e17c-152">Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="5e17c-153">下运行该应用程序的帐户必须具有读取权限要检查的数据库和日志文件。</span><span class="sxs-lookup"><span data-stu-id="5e17c-153">The account that the application is running under must have read permissions to the database and log files that are to be checked.</span></span>
  

