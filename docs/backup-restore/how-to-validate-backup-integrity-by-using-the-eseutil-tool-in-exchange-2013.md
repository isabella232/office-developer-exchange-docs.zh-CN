---
title: 通过使用 Eseutil 工具在 Exchange 2013 中验证备份完整性
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b0d325ba-4482-4ca2-9a69-c890f985b206
description: 了解如何使用 Eseutil 命令行工具来验证 Exchange 存储的备份。
ms.openlocfilehash: 03c4c23d433418911240bbe7c337308a989f3739
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19752683"
---
#  <a name="validate-backup-integrity-by-using-the-eseutil-tool-in-exchange-2013"></a><span data-ttu-id="3eaf9-103">通过使用 Eseutil 工具在 Exchange 2013 中验证备份完整性</span><span class="sxs-lookup"><span data-stu-id="3eaf9-103">Validate backup integrity by using the Eseutil tool in Exchange 2013</span></span>

<span data-ttu-id="3eaf9-104">了解如何使用 Eseutil 命令行工具来验证 Exchange 存储的备份。</span><span class="sxs-lookup"><span data-stu-id="3eaf9-104">Find out how to use the Eseutil command-line tool to validate a backup of the Exchange store.</span></span> 
  
<span data-ttu-id="3eaf9-105">**适用于：** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="3eaf9-105">**Applies to:** Exchange Server 2013</span></span> 
  
<span data-ttu-id="3eaf9-106">卷影复制服务 (VSS) 可以创建备份 Exchange 继续写入数据库的同时，因为服务器不触摸所有页面，并执行所需的一致性检查。</span><span class="sxs-lookup"><span data-stu-id="3eaf9-106">Because the Volume Shadow Copy Service (VSS) can create backups while Exchange continues to write to the database, the server does not touch all the pages and perform the necessary consistency checks.</span></span> <span data-ttu-id="3eaf9-107">因此，使用 VSS 任何备份和还原应用程序必须验证快照的一致性。</span><span class="sxs-lookup"><span data-stu-id="3eaf9-107">For this reason, any backup and restore application that uses VSS must verify snapshot consistency.</span></span> <span data-ttu-id="3eaf9-108">Exchange Server 2013 快照一致性检查支持以下两种方法：</span><span class="sxs-lookup"><span data-stu-id="3eaf9-108">Exchange Server 2013 supports the following two methods for checking snapshot consistency:</span></span> 
  
- <span data-ttu-id="3eaf9-109">CHKSGFILES API</span><span class="sxs-lookup"><span data-stu-id="3eaf9-109">The CHKSGFILES API</span></span>
    
- <span data-ttu-id="3eaf9-110">Eseutil 命令行工具</span><span class="sxs-lookup"><span data-stu-id="3eaf9-110">The Eseutil command-line tool</span></span>
    
