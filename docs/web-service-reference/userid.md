---
title: UserId
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
description: UserId 元素标识委派用户或具有文件夹访问权限的用户。
ms.openlocfilehash: 8e9867f5a8cdd62dd2dae55fbf527595ac14f46d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838469"
---
# <a name="userid"></a><span data-ttu-id="ec01e-103">UserId</span><span class="sxs-lookup"><span data-stu-id="ec01e-103">UserId</span></span>

<span data-ttu-id="ec01e-104">**UserId**元素标识委派用户或具有文件夹访问权限的用户。</span><span class="sxs-lookup"><span data-stu-id="ec01e-104">The **UserId** element identifies a delegate user or a user who has folder access permissions.</span></span> 
  
```xml
<UserId>
   <SID/>
   <PrimarySmtpAddress/>
   <DisplayName/>
   <DistinguishedUser/>
   <ExternalUserIdentity/>
</UserId>
```

 <span data-ttu-id="ec01e-105">**UserIdType**</span><span class="sxs-lookup"><span data-stu-id="ec01e-105">**UserIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ec01e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ec01e-106">Attributes and elements</span></span>

<span data-ttu-id="ec01e-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ec01e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ec01e-108">属性</span><span class="sxs-lookup"><span data-stu-id="ec01e-108">Attributes</span></span>

<span data-ttu-id="ec01e-109">无。</span><span class="sxs-lookup"><span data-stu-id="ec01e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ec01e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ec01e-110">Child elements</span></span>

|<span data-ttu-id="ec01e-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="ec01e-111">**Element**</span></span>|<span data-ttu-id="ec01e-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="ec01e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ec01e-113">SID</span><span class="sxs-lookup"><span data-stu-id="ec01e-113">SID</span></span>](sid.md) <br/> |<span data-ttu-id="ec01e-114">代表安全描述符定义语言 (SDDL) 窗体的安全标识符 (SID)。</span><span class="sxs-lookup"><span data-stu-id="ec01e-114">Represents the security descriptor definition language (SDDL) form of the security identifier (SID).</span></span>  <br/> |
|[<span data-ttu-id="ec01e-115">PrimarySmtpAddress</span><span class="sxs-lookup"><span data-stu-id="ec01e-115">PrimarySmtpAddress</span></span>](primarysmtpaddress.md) <br/> |<span data-ttu-id="ec01e-116">表示用于代理访问的帐户的主要简单邮件传输协议 (SMTP) 地址。</span><span class="sxs-lookup"><span data-stu-id="ec01e-116">Represents the primary Simple Mail Transfer Protocol (SMTP) address of an account to be used for delegate access.</span></span>  <br/> |
|[<span data-ttu-id="ec01e-117">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="ec01e-117">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="ec01e-118">定义文件夹、 联系人、 通讯组列表或代理用户的显示名称。</span><span class="sxs-lookup"><span data-stu-id="ec01e-118">Defines the display name of a folder, contact, distribution list, or delegate user.</span></span>  <br/> |
|[<span data-ttu-id="ec01e-119">DistinguishedUser</span><span class="sxs-lookup"><span data-stu-id="ec01e-119">DistinguishedUser</span></span>](distinguisheduser.md) <br/> |<span data-ttu-id="ec01e-120">标识匿名和默认代理访问的用户帐户。</span><span class="sxs-lookup"><span data-stu-id="ec01e-120">Identifies Anonymous and Default user accounts for delegate access.</span></span>  <br/> |
|[<span data-ttu-id="ec01e-121">ExternalUserIdentity</span><span class="sxs-lookup"><span data-stu-id="ec01e-121">ExternalUserIdentity</span></span>](externaluseridentity.md) <br/> |<span data-ttu-id="ec01e-122">标识外部委托用户或外部用户拥有文件夹访问权限。</span><span class="sxs-lookup"><span data-stu-id="ec01e-122">Identifies an external delegate user or an external user who has folder access permissions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ec01e-123">父元素</span><span class="sxs-lookup"><span data-stu-id="ec01e-123">Parent elements</span></span>

|<span data-ttu-id="ec01e-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="ec01e-124">**Element**</span></span>|<span data-ttu-id="ec01e-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="ec01e-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ec01e-126">DelegateUser</span><span class="sxs-lookup"><span data-stu-id="ec01e-126">DelegateUser</span></span>](delegateuser.md) <br/> |<span data-ttu-id="ec01e-127">标识要添加或更新的邮箱中的单个委托。</span><span class="sxs-lookup"><span data-stu-id="ec01e-127">Identifies a single delegate to add or update in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="ec01e-128">权限</span><span class="sxs-lookup"><span data-stu-id="ec01e-128">Permission</span></span>](permission.md) <br/> |<span data-ttu-id="ec01e-129">到文件夹定义用户拥有的访问权限。</span><span class="sxs-lookup"><span data-stu-id="ec01e-129">Defines the access that a user has to a folder.</span></span>  <br/> |
|[<span data-ttu-id="ec01e-130">CalendarPermission</span><span class="sxs-lookup"><span data-stu-id="ec01e-130">CalendarPermission</span></span>](calendarpermission.md) <br/> |<span data-ttu-id="ec01e-131">定义日历文件夹的用户具有的访问权限。</span><span class="sxs-lookup"><span data-stu-id="ec01e-131">Defines the access that a user has to a Calendar folder.</span></span>  <br/> |
|[<span data-ttu-id="ec01e-132">UserIds</span><span class="sxs-lookup"><span data-stu-id="ec01e-132">UserIds</span></span>](userids.md) <br/> |<span data-ttu-id="ec01e-133">包含用于获取或删除主体的邮箱的委派用户的数组。</span><span class="sxs-lookup"><span data-stu-id="ec01e-133">Contains an array of delegate users to get or remove from a principal's mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ec01e-134">文本值</span><span class="sxs-lookup"><span data-stu-id="ec01e-134">Text value</span></span>

