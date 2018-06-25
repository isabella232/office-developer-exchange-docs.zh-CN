---
title: 邮箱 （可用性）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Mailbox
api_type:
- schema
ms.assetid: affd192e-8914-473f-9098-d9bdf898de2c
description: 邮箱元素表示 SetUserOofSettings 邮箱用户或 GetUserOofSettings 请求。
ms.openlocfilehash: 2e901ae0df56542f56f247184254294735018468
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826254"
---
# <a name="mailbox-availability"></a><span data-ttu-id="f35dc-103">邮箱 （可用性）</span><span class="sxs-lookup"><span data-stu-id="f35dc-103">Mailbox (Availability)</span></span>

<span data-ttu-id="f35dc-104">**邮箱**元素表示 SetUserOofSettings 邮箱用户或 GetUserOofSettings 请求。</span><span class="sxs-lookup"><span data-stu-id="f35dc-104">The **Mailbox** element represents the mailbox user for a SetUserOofSettings or GetUserOofSettings request.</span></span> 
  
```xml
<Mailbox>
   <Name>...</Name>
   <Address>...</Address>
   <RoutingType>...</RoutingType>
</Mailbox>
```

<span data-ttu-id="f35dc-105">**EmailAddressType**</span><span class="sxs-lookup"><span data-stu-id="f35dc-105">**EmailAddressType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="f35dc-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f35dc-106">Attributes and elements</span></span>

<span data-ttu-id="f35dc-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f35dc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f35dc-108">属性</span><span class="sxs-lookup"><span data-stu-id="f35dc-108">Attributes</span></span>

<span data-ttu-id="f35dc-109">无。</span><span class="sxs-lookup"><span data-stu-id="f35dc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f35dc-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f35dc-110">Child elements</span></span>

|<span data-ttu-id="f35dc-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="f35dc-111">**Element**</span></span>|<span data-ttu-id="f35dc-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="f35dc-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f35dc-113">名称 （电子邮件地址）</span><span class="sxs-lookup"><span data-stu-id="f35dc-113">Name (EmailAddress)</span></span>](name-emailaddress.md) <br/> |<span data-ttu-id="f35dc-114">代表邮箱用户的显示名称。</span><span class="sxs-lookup"><span data-stu-id="f35dc-114">Represents the display name of the mailbox user.</span></span> <span data-ttu-id="f35dc-115">此元素是在 SetUserOofSettingsRequest 可选的。</span><span class="sxs-lookup"><span data-stu-id="f35dc-115">This element is optional in the SetUserOofSettingsRequest.</span></span> <span data-ttu-id="f35dc-116">GetUserOofSettingsRequest 将返回此元素。</span><span class="sxs-lookup"><span data-stu-id="f35dc-116">The GetUserOofSettingsRequest will return this element.</span></span>  <br/> |
|[<span data-ttu-id="f35dc-117">地址 （字符串）</span><span class="sxs-lookup"><span data-stu-id="f35dc-117">Address (string)</span></span>](address-string.md) <br/> |<span data-ttu-id="f35dc-118">代表邮箱用户的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="f35dc-118">Represents the e-mail address of the mailbox user.</span></span> <span data-ttu-id="f35dc-119">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="f35dc-119">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="f35dc-120">RoutingType （电子邮件地址）</span><span class="sxs-lookup"><span data-stu-id="f35dc-120">RoutingType (EmailAddress)</span></span>](routingtype-emailaddress.md) <br/> |<span data-ttu-id="f35dc-121">代表邮件路由的协议。</span><span class="sxs-lookup"><span data-stu-id="f35dc-121">Represents the routing protocol for the message.</span></span> <span data-ttu-id="f35dc-122">此元素是在 SetUserOofSettingsRequest 可选的。</span><span class="sxs-lookup"><span data-stu-id="f35dc-122">This element is optional in the SetUserOofSettingsRequest.</span></span> <span data-ttu-id="f35dc-123">GetUserOofSettingsRequest 将返回此元素。</span><span class="sxs-lookup"><span data-stu-id="f35dc-123">The GetUserOofSettingsRequest will return this element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f35dc-124">父元素</span><span class="sxs-lookup"><span data-stu-id="f35dc-124">Parent elements</span></span>

|<span data-ttu-id="f35dc-125">**元素**</span><span class="sxs-lookup"><span data-stu-id="f35dc-125">**Element**</span></span>|<span data-ttu-id="f35dc-126">**说明**</span><span class="sxs-lookup"><span data-stu-id="f35dc-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f35dc-127">GetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="f35dc-127">GetUserOofSettingsRequest</span></span>](getuseroofsettingsrequest.md) <br/> |<span data-ttu-id="f35dc-128">用于获取邮箱用户的外出 (OOF) 设置和消息。</span><span class="sxs-lookup"><span data-stu-id="f35dc-128">Used to get a mailbox user's Out of Office (OOF) settings and messages.</span></span>  <br/> <span data-ttu-id="f35dc-129">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="f35dc-129">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserOofSettingsRequest` <br/> |
|[<span data-ttu-id="f35dc-130">SetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="f35dc-130">SetUserOofSettingsRequest</span></span>](setuseroofsettingsrequest.md) <br/> |<span data-ttu-id="f35dc-131">用于设置邮箱用户的 OOF 设置和消息。</span><span class="sxs-lookup"><span data-stu-id="f35dc-131">Used to set a mailbox user's OOF settings and messages.</span></span>  <br/> <span data-ttu-id="f35dc-132">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="f35dc-132">The following is the XPath expression to this element:</span></span>  <br/>  `/SetUserOofSettingsRequest` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f35dc-133">注解</span><span class="sxs-lookup"><span data-stu-id="f35dc-133">Remarks</span></span>

<span data-ttu-id="f35dc-134">电子邮件地址用于标识日历文件夹包含 OOF 设置。</span><span class="sxs-lookup"><span data-stu-id="f35dc-134">The e-mail address is used to identify the calendar folder that contains the OOF settings.</span></span> 
  
<span data-ttu-id="f35dc-135">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f35dc-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f35dc-136">元素信息</span><span class="sxs-lookup"><span data-stu-id="f35dc-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f35dc-137">命名空间</span><span class="sxs-lookup"><span data-stu-id="f35dc-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f35dc-138">架构名称</span><span class="sxs-lookup"><span data-stu-id="f35dc-138">Schema Name</span></span>  <br/> |<span data-ttu-id="f35dc-139">类型架构</span><span class="sxs-lookup"><span data-stu-id="f35dc-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="f35dc-140">验证文件</span><span class="sxs-lookup"><span data-stu-id="f35dc-140">Validation File</span></span>  <br/> |<span data-ttu-id="f35dc-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f35dc-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f35dc-142">可以为空</span><span class="sxs-lookup"><span data-stu-id="f35dc-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="f35dc-143">False</span><span class="sxs-lookup"><span data-stu-id="f35dc-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f35dc-144">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f35dc-144">See also</span></span>

- [<span data-ttu-id="f35dc-145">GetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="f35dc-145">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)
- [<span data-ttu-id="f35dc-146">SetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="f35dc-146">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

