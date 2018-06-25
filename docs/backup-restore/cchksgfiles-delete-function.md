---
title: CChkSGFiles.Delete 函数
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Delete
api_type:
- dllExport
ms.assetid: 869e927f-7df2-4247-88ef-b8b05b29a700
description: 上次修改时间： 2013 年 2 月 22 日
ms.openlocfilehash: 5c41007a797e5a256692b2c4bdcb3cfae82c12ab
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752688"
---
# <a name="cchksgfilesdelete-function"></a><span data-ttu-id="8ae7a-103">CChkSGFiles.Delete 函数</span><span class="sxs-lookup"><span data-stu-id="8ae7a-103">CChkSGFiles.Delete function</span></span>

<span data-ttu-id="8ae7a-104">**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="8ae7a-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="8ae7a-105">销毁现有**CChkSGFiles**类的实例。</span><span class="sxs-lookup"><span data-stu-id="8ae7a-105">Destroys an existing instance of the **CChkSGFiles** class.</span></span> <span data-ttu-id="8ae7a-106">应用程序已完成使用指定的对象后，必须调用此函数。</span><span class="sxs-lookup"><span data-stu-id="8ae7a-106">You must call this function after the application has finished working with the specified object.</span></span> 
  
```cs
Static VOID __stdcall Delete 
(
        CCheckSGFiles  * pcchecksgfiles
);

```

## <a name="parameters"></a><span data-ttu-id="8ae7a-107">参数</span><span class="sxs-lookup"><span data-stu-id="8ae7a-107">Parameters</span></span>

### <a name="pcchecksgfiles"></a><span data-ttu-id="8ae7a-108">pcchecksgfiles</span><span class="sxs-lookup"><span data-stu-id="8ae7a-108">pcchecksgfiles</span></span> 
  
<span data-ttu-id="8ae7a-109">输入的参数。</span><span class="sxs-lookup"><span data-stu-id="8ae7a-109">Input parameter.</span></span> <span data-ttu-id="8ae7a-110">指向现有**CCheckSGFiles**对象的指针。</span><span class="sxs-lookup"><span data-stu-id="8ae7a-110">A pointer to an existing **CCheckSGFiles** object.</span></span> <span data-ttu-id="8ae7a-111">将然后释放与对象关联的内存。</span><span class="sxs-lookup"><span data-stu-id="8ae7a-111">The memory associated with the object will then be freed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8ae7a-112">返回值</span><span class="sxs-lookup"><span data-stu-id="8ae7a-112">Return value</span></span>

<span data-ttu-id="8ae7a-113">无。</span><span class="sxs-lookup"><span data-stu-id="8ae7a-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8ae7a-114">注解</span><span class="sxs-lookup"><span data-stu-id="8ae7a-114">Remarks</span></span>

<span data-ttu-id="8ae7a-115">**删除**函数释放与**CCheckSGFiles**对象关联的内存。</span><span class="sxs-lookup"><span data-stu-id="8ae7a-115">The **Delete** function frees the memory associated with the **CCheckSGFiles** object.</span></span> <span data-ttu-id="8ae7a-116">您调用**删除**后，将无效*pcchecksgfiles*参数中传递的指针，可以对该对象执行任何其他操作。</span><span class="sxs-lookup"><span data-stu-id="8ae7a-116">After you call **Delete**, the pointer passed in the  *pcchecksgfiles*  parameter will be invalid and no other operations can be performed on that object.</span></span> 
  
<span data-ttu-id="8ae7a-117">应用程序的应用程序使用**ErrCheckDbPages**函数，如果必须手动; 释放内存缓冲区**删除**函数不将其释放。</span><span class="sxs-lookup"><span data-stu-id="8ae7a-117">If the application uses the **ErrCheckDbPages** function, the application must free the memory buffer manually; the **Delete** function will not free it.</span></span> 
  
<span data-ttu-id="8ae7a-118">如果您使用 CHKSGFILES 多线程应用程序中，必须**删除**函数调用的应用程序的单线程部分中，且您可以为每个**CCheckSGFiles**对象调用它仅执行一次。</span><span class="sxs-lookup"><span data-stu-id="8ae7a-118">If you're using CHKSGFILES in a multithreaded application, you must call the **Delete** function in the single-threaded portion of the application, and you can call it only once for each **CCheckSGFiles** object.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="8ae7a-119">要求</span><span class="sxs-lookup"><span data-stu-id="8ae7a-119">Requirements</span></span>

<span data-ttu-id="8ae7a-120">Exchange 2013 只包括 CHKSGFILES API 的 64 位版本。</span><span class="sxs-lookup"><span data-stu-id="8ae7a-120">Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="8ae7a-121">下运行该应用程序的帐户必须具有对要检查的数据库和日志文件的读取访问权限。</span><span class="sxs-lookup"><span data-stu-id="8ae7a-121">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

