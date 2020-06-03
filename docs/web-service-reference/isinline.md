---
title: IsInline
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsInline
api_type:
- schema
ms.assetid: 5e7712c8-372a-4a16-be64-360c5ff3961a
description: IsInline 元素表示附件是否内联显示在项目中。
ms.openlocfilehash: 2b3b6392fe8867ae9782dcb7211c17f4f4d9becd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464208"
---
# <a name="isinline"></a><span data-ttu-id="05a55-103">IsInline</span><span class="sxs-lookup"><span data-stu-id="05a55-103">IsInline</span></span>

<span data-ttu-id="05a55-104">**IsInline**元素表示附件是否内联显示在项目中。</span><span class="sxs-lookup"><span data-stu-id="05a55-104">The **IsInline** element represents whether the attachment appears inline within an item.</span></span> 
  
```xml
<IsInline>true or false</IsInline>
```

 <span data-ttu-id="05a55-105">**boolean**</span><span class="sxs-lookup"><span data-stu-id="05a55-105">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="05a55-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="05a55-106">Attributes and elements</span></span>

<span data-ttu-id="05a55-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="05a55-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="05a55-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="05a55-108">Attributes</span></span>

<span data-ttu-id="05a55-109">无。</span><span class="sxs-lookup"><span data-stu-id="05a55-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="05a55-110">子元素</span><span class="sxs-lookup"><span data-stu-id="05a55-110">Child elements</span></span>

<span data-ttu-id="05a55-111">无。</span><span class="sxs-lookup"><span data-stu-id="05a55-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="05a55-112">父元素</span><span class="sxs-lookup"><span data-stu-id="05a55-112">Parent elements</span></span>

|<span data-ttu-id="05a55-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="05a55-113">**Element**</span></span>|<span data-ttu-id="05a55-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="05a55-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="05a55-115">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="05a55-115">FileAttachment</span></span>](fileattachment.md) <br/> |<span data-ttu-id="05a55-116">代表附加到 Exchange 存储中的项目的文件。</span><span class="sxs-lookup"><span data-stu-id="05a55-116">Represents a file that is attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="05a55-117">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="05a55-117">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="05a55-118">表示附加到另一个 Exchange 项目的 Exchange 项目。</span><span class="sxs-lookup"><span data-stu-id="05a55-118">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="05a55-119">文本值</span><span class="sxs-lookup"><span data-stu-id="05a55-119">Text value</span></span>

<span data-ttu-id="05a55-120">此元素可以是**true** ，也可以是**false**。</span><span class="sxs-lookup"><span data-stu-id="05a55-120">This element can be either **true** or **false**.</span></span> <span data-ttu-id="05a55-121">默认值为 **false**。</span><span class="sxs-lookup"><span data-stu-id="05a55-121">The default value is **false**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="05a55-122">备注</span><span class="sxs-lookup"><span data-stu-id="05a55-122">Remarks</span></span>

<span data-ttu-id="05a55-123">描述此元素的架构位于运行 Microsoft Exchange Server 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="05a55-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="05a55-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="05a55-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="05a55-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="05a55-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="05a55-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="05a55-126">Schema Name</span></span>  <br/> |<span data-ttu-id="05a55-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="05a55-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="05a55-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="05a55-128">Validation File</span></span>  <br/> |<span data-ttu-id="05a55-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="05a55-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="05a55-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="05a55-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="05a55-131">False</span><span class="sxs-lookup"><span data-stu-id="05a55-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="05a55-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="05a55-132">See also</span></span>



- [<span data-ttu-id="05a55-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="05a55-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

