---
title: CChkSGFiles.PgnoFromFileOffset 函数
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PgnoFromFileOffset
api_type:
- dllExport
ms.assetid: 3d69ca6d-5ed1-4038-859e-106e776eeec1
description: 上次修改时间： 2013 年 2 月 22 日
ms.openlocfilehash: d42ba7c8178c6fccdddec0b5da88a972f51184c6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752695"
---
# <a name="cchksgfilespgnofromfileoffset-function"></a><span data-ttu-id="9e4ad-103">CChkSGFiles.PgnoFromFileOffset 函数</span><span class="sxs-lookup"><span data-stu-id="9e4ad-103">CChkSGFiles.PgnoFromFileOffset function</span></span>

<span data-ttu-id="9e4ad-104">**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="9e4ad-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="9e4ad-105">返回到物理数据库文件中指定的字节索引的逻辑数据库页码对应。</span><span class="sxs-lookup"><span data-stu-id="9e4ad-105">Returns the logical database page number that corresponds to the specified byte index in the physical database file.</span></span> <span data-ttu-id="9e4ad-106">如果文件偏移量无效，或尚未**ErrCheckDbHeaders**函数调用的数据库，此函数将返回 0 （零）。</span><span class="sxs-lookup"><span data-stu-id="9e4ad-106">If the file offset is invalid, or if the **ErrCheckDbHeaders** function has not been called for the databases, this function returns 0 (zero).</span></span> 
  
```cs
Vitual ULONGPgnoFromFileOffset  
(
    Const ULONGLONGibFileOffset
);

```

## <a name="parameters"></a><span data-ttu-id="9e4ad-107">参数</span><span class="sxs-lookup"><span data-stu-id="9e4ad-107">Parameters</span></span>

### <a name="ibfileoffset"></a><span data-ttu-id="9e4ad-108">ibFileOffset</span><span class="sxs-lookup"><span data-stu-id="9e4ad-108">ibFileOffset</span></span>
  
<span data-ttu-id="9e4ad-109">输入的参数。</span><span class="sxs-lookup"><span data-stu-id="9e4ad-109">Input parameter.</span></span> <span data-ttu-id="9e4ad-110">偏移量数据库文件，以字节为单位。</span><span class="sxs-lookup"><span data-stu-id="9e4ad-110">The offset into a database file, in bytes.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9e4ad-111">返回值</span><span class="sxs-lookup"><span data-stu-id="9e4ad-111">Return value</span></span>

<span data-ttu-id="9e4ad-112">数据库文件的逻辑页码，其中包含指定的偏移量。</span><span class="sxs-lookup"><span data-stu-id="9e4ad-112">The database file's logical page number that includes the specified offset.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9e4ad-113">注解</span><span class="sxs-lookup"><span data-stu-id="9e4ad-113">Remarks</span></span>

<span data-ttu-id="9e4ad-114">如果**ibFileOffset**参数无效，则**PgnoFromFileOffset**函数将返回 0 （零）。</span><span class="sxs-lookup"><span data-stu-id="9e4ad-114">If the **ibFileOffset** parameter is invalid, the **PgnoFromFileOffset** function returns 0 (zero).</span></span> 
  
<span data-ttu-id="9e4ad-115">如果您尚未对**CCheckSGFiles**实例调用**ErrCheckDbHeaders**函数， **PgnoFromFileOffset**还返回 0 （零）。</span><span class="sxs-lookup"><span data-stu-id="9e4ad-115">**PgnoFromFileOffset** also returns 0 (zero) if you haven't called the **ErrCheckDbHeaders** function on the **CCheckSGFiles** instance.</span></span> <span data-ttu-id="9e4ad-116">您必须调用**ErrCheckDbHeaders**初始化数据库页面大小和分配到数据库标头的页数。</span><span class="sxs-lookup"><span data-stu-id="9e4ad-116">You must call **ErrCheckDbHeaders** to initialize the database page size and number of pages allocated to database headers.</span></span> 
  
<span data-ttu-id="9e4ad-117">您应使用**PgnoFromFileOffset**填充**页\_INFO**结构调用**ErrCheckDbPages**准备过程中的元素。</span><span class="sxs-lookup"><span data-stu-id="9e4ad-117">You should use **PgnoFromFileOffset** to fill in the **PAGE\_INFO** structure elements in preparation for calling **ErrCheckDbPages**.</span></span> <span data-ttu-id="9e4ad-118">**ErrCheckDbPages** **rgPageInfo**参数要求数组中的每个元素的**PAGE_INFO**结构，用正确初始化**ulPgno**成员值。</span><span class="sxs-lookup"><span data-stu-id="9e4ad-118">The **rgPageInfo** parameter to **ErrCheckDbPages** requires that each element in the array be a **PAGE_INFO** structure, with the **ulPgno** member values correctly initialized.</span></span> 
  
<span data-ttu-id="9e4ad-119">如果您使用 CHKSGFILES 多线程应用程序中，您可以在应用程序的多线程部分调用**PgnoFromFileOffset**函数。</span><span class="sxs-lookup"><span data-stu-id="9e4ad-119">If you're using CHKSGFILES in a multithreaded application, you can call the **PgnoFromFileOffset** function in the multithreaded portion of the application.</span></span> <span data-ttu-id="9e4ad-120">请注意，您就可以通常调用此函数多次所检查每个数据库。</span><span class="sxs-lookup"><span data-stu-id="9e4ad-120">Note that you would typically call this function multiple times for each database being checked.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="9e4ad-121">要求</span><span class="sxs-lookup"><span data-stu-id="9e4ad-121">Requirements</span></span>

<span data-ttu-id="9e4ad-122">Exchange Server 2013 只包括 CHKSGFILES API 的 64 位版本。</span><span class="sxs-lookup"><span data-stu-id="9e4ad-122">Exchange Server 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="9e4ad-123">下运行该应用程序的帐户必须具有读取权限要检查的数据库和日志文件。</span><span class="sxs-lookup"><span data-stu-id="9e4ad-123">The account that the application is running under must have read permission to the database and log files that are to be checked.</span></span>
  

