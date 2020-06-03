---
title: CChkSGFiles 函数
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
description: 上次修改时间：2013年2月22日
ms.openlocfilehash: 78d2dbee6253096d597b4ec2de3878f40ee1b6d7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526723"
---
# <a name="cchksgfileserrcheckdbpages-function"></a><span data-ttu-id="a1cd0-103">CChkSGFiles 函数</span><span class="sxs-lookup"><span data-stu-id="a1cd0-103">CChkSGFiles.ErrCheckDbPages function</span></span>

<span data-ttu-id="a1cd0-104">**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="a1cd0-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="a1cd0-105">验证指定数据库中的页面范围。</span><span class="sxs-lookup"><span data-stu-id="a1cd0-105">Validates a range of pages in a specified database.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="a1cd0-106">参数</span><span class="sxs-lookup"><span data-stu-id="a1cd0-106">Parameters</span></span>

### <a name="idb"></a><span data-ttu-id="a1cd0-107">.Idb</span><span class="sxs-lookup"><span data-stu-id="a1cd0-107">iDb</span></span>
  
<span data-ttu-id="a1cd0-108">输入参数。</span><span class="sxs-lookup"><span data-stu-id="a1cd0-108">Input parameter.</span></span> <span data-ttu-id="a1cd0-109">指向**ErrInit**函数的**rgwszDb []** 参数中指定的数据库数组的索引。</span><span class="sxs-lookup"><span data-stu-id="a1cd0-109">An index into the array of databases specified in the **rgwszDb[]** parameter to the **ErrInit** function.</span></span> <span data-ttu-id="a1cd0-110">将检查通过此参数编制索引的数据库。</span><span class="sxs-lookup"><span data-stu-id="a1cd0-110">The database indexed by this parameter will be checked.</span></span> 
    
### <a name="pvpagebuffer"></a><span data-ttu-id="a1cd0-111">pvPageBuffer</span><span class="sxs-lookup"><span data-stu-id="a1cd0-111">pvPageBuffer</span></span> 
  
<span data-ttu-id="a1cd0-112">输入参数。</span><span class="sxs-lookup"><span data-stu-id="a1cd0-112">Input parameter.</span></span> <span data-ttu-id="a1cd0-113">指向包含要检查的一个或多个数据库页面的缓冲区的指针。</span><span class="sxs-lookup"><span data-stu-id="a1cd0-113">A pointer to a buffer containing one or more database pages to be checked.</span></span> <span data-ttu-id="a1cd0-114">缓冲区的大小必须是数据库页面大小的倍数，与**ErrCheckDbHeaders**函数在**pcbDbPageSize**参数中返回的大小相同。</span><span class="sxs-lookup"><span data-stu-id="a1cd0-114">The size of the buffer must be a multiple of the database page size, as returned in the **pcbDbPageSize** parameter by the **ErrCheckDbHeaders** function.</span></span> <span data-ttu-id="a1cd0-115">调用**ErrCheckDbPages**之前，调用应用程序必须填充数据库页面内容的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="a1cd0-115">The calling application must fill the buffer with the database page contents before calling **ErrCheckDbPages**.</span></span>
    
### <a name="cbpagebuffer"></a><span data-ttu-id="a1cd0-116">cbPageBuffer</span><span class="sxs-lookup"><span data-stu-id="a1cd0-116">cbPageBuffer</span></span>
  
<span data-ttu-id="a1cd0-117">输入参数。</span><span class="sxs-lookup"><span data-stu-id="a1cd0-117">Input parameter.</span></span> <span data-ttu-id="a1cd0-118">**PvPageBuffer**参数的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="a1cd0-118">The size of the **pvPageBuffer** parameter, in bytes.</span></span> <span data-ttu-id="a1cd0-119">此值必须是数据库页面大小的倍数，与**ErrCheckDbHeaders**函数在**pcbDbPageSize**参数中返回的大小相同。</span><span class="sxs-lookup"><span data-stu-id="a1cd0-119">This value must be a multiple of the database page size, as returned in the **pcbDbPageSize** parameter by the **ErrCheckDbHeaders** function.</span></span> 
    
### <a name="rgpageinfo"></a><span data-ttu-id="a1cd0-120">rgPageInfo[]</span><span class="sxs-lookup"><span data-stu-id="a1cd0-120">rgPageInfo[]</span></span> 
  
