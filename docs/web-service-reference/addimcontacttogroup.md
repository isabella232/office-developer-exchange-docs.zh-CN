---
title: AddImContactToGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 65554e4c-c0d9-485e-9f01-ed1baa8280ab
description: AddImContactToGroup 元素定义将现有即时消息联系人添加到即时消息组的请求。
ms.openlocfilehash: b86b1cb69a1ebc7034e5a27047c14efbab7236ea
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459663"
---
# <a name="addimcontacttogroup"></a><span data-ttu-id="c764e-103">AddImContactToGroup</span><span class="sxs-lookup"><span data-stu-id="c764e-103">AddImContactToGroup</span></span>

<span data-ttu-id="c764e-104">**AddImContactToGroup**元素定义将现有即时消息联系人添加到即时消息组的请求。</span><span class="sxs-lookup"><span data-stu-id="c764e-104">The **AddImContactToGroup** element defines a request to add an existing instant messaging contact to an instant messaging group.</span></span> 
  
```XML
<AddImContactToGroup>
   <ContactId/>
   <GroupId/>
</AddImContactToGroup>
```

 <span data-ttu-id="c764e-105">**AddImContactToGroupType**</span><span class="sxs-lookup"><span data-stu-id="c764e-105">**AddImContactToGroupType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c764e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c764e-106">Attributes and elements</span></span>

<span data-ttu-id="c764e-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c764e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c764e-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="c764e-108">Attributes</span></span>

<span data-ttu-id="c764e-109">无。</span><span class="sxs-lookup"><span data-stu-id="c764e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c764e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c764e-110">Child elements</span></span>

<span data-ttu-id="c764e-111">[ContactId](contactid.md)  | [GroupId](groupid.md)</span><span class="sxs-lookup"><span data-stu-id="c764e-111">[ContactId](contactid.md) | [GroupId](groupid.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c764e-112">父元素</span><span class="sxs-lookup"><span data-stu-id="c764e-112">Parent elements</span></span>

<span data-ttu-id="c764e-113">无。</span><span class="sxs-lookup"><span data-stu-id="c764e-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c764e-114">说明</span><span class="sxs-lookup"><span data-stu-id="c764e-114">Remarks</span></span>

<span data-ttu-id="c764e-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="c764e-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c764e-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c764e-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c764e-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="c764e-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c764e-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="c764e-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c764e-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="c764e-119">Schema name</span></span>  <br/> |<span data-ttu-id="c764e-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="c764e-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c764e-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="c764e-121">Validation file</span></span>  <br/> |<span data-ttu-id="c764e-122">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="c764e-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c764e-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="c764e-123">Can be empty</span></span>  <br/> |<span data-ttu-id="c764e-124">false</span><span class="sxs-lookup"><span data-stu-id="c764e-124">false</span></span>  <br/> |
   

