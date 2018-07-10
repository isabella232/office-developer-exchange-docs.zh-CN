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
# <a name="cchksgfiles-class-reference"></a><span data-ttu-id="38ccd-103">CChkSGFiles 类参考 （英文）</span><span class="sxs-lookup"><span data-stu-id="38ccd-103">CChkSGFiles class reference</span></span>

<span data-ttu-id="38ccd-104">Exchange 2013 中查找 CHKSGFILES API 的参考信息。</span><span class="sxs-lookup"><span data-stu-id="38ccd-104">Find reference information for the CHKSGFILES API in Exchange 2013.</span></span>
  
<span data-ttu-id="38ccd-105">**适用于：** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="38ccd-105">**Applies to:** Exchange Server 2013</span></span> 
  
<span data-ttu-id="38ccd-106">CHKSGFILES API 使备份和还原应用程序以编程方式验证 Exchange Server 2013 事务日志文件和数据库的完整性。</span><span class="sxs-lookup"><span data-stu-id="38ccd-106">The CHKSGFILES API enables backup and restore applications to verify the integrity of Exchange Server 2013 transaction log files and databases programmatically.</span></span> <span data-ttu-id="38ccd-107">您可以使用此 API 中备份和还原使用卷影复制服务 (VSS) 的应用程序。</span><span class="sxs-lookup"><span data-stu-id="38ccd-107">You can use this API in backup and restore applications that use the Volume Shadow Copy Service (VSS).</span></span>
  
> [!NOTE]
> <span data-ttu-id="38ccd-108">存储组不可用在 Exchange 2013。</span><span class="sxs-lookup"><span data-stu-id="38ccd-108">Storage groups are not available in Exchange 2013.</span></span> <span data-ttu-id="38ccd-109">从开头 Exchange Server 2010 的 Exchange 版本中移除了存储组的支持。</span><span class="sxs-lookup"><span data-stu-id="38ccd-109">Support for storage groups was removed from versions of Exchange starting with Exchange Server 2010.</span></span> <span data-ttu-id="38ccd-110">与数据库和存储组的 Exchange 版本早于 Exchange 2010 中的向后兼容性，CHKSGFILES API 可以指定存储组。</span><span class="sxs-lookup"><span data-stu-id="38ccd-110">For backward compatibility with databases and storage groups in versions of Exchange earlier than Exchange 2010, the CHKSGFILES API enables you to specify storage groups.</span></span> <span data-ttu-id="38ccd-111">针对 Exchange 2013 数据库运行 CHKSGFILES 时，您应设置为空字符串的存储组标识符指定的参数。</span><span class="sxs-lookup"><span data-stu-id="38ccd-111">When you run CHKSGFILES against Exchange 2013 databases, you should set parameters that specify a storage group identifier to an empty string.</span></span> 
  
## <a name="file-location"></a><span data-ttu-id="38ccd-112">文件位置</span><span class="sxs-lookup"><span data-stu-id="38ccd-112">File location</span></span>
<span data-ttu-id="38ccd-113"><a name="bk_fileslocation"> </a></span><span class="sxs-lookup"><span data-stu-id="38ccd-113"></span></span>

<span data-ttu-id="38ccd-114">Exchange 2013 的一部分附带 CHKSGFILES API。</span><span class="sxs-lookup"><span data-stu-id="38ccd-114">The CHKSGFILES API ships as part of Exchange 2013.</span></span> <span data-ttu-id="38ccd-115">您可以使用此 API 上已安装了邮箱服务器角色的计算机。</span><span class="sxs-lookup"><span data-stu-id="38ccd-115">You can use this API on a computer that has the Mailbox server role installed.</span></span> 
  
<span data-ttu-id="38ccd-116">默认情况下，C:\Program Files\Microsoft\Exchange\V15\Bin 目录中安装 CHKSGFILES DLL。</span><span class="sxs-lookup"><span data-stu-id="38ccd-116">By default, the CHKSGFILES DLL is installed in the C:\Program Files\Microsoft\Exchange\V15\Bin directory.</span></span>
  
<span data-ttu-id="38ccd-117">Exchange 2013 包括仅 CHKSGFILES API 的 64 位 (amd64) 版本。</span><span class="sxs-lookup"><span data-stu-id="38ccd-117">Exchange 2013 includes only a 64-bit (amd64) version of the CHKSGFILES API.</span></span> 
  
