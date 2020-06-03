---
title: 使用 Exchange 2013 中的 Eseutil 工具验证备份完整性
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b0d325ba-4482-4ca2-9a69-c890f985b206
description: 了解如何使用 Eseutil 命令行工具验证 Exchange 存储的备份。
ms.openlocfilehash: e8f1a46e2d94729ae5586861317312e277216d63
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44452795"
---
#  <a name="validate-backup-integrity-by-using-the-eseutil-tool-in-exchange-2013"></a><span data-ttu-id="64423-103">使用 Exchange 2013 中的 Eseutil 工具验证备份完整性</span><span class="sxs-lookup"><span data-stu-id="64423-103">Validate backup integrity by using the Eseutil tool in Exchange 2013</span></span>

<span data-ttu-id="64423-104">了解如何使用 Eseutil 命令行工具验证 Exchange 存储的备份。</span><span class="sxs-lookup"><span data-stu-id="64423-104">Find out how to use the Eseutil command-line tool to validate a backup of the Exchange store.</span></span> 
  
<span data-ttu-id="64423-105">**适用于：** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="64423-105">**Applies to:** Exchange Server 2013</span></span> 
  
<span data-ttu-id="64423-106">由于卷影复制服务（VSS）可以在 Exchange 继续写入数据库时创建备份，因此服务器不会接触所有页面并执行必要的一致性检查。</span><span class="sxs-lookup"><span data-stu-id="64423-106">Because the Volume Shadow Copy Service (VSS) can create backups while Exchange continues to write to the database, the server does not touch all the pages and perform the necessary consistency checks.</span></span> <span data-ttu-id="64423-107">因此，使用 VSS 的任何备份和还原应用程序都必须验证快照一致性。</span><span class="sxs-lookup"><span data-stu-id="64423-107">For this reason, any backup and restore application that uses VSS must verify snapshot consistency.</span></span> <span data-ttu-id="64423-108">Exchange Server 2013 支持以下两种检查快照一致性的方法：</span><span class="sxs-lookup"><span data-stu-id="64423-108">Exchange Server 2013 supports the following two methods for checking snapshot consistency:</span></span> 
  
- <span data-ttu-id="64423-109">CHKSGFILES API</span><span class="sxs-lookup"><span data-stu-id="64423-109">The CHKSGFILES API</span></span>
    
- <span data-ttu-id="64423-110">Eseutil 命令行工具</span><span class="sxs-lookup"><span data-stu-id="64423-110">The Eseutil command-line tool</span></span>
    
