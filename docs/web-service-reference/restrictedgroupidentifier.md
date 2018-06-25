---
title: RestrictedGroupIdentifier
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RestrictedGroupIdentifier
api_type:
- schema
ms.assetid: a3ea3c81-9f99-4836-8cb4-2384ea63f093
description: RestrictGroupIdentifier 元素表示组安全标识符 (SID) 和用户令牌内受限制的组的属性。
ms.openlocfilehash: c6db8672b2afa855e83f2e9a2bf84c9ff33bdc7a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827206"
---
# <a name="restrictedgroupidentifier"></a><span data-ttu-id="b723d-103">RestrictedGroupIdentifier</span><span class="sxs-lookup"><span data-stu-id="b723d-103">RestrictedGroupIdentifier</span></span>

<span data-ttu-id="b723d-104">**RestrictGroupIdentifier**元素表示组安全标识符 (SID) 和用户令牌内受限制的组的属性。</span><span class="sxs-lookup"><span data-stu-id="b723d-104">The **RestrictGroupIdentifier** element represents the group security identifier (SID) and attributes for a restricted group within a user token.</span></span> 
  
```xml
<RestrictedGroupIdentifier Attributes="">
   <SecurityIdentifier/>
</RestrictedGroupIdentifier>
```

 <span data-ttu-id="b723d-105">**SidAndAttributesType**</span><span class="sxs-lookup"><span data-stu-id="b723d-105">**SidAndAttributesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b723d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b723d-106">Attributes and elements</span></span>

<span data-ttu-id="b723d-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b723d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b723d-108">属性</span><span class="sxs-lookup"><span data-stu-id="b723d-108">Attributes</span></span>

|<span data-ttu-id="b723d-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="b723d-109">**Attribute**</span></span>|<span data-ttu-id="b723d-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="b723d-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b723d-111">**Attributes**</span><span class="sxs-lookup"><span data-stu-id="b723d-111">**Attributes**</span></span> <br/> |<span data-ttu-id="b723d-112">包含组属性。</span><span class="sxs-lookup"><span data-stu-id="b723d-112">Contains group attributes.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b723d-113">子元素</span><span class="sxs-lookup"><span data-stu-id="b723d-113">Child elements</span></span>

|<span data-ttu-id="b723d-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="b723d-114">**Element**</span></span>|<span data-ttu-id="b723d-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="b723d-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b723d-116">SecurityIdentifier</span><span class="sxs-lookup"><span data-stu-id="b723d-116">SecurityIdentifier</span></span>](securityidentifier.md) <br/> |<span data-ttu-id="b723d-117">代表安全描述符定义语言 (SDDL) 窗体的安全标识符。</span><span class="sxs-lookup"><span data-stu-id="b723d-117">Represents the security descriptor definition language (SDDL) form of a security identifier.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b723d-118">父元素</span><span class="sxs-lookup"><span data-stu-id="b723d-118">Parent elements</span></span>

|<span data-ttu-id="b723d-119">**元素**</span><span class="sxs-lookup"><span data-stu-id="b723d-119">**Element**</span></span>|<span data-ttu-id="b723d-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="b723d-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b723d-121">RestrictedGroupSids</span><span class="sxs-lookup"><span data-stu-id="b723d-121">RestrictedGroupSids</span></span>](restrictedgroupsids.md) <br/> |<span data-ttu-id="b723d-122">表示用户令牌内受限制的组的集合。</span><span class="sxs-lookup"><span data-stu-id="b723d-122">Represents a collection of restricted groups within a user token.</span></span> <span data-ttu-id="b723d-123">不支持令牌序列化。</span><span class="sxs-lookup"><span data-stu-id="b723d-123">Token serialization is not supported.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b723d-124">备注</span><span class="sxs-lookup"><span data-stu-id="b723d-124">Remarks</span></span>

<span data-ttu-id="b723d-125">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b723d-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b723d-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="b723d-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b723d-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="b723d-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b723d-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="b723d-128">Schema Name</span></span>  <br/> |<span data-ttu-id="b723d-129">类型架构</span><span class="sxs-lookup"><span data-stu-id="b723d-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="b723d-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="b723d-130">Validation File</span></span>  <br/> |<span data-ttu-id="b723d-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b723d-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b723d-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="b723d-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="b723d-133">False</span><span class="sxs-lookup"><span data-stu-id="b723d-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b723d-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b723d-134">See also</span></span>



- [<span data-ttu-id="b723d-135">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b723d-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

