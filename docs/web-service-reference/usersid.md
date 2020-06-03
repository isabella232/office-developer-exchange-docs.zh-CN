---
title: UserSid
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UserSid
api_type:
- schema
ms.assetid: f8a0dcd9-8564-4e35-b307-c5d2761b48d8
description: UserSid 元素表示序列化安全上下文 SOAP 标头中的用户安全标识符的安全描述符定义语言（SDDL）形式。 不支持令牌序列化。
ms.openlocfilehash: b8ee51b1998546fc4ab14bd3666192ae63c8dba8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462015"
---
# <a name="usersid"></a><span data-ttu-id="d5d2c-104">UserSid</span><span class="sxs-lookup"><span data-stu-id="d5d2c-104">UserSid</span></span>

<span data-ttu-id="d5d2c-105">**UserSid**元素表示序列化安全上下文 SOAP 标头中的用户安全标识符的安全描述符定义语言（SDDL）形式。</span><span class="sxs-lookup"><span data-stu-id="d5d2c-105">The **UserSid** element represents the security descriptor definition language (SDDL) form of the user security identifier in a serialized security context SOAP header.</span></span> <span data-ttu-id="d5d2c-106">不支持令牌序列化。</span><span class="sxs-lookup"><span data-stu-id="d5d2c-106">Token serialization is not supported.</span></span> 
  
```xml
<UserSid/>
```

 <span data-ttu-id="d5d2c-107">**String**</span><span class="sxs-lookup"><span data-stu-id="d5d2c-107">**String**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d5d2c-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d5d2c-108">Attributes and elements</span></span>

<span data-ttu-id="d5d2c-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d5d2c-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d5d2c-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="d5d2c-110">Attributes</span></span>

<span data-ttu-id="d5d2c-111">无。</span><span class="sxs-lookup"><span data-stu-id="d5d2c-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d5d2c-112">子元素</span><span class="sxs-lookup"><span data-stu-id="d5d2c-112">Child elements</span></span>

<span data-ttu-id="d5d2c-113">无。</span><span class="sxs-lookup"><span data-stu-id="d5d2c-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d5d2c-114">父元素</span><span class="sxs-lookup"><span data-stu-id="d5d2c-114">Parent elements</span></span>

|<span data-ttu-id="d5d2c-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="d5d2c-115">**Element**</span></span>|<span data-ttu-id="d5d2c-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="d5d2c-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d5d2c-117">SerializedSecurityContext</span><span class="sxs-lookup"><span data-stu-id="d5d2c-117">SerializedSecurityContext</span></span>](serializedsecuritycontext.md) <br/> |<span data-ttu-id="d5d2c-118">在服务器到服务器身份验证中用于令牌序列化的 SOAP 标头中使用。</span><span class="sxs-lookup"><span data-stu-id="d5d2c-118">Used in the SOAP header for token serialization in server-to-server authentication.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d5d2c-119">文本值</span><span class="sxs-lookup"><span data-stu-id="d5d2c-119">Text value</span></span>

<span data-ttu-id="d5d2c-120">该文本值代表用户的安全标识符。</span><span class="sxs-lookup"><span data-stu-id="d5d2c-120">The text value represents a user's security identifier.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d5d2c-121">说明</span><span class="sxs-lookup"><span data-stu-id="d5d2c-121">Remarks</span></span>

<span data-ttu-id="d5d2c-122">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d5d2c-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d5d2c-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="d5d2c-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d5d2c-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="d5d2c-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d5d2c-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="d5d2c-125">Schema Name</span></span>  <br/> |<span data-ttu-id="d5d2c-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="d5d2c-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="d5d2c-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="d5d2c-127">Validation File</span></span>  <br/> |<span data-ttu-id="d5d2c-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d5d2c-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d5d2c-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="d5d2c-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="d5d2c-130">False</span><span class="sxs-lookup"><span data-stu-id="d5d2c-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d5d2c-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d5d2c-131">See also</span></span>



- [<span data-ttu-id="d5d2c-132">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d5d2c-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

