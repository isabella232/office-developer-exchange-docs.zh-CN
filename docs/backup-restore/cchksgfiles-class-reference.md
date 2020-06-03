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
# <a name="cchksgfiles-class-reference"></a><span data-ttu-id="09183-103">CChkSGFiles 类参考</span><span class="sxs-lookup"><span data-stu-id="09183-103">CChkSGFiles class reference</span></span>

<span data-ttu-id="09183-104">在 Exchange 2013 中查找 CHKSGFILES API 的参考信息。</span><span class="sxs-lookup"><span data-stu-id="09183-104">Find reference information for the CHKSGFILES API in Exchange 2013.</span></span>
  
<span data-ttu-id="09183-105">**适用于：** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="09183-105">**Applies to:** Exchange Server 2013</span></span> 
  
<span data-ttu-id="09183-106">CHKSGFILES API 使备份和还原应用程序能够以编程方式验证 Exchange Server 2013 事务日志文件和数据库的完整性。</span><span class="sxs-lookup"><span data-stu-id="09183-106">The CHKSGFILES API enables backup and restore applications to verify the integrity of Exchange Server 2013 transaction log files and databases programmatically.</span></span> <span data-ttu-id="09183-107">可以在使用卷影复制服务（VSS）的备份和还原应用程序中使用此 API。</span><span class="sxs-lookup"><span data-stu-id="09183-107">You can use this API in backup and restore applications that use the Volume Shadow Copy Service (VSS).</span></span>
  
> [!NOTE]
> <span data-ttu-id="09183-108">存储组在 Exchange 2013 中不可用。</span><span class="sxs-lookup"><span data-stu-id="09183-108">Storage groups are not available in Exchange 2013.</span></span> <span data-ttu-id="09183-109">从 exchange Server 2010 开始的 Exchange 版本中删除了对存储组的支持。</span><span class="sxs-lookup"><span data-stu-id="09183-109">Support for storage groups was removed from versions of Exchange starting with Exchange Server 2010.</span></span> <span data-ttu-id="09183-110">为了在 exchange 2010 之前的 Exchange 版本中与数据库和存储组保持向后兼容性，CHKSGFILES API 使您能够指定存储组。</span><span class="sxs-lookup"><span data-stu-id="09183-110">For backward compatibility with databases and storage groups in versions of Exchange earlier than Exchange 2010, the CHKSGFILES API enables you to specify storage groups.</span></span> <span data-ttu-id="09183-111">当您针对 Exchange 2013 数据库运行 CHKSGFILES 时，应将指定存储组标识符的参数设置为空字符串。</span><span class="sxs-lookup"><span data-stu-id="09183-111">When you run CHKSGFILES against Exchange 2013 databases, you should set parameters that specify a storage group identifier to an empty string.</span></span> 
  
## <a name="file-location"></a><span data-ttu-id="09183-112">文件位置</span><span class="sxs-lookup"><span data-stu-id="09183-112">File location</span></span>
<span data-ttu-id="09183-113"><a name="bk_fileslocation"> </a></span><span class="sxs-lookup"><span data-stu-id="09183-113"><a name="bk_fileslocation"> </a></span></span>

<span data-ttu-id="09183-114">CHKSGFILES API 作为 Exchange 2013 的一部分进行发行。</span><span class="sxs-lookup"><span data-stu-id="09183-114">The CHKSGFILES API ships as part of Exchange 2013.</span></span> <span data-ttu-id="09183-115">您可以在安装了邮箱服务器角色的计算机上使用此 API。</span><span class="sxs-lookup"><span data-stu-id="09183-115">You can use this API on a computer that has the Mailbox server role installed.</span></span> 
  
<span data-ttu-id="09183-116">默认情况下，CHKSGFILES DLL 安装在 C:\Program Files\Microsoft\Exchange\V15\Bin 目录中。</span><span class="sxs-lookup"><span data-stu-id="09183-116">By default, the CHKSGFILES DLL is installed in the C:\Program Files\Microsoft\Exchange\V15\Bin directory.</span></span>
  
<span data-ttu-id="09183-117">Exchange 2013 仅包含64位（amd64）版本的 CHKSGFILES API。</span><span class="sxs-lookup"><span data-stu-id="09183-117">Exchange 2013 includes only a 64-bit (amd64) version of the CHKSGFILES API.</span></span> 
  