<span data-ttu-id="38ccd-118">您可以在自定义应用程序从[Microsoft 下载中心](http://www.microsoft.com/en-us/download/details.aspx?id=36802)下载的.zip 文件中包含 CHKSGFILE.lib 库和用于 CHKSGFILES.hxx 头文件。</span><span class="sxs-lookup"><span data-stu-id="38ccd-118">You can download a .zip file that includes the CHKSGFILE.lib library and CHKSGFILES.hxx header files for use in your custom application from the [Microsoft Download Center](http://www.microsoft.com/en-us/download/details.aspx?id=36802).</span></span>
  
## <a name="development-languages"></a><span data-ttu-id="38ccd-119">开发语言</span><span class="sxs-lookup"><span data-stu-id="38ccd-119">Development languages</span></span>
<span data-ttu-id="38ccd-120"><a name="bk_developmentlanguages"> </a></span><span class="sxs-lookup"><span data-stu-id="38ccd-120"></span></span>

<span data-ttu-id="38ccd-121">CHKSGFILES API 用于 Visual Studio 开头 native C/c + + 中的 Visual Studio 2005 的版本。</span><span class="sxs-lookup"><span data-stu-id="38ccd-121">The CHKSGFILES API is intended for use with versions of Visual Studio starting with Visual Studio 2005 in native C/C++.</span></span> <span data-ttu-id="38ccd-122">CHKSGFILES API 不是在托管代码中使用。</span><span class="sxs-lookup"><span data-stu-id="38ccd-122">The CHKSGFILES API is not intended for use in managed code.</span></span> <span data-ttu-id="38ccd-123">尽管您可以使用 CHKSGFILES 创建 COM 互操作程序集，但我们不要发行 Exchange 2013 的受支持的 COM 互操作程序集。</span><span class="sxs-lookup"><span data-stu-id="38ccd-123">Although you can create a COM Interop assembly with CHKSGFILES, we do not ship a supported COM Interop assembly with Exchange 2013.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="38ccd-124">本节内容</span><span class="sxs-lookup"><span data-stu-id="38ccd-124">In this section</span></span>
<span data-ttu-id="38ccd-125"><a name="bk_inthissection"> </a></span><span class="sxs-lookup"><span data-stu-id="38ccd-125"></span></span>

- [<span data-ttu-id="38ccd-126">CChkSGFiles.CMaxDbPerSG 函数</span><span class="sxs-lookup"><span data-stu-id="38ccd-126">CChkSGFiles.CMaxDbPerSG function</span></span>](cchksgfiles-cmaxdbpersg-function.md)
    
- [<span data-ttu-id="38ccd-127">CChkSGFiles.Delete 函数</span><span class="sxs-lookup"><span data-stu-id="38ccd-127">CChkSGFiles.Delete function</span></span>](cchksgfiles-delete-function.md)
    
- [<span data-ttu-id="38ccd-128">CChkSGFiles.ERR 枚举</span><span class="sxs-lookup"><span data-stu-id="38ccd-128">CChkSGFiles.ERR enumeration</span></span>](cchksgfiles-err-enumeration.md)
    
- [<span data-ttu-id="38ccd-129">CChkSGFiles.ErrCheckDbHeaders 函数</span><span class="sxs-lookup"><span data-stu-id="38ccd-129">CChkSGFiles.ErrCheckDbHeaders function</span></span>](cchksgfiles-errcheckdbheaders-function.md)
    
- [<span data-ttu-id="38ccd-130">CChkSGFiles.ErrCheckDbPages 函数</span><span class="sxs-lookup"><span data-stu-id="38ccd-130">CChkSGFiles.ErrCheckDbPages function</span></span>](cchksgfiles-errcheckdbpages-function.md)
    
- [<span data-ttu-id="38ccd-131">CChkSGFiles.ErrCheckLogs 函数</span><span class="sxs-lookup"><span data-stu-id="38ccd-131">CChkSGFiles.ErrCheckLogs function</span></span>](cchksgfiles-errchecklogs-function.md)
    
- [<span data-ttu-id="38ccd-132">CChkSGFiles.ErrGetHeader 函数 （保留）</span><span class="sxs-lookup"><span data-stu-id="38ccd-132">CChkSGFiles.ErrGetHeader function (reserved)</span></span>](cchksgfiles-errgetheader-function-reserved.md)
    
- [<span data-ttu-id="38ccd-133">CChkSGFiles.ErrInit 函数</span><span class="sxs-lookup"><span data-stu-id="38ccd-133">CChkSGFiles.ErrInit function</span></span>](cchksgfiles-errinit-function.md)
    
- [<span data-ttu-id="38ccd-134">CChkSGFiles.ErrTerm 函数</span><span class="sxs-lookup"><span data-stu-id="38ccd-134">CChkSGFiles.ErrTerm function</span></span>](cchksgfiles-errterm-function.md)
    
- [<span data-ttu-id="38ccd-135">CChkSGFiles.iDbInvalid 枚举</span><span class="sxs-lookup"><span data-stu-id="38ccd-135">CChkSGFiles.iDbInvalid enumeration</span></span>](cchksgfiles-idbinvalid-enumeration.md)
    
- [<span data-ttu-id="38ccd-136">CChkSGFiles.New 函数</span><span class="sxs-lookup"><span data-stu-id="38ccd-136">CChkSGFiles.New function</span></span>](cchksgfiles-new-function.md)
    
- [<span data-ttu-id="38ccd-137">CChkSGFiles.NO_FLAGS 枚举</span><span class="sxs-lookup"><span data-stu-id="38ccd-137">CChkSGFiles.NO_FLAGS enumeration</span></span>](cchksgfiles-no_flags-enumeration.md)
    
- [<span data-ttu-id="38ccd-138">CChkSGFiles.PAGE_INFO 结构</span><span class="sxs-lookup"><span data-stu-id="38ccd-138">CChkSGFiles.PAGE_INFO struct</span></span>](cchksgfiles-page_info-struct.md)
    
- [<span data-ttu-id="38ccd-139">CChkSGFiles.PgnoFromFileOffset 函数</span><span class="sxs-lookup"><span data-stu-id="38ccd-139">CChkSGFiles.PgnoFromFileOffset function</span></span>](cchksgfiles-pgnofromfileoffset-function.md)
    
## <a name="see-also"></a><span data-ttu-id="38ccd-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="38ccd-140">See also</span></span>

- [<span data-ttu-id="38ccd-141">Exchange Online 和 Exchange 开发</span><span class="sxs-lookup"><span data-stu-id="38ccd-141">Exchange Online and Exchange development</span></span>](../exchange-server-development.md)
- [<span data-ttu-id="38ccd-142">备份、 还原和灾难恢复</span><span class="sxs-lookup"><span data-stu-id="38ccd-142">Backup, Restore, and Disaster Recovery</span></span>](http://technet.microsoft.com/zh-cn/library/dd876874)
    

