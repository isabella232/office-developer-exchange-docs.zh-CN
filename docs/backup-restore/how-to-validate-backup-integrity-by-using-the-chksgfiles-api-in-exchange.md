---
title: 使用 CHKSGFILES API 在 Exchange 2013 中验证备份完整性
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 607cbeb9-0a02-4079-8a4d-34bdeb560224
description: 了解如何使用 CHKSGFILES API 在 Exchange 2013 验证 Exchange 存储的备份。
ms.openlocfilehash: 968484cd5bb7439730685643683e1d850bec33ca
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19752691"
---
# <a name="validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange-2013"></a><span data-ttu-id="5718a-103">使用 CHKSGFILES API 在 Exchange 2013 中验证备份完整性</span><span class="sxs-lookup"><span data-stu-id="5718a-103">Validate backup integrity by using the CHKSGFILES API in Exchange 2013</span></span>

<span data-ttu-id="5718a-104">了解如何使用 CHKSGFILES API 在 Exchange 2013 验证 Exchange 存储的备份。</span><span class="sxs-lookup"><span data-stu-id="5718a-104">Find out how to use the CHKSGFILES API to validate a backup of the Exchange store in Exchange 2013.</span></span>
  
<span data-ttu-id="5718a-105">**适用于：** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="5718a-105">**Applies to:** Exchange Server 2013</span></span> 
  
<span data-ttu-id="5718a-106">备份操作期间托管的卷影复制服务 (VSS)，Exchange Server 2013 无法读取完整地复制每个数据库文件，并验证其校验和完整性。</span><span class="sxs-lookup"><span data-stu-id="5718a-106">During backup operations managed by the Volume Shadow Copy Service (VSS), Exchange Server 2013 cannot read each database file in its entirety and verify its checksum integrity.</span></span> <span data-ttu-id="5718a-107">因此，您可能希望您备份的应用程序，以验证数据库和事务日志文件的完整性。</span><span class="sxs-lookup"><span data-stu-id="5718a-107">Therefore, you might want your backup application to verify database and transaction log file integrity.</span></span> <span data-ttu-id="5718a-108">我们建议您备份应用程序验证之前告知 Exchange 书写器完成备份后的卷影副本集的物理一致性。</span><span class="sxs-lookup"><span data-stu-id="5718a-108">We recommend that your backup application verify the physical consistency of the shadow copy set prior to informing the Exchange writer that the backup is complete.</span></span> <span data-ttu-id="5718a-109">成功备份后，Exchange 存储更新的备份的数据库以反映上次成功备份时间，并从服务器删除事务日志不再需要滚从最后一次成功备份的标题。</span><span class="sxs-lookup"><span data-stu-id="5718a-109">After a successful backup, the Exchange store updates the headers of the backed-up databases to reflect the last successful backup times and removes transaction logs from the server that are no longer required to roll forward from the last successful backup.</span></span>
  
## <a name="prerequisites-for-validating-backup-integrity"></a><span data-ttu-id="5718a-110">验证备份完整性的先决条件</span><span class="sxs-lookup"><span data-stu-id="5718a-110">Prerequisites for validating backup integrity</span></span>

<span data-ttu-id="5718a-111">您的应用程序可以验证备份的完整性之前，您必须具有访问以下：</span><span class="sxs-lookup"><span data-stu-id="5718a-111">Before your application can validate the integrity of your backup, you must have access to the following:</span></span>
  
