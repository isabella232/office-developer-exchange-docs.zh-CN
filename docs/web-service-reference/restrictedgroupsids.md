---
title: RestrictedGroupSids
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RestrictedGroupSids
api_type:
- schema
ms.assetid: 569ab552-5616-444a-a7f5-de366a684a34
description: RestrictedGroupSids 元素表示用户令牌中受限制的组的集合。
ms.openlocfilehash: 739a73d2ac4bdbbee03650d035271b5c8d9ea25a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465357"
---
# <a name="restrictedgroupsids"></a><span data-ttu-id="f4be5-103">RestrictedGroupSids</span><span class="sxs-lookup"><span data-stu-id="f4be5-103">RestrictedGroupSids</span></span>

<span data-ttu-id="f4be5-104">**RestrictedGroupSids**元素表示用户令牌中受限制的组的集合。</span><span class="sxs-lookup"><span data-stu-id="f4be5-104">The **RestrictedGroupSids** element represents a collection of restricted groups from a user's token.</span></span> 
  
```xml
<RestrictedGroupSids>
   <RestrictedGroupIdentifier/>
</RestrictedGroupSids>
```

 <span data-ttu-id="f4be5-105">**NonEmptyArrayOfRestrictedGroupIdentifiersType**</span><span class="sxs-lookup"><span data-stu-id="f4be5-105">**NonEmptyArrayOfRestrictedGroupIdentifiersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f4be5-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f4be5-106">Attributes and elements</span></span>

<span data-ttu-id="f4be5-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f4be5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f4be5-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="f4be5-108">Attributes</span></span>

<span data-ttu-id="f4be5-109">无。</span><span class="sxs-lookup"><span data-stu-id="f4be5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f4be5-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f4be5-110">Child elements</span></span>

|<span data-ttu-id="f4be5-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="f4be5-111">**Element**</span></span>|<span data-ttu-id="f4be5-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="f4be5-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f4be5-113">RestrictedGroupIdentifier</span><span class="sxs-lookup"><span data-stu-id="f4be5-113">RestrictedGroupIdentifier</span></span>](restrictedgroupidentifier.md) <br/> |<span data-ttu-id="f4be5-114">表示受限制的组的组安全标识符（SID）和属性。</span><span class="sxs-lookup"><span data-stu-id="f4be5-114">Represents the group security identifier (SID) and attributes for a restricted group.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f4be5-115">父元素</span><span class="sxs-lookup"><span data-stu-id="f4be5-115">Parent elements</span></span>

|<span data-ttu-id="f4be5-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="f4be5-116">**Element**</span></span>|<span data-ttu-id="f4be5-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="f4be5-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f4be5-118">SerializedSecurityContext</span><span class="sxs-lookup"><span data-stu-id="f4be5-118">SerializedSecurityContext</span></span>](serializedsecuritycontext.md) <br/> |<span data-ttu-id="f4be5-119">在服务器到服务器身份验证中用于令牌序列化的 SOAP 标头中使用。</span><span class="sxs-lookup"><span data-stu-id="f4be5-119">Used in the SOAP header for token serialization in server- to-server authentication.</span></span> <span data-ttu-id="f4be5-120">不支持令牌序列化。</span><span class="sxs-lookup"><span data-stu-id="f4be5-120">Token serialization is not supported.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f4be5-121">说明</span><span class="sxs-lookup"><span data-stu-id="f4be5-121">Remarks</span></span>

<span data-ttu-id="f4be5-122">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f4be5-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f4be5-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="f4be5-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f4be5-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="f4be5-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f4be5-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="f4be5-125">Schema Name</span></span>  <br/> |<span data-ttu-id="f4be5-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="f4be5-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="f4be5-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="f4be5-127">Validation File</span></span>  <br/> |<span data-ttu-id="f4be5-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f4be5-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f4be5-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="f4be5-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="f4be5-130">False</span><span class="sxs-lookup"><span data-stu-id="f4be5-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f4be5-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f4be5-131">See also</span></span>



- [<span data-ttu-id="f4be5-132">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f4be5-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

