---
title: GroupSids
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GroupSids
api_type:
- schema
ms.assetid: ebb00653-83f0-4080-a902-c38df6719800
description: GroupSids 元素表示 Active Directory 目录服务组对象安全标识符的集合。
ms.openlocfilehash: 40f36176fcaa3e2160237f269fb2dc3b12bf8af2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530062"
---
# <a name="groupsids"></a><span data-ttu-id="dc78a-103">GroupSids</span><span class="sxs-lookup"><span data-stu-id="dc78a-103">GroupSids</span></span>

<span data-ttu-id="dc78a-104">**GroupSids**元素表示 Active directory 目录服务组对象安全标识符的集合。</span><span class="sxs-lookup"><span data-stu-id="dc78a-104">The **GroupSids** element represents a collection of Active Directory directory service group object security identifiers.</span></span> 
  
```xml
<GroupSids>
   <GroupIdentifier/>
</GroupSids>
```

 <span data-ttu-id="dc78a-105">**NonEmptyArrayOfGroupIdentifiersType**</span><span class="sxs-lookup"><span data-stu-id="dc78a-105">**NonEmptyArrayOfGroupIdentifiersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dc78a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="dc78a-106">Attributes and elements</span></span>

<span data-ttu-id="dc78a-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="dc78a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dc78a-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="dc78a-108">Attributes</span></span>

<span data-ttu-id="dc78a-109">无。</span><span class="sxs-lookup"><span data-stu-id="dc78a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dc78a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="dc78a-110">Child elements</span></span>

|<span data-ttu-id="dc78a-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="dc78a-111">**Element**</span></span>|<span data-ttu-id="dc78a-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="dc78a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dc78a-113">GroupIdentifier</span><span class="sxs-lookup"><span data-stu-id="dc78a-113">GroupIdentifier</span></span>](groupidentifier.md) <br/> |<span data-ttu-id="dc78a-114">代表帐户所属的 Active Directory 对象组的单个安全标识符和属性。</span><span class="sxs-lookup"><span data-stu-id="dc78a-114">Represents a single security identifier and attribute for an Active Directory object group of which the account is a member.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="dc78a-115">父元素</span><span class="sxs-lookup"><span data-stu-id="dc78a-115">Parent elements</span></span>

|<span data-ttu-id="dc78a-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="dc78a-116">**Element**</span></span>|<span data-ttu-id="dc78a-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="dc78a-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dc78a-118">SerializedSecurityContext</span><span class="sxs-lookup"><span data-stu-id="dc78a-118">SerializedSecurityContext</span></span>](serializedsecuritycontext.md) <br/> |<span data-ttu-id="dc78a-119">在服务器到服务器身份验证中用于令牌序列化的简单对象访问协议（SOAP）标头中使用。</span><span class="sxs-lookup"><span data-stu-id="dc78a-119">Used in the Simple Object Access Protocol (SOAP) header for token serialization in server-to-server authentication.</span></span> <span data-ttu-id="dc78a-120">不支持令牌序列化。</span><span class="sxs-lookup"><span data-stu-id="dc78a-120">Token serialization is not supported.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dc78a-121">说明</span><span class="sxs-lookup"><span data-stu-id="dc78a-121">Remarks</span></span>

<span data-ttu-id="dc78a-122">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="dc78a-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dc78a-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="dc78a-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dc78a-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="dc78a-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="dc78a-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="dc78a-125">Schema Name</span></span>  <br/> |<span data-ttu-id="dc78a-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="dc78a-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="dc78a-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="dc78a-127">Validation File</span></span>  <br/> |<span data-ttu-id="dc78a-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="dc78a-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="dc78a-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="dc78a-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="dc78a-130">False</span><span class="sxs-lookup"><span data-stu-id="dc78a-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dc78a-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="dc78a-131">See also</span></span>



- [<span data-ttu-id="dc78a-132">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="dc78a-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

