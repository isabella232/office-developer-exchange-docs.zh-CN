---
title: AddNewImContactToGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d5913619-0c13-429d-b9d2-057e8af220f1
description: AddNewImContactToGroup 元素定义将新的即时消息联系人添加到即时消息组的请求。
ms.openlocfilehash: 2736bac6880a11101e9bffee12033c838705700e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753116"
---
# <a name="addnewimcontacttogroup"></a><span data-ttu-id="ab4cb-103">AddNewImContactToGroup</span><span class="sxs-lookup"><span data-stu-id="ab4cb-103">AddNewImContactToGroup</span></span>

<span data-ttu-id="ab4cb-104">**AddNewImContactToGroup**元素定义将新的即时消息联系人添加到即时消息组的请求。</span><span class="sxs-lookup"><span data-stu-id="ab4cb-104">The **AddNewImContactToGroup** element defines a request to add a new instant messaging contact to an instant messaging group.</span></span> 
  
```XML
<AddNewImContactToGroup>
   <ImAddress/>
   <DisplayName/>
   <GroupId/>
</AddNewImContactToGroup>
```

 <span data-ttu-id="ab4cb-105">**AddNewImContactToGroupType**</span><span class="sxs-lookup"><span data-stu-id="ab4cb-105">**AddNewImContactToGroupType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ab4cb-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ab4cb-106">Attributes and elements</span></span>

<span data-ttu-id="ab4cb-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ab4cb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ab4cb-108">属性</span><span class="sxs-lookup"><span data-stu-id="ab4cb-108">Attributes</span></span>

<span data-ttu-id="ab4cb-109">无。</span><span class="sxs-lookup"><span data-stu-id="ab4cb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ab4cb-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ab4cb-110">Child elements</span></span>

<span data-ttu-id="ab4cb-111">[ImAddress (NonEmptyStringType)](imaddress-nonemptystringtype.md) | [DisplayName (NonEmptyStringType)](displayname-nonemptystringtype.md) | [GroupId](groupid.md)</span><span class="sxs-lookup"><span data-stu-id="ab4cb-111">[ImAddress (NonEmptyStringType)](imaddress-nonemptystringtype.md) | [DisplayName (NonEmptyStringType)](displayname-nonemptystringtype.md) | [GroupId](groupid.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ab4cb-112">父元素</span><span class="sxs-lookup"><span data-stu-id="ab4cb-112">Parent elements</span></span>

<span data-ttu-id="ab4cb-113">无。</span><span class="sxs-lookup"><span data-stu-id="ab4cb-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ab4cb-114">备注</span><span class="sxs-lookup"><span data-stu-id="ab4cb-114">Remarks</span></span>

<span data-ttu-id="ab4cb-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="ab4cb-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ab4cb-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ab4cb-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ab4cb-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="ab4cb-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ab4cb-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="ab4cb-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ab4cb-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="ab4cb-119">Schema name</span></span>  <br/> |<span data-ttu-id="ab4cb-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="ab4cb-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ab4cb-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="ab4cb-121">Validation file</span></span>  <br/> |<span data-ttu-id="ab4cb-122">messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ab4cb-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ab4cb-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="ab4cb-123">Can be empty</span></span>  <br/> |<span data-ttu-id="ab4cb-124">false</span><span class="sxs-lookup"><span data-stu-id="ab4cb-124">false</span></span>  <br/> |
   

