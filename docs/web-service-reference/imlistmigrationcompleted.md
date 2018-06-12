---
title: ImListMigrationCompleted
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6eed9502-5d9e-4345-ba23-3582ff487147
description: ImListMigrationCompleted 元素指示是否在 Exchange 存储包含使用即时消息客户端的即时消息项目。
ms.openlocfilehash: 25f1b583b354a71958fbc8052c492726dc0eb7db
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825893"
---
# <a name="imlistmigrationcompleted"></a><span data-ttu-id="91145-103">ImListMigrationCompleted</span><span class="sxs-lookup"><span data-stu-id="91145-103">ImListMigrationCompleted</span></span>

<span data-ttu-id="91145-104">**ImListMigrationCompleted**元素指示是否在 Exchange 存储包含即时消息使用即时消息客户端的项目。</span><span class="sxs-lookup"><span data-stu-id="91145-104">The **ImListMigrationCompleted** element indicates whether the Exchange store contains the instant messaging items used by instant messaging clients.</span></span> 
  
```XML
<ImListMigrationCompleted>true | false</ImListMigrationCompleted>
```

 <span data-ttu-id="91145-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="91145-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="91145-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="91145-106">Attributes and elements</span></span>

<span data-ttu-id="91145-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="91145-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="91145-108">属性</span><span class="sxs-lookup"><span data-stu-id="91145-108">Attributes</span></span>

<span data-ttu-id="91145-109">无。</span><span class="sxs-lookup"><span data-stu-id="91145-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="91145-110">子元素</span><span class="sxs-lookup"><span data-stu-id="91145-110">Child elements</span></span>

<span data-ttu-id="91145-111">无。</span><span class="sxs-lookup"><span data-stu-id="91145-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="91145-112">父元素</span><span class="sxs-lookup"><span data-stu-id="91145-112">Parent elements</span></span>

[<span data-ttu-id="91145-113">SetImListMigrationCompleted</span><span class="sxs-lookup"><span data-stu-id="91145-113">SetImListMigrationCompleted</span></span>](setimlistmigrationcompleted.md)
  
## <a name="text-value"></a><span data-ttu-id="91145-114">文本值</span><span class="sxs-lookup"><span data-stu-id="91145-114">Text value</span></span>

<span data-ttu-id="91145-115">文本值为**true**的**ImListMigrationCompleted**元素指示存储已迁移到 Exchange 即时消息联系人存储。</span><span class="sxs-lookup"><span data-stu-id="91145-115">A text value of **true** for the **ImListMigrationCompleted** element indicates that the instant messaging contacts store has been migrated to the Exchange store.</span></span> <span data-ttu-id="91145-116">如果值为**false**指示尚未迁移的即时消息联系人存储。</span><span class="sxs-lookup"><span data-stu-id="91145-116">A value of **false** indicates that the instant message contacts store has not been migrated.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="91145-117">备注</span><span class="sxs-lookup"><span data-stu-id="91145-117">Remarks</span></span>

<span data-ttu-id="91145-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="91145-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="91145-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="91145-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="91145-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="91145-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="91145-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="91145-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="91145-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="91145-122">Schema name</span></span>  <br/> |<span data-ttu-id="91145-123">消息架构</span><span class="sxs-lookup"><span data-stu-id="91145-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="91145-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="91145-124">Validation file</span></span>  <br/> |<span data-ttu-id="91145-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="91145-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="91145-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="91145-126">Can be empty</span></span>  <br/> ||
   

