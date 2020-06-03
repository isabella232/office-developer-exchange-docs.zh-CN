---
title: IsWritable
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d4af8eee-7001-4a8e-b9bd-d14882f2406b
description: IsWritable 元素指定基础联系人或 Active Directory 收件人是否可以写入。
ms.openlocfilehash: 96075adc1772027456f8829eee43bdc734644c09
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467569"
---
# <a name="iswritable"></a><span data-ttu-id="c7589-103">IsWritable</span><span class="sxs-lookup"><span data-stu-id="c7589-103">IsWritable</span></span>

<span data-ttu-id="c7589-104">**IsWritable**元素指定基础联系人或 Active Directory 收件人是否可以写入。</span><span class="sxs-lookup"><span data-stu-id="c7589-104">The **IsWritable** element specifies whether the underlying contact or Active Directory recipient can be written to.</span></span> 
  
```XML
<IsWritable> true | false </IsWritable>
```

 <span data-ttu-id="c7589-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="c7589-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c7589-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c7589-106">Attributes and elements</span></span>

<span data-ttu-id="c7589-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c7589-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c7589-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="c7589-108">Attributes</span></span>

<span data-ttu-id="c7589-109">无。</span><span class="sxs-lookup"><span data-stu-id="c7589-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c7589-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c7589-110">Child elements</span></span>

<span data-ttu-id="c7589-111">无。</span><span class="sxs-lookup"><span data-stu-id="c7589-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c7589-112">父元素</span><span class="sxs-lookup"><span data-stu-id="c7589-112">Parent elements</span></span>

[<span data-ttu-id="c7589-113">归属（PersonaAttributionType）</span><span class="sxs-lookup"><span data-stu-id="c7589-113">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md)
  
## <a name="text-value"></a><span data-ttu-id="c7589-114">文本值</span><span class="sxs-lookup"><span data-stu-id="c7589-114">Text value</span></span>

<span data-ttu-id="c7589-115">如果**IsWritable**元素的文本值为**true** ，则表示联系人或 Active Directory 对象可用于写入访问。</span><span class="sxs-lookup"><span data-stu-id="c7589-115">A text value of **true** for the **IsWritable** element indicates that the contact or Active Directory object is available for write access.</span></span> <span data-ttu-id="c7589-116">如果值为**false** ，则表示联系人或 Active Directory 对象不可用于写访问。</span><span class="sxs-lookup"><span data-stu-id="c7589-116">A value of **false** indicates that the contact or Active Directory object is not available for write access.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c7589-117">备注</span><span class="sxs-lookup"><span data-stu-id="c7589-117">Remarks</span></span>

<span data-ttu-id="c7589-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="c7589-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c7589-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c7589-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  

