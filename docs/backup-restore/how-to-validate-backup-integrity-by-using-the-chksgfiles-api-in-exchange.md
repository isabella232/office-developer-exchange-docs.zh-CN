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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752691"
---
# <a name="validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange-2013"></a>使用 CHKSGFILES API 在 Exchange 2013 中验证备份完整性

了解如何使用 CHKSGFILES API 在 Exchange 2013 验证 Exchange 存储的备份。
  
**适用于：** Exchange Server 2013 
  
备份操作期间托管的卷影复制服务 (VSS)，Exchange Server 2013 无法读取完整地复制每个数据库文件，并验证其校验和完整性。 因此，您可能希望您备份的应用程序，以验证数据库和事务日志文件的完整性。 我们建议您备份应用程序验证之前告知 Exchange 书写器完成备份后的卷影副本集的物理一致性。 成功备份后，Exchange 存储更新的备份的数据库以反映上次成功备份时间，并从服务器删除事务日志不再需要滚从最后一次成功备份的标题。
  
## <a name="prerequisites-for-validating-backup-integrity"></a>验证备份完整性的先决条件

您的应用程序可以验证备份的完整性之前，您必须具有访问以下：
  
- 从 Exchange 存储备份文件。
- 开始使用 Visual Studio 2010 的 Visual Studio 的版本。
- CHKSGFILES 库和头文件。 您可以从[Microsoft 下载中心](http://www.microsoft.com/en-us/download/details.aspx?id=36802)下载库和头文件。
    
## <a name="validate-backup-integrity"></a>验证备份完整性

以下过程介绍如何验证数据完整性中备份和还原应用程序。
  
### <a name="to-validate-backup-integrity"></a>验证备份完整性

1. 创建**CChkSGFiles**类的新实例。 
   
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

   第一个代码行创建 error 对象并将其初始值设置为成功，创建一个对象，检查数据库的有效性。 然后， [CChkSGFiles.New 函数](cchksgfiles-new-function.md)创建**CChkSGFiles**类的新实例。 快速检查新对象的指示的任何问题出现时创建的新实例。 
    
2. 初始化**CChkSGFiles**对象。 
   
   ```cpp
   Call( pcchecksgfiles->ErrInit(
   rgwszDb,
   cDb,
   wszLogPath,
   wszBaseName ) );
   ```
   
   有关参数的详细信息，请参阅[CChkSGFiles.ErrInit 函数](cchksgfiles-errinit-function.md)。
   
3. 使用[CChkSGFiles.ErrCheckDbHeaders 函数](cchksgfiles-errcheckdbheaders-function.md)通过检查数据库标头中验证数据库的完整性。
   
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
   
   有关参数的详细信息，请参阅[CChkSGFiles.ErrCheckDbHeaders 函数](cchksgfiles-errcheckdbheaders-function.md)。
   
4. 处理错误，并使用[CChkSGFiles.Delete 函数](cchksgfiles-delete-function.md)从内存中删除的**CChkSGFiles**类。 
   
   ```cpp
   HandleError:
   CCheckSGFiles::Delete( pcchecksgfiles );  
   ```

## <a name="see-also"></a>另请参阅

- [CChkSGFiles 类参考 （英文）](cchksgfiles-class-reference.md)
- [构建备份和还原 Exchange 2013 的应用程序](build-backup-and-restore-applications-for-exchange-2013.md)
- [Exchange 2013 的备份和还原概念](backup-and-restore-concepts-for-exchange-2013.md)
    

