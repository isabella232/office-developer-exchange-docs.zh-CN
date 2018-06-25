---
title: 成员 (MemberListType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Members
api_type:
- schema
ms.assetid: cbd38049-2ef7-40bf-9bec-0469af0f58ec
description: 成员元素提供通讯组列表成员的列表。
ms.openlocfilehash: 8cf9ed7a64a908614ce7be30a9bef631739fcebf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826439"
---
# <a name="members-memberlisttype"></a><span data-ttu-id="ed1f0-103">成员 (MemberListType)</span><span class="sxs-lookup"><span data-stu-id="ed1f0-103">Members (MemberListType)</span></span>

<span data-ttu-id="ed1f0-104">**成员**元素提供通讯组列表成员的列表。</span><span class="sxs-lookup"><span data-stu-id="ed1f0-104">The **Members** element provides the list of members for a distribution list.</span></span> 
  
```xml
<Members>
   <Member/>
</Members>
```

<span data-ttu-id="ed1f0-105">**MemberListType**</span><span class="sxs-lookup"><span data-stu-id="ed1f0-105">**MemberListType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="ed1f0-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ed1f0-106">Attributes and elements</span></span>

<span data-ttu-id="ed1f0-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ed1f0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ed1f0-108">属性</span><span class="sxs-lookup"><span data-stu-id="ed1f0-108">Attributes</span></span>

<span data-ttu-id="ed1f0-109">无。</span><span class="sxs-lookup"><span data-stu-id="ed1f0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ed1f0-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ed1f0-110">Child elements</span></span>

|<span data-ttu-id="ed1f0-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="ed1f0-111">**Element**</span></span>|<span data-ttu-id="ed1f0-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="ed1f0-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ed1f0-113">成员</span><span class="sxs-lookup"><span data-stu-id="ed1f0-113">Member</span></span>](member-ex15websvcsotherref.md) <br/> |<span data-ttu-id="ed1f0-114">为一个完全解析电子邮件地址，以及在服务器上的地址的状态提供标识符。</span><span class="sxs-lookup"><span data-stu-id="ed1f0-114">Provides an identifier for a fully resolved e-mail address, and the status of that address on the server.</span></span> <span data-ttu-id="ed1f0-115">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="ed1f0-115">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ed1f0-116">父元素</span><span class="sxs-lookup"><span data-stu-id="ed1f0-116">Parent elements</span></span>

|<span data-ttu-id="ed1f0-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="ed1f0-117">**Element**</span></span>|<span data-ttu-id="ed1f0-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="ed1f0-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ed1f0-119">DistributionList</span><span class="sxs-lookup"><span data-stu-id="ed1f0-119">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="ed1f0-120">表示通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="ed1f0-120">Represents a distribution list.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ed1f0-121">备注</span><span class="sxs-lookup"><span data-stu-id="ed1f0-121">Remarks</span></span>

<span data-ttu-id="ed1f0-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ed1f0-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ed1f0-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="ed1f0-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ed1f0-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="ed1f0-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ed1f0-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="ed1f0-125">Schema Name</span></span>  <br/> |<span data-ttu-id="ed1f0-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="ed1f0-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="ed1f0-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="ed1f0-127">Validation File</span></span>  <br/> |<span data-ttu-id="ed1f0-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ed1f0-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ed1f0-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="ed1f0-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="ed1f0-130">False</span><span class="sxs-lookup"><span data-stu-id="ed1f0-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ed1f0-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ed1f0-131">See also</span></span>

- [<span data-ttu-id="ed1f0-132">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="ed1f0-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

