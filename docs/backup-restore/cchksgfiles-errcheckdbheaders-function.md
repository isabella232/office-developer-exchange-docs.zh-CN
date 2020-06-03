---
title: CChkSGFiles 函数
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
description: 上次修改时间：2013年2月22日
ms.openlocfilehash: a62c5940322d3d7a71f2db93214f1e970fc6859b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455245"
---
# <a name="cchksgfileserrcheckdbheaders-function"></a><span data-ttu-id="90eba-103">CChkSGFiles 函数</span><span class="sxs-lookup"><span data-stu-id="90eba-103">CChkSGFiles.ErrCheckDbHeaders function</span></span>

<span data-ttu-id="90eba-104">**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="90eba-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span> 
  
<span data-ttu-id="90eba-105">验证由**ErrInit**函数指定的数据库文件的标头。</span><span class="sxs-lookup"><span data-stu-id="90eba-105">Validates the headers of the database files that were specified by the **ErrInit** function.</span></span> <span data-ttu-id="90eba-106">此函数还返回每个指定数据库中的页面大小和页面数目。</span><span class="sxs-lookup"><span data-stu-id="90eba-106">This function also returns the page size and number of pages in each of the specified databases.</span></span> 
  
```cs
Vitual ERRErrCheckDbHeaders  
(
        ULONG  * const pcbDbPageSize,
        ULONG  * const pcHeaderPagesPerDb,
        ULONG   const piDbErrorEncountered,
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a><span data-ttu-id="90eba-107">参数</span><span class="sxs-lookup"><span data-stu-id="90eba-107">Parameters</span></span>

### <a name="pcbdbpagesize"></a><span data-ttu-id="90eba-108">pcbDbPageSize</span><span class="sxs-lookup"><span data-stu-id="90eba-108">pcbDbPageSize</span></span> 
  
<span data-ttu-id="90eba-109">输出参数。</span><span class="sxs-lookup"><span data-stu-id="90eba-109">Output parameter.</span></span> <span data-ttu-id="90eba-110">每个指定数据库的页面大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="90eba-110">The page size of each of the specified databases, in bytes.</span></span>
    
### <a name="pcheaderpagesperdb"></a><span data-ttu-id="90eba-111">pcHeaderPagesPerDb</span><span class="sxs-lookup"><span data-stu-id="90eba-111">pcHeaderPagesPerDb</span></span> 
  
<span data-ttu-id="90eba-112">输出参数。</span><span class="sxs-lookup"><span data-stu-id="90eba-112">Output parameter.</span></span> <span data-ttu-id="90eba-113">在每个指定数据库的开头，由数据库引擎保留以供内部使用的页面数。</span><span class="sxs-lookup"><span data-stu-id="90eba-113">The number of pages at the beginning of each specified database that are reserved by the database engine for internal use.</span></span> <span data-ttu-id="90eba-114">请注意，*不*应将标头页传递给**ErrCheckDbPages**函数以进行验证。</span><span class="sxs-lookup"><span data-stu-id="90eba-114">Note that you should *not* pass header pages to the **ErrCheckDbPages** function for validation.</span></span> 
    
### <a name="pidberrorencountered"></a><span data-ttu-id="90eba-115">piDbErrorEncountered</span><span class="sxs-lookup"><span data-stu-id="90eba-115">piDbErrorEncountered</span></span>
  
<span data-ttu-id="90eba-116">输出参数。</span><span class="sxs-lookup"><span data-stu-id="90eba-116">Output parameter.</span></span> <span data-ttu-id="90eba-117">如果函数的返回值指示错误，则此参数将是传递给**ErrInit**函数的**rgwszDb []** 数组的索引。</span><span class="sxs-lookup"><span data-stu-id="90eba-117">If the return value of the function indicates an error, this parameter will be an index into the **rgwszDb[]** array passed to the **ErrInit** function.</span></span> <span data-ttu-id="90eba-118">已编制索引的数组元素表示遇到错误的数据库。</span><span class="sxs-lookup"><span data-stu-id="90eba-118">The indexed array element represents the database in which the error was encountered.</span></span> <span data-ttu-id="90eba-119">如果函数不返回错误值，则此参数值无效。</span><span class="sxs-lookup"><span data-stu-id="90eba-119">If the function does not return an error value, this parameter value is invalid.</span></span> 
    
### <a name="ulflags"></a><span data-ttu-id="90eba-120">ulFlags</span><span class="sxs-lookup"><span data-stu-id="90eba-120">ulFlags</span></span> 
  
<span data-ttu-id="90eba-121">可选的输入参数。</span><span class="sxs-lookup"><span data-stu-id="90eba-121">Optional input parameter.</span></span> <span data-ttu-id="90eba-122">保留此值以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="90eba-122">This value is reserved for future use.</span></span> <span data-ttu-id="90eba-123">传递的值应为0（零）。</span><span class="sxs-lookup"><span data-stu-id="90eba-123">The value passed should be 0 (zero).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="90eba-124">返回值</span><span class="sxs-lookup"><span data-stu-id="90eba-124">Return value</span></span>

<span data-ttu-id="90eba-125">此函数返回[CChkSGFiles 枚举](cchksgfiles-err-enumeration.md)中的错误代码。</span><span class="sxs-lookup"><span data-stu-id="90eba-125">This function returns an error code from the [CChkSGFiles.ERR enumeration](cchksgfiles-err-enumeration.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="90eba-126">备注</span><span class="sxs-lookup"><span data-stu-id="90eba-126">Remarks</span></span>

<span data-ttu-id="90eba-127">**ErrCheckDbHeaders**验证使用**ErrInit**注册的所有数据库是否具有相同的日志签名和数据库页面大小。</span><span class="sxs-lookup"><span data-stu-id="90eba-127">**ErrCheckDbHeaders** verifies that all databases registered with **ErrInit** have the same log signature and database page size.</span></span> <span data-ttu-id="90eba-128">您还可以使用最低的**genMin**参数值和最高的**genMax**参数值来确定将所有已注册的数据库置于干净关闭状态所需的一组日志文件。</span><span class="sxs-lookup"><span data-stu-id="90eba-128">You can also use the lowest **genMin** parameter value and the highest **genMax** parameter value to determine the set of log files that are necessary to bring all of the registered databases to a clean-shutdown state.</span></span> 
  
<span data-ttu-id="90eba-129">仅当检测到错误（由非零**ErrCheckDbHeaders**返回值所指示）时，才会设置**piDbErrorEncountered**参数。</span><span class="sxs-lookup"><span data-stu-id="90eba-129">The **piDbErrorEncountered** parameter is set only when an error is detected, as indicated by a non-zero **ErrCheckDbHeaders** return value.</span></span> 
  
<span data-ttu-id="90eba-130">当此函数中出现错误时，将向 Windows 错误事件日志中添加一个错误事件。</span><span class="sxs-lookup"><span data-stu-id="90eba-130">When an error occurs in this function, an error event will be added to the Windows Error event log.</span></span>
  
<span data-ttu-id="90eba-131">只能在调用**ErrInit**后调用**ErrCheckDbHeaders** ，并且必须先调用它，然后才能调用**ErrCheckDbPages**和**ErrCheckLogs**。</span><span class="sxs-lookup"><span data-stu-id="90eba-131">You can call **ErrCheckDbHeaders** only after calling **ErrInit**, and you must call it before calling **ErrCheckDbPages** and **ErrCheckLogs**.</span></span>
  
<span data-ttu-id="90eba-132">如果要在多线程应用程序中使用 CHKSGFILES，则必须在单线程部分调用**ErrCheckDbHeaders**函数，并且只能为每个**CCheckSGFiles**对象调用一次该函数。</span><span class="sxs-lookup"><span data-stu-id="90eba-132">If you're using CHKSGFILES in a multithreaded application, you must call the **ErrCheckDbHeaders** function in the single-threaded portion, and you can call it only once for each **CCheckSGFiles** object.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="90eba-133">Requirements</span><span class="sxs-lookup"><span data-stu-id="90eba-133">Requirements</span></span>

<span data-ttu-id="90eba-134">Exchange 2013 仅包含64位版本的 CHKSGFILES API。</span><span class="sxs-lookup"><span data-stu-id="90eba-134">Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="90eba-135">运行应用程序所使用的帐户必须具有对要检查的数据库和日志文件的读取访问权限。</span><span class="sxs-lookup"><span data-stu-id="90eba-135">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

