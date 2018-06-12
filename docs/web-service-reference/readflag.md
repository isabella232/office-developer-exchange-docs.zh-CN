---
title: ReadFlag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9d91aa89-9f9f-4877-846d-aaf48bbeec7c
description: ReadFlag 元素指示要在文件夹中的项目上设置的读取的状态。
ms.openlocfilehash: f3156a51fbdd3372dd28f2065499d26a50b3d497
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826954"
---
# <a name="readflag"></a><span data-ttu-id="a0fe3-103">ReadFlag</span><span class="sxs-lookup"><span data-stu-id="a0fe3-103">ReadFlag</span></span>

<span data-ttu-id="a0fe3-104">**ReadFlag**元素指示要在文件夹中的项目上设置的读取的状态。</span><span class="sxs-lookup"><span data-stu-id="a0fe3-104">The **ReadFlag** element indicates the read state to set on items in a folder.</span></span> 
  
```XML
<ReadFlag>true | false</ReadFlag>
```

 <span data-ttu-id="a0fe3-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="a0fe3-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a0fe3-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a0fe3-106">Attributes and elements</span></span>

<span data-ttu-id="a0fe3-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a0fe3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a0fe3-108">属性</span><span class="sxs-lookup"><span data-stu-id="a0fe3-108">Attributes</span></span>

<span data-ttu-id="a0fe3-109">无。</span><span class="sxs-lookup"><span data-stu-id="a0fe3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a0fe3-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a0fe3-110">Child elements</span></span>

<span data-ttu-id="a0fe3-111">无。</span><span class="sxs-lookup"><span data-stu-id="a0fe3-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a0fe3-112">父元素</span><span class="sxs-lookup"><span data-stu-id="a0fe3-112">Parent elements</span></span>

[<span data-ttu-id="a0fe3-113">MarkAllItemsAsRead</span><span class="sxs-lookup"><span data-stu-id="a0fe3-113">MarkAllItemsAsRead</span></span>](markallitemsasread.md)
  
## <a name="text-value"></a><span data-ttu-id="a0fe3-114">文本值</span><span class="sxs-lookup"><span data-stu-id="a0fe3-114">Text value</span></span>

<span data-ttu-id="a0fe3-115">文本值为**true**的**ReadFlag**元素指示文件夹中的项目将被标记为只读。</span><span class="sxs-lookup"><span data-stu-id="a0fe3-115">A text value of **true** for the **ReadFlag** element indicates that the items in the folder will be marked as read.</span></span> <span data-ttu-id="a0fe3-116">如果值为**false**指示文件夹中的项目将被标记为未读。</span><span class="sxs-lookup"><span data-stu-id="a0fe3-116">A value of **false** indicates that the items in the folder will be marked as unread.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a0fe3-117">备注</span><span class="sxs-lookup"><span data-stu-id="a0fe3-117">Remarks</span></span>

<span data-ttu-id="a0fe3-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="a0fe3-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a0fe3-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a0fe3-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a0fe3-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="a0fe3-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a0fe3-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="a0fe3-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a0fe3-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="a0fe3-122">Schema name</span></span>  <br/> |<span data-ttu-id="a0fe3-123">消息架构</span><span class="sxs-lookup"><span data-stu-id="a0fe3-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a0fe3-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="a0fe3-124">Validation file</span></span>  <br/> |<span data-ttu-id="a0fe3-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a0fe3-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a0fe3-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="a0fe3-126">Can be empty</span></span>  <br/> ||
   

