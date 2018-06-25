---
title: IsWritable
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d4af8eee-7001-4a8e-b9bd-d14882f2406b
description: IsWritable 元素指定是否可以向写入基础联系人或 Active Directory 收件人。
ms.openlocfilehash: 03f258d01ecfc12dfa4e09ac88f4a75340d2acf3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826158"
---
# <a name="iswritable"></a><span data-ttu-id="f114a-103">IsWritable</span><span class="sxs-lookup"><span data-stu-id="f114a-103">IsWritable</span></span>

<span data-ttu-id="f114a-104">**IsWritable**元素指定是否可以向写入基础联系人或 Active Directory 收件人。</span><span class="sxs-lookup"><span data-stu-id="f114a-104">The **IsWritable** element specifies whether the underlying contact or Active Directory recipient can be written to.</span></span> 
  
```XML
<IsWritable> true | false </IsWritable>
```

 <span data-ttu-id="f114a-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="f114a-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f114a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f114a-106">Attributes and elements</span></span>

<span data-ttu-id="f114a-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f114a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f114a-108">属性</span><span class="sxs-lookup"><span data-stu-id="f114a-108">Attributes</span></span>

<span data-ttu-id="f114a-109">无。</span><span class="sxs-lookup"><span data-stu-id="f114a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f114a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f114a-110">Child elements</span></span>

<span data-ttu-id="f114a-111">无。</span><span class="sxs-lookup"><span data-stu-id="f114a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f114a-112">父元素</span><span class="sxs-lookup"><span data-stu-id="f114a-112">Parent elements</span></span>

[<span data-ttu-id="f114a-113">归属 (PersonaAttributionType)</span><span class="sxs-lookup"><span data-stu-id="f114a-113">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md)
  
## <a name="text-value"></a><span data-ttu-id="f114a-114">文本值</span><span class="sxs-lookup"><span data-stu-id="f114a-114">Text value</span></span>

<span data-ttu-id="f114a-115">文本值为**true**的**IsWritable**元素指示的联系人或 Active Directory 对象是可供写访问权限。</span><span class="sxs-lookup"><span data-stu-id="f114a-115">A text value of **true** for the **IsWritable** element indicates that the contact or Active Directory object is available for write access.</span></span> <span data-ttu-id="f114a-116">如果值为**false**指示的联系人或 Active Directory 对象不可用的写访问权限。</span><span class="sxs-lookup"><span data-stu-id="f114a-116">A value of **false** indicates that the contact or Active Directory object is not available for write access.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f114a-117">备注</span><span class="sxs-lookup"><span data-stu-id="f114a-117">Remarks</span></span>

<span data-ttu-id="f114a-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="f114a-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="f114a-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f114a-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  

