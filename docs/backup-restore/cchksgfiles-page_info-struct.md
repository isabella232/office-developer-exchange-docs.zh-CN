---
title: CChkSGFiles 结构 PAGE_INFO 结构
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
description: 上次修改时间：2013年2月22日
ms.openlocfilehash: 5ec9f4303b26ea95b125adac6943945ae1276439
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456337"
---
# <a name="cchksgfilespage_info-struct"></a><span data-ttu-id="f4f52-103">CChkSGFiles 结构 PAGE_INFO 结构</span><span class="sxs-lookup"><span data-stu-id="f4f52-103">CChkSGFiles.PAGE_INFO struct</span></span>

<span data-ttu-id="f4f52-104">**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="f4f52-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="f4f52-105">保留 Exchange 数据库页面的信息。</span><span class="sxs-lookup"><span data-stu-id="f4f52-105">Holds information for an Exchange database page.</span></span> <span data-ttu-id="f4f52-106">此结构与**ErrCheckDbPages**函数一起使用。</span><span class="sxs-lookup"><span data-stu-id="f4f52-106">This structure is used with the **ErrCheckDbPages** function.</span></span> 
  
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

## <a name="members"></a><span data-ttu-id="f4f52-107">Members</span><span class="sxs-lookup"><span data-stu-id="f4f52-107">Members</span></span>

### <a name="ulpgno"></a><span data-ttu-id="f4f52-108">ulPgNo</span><span class="sxs-lookup"><span data-stu-id="f4f52-108">ulPgNo</span></span>
  
<span data-ttu-id="f4f52-109">无符号长。</span><span class="sxs-lookup"><span data-stu-id="f4f52-109">Unsigned Long.</span></span> <span data-ttu-id="f4f52-110">要检查的数据库页面的逻辑页面编号。</span><span class="sxs-lookup"><span data-stu-id="f4f52-110">Logical page number of the database page to be checked.</span></span> <span data-ttu-id="f4f52-111">在调用**ErrCheckDbPages**之前，必须先设置此值。</span><span class="sxs-lookup"><span data-stu-id="f4f52-111">This value must be set before calling **ErrCheckDbPages**.</span></span> <span data-ttu-id="f4f52-112">如果应用程序正在根据文件偏移量读取文件，并且必须将这些文件偏移量映射到逻辑页码，则您将发现**PgnoFromFileOffset**方法对于确定此字段的值很有用。</span><span class="sxs-lookup"><span data-stu-id="f4f52-112">If the application is reading the file based on file offsets, and must therefore map those file offsets to logical page numbers, you will find the **PgnoFromFileOffset** method useful to determine the value for this field.</span></span> <span data-ttu-id="f4f52-113">**ErrCheckDbPages**不会修改此值。</span><span class="sxs-lookup"><span data-stu-id="f4f52-113">**ErrCheckDbPages** does not modify this value.</span></span> 
    
### <a name="fpageisinitialized"></a><span data-ttu-id="f4f52-114">fPageIsInitialized</span><span class="sxs-lookup"><span data-stu-id="f4f52-114">fPageIsInitialized</span></span> 
  
<span data-ttu-id="f4f52-115">布尔.</span><span class="sxs-lookup"><span data-stu-id="f4f52-115">Boolean.</span></span> <span data-ttu-id="f4f52-116">如果值为 TRUE，则表示数据库页包含数据。</span><span class="sxs-lookup"><span data-stu-id="f4f52-116">A value of TRUE indicates that the database page contains data.</span></span> <span data-ttu-id="f4f52-117">如果值为 FALSE，则表示页面仅包含零。</span><span class="sxs-lookup"><span data-stu-id="f4f52-117">A value of FALSE indicates that the page contains only zeros.</span></span> <span data-ttu-id="f4f52-118">**ErrCheckDbPages**设置此值。</span><span class="sxs-lookup"><span data-stu-id="f4f52-118">**ErrCheckDbPages** sets this value.</span></span> 
    
### <a name="fcorrectableerror"></a><span data-ttu-id="f4f52-119">fCorrectableError</span><span class="sxs-lookup"><span data-stu-id="f4f52-119">fCorrectableError</span></span>
  
<span data-ttu-id="f4f52-120">布尔.</span><span class="sxs-lookup"><span data-stu-id="f4f52-120">Boolean.</span></span> <span data-ttu-id="f4f52-121">值为 TRUE 表示在数据库页面中检测到校验和不匹配，但这是一个可更正的错误。</span><span class="sxs-lookup"><span data-stu-id="f4f52-121">A value of TRUE indicates that there was a checksum mismatch detected in the database page, but that it is a correctable error.</span></span> <span data-ttu-id="f4f52-122">**ErrCheckDbPages**设置此值。</span><span class="sxs-lookup"><span data-stu-id="f4f52-122">**ErrCheckDbPages** sets this value.</span></span> 
    
### <a name="checksumactual"></a><span data-ttu-id="f4f52-123">checksumActual</span><span class="sxs-lookup"><span data-stu-id="f4f52-123">checksumActual</span></span>
  
<span data-ttu-id="f4f52-124">无符号64位整数。</span><span class="sxs-lookup"><span data-stu-id="f4f52-124">Unsigned 64-bit integer.</span></span> <span data-ttu-id="f4f52-125">指示存储在此逻辑页面的数据库中的校验和值。</span><span class="sxs-lookup"><span data-stu-id="f4f52-125">Indicates the checksum value stored in the database for this logical page.</span></span> <span data-ttu-id="f4f52-126">**ErrCheckDbPages**设置此值。</span><span class="sxs-lookup"><span data-stu-id="f4f52-126">**ErrCheckDbPages** sets this value.</span></span> 
    
