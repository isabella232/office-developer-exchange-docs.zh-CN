---
title: MarkAllItemsAsRead
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 22244afb-99ec-41b4-8f73-3fbccd56d1ab
description: MarkAllItemsAsRead 元素包含将文件夹中的所有项目标记为已读的请求。
ms.openlocfilehash: 0338b2a1eed503b7e8fb0ec8b4a8ebcf12b6dbd6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530886"
---
# <a name="markallitemsasread"></a><span data-ttu-id="1ea75-103">MarkAllItemsAsRead</span><span class="sxs-lookup"><span data-stu-id="1ea75-103">MarkAllItemsAsRead</span></span>

<span data-ttu-id="1ea75-104">**MarkAllItemsAsRead**元素包含将文件夹中的所有项目标记为已读的请求。</span><span class="sxs-lookup"><span data-stu-id="1ea75-104">The **MarkAllItemsAsRead** element contains the request to mark all the items in a folder as read.</span></span> 
  
```XML
<MarkAllItemsAsRead>
   <ReadFlag/>
   <SuppressReadReceipts/>
   <FolderIds/>
</MarkAllItemsAsRead>
```

 <span data-ttu-id="1ea75-105">**MarkAllItemsAsReadType**</span><span class="sxs-lookup"><span data-stu-id="1ea75-105">**MarkAllItemsAsReadType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1ea75-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1ea75-106">Attributes and elements</span></span>

<span data-ttu-id="1ea75-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1ea75-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1ea75-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="1ea75-108">Attributes</span></span>

<span data-ttu-id="1ea75-109">无。</span><span class="sxs-lookup"><span data-stu-id="1ea75-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1ea75-110">子元素</span><span class="sxs-lookup"><span data-stu-id="1ea75-110">Child elements</span></span>

<span data-ttu-id="1ea75-111">[ReadFlag](readflag.md)  | [SuppressReadReceipts](suppressreadreceipts.md)  | [FolderIds](folderids.md)</span><span class="sxs-lookup"><span data-stu-id="1ea75-111">[ReadFlag](readflag.md) | [SuppressReadReceipts](suppressreadreceipts.md) | [FolderIds](folderids.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1ea75-112">父元素</span><span class="sxs-lookup"><span data-stu-id="1ea75-112">Parent elements</span></span>

<span data-ttu-id="1ea75-113">无。</span><span class="sxs-lookup"><span data-stu-id="1ea75-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1ea75-114">说明</span><span class="sxs-lookup"><span data-stu-id="1ea75-114">Remarks</span></span>

<span data-ttu-id="1ea75-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="1ea75-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="1ea75-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1ea75-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1ea75-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="1ea75-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1ea75-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="1ea75-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1ea75-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="1ea75-119">Schema name</span></span>  <br/> |<span data-ttu-id="1ea75-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="1ea75-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1ea75-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="1ea75-121">Validation file</span></span>  <br/> |<span data-ttu-id="1ea75-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1ea75-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1ea75-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="1ea75-123">Can be empty</span></span>  <br/> ||
   