- <span data-ttu-id="5718a-112">从 Exchange 存储备份文件。</span><span class="sxs-lookup"><span data-stu-id="5718a-112">Files from your Exchange store backup.</span></span>
- <span data-ttu-id="5718a-113">开始使用 Visual Studio 2010 的 Visual Studio 的版本。</span><span class="sxs-lookup"><span data-stu-id="5718a-113">A version of Visual Studio starting with Visual Studio 2010.</span></span>
- <span data-ttu-id="5718a-114">CHKSGFILES 库和头文件。</span><span class="sxs-lookup"><span data-stu-id="5718a-114">The CHKSGFILES library and header files.</span></span> <span data-ttu-id="5718a-115">您可以从[Microsoft 下载中心](http://www.microsoft.com/en-us/download/details.aspx?id=36802)下载库和头文件。</span><span class="sxs-lookup"><span data-stu-id="5718a-115">You can download the library and header files from the [Microsoft Download Center](http://www.microsoft.com/en-us/download/details.aspx?id=36802).</span></span>
    
## <a name="validate-backup-integrity"></a><span data-ttu-id="5718a-116">验证备份完整性</span><span class="sxs-lookup"><span data-stu-id="5718a-116">Validate backup integrity</span></span>

<span data-ttu-id="5718a-117">以下过程介绍如何验证数据完整性中备份和还原应用程序。</span><span class="sxs-lookup"><span data-stu-id="5718a-117">The following procedure describes how to validate data integrity in your backup and restore application.</span></span>
  
### <a name="to-validate-backup-integrity"></a><span data-ttu-id="5718a-118">验证备份完整性</span><span class="sxs-lookup"><span data-stu-id="5718a-118">To validate backup integrity</span></span>

1. <span data-ttu-id="5718a-119">创建**CChkSGFiles**类的新实例。</span><span class="sxs-lookup"><span data-stu-id="5718a-119">Create a new instance of the **CChkSGFiles** class.</span></span> 
   
   ```cpp
   CCheckSGFiles::ERRerr = CCheckSGFiles::errSuccess;
   ULONGiDbError = (ULONG)CCheckSGFiles::iDbInvalid;
   CCheckSGFiles * const pcchecksgfiles = CCheckSGFiles::New();
   if ( NULL == pcchecksgfiles )
   {
     err = CCheckSGFiles::errOutOfMemory;
     printf( "ERROR: Could not allocate CCheckSGFiles object.\n" );
     goto HandleError;
   }
   ```

   <span data-ttu-id="5718a-120">第一个代码行创建 error 对象并将其初始值设置为成功，创建一个对象，检查数据库的有效性。</span><span class="sxs-lookup"><span data-stu-id="5718a-120">The first lines of code create an error object and set its initial value to success, and create an object that checks the validity of the database.</span></span> <span data-ttu-id="5718a-121">然后， [CChkSGFiles.New 函数](cchksgfiles-new-function.md)创建**CChkSGFiles**类的新实例。</span><span class="sxs-lookup"><span data-stu-id="5718a-121">Then, the [CChkSGFiles.New function](cchksgfiles-new-function.md) creates a new instance of the **CChkSGFiles** class.</span></span> <span data-ttu-id="5718a-122">快速检查新对象的指示的任何问题出现时创建的新实例。</span><span class="sxs-lookup"><span data-stu-id="5718a-122">A quick check of the new object indicates whether any issues occurred when the new instance was created.</span></span> 
    
2. <span data-ttu-id="5718a-123">初始化**CChkSGFiles**对象。</span><span class="sxs-lookup"><span data-stu-id="5718a-123">Initialize the **CChkSGFiles** object.</span></span> 
   
   ```cpp
   Call( pcchecksgfiles->ErrInit(
   rgwszDb,
   cDb,
   wszLogPath,
   wszBaseName ) );
   ```
   
   <span data-ttu-id="5718a-124">有关参数的详细信息，请参阅[CChkSGFiles.ErrInit 函数](cchksgfiles-errinit-function.md)。</span><span class="sxs-lookup"><span data-stu-id="5718a-124">For more information about the parameters, see [CChkSGFiles.ErrInit function](cchksgfiles-errinit-function.md).</span></span>
   
3. <span data-ttu-id="5718a-125">使用[CChkSGFiles.ErrCheckDbHeaders 函数](cchksgfiles-errcheckdbheaders-function.md)通过检查数据库标头中验证数据库的完整性。</span><span class="sxs-lookup"><span data-stu-id="5718a-125">Use the [CChkSGFiles.ErrCheckDbHeaders function](cchksgfiles-errcheckdbheaders-function.md) to validate database integrity by checking the database headers.</span></span>
   
   ```cpp
   err = pcchecksgfiles->ErrCheckDbHeaders(
   &amp;cbDbPageSize,
   &amp;cDbHeaderPages,
   &amp;iDbError );
   if ( CCheckSGFiles::errSuccess != err )
   {
   if ( CCheckSGFiles::iDbInvalid != iDbError )
   {
   printf(
   "ERROR: Database header validation for '%S' failed with error %d (0x%x)\n",
   rgwszDb[ iDbError ],
   err,
   err );
   }
   goto HandleError;
   }
   ```
   
   <span data-ttu-id="5718a-126">有关参数的详细信息，请参阅[CChkSGFiles.ErrCheckDbHeaders 函数](cchksgfiles-errcheckdbheaders-function.md)。</span><span class="sxs-lookup"><span data-stu-id="5718a-126">For more information about the parameters, see [CChkSGFiles.ErrCheckDbHeaders function](cchksgfiles-errcheckdbheaders-function.md).</span></span>
   
4. <span data-ttu-id="5718a-127">处理错误，并使用[CChkSGFiles.Delete 函数](cchksgfiles-delete-function.md)从内存中删除的**CChkSGFiles**类。</span><span class="sxs-lookup"><span data-stu-id="5718a-127">Handle errors, and use the [CChkSGFiles.Delete function](cchksgfiles-delete-function.md) to remove the **CChkSGFiles** class from memory.</span></span> 
   
   ```cpp
   HandleError:
   CCheckSGFiles::Delete( pcchecksgfiles );  
   ```

## <a name="see-also"></a><span data-ttu-id="5718a-128">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5718a-128">See also</span></span>

- [<span data-ttu-id="5718a-129">CChkSGFiles 类参考 （英文）</span><span class="sxs-lookup"><span data-stu-id="5718a-129">CChkSGFiles class reference</span></span>](cchksgfiles-class-reference.md)
- [<span data-ttu-id="5718a-130">构建备份和还原 Exchange 2013 的应用程序</span><span class="sxs-lookup"><span data-stu-id="5718a-130">Build backup and restore applications for Exchange 2013</span></span>](build-backup-and-restore-applications-for-exchange-2013.md)
- [<span data-ttu-id="5718a-131">Exchange 2013 的备份和还原概念</span><span class="sxs-lookup"><span data-stu-id="5718a-131">Backup and restore concepts for Exchange 2013</span></span>](backup-and-restore-concepts-for-exchange-2013.md)
    