<span data-ttu-id="ec01e-135">无。</span><span class="sxs-lookup"><span data-stu-id="ec01e-135">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ec01e-136">备注</span><span class="sxs-lookup"><span data-stu-id="ec01e-136">Remarks</span></span>

<span data-ttu-id="ec01e-137">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ec01e-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ec01e-138">元素信息</span><span class="sxs-lookup"><span data-stu-id="ec01e-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ec01e-139">命名空间</span><span class="sxs-lookup"><span data-stu-id="ec01e-139">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ec01e-140">架构名称</span><span class="sxs-lookup"><span data-stu-id="ec01e-140">Schema Name</span></span>  <br/> |<span data-ttu-id="ec01e-141">类型架构</span><span class="sxs-lookup"><span data-stu-id="ec01e-141">Types schema</span></span>  <br/> |
|<span data-ttu-id="ec01e-142">验证文件</span><span class="sxs-lookup"><span data-stu-id="ec01e-142">Validation File</span></span>  <br/> |<span data-ttu-id="ec01e-143">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ec01e-143">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ec01e-144">可以为空</span><span class="sxs-lookup"><span data-stu-id="ec01e-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="ec01e-145">False</span><span class="sxs-lookup"><span data-stu-id="ec01e-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ec01e-146">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ec01e-146">See also</span></span>



[<span data-ttu-id="ec01e-147">AddDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="ec01e-147">AddDelegate operation</span></span>](adddelegate-operation.md)
  
[<span data-ttu-id="ec01e-148">UpdateDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="ec01e-148">UpdateDelegate operation</span></span>](updatedelegate-operation.md)


- [<span data-ttu-id="ec01e-149">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="ec01e-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="ec01e-150">添加代理人</span><span class="sxs-lookup"><span data-stu-id="ec01e-150">Adding Delegates</span></span>](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

