---
title: AddImContactToGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 65554e4c-c0d9-485e-9f01-ed1baa8280ab
description: AddImContactToGroup 元素定义将现有的即时消息联系人添加到即时消息组的请求。
ms.openlocfilehash: 71c841ce6df2ed7dcbbf77597b26f3e3e742a7fb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753188"
---
# <a name="addimcontacttogroup"></a><span data-ttu-id="025ac-103">AddImContactToGroup</span><span class="sxs-lookup"><span data-stu-id="025ac-103">AddImContactToGroup</span></span>

<span data-ttu-id="025ac-104">**AddImContactToGroup**元素定义将现有的即时消息联系人添加到即时消息组的请求。</span><span class="sxs-lookup"><span data-stu-id="025ac-104">The **AddImContactToGroup** element defines a request to add an existing instant messaging contact to an instant messaging group.</span></span> 
  
```XML
<AddImContactToGroup>
   <ContactId/>
   <GroupId/>
</AddImContactToGroup>
```

 <span data-ttu-id="025ac-105">**AddImContactToGroupType**</span><span class="sxs-lookup"><span data-stu-id="025ac-105">**AddImContactToGroupType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="025ac-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="025ac-106">Attributes and elements</span></span>

<span data-ttu-id="025ac-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="025ac-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="025ac-108">属性</span><span class="sxs-lookup"><span data-stu-id="025ac-108">Attributes</span></span>

<span data-ttu-id="025ac-109">无。</span><span class="sxs-lookup"><span data-stu-id="025ac-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="025ac-110">子元素</span><span class="sxs-lookup"><span data-stu-id="025ac-110">Child elements</span></span>

<span data-ttu-id="025ac-111">[ContactId](contactid.md) | [GroupId](groupid.md)</span><span class="sxs-lookup"><span data-stu-id="025ac-111">[ContactId](contactid.md) | [GroupId](groupid.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="025ac-112">父元素</span><span class="sxs-lookup"><span data-stu-id="025ac-112">Parent elements</span></span>

<span data-ttu-id="025ac-113">无。</span><span class="sxs-lookup"><span data-stu-id="025ac-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="025ac-114">备注</span><span class="sxs-lookup"><span data-stu-id="025ac-114">Remarks</span></span>

<span data-ttu-id="025ac-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="025ac-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="025ac-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="025ac-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="025ac-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="025ac-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="025ac-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="025ac-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="025ac-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="025ac-119">Schema name</span></span>  <br/> |<span data-ttu-id="025ac-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="025ac-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="025ac-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="025ac-121">Validation file</span></span>  <br/> |<span data-ttu-id="025ac-122">messages.xsd</span><span class="sxs-lookup"><span data-stu-id="025ac-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="025ac-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="025ac-123">Can be empty</span></span>  <br/> |<span data-ttu-id="025ac-124">false</span><span class="sxs-lookup"><span data-stu-id="025ac-124">false</span></span>  <br/> |
   

