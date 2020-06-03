---
title: UserID
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UserId
api_type:
- schema
ms.assetid: 244af9e0-bf3c-46b4-8bfa-9719a1ed3107
description: UserId 元素标识的代理用户或具有文件夹访问权限的用户。
ms.openlocfilehash: 68075e335383835ddce9575d85ba5fa945ed305c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455539"
---
# <a name="userid"></a><span data-ttu-id="27bf8-103">UserID</span><span class="sxs-lookup"><span data-stu-id="27bf8-103">UserId</span></span>

<span data-ttu-id="27bf8-104">**UserId**元素标识的代理用户或具有文件夹访问权限的用户。</span><span class="sxs-lookup"><span data-stu-id="27bf8-104">The **UserId** element identifies a delegate user or a user who has folder access permissions.</span></span> 
  
```xml
<UserId>
   <SID/>
   <PrimarySmtpAddress/>
   <DisplayName/>
   <DistinguishedUser/>
   <ExternalUserIdentity/>
</UserId>
```

 <span data-ttu-id="27bf8-105">**UserIdType**</span><span class="sxs-lookup"><span data-stu-id="27bf8-105">**UserIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="27bf8-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="27bf8-106">Attributes and elements</span></span>

<span data-ttu-id="27bf8-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="27bf8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="27bf8-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="27bf8-108">Attributes</span></span>

<span data-ttu-id="27bf8-109">无。</span><span class="sxs-lookup"><span data-stu-id="27bf8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="27bf8-110">子元素</span><span class="sxs-lookup"><span data-stu-id="27bf8-110">Child elements</span></span>

