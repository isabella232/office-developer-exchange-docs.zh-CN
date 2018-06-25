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
description: DistinguishedUser 元素标识匿名和默认代理访问的用户帐户。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。
ms.openlocfilehash: b14be22bfe5316b9ab254e63cdfa0757596b8b92
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753957"
---
# <a name="distinguisheduser"></a><span data-ttu-id="4f3b8-104">DistinguishedUser</span><span class="sxs-lookup"><span data-stu-id="4f3b8-104">DistinguishedUser</span></span>

<span data-ttu-id="4f3b8-105">**DistinguishedUser**元素标识匿名和默认代理访问的用户帐户。</span><span class="sxs-lookup"><span data-stu-id="4f3b8-105">The **DistinguishedUser** element identifies Anonymous and Default user accounts for delegate access.</span></span> <span data-ttu-id="4f3b8-106">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="4f3b8-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<DistinguishedUser>Default or Anonymous</DistinguishedUser>
```

 <span data-ttu-id="4f3b8-107">**DistinguishedUserType**</span><span class="sxs-lookup"><span data-stu-id="4f3b8-107">**DistinguishedUserType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4f3b8-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4f3b8-108">Attributes and elements</span></span>

<span data-ttu-id="4f3b8-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4f3b8-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4f3b8-110">属性</span><span class="sxs-lookup"><span data-stu-id="4f3b8-110">Attributes</span></span>

<span data-ttu-id="4f3b8-111">无。</span><span class="sxs-lookup"><span data-stu-id="4f3b8-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4f3b8-112">子元素</span><span class="sxs-lookup"><span data-stu-id="4f3b8-112">Child elements</span></span>

<span data-ttu-id="4f3b8-113">无。</span><span class="sxs-lookup"><span data-stu-id="4f3b8-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4f3b8-114">父元素</span><span class="sxs-lookup"><span data-stu-id="4f3b8-114">Parent elements</span></span>

|<span data-ttu-id="4f3b8-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="4f3b8-115">**Element**</span></span>|<span data-ttu-id="4f3b8-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="4f3b8-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4f3b8-117">用户 Id</span><span class="sxs-lookup"><span data-stu-id="4f3b8-117">UserId</span></span>](userid.md) <br/> |<span data-ttu-id="4f3b8-118">标识委派用户或具有文件夹访问权限的用户。</span><span class="sxs-lookup"><span data-stu-id="4f3b8-118">Identifies a delegate user or a user who has folder access permissions.</span></span> <span data-ttu-id="4f3b8-119">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="4f3b8-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4f3b8-120">文本值</span><span class="sxs-lookup"><span data-stu-id="4f3b8-120">Text value</span></span>

<span data-ttu-id="4f3b8-121">**默认**文本值介绍委托用户添加到的主体的邮箱的默认设置。</span><span class="sxs-lookup"><span data-stu-id="4f3b8-121">A text value of **Default** describes the default setting for delegate users who are added to the principal's mailbox.</span></span> <span data-ttu-id="4f3b8-122">文本值的**匿名**介绍匿名用户具有的主体的邮箱的委托访问设置。</span><span class="sxs-lookup"><span data-stu-id="4f3b8-122">A text value of **Anonymous** describes the delegate access settings that anonymous users have on the principal's mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4f3b8-123">备注</span><span class="sxs-lookup"><span data-stu-id="4f3b8-123">Remarks</span></span>

<span data-ttu-id="4f3b8-124">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="4f3b8-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4f3b8-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="4f3b8-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4f3b8-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="4f3b8-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4f3b8-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="4f3b8-127">Schema Name</span></span>  <br/> |<span data-ttu-id="4f3b8-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="4f3b8-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="4f3b8-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="4f3b8-129">Validation File</span></span>  <br/> |<span data-ttu-id="4f3b8-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4f3b8-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4f3b8-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="4f3b8-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="4f3b8-132">False</span><span class="sxs-lookup"><span data-stu-id="4f3b8-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4f3b8-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4f3b8-133">See also</span></span>

- [<span data-ttu-id="4f3b8-134">AddDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="4f3b8-134">AddDelegate operation</span></span>](adddelegate-operation.md)  
- [<span data-ttu-id="4f3b8-135">UpdateDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="4f3b8-135">UpdateDelegate operation</span></span>](updatedelegate-operation.md)
- [<span data-ttu-id="4f3b8-136">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="4f3b8-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="4f3b8-137">添加代理人</span><span class="sxs-lookup"><span data-stu-id="4f3b8-137">Adding Delegates</span></span>](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

