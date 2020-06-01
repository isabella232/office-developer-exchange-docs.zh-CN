---
title: DisplayNameFirstLast
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 013c17c9-cb37-4028-9fe6-c3f47441d0f7
description: DisplayNameFirstLast 元素指定 "名称"、"姓"、"姓" 格式的关联角色的显示名称。
ms.openlocfilehash: 6ba35b6a17a64d46655e51691847b9aecbf52f40
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464110"
---
# <a name="displaynamefirstlast"></a><span data-ttu-id="467f3-103">DisplayNameFirstLast</span><span class="sxs-lookup"><span data-stu-id="467f3-103">DisplayNameFirstLast</span></span>

<span data-ttu-id="467f3-104">**DisplayNameFirstLast**元素指定 "名"、"First name"、"Last name" 格式的关联角色的显示名称。</span><span class="sxs-lookup"><span data-stu-id="467f3-104">The **DisplayNameFirstLast** element specifies the display name of the associated persona in the format, "First Name", "Last Name".</span></span> 
  
```XML
<DisplayNameFirstLast>
```

 <span data-ttu-id="467f3-105">**string**</span><span class="sxs-lookup"><span data-stu-id="467f3-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="467f3-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="467f3-106">Attributes and elements</span></span>

<span data-ttu-id="467f3-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="467f3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="467f3-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="467f3-108">Attributes</span></span>

<span data-ttu-id="467f3-109">无。</span><span class="sxs-lookup"><span data-stu-id="467f3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="467f3-110">子元素</span><span class="sxs-lookup"><span data-stu-id="467f3-110">Child elements</span></span>

<span data-ttu-id="467f3-111">无。</span><span class="sxs-lookup"><span data-stu-id="467f3-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="467f3-112">父元素</span><span class="sxs-lookup"><span data-stu-id="467f3-112">Parent elements</span></span>

|<span data-ttu-id="467f3-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="467f3-113">**Element**</span></span>|<span data-ttu-id="467f3-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="467f3-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="467f3-115">角色</span><span class="sxs-lookup"><span data-stu-id="467f3-115">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="467f3-116">指定由**GetPersona**请求返回的一组角色数据。</span><span class="sxs-lookup"><span data-stu-id="467f3-116">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="467f3-117">文本值</span><span class="sxs-lookup"><span data-stu-id="467f3-117">Text value</span></span>

<span data-ttu-id="467f3-118">**DisplayNameFirstLast**元素的文本值是一个包含显示名称的字符串值，其中先具有给定的名称。</span><span class="sxs-lookup"><span data-stu-id="467f3-118">The text value of the **DisplayNameFirstLast** element is a string value containing the display name, with the given name first.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="467f3-119">备注</span><span class="sxs-lookup"><span data-stu-id="467f3-119">Remarks</span></span>

<span data-ttu-id="467f3-120">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="467f3-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="467f3-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="467f3-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="467f3-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="467f3-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="467f3-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="467f3-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="467f3-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="467f3-124">Schema Name</span></span>  <br/> |<span data-ttu-id="467f3-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="467f3-125">Type schema</span></span>  <br/> |
|<span data-ttu-id="467f3-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="467f3-126">Validation File</span></span>  <br/> |<span data-ttu-id="467f3-127">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="467f3-127">types.xsd</span></span>  <br/> |
|<span data-ttu-id="467f3-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="467f3-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="467f3-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="467f3-129">See also</span></span>

- [<span data-ttu-id="467f3-130">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="467f3-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