|<span data-ttu-id="27bf8-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="27bf8-111">**Element**</span></span>|<span data-ttu-id="27bf8-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="27bf8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="27bf8-113">SID</span><span class="sxs-lookup"><span data-stu-id="27bf8-113">SID</span></span>](sid.md) <br/> |<span data-ttu-id="27bf8-114">表示安全标识符（SID）的安全描述符定义语言（SDDL）形式。</span><span class="sxs-lookup"><span data-stu-id="27bf8-114">Represents the security descriptor definition language (SDDL) form of the security identifier (SID).</span></span>  <br/> |
|[<span data-ttu-id="27bf8-115">PrimarySmtpAddress</span><span class="sxs-lookup"><span data-stu-id="27bf8-115">PrimarySmtpAddress</span></span>](primarysmtpaddress.md) <br/> |<span data-ttu-id="27bf8-116">表示要用于代理访问的帐户的主要简单邮件传输协议（SMTP）地址。</span><span class="sxs-lookup"><span data-stu-id="27bf8-116">Represents the primary Simple Mail Transfer Protocol (SMTP) address of an account to be used for delegate access.</span></span>  <br/> |
|[<span data-ttu-id="27bf8-117">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="27bf8-117">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="27bf8-118">定义文件夹、联系人、通讯组列表或代理用户的显示名称。</span><span class="sxs-lookup"><span data-stu-id="27bf8-118">Defines the display name of a folder, contact, distribution list, or delegate user.</span></span>  <br/> |
|[<span data-ttu-id="27bf8-119">DistinguishedUser</span><span class="sxs-lookup"><span data-stu-id="27bf8-119">DistinguishedUser</span></span>](distinguisheduser.md) <br/> |<span data-ttu-id="27bf8-120">标识代理访问的匿名和默认用户帐户。</span><span class="sxs-lookup"><span data-stu-id="27bf8-120">Identifies Anonymous and Default user accounts for delegate access.</span></span>  <br/> |
|[<span data-ttu-id="27bf8-121">ExternalUserIdentity</span><span class="sxs-lookup"><span data-stu-id="27bf8-121">ExternalUserIdentity</span></span>](externaluseridentity.md) <br/> |<span data-ttu-id="27bf8-122">标识具有文件夹访问权限的外部代理用户或外部用户。</span><span class="sxs-lookup"><span data-stu-id="27bf8-122">Identifies an external delegate user or an external user who has folder access permissions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="27bf8-123">父元素</span><span class="sxs-lookup"><span data-stu-id="27bf8-123">Parent elements</span></span>

|<span data-ttu-id="27bf8-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="27bf8-124">**Element**</span></span>|<span data-ttu-id="27bf8-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="27bf8-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="27bf8-126">DelegateUser</span><span class="sxs-lookup"><span data-stu-id="27bf8-126">DelegateUser</span></span>](delegateuser.md) <br/> |<span data-ttu-id="27bf8-127">标识要在邮箱中添加或更新的单个代理。</span><span class="sxs-lookup"><span data-stu-id="27bf8-127">Identifies a single delegate to add or update in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="27bf8-128">权限</span><span class="sxs-lookup"><span data-stu-id="27bf8-128">Permission</span></span>](permission.md) <br/> |<span data-ttu-id="27bf8-129">到文件夹定义用户拥有的访问权限。</span><span class="sxs-lookup"><span data-stu-id="27bf8-129">Defines the access that a user has to a folder.</span></span>  <br/> |
|[<span data-ttu-id="27bf8-130">CalendarPermission</span><span class="sxs-lookup"><span data-stu-id="27bf8-130">CalendarPermission</span></span>](calendarpermission.md) <br/> |<span data-ttu-id="27bf8-131">定义日历文件夹的用户具有的访问权限。</span><span class="sxs-lookup"><span data-stu-id="27bf8-131">Defines the access that a user has to a Calendar folder.</span></span>  <br/> |
|[<span data-ttu-id="27bf8-132">UserIds</span><span class="sxs-lookup"><span data-stu-id="27bf8-132">UserIds</span></span>](userids.md) <br/> |<span data-ttu-id="27bf8-133">包含要从主体邮箱中获取或删除的委派用户的数组。</span><span class="sxs-lookup"><span data-stu-id="27bf8-133">Contains an array of delegate users to get or remove from a principal's mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="27bf8-134">文本值</span><span class="sxs-lookup"><span data-stu-id="27bf8-134">Text value</span></span>

<span data-ttu-id="27bf8-135">无。</span><span class="sxs-lookup"><span data-stu-id="27bf8-135">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="27bf8-136">说明</span><span class="sxs-lookup"><span data-stu-id="27bf8-136">Remarks</span></span>

<span data-ttu-id="27bf8-137">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="27bf8-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="27bf8-138">元素信息</span><span class="sxs-lookup"><span data-stu-id="27bf8-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="27bf8-139">命名空间</span><span class="sxs-lookup"><span data-stu-id="27bf8-139">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="27bf8-140">架构名称</span><span class="sxs-lookup"><span data-stu-id="27bf8-140">Schema Name</span></span>  <br/> |<span data-ttu-id="27bf8-141">类型架构</span><span class="sxs-lookup"><span data-stu-id="27bf8-141">Types schema</span></span>  <br/> |
|<span data-ttu-id="27bf8-142">验证文件</span><span class="sxs-lookup"><span data-stu-id="27bf8-142">Validation File</span></span>  <br/> |<span data-ttu-id="27bf8-143">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="27bf8-143">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="27bf8-144">可以为空</span><span class="sxs-lookup"><span data-stu-id="27bf8-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="27bf8-145">False</span><span class="sxs-lookup"><span data-stu-id="27bf8-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="27bf8-146">另请参阅</span><span class="sxs-lookup"><span data-stu-id="27bf8-146">See also</span></span>



[<span data-ttu-id="27bf8-147">AddDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="27bf8-147">AddDelegate operation</span></span>](adddelegate-operation.md)
  
[<span data-ttu-id="27bf8-148">UpdateDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="27bf8-148">UpdateDelegate operation</span></span>](updatedelegate-operation.md)


- [<span data-ttu-id="27bf8-149">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="27bf8-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="27bf8-150">添加委派</span><span class="sxs-lookup"><span data-stu-id="27bf8-150">Adding Delegates</span></span>](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

