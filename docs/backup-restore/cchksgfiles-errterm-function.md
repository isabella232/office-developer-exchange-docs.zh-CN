---
title: CChkSGFiles.ErrTerm 函数
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ErrTerm
api_type:
- dllExport
ms.assetid: eea20a55-4a2a-4209-ae79-dc1ee1cd631b
description: 上次修改时间： 2013 年 2 月 25 日
ms.openlocfilehash: 099ec33663baa2414a0c28b90364523b6191c697
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19752692"
---
# <a name="cchksgfileserrterm-function"></a><span data-ttu-id="a6b29-103">CChkSGFiles.ErrTerm 函数</span><span class="sxs-lookup"><span data-stu-id="a6b29-103">CChkSGFiles.ErrTerm function</span></span>
  
<span data-ttu-id="a6b29-104">**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="a6b29-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="a6b29-105">提供数据库和日志验证，这表明已成功验证是否所有数据库页和日志的总体状态。</span><span class="sxs-lookup"><span data-stu-id="a6b29-105">Provides an overall status of the database and log verification, which indicates whether all the database pages and logs were successfully verified.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="a6b29-106">存储组不可用在 Exchange 2013。</span><span class="sxs-lookup"><span data-stu-id="a6b29-106">Storage groups are not available in Exchange 2013.</span></span> <span data-ttu-id="a6b29-107">与数据库和存储组的 Exchange 版本早于 Exchange Server 2010 中的向后兼容性，CHKSGFILES API 可以指定存储组。</span><span class="sxs-lookup"><span data-stu-id="a6b29-107">For backward compatibility with databases and storage groups in versions of Exchange earlier than Exchange Server 2010, the CHKSGFILES API enables you to specify storage groups.</span></span> <span data-ttu-id="a6b29-108">针对 Exchange 2013 数据库运行 CHKSGFILES 时，您应设置为空字符串的存储组标识符指定的参数。</span><span class="sxs-lookup"><span data-stu-id="a6b29-108">When you run CHKSGFILES against Exchange 2013 databases, you should set parameters that specify a storage group identifier to an empty string.</span></span> 
  