### <a name="checksumexpected"></a><span data-ttu-id="f4f52-127">checksumExpected</span><span class="sxs-lookup"><span data-stu-id="f4f52-127">checksumExpected</span></span>
  
<span data-ttu-id="f4f52-128">无符号64位整数。</span><span class="sxs-lookup"><span data-stu-id="f4f52-128">Unsigned 64-bit integer.</span></span> <span data-ttu-id="f4f52-129">这是为数据库页面计算的预期校验和值;它是由**ErrCheckDbPages**设置的。</span><span class="sxs-lookup"><span data-stu-id="f4f52-129">This is the expected checksum value that is calculated for the database page; it is set by **ErrCheckDbPages**.</span></span> <span data-ttu-id="f4f52-130">如果此值不同于存储在数据库页面上的值（即，在**checksumActual**中返回的值），则**ErrCheckDbPages**将指示在此数据库页面上发现了一个错误。</span><span class="sxs-lookup"><span data-stu-id="f4f52-130">If this value is different from that stored on the database page (that is, the value returned in **checksumActual**), **ErrCheckDbPages** will indicate that an error was found on this database page.</span></span> 
    
### <a name="dbtime"></a><span data-ttu-id="f4f52-131">dbTime</span><span class="sxs-lookup"><span data-stu-id="f4f52-131">dbTime</span></span>
  
<span data-ttu-id="f4f52-132">无符号64位整数。</span><span class="sxs-lookup"><span data-stu-id="f4f52-132">Unsigned 64-bit integer.</span></span> <span data-ttu-id="f4f52-133">**ErrCheckDbPages**将此成员设置为数据库页面上的时间戳。</span><span class="sxs-lookup"><span data-stu-id="f4f52-133">**ErrCheckDbPages** sets this member to the timestamp on the database page.</span></span> 
    
### <a name="checksumpagestructure"></a><span data-ttu-id="f4f52-134">checksumPageStructure</span><span class="sxs-lookup"><span data-stu-id="f4f52-134">checksumPageStructure</span></span> 
  
<span data-ttu-id="f4f52-135">无符号 64-bt 整数。</span><span class="sxs-lookup"><span data-stu-id="f4f52-135">Unsigned 64-bt integer.</span></span> <span data-ttu-id="f4f52-136">**ErrCheckDbPages**将此成员设置为页面内容的计算的校验和值，而不需要在确定逻辑页面等效性时不需要的数据。</span><span class="sxs-lookup"><span data-stu-id="f4f52-136">**ErrCheckDbPages** sets this member to the calculated checksum value of the contents of the page excluding data which is unnecessary when determining the logical page equivalence.</span></span> <span data-ttu-id="f4f52-137">例如，不需要考虑未使用的数据库页面空间中的数据值。</span><span class="sxs-lookup"><span data-stu-id="f4f52-137">For example, it is unnecessary to consider the data values in unused database page space.</span></span> <span data-ttu-id="f4f52-138">仅当**checksumActual**和**checksumExpected**值彼此相等时，此成员才有效。</span><span class="sxs-lookup"><span data-stu-id="f4f52-138">This member is only valid if the **checksumActual**  and  **checksumExpected**  values are equal to each other.</span></span> 
    
### <a name="ulflags"></a><span data-ttu-id="f4f52-139">ulFlags</span><span class="sxs-lookup"><span data-stu-id="f4f52-139">ulFlags</span></span>
  
<span data-ttu-id="f4f52-140">无符号64位整数。</span><span class="sxs-lookup"><span data-stu-id="f4f52-140">Unsigned 64-bit integer.</span></span> <span data-ttu-id="f4f52-141">保留供以后使用。</span><span class="sxs-lookup"><span data-stu-id="f4f52-141">Reserved for future use.</span></span> <span data-ttu-id="f4f52-142">在调用**ErrCheckDbPages**之前，必须将此字段的值设置为0（零）。</span><span class="sxs-lookup"><span data-stu-id="f4f52-142">The value of this field must be set to 0 (zero) before calling **ErrCheckDbPages**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f4f52-143">备注</span><span class="sxs-lookup"><span data-stu-id="f4f52-143">Remarks</span></span>

<span data-ttu-id="f4f52-144">调用**ErrCheckDbPages**函数时， **RgPageInfo**参数是**页面 \_ 信息**结构的数组。</span><span class="sxs-lookup"><span data-stu-id="f4f52-144">When calling the **ErrCheckDbPages** function, the **rgPageInfo**  parameter is an array of **PAGE\_INFO** structures.</span></span> <span data-ttu-id="f4f52-145">对于要检查的每个数据库页面，必须有一个**页面 \_ 信息**结构。</span><span class="sxs-lookup"><span data-stu-id="f4f52-145">There must be one **PAGE\_INFO** structure for each database page to be checked.</span></span> 
  
<span data-ttu-id="f4f52-146">应用程序必须将**ulPgno**成员设置为适当的值，并且还必须在调用**ErrCheckDbPages**之前将**ulFlags**成员设置为0（零）。</span><span class="sxs-lookup"><span data-stu-id="f4f52-146">The application must set the **ulPgno**  member to the proper value, and must also set the  **ulFlags**  member to 0 (zero) before calling **ErrCheckDbPages**.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="f4f52-147">Requirements</span><span class="sxs-lookup"><span data-stu-id="f4f52-147">Requirements</span></span>

<span data-ttu-id="f4f52-148">Exchange Server 2013 仅包含64位版本的 CHKSGFILES API。</span><span class="sxs-lookup"><span data-stu-id="f4f52-148">Exchange Server 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="f4f52-149">运行应用程序所使用的帐户必须具有对要检查的数据库和日志文件的读取访问权限。</span><span class="sxs-lookup"><span data-stu-id="f4f52-149">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

