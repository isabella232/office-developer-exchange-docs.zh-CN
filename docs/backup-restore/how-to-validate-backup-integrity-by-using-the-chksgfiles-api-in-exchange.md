---
title: 使用 Exchange 2013 中的 CHKSGFILES API 验证备份完整性
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 607cbeb9-0a02-4079-8a4d-34bdeb560224
description: 了解如何使用 CHKSGFILES API 验证 exchange 存储在 Exchange 2013 中的备份。
ms.openlocfilehash: c101413793cf3b952d3db3e0f792c8bcf2dd9fc9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44452858"
---
# <a name="validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange-2013"></a><span data-ttu-id="36d13-103">使用 Exchange 2013 中的 CHKSGFILES API 验证备份完整性</span><span class="sxs-lookup"><span data-stu-id="36d13-103">Validate backup integrity by using the CHKSGFILES API in Exchange 2013</span></span>

<span data-ttu-id="36d13-104">了解如何使用 CHKSGFILES API 验证 exchange 存储在 Exchange 2013 中的备份。</span><span class="sxs-lookup"><span data-stu-id="36d13-104">Find out how to use the CHKSGFILES API to validate a backup of the Exchange store in Exchange 2013.</span></span>
  
<span data-ttu-id="36d13-105">**适用于：** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="36d13-105">**Applies to:** Exchange Server 2013</span></span> 
  
<span data-ttu-id="36d13-106">在卷影复制服务（VSS）管理的备份操作过程中，Exchange Server 2013 无法完全读取每个数据库文件，并验证其校验和完整性。</span><span class="sxs-lookup"><span data-stu-id="36d13-106">During backup operations managed by the Volume Shadow Copy Service (VSS), Exchange Server 2013 cannot read each database file in its entirety and verify its checksum integrity.</span></span> <span data-ttu-id="36d13-107">因此，您可能希望备份应用程序验证数据库和事务日志文件的完整性。</span><span class="sxs-lookup"><span data-stu-id="36d13-107">Therefore, you might want your backup application to verify database and transaction log file integrity.</span></span> <span data-ttu-id="36d13-108">我们建议您的备份应用程序先验证卷影副本集的物理一致性，然后再通知 Exchange 编写器备份已完成。</span><span class="sxs-lookup"><span data-stu-id="36d13-108">We recommend that your backup application verify the physical consistency of the shadow copy set prior to informing the Exchange writer that the backup is complete.</span></span> <span data-ttu-id="36d13-109">成功备份后，Exchange 存储将更新已备份数据库的标头，以反映上次成功备份的时间，并从服务器中删除不再需要的事务日志，以从上次成功的备份中向前滚动。</span><span class="sxs-lookup"><span data-stu-id="36d13-109">After a successful backup, the Exchange store updates the headers of the backed-up databases to reflect the last successful backup times and removes transaction logs from the server that are no longer required to roll forward from the last successful backup.</span></span>
  
## <a name="prerequisites-for-validating-backup-integrity"></a><span data-ttu-id="36d13-110">验证备份完整性的先决条件</span><span class="sxs-lookup"><span data-stu-id="36d13-110">Prerequisites for validating backup integrity</span></span>

<span data-ttu-id="36d13-111">在您的应用程序可以验证备份的完整性之前，您必须能够访问以下内容：</span><span class="sxs-lookup"><span data-stu-id="36d13-111">Before your application can validate the integrity of your backup, you must have access to the following:</span></span>
  
