---
title: CChkSGFiles 函数
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
description: 上次修改时间：2013年2月22日
ms.openlocfilehash: 38cb72b42727855f652de607bb2a02ecdeaae16e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44447048"
---
# <a name="cchksgfilesdelete-function"></a><span data-ttu-id="efe69-103">CChkSGFiles 函数</span><span class="sxs-lookup"><span data-stu-id="efe69-103">CChkSGFiles.Delete function</span></span>

<span data-ttu-id="efe69-104">**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="efe69-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="efe69-105">销毁**CChkSGFiles**类的现有实例。</span><span class="sxs-lookup"><span data-stu-id="efe69-105">Destroys an existing instance of the **CChkSGFiles** class.</span></span> <span data-ttu-id="efe69-106">在应用程序完成对指定对象的操作后，必须调用此函数。</span><span class="sxs-lookup"><span data-stu-id="efe69-106">You must call this function after the application has finished working with the specified object.</span></span> 
  
```cs
Static VOID __stdcall Delete 
(
        CCheckSGFiles  * pcchecksgfiles
);

```

## <a name="parameters"></a><span data-ttu-id="efe69-107">参数</span><span class="sxs-lookup"><span data-stu-id="efe69-107">Parameters</span></span>

### <a name="pcchecksgfiles"></a><span data-ttu-id="efe69-108">pcchecksgfiles</span><span class="sxs-lookup"><span data-stu-id="efe69-108">pcchecksgfiles</span></span> 
  
<span data-ttu-id="efe69-109">输入参数。</span><span class="sxs-lookup"><span data-stu-id="efe69-109">Input parameter.</span></span> <span data-ttu-id="efe69-110">指向现有**CCheckSGFiles**对象的指针。</span><span class="sxs-lookup"><span data-stu-id="efe69-110">A pointer to an existing **CCheckSGFiles** object.</span></span> <span data-ttu-id="efe69-111">然后，将释放与该对象关联的内存。</span><span class="sxs-lookup"><span data-stu-id="efe69-111">The memory associated with the object will then be freed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="efe69-112">返回值</span><span class="sxs-lookup"><span data-stu-id="efe69-112">Return value</span></span>

<span data-ttu-id="efe69-113">无。</span><span class="sxs-lookup"><span data-stu-id="efe69-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="efe69-114">说明</span><span class="sxs-lookup"><span data-stu-id="efe69-114">Remarks</span></span>

<span data-ttu-id="efe69-115">**Delete**函数释放与**CCheckSGFiles**对象相关联的内存。</span><span class="sxs-lookup"><span data-stu-id="efe69-115">The **Delete** function frees the memory associated with the **CCheckSGFiles** object.</span></span> <span data-ttu-id="efe69-116">调用**Delete**后，在*pcchecksgfiles*参数中传递的指针将无效，并且无法对该对象执行其他操作。</span><span class="sxs-lookup"><span data-stu-id="efe69-116">After you call **Delete**, the pointer passed in the  *pcchecksgfiles*  parameter will be invalid and no other operations can be performed on that object.</span></span> 
  
<span data-ttu-id="efe69-117">如果应用程序使用**ErrCheckDbPages**函数，应用程序必须手动释放内存缓冲区;**删除**函数将无法释放它。</span><span class="sxs-lookup"><span data-stu-id="efe69-117">If the application uses the **ErrCheckDbPages** function, the application must free the memory buffer manually; the **Delete** function will not free it.</span></span> 
  
<span data-ttu-id="efe69-118">如果要在多线程应用程序中使用 CHKSGFILES，则必须在应用程序的单线程部分调用 Delete 函数，并且只能为每个**CCheckSGFiles**对象调用一次**Delete**函数。</span><span class="sxs-lookup"><span data-stu-id="efe69-118">If you're using CHKSGFILES in a multithreaded application, you must call the **Delete** function in the single-threaded portion of the application, and you can call it only once for each **CCheckSGFiles** object.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="efe69-119">Requirements</span><span class="sxs-lookup"><span data-stu-id="efe69-119">Requirements</span></span>

<span data-ttu-id="efe69-120">Exchange 2013 仅包含64位版本的 CHKSGFILES API。</span><span class="sxs-lookup"><span data-stu-id="efe69-120">Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="efe69-121">运行应用程序所使用的帐户必须具有对要检查的数据库和日志文件的读取访问权限。</span><span class="sxs-lookup"><span data-stu-id="efe69-121">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

