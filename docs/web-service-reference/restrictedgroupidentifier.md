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
description: RestrictGroupIdentifier 元素表示用户令牌中的受限制组的组安全标识符（SID）和属性。
ms.openlocfilehash: c95af4e09324e96f4551a05490dc200aec0cbd46
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465364"
---
# <a name="restrictedgroupidentifier"></a><span data-ttu-id="24e8a-103">RestrictedGroupIdentifier</span><span class="sxs-lookup"><span data-stu-id="24e8a-103">RestrictedGroupIdentifier</span></span>

<span data-ttu-id="24e8a-104">**RestrictGroupIdentifier**元素表示用户令牌中的受限制组的组安全标识符（SID）和属性。</span><span class="sxs-lookup"><span data-stu-id="24e8a-104">The **RestrictGroupIdentifier** element represents the group security identifier (SID) and attributes for a restricted group within a user token.</span></span> 
  
```xml
<RestrictedGroupIdentifier Attributes="">
   <SecurityIdentifier/>
</RestrictedGroupIdentifier>
```

 <span data-ttu-id="24e8a-105">**SidAndAttributesType**</span><span class="sxs-lookup"><span data-stu-id="24e8a-105">**SidAndAttributesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="24e8a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="24e8a-106">Attributes and elements</span></span>

<span data-ttu-id="24e8a-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="24e8a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="24e8a-108">属性</span><span class="sxs-lookup"><span data-stu-id="24e8a-108">Attributes</span></span>

|<span data-ttu-id="24e8a-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="24e8a-109">**Attribute**</span></span>|<span data-ttu-id="24e8a-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="24e8a-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="24e8a-111">**Attributes**</span><span class="sxs-lookup"><span data-stu-id="24e8a-111">**Attributes**</span></span> <br/> |<span data-ttu-id="24e8a-112">包含组属性。</span><span class="sxs-lookup"><span data-stu-id="24e8a-112">Contains group attributes.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="24e8a-113">子元素</span><span class="sxs-lookup"><span data-stu-id="24e8a-113">Child elements</span></span>

|<span data-ttu-id="24e8a-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="24e8a-114">**Element**</span></span>|<span data-ttu-id="24e8a-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="24e8a-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="24e8a-116">SecurityIdentifier</span><span class="sxs-lookup"><span data-stu-id="24e8a-116">SecurityIdentifier</span></span>](securityidentifier.md) <br/> |<span data-ttu-id="24e8a-117">表示安全标识符的安全描述符定义语言（SDDL）形式。</span><span class="sxs-lookup"><span data-stu-id="24e8a-117">Represents the security descriptor definition language (SDDL) form of a security identifier.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="24e8a-118">父元素</span><span class="sxs-lookup"><span data-stu-id="24e8a-118">Parent elements</span></span>

|<span data-ttu-id="24e8a-119">**元素**</span><span class="sxs-lookup"><span data-stu-id="24e8a-119">**Element**</span></span>|<span data-ttu-id="24e8a-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="24e8a-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="24e8a-121">RestrictedGroupSids</span><span class="sxs-lookup"><span data-stu-id="24e8a-121">RestrictedGroupSids</span></span>](restrictedgroupsids.md) <br/> |<span data-ttu-id="24e8a-122">表示用户令牌中受限制的组的集合。</span><span class="sxs-lookup"><span data-stu-id="24e8a-122">Represents a collection of restricted groups within a user token.</span></span> <span data-ttu-id="24e8a-123">不支持令牌序列化。</span><span class="sxs-lookup"><span data-stu-id="24e8a-123">Token serialization is not supported.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="24e8a-124">说明</span><span class="sxs-lookup"><span data-stu-id="24e8a-124">Remarks</span></span>

<span data-ttu-id="24e8a-125">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="24e8a-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="24e8a-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="24e8a-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="24e8a-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="24e8a-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="24e8a-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="24e8a-128">Schema Name</span></span>  <br/> |<span data-ttu-id="24e8a-129">类型架构</span><span class="sxs-lookup"><span data-stu-id="24e8a-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="24e8a-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="24e8a-130">Validation File</span></span>  <br/> |<span data-ttu-id="24e8a-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="24e8a-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="24e8a-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="24e8a-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="24e8a-133">False</span><span class="sxs-lookup"><span data-stu-id="24e8a-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="24e8a-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="24e8a-134">See also</span></span>



- [<span data-ttu-id="24e8a-135">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="24e8a-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

