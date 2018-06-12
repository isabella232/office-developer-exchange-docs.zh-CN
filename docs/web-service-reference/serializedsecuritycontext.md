---
title: SerializedSecurityContext
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SerializedSecurityContext
api_type:
- schema
ms.assetid: a02c4fc1-ed1a-40d9-a18e-6cfdae21a690
description: SerializedSecurityContext 元素用于简单对象访问协议 (SOAP) 标头中令牌序列化的服务器到服务器身份验证。 不支持令牌序列化。
ms.openlocfilehash: c5590551dc0780d918b05902e4f48fb9d1390b59
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827363"
---
# <a name="serializedsecuritycontext"></a><span data-ttu-id="4f2a5-104">SerializedSecurityContext</span><span class="sxs-lookup"><span data-stu-id="4f2a5-104">SerializedSecurityContext</span></span>

<span data-ttu-id="4f2a5-105">**SerializedSecurityContext**元素用于简单对象访问协议 (SOAP) 标头中令牌序列化的服务器到服务器身份验证。</span><span class="sxs-lookup"><span data-stu-id="4f2a5-105">The **SerializedSecurityContext** element is used in the Simple Object Access Protocol (SOAP) header for token serialization in server-to-server authentication.</span></span> <span data-ttu-id="4f2a5-106">不支持令牌序列化。</span><span class="sxs-lookup"><span data-stu-id="4f2a5-106">Token serialization is not supported.</span></span> 
  
```xml
<SerializedSecurityContext>
   <UserSid/>
   <GroupSids/>
   <RestrictedGroupSids/>
   <PrimarySmtpAddress/>
</SerializedSecurityContext>
```

 <span data-ttu-id="4f2a5-107">**SerializedSecurityContextType**</span><span class="sxs-lookup"><span data-stu-id="4f2a5-107">**SerializedSecurityContextType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4f2a5-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4f2a5-108">Attributes and elements</span></span>

<span data-ttu-id="4f2a5-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4f2a5-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4f2a5-110">属性</span><span class="sxs-lookup"><span data-stu-id="4f2a5-110">Attributes</span></span>

<span data-ttu-id="4f2a5-111">无。</span><span class="sxs-lookup"><span data-stu-id="4f2a5-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4f2a5-112">子元素</span><span class="sxs-lookup"><span data-stu-id="4f2a5-112">Child elements</span></span>

|<span data-ttu-id="4f2a5-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="4f2a5-113">**Element**</span></span>|<span data-ttu-id="4f2a5-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="4f2a5-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4f2a5-115">UserSid</span><span class="sxs-lookup"><span data-stu-id="4f2a5-115">UserSid</span></span>](usersid.md) <br/> |<span data-ttu-id="4f2a5-116">代表安全描述符定义语言 (SDDL) 窗体的序列化的安全性上下文 SOAP 标头中的用户安全标识符。</span><span class="sxs-lookup"><span data-stu-id="4f2a5-116">Represents the security descriptor definition language (SDDL) form of the user security identifier in a serialized security context SOAP header.</span></span>  <br/> |
|[<span data-ttu-id="4f2a5-117">GroupSids</span><span class="sxs-lookup"><span data-stu-id="4f2a5-117">GroupSids</span></span>](groupsids.md) <br/> |<span data-ttu-id="4f2a5-118">代表 Active Directory 目录服务组对象安全标识符的集合。</span><span class="sxs-lookup"><span data-stu-id="4f2a5-118">Represents a collection of Active Directory directory service group object security identifiers.</span></span>  <br/> |
|[<span data-ttu-id="4f2a5-119">RestrictedGroupSids</span><span class="sxs-lookup"><span data-stu-id="4f2a5-119">RestrictedGroupSids</span></span>](restrictedgroupsids.md) <br/> |<span data-ttu-id="4f2a5-120">表示组安全标识符和受限制的组的属性。</span><span class="sxs-lookup"><span data-stu-id="4f2a5-120">Represents the group security identifier and attributes for a restricted group.</span></span>  <br/> |
|[<span data-ttu-id="4f2a5-121">PrimarySmtpAddress</span><span class="sxs-lookup"><span data-stu-id="4f2a5-121">PrimarySmtpAddress</span></span>](primarysmtpaddress.md) <br/> |<span data-ttu-id="4f2a5-122">代表要用于服务器到服务器授权的帐户的主要简单邮件传输协议 (SMTP) 地址。</span><span class="sxs-lookup"><span data-stu-id="4f2a5-122">Represents the primary Simple Mail Transfer Protocol (SMTP) address of an account to be used for server-to-server authorization.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4f2a5-123">父元素</span><span class="sxs-lookup"><span data-stu-id="4f2a5-123">Parent elements</span></span>

<span data-ttu-id="4f2a5-124">无。</span><span class="sxs-lookup"><span data-stu-id="4f2a5-124">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4f2a5-125">备注</span><span class="sxs-lookup"><span data-stu-id="4f2a5-125">Remarks</span></span>

<span data-ttu-id="4f2a5-126">描述此元素的架构位于运行 Microsoft Exchange Server 2007 的安装了客户端访问服务器 (CAS) 角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="4f2a5-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server (CAS) role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4f2a5-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="4f2a5-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4f2a5-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="4f2a5-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4f2a5-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="4f2a5-129">Schema Name</span></span>  <br/> |<span data-ttu-id="4f2a5-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="4f2a5-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="4f2a5-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="4f2a5-131">Validation File</span></span>  <br/> |<span data-ttu-id="4f2a5-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4f2a5-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4f2a5-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="4f2a5-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="4f2a5-134">False</span><span class="sxs-lookup"><span data-stu-id="4f2a5-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4f2a5-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4f2a5-135">See also</span></span>



- [<span data-ttu-id="4f2a5-136">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="4f2a5-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="4f2a5-137">EWS 中的服务器到服务器授权</span><span class="sxs-lookup"><span data-stu-id="4f2a5-137">Server-to-server authorization in EWS</span></span>](http://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)