<span data-ttu-id="a1cd0-121">输入/输出参数。</span><span class="sxs-lookup"><span data-stu-id="a1cd0-121">Input/output parameter.</span></span> <span data-ttu-id="a1cd0-122">**ErrCheckDbPages**使用所检查的每个数据库页面的详细结果填充的**页面 \_ 信息**结构的数组。</span><span class="sxs-lookup"><span data-stu-id="a1cd0-122">An array of **PAGE\_INFO** structures that **ErrCheckDbPages** fills with detailed results of each database page that is checked.</span></span> <span data-ttu-id="a1cd0-123">对于在**pvPageBuffer**参数中传递的每个数据库页面，该数组必须具有一个元素，并且每个**页面 \_ 信息**结构中的**ulPgno**字段必须设置为与数据库页面相对应的逻辑页面编号。</span><span class="sxs-lookup"><span data-stu-id="a1cd0-123">The array must have one element for each database page passed in the **pvPageBuffer** parameter, and the **ulPgno** field in each **PAGE\_INFO** structure must be set to the logical page number that corresponds to the database page.</span></span> <span data-ttu-id="a1cd0-124">有关详细信息，请参阅本主题后面的 "备注"。</span><span class="sxs-lookup"><span data-stu-id="a1cd0-124">For more information, see "Remarks" later in this topic.</span></span> 
    
### <a name="cpageinfo"></a><span data-ttu-id="a1cd0-125">cPageInfo</span><span class="sxs-lookup"><span data-stu-id="a1cd0-125">cPageInfo</span></span>
  
<span data-ttu-id="a1cd0-126">输入参数。</span><span class="sxs-lookup"><span data-stu-id="a1cd0-126">Input parameter.</span></span> <span data-ttu-id="a1cd0-127">**RgPageInfo []** 数组中的条目数。</span><span class="sxs-lookup"><span data-stu-id="a1cd0-127">The number of entries in the **rgPageInfo[]** array.</span></span> <span data-ttu-id="a1cd0-128">此值必须等于在**pvPageBuffer**参数中传递的数据库页面的数目。</span><span class="sxs-lookup"><span data-stu-id="a1cd0-128">This value must be equal to the number of database pages passed in the **pvPageBuffer** parameter.</span></span> 
    
### <a name="ulflags"></a><span data-ttu-id="a1cd0-129">ulFlags</span><span class="sxs-lookup"><span data-stu-id="a1cd0-129">ulFlags</span></span> 
  
<span data-ttu-id="a1cd0-130">可选的输入参数。</span><span class="sxs-lookup"><span data-stu-id="a1cd0-130">Optional input parameter.</span></span> <span data-ttu-id="a1cd0-131">保留此值以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="a1cd0-131">This value is reserved for future use.</span></span> <span data-ttu-id="a1cd0-132">此参数中传递的值应为0（零）。</span><span class="sxs-lookup"><span data-stu-id="a1cd0-132">The value passed in this parameter should be 0 (zero).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a1cd0-133">返回值</span><span class="sxs-lookup"><span data-stu-id="a1cd0-133">Return value</span></span>

<span data-ttu-id="a1cd0-134">[ERR](cchksgfiles-err-enumeration.md)枚举中的错误代码。</span><span class="sxs-lookup"><span data-stu-id="a1cd0-134">An error code from the [ERR](cchksgfiles-err-enumeration.md) enumeration.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a1cd0-135">备注</span><span class="sxs-lookup"><span data-stu-id="a1cd0-135">Remarks</span></span>

<span data-ttu-id="a1cd0-136">请注意，您需要在传递给**ErrInit**函数的数据库数组中指定数据库。</span><span class="sxs-lookup"><span data-stu-id="a1cd0-136">Note that you need to have specified the database in the array of databases passed to the **ErrInit** function.</span></span> <span data-ttu-id="a1cd0-137">此外，还必须在**ErrCheckDbPages**之前调用**ErrCheckDbHeaders** 。</span><span class="sxs-lookup"><span data-stu-id="a1cd0-137">Also, **ErrCheckDbHeaders** must be called before **ErrCheckDbPages**.</span></span>
  
<span data-ttu-id="a1cd0-138">调用应用程序必须分配足够大的内存缓冲区，以容纳要检查的数据库页。</span><span class="sxs-lookup"><span data-stu-id="a1cd0-138">The calling application must allocate a memory buffer that is large enough to hold the database pages to be checked.</span></span> <span data-ttu-id="a1cd0-139">应用程序负责使用一个或多个此类数据库页的内容填充缓冲区。</span><span class="sxs-lookup"><span data-stu-id="a1cd0-139">The application is responsible for filling the buffer with the contents of one or more such database pages.</span></span> 
  
