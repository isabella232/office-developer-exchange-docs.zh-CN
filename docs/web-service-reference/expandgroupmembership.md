---
title: ExpandGroupMembership
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8989e96b-8fa1-4858-93b2-2cbdb30b9ca9
description: ExpandGroupMembership 元素指示是否展开 GetSearchableMailboxes 请求返回的组的成员身份。
ms.openlocfilehash: 8a94aa3da165ecc13282127e75c8d166f3972ead
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456904"
---
# <a name="expandgroupmembership"></a><span data-ttu-id="914de-103">ExpandGroupMembership</span><span class="sxs-lookup"><span data-stu-id="914de-103">ExpandGroupMembership</span></span>

<span data-ttu-id="914de-104">**ExpandGroupMembership**元素指示是否展开**GetSearchableMailboxes**请求返回的组的成员身份。</span><span class="sxs-lookup"><span data-stu-id="914de-104">The **ExpandGroupMembership** element indicates whether to expand the membership of the group returned from a **GetSearchableMailboxes** request.</span></span> 
  
```XML
<ExpandGroupMembership>true | false</ExpandGroupMembership>
```

 <span data-ttu-id="914de-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="914de-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="914de-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="914de-106">Attributes and elements</span></span>

<span data-ttu-id="914de-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="914de-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="914de-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="914de-108">Attributes</span></span>

<span data-ttu-id="914de-109">无。</span><span class="sxs-lookup"><span data-stu-id="914de-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="914de-110">子元素</span><span class="sxs-lookup"><span data-stu-id="914de-110">Child elements</span></span>

<span data-ttu-id="914de-111">无。</span><span class="sxs-lookup"><span data-stu-id="914de-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="914de-112">父元素</span><span class="sxs-lookup"><span data-stu-id="914de-112">Parent elements</span></span>

<span data-ttu-id="914de-113">[GetDiscoverySearchConfiguration](getdiscoverysearchconfiguration.md)  | [GetSearchableMailboxes](getsearchablemailboxes.md)</span><span class="sxs-lookup"><span data-stu-id="914de-113">[GetDiscoverySearchConfiguration](getdiscoverysearchconfiguration.md) | [GetSearchableMailboxes](getsearchablemailboxes.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="914de-114">文本值</span><span class="sxs-lookup"><span data-stu-id="914de-114">Text value</span></span>

<span data-ttu-id="914de-115">如果**ExpandGroupElement**元素的文本值为**true** ，则表明组成员身份已展开。</span><span class="sxs-lookup"><span data-stu-id="914de-115">A text value of **true** for the **ExpandGroupElement** element indicates that group membership is expanded.</span></span> <span data-ttu-id="914de-116">**如果值为 false** ，则表示不展开组成员身份以显示组的成员。</span><span class="sxs-lookup"><span data-stu-id="914de-116">A value of **false** indicates that the group membership is not expanded to show the members of the group.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="914de-117">备注</span><span class="sxs-lookup"><span data-stu-id="914de-117">Remarks</span></span>

<span data-ttu-id="914de-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="914de-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="914de-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="914de-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="914de-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="914de-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="914de-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="914de-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="914de-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="914de-122">Schema name</span></span>  <br/> |<span data-ttu-id="914de-123">消息架构</span><span class="sxs-lookup"><span data-stu-id="914de-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="914de-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="914de-124">Validation file</span></span>  <br/> |<span data-ttu-id="914de-125">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="914de-125">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="914de-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="914de-126">Can be empty</span></span>  <br/> |<span data-ttu-id="914de-127">false</span><span class="sxs-lookup"><span data-stu-id="914de-127">false</span></span>  <br/> |
   

