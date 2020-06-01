---
title: MarkAsJunk
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f06bafc6-7ee3-4b2b-9fd1-7c51328f4729
description: MarkAsJunk 元素指定将项目移动到 "垃圾邮件" 文件夹，并将发件人添加到 "阻止的发件人" 列表中的请求。
ms.openlocfilehash: 99adc423864f3096772394ef290df20e158e457d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467079"
---
# <a name="markasjunk"></a><span data-ttu-id="215e4-103">MarkAsJunk</span><span class="sxs-lookup"><span data-stu-id="215e4-103">MarkAsJunk</span></span>

<span data-ttu-id="215e4-104">**MarkAsJunk**元素指定将项目移动到 "垃圾邮件" 文件夹，并将发件人添加到 "阻止的发件人" 列表中的请求。</span><span class="sxs-lookup"><span data-stu-id="215e4-104">The **MarkAsJunk** element specifies the request to move an item to the junk mail folder and to add the sender to the blocked sender list.</span></span> 
  
```XML
<MarkAsJunk IsJunk="true | false" MoveItem="true | false">
   <ItemIds/>
</MarkAsJunk>
```

 <span data-ttu-id="215e4-105">**MarkAsJunkType**</span><span class="sxs-lookup"><span data-stu-id="215e4-105">**MarkAsJunkType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="215e4-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="215e4-106">Attributes and elements</span></span>

<span data-ttu-id="215e4-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="215e4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="215e4-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="215e4-108">Attributes</span></span>

|<span data-ttu-id="215e4-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="215e4-109">**Attribute**</span></span>|<span data-ttu-id="215e4-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="215e4-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="215e4-111">IsJunk</span><span class="sxs-lookup"><span data-stu-id="215e4-111">IsJunk</span></span>  <br/> |<span data-ttu-id="215e4-112">**IsJunk**属性的文本值为**true**表示将电子邮件发件人添加到 "阻止的发件人" 列表中。</span><span class="sxs-lookup"><span data-stu-id="215e4-112">A text value of **true** for the **IsJunk** attribute indicates that the email sender is added to the blocked sender list.</span></span> <span data-ttu-id="215e4-113">如果值为**false** ，则表示电子邮件发件人已从阻止的发件人列表中删除（如果该电子邮件发件人已在列表中）。</span><span class="sxs-lookup"><span data-stu-id="215e4-113">A value of **false** indicates that the email sender is removed from the blocked sender list, if the email sender is already on the list.</span></span>  <br/> |
|<span data-ttu-id="215e4-114">MoveItem</span><span class="sxs-lookup"><span data-stu-id="215e4-114">MoveItem</span></span>  <br/> |<span data-ttu-id="215e4-115">**MoveItem**属性的文本值为**true**表示将项目移动到默认的 "垃圾邮件" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="215e4-115">A text value of **true** for the **MoveItem** attribute indicates that the item is moved to the default junk mail folder.</span></span> <span data-ttu-id="215e4-116">**如果值为 false** ，则表示项目不会移动到默认的垃圾邮件文件夹。</span><span class="sxs-lookup"><span data-stu-id="215e4-116">A value of **false** indicates that the item is not moved to the default junk mail folder.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="215e4-117">子元素</span><span class="sxs-lookup"><span data-stu-id="215e4-117">Child elements</span></span>

[<span data-ttu-id="215e4-118">ItemIds</span><span class="sxs-lookup"><span data-stu-id="215e4-118">ItemIds</span></span>](itemids.md)
  
### <a name="parent-elements"></a><span data-ttu-id="215e4-119">父元素</span><span class="sxs-lookup"><span data-stu-id="215e4-119">Parent elements</span></span>

<span data-ttu-id="215e4-120">无。</span><span class="sxs-lookup"><span data-stu-id="215e4-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="215e4-121">说明</span><span class="sxs-lookup"><span data-stu-id="215e4-121">Remarks</span></span>

<span data-ttu-id="215e4-122">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="215e4-122">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="215e4-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="215e4-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="215e4-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="215e4-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="215e4-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="215e4-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="215e4-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="215e4-126">Schema name</span></span>  <br/> |<span data-ttu-id="215e4-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="215e4-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="215e4-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="215e4-128">Validation file</span></span>  <br/> |<span data-ttu-id="215e4-129">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="215e4-129">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="215e4-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="215e4-130">Can be empty</span></span>  <br/> ||
   

