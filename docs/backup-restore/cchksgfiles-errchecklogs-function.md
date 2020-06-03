---
title: CChkSGFiles 函数
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ErrCheckLogs
api_type:
- dllExport
ms.assetid: cec0df4b-4679-4682-bacf-69b4f4aef343
description: 上次修改时间：2013年2月22日
ms.openlocfilehash: 71e21bb3a748a532f9e3167e0b36898acde71b02
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526716"
---
# <a name="cchksgfileserrchecklogs-function"></a><span data-ttu-id="bb32e-103">CChkSGFiles 函数</span><span class="sxs-lookup"><span data-stu-id="bb32e-103">CChkSGFiles.ErrCheckLogs function</span></span>

<span data-ttu-id="bb32e-104">**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="bb32e-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="bb32e-105">验证在**ErrInit**函数中指定的所有数据库文件的日志文件。</span><span class="sxs-lookup"><span data-stu-id="bb32e-105">Validates the log files of all the database files that were specified in the **ErrInit** function.</span></span> <span data-ttu-id="bb32e-106">经过验证的日志是指路径中存在的日志，并将三个字母的基本日志文件名传递给**ErrInit**。</span><span class="sxs-lookup"><span data-stu-id="bb32e-106">The validated logs are those that exist in the path, and that have the three-letter base log file name passed to **ErrInit**.</span></span>
  
