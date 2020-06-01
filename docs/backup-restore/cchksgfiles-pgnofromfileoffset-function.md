---
title: CChkSGFiles 函数
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
description: 上次修改时间：2013年2月22日
ms.openlocfilehash: 3c8f749a03b4aa251bf9312eba5d7e2d46c91fae
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44452893"
---
# <a name="cchksgfilespgnofromfileoffset-function"></a><span data-ttu-id="573b2-103">CChkSGFiles 函数</span><span class="sxs-lookup"><span data-stu-id="573b2-103">CChkSGFiles.PgnoFromFileOffset function</span></span>

<span data-ttu-id="573b2-104">**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="573b2-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="573b2-105">返回与物理数据库文件中指定的字节索引相对应的逻辑数据库页面编号。</span><span class="sxs-lookup"><span data-stu-id="573b2-105">Returns the logical database page number that corresponds to the specified byte index in the physical database file.</span></span> <span data-ttu-id="573b2-106">如果文件偏移量无效，或者尚未为数据库调用**ErrCheckDbHeaders**函数，则此函数返回0（零）。</span><span class="sxs-lookup"><span data-stu-id="573b2-106">If the file offset is invalid, or if the **ErrCheckDbHeaders** function has not been called for the databases, this function returns 0 (zero).</span></span> 
  
```cs
Vitual ULONGPgnoFromFileOffset  
(
    Const ULONGLONGibFileOffset
);

```

## <a name="parameters"></a><span data-ttu-id="573b2-107">参数</span><span class="sxs-lookup"><span data-stu-id="573b2-107">Parameters</span></span>

### <a name="ibfileoffset"></a><span data-ttu-id="573b2-108">ibFileOffset</span><span class="sxs-lookup"><span data-stu-id="573b2-108">ibFileOffset</span></span>
  
<span data-ttu-id="573b2-109">输入参数。</span><span class="sxs-lookup"><span data-stu-id="573b2-109">Input parameter.</span></span> <span data-ttu-id="573b2-110">数据库文件中的偏移量（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="573b2-110">The offset into a database file, in bytes.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="573b2-111">返回值</span><span class="sxs-lookup"><span data-stu-id="573b2-111">Return value</span></span>

<span data-ttu-id="573b2-112">包含指定偏移量的数据库文件的逻辑页面编号。</span><span class="sxs-lookup"><span data-stu-id="573b2-112">The database file's logical page number that includes the specified offset.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="573b2-113">备注</span><span class="sxs-lookup"><span data-stu-id="573b2-113">Remarks</span></span>

<span data-ttu-id="573b2-114">如果**ibFileOffset**参数无效，则**PgnoFromFileOffset**函数将返回0（零）。</span><span class="sxs-lookup"><span data-stu-id="573b2-114">If the **ibFileOffset** parameter is invalid, the **PgnoFromFileOffset** function returns 0 (zero).</span></span> 
  
<span data-ttu-id="573b2-115">如果您未在**CCheckSGFiles**实例上调用**ErrCheckDbHeaders**函数，则**PgnoFromFileOffset**也返回0（零）。</span><span class="sxs-lookup"><span data-stu-id="573b2-115">**PgnoFromFileOffset** also returns 0 (zero) if you haven't called the **ErrCheckDbHeaders** function on the **CCheckSGFiles** instance.</span></span> <span data-ttu-id="573b2-116">必须调用**ErrCheckDbHeaders**以初始化数据库页面大小和分配给数据库标头的页面数。</span><span class="sxs-lookup"><span data-stu-id="573b2-116">You must call **ErrCheckDbHeaders** to initialize the database page size and number of pages allocated to database headers.</span></span> 
  
<span data-ttu-id="573b2-117">应使用**PgnoFromFileOffset**在准备调用**ErrCheckDbPages**的过程中填写**页面 \_ 信息**结构元素。</span><span class="sxs-lookup"><span data-stu-id="573b2-117">You should use **PgnoFromFileOffset** to fill in the **PAGE\_INFO** structure elements in preparation for calling **ErrCheckDbPages**.</span></span> <span data-ttu-id="573b2-118">**ErrCheckDbPages**的**rgPageInfo**参数要求数组中的每个元素都是一个**PAGE_INFO**结构，其中**ulPgno**成员的值已正确初始化。</span><span class="sxs-lookup"><span data-stu-id="573b2-118">The **rgPageInfo** parameter to **ErrCheckDbPages** requires that each element in the array be a **PAGE_INFO** structure, with the **ulPgno** member values correctly initialized.</span></span> 
  
<span data-ttu-id="573b2-119">如果要在多线程应用程序中使用 CHKSGFILES，则可以在应用程序的多线程部分调用**PgnoFromFileOffset**函数。</span><span class="sxs-lookup"><span data-stu-id="573b2-119">If you're using CHKSGFILES in a multithreaded application, you can call the **PgnoFromFileOffset** function in the multithreaded portion of the application.</span></span> <span data-ttu-id="573b2-120">请注意，对于所检查的每个数据库，通常需要多次调用此函数。</span><span class="sxs-lookup"><span data-stu-id="573b2-120">Note that you would typically call this function multiple times for each database being checked.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="573b2-121">Requirements</span><span class="sxs-lookup"><span data-stu-id="573b2-121">Requirements</span></span>

<span data-ttu-id="573b2-122">Exchange Server 2013 仅包含64位版本的 CHKSGFILES API。</span><span class="sxs-lookup"><span data-stu-id="573b2-122">Exchange Server 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="573b2-123">运行应用程序所使用的帐户必须具有对要检查的数据库和日志文件的读取权限。</span><span class="sxs-lookup"><span data-stu-id="573b2-123">The account that the application is running under must have read permission to the database and log files that are to be checked.</span></span>
  

