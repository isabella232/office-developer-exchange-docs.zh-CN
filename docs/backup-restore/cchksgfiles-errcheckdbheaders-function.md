---
title: CChkSGFiles.ErrCheckDbHeaders 函数
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ErrCheckDbHeaders
api_type:
- dllExport
ms.assetid: 75289cd2-35b1-4f75-a651-dce01f1ddda1
description: 上次修改时间： 2013 年 2 月 22 日
ms.openlocfilehash: a407019063b34970e883a00ca4f4d730935d7cba
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752694"
---
# <a name="cchksgfileserrcheckdbheaders-function"></a><span data-ttu-id="4eff4-103">CChkSGFiles.ErrCheckDbHeaders 函数</span><span class="sxs-lookup"><span data-stu-id="4eff4-103">CChkSGFiles.ErrCheckDbHeaders function</span></span>

<span data-ttu-id="4eff4-104">**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="4eff4-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span> 
  
<span data-ttu-id="4eff4-105">验证**ErrInit**函数由指定的数据库文件的标题。</span><span class="sxs-lookup"><span data-stu-id="4eff4-105">Validates the headers of the database files that were specified by the **ErrInit** function.</span></span> <span data-ttu-id="4eff4-106">此函数还返回每个指定的数据库中的页面大小和数量页面。</span><span class="sxs-lookup"><span data-stu-id="4eff4-106">This function also returns the page size and number of pages in each of the specified databases.</span></span> 
  
