---
title: CChkSGFiles 函数
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
description: 上次修改时间：2013年2月22日
ms.openlocfilehash: b7c3517779eb07ef053c1dd4fa25544310fb3343
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455259"
---
# <a name="cchksgfilescmaxdbpersg-function"></a><span data-ttu-id="90d69-103">CChkSGFiles 函数</span><span class="sxs-lookup"><span data-stu-id="90d69-103">CChkSGFiles.CMaxDbPerSG function</span></span>

<span data-ttu-id="90d69-104">**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="90d69-104">**Applies to:** Exchange Server 2003 | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013</span></span>
  
<span data-ttu-id="90d69-105">返回单个 Exchange server 存储组中允许的最大数据库数。</span><span class="sxs-lookup"><span data-stu-id="90d69-105">Returns the maximum number of databases allowed in a single Exchange server storage group.</span></span>
  
```cs
Static ULONG  __stdcall CMaxDbPerSG  ();

```

## <a name="parameters"></a><span data-ttu-id="90d69-106">参数</span><span class="sxs-lookup"><span data-stu-id="90d69-106">Parameters</span></span>

<span data-ttu-id="90d69-107">无。</span><span class="sxs-lookup"><span data-stu-id="90d69-107">None.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="90d69-108">返回值</span><span class="sxs-lookup"><span data-stu-id="90d69-108">Return value</span></span>

<span data-ttu-id="90d69-109">指定的 Exchange 服务器允许每个存储组的最大数据库数。</span><span class="sxs-lookup"><span data-stu-id="90d69-109">The maximum number of databases that the specified Exchange server allows per storage group.</span></span> <span data-ttu-id="90d69-110">因为存储组不是 Exchange 2013 的一部分，所以此函数返回1。</span><span class="sxs-lookup"><span data-stu-id="90d69-110">Because storage groups are not part of Exchange 2013, this function returns 1.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="90d69-111">备注</span><span class="sxs-lookup"><span data-stu-id="90d69-111">Remarks</span></span>

<span data-ttu-id="90d69-112">您可以使用**CCheckSGFiles**对象来验证仅在一个存储组中的数据库（和事务日志文件），因此**CMaxDbPerSG**函数返回的值还表示您可以使用**CCheckSGFiles**类的实例进行检查的数据库的最大数量。</span><span class="sxs-lookup"><span data-stu-id="90d69-112">You can use the **CCheckSGFiles** object to validate databases (and transaction log files) in only one storage group, so the value returned by the **CMaxDbPerSG** function also represents the maximum number of databases that you can check by using an instance of the **CCheckSGFiles** class.</span></span> 
  
<span data-ttu-id="90d69-113">请注意，默认情况下，Exchange Server 2003 和 Exchange Server 2007 允许每个存储组最多5个数据库。</span><span class="sxs-lookup"><span data-stu-id="90d69-113">Note that by default, Exchange Server 2003 and Exchange Server 2007 allow a maximum of five databases per storage group.</span></span>
  
## <a name="requirements"></a><span data-ttu-id="90d69-114">Requirements</span><span class="sxs-lookup"><span data-stu-id="90d69-114">Requirements</span></span>

<span data-ttu-id="90d69-115">Exchange 2013 仅包含64位版本的 CHKSGFILES API。</span><span class="sxs-lookup"><span data-stu-id="90d69-115">Exchange 2013 only includes a 64-bit version of the CHKSGFILES API.</span></span>
  
<span data-ttu-id="90d69-116">运行应用程序所使用的帐户必须具有对要检查的数据库和日志文件的读取访问权限。</span><span class="sxs-lookup"><span data-stu-id="90d69-116">The account that the application is running under must have read access permissions to the database and log files that are to be checked.</span></span>
  

