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
description: 在服务器到服务器身份验证中，在令牌序列化的简单对象访问协议（SOAP）头中使用 SerializedSecurityContext 元素。 不支持令牌序列化。
ms.openlocfilehash: 58fea1c7f613315d59e81935561f92f318afc769
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462050"
---
# <a name="serializedsecuritycontext"></a><span data-ttu-id="2d4ec-104">SerializedSecurityContext</span><span class="sxs-lookup"><span data-stu-id="2d4ec-104">SerializedSecurityContext</span></span>

<span data-ttu-id="2d4ec-105">在服务器到服务器身份验证中，在令牌序列化的简单对象访问协议（SOAP）头中使用**SerializedSecurityContext**元素。</span><span class="sxs-lookup"><span data-stu-id="2d4ec-105">The **SerializedSecurityContext** element is used in the Simple Object Access Protocol (SOAP) header for token serialization in server-to-server authentication.</span></span> <span data-ttu-id="2d4ec-106">不支持令牌序列化。</span><span class="sxs-lookup"><span data-stu-id="2d4ec-106">Token serialization is not supported.</span></span> 
  
```xml
<SerializedSecurityContext>
   <UserSid/>
   <GroupSids/>
   <RestrictedGroupSids/>
   <PrimarySmtpAddress/>
</SerializedSecurityContext>
```

 <span data-ttu-id="2d4ec-107">**SerializedSecurityContextType**</span><span class="sxs-lookup"><span data-stu-id="2d4ec-107">**SerializedSecurityContextType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2d4ec-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2d4ec-108">Attributes and elements</span></span>

<span data-ttu-id="2d4ec-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2d4ec-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2d4ec-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="2d4ec-110">Attributes</span></span>

<span data-ttu-id="2d4ec-111">无。</span><span class="sxs-lookup"><span data-stu-id="2d4ec-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2d4ec-112">子元素</span><span class="sxs-lookup"><span data-stu-id="2d4ec-112">Child elements</span></span>

|<span data-ttu-id="2d4ec-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="2d4ec-113">**Element**</span></span>|<span data-ttu-id="2d4ec-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="2d4ec-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2d4ec-115">UserSid</span><span class="sxs-lookup"><span data-stu-id="2d4ec-115">UserSid</span></span>](usersid.md) <br/> |<span data-ttu-id="2d4ec-116">表示在序列化安全上下文 SOAP 标头中的用户安全标识符的安全描述符定义语言（SDDL）形式。</span><span class="sxs-lookup"><span data-stu-id="2d4ec-116">Represents the security descriptor definition language (SDDL) form of the user security identifier in a serialized security context SOAP header.</span></span>  <br/> |
|[<span data-ttu-id="2d4ec-117">GroupSids</span><span class="sxs-lookup"><span data-stu-id="2d4ec-117">GroupSids</span></span>](groupsids.md) <br/> |<span data-ttu-id="2d4ec-118">表示 Active Directory 目录服务组对象安全标识符的集合。</span><span class="sxs-lookup"><span data-stu-id="2d4ec-118">Represents a collection of Active Directory directory service group object security identifiers.</span></span>  <br/> |
|[<span data-ttu-id="2d4ec-119">RestrictedGroupSids</span><span class="sxs-lookup"><span data-stu-id="2d4ec-119">RestrictedGroupSids</span></span>](restrictedgroupsids.md) <br/> |<span data-ttu-id="2d4ec-120">表示受限制的组的组安全标识符和属性。</span><span class="sxs-lookup"><span data-stu-id="2d4ec-120">Represents the group security identifier and attributes for a restricted group.</span></span>  <br/> |
|[<span data-ttu-id="2d4ec-121">PrimarySmtpAddress</span><span class="sxs-lookup"><span data-stu-id="2d4ec-121">PrimarySmtpAddress</span></span>](primarysmtpaddress.md) <br/> |<span data-ttu-id="2d4ec-122">表示要用于服务器到服务器身份验证的帐户的主要简单邮件传输协议（SMTP）地址。</span><span class="sxs-lookup"><span data-stu-id="2d4ec-122">Represents the primary Simple Mail Transfer Protocol (SMTP) address of an account to be used for server-to-server authorization.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2d4ec-123">父元素</span><span class="sxs-lookup"><span data-stu-id="2d4ec-123">Parent elements</span></span>

<span data-ttu-id="2d4ec-124">无。</span><span class="sxs-lookup"><span data-stu-id="2d4ec-124">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2d4ec-125">说明</span><span class="sxs-lookup"><span data-stu-id="2d4ec-125">Remarks</span></span>

<span data-ttu-id="2d4ec-126">描述此元素的架构位于运行 Microsoft Exchange Server 2007 且安装了客户端访问服务器（CAS）角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2d4ec-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server (CAS) role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2d4ec-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="2d4ec-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2d4ec-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="2d4ec-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2d4ec-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="2d4ec-129">Schema Name</span></span>  <br/> |<span data-ttu-id="2d4ec-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="2d4ec-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="2d4ec-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="2d4ec-131">Validation File</span></span>  <br/> |<span data-ttu-id="2d4ec-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2d4ec-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2d4ec-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="2d4ec-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="2d4ec-134">False</span><span class="sxs-lookup"><span data-stu-id="2d4ec-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2d4ec-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2d4ec-135">See also</span></span>



- [<span data-ttu-id="2d4ec-136">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2d4ec-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="2d4ec-137">EWS 中的服务器到服务器授权</span><span class="sxs-lookup"><span data-stu-id="2d4ec-137">Server-to-server authorization in EWS</span></span>](https://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)

