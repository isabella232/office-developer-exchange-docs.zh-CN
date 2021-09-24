---
title: CChkSGFiles 类参考
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 9347d5f6-95bb-4045-9c86-0dc0ded24fe8
description: 查找 2013 年 10 月 CHKSGFILES API Exchange信息。
ms.openlocfilehash: 2daf31c41a47684b85ede196b415884335c3ca79
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510531"
---
# <a name="cchksgfiles-class-reference"></a>CChkSGFiles 类参考

查找 2013 年 10 月 CHKSGFILES API Exchange信息。
  
**适用于：Exchange Server** 2013 
  
CHKSGFILES API 支持备份和还原应用程序以编程方式验证 Exchange Server 2013 事务日志文件和数据库的完整性。 可以在使用 VSS 卷影复制服务的备份和还原应用程序中使用此 API (VSS) 。
  
> [!NOTE]
> 存储 2013 年 10 月Exchange组。 从 2010 年 10 Exchange开始，从 Exchange Server中删除了对存储组的支持。 为了向后兼容 Exchange 2010 Exchange之前版本的数据库和存储组，CHKSGFILES API 允许您指定存储组。 对 2013 Exchange CHKSGFILES 时，应该将指定存储组标识符的参数设置为空字符串。 
  
## <a name="file-location"></a>文件位置
<a name="bk_fileslocation"> </a>

CHKSGFILES API 作为 Exchange 2013 的一部分提供。 可以在安装了邮箱服务器角色的计算机上使用此 API。 
  
默认情况下，CHKSGFILES DLL 安装在 C：\Program Files\Microsoft\Exchange\V15\Bin 目录中。
  
Exchange 2013 仅包括 64 位 (amd64) 版本的 CHKSGFILES API。 
  
你可以从 [Microsoft](https://www.microsoft.com/download/details.aspx?id=36802)下载.zip下载一个包含 CHKSGFILE.lib 库和 CHKSGFILES.hxx 头文件以在自定义应用程序中使用的文件。
  
## <a name="development-languages"></a>开发语言
<a name="bk_developmentlanguages"> </a>

CHKSGFILES API 旨在与 2005 年 Visual Studio C/C++ 中的 Visual Studio 版本一起使用。 CHKSGFILES API 不适合在托管代码中使用。 尽管可以使用 CHKSGFILES 创建 COM 互操作程序集，但我们不会将支持的 COM 互操作程序集与 Exchange 2013 一起提供。
  
## <a name="in-this-section"></a>本节内容
<a name="bk_inthissection"> </a>

- [CChkSGFiles.CMaxDbPerSG 函数](cchksgfiles-cmaxdbpersg-function.md)
    
- [CChkSGFiles.Delete 函数](cchksgfiles-delete-function.md)
    
- [CChkSGFiles.ERR 枚举](cchksgfiles-err-enumeration.md)
    
- [CChkSGFiles.ErrCheckDbHeaders 函数](cchksgfiles-errcheckdbheaders-function.md)
    
- [CChkSGFiles.ErrCheckDbPages 函数](cchksgfiles-errcheckdbpages-function.md)
    
- [CChkSGFiles.ErrCheckLogs 函数](cchksgfiles-errchecklogs-function.md)
    
- [CChkSGFiles.ErrGetHeader 函数（预留）](cchksgfiles-errgetheader-function-reserved.md)
    
- [CChkSGFiles.ErrInit 函数](cchksgfiles-errinit-function.md)
    
- [CChkSGFiles.ErrTerm 函数](cchksgfiles-errterm-function.md)
    
- [CChkSGFiles.iDbInvalid 枚举](cchksgfiles-idbinvalid-enumeration.md)
    
- [CChkSGFiles.New 函数](cchksgfiles-new-function.md)
    
- [CChkSGFiles.NO_FLAGS 枚举](cchksgfiles-no_flags-enumeration.md)
    
- [CChkSGFiles.PAGE_INFO 结构](cchksgfiles-page_info-struct.md)
    
- [CChkSGFiles.PgnoFromFileOffset 函数](cchksgfiles-pgnofromfileoffset-function.md)
    
## <a name="see-also"></a>另请参阅

- [Exchange Online 和 Exchange 开发](../exchange-server-development.md)
- [备份、还原和灾难恢复](https://technet.microsoft.com/library/dd876874)
    