<span data-ttu-id="a1cd0-140">调用应用程序必须先调用**ErrCheckDbHeaders** ，然后才能调用**ErrCheckDbPages**。</span><span class="sxs-lookup"><span data-stu-id="a1cd0-140">The calling application must call **ErrCheckDbHeaders** before calling **ErrCheckDbPages**.</span></span> <span data-ttu-id="a1cd0-141">可以根据需要多次调用此函数，以涵盖要检查的所有数据库文件中的所有页面。</span><span class="sxs-lookup"><span data-stu-id="a1cd0-141">This function can be called as many times as necessary to cover all the pages in all database files that are to be checked.</span></span>
  
<span data-ttu-id="a1cd0-142">在**rgPageInfo []** 参数中，返回的每个元素都包含有关**页面 \_ 信息**结构中的数据库页面的信息。</span><span class="sxs-lookup"><span data-stu-id="a1cd0-142">In the **rgPageInfo[]** parameter, each element returned contains information about the database page in a **PAGE\_INFO** structure.</span></span> <span data-ttu-id="a1cd0-143">如果**ErrCheckDbPages**函数返回一个错误，则应用程序应检查每个**页面 \_ 信息**结构以确定在哪个页面上发现了错误。</span><span class="sxs-lookup"><span data-stu-id="a1cd0-143">If the **ErrCheckDbPages** function returns an error, the application should check each **PAGE\_INFO** structure to determine on which page the error was found.</span></span> <span data-ttu-id="a1cd0-144">例如，比较**checksumActual**和**checksumExpected**值将指示是否在该数据库页上检测到校验和错误。</span><span class="sxs-lookup"><span data-stu-id="a1cd0-144">For example, comparing the **checksumActual** and **checksumExpected** values will indicate whether a checksum error was detected on that database page.</span></span> 
  
<span data-ttu-id="a1cd0-145">如果**ErrCheckDbPages**检测到数据库内容中的任何错误，它将创建一个 Windows 错误事件日志条目。</span><span class="sxs-lookup"><span data-stu-id="a1cd0-145">If **ErrCheckDbPages** detects any errors in the database content, it will create a Windows Error event log entry.</span></span> 
  
<span data-ttu-id="a1cd0-146">**CChkSGFiles**对象确定是否实际检查了使用**ErrInit**函数注册的所有数据库。</span><span class="sxs-lookup"><span data-stu-id="a1cd0-146">The **CChkSGFiles** object determines whether all the databases registered with the **ErrInit** function were actually checked.</span></span> <span data-ttu-id="a1cd0-147">具体来说， **CChkSGFiles**使用**ErrCheckDbPages**函数来确定是否实际验证**ErrCheckDbHeaders**指示的相同数量的数据库页面。</span><span class="sxs-lookup"><span data-stu-id="a1cd0-147">Specifically, **CChkSGFiles** uses the **ErrCheckDbPages** function to determine whether the same number of database pages indicated by **ErrCheckDbHeaders** were actually verified.</span></span> <span data-ttu-id="a1cd0-148">如果未成功检查每个数据库中的正确数量的页面， **ErrTerm**函数将返回一个错误。</span><span class="sxs-lookup"><span data-stu-id="a1cd0-148">If the correct number of pages in each database were not successfully checked, the **ErrTerm** function returns an error.</span></span> 
  
<span data-ttu-id="a1cd0-149">如果要在多线程应用程序中使用 CHKSGFILES，则可以在应用程序的多线程部分调用**ErrCheckDbPages**函数。</span><span class="sxs-lookup"><span data-stu-id="a1cd0-149">If you're using CHKSGFILES in a multithreaded application, you can call the **ErrCheckDbPages** function in the multithreaded portion of the application.</span></span> <span data-ttu-id="a1cd0-150">请注意，对于所检查的每个数据库， **ErrCheckDbPages**通常被多次调用。</span><span class="sxs-lookup"><span data-stu-id="a1cd0-150">Note that **ErrCheckDbPages** is typically called multiple times for each database that is checked.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="a1cd0-151">Requirements</span><span class="sxs-lookup"><span data-stu-id="a1cd0-151">Requirements</span></span>

<span data-ttu-id="a1cd0-152">Exchange 2013 仅包含64位版本的 CHKSGFILES API。</span><span class="sxs-lookup"><span data-stu-id="a1cd0-152">Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="a1cd0-153">运行应用程序所使用的帐户必须具有对要检查的数据库和日志文件的读取权限。</span><span class="sxs-lookup"><span data-stu-id="a1cd0-153">The account that the application is running under must have read permissions to the database and log files that are to be checked.</span></span>
  

