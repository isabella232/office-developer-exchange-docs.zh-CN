---
title: 在 2013 年 6 月使用 CHKSGFILES API Exchange完整性
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 607cbeb9-0a02-4079-8a4d-34bdeb560224
description: 了解如何使用 CHKSGFILES API 验证 Exchange 2013 Exchange备份。
ms.openlocfilehash: 7a12a0a8f66128970a782da50ba59f41767c60d3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516228"
---
# <a name="validate-backup-integrity-by-using-the-chksgfiles-api-in-exchange-2013"></a>在 2013 年 6 月使用 CHKSGFILES API Exchange完整性

了解如何使用 CHKSGFILES API 验证 Exchange 2013 Exchange备份。
  
**适用于：Exchange Server** 2013 
  
在由卷影复制服务 (VSS) 管理的备份操作期间，Exchange Server 2013 无法完整读取每个数据库文件并验证其校验和完整性。 因此，您可能希望备份应用程序验证数据库和事务日志文件完整性。 建议您的备份应用程序先验证卷影副本集的物理一致性，Exchange编写器完成备份。 成功备份后，Exchange 存储将更新备份数据库的标头，以反映上次成功备份的时间，并从服务器中删除不再需要从上次成功备份中向前滚动的事务日志。
  
## <a name="prerequisites-for-validating-backup-integrity"></a>验证备份完整性的先决条件

在您的应用程序可以验证备份的完整性之前，您必须有权访问以下内容：
  
- 来自应用商店Exchange备份的文件。
- 从 2010 Visual Studio 2010 Visual Studio版本。
- CHKSGFILES 库和头文件。 可以从 Microsoft 下载中心下载库和 [头文件](https://www.microsoft.com/download/details.aspx?id=36802)。
    
## <a name="validate-backup-integrity"></a>验证备份完整性

以下过程介绍如何在备份和还原应用程序中验证数据完整性。
  
### <a name="to-validate-backup-integrity"></a>验证备份完整性

1. 创建 **CChkSGFiles** 类的新实例。 
   
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

   第一行代码创建一个错误对象，并设置其初始值为 success，并创建一个检查数据库有效性的对象。 然后 [，CChkSGFiles.New](cchksgfiles-new-function.md) 函数创建 **CChkSGFiles** 类的新实例。 快速检查新对象可指示在新建实例时是否发生了任何问题。 
    
2. 初始化 **CChkSGFiles** 对象。 
   
   ```cpp
   Call( pcchecksgfiles->ErrInit(
   rgwszDb,
   cDb,
   wszLogPath,
   wszBaseName ) );
   ```
   
   有关参数详细信息，请参阅 [CChkSGFiles.ErrInit 函数](cchksgfiles-errinit-function.md)。
   
3. 使用 [CChkSGFiles.ErrCheckDbHeaders](cchksgfiles-errcheckdbheaders-function.md) 函数通过检查数据库标头来验证数据库完整性。
   
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
   
   有关参数详细信息，请参阅 [CChkSGFiles.ErrCheckDbHeaders 函数](cchksgfiles-errcheckdbheaders-function.md)。
   
4. 处理错误，并使用 [CChkSGFiles.Delete 函数](cchksgfiles-delete-function.md) 从内存中删除 **CChkSGFiles** 类。 
   
   ```cpp
   HandleError:
   CCheckSGFiles::Delete( pcchecksgfiles );  
   ```

## <a name="see-also"></a>另请参阅

- [CChkSGFiles 类参考](cchksgfiles-class-reference.md)
- [构建适用于 Exchange 2013 的备份和还原应用程序](build-backup-and-restore-applications-for-exchange-2013.md)
- [Exchange 2013 的备份和还原概念](backup-and-restore-concepts-for-exchange-2013.md)
    

