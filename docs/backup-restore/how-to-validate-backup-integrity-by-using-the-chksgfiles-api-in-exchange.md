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
# <a name="validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange-2013"></a>使用 Exchange 2013 中的 CHKSGFILES API 验证备份完整性

了解如何使用 CHKSGFILES API 验证 exchange 存储在 Exchange 2013 中的备份。
  
**适用于：** Exchange Server 2013 
  
在卷影复制服务（VSS）管理的备份操作过程中，Exchange Server 2013 无法完全读取每个数据库文件，并验证其校验和完整性。 因此，您可能希望备份应用程序验证数据库和事务日志文件的完整性。 我们建议您的备份应用程序先验证卷影副本集的物理一致性，然后再通知 Exchange 编写器备份已完成。 成功备份后，Exchange 存储将更新已备份数据库的标头，以反映上次成功备份的时间，并从服务器中删除不再需要的事务日志，以从上次成功的备份中向前滚动。
  
## <a name="prerequisites-for-validating-backup-integrity"></a>验证备份完整性的先决条件

在您的应用程序可以验证备份的完整性之前，您必须能够访问以下内容：
  
- Exchange 存储备份中的文件。
- 以 Visual Studio 2010 开头的 Visual Studio 版本。
- CHKSGFILES 库和头文件。 您可以从[Microsoft 下载中心](https://www.microsoft.com/download/details.aspx?id=36802)下载库和头文件。
    
## <a name="validate-backup-integrity"></a>验证备份完整性

以下过程介绍如何验证备份和还原应用程序中的数据完整性。
  
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

   代码的第一行创建一个 error 对象，并将其初始值设置为 "成功"，并创建一个用于检查数据库有效性的对象。 然后， [CChkSGFiles 函数](cchksgfiles-new-function.md)创建**CChkSGFiles**类的新实例。 新对象的快速检查指示创建新实例时是否出现任何问题。 
    
2. 初始化**CChkSGFiles**对象。 
   
   ```cpp
   Call( pcchecksgfiles->ErrInit(
   rgwszDb,
   cDb,
   wszLogPath,
   wszBaseName ) );
   ```
   
   有关参数的详细信息，请参阅[CChkSGFiles 函数](cchksgfiles-errinit-function.md)。
   
3. 通过检查数据库标头，使用[ErrCheckDbHeaders 函数](cchksgfiles-errcheckdbheaders-function.md)来验证数据库的完整性 CChkSGFiles。
   
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
   
   有关参数的详细信息，请参阅[CChkSGFiles 函数](cchksgfiles-errcheckdbheaders-function.md)。
   
4. 处理错误，并使用[CChkSGFiles 函数](cchksgfiles-delete-function.md)从内存中删除**CChkSGFiles**类。 
   
   ```cpp
   HandleError:
   CCheckSGFiles::Delete( pcchecksgfiles );  
   ```

## <a name="see-also"></a>另请参阅

- [CChkSGFiles 类参考](cchksgfiles-class-reference.md)
- [为 Exchange 2013 生成备份和还原应用程序](build-backup-and-restore-applications-for-exchange-2013.md)
- [Exchange 2013 的备份和还原概念](backup-and-restore-concepts-for-exchange-2013.md)
    

