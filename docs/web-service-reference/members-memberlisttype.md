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
description: Members 元素提供通讯组列表成员的列表。
ms.openlocfilehash: 2cdfb81dfbc223db365d49ed44d4893339eb4653
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462428"
---
# <a name="members-memberlisttype"></a><span data-ttu-id="b0876-103">成员 (MemberListType)</span><span class="sxs-lookup"><span data-stu-id="b0876-103">Members (MemberListType)</span></span>

<span data-ttu-id="b0876-104">**Members**元素提供通讯组列表成员的列表。</span><span class="sxs-lookup"><span data-stu-id="b0876-104">The **Members** element provides the list of members for a distribution list.</span></span> 
  
```xml
<Members>
   <Member/>
</Members>
```

<span data-ttu-id="b0876-105">**MemberListType**</span><span class="sxs-lookup"><span data-stu-id="b0876-105">**MemberListType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="b0876-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b0876-106">Attributes and elements</span></span>

<span data-ttu-id="b0876-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b0876-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b0876-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="b0876-108">Attributes</span></span>

<span data-ttu-id="b0876-109">无。</span><span class="sxs-lookup"><span data-stu-id="b0876-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b0876-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b0876-110">Child elements</span></span>

|<span data-ttu-id="b0876-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="b0876-111">**Element**</span></span>|<span data-ttu-id="b0876-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="b0876-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b0876-113">成员</span><span class="sxs-lookup"><span data-stu-id="b0876-113">Member</span></span>](member-ex15websvcsotherref.md) <br/> |<span data-ttu-id="b0876-114">提供完全解析的电子邮件地址的标识符，以及该地址在服务器上的状态。</span><span class="sxs-lookup"><span data-stu-id="b0876-114">Provides an identifier for a fully resolved e-mail address, and the status of that address on the server.</span></span> <span data-ttu-id="b0876-115">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="b0876-115">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b0876-116">父元素</span><span class="sxs-lookup"><span data-stu-id="b0876-116">Parent elements</span></span>

|<span data-ttu-id="b0876-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="b0876-117">**Element**</span></span>|<span data-ttu-id="b0876-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="b0876-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b0876-119">DistributionList</span><span class="sxs-lookup"><span data-stu-id="b0876-119">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="b0876-120">表示通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="b0876-120">Represents a distribution list.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b0876-121">说明</span><span class="sxs-lookup"><span data-stu-id="b0876-121">Remarks</span></span>

<span data-ttu-id="b0876-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b0876-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b0876-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="b0876-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b0876-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="b0876-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b0876-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="b0876-125">Schema Name</span></span>  <br/> |<span data-ttu-id="b0876-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="b0876-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="b0876-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="b0876-127">Validation File</span></span>  <br/> |<span data-ttu-id="b0876-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b0876-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b0876-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="b0876-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="b0876-130">False</span><span class="sxs-lookup"><span data-stu-id="b0876-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b0876-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b0876-131">See also</span></span>

- [<span data-ttu-id="b0876-132">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b0876-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

