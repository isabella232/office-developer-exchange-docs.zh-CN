---
title: HasLocationChanged
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5fd465b4-6070-4cd0-9ac3-ed9d2bfd5951
description: HasLocationChanged 元素指定会议的 location 属性是否已更改。
ms.openlocfilehash: 4f774adcf4a7666f40524931504f1172e15ba24d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462442"
---
# <a name="haslocationchanged"></a><span data-ttu-id="54077-103">HasLocationChanged</span><span class="sxs-lookup"><span data-stu-id="54077-103">HasLocationChanged</span></span>

<span data-ttu-id="54077-104">**HasLocationChanged**元素指定会议的 location 属性是否已更改。</span><span class="sxs-lookup"><span data-stu-id="54077-104">The **HasLocationChanged** element specifies whether the location property of a meeting has changed.</span></span> 
  
```XML
<HasLocationChanged> true | false </HasLocationChanged>
```

 <span data-ttu-id="54077-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="54077-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="54077-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="54077-106">Attributes and elements</span></span>

<span data-ttu-id="54077-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="54077-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="54077-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="54077-108">Attributes</span></span>

<span data-ttu-id="54077-109">无。</span><span class="sxs-lookup"><span data-stu-id="54077-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="54077-110">子元素</span><span class="sxs-lookup"><span data-stu-id="54077-110">Child elements</span></span>

<span data-ttu-id="54077-111">无。</span><span class="sxs-lookup"><span data-stu-id="54077-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="54077-112">父元素</span><span class="sxs-lookup"><span data-stu-id="54077-112">Parent elements</span></span>

|<span data-ttu-id="54077-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="54077-113">**Element**</span></span>|<span data-ttu-id="54077-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="54077-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="54077-115">ChangeHighlights</span><span class="sxs-lookup"><span data-stu-id="54077-115">ChangeHighlights</span></span>](changehighlights.md) <br/> |<span data-ttu-id="54077-116">指定会议请求邮件的两个版本之间的变化。</span><span class="sxs-lookup"><span data-stu-id="54077-116">Specifies what has changed between two versions of a meeting request message.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="54077-117">文本值</span><span class="sxs-lookup"><span data-stu-id="54077-117">Text value</span></span>

<span data-ttu-id="54077-118">如果**HasLocationChanged**元素的文本值为**true** ，则表示会议的 location 属性已更改。</span><span class="sxs-lookup"><span data-stu-id="54077-118">A text value of **true** for the **HasLocationChanged** element indicates that the location property of a meeting has changed.</span></span> <span data-ttu-id="54077-119">值**为 false**表示会议的 location 属性未发生更改。</span><span class="sxs-lookup"><span data-stu-id="54077-119">A value **false** indicates that the location property of a meeting has not changed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="54077-120">备注</span><span class="sxs-lookup"><span data-stu-id="54077-120">Remarks</span></span>

<span data-ttu-id="54077-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="54077-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="54077-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="54077-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="54077-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="54077-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="54077-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="54077-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="54077-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="54077-125">Schema Name</span></span>  <br/> |<span data-ttu-id="54077-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="54077-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="54077-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="54077-127">Validation File</span></span>  <br/> |<span data-ttu-id="54077-128">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="54077-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="54077-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="54077-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="54077-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="54077-130">See also</span></span>



- [<span data-ttu-id="54077-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="54077-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