<span data-ttu-id="3eaf9-111">我们建议您使用 CHKSGFILES API，因为容易得多备份应用程序来检测、 诊断，并报告期间 CHKSGFILES 一致性找到的错误检查。</span><span class="sxs-lookup"><span data-stu-id="3eaf9-111">We recommend that you use the CHKSGFILES API because it is easier for the backup application to detect, diagnose, and report errors that are found during the CHKSGFILES consistency check.</span></span> <span data-ttu-id="3eaf9-112">有关如何使用 CHKSGFILES API 的信息，请参阅[使用 CHKSGFILES API 在 Exchange 2013 验证备份完整性](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="3eaf9-112">For information about how to use the CHKSGFILES API, see [Validate backup integrity by using the CHKSGFILES API in Exchange 2013](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md).</span></span>
  
## <a name="running-the-eseutil-tool"></a><span data-ttu-id="3eaf9-113">运行 Eseutil 工具</span><span class="sxs-lookup"><span data-stu-id="3eaf9-113">Running the Eseutil tool</span></span>

<span data-ttu-id="3eaf9-114">若要检查的快照一致性，请针对下表中标识的数据库和日志文件运行 eseutil 命令。</span><span class="sxs-lookup"><span data-stu-id="3eaf9-114">To check the snapshot consistency, run the eseutil command against the database and log files that are identified in the following table.</span></span> 
  
<span data-ttu-id="3eaf9-115">**表 1。每种备份类型的 Eseutil.exe 命令**</span><span class="sxs-lookup"><span data-stu-id="3eaf9-115">**Table 1. Eseutil.exe commands for each backup type**</span></span>

|<span data-ttu-id="3eaf9-116">**文件类型/备份类型**</span><span class="sxs-lookup"><span data-stu-id="3eaf9-116">**File type/backup type**</span></span>|<span data-ttu-id="3eaf9-117">**完整备份**</span><span class="sxs-lookup"><span data-stu-id="3eaf9-117">**Full backup**</span></span>|<span data-ttu-id="3eaf9-118">**副本备份**</span><span class="sxs-lookup"><span data-stu-id="3eaf9-118">**Copy backup**</span></span>|<span data-ttu-id="3eaf9-119">**增量备份**</span><span class="sxs-lookup"><span data-stu-id="3eaf9-119">**Incremental backup**</span></span>|<span data-ttu-id="3eaf9-120">**差异备份**</span><span class="sxs-lookup"><span data-stu-id="3eaf9-120">**Differential backup**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3eaf9-121">.edb</span><span class="sxs-lookup"><span data-stu-id="3eaf9-121">.edb</span></span>  <br/> |<span data-ttu-id="3eaf9-122">"eseutil /k /i"</span><span class="sxs-lookup"><span data-stu-id="3eaf9-122">"eseutil /k /i"</span></span>  <br/> |<span data-ttu-id="3eaf9-123">"eseutil /k /i"</span><span class="sxs-lookup"><span data-stu-id="3eaf9-123">"eseutil /k /i"</span></span>  <br/> |<span data-ttu-id="3eaf9-124">不适用</span><span class="sxs-lookup"><span data-stu-id="3eaf9-124">Not applicable</span></span>  <br/> |<span data-ttu-id="3eaf9-125">不适用</span><span class="sxs-lookup"><span data-stu-id="3eaf9-125">Not applicable</span></span>  <br/> |
|<span data-ttu-id="3eaf9-126">.log</span><span class="sxs-lookup"><span data-stu-id="3eaf9-126">.log</span></span>  <br/> |<span data-ttu-id="3eaf9-127">"eseutil /k"(1)</span><span class="sxs-lookup"><span data-stu-id="3eaf9-127">"eseutil /k" (1)</span></span>  <br/> |<span data-ttu-id="3eaf9-128">"eseutil /k"(1)</span><span class="sxs-lookup"><span data-stu-id="3eaf9-128">"eseutil /k" (1)</span></span>  <br/> |<span data-ttu-id="3eaf9-129">"eseutil /k"(2)</span><span class="sxs-lookup"><span data-stu-id="3eaf9-129">"eseutil /k" (2)</span></span>  <br/> |<span data-ttu-id="3eaf9-130">"eseutil /k"(2)</span><span class="sxs-lookup"><span data-stu-id="3eaf9-130">"eseutil /k" (2)</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="3eaf9-131">不需要对.stm 和.chk 文件运行 eseutil 命令。</span><span class="sxs-lookup"><span data-stu-id="3eaf9-131">You do not need to run the eseutil command against .stm and .chk files.</span></span> 
  
<span data-ttu-id="3eaf9-132">等于或大于检查点日志文件的号码所需才能恢复快照数据库的生成，所有具有数字的日志文件生成的日志文件。</span><span class="sxs-lookup"><span data-stu-id="3eaf9-132">All the log files that have a log file generation number that is equal to or greater than the generation number of the checkpoint log file are required in order to recover a snapshot database.</span></span> <span data-ttu-id="3eaf9-133">如果存在，也是必需的数据库恢复当前日志文件 (Enn.log)。</span><span class="sxs-lookup"><span data-stu-id="3eaf9-133">If it exists, the current log file (Enn.log) is also required for database recovery.</span></span> <span data-ttu-id="3eaf9-134">如果任何所需的日志文件的失败一致性检查，请求者必须确保调用[BackupComplete](http://msdn.microsoft.com/en-us/library/windows/desktop/aa382651%28v=vs.85%29.aspx)方法之前备份的组件的状态设置为 FALSE。</span><span class="sxs-lookup"><span data-stu-id="3eaf9-134">If any of the required log files fail the consistency check, the requester must make sure that the status of the backup component is set to FALSE before it calls the [BackupComplete](http://msdn.microsoft.com/en-us/library/windows/desktop/aa382651%28v=vs.85%29.aspx) method.</span></span> <span data-ttu-id="3eaf9-135">若要确定检查点日志文件，针对快照检查点文件运行 Eseutil.exe 和分析的输出"检查点:。"</span><span class="sxs-lookup"><span data-stu-id="3eaf9-135">To identify the checkpoint log file, run Eseutil.exe against the snapshot checkpoint file and parse the output for "Checkpoint:."</span></span> <span data-ttu-id="3eaf9-136">下面的示例演示如何对检查点文件运行 Eseutil.exe。</span><span class="sxs-lookup"><span data-stu-id="3eaf9-136">The following example shows how to run Eseutil.exe against a checkpoint file.</span></span> 
  
```cpp
c:\eseutil.exe /mk E01.chk
Checkpoint: (0x20, 9D, 187)
```

<span data-ttu-id="3eaf9-137">在示例中的第二行是返回的值，其中 0x20 是十六进制的日志生成编号的检查点日志文件。</span><span class="sxs-lookup"><span data-stu-id="3eaf9-137">The second line in the example is the return value, where 0x20 is the hexadecimal log generation number of the checkpoint log file.</span></span> <span data-ttu-id="3eaf9-138">本示例中，任何日志文件，包括 E01000020.log 和更高版本，必须无法损坏才能恢复的快照数据库，即使数据库本身已过物理一致性检查。</span><span class="sxs-lookup"><span data-stu-id="3eaf9-138">In this example, any log files, including E01000020.log and greater, must not be corrupt in order to recover the snapshot database, even if the database itself has already passed the physical consistency check.</span></span>
  
<span data-ttu-id="3eaf9-139">在增量备份或差异备份集中的所有日志文件都所需的数据库恢复。</span><span class="sxs-lookup"><span data-stu-id="3eaf9-139">All log files in an incremental or differential backup set are required for database recovery.</span></span> <span data-ttu-id="3eaf9-140">您可以通过对日志文件前缀运行 Eseutil.exe 检查日志序列的一致性。</span><span class="sxs-lookup"><span data-stu-id="3eaf9-140">You can check the consistency of a log sequence by running Eseutil.exe against the log file prefix.</span></span> <span data-ttu-id="3eaf9-141">下面的示例演示如何在给定路径上针对所有文件的窗体 E01xxxxx.log 运行一致性检查。</span><span class="sxs-lookup"><span data-stu-id="3eaf9-141">The following example shows how to run consistency checks against all the files of the form E01xxxxx.log on a given path.</span></span>
  
```cpp
c:\eseutil /k E01
```

## <a name="checking-the-eseutilexe-output"></a><span data-ttu-id="3eaf9-142">检查 Eseutil.exe 输出</span><span class="sxs-lookup"><span data-stu-id="3eaf9-142">Checking the Eseutil.exe output</span></span>

<span data-ttu-id="3eaf9-143">请求者必须验证负退出错误级别错误的所有值返回。</span><span class="sxs-lookup"><span data-stu-id="3eaf9-143">The requester must verify that all the exit ERRORLEVEL error values that are returned are nonnegative.</span></span> <span data-ttu-id="3eaf9-144">有关错误级别值的信息，请参阅[参考 Eseutil 的常见错误](http://technet.microsoft.com/en-us/library/aa996759%28v=exchg.80%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="3eaf9-144">For information about ERRORLEVEL values, see [Reference for Common Eseutil Errors](http://technet.microsoft.com/en-us/library/aa996759%28v=exchg.80%29.aspx).</span></span> <span data-ttu-id="3eaf9-145">若要查看在命令行错误级别，请键入"回显 %错误级别 %"Eseutil.exe 完成运行后。</span><span class="sxs-lookup"><span data-stu-id="3eaf9-145">To see the ERRORLEVEL at the command line, type "echo %errorlevel%" after Eseutil.exe finishes running.</span></span> <span data-ttu-id="3eaf9-146">负错误级别指示一个或多个文件已损坏。</span><span class="sxs-lookup"><span data-stu-id="3eaf9-146">A negative ERRORLEVEL indicates that one or more files is corrupted.</span></span>
  
<span data-ttu-id="3eaf9-147">请求者调用**BackupComplete**方法之前，则必须确保备份的组件的状态反映一致性检查的结果。</span><span class="sxs-lookup"><span data-stu-id="3eaf9-147">Before the requester calls the **BackupComplete** method, it must make sure that the status of the backup component reflects the result of the consistency check.</span></span> <span data-ttu-id="3eaf9-148">如果发现任何损坏，状态将为 FALSE;如果找到没有损坏，状态将设为 TRUE。</span><span class="sxs-lookup"><span data-stu-id="3eaf9-148">If any corruption was found, the status will be FALSE; if no corruption was found, the status will be TRUE.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3eaf9-149">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3eaf9-149">See also</span></span>

- [<span data-ttu-id="3eaf9-150">使用 CHKSGFILES API 在 Exchange 2013 中验证备份完整性</span><span class="sxs-lookup"><span data-stu-id="3eaf9-150">Validate backup integrity by using the CHKSGFILES API in Exchange 2013</span></span>](how-to-validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange.md)
- [<span data-ttu-id="3eaf9-151">构建备份和还原 Exchange 2013 的应用程序</span><span class="sxs-lookup"><span data-stu-id="3eaf9-151">Build backup and restore applications for Exchange 2013</span></span>](build-backup-and-restore-applications-for-exchange-2013.md)
- [<span data-ttu-id="3eaf9-152">CChkSGFiles 类参考 （英文）</span><span class="sxs-lookup"><span data-stu-id="3eaf9-152">CChkSGFiles class reference</span></span>](cchksgfiles-class-reference.md)
- [<span data-ttu-id="3eaf9-153">Exchange 2013 的备份和还原概念</span><span class="sxs-lookup"><span data-stu-id="3eaf9-153">Backup and restore concepts for Exchange 2013</span></span>](backup-and-restore-concepts-for-exchange-2013.md)
    

