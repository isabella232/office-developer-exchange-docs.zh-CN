---
title: DistinguishedUser
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DistinguishedUser
api_type:
- schema
ms.assetid: 9362699d-666a-4acf-8fa1-c6669f0a2ae5
description: DistinguishedUser 元素标识代理访问的匿名帐户和默认用户帐户。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: 922c36251290d7090cdafbed9e570144593ca97e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530731"
---
# <a name="distinguisheduser"></a><span data-ttu-id="a36cc-104">DistinguishedUser</span><span class="sxs-lookup"><span data-stu-id="a36cc-104">DistinguishedUser</span></span>

<span data-ttu-id="a36cc-105">**DistinguishedUser**元素标识代理访问的匿名帐户和默认用户帐户。</span><span class="sxs-lookup"><span data-stu-id="a36cc-105">The **DistinguishedUser** element identifies Anonymous and Default user accounts for delegate access.</span></span> <span data-ttu-id="a36cc-106">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="a36cc-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<DistinguishedUser>Default or Anonymous</DistinguishedUser>
```

 <span data-ttu-id="a36cc-107">**DistinguishedUserType**</span><span class="sxs-lookup"><span data-stu-id="a36cc-107">**DistinguishedUserType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a36cc-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a36cc-108">Attributes and elements</span></span>

<span data-ttu-id="a36cc-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a36cc-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a36cc-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="a36cc-110">Attributes</span></span>

<span data-ttu-id="a36cc-111">无。</span><span class="sxs-lookup"><span data-stu-id="a36cc-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a36cc-112">子元素</span><span class="sxs-lookup"><span data-stu-id="a36cc-112">Child elements</span></span>

<span data-ttu-id="a36cc-113">无。</span><span class="sxs-lookup"><span data-stu-id="a36cc-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a36cc-114">父元素</span><span class="sxs-lookup"><span data-stu-id="a36cc-114">Parent elements</span></span>

|<span data-ttu-id="a36cc-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="a36cc-115">**Element**</span></span>|<span data-ttu-id="a36cc-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="a36cc-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a36cc-117">UserId</span><span class="sxs-lookup"><span data-stu-id="a36cc-117">UserId</span></span>](userid.md) <br/> |<span data-ttu-id="a36cc-118">标识代理用户或具有文件夹访问权限的用户。</span><span class="sxs-lookup"><span data-stu-id="a36cc-118">Identifies a delegate user or a user who has folder access permissions.</span></span> <span data-ttu-id="a36cc-119">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="a36cc-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a36cc-120">文本值</span><span class="sxs-lookup"><span data-stu-id="a36cc-120">Text value</span></span>

<span data-ttu-id="a36cc-121">**默认**的文本值描述了为添加到主体邮箱的用户委派用户的默认设置。</span><span class="sxs-lookup"><span data-stu-id="a36cc-121">A text value of **Default** describes the default setting for delegate users who are added to the principal's mailbox.</span></span> <span data-ttu-id="a36cc-122">"**匿名**" 文本值描述匿名用户对主体邮箱的代理访问设置。</span><span class="sxs-lookup"><span data-stu-id="a36cc-122">A text value of **Anonymous** describes the delegate access settings that anonymous users have on the principal's mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a36cc-123">说明</span><span class="sxs-lookup"><span data-stu-id="a36cc-123">Remarks</span></span>

<span data-ttu-id="a36cc-124">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a36cc-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a36cc-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="a36cc-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a36cc-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="a36cc-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a36cc-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="a36cc-127">Schema Name</span></span>  <br/> |<span data-ttu-id="a36cc-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="a36cc-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="a36cc-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="a36cc-129">Validation File</span></span>  <br/> |<span data-ttu-id="a36cc-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a36cc-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a36cc-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="a36cc-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="a36cc-132">False</span><span class="sxs-lookup"><span data-stu-id="a36cc-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a36cc-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a36cc-133">See also</span></span>

- [<span data-ttu-id="a36cc-134">AddDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="a36cc-134">AddDelegate operation</span></span>](adddelegate-operation.md)  
- [<span data-ttu-id="a36cc-135">UpdateDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="a36cc-135">UpdateDelegate operation</span></span>](updatedelegate-operation.md)
- [<span data-ttu-id="a36cc-136">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a36cc-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="a36cc-137">添加委派</span><span class="sxs-lookup"><span data-stu-id="a36cc-137">Adding Delegates</span></span>](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

