---
title: CChkSGFiles.PAGE_INFO 结构
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PAGE_INFO
api_type:
- dllExport
ms.assetid: 408335e1-6977-441f-bfad-ede791d1630c
description: 上次修改时间： 2013 年 2 月 22 日
ms.openlocfilehash: fa66d253b4fc6bd5c29a39c5323f59bf323a906f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753627"
---
# <a name="cchksgfilespageinfo-struct"></a><span data-ttu-id="72297-103">CChkSGFiles.PAGE_INFO 结构</span><span class="sxs-lookup"><span data-stu-id="72297-103">CChkSGFiles.PAGE_INFO struct</span></span>

<span data-ttu-id="72297-104">**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="72297-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="72297-105">包含一个 Exchange 数据库页的信息。</span><span class="sxs-lookup"><span data-stu-id="72297-105">Holds information for an Exchange database page.</span></span> <span data-ttu-id="72297-106">该结构用于**ErrCheckDbPages**函数。</span><span class="sxs-lookup"><span data-stu-id="72297-106">This structure is used with the **ErrCheckDbPages** function.</span></span> 
  
```cs
Struct PAGE_INFO  
{
        ULONGulPgno;
        BOOLfPageIsInitialized : 1;
        BOOLfCorrectableError : 1;
        ULONGLONGchecksumActual;
        ULONGLONGchecksumExpected;
        ULONGLONGdbTime;
        ULONGLONGchecksumPageStructure;
        ULONGLONGulFlags;
}

```

## <a name="members"></a><span data-ttu-id="72297-107">成员</span><span class="sxs-lookup"><span data-stu-id="72297-107">Members</span></span>

### <a name="ulpgno"></a><span data-ttu-id="72297-108">ulPgNo</span><span class="sxs-lookup"><span data-stu-id="72297-108">ulPgNo</span></span>
  
<span data-ttu-id="72297-109">无符号长。</span><span class="sxs-lookup"><span data-stu-id="72297-109">Unsigned Long.</span></span> <span data-ttu-id="72297-110">逻辑页的数据库页上，要检查的数。</span><span class="sxs-lookup"><span data-stu-id="72297-110">Logical page number of the database page to be checked.</span></span> <span data-ttu-id="72297-111">调用**ErrCheckDbPages**之前，必须设置此值。</span><span class="sxs-lookup"><span data-stu-id="72297-111">This value must be set before calling **ErrCheckDbPages**.</span></span> <span data-ttu-id="72297-112">如果应用程序阅读基于文件偏移量的文件，因此必须将这些文件偏移映射到逻辑页码，您将发现**PgnoFromFileOffset**方法可用来确定该字段的值。</span><span class="sxs-lookup"><span data-stu-id="72297-112">If the application is reading the file based on file offsets, and must therefore map those file offsets to logical page numbers, you will find the **PgnoFromFileOffset** method useful to determine the value for this field.</span></span> <span data-ttu-id="72297-113">**ErrCheckDbPages**不修改此值。</span><span class="sxs-lookup"><span data-stu-id="72297-113">**ErrCheckDbPages** does not modify this value.</span></span> 
    
### <a name="fpageisinitialized"></a><span data-ttu-id="72297-114">fPageIsInitialized</span><span class="sxs-lookup"><span data-stu-id="72297-114">fPageIsInitialized</span></span> 
  
<span data-ttu-id="72297-115">布尔值。</span><span class="sxs-lookup"><span data-stu-id="72297-115">Boolean.</span></span> <span data-ttu-id="72297-116">值为 TRUE 指示数据库页包含数据。</span><span class="sxs-lookup"><span data-stu-id="72297-116">A value of TRUE indicates that the database page contains data.</span></span> <span data-ttu-id="72297-117">值为 FALSE 指示页包含仅零。</span><span class="sxs-lookup"><span data-stu-id="72297-117">A value of FALSE indicates that the page contains only zeros.</span></span> <span data-ttu-id="72297-118">**ErrCheckDbPages**设置此值。</span><span class="sxs-lookup"><span data-stu-id="72297-118">**ErrCheckDbPages** sets this value.</span></span> 
    
### <a name="fcorrectableerror"></a><span data-ttu-id="72297-119">fCorrectableError</span><span class="sxs-lookup"><span data-stu-id="72297-119">fCorrectableError</span></span>
  
<span data-ttu-id="72297-120">布尔值。</span><span class="sxs-lookup"><span data-stu-id="72297-120">Boolean.</span></span> <span data-ttu-id="72297-121">值为 TRUE 指示出现在数据库页中检测到校验和不匹配，但它是可纠正错误。</span><span class="sxs-lookup"><span data-stu-id="72297-121">A value of TRUE indicates that there was a checksum mismatch detected in the database page, but that it is a correctable error.</span></span> <span data-ttu-id="72297-122">**ErrCheckDbPages**设置此值。</span><span class="sxs-lookup"><span data-stu-id="72297-122">**ErrCheckDbPages** sets this value.</span></span> 
    
### <a name="checksumactual"></a><span data-ttu-id="72297-123">checksumActual</span><span class="sxs-lookup"><span data-stu-id="72297-123">checksumActual</span></span>
  
<span data-ttu-id="72297-124">无符号的 64 位整数。</span><span class="sxs-lookup"><span data-stu-id="72297-124">Unsigned 64-bit integer.</span></span> <span data-ttu-id="72297-125">指示此逻辑页数据库中存储的校验和值。</span><span class="sxs-lookup"><span data-stu-id="72297-125">Indicates the checksum value stored in the database for this logical page.</span></span> <span data-ttu-id="72297-126">**ErrCheckDbPages**设置此值。</span><span class="sxs-lookup"><span data-stu-id="72297-126">**ErrCheckDbPages** sets this value.</span></span> 
    
