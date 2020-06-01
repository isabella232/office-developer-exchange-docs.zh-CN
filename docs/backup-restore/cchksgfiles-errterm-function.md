---
title: CChkSGFiles 函数
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
description: 上次修改时间：2013年2月25日
ms.openlocfilehash: 12b07fba69054d327c7250bbf83e4c77016e8b3f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466197"
---
# <a name="cchksgfileserrterm-function"></a><span data-ttu-id="3ea7f-103">CChkSGFiles 函数</span><span class="sxs-lookup"><span data-stu-id="3ea7f-103">CChkSGFiles.ErrTerm function</span></span>
  
<span data-ttu-id="3ea7f-104">**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="3ea7f-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="3ea7f-105">提供数据库和日志验证的总体状态，以指示是否已成功验证所有数据库页和日志。</span><span class="sxs-lookup"><span data-stu-id="3ea7f-105">Provides an overall status of the database and log verification, which indicates whether all the database pages and logs were successfully verified.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="3ea7f-106">存储组在 Exchange 2013 中不可用。</span><span class="sxs-lookup"><span data-stu-id="3ea7f-106">Storage groups are not available in Exchange 2013.</span></span> <span data-ttu-id="3ea7f-107">为了在 exchange Server 2010 之前的 Exchange 版本中与数据库和存储组保持向后兼容性，CHKSGFILES API 使您能够指定存储组。</span><span class="sxs-lookup"><span data-stu-id="3ea7f-107">For backward compatibility with databases and storage groups in versions of Exchange earlier than Exchange Server 2010, the CHKSGFILES API enables you to specify storage groups.</span></span> <span data-ttu-id="3ea7f-108">当您针对 Exchange 2013 数据库运行 CHKSGFILES 时，应将指定存储组标识符的参数设置为空字符串。</span><span class="sxs-lookup"><span data-stu-id="3ea7f-108">When you run CHKSGFILES against Exchange 2013 databases, you should set parameters that specify a storage group identifier to an empty string.</span></span> 
  
