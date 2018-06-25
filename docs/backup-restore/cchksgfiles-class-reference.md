---
title: CChkSGFiles 类参考 （英文）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9347d5f6-95bb-4045-9c86-0dc0ded24fe8
description: Exchange 2013 中查找 CHKSGFILES API 的参考信息。
ms.openlocfilehash: 583ac5e16ab60d119c3028bf81123e9f60a58ff4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752689"
---
# <a name="cchksgfiles-class-reference"></a>CChkSGFiles 类参考 （英文）

Exchange 2013 中查找 CHKSGFILES API 的参考信息。
  
**适用于：** Exchange Server 2013 
  
CHKSGFILES API 使备份和还原应用程序以编程方式验证 Exchange Server 2013 事务日志文件和数据库的完整性。 您可以使用此 API 中备份和还原使用卷影复制服务 (VSS) 的应用程序。
  
> [!NOTE]
> 存储组不可用在 Exchange 2013。 从开头 Exchange Server 2010 的 Exchange 版本中移除了存储组的支持。 与数据库和存储组的 Exchange 版本早于 Exchange 2010 中的向后兼容性，CHKSGFILES API 可以指定存储组。 针对 Exchange 2013 数据库运行 CHKSGFILES 时，您应设置为空字符串的存储组标识符指定的参数。 
  
## <a name="file-location"></a>文件位置
<a name="bk_fileslocation"> </a>

Exchange 2013 的一部分附带 CHKSGFILES API。 您可以使用此 API 上已安装了邮箱服务器角色的计算机。 
  
默认情况下，C:\Program Files\Microsoft\Exchange\V15\Bin 目录中安装 CHKSGFILES DLL。
  
Exchange 2013 包括仅 CHKSGFILES API 的 64 位 (amd64) 版本。 
  
您可以在自定义应用程序从[Microsoft 下载中心](http://www.microsoft.com/en-us/download/details.aspx?id=36802)下载的.zip 文件中包含 CHKSGFILE.lib 库和用于 CHKSGFILES.hxx 头文件。
  
## <a name="development-languages"></a>开发语言
<a name="bk_developmentlanguages"> </a>

CHKSGFILES API 用于 Visual Studio 开头 native C/c + + 中的 Visual Studio 2005 的版本。 CHKSGFILES API 不是在托管代码中使用。 尽管您可以使用 CHKSGFILES 创建 COM 互操作程序集，但我们不要发行 Exchange 2013 的受支持的 COM 互操作程序集。
  
## <a name="in-this-section"></a>本节内容
<a name="bk_inthissection"> </a>

- [CChkSGFiles.CMaxDbPerSG 函数](cchksgfiles-cmaxdbpersg-function.md)
    
- [CChkSGFiles.Delete 函数](cchksgfiles-delete-function.md)
    
- [CChkSGFiles.ERR 枚举](cchksgfiles-err-enumeration.md)
    
- [CChkSGFiles.ErrCheckDbHeaders 函数](cchksgfiles-errcheckdbheaders-function.md)
    
- [CChkSGFiles.ErrCheckDbPages 函数](cchksgfiles-errcheckdbpages-function.md)
    
- [CChkSGFiles.ErrCheckLogs 函数](cchksgfiles-errchecklogs-function.md)
    
- [CChkSGFiles.ErrGetHeader 函数 （保留）](cchksgfiles-errgetheader-function-reserved.md)
    
- [CChkSGFiles.ErrInit 函数](cchksgfiles-errinit-function.md)
    
- [CChkSGFiles.ErrTerm 函数](cchksgfiles-errterm-function.md)
    
- [CChkSGFiles.iDbInvalid 枚举](cchksgfiles-idbinvalid-enumeration.md)
    
- [CChkSGFiles.New 函数](cchksgfiles-new-function.md)
    
- [CChkSGFiles.NO_FLAGS 枚举](cchksgfiles-no_flags-enumeration.md)
    
- [CChkSGFiles.PAGE_INFO 结构](cchksgfiles-page_info-struct.md)
    
- [CChkSGFiles.PgnoFromFileOffset 函数](cchksgfiles-pgnofromfileoffset-function.md)
    
## <a name="see-also"></a>另请参阅

- [Exchange Online 和 Exchange 开发](../exchange-server-development.md)
- [备份、 还原和灾难恢复](http://technet.microsoft.com/en-us/library/dd876874)
    

