---
title: ReadFlag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9d91aa89-9f9f-4877-846d-aaf48bbeec7c
description: ReadFlag 元素指示要对文件夹中的项目设置的读取状态。
ms.openlocfilehash: 1d3b9f3fe199ed2e63bdb632135120a5f89f4d1f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529894"
---
# <a name="readflag"></a><span data-ttu-id="8a4ee-103">ReadFlag</span><span class="sxs-lookup"><span data-stu-id="8a4ee-103">ReadFlag</span></span>

<span data-ttu-id="8a4ee-104">**ReadFlag**元素指示要对文件夹中的项目设置的读取状态。</span><span class="sxs-lookup"><span data-stu-id="8a4ee-104">The **ReadFlag** element indicates the read state to set on items in a folder.</span></span> 
  
```XML
<ReadFlag>true | false</ReadFlag>
```

 <span data-ttu-id="8a4ee-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="8a4ee-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8a4ee-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8a4ee-106">Attributes and elements</span></span>

<span data-ttu-id="8a4ee-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8a4ee-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8a4ee-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="8a4ee-108">Attributes</span></span>

<span data-ttu-id="8a4ee-109">无。</span><span class="sxs-lookup"><span data-stu-id="8a4ee-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8a4ee-110">子元素</span><span class="sxs-lookup"><span data-stu-id="8a4ee-110">Child elements</span></span>

<span data-ttu-id="8a4ee-111">无。</span><span class="sxs-lookup"><span data-stu-id="8a4ee-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8a4ee-112">父元素</span><span class="sxs-lookup"><span data-stu-id="8a4ee-112">Parent elements</span></span>

[<span data-ttu-id="8a4ee-113">MarkAllItemsAsRead</span><span class="sxs-lookup"><span data-stu-id="8a4ee-113">MarkAllItemsAsRead</span></span>](markallitemsasread.md)
  
## <a name="text-value"></a><span data-ttu-id="8a4ee-114">文本值</span><span class="sxs-lookup"><span data-stu-id="8a4ee-114">Text value</span></span>

<span data-ttu-id="8a4ee-115">如果**ReadFlag**元素的文本值为**true** ，则表示该文件夹中的项目将被标记为已读。</span><span class="sxs-lookup"><span data-stu-id="8a4ee-115">A text value of **true** for the **ReadFlag** element indicates that the items in the folder will be marked as read.</span></span> <span data-ttu-id="8a4ee-116">如果值为**false** ，则表示文件夹中的项目将被标记为未读。</span><span class="sxs-lookup"><span data-stu-id="8a4ee-116">A value of **false** indicates that the items in the folder will be marked as unread.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8a4ee-117">备注</span><span class="sxs-lookup"><span data-stu-id="8a4ee-117">Remarks</span></span>

<span data-ttu-id="8a4ee-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="8a4ee-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="8a4ee-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8a4ee-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8a4ee-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="8a4ee-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8a4ee-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="8a4ee-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8a4ee-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="8a4ee-122">Schema name</span></span>  <br/> |<span data-ttu-id="8a4ee-123">消息架构</span><span class="sxs-lookup"><span data-stu-id="8a4ee-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8a4ee-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="8a4ee-124">Validation file</span></span>  <br/> |<span data-ttu-id="8a4ee-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8a4ee-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8a4ee-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="8a4ee-126">Can be empty</span></span>  <br/> ||
   

