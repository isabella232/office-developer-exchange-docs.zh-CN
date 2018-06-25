---
title: CChkSGFiles.ERR 枚举
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ERR
api_type:
- dllExport
ms.assetid: f0efe195-91c3-4f3a-8c7d-e5dba336465a
description: 上次修改时间： 2015 年 3 月 9 日
ms.openlocfilehash: 20f10c43e3b92604bb51e1aa5f896a8bd7c4b335
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753633"
---
# <a name="cchksgfileserr-enumeration"></a><span data-ttu-id="4c0f4-103">CChkSGFiles.ERR 枚举</span><span class="sxs-lookup"><span data-stu-id="4c0f4-103">CChkSGFiles.ERR enumeration</span></span> 
  
<span data-ttu-id="4c0f4-104">**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="4c0f4-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="4c0f4-105">指示被调用的函数的结果。</span><span class="sxs-lookup"><span data-stu-id="4c0f4-105">Indicates the results of the called function.</span></span> <span data-ttu-id="4c0f4-106">此枚举由**CCheckSGFiles**类的多个函数返回。</span><span class="sxs-lookup"><span data-stu-id="4c0f4-106">This enumeration is returned by many functions of the **CCheckSGFiles** class.</span></span> 
  
```cs
Enum ERR  
{
        errSuccess = 0,
        errTaskDropped = -106,
        errRequiredLogFilesMissing = -543,
        errInvalidParameter = -1003,
        errOutOfMemory = -1011,
        errReadVerifyFailure = -1018,
        errTooManyActiveUsers = -1059,
        errDatabaseCorrupted = -1206
}

```

## <a name="values"></a><span data-ttu-id="4c0f4-107">值</span><span class="sxs-lookup"><span data-stu-id="4c0f4-107">Values</span></span>

|<span data-ttu-id="4c0f4-108">**成员名称**</span><span class="sxs-lookup"><span data-stu-id="4c0f4-108">**Member name**</span></span>|<span data-ttu-id="4c0f4-109">**值**</span><span class="sxs-lookup"><span data-stu-id="4c0f4-109">**Value**</span></span>|<span data-ttu-id="4c0f4-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="4c0f4-110">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4c0f4-111">errSuccess</span><span class="sxs-lookup"><span data-stu-id="4c0f4-111">errSuccess</span></span>  <br/> |<span data-ttu-id="4c0f4-112">0</span><span class="sxs-lookup"><span data-stu-id="4c0f4-112">0</span></span>  <br/> |<span data-ttu-id="4c0f4-113">没有任何错误完成函数。</span><span class="sxs-lookup"><span data-stu-id="4c0f4-113">The function completed without any errors.</span></span>  <br/> |
|<span data-ttu-id="4c0f4-114">errTaskDropped</span><span class="sxs-lookup"><span data-stu-id="4c0f4-114">errTaskDropped</span></span>  <br/> |<span data-ttu-id="4c0f4-115">-106</span><span class="sxs-lookup"><span data-stu-id="4c0f4-115">-106</span></span>  <br/> |<span data-ttu-id="4c0f4-116">返回由**ErrTerm**函数，以指示已选中不是所有数据库页面和事务日志文件，或验证期间遇到了错误。</span><span class="sxs-lookup"><span data-stu-id="4c0f4-116">Returned by the **ErrTerm** function to indicate that not all database pages and transaction log files were checked, or that errors were encountered during the verification.</span></span>  <br/> |
|<span data-ttu-id="4c0f4-117">errRequiredLogFilesMissing</span><span class="sxs-lookup"><span data-stu-id="4c0f4-117">errRequiredLogFilesMissing</span></span>  <br/> |<span data-ttu-id="4c0f4-118">-543</span><span class="sxs-lookup"><span data-stu-id="4c0f4-118">-543</span></span>  <br/> |<span data-ttu-id="4c0f4-119">一个或多个日志文件所需数据库置于干净关闭状态找不到在日志文件路径，或没有指定三个字母的基名称。</span><span class="sxs-lookup"><span data-stu-id="4c0f4-119">One or more log files that are required to bring the database to a clean-shutdown state was not found in the log file path, or did not have the specified three-letter base name.</span></span>  <br/> |
|<span data-ttu-id="4c0f4-120">errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="4c0f4-120">errInvalidParameter</span></span>  <br/> |<span data-ttu-id="4c0f4-121">-1003</span><span class="sxs-lookup"><span data-stu-id="4c0f4-121">-1003</span></span>  <br/> |<span data-ttu-id="4c0f4-122">一个或多个已传递给函数的参数无效。</span><span class="sxs-lookup"><span data-stu-id="4c0f4-122">One or more parameters that were passed to the function were invalid.</span></span>  <br/> |
|<span data-ttu-id="4c0f4-123">errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="4c0f4-123">errOutOfMemory</span></span>  <br/> |<span data-ttu-id="4c0f4-124">-1011</span><span class="sxs-lookup"><span data-stu-id="4c0f4-124">-1011</span></span>  <br/> |<span data-ttu-id="4c0f4-125">内存不足时可用于完成请求的操作。</span><span class="sxs-lookup"><span data-stu-id="4c0f4-125">Insufficient memory was available to complete the requested operation.</span></span>  <br/> |
|<span data-ttu-id="4c0f4-126">errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="4c0f4-126">errReadVerifyFailure</span></span>  <br/> |<span data-ttu-id="4c0f4-127">-1018</span><span class="sxs-lookup"><span data-stu-id="4c0f4-127">-1018</span></span>  <br/> |<span data-ttu-id="4c0f4-128">在数据库页上存储的校验和与其预期的校验和不匹配。</span><span class="sxs-lookup"><span data-stu-id="4c0f4-128">The checksum that is stored on a database page does not match its expected checksum.</span></span>  <br/> |
|<span data-ttu-id="4c0f4-129">errTooManyActiveUsers</span><span class="sxs-lookup"><span data-stu-id="4c0f4-129">errTooManyActiveUsers</span></span>  <br/> |<span data-ttu-id="4c0f4-130">-1059</span><span class="sxs-lookup"><span data-stu-id="4c0f4-130">-1059</span></span>  <br/> |<span data-ttu-id="4c0f4-131">仍使用该对象时调用了**ErrTerm**函数。</span><span class="sxs-lookup"><span data-stu-id="4c0f4-131">The **ErrTerm** function was called while the object was still being used.</span></span> <span data-ttu-id="4c0f4-132">发生这种情况**ErrTerm**称为之前**ErrCheckDbPages**或返回**ErrCheckLogFiles**了。</span><span class="sxs-lookup"><span data-stu-id="4c0f4-132">This can occur if **ErrTerm** is called before **ErrCheckDbPages** or **ErrCheckLogFiles** has returned.</span></span>  <br/> |
   
## <a name="requirements"></a><span data-ttu-id="4c0f4-133">要求</span><span class="sxs-lookup"><span data-stu-id="4c0f4-133">Requirements</span></span>

<span data-ttu-id="4c0f4-134">Exchange Server 2013 只包括 CHKSGFILES API 的 64 位版本。</span><span class="sxs-lookup"><span data-stu-id="4c0f4-134">Exchange Server 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="4c0f4-135">下运行该应用程序的帐户必须具有对要检查的数据库和日志文件的读取访问权限。</span><span class="sxs-lookup"><span data-stu-id="4c0f4-135">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

