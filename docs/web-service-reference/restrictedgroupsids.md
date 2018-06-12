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
description: RestrictedGroupSids 元素从用户的令牌表示受限制的组的集合。
ms.openlocfilehash: fcfee809261c7ed0a4e0d092c091841fec641e46
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827201"
---
# <a name="restrictedgroupsids"></a><span data-ttu-id="17fc0-103">RestrictedGroupSids</span><span class="sxs-lookup"><span data-stu-id="17fc0-103">RestrictedGroupSids</span></span>

<span data-ttu-id="17fc0-104">**RestrictedGroupSids**元素从用户的令牌表示受限制的组的集合。</span><span class="sxs-lookup"><span data-stu-id="17fc0-104">The **RestrictedGroupSids** element represents a collection of restricted groups from a user's token.</span></span> 
  
```xml
<RestrictedGroupSids>
   <RestrictedGroupIdentifier/>
</RestrictedGroupSids>
```

 <span data-ttu-id="17fc0-105">**NonEmptyArrayOfRestrictedGroupIdentifiersType**</span><span class="sxs-lookup"><span data-stu-id="17fc0-105">**NonEmptyArrayOfRestrictedGroupIdentifiersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="17fc0-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="17fc0-106">Attributes and elements</span></span>

<span data-ttu-id="17fc0-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="17fc0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="17fc0-108">属性</span><span class="sxs-lookup"><span data-stu-id="17fc0-108">Attributes</span></span>

<span data-ttu-id="17fc0-109">无。</span><span class="sxs-lookup"><span data-stu-id="17fc0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="17fc0-110">子元素</span><span class="sxs-lookup"><span data-stu-id="17fc0-110">Child elements</span></span>

|<span data-ttu-id="17fc0-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="17fc0-111">**Element**</span></span>|<span data-ttu-id="17fc0-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="17fc0-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="17fc0-113">RestrictedGroupIdentifier</span><span class="sxs-lookup"><span data-stu-id="17fc0-113">RestrictedGroupIdentifier</span></span>](restrictedgroupidentifier.md) <br/> |<span data-ttu-id="17fc0-114">表示组安全标识符 (SID) 和受限制的组的属性。</span><span class="sxs-lookup"><span data-stu-id="17fc0-114">Represents the group security identifier (SID) and attributes for a restricted group.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="17fc0-115">父元素</span><span class="sxs-lookup"><span data-stu-id="17fc0-115">Parent elements</span></span>

|<span data-ttu-id="17fc0-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="17fc0-116">**Element**</span></span>|<span data-ttu-id="17fc0-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="17fc0-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="17fc0-118">SerializedSecurityContext</span><span class="sxs-lookup"><span data-stu-id="17fc0-118">SerializedSecurityContext</span></span>](serializedsecuritycontext.md) <br/> |<span data-ttu-id="17fc0-119">用于服务器到服务器身份验证中的令牌序列化的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="17fc0-119">Used in the SOAP header for token serialization in server- to-server authentication.</span></span> <span data-ttu-id="17fc0-120">不支持令牌序列化。</span><span class="sxs-lookup"><span data-stu-id="17fc0-120">Token serialization is not supported.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="17fc0-121">备注</span><span class="sxs-lookup"><span data-stu-id="17fc0-121">Remarks</span></span>

<span data-ttu-id="17fc0-122">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="17fc0-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="17fc0-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="17fc0-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="17fc0-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="17fc0-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="17fc0-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="17fc0-125">Schema Name</span></span>  <br/> |<span data-ttu-id="17fc0-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="17fc0-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="17fc0-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="17fc0-127">Validation File</span></span>  <br/> |<span data-ttu-id="17fc0-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="17fc0-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="17fc0-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="17fc0-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="17fc0-130">False</span><span class="sxs-lookup"><span data-stu-id="17fc0-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="17fc0-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="17fc0-131">See also</span></span>



- [<span data-ttu-id="17fc0-132">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="17fc0-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

