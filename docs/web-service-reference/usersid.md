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
description: UserSid 元素均表示安全描述符定义语言 (SDDL) 窗体的序列化的安全性上下文 SOAP 标头中的用户安全标识符。 不支持令牌序列化。
ms.openlocfilehash: 3c72f68638f99a4ee5081517027f0834ebf65b49
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838492"
---
# <a name="usersid"></a><span data-ttu-id="5df1d-104">UserSid</span><span class="sxs-lookup"><span data-stu-id="5df1d-104">UserSid</span></span>

<span data-ttu-id="5df1d-105">**UserSid**元素均表示安全描述符定义语言 (SDDL) 窗体的序列化的安全性上下文 SOAP 标头中的用户安全标识符。</span><span class="sxs-lookup"><span data-stu-id="5df1d-105">The **UserSid** element represents the security descriptor definition language (SDDL) form of the user security identifier in a serialized security context SOAP header.</span></span> <span data-ttu-id="5df1d-106">不支持令牌序列化。</span><span class="sxs-lookup"><span data-stu-id="5df1d-106">Token serialization is not supported.</span></span> 
  
```xml
<UserSid/>
```

 <span data-ttu-id="5df1d-107">**字符串**</span><span class="sxs-lookup"><span data-stu-id="5df1d-107">**String**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5df1d-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5df1d-108">Attributes and elements</span></span>

<span data-ttu-id="5df1d-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5df1d-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5df1d-110">属性</span><span class="sxs-lookup"><span data-stu-id="5df1d-110">Attributes</span></span>

<span data-ttu-id="5df1d-111">无。</span><span class="sxs-lookup"><span data-stu-id="5df1d-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5df1d-112">子元素</span><span class="sxs-lookup"><span data-stu-id="5df1d-112">Child elements</span></span>

<span data-ttu-id="5df1d-113">无。</span><span class="sxs-lookup"><span data-stu-id="5df1d-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5df1d-114">父元素</span><span class="sxs-lookup"><span data-stu-id="5df1d-114">Parent elements</span></span>

|<span data-ttu-id="5df1d-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="5df1d-115">**Element**</span></span>|<span data-ttu-id="5df1d-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="5df1d-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5df1d-117">SerializedSecurityContext</span><span class="sxs-lookup"><span data-stu-id="5df1d-117">SerializedSecurityContext</span></span>](serializedsecuritycontext.md) <br/> |<span data-ttu-id="5df1d-118">用于服务器到服务器身份验证中的令牌序列化的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="5df1d-118">Used in the SOAP header for token serialization in server-to-server authentication.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5df1d-119">文本值</span><span class="sxs-lookup"><span data-stu-id="5df1d-119">Text value</span></span>

<span data-ttu-id="5df1d-120">文本值表示用户的安全标识符。</span><span class="sxs-lookup"><span data-stu-id="5df1d-120">The text value represents a user's security identifier.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5df1d-121">备注</span><span class="sxs-lookup"><span data-stu-id="5df1d-121">Remarks</span></span>

<span data-ttu-id="5df1d-122">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="5df1d-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5df1d-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="5df1d-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5df1d-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="5df1d-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5df1d-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="5df1d-125">Schema Name</span></span>  <br/> |<span data-ttu-id="5df1d-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="5df1d-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="5df1d-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="5df1d-127">Validation File</span></span>  <br/> |<span data-ttu-id="5df1d-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5df1d-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5df1d-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="5df1d-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="5df1d-130">False</span><span class="sxs-lookup"><span data-stu-id="5df1d-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5df1d-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5df1d-131">See also</span></span>



- [<span data-ttu-id="5df1d-132">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="5df1d-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

