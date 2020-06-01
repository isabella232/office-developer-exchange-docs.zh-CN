---
title: SetImListMigrationCompleted
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4b806441-0429-44c4-90b7-1ae5c6ab9128
description: SetImListMigrationCompleted 元素表示一个请求，以指示 Exchange 存储区是否包含即时消息客户端使用的即时消息项目。
ms.openlocfilehash: e5b16044ee72a9e931a2707d3f7823931f8a642a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464824"
---
# <a name="setimlistmigrationcompleted"></a><span data-ttu-id="241fa-103">SetImListMigrationCompleted</span><span class="sxs-lookup"><span data-stu-id="241fa-103">SetImListMigrationCompleted</span></span>

<span data-ttu-id="241fa-104">**SetImListMigrationCompleted**元素表示一个请求，以指示 Exchange 存储区是否包含即时消息客户端使用的即时消息项目。</span><span class="sxs-lookup"><span data-stu-id="241fa-104">The **SetImListMigrationCompleted** element represents a request to indicate whether the Exchange store contains the instant messaging items used by instant messaging clients.</span></span> 
  
```XML
<SetImListMigrationCompleted>
   <ImListMigrationCompleted/>
</SetImListMigrationCompleted>
```

 <span data-ttu-id="241fa-105">**SetImListMigrationCompletedType**</span><span class="sxs-lookup"><span data-stu-id="241fa-105">**SetImListMigrationCompletedType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="241fa-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="241fa-106">Attributes and elements</span></span>

<span data-ttu-id="241fa-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="241fa-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="241fa-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="241fa-108">Attributes</span></span>

<span data-ttu-id="241fa-109">无。</span><span class="sxs-lookup"><span data-stu-id="241fa-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="241fa-110">子元素</span><span class="sxs-lookup"><span data-stu-id="241fa-110">Child elements</span></span>

[<span data-ttu-id="241fa-111">ImListMigrationCompleted</span><span class="sxs-lookup"><span data-stu-id="241fa-111">ImListMigrationCompleted</span></span>](imlistmigrationcompleted.md)
  
### <a name="parent-elements"></a><span data-ttu-id="241fa-112">父元素</span><span class="sxs-lookup"><span data-stu-id="241fa-112">Parent elements</span></span>

<span data-ttu-id="241fa-113">无。</span><span class="sxs-lookup"><span data-stu-id="241fa-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="241fa-114">说明</span><span class="sxs-lookup"><span data-stu-id="241fa-114">Remarks</span></span>

<span data-ttu-id="241fa-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="241fa-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="241fa-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="241fa-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="241fa-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="241fa-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="241fa-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="241fa-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="241fa-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="241fa-119">Schema name</span></span>  <br/> |<span data-ttu-id="241fa-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="241fa-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="241fa-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="241fa-121">Validation file</span></span>  <br/> |<span data-ttu-id="241fa-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="241fa-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="241fa-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="241fa-123">Can be empty</span></span>  <br/> |<span data-ttu-id="241fa-124">false</span><span class="sxs-lookup"><span data-stu-id="241fa-124">false</span></span>  <br/> |
   