- <span data-ttu-id="36d13-112">Exchange 存储备份中的文件。</span><span class="sxs-lookup"><span data-stu-id="36d13-112">Files from your Exchange store backup.</span></span>
- <span data-ttu-id="36d13-113">以 Visual Studio 2010 开头的 Visual Studio 版本。</span><span class="sxs-lookup"><span data-stu-id="36d13-113">A version of Visual Studio starting with Visual Studio 2010.</span></span>
- <span data-ttu-id="36d13-114">CHKSGFILES 库和头文件。</span><span class="sxs-lookup"><span data-stu-id="36d13-114">The CHKSGFILES library and header files.</span></span> <span data-ttu-id="36d13-115">您可以从[Microsoft 下载中心](https://www.microsoft.com/download/details.aspx?id=36802)下载库和头文件。</span><span class="sxs-lookup"><span data-stu-id="36d13-115">You can download the library and header files from the [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=36802).</span></span>
    
## <a name="validate-backup-integrity"></a><span data-ttu-id="36d13-116">验证备份完整性</span><span class="sxs-lookup"><span data-stu-id="36d13-116">Validate backup integrity</span></span>

<span data-ttu-id="36d13-117">以下过程介绍如何验证备份和还原应用程序中的数据完整性。</span><span class="sxs-lookup"><span data-stu-id="36d13-117">The following procedure describes how to validate data integrity in your backup and restore application.</span></span>
  
### <a name="to-validate-backup-integrity"></a><span data-ttu-id="36d13-118">验证备份完整性</span><span class="sxs-lookup"><span data-stu-id="36d13-118">To validate backup integrity</span></span>

1. <span data-ttu-id="36d13-119">创建**CChkSGFiles**类的新实例。</span><span class="sxs-lookup"><span data-stu-id="36d13-119">Create a new instance of the **CChkSGFiles** class.</span></span> 
   
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

   <span data-ttu-id="36d13-120">代码的第一行创建一个 error 对象，并将其初始值设置为 "成功"，并创建一个用于检查数据库有效性的对象。</span><span class="sxs-lookup"><span data-stu-id="36d13-120">The first lines of code create an error object and set its initial value to success, and create an object that checks the validity of the database.</span></span> <span data-ttu-id="36d13-121">然后， [CChkSGFiles 函数](cchksgfiles-new-function.md)创建**CChkSGFiles**类的新实例。</span><span class="sxs-lookup"><span data-stu-id="36d13-121">Then, the [CChkSGFiles.New function](cchksgfiles-new-function.md) creates a new instance of the **CChkSGFiles** class.</span></span> <span data-ttu-id="36d13-122">新对象的快速检查指示创建新实例时是否出现任何问题。</span><span class="sxs-lookup"><span data-stu-id="36d13-122">A quick check of the new object indicates whether any issues occurred when the new instance was created.</span></span> 
    
2. <span data-ttu-id="36d13-123">初始化**CChkSGFiles**对象。</span><span class="sxs-lookup"><span data-stu-id="36d13-123">Initialize the **CChkSGFiles** object.</span></span> 
   
   ```cpp
   Call( pcchecksgfiles->ErrInit(
   rgwszDb,
   cDb,
   wszLogPath,
   wszBaseName ) );
   ```
   
   <span data-ttu-id="36d13-124">有关参数的详细信息，请参阅[CChkSGFiles 函数](cchksgfiles-errinit-function.md)。</span><span class="sxs-lookup"><span data-stu-id="36d13-124">For more information about the parameters, see [CChkSGFiles.ErrInit function](cchksgfiles-errinit-function.md).</span></span>
   
3. <span data-ttu-id="36d13-125">通过检查数据库标头，使用[ErrCheckDbHeaders 函数](cchksgfiles-errcheckdbheaders-function.md)来验证数据库的完整性 CChkSGFiles。</span><span class="sxs-lookup"><span data-stu-id="36d13-125">Use the [CChkSGFiles.ErrCheckDbHeaders function](cchksgfiles-errcheckdbheaders-function.md) to validate database integrity by checking the database headers.</span></span>
   
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
   
   <span data-ttu-id="36d13-126">有关参数的详细信息，请参阅[CChkSGFiles 函数](cchksgfiles-errcheckdbheaders-function.md)。</span><span class="sxs-lookup"><span data-stu-id="36d13-126">For more information about the parameters, see [CChkSGFiles.ErrCheckDbHeaders function](cchksgfiles-errcheckdbheaders-function.md).</span></span>
   
4. <span data-ttu-id="36d13-127">处理错误，并使用[CChkSGFiles 函数](cchksgfiles-delete-function.md)从内存中删除**CChkSGFiles**类。</span><span class="sxs-lookup"><span data-stu-id="36d13-127">Handle errors, and use the [CChkSGFiles.Delete function](cchksgfiles-delete-function.md) to remove the **CChkSGFiles** class from memory.</span></span> 
   
   ```cpp
   HandleError:
   CCheckSGFiles::Delete( pcchecksgfiles );  
   ```

## <a name="see-also"></a><span data-ttu-id="36d13-128">另请参阅</span><span class="sxs-lookup"><span data-stu-id="36d13-128">See also</span></span>

- [<span data-ttu-id="36d13-129">CChkSGFiles 类参考</span><span class="sxs-lookup"><span data-stu-id="36d13-129">CChkSGFiles class reference</span></span>](cchksgfiles-class-reference.md)
- [<span data-ttu-id="36d13-130">为 Exchange 2013 生成备份和还原应用程序</span><span class="sxs-lookup"><span data-stu-id="36d13-130">Build backup and restore applications for Exchange 2013</span></span>](build-backup-and-restore-applications-for-exchange-2013.md)
- [<span data-ttu-id="36d13-131">Exchange 2013 的备份和还原概念</span><span class="sxs-lookup"><span data-stu-id="36d13-131">Backup and restore concepts for Exchange 2013</span></span>](backup-and-restore-concepts-for-exchange-2013.md)
    

