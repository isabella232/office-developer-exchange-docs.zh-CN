---
title: CChkSGFiles 枚举
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
description: 上次修改时间：2015 年 3 月 9 日
ms.openlocfilehash: dbc76601a808f79ce3ed5b5dc9fbe4cf92efb015
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455252"
---
# <a name="cchksgfileserr-enumeration"></a><span data-ttu-id="723cc-103">CChkSGFiles 枚举</span><span class="sxs-lookup"><span data-stu-id="723cc-103">CChkSGFiles.ERR enumeration</span></span> 
  
<span data-ttu-id="723cc-104">**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="723cc-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="723cc-105">指示被调用函数的结果。</span><span class="sxs-lookup"><span data-stu-id="723cc-105">Indicates the results of the called function.</span></span> <span data-ttu-id="723cc-106">**CCheckSGFiles**类的多个函数返回此枚举。</span><span class="sxs-lookup"><span data-stu-id="723cc-106">This enumeration is returned by many functions of the **CCheckSGFiles** class.</span></span> 
  
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

## <a name="values"></a><span data-ttu-id="723cc-107">值</span><span class="sxs-lookup"><span data-stu-id="723cc-107">Values</span></span>

|<span data-ttu-id="723cc-108">**成员名称**</span><span class="sxs-lookup"><span data-stu-id="723cc-108">**Member name**</span></span>|<span data-ttu-id="723cc-109">**值**</span><span class="sxs-lookup"><span data-stu-id="723cc-109">**Value**</span></span>|<span data-ttu-id="723cc-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="723cc-110">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="723cc-111">errSuccess</span><span class="sxs-lookup"><span data-stu-id="723cc-111">errSuccess</span></span>  <br/> |<span data-ttu-id="723cc-112">0</span><span class="sxs-lookup"><span data-stu-id="723cc-112">0</span></span>  <br/> |<span data-ttu-id="723cc-113">函数已完成，没有任何错误。</span><span class="sxs-lookup"><span data-stu-id="723cc-113">The function completed without any errors.</span></span>  <br/> |
|<span data-ttu-id="723cc-114">errTaskDropped</span><span class="sxs-lookup"><span data-stu-id="723cc-114">errTaskDropped</span></span>  <br/> |<span data-ttu-id="723cc-115">-106</span><span class="sxs-lookup"><span data-stu-id="723cc-115">-106</span></span>  <br/> |<span data-ttu-id="723cc-116">由**ErrTerm**函数返回以指示并不检查所有数据库页和事务日志文件，或者在验证过程中遇到错误。</span><span class="sxs-lookup"><span data-stu-id="723cc-116">Returned by the **ErrTerm** function to indicate that not all database pages and transaction log files were checked, or that errors were encountered during the verification.</span></span>  <br/> |
|<span data-ttu-id="723cc-117">errRequiredLogFilesMissing</span><span class="sxs-lookup"><span data-stu-id="723cc-117">errRequiredLogFilesMissing</span></span>  <br/> |<span data-ttu-id="723cc-118">-543</span><span class="sxs-lookup"><span data-stu-id="723cc-118">-543</span></span>  <br/> |<span data-ttu-id="723cc-119">在日志文件路径中找不到将数据库引入干净关闭状态所需的一个或多个日志文件，或者没有指定的三个字母的基本名称。</span><span class="sxs-lookup"><span data-stu-id="723cc-119">One or more log files that are required to bring the database to a clean-shutdown state was not found in the log file path, or did not have the specified three-letter base name.</span></span>  <br/> |
|<span data-ttu-id="723cc-120">errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="723cc-120">errInvalidParameter</span></span>  <br/> |<span data-ttu-id="723cc-121">-1003</span><span class="sxs-lookup"><span data-stu-id="723cc-121">-1003</span></span>  <br/> |<span data-ttu-id="723cc-122">传递给函数的一个或多个参数无效。</span><span class="sxs-lookup"><span data-stu-id="723cc-122">One or more parameters that were passed to the function were invalid.</span></span>  <br/> |
|<span data-ttu-id="723cc-123">errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="723cc-123">errOutOfMemory</span></span>  <br/> |<span data-ttu-id="723cc-124">-1011</span><span class="sxs-lookup"><span data-stu-id="723cc-124">-1011</span></span>  <br/> |<span data-ttu-id="723cc-125">可用内存不足，无法完成所请求的操作。</span><span class="sxs-lookup"><span data-stu-id="723cc-125">Insufficient memory was available to complete the requested operation.</span></span>  <br/> |
|<span data-ttu-id="723cc-126">errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="723cc-126">errReadVerifyFailure</span></span>  <br/> |<span data-ttu-id="723cc-127">-1018</span><span class="sxs-lookup"><span data-stu-id="723cc-127">-1018</span></span>  <br/> |<span data-ttu-id="723cc-128">存储在数据库页面上的校验和与它的预期校验和不匹配。</span><span class="sxs-lookup"><span data-stu-id="723cc-128">The checksum that is stored on a database page does not match its expected checksum.</span></span>  <br/> |
|<span data-ttu-id="723cc-129">errTooManyActiveUsers</span><span class="sxs-lookup"><span data-stu-id="723cc-129">errTooManyActiveUsers</span></span>  <br/> |<span data-ttu-id="723cc-130">-1059</span><span class="sxs-lookup"><span data-stu-id="723cc-130">-1059</span></span>  <br/> |<span data-ttu-id="723cc-131">当仍在使用对象时，调用**ErrTerm**函数。</span><span class="sxs-lookup"><span data-stu-id="723cc-131">The **ErrTerm** function was called while the object was still being used.</span></span> <span data-ttu-id="723cc-132">如果在**ErrCheckDbPages**或**ErrCheckLogFiles**返回之前调用**ErrTerm** ，则可能会发生此情况。</span><span class="sxs-lookup"><span data-stu-id="723cc-132">This can occur if **ErrTerm** is called before **ErrCheckDbPages** or **ErrCheckLogFiles** has returned.</span></span>  <br/> |
   
## <a name="requirements"></a><span data-ttu-id="723cc-133">Requirements</span><span class="sxs-lookup"><span data-stu-id="723cc-133">Requirements</span></span>

<span data-ttu-id="723cc-134">Exchange Server 2013 仅包含64位版本的 CHKSGFILES API。</span><span class="sxs-lookup"><span data-stu-id="723cc-134">Exchange Server 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="723cc-135">运行应用程序所使用的帐户必须具有对要检查的数据库和日志文件的读取访问权限。</span><span class="sxs-lookup"><span data-stu-id="723cc-135">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