```cs
Vitual ERRErrCheckDbHeaders  
(
        ULONG  * const pcbDbPageSize,
        ULONG  * const pcHeaderPagesPerDb,
        ULONG   const piDbErrorEncountered,
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a><span data-ttu-id="4eff4-107">参数</span><span class="sxs-lookup"><span data-stu-id="4eff4-107">Parameters</span></span>

### <a name="pcbdbpagesize"></a><span data-ttu-id="4eff4-108">pcbDbPageSize</span><span class="sxs-lookup"><span data-stu-id="4eff4-108">pcbDbPageSize</span></span> 
  
<span data-ttu-id="4eff4-109">输出参数。</span><span class="sxs-lookup"><span data-stu-id="4eff4-109">Output parameter.</span></span> <span data-ttu-id="4eff4-110">每个指定的数据库，以字节为单位的页面大小。</span><span class="sxs-lookup"><span data-stu-id="4eff4-110">The page size of each of the specified databases, in bytes.</span></span>
    
### <a name="pcheaderpagesperdb"></a><span data-ttu-id="4eff4-111">pcHeaderPagesPerDb</span><span class="sxs-lookup"><span data-stu-id="4eff4-111">pcHeaderPagesPerDb</span></span> 
  
<span data-ttu-id="4eff4-112">输出参数。</span><span class="sxs-lookup"><span data-stu-id="4eff4-112">Output parameter.</span></span> <span data-ttu-id="4eff4-113">每个开头的页数指定保留供内部使用数据库引擎的数据库。</span><span class="sxs-lookup"><span data-stu-id="4eff4-113">The number of pages at the beginning of each specified database that are reserved by the database engine for internal use.</span></span> <span data-ttu-id="4eff4-114">请注意，您应该*传递标题页用于验证**ErrCheckDbPages**函数*。</span><span class="sxs-lookup"><span data-stu-id="4eff4-114">Note that you should *not* pass header pages to the **ErrCheckDbPages** function for validation.</span></span> 
    
### <a name="pidberrorencountered"></a><span data-ttu-id="4eff4-115">piDbErrorEncountered</span><span class="sxs-lookup"><span data-stu-id="4eff4-115">piDbErrorEncountered</span></span>
  
<span data-ttu-id="4eff4-116">输出参数。</span><span class="sxs-lookup"><span data-stu-id="4eff4-116">Output parameter.</span></span> <span data-ttu-id="4eff4-117">如果该函数的返回值指示错误，此参数将传递给**ErrInit**函数**rgwszDb []** 数组的索引。</span><span class="sxs-lookup"><span data-stu-id="4eff4-117">If the return value of the function indicates an error, this parameter will be an index into the **rgwszDb[]** array passed to the **ErrInit** function.</span></span> <span data-ttu-id="4eff4-118">索引的数组元素表示遇到错误的数据库。</span><span class="sxs-lookup"><span data-stu-id="4eff4-118">The indexed array element represents the database in which the error was encountered.</span></span> <span data-ttu-id="4eff4-119">如果该函数不返回错误值，此参数值无效。</span><span class="sxs-lookup"><span data-stu-id="4eff4-119">If the function does not return an error value, this parameter value is invalid.</span></span> 
    
### <a name="ulflags"></a><span data-ttu-id="4eff4-120">ulFlags</span><span class="sxs-lookup"><span data-stu-id="4eff4-120">ulFlags</span></span> 
  
<span data-ttu-id="4eff4-121">可选的输入的参数。</span><span class="sxs-lookup"><span data-stu-id="4eff4-121">Optional input parameter.</span></span> <span data-ttu-id="4eff4-122">此值保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="4eff4-122">This value is reserved for future use.</span></span> <span data-ttu-id="4eff4-123">传递的值应为 0 （零）。</span><span class="sxs-lookup"><span data-stu-id="4eff4-123">The value passed should be 0 (zero).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4eff4-124">返回值</span><span class="sxs-lookup"><span data-stu-id="4eff4-124">Return value</span></span>

<span data-ttu-id="4eff4-125">此函数返回[CChkSGFiles.ERR 枚举](cchksgfiles-err-enumeration.md)中的错误代码。</span><span class="sxs-lookup"><span data-stu-id="4eff4-125">This function returns an error code from the [CChkSGFiles.ERR enumeration](cchksgfiles-err-enumeration.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4eff4-126">注解</span><span class="sxs-lookup"><span data-stu-id="4eff4-126">Remarks</span></span>

<span data-ttu-id="4eff4-127">**ErrCheckDbHeaders**验证**ErrInit**注册的所有数据库都具有相同的日志签名和数据库页面大小。</span><span class="sxs-lookup"><span data-stu-id="4eff4-127">**ErrCheckDbHeaders** verifies that all databases registered with **ErrInit** have the same log signature and database page size.</span></span> <span data-ttu-id="4eff4-128">您可以使用最低**genMin**参数值和最高**genMax**参数值来确定所需的所有已注册数据库置于干净关闭状态的日志文件的集合。</span><span class="sxs-lookup"><span data-stu-id="4eff4-128">You can also use the lowest **genMin** parameter value and the highest **genMax** parameter value to determine the set of log files that are necessary to bring all of the registered databases to a clean-shutdown state.</span></span> 
  
<span data-ttu-id="4eff4-129">**PiDbErrorEncountered**参数设置仅在检测到错误时，由非零**ErrCheckDbHeaders**返回值。</span><span class="sxs-lookup"><span data-stu-id="4eff4-129">The **piDbErrorEncountered** parameter is set only when an error is detected, as indicated by a non-zero **ErrCheckDbHeaders** return value.</span></span> 
  
<span data-ttu-id="4eff4-130">在此函数中出现错误时发生，则 error 事件将添加到 Windows 错误事件日志。</span><span class="sxs-lookup"><span data-stu-id="4eff4-130">When an error occurs in this function, an error event will be added to the Windows Error event log.</span></span>
  
<span data-ttu-id="4eff4-131">您可以调用**ErrInit**后才, 调用**ErrCheckDbHeaders**和调用**ErrCheckDbPages**和**ErrCheckLogs**之前必须调用。</span><span class="sxs-lookup"><span data-stu-id="4eff4-131">You can call **ErrCheckDbHeaders** only after calling **ErrInit**, and you must call it before calling **ErrCheckDbPages** and **ErrCheckLogs**.</span></span>
  
<span data-ttu-id="4eff4-132">如果您使用 CHKSGFILES 多线程应用程序中，您必须**ErrCheckDbHeaders**函数调用中的单线程部分中，且您可以为每个**CCheckSGFiles**对象调用它仅执行一次。</span><span class="sxs-lookup"><span data-stu-id="4eff4-132">If you're using CHKSGFILES in a multithreaded application, you must call the **ErrCheckDbHeaders** function in the single-threaded portion, and you can call it only once for each **CCheckSGFiles** object.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="4eff4-133">要求</span><span class="sxs-lookup"><span data-stu-id="4eff4-133">Requirements</span></span>

<span data-ttu-id="4eff4-134">Exchange 2013 只包括 CHKSGFILES API 的 64 位版本。</span><span class="sxs-lookup"><span data-stu-id="4eff4-134">Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="4eff4-135">下运行该应用程序的帐户必须具有对要检查的数据库和日志文件的读取访问权限。</span><span class="sxs-lookup"><span data-stu-id="4eff4-135">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

