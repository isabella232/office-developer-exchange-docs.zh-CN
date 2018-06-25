---
title: MarkAsJunk
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f06bafc6-7ee3-4b2b-9fd1-7c51328f4729
description: MarkAsJunk 元素指定的请求将项目移动到垃圾邮件文件夹并将发件人添加到阻止发件人列表。
ms.openlocfilehash: fbb3eee7ce350954888931ca55b27f596656b161
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826350"
---
# <a name="markasjunk"></a><span data-ttu-id="e6374-103">MarkAsJunk</span><span class="sxs-lookup"><span data-stu-id="e6374-103">MarkAsJunk</span></span>

<span data-ttu-id="e6374-104">**MarkAsJunk**元素指定的请求将项目移动到垃圾邮件文件夹并将发件人添加到阻止发件人列表。</span><span class="sxs-lookup"><span data-stu-id="e6374-104">The **MarkAsJunk** element specifies the request to move an item to the junk mail folder and to add the sender to the blocked sender list.</span></span> 
  
```XML
<MarkAsJunk IsJunk="true | false" MoveItem="true | false">
   <ItemIds/>
</MarkAsJunk>
```

 <span data-ttu-id="e6374-105">**MarkAsJunkType**</span><span class="sxs-lookup"><span data-stu-id="e6374-105">**MarkAsJunkType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e6374-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e6374-106">Attributes and elements</span></span>

<span data-ttu-id="e6374-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e6374-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e6374-108">属性</span><span class="sxs-lookup"><span data-stu-id="e6374-108">Attributes</span></span>

|<span data-ttu-id="e6374-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="e6374-109">**Attribute**</span></span>|<span data-ttu-id="e6374-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="e6374-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e6374-111">IsJunk</span><span class="sxs-lookup"><span data-stu-id="e6374-111">IsJunk</span></span>  <br/> |<span data-ttu-id="e6374-112">文本值为**true**的**IsJunk**属性指示将电子邮件发件人添加到阻止发件人列表。</span><span class="sxs-lookup"><span data-stu-id="e6374-112">A text value of **true** for the **IsJunk** attribute indicates that the email sender is added to the blocked sender list.</span></span> <span data-ttu-id="e6374-113">如果值为**false**指示电子邮件发件人已从阻止发件人列表中，如果电子邮件发件人已在列表。</span><span class="sxs-lookup"><span data-stu-id="e6374-113">A value of **false** indicates that the email sender is removed from the blocked sender list, if the email sender is already on the list.</span></span>  <br/> |
|<span data-ttu-id="e6374-114">MoveItem</span><span class="sxs-lookup"><span data-stu-id="e6374-114">MoveItem</span></span>  <br/> |<span data-ttu-id="e6374-115">文本值为**true**的**MoveItem**属性指示的项目将被移动到默认的垃圾邮件文件夹。</span><span class="sxs-lookup"><span data-stu-id="e6374-115">A text value of **true** for the **MoveItem** attribute indicates that the item is moved to the default junk mail folder.</span></span> <span data-ttu-id="e6374-116">如果值为**false**指示项目也不会移动至默认垃圾邮件文件夹。</span><span class="sxs-lookup"><span data-stu-id="e6374-116">A value of **false** indicates that the item is not moved to the default junk mail folder.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e6374-117">子元素</span><span class="sxs-lookup"><span data-stu-id="e6374-117">Child elements</span></span>

[<span data-ttu-id="e6374-118">ItemIds</span><span class="sxs-lookup"><span data-stu-id="e6374-118">ItemIds</span></span>](itemids.md)
  
### <a name="parent-elements"></a><span data-ttu-id="e6374-119">父元素</span><span class="sxs-lookup"><span data-stu-id="e6374-119">Parent elements</span></span>

<span data-ttu-id="e6374-120">无。</span><span class="sxs-lookup"><span data-stu-id="e6374-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e6374-121">备注</span><span class="sxs-lookup"><span data-stu-id="e6374-121">Remarks</span></span>

<span data-ttu-id="e6374-122">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="e6374-122">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e6374-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e6374-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e6374-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="e6374-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e6374-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="e6374-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e6374-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="e6374-126">Schema name</span></span>  <br/> |<span data-ttu-id="e6374-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="e6374-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e6374-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="e6374-128">Validation file</span></span>  <br/> |<span data-ttu-id="e6374-129">messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e6374-129">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e6374-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="e6374-130">Can be empty</span></span>  <br/> ||
   