<span data-ttu-id="09183-118">您可以从[Microsoft 下载中心](https://www.microsoft.com/download/details.aspx?id=36802)下载包含 CHKSGFILE 库和 CHKSGFILES 头文件的 .zip 文件，以供自定义应用程序使用。</span><span class="sxs-lookup"><span data-stu-id="09183-118">You can download a .zip file that includes the CHKSGFILE.lib library and CHKSGFILES.hxx header files for use in your custom application from the [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=36802).</span></span>
  
## <a name="development-languages"></a><span data-ttu-id="09183-119">开发语言</span><span class="sxs-lookup"><span data-stu-id="09183-119">Development languages</span></span>
<span data-ttu-id="09183-120"><a name="bk_developmentlanguages"> </a></span><span class="sxs-lookup"><span data-stu-id="09183-120"><a name="bk_developmentlanguages"> </a></span></span>

<span data-ttu-id="09183-121">CHKSGFILES API 适用于 Visual Studio 的版本，从本机 C/c + + 中的 Visual Studio 2005 开始使用。</span><span class="sxs-lookup"><span data-stu-id="09183-121">The CHKSGFILES API is intended for use with versions of Visual Studio starting with Visual Studio 2005 in native C/C++.</span></span> <span data-ttu-id="09183-122">CHKSGFILES API 不适合在托管代码中使用。</span><span class="sxs-lookup"><span data-stu-id="09183-122">The CHKSGFILES API is not intended for use in managed code.</span></span> <span data-ttu-id="09183-123">尽管可以使用 CHKSGFILES 创建 COM 互操作程序集，但我们并不会在 Exchange 2013 中附带支持的 COM 互操作程序集。</span><span class="sxs-lookup"><span data-stu-id="09183-123">Although you can create a COM Interop assembly with CHKSGFILES, we do not ship a supported COM Interop assembly with Exchange 2013.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="09183-124">本节内容</span><span class="sxs-lookup"><span data-stu-id="09183-124">In this section</span></span>
<span data-ttu-id="09183-125"><a name="bk_inthissection"> </a></span><span class="sxs-lookup"><span data-stu-id="09183-125"><a name="bk_inthissection"> </a></span></span>

- [<span data-ttu-id="09183-126">CChkSGFiles 函数</span><span class="sxs-lookup"><span data-stu-id="09183-126">CChkSGFiles.CMaxDbPerSG function</span></span>](cchksgfiles-cmaxdbpersg-function.md)
    
- [<span data-ttu-id="09183-127">CChkSGFiles 函数</span><span class="sxs-lookup"><span data-stu-id="09183-127">CChkSGFiles.Delete function</span></span>](cchksgfiles-delete-function.md)
    
- [<span data-ttu-id="09183-128">CChkSGFiles 枚举</span><span class="sxs-lookup"><span data-stu-id="09183-128">CChkSGFiles.ERR enumeration</span></span>](cchksgfiles-err-enumeration.md)
    
- [<span data-ttu-id="09183-129">CChkSGFiles 函数</span><span class="sxs-lookup"><span data-stu-id="09183-129">CChkSGFiles.ErrCheckDbHeaders function</span></span>](cchksgfiles-errcheckdbheaders-function.md)
    
- [<span data-ttu-id="09183-130">CChkSGFiles 函数</span><span class="sxs-lookup"><span data-stu-id="09183-130">CChkSGFiles.ErrCheckDbPages function</span></span>](cchksgfiles-errcheckdbpages-function.md)
    
- [<span data-ttu-id="09183-131">CChkSGFiles 函数</span><span class="sxs-lookup"><span data-stu-id="09183-131">CChkSGFiles.ErrCheckLogs function</span></span>](cchksgfiles-errchecklogs-function.md)
    
- [<span data-ttu-id="09183-132">CChkSGFiles 函数（保留）</span><span class="sxs-lookup"><span data-stu-id="09183-132">CChkSGFiles.ErrGetHeader function (reserved)</span></span>](cchksgfiles-errgetheader-function-reserved.md)
    
- [<span data-ttu-id="09183-133">CChkSGFiles 函数</span><span class="sxs-lookup"><span data-stu-id="09183-133">CChkSGFiles.ErrInit function</span></span>](cchksgfiles-errinit-function.md)
    
- [<span data-ttu-id="09183-134">CChkSGFiles 函数</span><span class="sxs-lookup"><span data-stu-id="09183-134">CChkSGFiles.ErrTerm function</span></span>](cchksgfiles-errterm-function.md)
    
- [<span data-ttu-id="09183-135">IDbInvalid 枚举 CChkSGFiles</span><span class="sxs-lookup"><span data-stu-id="09183-135">CChkSGFiles.iDbInvalid enumeration</span></span>](cchksgfiles-idbinvalid-enumeration.md)
    
- [<span data-ttu-id="09183-136">CChkSGFiles 函数</span><span class="sxs-lookup"><span data-stu-id="09183-136">CChkSGFiles.New function</span></span>](cchksgfiles-new-function.md)
    
- [<span data-ttu-id="09183-137">NO_FLAGS CChkSGFiles 枚举</span><span class="sxs-lookup"><span data-stu-id="09183-137">CChkSGFiles.NO_FLAGS enumeration</span></span>](cchksgfiles-no_flags-enumeration.md)
    
- [<span data-ttu-id="09183-138">CChkSGFiles 结构 PAGE_INFO 结构</span><span class="sxs-lookup"><span data-stu-id="09183-138">CChkSGFiles.PAGE_INFO struct</span></span>](cchksgfiles-page_info-struct.md)
    
- [<span data-ttu-id="09183-139">CChkSGFiles 函数</span><span class="sxs-lookup"><span data-stu-id="09183-139">CChkSGFiles.PgnoFromFileOffset function</span></span>](cchksgfiles-pgnofromfileoffset-function.md)
    
## <a name="see-also"></a><span data-ttu-id="09183-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="09183-140">See also</span></span>

- [<span data-ttu-id="09183-141">Exchange Online 和 Exchange 开发</span><span class="sxs-lookup"><span data-stu-id="09183-141">Exchange Online and Exchange development</span></span>](../exchange-server-development.md)
- [<span data-ttu-id="09183-142">备份、还原和灾难恢复</span><span class="sxs-lookup"><span data-stu-id="09183-142">Backup, Restore, and Disaster Recovery</span></span>](https://technet.microsoft.com/library/dd876874)
    