```cs
Vitual ERRErrTerm 
(
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a><span data-ttu-id="a6b29-109">参数</span><span class="sxs-lookup"><span data-stu-id="a6b29-109">Parameters</span></span>

### <a name="ulflags"></a><span data-ttu-id="a6b29-110">ulFlags</span><span class="sxs-lookup"><span data-stu-id="a6b29-110">ulFlags</span></span>
  
<span data-ttu-id="a6b29-111">可选的输入的参数。</span><span class="sxs-lookup"><span data-stu-id="a6b29-111">Optional input parameter.</span></span> <span data-ttu-id="a6b29-112">此值保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="a6b29-112">This value is reserved for future use.</span></span> <span data-ttu-id="a6b29-113">通过此参数传递的值应为 0 （零）。</span><span class="sxs-lookup"><span data-stu-id="a6b29-113">The value passed by this parameter should be 0 (zero).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a6b29-114">返回值</span><span class="sxs-lookup"><span data-stu-id="a6b29-114">Return value</span></span>

<span data-ttu-id="a6b29-115">从[ERR](cchksgfiles-err-enumeration.md)枚举错误代码。</span><span class="sxs-lookup"><span data-stu-id="a6b29-115">An error code from the [ERR](cchksgfiles-err-enumeration.md) enumeration.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a6b29-116">备注</span><span class="sxs-lookup"><span data-stu-id="a6b29-116">Remarks</span></span>

<span data-ttu-id="a6b29-117">**CChkSGFiles**对象确定是否已实际签**ErrInit**函数注册的所有数据库。</span><span class="sxs-lookup"><span data-stu-id="a6b29-117">The **CChkSGFiles** object determines whether all the databases registered with the **ErrInit** function were actually checked.</span></span> <span data-ttu-id="a6b29-118">此对象使用**ErrCheckDbPages**函数以验证相同数量的页面由**ErrCheckDbHeaders**函数实际上已验证的数据库。</span><span class="sxs-lookup"><span data-stu-id="a6b29-118">This object uses the **ErrCheckDbPages** function to verify that the same number of database pages identified by the **ErrCheckDbHeaders** function were actually verified.</span></span> <span data-ttu-id="a6b29-119">如果正确的每个数据库中的页面数不成功进行检查，则**ErrTerm**函数将返回错误。</span><span class="sxs-lookup"><span data-stu-id="a6b29-119">If the correct number of pages in each database are not successfully checked, the **ErrTerm** function returns an error.</span></span> 
  
<span data-ttu-id="a6b29-120">如果数据库网页保持为签与**ErrCheckDbPages**数少于的由**ErrCheckDbHeaders**，此函数在 Windows 事件日志中，创建一条错误，并**ErrTerm**返回错误。</span><span class="sxs-lookup"><span data-stu-id="a6b29-120">If the number of database pages checked with **ErrCheckDbPages** is less than that indicated by **ErrCheckDbHeaders**, this function creates an error in the Windows Event log, and **ErrTerm** returns an error.</span></span> 
  
<span data-ttu-id="a6b29-121">此函数使用**ErrCheckDbPages**检查数据库页面的数量大于**ErrCheckDbHeaders**所指示的如果在 Windows 事件日志，以指示的应用程序可能不必要地检查某些中创建一条警告数据库页多次。</span><span class="sxs-lookup"><span data-stu-id="a6b29-121">If the number of database pages checked with **ErrCheckDbPages** is greater than that indicated by **ErrCheckDbHeaders**, this function creates a warning in the Windows Event log to indicate that the application might be unnecessarily checking some database pages more than once.</span></span> <span data-ttu-id="a6b29-122">在这种情况下，但是， **ErrTerm**函数成功。</span><span class="sxs-lookup"><span data-stu-id="a6b29-122">In this case, however, the **ErrTerm** function succeeds.</span></span> 
  
<span data-ttu-id="a6b29-123">**CChkSGFiles**对象还决定是否已实际签注册**ErrInit**的日志文件。</span><span class="sxs-lookup"><span data-stu-id="a6b29-123">The **CChkSGFiles** object also determines whether the log files registered with **ErrInit** were actually checked.</span></span> <span data-ttu-id="a6b29-124">如果未成功签所有日志， **ErrTerm**函数将返回错误。</span><span class="sxs-lookup"><span data-stu-id="a6b29-124">If not all the logs were successfully checked, the **ErrTerm** function returns an error.</span></span> 
  
<span data-ttu-id="a6b29-125">当**ErrTerm**返回错误时，它将发现的第一个错误，即使它检查**ErrInit**注册的所有数据库的验证状态。</span><span class="sxs-lookup"><span data-stu-id="a6b29-125">When **ErrTerm** returns an error, it will be the first error it finds, even though it checks the verification status for all databases registered with **ErrInit**.</span></span>
  
<span data-ttu-id="a6b29-126">如果您使用 CHKSGFILES 多线程应用程序中，您必须将应用程序的单线程部分调用**ErrTerm**函数且您可以调用它不能超过一次为每个**CCheckSGFiles**对象。</span><span class="sxs-lookup"><span data-stu-id="a6b29-126">If you're using CHKSGFILES in a multithreaded application, you must call the **ErrTerm** function in the single-threaded portion of the application, and you can call it no more than once for each **CCheckSGFiles** object.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="a6b29-127">要求</span><span class="sxs-lookup"><span data-stu-id="a6b29-127">Requirements</span></span>

<span data-ttu-id="a6b29-128">Exchange 2013 只包括 CHKSGFILES 的 64 位版本。</span><span class="sxs-lookup"><span data-stu-id="a6b29-128">Exchange 2013 only includes a 64-bit version of CHKSGFILES.</span></span>
  
<span data-ttu-id="a6b29-129">下运行该应用程序的帐户必须具有对要检查的数据库和日志文件的读取访问权限。</span><span class="sxs-lookup"><span data-stu-id="a6b29-129">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

