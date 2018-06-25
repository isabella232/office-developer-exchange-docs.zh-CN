---
title: CChkSGFiles.ErrCheckLogs 函数
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
description: 上次修改时间： 2013 年 2 月 22 日
ms.openlocfilehash: 5b1070de73bc23ae09ddb7835bd72c8e8a71a95f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752690"
---
# <a name="cchksgfileserrchecklogs-function"></a><span data-ttu-id="cd157-103">CChkSGFiles.ErrCheckLogs 函数</span><span class="sxs-lookup"><span data-stu-id="cd157-103">CChkSGFiles.ErrCheckLogs function</span></span>

<span data-ttu-id="cd157-104">**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="cd157-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="cd157-105">验证已**ErrInit**函数中指定的所有数据库文件的日志文件。</span><span class="sxs-lookup"><span data-stu-id="cd157-105">Validates the log files of all the database files that were specified in the **ErrInit** function.</span></span> <span data-ttu-id="cd157-106">验证的日志那些在位于路径，并具有三个字母基本日志文件名称传递给**ErrInit**。</span><span class="sxs-lookup"><span data-stu-id="cd157-106">The validated logs are those that exist in the path, and that have the three-letter base log file name passed to **ErrInit**.</span></span>
  
```cs
Vitual ERRErrCheckLogs 
(
        BOOL  * const pfOnlyUnnecessaryLogsCorrup,
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a><span data-ttu-id="cd157-107">参数</span><span class="sxs-lookup"><span data-stu-id="cd157-107">Parameters</span></span>

### <a name="pfonlyunnecessarylogscorrupt"></a><span data-ttu-id="cd157-108">pfOnlyUnnecessaryLogsCorrupt</span><span class="sxs-lookup"><span data-stu-id="cd157-108">pfOnlyUnnecessaryLogsCorrupt</span></span> 
  
<span data-ttu-id="cd157-109">输出参数。</span><span class="sxs-lookup"><span data-stu-id="cd157-109">Output parameter.</span></span> <span data-ttu-id="cd157-110">**True**，此参数指示发现事务日志文件，但这些错误错误时已所有到，则不需要的日志文件中找到将数据库置于干净关闭状态丢失数据。</span><span class="sxs-lookup"><span data-stu-id="cd157-110">When **true**, this parameter indicates that errors were found in the transaction log files, but those errors were all found in log files that are not needed to bring the database to a clean-shutdown state without data loss.</span></span> <span data-ttu-id="cd157-111">仅当**ErrCheckLogs**返回**errSuccess**时，此参数中返回一个**true**值是有效。</span><span class="sxs-lookup"><span data-stu-id="cd157-111">A **true** value returned in this parameter is valid only when **ErrCheckLogs** returns **errSuccess**.</span></span> 
    
### <a name="ulflags"></a><span data-ttu-id="cd157-112">ulFlags</span><span class="sxs-lookup"><span data-stu-id="cd157-112">ulFlags</span></span>
  
<span data-ttu-id="cd157-113">可选的输入的参数。</span><span class="sxs-lookup"><span data-stu-id="cd157-113">Optional input parameter.</span></span> <span data-ttu-id="cd157-114">此值保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="cd157-114">This value is reserved for future use.</span></span> <span data-ttu-id="cd157-115">通过此参数传递的值应为 0 （零）。</span><span class="sxs-lookup"><span data-stu-id="cd157-115">The value passed by this parameter should be 0 (zero).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cd157-116">返回值</span><span class="sxs-lookup"><span data-stu-id="cd157-116">Return value</span></span>

<span data-ttu-id="cd157-117">从[ERR](cchksgfiles-err-enumeration.md)枚举错误代码。</span><span class="sxs-lookup"><span data-stu-id="cd157-117">An error code from the [ERR](cchksgfiles-err-enumeration.md) enumeration.</span></span> 
  
<span data-ttu-id="cd157-118">务必要记住甚至在日志文件中找到错误时，此函数可以返回**errSuccess** 。</span><span class="sxs-lookup"><span data-stu-id="cd157-118">It's important to remember that this function can return **errSuccess** even when errors are found in the log files.</span></span> <span data-ttu-id="cd157-119">因此，当**ErrCheckLogs**返回**errSuccess**，应用程序还应检查**pfOnlyUnnecessaryLogsCorrupt**返回参数。</span><span class="sxs-lookup"><span data-stu-id="cd157-119">Therefore, when **ErrCheckLogs** returns **errSuccess**, the application should also check the  **pfOnlyUnnecessaryLogsCorrupt** return parameter.</span></span> <span data-ttu-id="cd157-120">如果**ErrCheckLogs**返回**errSuccess**时， **pfOnlyUnnecessaryLogsCorrupts**为**true** ，则表示的发现一个或多个错误，但仅在不需要以显示最新的数据库的日志文件。</span><span class="sxs-lookup"><span data-stu-id="cd157-120">If **pfOnlyUnnecessaryLogsCorrupts** is **true** when **ErrCheckLogs** returns **errSuccess**, this indicates that one or more errors were found, but only in log files not needed to bring the database up-to-date.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cd157-121">注解</span><span class="sxs-lookup"><span data-stu-id="cd157-121">Remarks</span></span>

<span data-ttu-id="cd157-122">可以调用**ErrCheckLogs**函数之前，必须调用**ErrCheckDbHeaders**函数。</span><span class="sxs-lookup"><span data-stu-id="cd157-122">The **ErrCheckDbHeaders** function must be called before the **ErrCheckLogs** function can be called.</span></span> 
  
<span data-ttu-id="cd157-123">当正在检查 Exchange 数据库事务日志文件时，日志文件的一些将需要存储组中将数据库置于干净关闭状态，而不会数据丢失，而可能不需要其他日志文件。</span><span class="sxs-lookup"><span data-stu-id="cd157-123">When Exchange database transaction log files are being checked, some of the log files will be necessary to bring the databases in the storage group to a clean-shutdown state without data loss, whereas other log files might not be needed.</span></span> <span data-ttu-id="cd157-124">**ErrCheckLogs**函数确定最早和最新日志文件所需以显示最新的数据库。</span><span class="sxs-lookup"><span data-stu-id="cd157-124">The **ErrCheckLogs** function determines both the oldest and the newest log files that are needed to bring the databases up to date.</span></span> 
  
<span data-ttu-id="cd157-125">**ErrCheckLogs**函数验证传递给**ErrInit**函数还可以指定三个字母的基文件名指定路径中的所有日志文件。</span><span class="sxs-lookup"><span data-stu-id="cd157-125">The **ErrCheckLogs** function verifies all the log files in the specified paths that also have the specified three-letter base file name, as passed to the **ErrInit** function.</span></span> 
  
<span data-ttu-id="cd157-126">如果在日志文件中没有发现任何错误， **ErrCheckLogs**返回**errSuccess**。</span><span class="sxs-lookup"><span data-stu-id="cd157-126">If no errors are found in the log files, **ErrCheckLogs** returns **errSuccess**.</span></span> 
  
<span data-ttu-id="cd157-127">如果找到任何所需的日志文件可能已损坏， **ErrCheckLogs**将返回错误。</span><span class="sxs-lookup"><span data-stu-id="cd157-127">If any of the required log files are found to be corrupted, **ErrCheckLogs** returns an error.</span></span> 
  
<span data-ttu-id="cd157-128">如果仅在早于所需的最早那些的日志文件中没有发现错误，该函数将返回**errSuccess** ，并将返回参数**pfOnlyUnnecessaryLogCorrupt**设置为**true**。</span><span class="sxs-lookup"><span data-stu-id="cd157-128">If errors are found only in log files that are older than the earliest ones needed, the function returns **errSuccess** and sets the return parameter **pfOnlyUnnecessaryLogCorrupt** to **true**.</span></span> <span data-ttu-id="cd157-129">应用程序应认识到，没有错误某些这些旧的日志文件，如果跟随，则它可能将通知用户。</span><span class="sxs-lookup"><span data-stu-id="cd157-129">The application should recognize that there are errors in some of those old log files, and if so, it will possibly alert the user.</span></span> <span data-ttu-id="cd157-130">在任何情况下，这些错误应该不会影响数据库的总体完整性，或影响是否播放日志向前将成功。</span><span class="sxs-lookup"><span data-stu-id="cd157-130">In any case, those errors should not affect the overall integrity of the database or affect whether playing the logs forward will succeed.</span></span>
  
<span data-ttu-id="cd157-131">如果没有发现任何后的最早创建的日志文件中的错误日志**ErrCheckLogs**确定所需、 函数将返回错误。</span><span class="sxs-lookup"><span data-stu-id="cd157-131">If errors are found in any log file created after the earliest log that **ErrCheckLogs** determines is needed, the function returns an error.</span></span> <span data-ttu-id="cd157-132">偶数晚于什么生成的日志文件中找到的日志文件错误如果是，以使最新的数据库，将返回错误。</span><span class="sxs-lookup"><span data-stu-id="cd157-132">The error will be returned even if the log file error was found in a log file that was generated later than what is needed to bring the database up to date.</span></span> <span data-ttu-id="cd157-133">尽管就可以通过使用标识的日志文件将数据库置于干净关闭状态，更高版本损坏的日志文件中指定的事务将不会应用，从而导致数据丢失时还原数据库。</span><span class="sxs-lookup"><span data-stu-id="cd157-133">Although it would be possible to bring the databases to a clean-shutdown state by using the identified log files, transactions specified in the later corrupted log files would not be applied, resulting in data loss when the database is restored.</span></span> 
  
<span data-ttu-id="cd157-134">**CChkSGFiles**对象确定是否实际检查了所有与**ErrInit**函数注册的日志文件。</span><span class="sxs-lookup"><span data-stu-id="cd157-134">The **CChkSGFiles** object determines whether all of the log files registered with the **ErrInit** function were actually checked.</span></span> <span data-ttu-id="cd157-135">如果不是所有日志未成功签， **ErrTerm**函数将返回错误。</span><span class="sxs-lookup"><span data-stu-id="cd157-135">If not all of the logs were not successfully checked, the **ErrTerm** function returns an error.</span></span> 
  
<span data-ttu-id="cd157-136">如果您使用 CHKSGFILES 多线程应用程序中，您可以将应用程序的多线程部分中调用**ErrCheckLogs**函数，但您可以为每个**CCheckSGFiles**对象调用它仅执行一次。</span><span class="sxs-lookup"><span data-stu-id="cd157-136">If you're using CHKSGFILES in a multithreaded application, you can call the **ErrCheckLogs** function in the multithreaded portion of the application, but you can call it only once for each **CCheckSGFiles** object.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="cd157-137">要求</span><span class="sxs-lookup"><span data-stu-id="cd157-137">Requirements</span></span>

<span data-ttu-id="cd157-138">Exchange 2013 只包括 CHKSGFILES API 的 64 位版本。</span><span class="sxs-lookup"><span data-stu-id="cd157-138">Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="cd157-139">下运行该应用程序的帐户必须具有对要检查的数据库和日志文件的读取访问权限。</span><span class="sxs-lookup"><span data-stu-id="cd157-139">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

