---
title: CChkSGFiles.CMaxDbPerSG 函数
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CMaxDbPerSG
api_type:
- dllExport
ms.assetid: 5871988b-a5d7-42cc-9b83-8fededb5072f
description: 上次修改时间： 2013 年 2 月 22 日
ms.openlocfilehash: bf09074bab6dee13e97e8a59a22ae1b19522a5e5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753650"
---
# <a name="cchksgfilescmaxdbpersg-function"></a><span data-ttu-id="0a831-103">CChkSGFiles.CMaxDbPerSG 函数</span><span class="sxs-lookup"><span data-stu-id="0a831-103">CChkSGFiles.CMaxDbPerSG function</span></span>

<span data-ttu-id="0a831-104">**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="0a831-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="0a831-105">返回数据库中一个 Exchange 服务器存储组允许的最大数目。</span><span class="sxs-lookup"><span data-stu-id="0a831-105">Returns the maximum number of databases allowed in a single Exchange server storage group.</span></span>
  
```cs
Static ULONG  __stdcall CMaxDbPerSG  ();

```

## <a name="parameters"></a><span data-ttu-id="0a831-106">参数</span><span class="sxs-lookup"><span data-stu-id="0a831-106">Parameters</span></span>

<span data-ttu-id="0a831-107">无。</span><span class="sxs-lookup"><span data-stu-id="0a831-107">None.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="0a831-108">返回值</span><span class="sxs-lookup"><span data-stu-id="0a831-108">Return value</span></span>

<span data-ttu-id="0a831-109">指定的 Exchange 服务器允许每个存储组的数据库的最大数目。</span><span class="sxs-lookup"><span data-stu-id="0a831-109">The maximum number of databases that the specified Exchange server allows per storage group.</span></span> <span data-ttu-id="0a831-110">由于存储组不是 Exchange 2013 的一部分，此函数返回 1。</span><span class="sxs-lookup"><span data-stu-id="0a831-110">Because storage groups are not part of Exchange 2013, this function returns 1.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0a831-111">注解</span><span class="sxs-lookup"><span data-stu-id="0a831-111">Remarks</span></span>

<span data-ttu-id="0a831-112">您可以使用**CCheckSGFiles**对象，由**CMaxDbPerSG**函数返回的值还代表您可以通过使用检查的数据库的最大数目，以便只有一个存储组中，验证数据库 （和事务日志文件）**CCheckSGFiles**类的实例。</span><span class="sxs-lookup"><span data-stu-id="0a831-112">You can use the **CCheckSGFiles** object to validate databases (and transaction log files) in only one storage group, so the value returned by the **CMaxDbPerSG** function also represents the maximum number of databases that you can check by using an instance of the **CCheckSGFiles** class.</span></span> 
  
<span data-ttu-id="0a831-113">请注意，默认情况下，Exchange Server 2003 和 Exchange Server 2007 允许每个存储组的五个数据库的最大值。</span><span class="sxs-lookup"><span data-stu-id="0a831-113">Note that by default, Exchange Server 2003 and Exchange Server 2007 allow a maximum of five databases per storage group.</span></span>
  
## <a name="requirements"></a><span data-ttu-id="0a831-114">要求</span><span class="sxs-lookup"><span data-stu-id="0a831-114">Requirements</span></span>

<span data-ttu-id="0a831-115">Exchange 2013 只包括 CHKSGFILES API 的 64 位版本。</span><span class="sxs-lookup"><span data-stu-id="0a831-115">Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="0a831-116">下运行该应用程序的帐户必须具有对要检查的数据库和日志文件的读取访问权限。</span><span class="sxs-lookup"><span data-stu-id="0a831-116">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

