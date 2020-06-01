---
title: ImListMigrationCompleted
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6eed9502-5d9e-4345-ba23-3582ff487147
description: ImListMigrationCompleted 元素指示 Exchange 存储是否包含即时消息客户端使用的即时消息项目。
ms.openlocfilehash: 09f37d6e3663aab7cb98fc922f727ddd604f2acd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456022"
---
# <a name="imlistmigrationcompleted"></a><span data-ttu-id="9fc57-103">ImListMigrationCompleted</span><span class="sxs-lookup"><span data-stu-id="9fc57-103">ImListMigrationCompleted</span></span>

<span data-ttu-id="9fc57-104">**ImListMigrationCompleted**元素指示 Exchange 存储是否包含即时消息客户端使用的即时消息项目。</span><span class="sxs-lookup"><span data-stu-id="9fc57-104">The **ImListMigrationCompleted** element indicates whether the Exchange store contains the instant messaging items used by instant messaging clients.</span></span> 
  
```XML
<ImListMigrationCompleted>true | false</ImListMigrationCompleted>
```

 <span data-ttu-id="9fc57-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="9fc57-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9fc57-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9fc57-106">Attributes and elements</span></span>

<span data-ttu-id="9fc57-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9fc57-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9fc57-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="9fc57-108">Attributes</span></span>

<span data-ttu-id="9fc57-109">无。</span><span class="sxs-lookup"><span data-stu-id="9fc57-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9fc57-110">子元素</span><span class="sxs-lookup"><span data-stu-id="9fc57-110">Child elements</span></span>

<span data-ttu-id="9fc57-111">无。</span><span class="sxs-lookup"><span data-stu-id="9fc57-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9fc57-112">父元素</span><span class="sxs-lookup"><span data-stu-id="9fc57-112">Parent elements</span></span>

[<span data-ttu-id="9fc57-113">SetImListMigrationCompleted</span><span class="sxs-lookup"><span data-stu-id="9fc57-113">SetImListMigrationCompleted</span></span>](setimlistmigrationcompleted.md)
  
## <a name="text-value"></a><span data-ttu-id="9fc57-114">文本值</span><span class="sxs-lookup"><span data-stu-id="9fc57-114">Text value</span></span>

<span data-ttu-id="9fc57-115">如果**ImListMigrationCompleted**元素的文本值为**true** ，则表示即时消息联系人存储已迁移到 Exchange 存储。</span><span class="sxs-lookup"><span data-stu-id="9fc57-115">A text value of **true** for the **ImListMigrationCompleted** element indicates that the instant messaging contacts store has been migrated to the Exchange store.</span></span> <span data-ttu-id="9fc57-116">**如果值为 false** ，则表示即时消息联系人存储尚未迁移。</span><span class="sxs-lookup"><span data-stu-id="9fc57-116">A value of **false** indicates that the instant message contacts store has not been migrated.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9fc57-117">备注</span><span class="sxs-lookup"><span data-stu-id="9fc57-117">Remarks</span></span>

<span data-ttu-id="9fc57-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="9fc57-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="9fc57-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9fc57-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9fc57-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="9fc57-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9fc57-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="9fc57-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9fc57-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="9fc57-122">Schema name</span></span>  <br/> |<span data-ttu-id="9fc57-123">消息架构</span><span class="sxs-lookup"><span data-stu-id="9fc57-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9fc57-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="9fc57-124">Validation file</span></span>  <br/> |<span data-ttu-id="9fc57-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9fc57-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9fc57-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="9fc57-126">Can be empty</span></span>  <br/> ||
   