```cs
Vitual ERRErrTerm 
(
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a><span data-ttu-id="3ea7f-109">参数</span><span class="sxs-lookup"><span data-stu-id="3ea7f-109">Parameters</span></span>

### <a name="ulflags"></a><span data-ttu-id="3ea7f-110">ulFlags</span><span class="sxs-lookup"><span data-stu-id="3ea7f-110">ulFlags</span></span>
  
<span data-ttu-id="3ea7f-111">可选的输入参数。</span><span class="sxs-lookup"><span data-stu-id="3ea7f-111">Optional input parameter.</span></span> <span data-ttu-id="3ea7f-112">保留此值以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="3ea7f-112">This value is reserved for future use.</span></span> <span data-ttu-id="3ea7f-113">此参数传递的值应为0（零）。</span><span class="sxs-lookup"><span data-stu-id="3ea7f-113">The value passed by this parameter should be 0 (zero).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3ea7f-114">返回值</span><span class="sxs-lookup"><span data-stu-id="3ea7f-114">Return value</span></span>

<span data-ttu-id="3ea7f-115">[ERR](cchksgfiles-err-enumeration.md)枚举中的错误代码。</span><span class="sxs-lookup"><span data-stu-id="3ea7f-115">An error code from the [ERR](cchksgfiles-err-enumeration.md) enumeration.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3ea7f-116">备注</span><span class="sxs-lookup"><span data-stu-id="3ea7f-116">Remarks</span></span>

<span data-ttu-id="3ea7f-117">**CChkSGFiles**对象确定是否实际检查了使用**ErrInit**函数注册的所有数据库。</span><span class="sxs-lookup"><span data-stu-id="3ea7f-117">The **CChkSGFiles** object determines whether all the databases registered with the **ErrInit** function were actually checked.</span></span> <span data-ttu-id="3ea7f-118">此对象使用**ErrCheckDbPages**函数验证是否实际验证了**ErrCheckDbHeaders**函数所标识的相同数量的数据库页。</span><span class="sxs-lookup"><span data-stu-id="3ea7f-118">This object uses the **ErrCheckDbPages** function to verify that the same number of database pages identified by the **ErrCheckDbHeaders** function were actually verified.</span></span> <span data-ttu-id="3ea7f-119">如果未成功检查每个数据库中的正确数量的页面， **ErrTerm**函数将返回一个错误。</span><span class="sxs-lookup"><span data-stu-id="3ea7f-119">If the correct number of pages in each database are not successfully checked, the **ErrTerm** function returns an error.</span></span> 
  
<span data-ttu-id="3ea7f-120">如果使用**ErrCheckDbPages**选中的数据库页面的数量小于**ErrCheckDbHeaders**所指示的数目，则此函数会在 Windows 事件日志中创建一个错误， **ErrTerm**将返回错误。</span><span class="sxs-lookup"><span data-stu-id="3ea7f-120">If the number of database pages checked with **ErrCheckDbPages** is less than that indicated by **ErrCheckDbHeaders**, this function creates an error in the Windows Event log, and **ErrTerm** returns an error.</span></span> 
  
<span data-ttu-id="3ea7f-121">如果使用**ErrCheckDbPages**检查的数据库页面的数量大于**ErrCheckDbHeaders**所指示的数目，则此函数会在 Windows 事件日志中创建一个警告，以指示该应用程序可能不需要多次检查某些数据库页。</span><span class="sxs-lookup"><span data-stu-id="3ea7f-121">If the number of database pages checked with **ErrCheckDbPages** is greater than that indicated by **ErrCheckDbHeaders**, this function creates a warning in the Windows Event log to indicate that the application might be unnecessarily checking some database pages more than once.</span></span> <span data-ttu-id="3ea7f-122">但在这种情况下， **ErrTerm**函数将成功。</span><span class="sxs-lookup"><span data-stu-id="3ea7f-122">In this case, however, the **ErrTerm** function succeeds.</span></span> 
  
<span data-ttu-id="3ea7f-123">**CChkSGFiles**对象还确定是否实际检查了在**ErrInit**中注册的日志文件。</span><span class="sxs-lookup"><span data-stu-id="3ea7f-123">The **CChkSGFiles** object also determines whether the log files registered with **ErrInit** were actually checked.</span></span> <span data-ttu-id="3ea7f-124">如果未成功检查所有日志， **ErrTerm**函数将返回一个错误。</span><span class="sxs-lookup"><span data-stu-id="3ea7f-124">If not all the logs were successfully checked, the **ErrTerm** function returns an error.</span></span> 
  
<span data-ttu-id="3ea7f-125">当**ErrTerm**返回错误时，它将是它找到的第一个错误，即使它检查所有注册到**ErrInit**的数据库的验证状态。</span><span class="sxs-lookup"><span data-stu-id="3ea7f-125">When **ErrTerm** returns an error, it will be the first error it finds, even though it checks the verification status for all databases registered with **ErrInit**.</span></span>
  
<span data-ttu-id="3ea7f-126">如果要在多线程应用程序中使用 CHKSGFILES，则必须在应用程序的单线程部分调用**ErrTerm**函数，并且对于每个**CCheckSGFiles**对象，您可以调用该函数，而不能超过一次。</span><span class="sxs-lookup"><span data-stu-id="3ea7f-126">If you're using CHKSGFILES in a multithreaded application, you must call the **ErrTerm** function in the single-threaded portion of the application, and you can call it no more than once for each **CCheckSGFiles** object.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="3ea7f-127">Requirements</span><span class="sxs-lookup"><span data-stu-id="3ea7f-127">Requirements</span></span>

<span data-ttu-id="3ea7f-128">Exchange 2013 仅包含64位版本的 CHKSGFILES。</span><span class="sxs-lookup"><span data-stu-id="3ea7f-128">Exchange 2013 only includes a 64-bit version of CHKSGFILES.</span></span>
  
<span data-ttu-id="3ea7f-129">运行应用程序所使用的帐户必须具有对要检查的数据库和日志文件的读取访问权限。</span><span class="sxs-lookup"><span data-stu-id="3ea7f-129">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

