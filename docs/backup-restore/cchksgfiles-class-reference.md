---
title: CChkSGFiles 类参考
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9347d5f6-95bb-4045-9c86-0dc0ded24fe8
description: 在 Exchange 2013 中查找 CHKSGFILES API 的参考信息。
ms.openlocfilehash: 38b1f2c900767c22594636f0c6ddf4855961aec4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526730"
---
# <a name="cchksgfiles-class-reference"></a>CChkSGFiles 类参考

在 Exchange 2013 中查找 CHKSGFILES API 的参考信息。
  
**适用于：** Exchange Server 2013 
  
CHKSGFILES API 使备份和还原应用程序能够以编程方式验证 Exchange Server 2013 事务日志文件和数据库的完整性。 可以在使用卷影复制服务（VSS）的备份和还原应用程序中使用此 API。
  
> [!NOTE]
> 存储组在 Exchange 2013 中不可用。 从 exchange Server 2010 开始的 Exchange 版本中删除了对存储组的支持。 为了在 exchange 2010 之前的 Exchange 版本中与数据库和存储组保持向后兼容性，CHKSGFILES API 使您能够指定存储组。 当您针对 Exchange 2013 数据库运行 CHKSGFILES 时，应将指定存储组标识符的参数设置为空字符串。 
  
## <a name="file-location"></a>文件位置
<a name="bk_fileslocation"> </a>

CHKSGFILES API 作为 Exchange 2013 的一部分进行发行。 您可以在安装了邮箱服务器角色的计算机上使用此 API。 
  
默认情况下，CHKSGFILES DLL 安装在 C:\Program Files\Microsoft\Exchange\V15\Bin 目录中。
  
Exchange 2013 仅包含64位（amd64）版本的 CHKSGFILES API。 
  
您可以从[Microsoft 下载中心](https://www.microsoft.com/download/details.aspx?id=36802)下载包含 CHKSGFILE 库和 CHKSGFILES 头文件的 .zip 文件，以供自定义应用程序使用。
  
## <a name="development-languages"></a>开发语言
<a name="bk_developmentlanguages"> </a>

CHKSGFILES API 适用于 Visual Studio 的版本，从本机 C/c + + 中的 Visual Studio 2005 开始使用。 CHKSGFILES API 不适合在托管代码中使用。 尽管可以使用 CHKSGFILES 创建 COM 互操作程序集，但我们并不会在 Exchange 2013 中附带支持的 COM 互操作程序集。
  
## <a name="in-this-section"></a>本节内容
<a name="bk_inthissection"> </a>

- [CChkSGFiles 函数](cchksgfiles-cmaxdbpersg-function.md)
    
- [CChkSGFiles 函数](cchksgfiles-delete-function.md)
    
- [CChkSGFiles 枚举](cchksgfiles-err-enumeration.md)
    
- [CChkSGFiles 函数](cchksgfiles-errcheckdbheaders-function.md)
    
- [CChkSGFiles 函数](cchksgfiles-errcheckdbpages-function.md)
    
- [CChkSGFiles 函数](cchksgfiles-errchecklogs-function.md)
    
- [CChkSGFiles 函数（保留）](cchksgfiles-errgetheader-function-reserved.md)
    
- [CChkSGFiles 函数](cchksgfiles-errinit-function.md)
    
- [CChkSGFiles 函数](cchksgfiles-errterm-function.md)
    
- [IDbInvalid 枚举 CChkSGFiles](cchksgfiles-idbinvalid-enumeration.md)
    
- [CChkSGFiles 函数](cchksgfiles-new-function.md)
    
- [NO_FLAGS CChkSGFiles 枚举](cchksgfiles-no_flags-enumeration.md)
    
- [CChkSGFiles 结构 PAGE_INFO 结构](cchksgfiles-page_info-struct.md)
    
- [CChkSGFiles 函数](cchksgfiles-pgnofromfileoffset-function.md)
    
## <a name="see-also"></a>另请参阅

- [Exchange Online 和 Exchange 开发](../exchange-server-development.md)
- [备份、还原和灾难恢复](https://technet.microsoft.com/library/dd876874)
    

