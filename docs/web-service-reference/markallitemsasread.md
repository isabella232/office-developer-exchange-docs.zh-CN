---
title: MarkAllItemsAsRead
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 22244afb-99ec-41b4-8f73-3fbccd56d1ab
description: MarkAllItemsAsRead 元素包含请求标记为已读文件夹中的所有项目。
ms.openlocfilehash: 9d7eb8eb7194cb5d77e909dc08abfb70e2385d56
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826346"
---
# <a name="markallitemsasread"></a><span data-ttu-id="8a2ad-103">MarkAllItemsAsRead</span><span class="sxs-lookup"><span data-stu-id="8a2ad-103">MarkAllItemsAsRead</span></span>

<span data-ttu-id="8a2ad-104">**MarkAllItemsAsRead**元素包含请求标记为已读文件夹中的所有项目。</span><span class="sxs-lookup"><span data-stu-id="8a2ad-104">The **MarkAllItemsAsRead** element contains the request to mark all the items in a folder as read.</span></span> 
  
```XML
<MarkAllItemsAsRead>
   <ReadFlag/>
   <SuppressReadReceipts/>
   <FolderIds/>
</MarkAllItemsAsRead>
```

 <span data-ttu-id="8a2ad-105">**MarkAllItemsAsReadType**</span><span class="sxs-lookup"><span data-stu-id="8a2ad-105">**MarkAllItemsAsReadType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8a2ad-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8a2ad-106">Attributes and elements</span></span>

<span data-ttu-id="8a2ad-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8a2ad-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8a2ad-108">属性</span><span class="sxs-lookup"><span data-stu-id="8a2ad-108">Attributes</span></span>

<span data-ttu-id="8a2ad-109">无。</span><span class="sxs-lookup"><span data-stu-id="8a2ad-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8a2ad-110">子元素</span><span class="sxs-lookup"><span data-stu-id="8a2ad-110">Child elements</span></span>

<span data-ttu-id="8a2ad-111">[ReadFlag](readflag.md) | [SuppressReadReceipts](suppressreadreceipts.md) | [FolderIds](folderids.md)</span><span class="sxs-lookup"><span data-stu-id="8a2ad-111">[ReadFlag](readflag.md) | [SuppressReadReceipts](suppressreadreceipts.md) | [FolderIds](folderids.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8a2ad-112">父元素</span><span class="sxs-lookup"><span data-stu-id="8a2ad-112">Parent elements</span></span>

<span data-ttu-id="8a2ad-113">无。</span><span class="sxs-lookup"><span data-stu-id="8a2ad-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8a2ad-114">备注</span><span class="sxs-lookup"><span data-stu-id="8a2ad-114">Remarks</span></span>

<span data-ttu-id="8a2ad-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="8a2ad-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="8a2ad-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8a2ad-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8a2ad-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="8a2ad-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8a2ad-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="8a2ad-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8a2ad-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="8a2ad-119">Schema name</span></span>  <br/> |<span data-ttu-id="8a2ad-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="8a2ad-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8a2ad-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="8a2ad-121">Validation file</span></span>  <br/> |<span data-ttu-id="8a2ad-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8a2ad-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8a2ad-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="8a2ad-123">Can be empty</span></span>  <br/> ||
   