<span data-ttu-id="64423-111">建议使用 CHKSGFILES API，因为备份应用程序可以更轻松地检测、诊断和报告 CHKSGFILES 一致性检查过程中发现的错误。</span><span class="sxs-lookup"><span data-stu-id="64423-111">We recommend that you use the CHKSGFILES API because it is easier for the backup application to detect, diagnose, and report errors that are found during the CHKSGFILES consistency check.</span></span> <span data-ttu-id="64423-112">有关如何使用 CHKSGFILES API 的信息，请参阅[使用 Exchange 2013 中的 CHKSGFILES API 验证备份完整性](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="64423-112">For information about how to use the CHKSGFILES API, see [Validate backup integrity by using the CHKSGFILES API in Exchange 2013](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md).</span></span>
  
## <a name="running-the-eseutil-tool"></a><span data-ttu-id="64423-113">运行 Eseutil 工具</span><span class="sxs-lookup"><span data-stu-id="64423-113">Running the Eseutil tool</span></span>

<span data-ttu-id="64423-114">若要检查快照一致性，请对下表中标识的数据库和日志文件运行 eseutil 命令。</span><span class="sxs-lookup"><span data-stu-id="64423-114">To check the snapshot consistency, run the eseutil command against the database and log files that are identified in the following table.</span></span> 
  
<span data-ttu-id="64423-115">**表1。每种备份类型的 Eseutil 命令**</span><span class="sxs-lookup"><span data-stu-id="64423-115">**Table 1. Eseutil.exe commands for each backup type**</span></span>

|<span data-ttu-id="64423-116">**文件类型/备份类型**</span><span class="sxs-lookup"><span data-stu-id="64423-116">**File type/backup type**</span></span>|<span data-ttu-id="64423-117">**完整备份**</span><span class="sxs-lookup"><span data-stu-id="64423-117">**Full backup**</span></span>|<span data-ttu-id="64423-118">**副本备份**</span><span class="sxs-lookup"><span data-stu-id="64423-118">**Copy backup**</span></span>|<span data-ttu-id="64423-119">**增量备份**</span><span class="sxs-lookup"><span data-stu-id="64423-119">**Incremental backup**</span></span>|<span data-ttu-id="64423-120">**差异备份**</span><span class="sxs-lookup"><span data-stu-id="64423-120">**Differential backup**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="64423-121">.edb</span><span class="sxs-lookup"><span data-stu-id="64423-121">.edb</span></span>  <br/> |<span data-ttu-id="64423-122">"eseutil/k/i"</span><span class="sxs-lookup"><span data-stu-id="64423-122">"eseutil /k /i"</span></span>  <br/> |<span data-ttu-id="64423-123">"eseutil/k/i"</span><span class="sxs-lookup"><span data-stu-id="64423-123">"eseutil /k /i"</span></span>  <br/> |<span data-ttu-id="64423-124">不适用</span><span class="sxs-lookup"><span data-stu-id="64423-124">Not applicable</span></span>  <br/> |<span data-ttu-id="64423-125">不适用</span><span class="sxs-lookup"><span data-stu-id="64423-125">Not applicable</span></span>  <br/> |
|<span data-ttu-id="64423-126">.log</span><span class="sxs-lookup"><span data-stu-id="64423-126">.log</span></span>  <br/> |<span data-ttu-id="64423-127">"eseutil/k" （1）</span><span class="sxs-lookup"><span data-stu-id="64423-127">"eseutil /k" (1)</span></span>  <br/> |<span data-ttu-id="64423-128">"eseutil/k" （1）</span><span class="sxs-lookup"><span data-stu-id="64423-128">"eseutil /k" (1)</span></span>  <br/> |<span data-ttu-id="64423-129">"eseutil/k" （2）</span><span class="sxs-lookup"><span data-stu-id="64423-129">"eseutil /k" (2)</span></span>  <br/> |<span data-ttu-id="64423-130">"eseutil/k" （2）</span><span class="sxs-lookup"><span data-stu-id="64423-130">"eseutil /k" (2)</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="64423-131">您无需对 .stm 和 .chk 文件运行 eseutil 命令。</span><span class="sxs-lookup"><span data-stu-id="64423-131">You do not need to run the eseutil command against .stm and .chk files.</span></span> 
  
<span data-ttu-id="64423-132">必须有日志文件生成号等于或大于检查点日志文件世代号的所有日志文件，才能恢复快照数据库。</span><span class="sxs-lookup"><span data-stu-id="64423-132">All the log files that have a log file generation number that is equal to or greater than the generation number of the checkpoint log file are required in order to recover a snapshot database.</span></span> <span data-ttu-id="64423-133">如果存在，则数据库恢复也需要当前日志文件（Enn）。</span><span class="sxs-lookup"><span data-stu-id="64423-133">If it exists, the current log file (Enn.log) is also required for database recovery.</span></span> <span data-ttu-id="64423-134">如果任何必需的日志文件未通过一致性检查，请求者必须确保在调用[BackupComplete](https://msdn.microsoft.com/library/windows/desktop/aa382651%28v=vs.85%29.aspx)方法之前将备份组件的状态设置为 FALSE。</span><span class="sxs-lookup"><span data-stu-id="64423-134">If any of the required log files fail the consistency check, the requester must make sure that the status of the backup component is set to FALSE before it calls the [BackupComplete](https://msdn.microsoft.com/library/windows/desktop/aa382651%28v=vs.85%29.aspx) method.</span></span> <span data-ttu-id="64423-135">若要确定检查点日志文件，请针对快照检查点文件运行 Eseutil，并分析 "检查点：" 的输出。</span><span class="sxs-lookup"><span data-stu-id="64423-135">To identify the checkpoint log file, run Eseutil.exe against the snapshot checkpoint file and parse the output for "Checkpoint:."</span></span> <span data-ttu-id="64423-136">下面的示例演示如何对检查点文件运行 Eseutil。</span><span class="sxs-lookup"><span data-stu-id="64423-136">The following example shows how to run Eseutil.exe against a checkpoint file.</span></span> 
  
```cpp
c:\eseutil.exe /mk E01.chk
Checkpoint: (0x20, 9D, 187)
```

<span data-ttu-id="64423-137">该示例中的第二行是返回值，其中0x20 是检查点日志文件的十六进制日志生成编号。</span><span class="sxs-lookup"><span data-stu-id="64423-137">The second line in the example is the return value, where 0x20 is the hexadecimal log generation number of the checkpoint log file.</span></span> <span data-ttu-id="64423-138">在此示例中，任何日志文件（包括 E01000020 和更高版本）都必须损坏才能恢复快照数据库，即使数据库本身已经通过了物理一致性检查也是如此。</span><span class="sxs-lookup"><span data-stu-id="64423-138">In this example, any log files, including E01000020.log and greater, must not be corrupt in order to recover the snapshot database, even if the database itself has already passed the physical consistency check.</span></span>
  
<span data-ttu-id="64423-139">数据库恢复需要增量备份或差异备份集中的所有日志文件。</span><span class="sxs-lookup"><span data-stu-id="64423-139">All log files in an incremental or differential backup set are required for database recovery.</span></span> <span data-ttu-id="64423-140">您可以通过对日志文件前缀运行 Eseutil 来检查日志序列的一致性。</span><span class="sxs-lookup"><span data-stu-id="64423-140">You can check the consistency of a log sequence by running Eseutil.exe against the log file prefix.</span></span> <span data-ttu-id="64423-141">下面的示例演示如何对给定路径上 E01xxxxx 形式的所有文件运行一致性检查。</span><span class="sxs-lookup"><span data-stu-id="64423-141">The following example shows how to run consistency checks against all the files of the form E01xxxxx.log on a given path.</span></span>
  
```cpp
c:\eseutil /k E01
```

## <a name="checking-the-eseutilexe-output"></a><span data-ttu-id="64423-142">检查 Eseutil.exe 输出</span><span class="sxs-lookup"><span data-stu-id="64423-142">Checking the Eseutil.exe output</span></span>

<span data-ttu-id="64423-143">请求者必须验证返回的所有退出 ERRORLEVEL 错误值是否为非负。</span><span class="sxs-lookup"><span data-stu-id="64423-143">The requester must verify that all the exit ERRORLEVEL error values that are returned are nonnegative.</span></span> <span data-ttu-id="64423-144">有关 ERRORLEVEL 值的信息，请参阅[常见 Eseutil 错误的参考](https://technet.microsoft.com/library/aa996759%28v=exchg.80%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="64423-144">For information about ERRORLEVEL values, see [Reference for Common Eseutil Errors](https://technet.microsoft.com/library/aa996759%28v=exchg.80%29.aspx).</span></span> <span data-ttu-id="64423-145">若要在命令行中查看 ERRORLEVEL，请在运行 Eseutil 后键入 "echo% ERRORLEVEL%"。</span><span class="sxs-lookup"><span data-stu-id="64423-145">To see the ERRORLEVEL at the command line, type "echo %errorlevel%" after Eseutil.exe finishes running.</span></span> <span data-ttu-id="64423-146">负 ERRORLEVEL 表示一个或多个文件已损坏。</span><span class="sxs-lookup"><span data-stu-id="64423-146">A negative ERRORLEVEL indicates that one or more files is corrupted.</span></span>
  
<span data-ttu-id="64423-147">在请求者调用**BackupComplete**方法之前，必须确保备份组件的状态反映了一致性检查的结果。</span><span class="sxs-lookup"><span data-stu-id="64423-147">Before the requester calls the **BackupComplete** method, it must make sure that the status of the backup component reflects the result of the consistency check.</span></span> <span data-ttu-id="64423-148">如果发现任何损坏，则状态将为 FALSE;如果未发现损坏，状态将为 TRUE。</span><span class="sxs-lookup"><span data-stu-id="64423-148">If any corruption was found, the status will be FALSE; if no corruption was found, the status will be TRUE.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="64423-149">另请参阅</span><span class="sxs-lookup"><span data-stu-id="64423-149">See also</span></span>

- [<span data-ttu-id="64423-150">使用 Exchange 2013 中的 CHKSGFILES API 验证备份完整性</span><span class="sxs-lookup"><span data-stu-id="64423-150">Validate backup integrity by using the CHKSGFILES API in Exchange 2013</span></span>](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md)
- [<span data-ttu-id="64423-151">为 Exchange 2013 生成备份和还原应用程序</span><span class="sxs-lookup"><span data-stu-id="64423-151">Build backup and restore applications for Exchange 2013</span></span>](build-backup-and-restore-applications-for-exchange-2013.md)
- [<span data-ttu-id="64423-152">CChkSGFiles 类参考</span><span class="sxs-lookup"><span data-stu-id="64423-152">CChkSGFiles class reference</span></span>](cchksgfiles-class-reference.md)
- [<span data-ttu-id="64423-153">Exchange 2013 的备份和还原概念</span><span class="sxs-lookup"><span data-stu-id="64423-153">Backup and restore concepts for Exchange 2013</span></span>](backup-and-restore-concepts-for-exchange-2013.md)
    