### <a name="checksumexpected"></a><span data-ttu-id="72297-127">checksumExpected</span><span class="sxs-lookup"><span data-stu-id="72297-127">checksumExpected</span></span>
  
<span data-ttu-id="72297-128">无符号的 64 位整数。</span><span class="sxs-lookup"><span data-stu-id="72297-128">Unsigned 64-bit integer.</span></span> <span data-ttu-id="72297-129">这是数据库页中; 计算预期的校验和值由**ErrCheckDbPages**设置。</span><span class="sxs-lookup"><span data-stu-id="72297-129">This is the expected checksum value that is calculated for the database page; it is set by **ErrCheckDbPages**.</span></span> <span data-ttu-id="72297-130">如果此值是不同于存储在数据库页上的 （即，返回的值在**checksumActual**）， **ErrCheckDbPages**将指示此数据库页上找到错误。</span><span class="sxs-lookup"><span data-stu-id="72297-130">If this value is different from that stored on the database page (that is, the value returned in **checksumActual**), **ErrCheckDbPages** will indicate that an error was found on this database page.</span></span> 
    
### <a name="dbtime"></a><span data-ttu-id="72297-131">dbTime</span><span class="sxs-lookup"><span data-stu-id="72297-131">dbTime</span></span>
  
<span data-ttu-id="72297-132">无符号的 64 位整数。</span><span class="sxs-lookup"><span data-stu-id="72297-132">Unsigned 64-bit integer.</span></span> <span data-ttu-id="72297-133">**ErrCheckDbPages**数据库页上设置为时间戳的此成员。</span><span class="sxs-lookup"><span data-stu-id="72297-133">**ErrCheckDbPages** sets this member to the timestamp on the database page.</span></span> 
    
### <a name="checksumpagestructure"></a><span data-ttu-id="72297-134">checksumPageStructure</span><span class="sxs-lookup"><span data-stu-id="72297-134">checksumPageStructure</span></span> 
  
<span data-ttu-id="72297-135">无符号的 64 bt 整数。</span><span class="sxs-lookup"><span data-stu-id="72297-135">Unsigned 64-bt integer.</span></span> <span data-ttu-id="72297-136">**ErrCheckDbPages**将此成员设置为不包括这是不必要时确定逻辑页等价数据页上的内容的计算校验和值。</span><span class="sxs-lookup"><span data-stu-id="72297-136">**ErrCheckDbPages** sets this member to the calculated checksum value of the contents of the page excluding data which is unnecessary when determining the logical page equivalence.</span></span> <span data-ttu-id="72297-137">例如，不需要考虑未使用的数据库页空间中的数据值。</span><span class="sxs-lookup"><span data-stu-id="72297-137">For example, it is unnecessary to consider the data values in unused database page space.</span></span> <span data-ttu-id="72297-138">此成员才如果**checksumActual**和**checksumExpected**值等于每个其他有效。</span><span class="sxs-lookup"><span data-stu-id="72297-138">This member is only valid if the **checksumActual**  and  **checksumExpected**  values are equal to each other.</span></span> 
    
### <a name="ulflags"></a><span data-ttu-id="72297-139">ulFlags</span><span class="sxs-lookup"><span data-stu-id="72297-139">ulFlags</span></span>
  
<span data-ttu-id="72297-140">无符号的 64 位整数。</span><span class="sxs-lookup"><span data-stu-id="72297-140">Unsigned 64-bit integer.</span></span> <span data-ttu-id="72297-141">保留以备今后使用。</span><span class="sxs-lookup"><span data-stu-id="72297-141">Reserved for future use.</span></span> <span data-ttu-id="72297-142">此字段的值必须调用**ErrCheckDbPages**之前设置为 0 （零）。</span><span class="sxs-lookup"><span data-stu-id="72297-142">The value of this field must be set to 0 (zero) before calling **ErrCheckDbPages**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="72297-143">注解</span><span class="sxs-lookup"><span data-stu-id="72297-143">Remarks</span></span>

<span data-ttu-id="72297-144">调用**ErrCheckDbPages**函数的**rgPageInfo**参数是一个数组**页\_INFO**结构。</span><span class="sxs-lookup"><span data-stu-id="72297-144">When calling the **ErrCheckDbPages** function, the **rgPageInfo**  parameter is an array of **PAGE\_INFO** structures.</span></span> <span data-ttu-id="72297-145">必须有一个**页\_INFO**要检查每个数据库页的结构。</span><span class="sxs-lookup"><span data-stu-id="72297-145">There must be one **PAGE\_INFO** structure for each database page to be checked.</span></span> 
  
<span data-ttu-id="72297-146">应用程序必须设置为适当值， **ulPgno**成员，还必须将**ulFlags**成员为 0 （零） 调用**ErrCheckDbPages**之前。</span><span class="sxs-lookup"><span data-stu-id="72297-146">The application must set the **ulPgno**  member to the proper value, and must also set the  **ulFlags**  member to 0 (zero) before calling **ErrCheckDbPages**.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="72297-147">要求</span><span class="sxs-lookup"><span data-stu-id="72297-147">Requirements</span></span>

<span data-ttu-id="72297-148">Exchange Server 2013 只包括 CHKSGFILES API 的 64 位版本。</span><span class="sxs-lookup"><span data-stu-id="72297-148">Exchange Server 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="72297-149">下运行该应用程序的帐户必须具有对要检查的数据库和日志文件的读取访问权限。</span><span class="sxs-lookup"><span data-stu-id="72297-149">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

