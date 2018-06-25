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
ms.openlocfilehash: c24c8ea3c3b7d37f41986997ed924c951b4a48ef
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825790"
---
# <a name="groupsids"></a><span data-ttu-id="48cdc-103">GroupSids</span><span class="sxs-lookup"><span data-stu-id="48cdc-103">GroupSids</span></span>

<span data-ttu-id="48cdc-104">**GroupSids**元素表示 Active Directory 目录服务组对象安全标识符的集合。</span><span class="sxs-lookup"><span data-stu-id="48cdc-104">The **GroupSids** element represents a collection of Active Directory directory service group object security identifiers.</span></span> 
  
```xml
<GroupSids>
   <GroupIdentifier/>
</GroupSids>
```

 <span data-ttu-id="48cdc-105">**NonEmptyArrayOfGroupIdentifiersType**</span><span class="sxs-lookup"><span data-stu-id="48cdc-105">**NonEmptyArrayOfGroupIdentifiersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="48cdc-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="48cdc-106">Attributes and elements</span></span>

<span data-ttu-id="48cdc-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="48cdc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="48cdc-108">属性</span><span class="sxs-lookup"><span data-stu-id="48cdc-108">Attributes</span></span>

<span data-ttu-id="48cdc-109">无。</span><span class="sxs-lookup"><span data-stu-id="48cdc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="48cdc-110">子元素</span><span class="sxs-lookup"><span data-stu-id="48cdc-110">Child elements</span></span>

|<span data-ttu-id="48cdc-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="48cdc-111">**Element**</span></span>|<span data-ttu-id="48cdc-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="48cdc-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="48cdc-113">GroupIdentifier</span><span class="sxs-lookup"><span data-stu-id="48cdc-113">GroupIdentifier</span></span>](groupidentifier.md) <br/> |<span data-ttu-id="48cdc-114">代表单个安全标识符和 Active Directory 对象所在的组帐户成员属性。</span><span class="sxs-lookup"><span data-stu-id="48cdc-114">Represents a single security identifier and attribute for an Active Directory object group of which the account is a member.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="48cdc-115">父元素</span><span class="sxs-lookup"><span data-stu-id="48cdc-115">Parent elements</span></span>

|<span data-ttu-id="48cdc-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="48cdc-116">**Element**</span></span>|<span data-ttu-id="48cdc-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="48cdc-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="48cdc-118">SerializedSecurityContext</span><span class="sxs-lookup"><span data-stu-id="48cdc-118">SerializedSecurityContext</span></span>](serializedsecuritycontext.md) <br/> |<span data-ttu-id="48cdc-119">简单对象访问协议 (SOAP) 标头中用于服务器到服务器身份验证中的令牌序列化。</span><span class="sxs-lookup"><span data-stu-id="48cdc-119">Used in the Simple Object Access Protocol (SOAP) header for token serialization in server-to-server authentication.</span></span> <span data-ttu-id="48cdc-120">不支持令牌序列化。</span><span class="sxs-lookup"><span data-stu-id="48cdc-120">Token serialization is not supported.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="48cdc-121">备注</span><span class="sxs-lookup"><span data-stu-id="48cdc-121">Remarks</span></span>

<span data-ttu-id="48cdc-122">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="48cdc-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="48cdc-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="48cdc-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="48cdc-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="48cdc-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="48cdc-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="48cdc-125">Schema Name</span></span>  <br/> |<span data-ttu-id="48cdc-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="48cdc-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="48cdc-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="48cdc-127">Validation File</span></span>  <br/> |<span data-ttu-id="48cdc-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="48cdc-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="48cdc-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="48cdc-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="48cdc-130">False</span><span class="sxs-lookup"><span data-stu-id="48cdc-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="48cdc-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="48cdc-131">See also</span></span>



- [<span data-ttu-id="48cdc-132">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="48cdc-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