```cs
Vitual ERRErrCheckLogs 
(
        BOOL  * const pfOnlyUnnecessaryLogsCorrup,
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a><span data-ttu-id="bb32e-107">参数</span><span class="sxs-lookup"><span data-stu-id="bb32e-107">Parameters</span></span>

### <a name="pfonlyunnecessarylogscorrupt"></a><span data-ttu-id="bb32e-108">pfOnlyUnnecessaryLogsCorrupt</span><span class="sxs-lookup"><span data-stu-id="bb32e-108">pfOnlyUnnecessaryLogsCorrupt</span></span> 
  
<span data-ttu-id="bb32e-109">输出参数。</span><span class="sxs-lookup"><span data-stu-id="bb32e-109">Output parameter.</span></span> <span data-ttu-id="bb32e-110">如果**为 true，则**此参数指示在事务日志文件中发现错误，但这些错误都在日志文件中，这些错误在不丢失数据的情况下，不需要将数据库置于干净关闭状态。</span><span class="sxs-lookup"><span data-stu-id="bb32e-110">When **true**, this parameter indicates that errors were found in the transaction log files, but those errors were all found in log files that are not needed to bring the database to a clean-shutdown state without data loss.</span></span> <span data-ttu-id="bb32e-111">此参数中返回的**true**值仅在**ErrCheckLogs**返回**errSuccess**时有效。</span><span class="sxs-lookup"><span data-stu-id="bb32e-111">A **true** value returned in this parameter is valid only when **ErrCheckLogs** returns **errSuccess**.</span></span> 
    
### <a name="ulflags"></a><span data-ttu-id="bb32e-112">ulFlags</span><span class="sxs-lookup"><span data-stu-id="bb32e-112">ulFlags</span></span>
  
<span data-ttu-id="bb32e-113">可选的输入参数。</span><span class="sxs-lookup"><span data-stu-id="bb32e-113">Optional input parameter.</span></span> <span data-ttu-id="bb32e-114">保留此值以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="bb32e-114">This value is reserved for future use.</span></span> <span data-ttu-id="bb32e-115">此参数传递的值应为0（零）。</span><span class="sxs-lookup"><span data-stu-id="bb32e-115">The value passed by this parameter should be 0 (zero).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bb32e-116">返回值</span><span class="sxs-lookup"><span data-stu-id="bb32e-116">Return value</span></span>

<span data-ttu-id="bb32e-117">[ERR](cchksgfiles-err-enumeration.md)枚举中的错误代码。</span><span class="sxs-lookup"><span data-stu-id="bb32e-117">An error code from the [ERR](cchksgfiles-err-enumeration.md) enumeration.</span></span> 
  
<span data-ttu-id="bb32e-118">请务必记住，即使在日志文件中发现错误，此函数也可以返回**errSuccess** 。</span><span class="sxs-lookup"><span data-stu-id="bb32e-118">It's important to remember that this function can return **errSuccess** even when errors are found in the log files.</span></span> <span data-ttu-id="bb32e-119">因此，当**ErrCheckLogs**返回**errSuccess**时，应用程序还应检查**pfOnlyUnnecessaryLogsCorrupt**返回参数。</span><span class="sxs-lookup"><span data-stu-id="bb32e-119">Therefore, when **ErrCheckLogs** returns **errSuccess**, the application should also check the  **pfOnlyUnnecessaryLogsCorrupt** return parameter.</span></span> <span data-ttu-id="bb32e-120">如果**ErrCheckLogs**返回**errSuccess**时**pfOnlyUnnecessaryLogsCorrupts**为**true** ，则表示发现一个或多个错误，但仅在不需要将数据库更新为最新的日志文件中。</span><span class="sxs-lookup"><span data-stu-id="bb32e-120">If **pfOnlyUnnecessaryLogsCorrupts** is **true** when **ErrCheckLogs** returns **errSuccess**, this indicates that one or more errors were found, but only in log files not needed to bring the database up-to-date.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bb32e-121">备注</span><span class="sxs-lookup"><span data-stu-id="bb32e-121">Remarks</span></span>

<span data-ttu-id="bb32e-122">必须先调用**ErrCheckDbHeaders**函数，然后才能调用**ErrCheckLogs**函数。</span><span class="sxs-lookup"><span data-stu-id="bb32e-122">The **ErrCheckDbHeaders** function must be called before the **ErrCheckLogs** function can be called.</span></span> 
  
<span data-ttu-id="bb32e-123">检查 Exchange 数据库事务日志文件时，必须有一些日志文件将存储组中的数据库置于干净关闭状态，而不会丢失数据，而可能不需要其他日志文件。</span><span class="sxs-lookup"><span data-stu-id="bb32e-123">When Exchange database transaction log files are being checked, some of the log files will be necessary to bring the databases in the storage group to a clean-shutdown state without data loss, whereas other log files might not be needed.</span></span> <span data-ttu-id="bb32e-124">**ErrCheckLogs**函数确定将数据库更新为最新所需的最旧和最新日志文件。</span><span class="sxs-lookup"><span data-stu-id="bb32e-124">The **ErrCheckLogs** function determines both the oldest and the newest log files that are needed to bring the databases up to date.</span></span> 
  
<span data-ttu-id="bb32e-125">**ErrCheckLogs**函数验证指定路径中的所有日志文件，这些日志文件也具有指定的三个字母的基本文件名（传递给**ErrInit**函数）。</span><span class="sxs-lookup"><span data-stu-id="bb32e-125">The **ErrCheckLogs** function verifies all the log files in the specified paths that also have the specified three-letter base file name, as passed to the **ErrInit** function.</span></span> 
  
<span data-ttu-id="bb32e-126">如果日志文件中未发现任何错误， **ErrCheckLogs**将返回**errSuccess**。</span><span class="sxs-lookup"><span data-stu-id="bb32e-126">If no errors are found in the log files, **ErrCheckLogs** returns **errSuccess**.</span></span> 
  
<span data-ttu-id="bb32e-127">如果发现任何所需的日志文件已损坏， **ErrCheckLogs**将返回错误。</span><span class="sxs-lookup"><span data-stu-id="bb32e-127">If any of the required log files are found to be corrupted, **ErrCheckLogs** returns an error.</span></span> 
  
<span data-ttu-id="bb32e-128">如果仅在日志文件中找到比所需的最早时间更早的错误，函数将返回**errSuccess** ，并将返回参数**pfOnlyUnnecessaryLogCorrupt**设置为**true**。</span><span class="sxs-lookup"><span data-stu-id="bb32e-128">If errors are found only in log files that are older than the earliest ones needed, the function returns **errSuccess** and sets the return parameter **pfOnlyUnnecessaryLogCorrupt** to **true**.</span></span> <span data-ttu-id="bb32e-129">应用程序应识别某些旧日志文件中存在错误，如果是，则可能会提醒用户。</span><span class="sxs-lookup"><span data-stu-id="bb32e-129">The application should recognize that there are errors in some of those old log files, and if so, it will possibly alert the user.</span></span> <span data-ttu-id="bb32e-130">在任何情况下，这些错误都不会影响数据库的整体完整性，也不会影响播放日志是否将成功。</span><span class="sxs-lookup"><span data-stu-id="bb32e-130">In any case, those errors should not affect the overall integrity of the database or affect whether playing the logs forward will succeed.</span></span>
  
<span data-ttu-id="bb32e-131">如果在需要**ErrCheckLogs**确定的最早日志之后创建的任何日志文件中都存在错误，则该函数将返回错误。</span><span class="sxs-lookup"><span data-stu-id="bb32e-131">If errors are found in any log file created after the earliest log that **ErrCheckLogs** determines is needed, the function returns an error.</span></span> <span data-ttu-id="bb32e-132">即使在生成的日志文件中发现的日志文件错误比将数据库更新为最新所需的日志文件中，也会返回该错误。</span><span class="sxs-lookup"><span data-stu-id="bb32e-132">The error will be returned even if the log file error was found in a log file that was generated later than what is needed to bring the database up to date.</span></span> <span data-ttu-id="bb32e-133">尽管可以使用已标识的日志文件将数据库置于干净关闭状态，但不会应用在以后损坏的日志文件中指定的事务，从而导致在还原数据库时丢失数据。</span><span class="sxs-lookup"><span data-stu-id="bb32e-133">Although it would be possible to bring the databases to a clean-shutdown state by using the identified log files, transactions specified in the later corrupted log files would not be applied, resulting in data loss when the database is restored.</span></span> 
  
<span data-ttu-id="bb32e-134">**CChkSGFiles**对象确定是否实际检查了使用**ErrInit**函数注册的所有日志文件。</span><span class="sxs-lookup"><span data-stu-id="bb32e-134">The **CChkSGFiles** object determines whether all of the log files registered with the **ErrInit** function were actually checked.</span></span> <span data-ttu-id="bb32e-135">如果未成功检查所有日志， **ErrTerm**函数将返回一个错误。</span><span class="sxs-lookup"><span data-stu-id="bb32e-135">If not all of the logs were not successfully checked, the **ErrTerm** function returns an error.</span></span> 
  
<span data-ttu-id="bb32e-136">如果您在多线程应用程序中使用 CHKSGFILES，则可以在应用程序的多线程部分调用**ErrCheckLogs**函数，但只能为每个**CCheckSGFiles**对象调用一次该函数。</span><span class="sxs-lookup"><span data-stu-id="bb32e-136">If you're using CHKSGFILES in a multithreaded application, you can call the **ErrCheckLogs** function in the multithreaded portion of the application, but you can call it only once for each **CCheckSGFiles** object.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="bb32e-137">Requirements</span><span class="sxs-lookup"><span data-stu-id="bb32e-137">Requirements</span></span>

<span data-ttu-id="bb32e-138">Exchange 2013 仅包含64位版本的 CHKSGFILES API。</span><span class="sxs-lookup"><span data-stu-id="bb32e-138">Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="bb32e-139">运行应用程序所使用的帐户必须具有对要检查的数据库和日志文件的读取访问权限。</span><span class="sxs-lookup"><span data-stu-id="bb32e-139">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

