---
title: ViewPrivateItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ViewPrivateItems
api_type:
- schema
ms.assetid: 80b949ac-440c-4a01-b428-ebafb5b1b802
description: ViewPrivateItems 元素指示委托用户或客户端应用程序是否有权查看的主体的邮箱中的专用的项目。
ms.openlocfilehash: c35f24ae79e907424cb5cfb0efeec2307334ca12
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838530"
---
# <a name="viewprivateitems"></a><span data-ttu-id="3bdcc-103">ViewPrivateItems</span><span class="sxs-lookup"><span data-stu-id="3bdcc-103">ViewPrivateItems</span></span>

<span data-ttu-id="3bdcc-104">**ViewPrivateItems**元素指示委托用户或客户端应用程序是否有权查看的主体的邮箱中的专用的项目。</span><span class="sxs-lookup"><span data-stu-id="3bdcc-104">The **ViewPrivateItems** element indicates whether a delegate user or client application has permission to view private items in the principal's mailbox.</span></span> 
  
```XML
<ViewPrivateItems>true | false</ViewPrivateItems>
```

 <span data-ttu-id="3bdcc-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="3bdcc-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3bdcc-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="3bdcc-106">Attributes and elements</span></span>

<span data-ttu-id="3bdcc-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3bdcc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3bdcc-108">属性</span><span class="sxs-lookup"><span data-stu-id="3bdcc-108">Attributes</span></span>

<span data-ttu-id="3bdcc-109">无。</span><span class="sxs-lookup"><span data-stu-id="3bdcc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3bdcc-110">子元素</span><span class="sxs-lookup"><span data-stu-id="3bdcc-110">Child elements</span></span>

<span data-ttu-id="3bdcc-111">无。</span><span class="sxs-lookup"><span data-stu-id="3bdcc-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3bdcc-112">父元素</span><span class="sxs-lookup"><span data-stu-id="3bdcc-112">Parent elements</span></span>

|<span data-ttu-id="3bdcc-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="3bdcc-113">**Element**</span></span>|<span data-ttu-id="3bdcc-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="3bdcc-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3bdcc-115">DelegateUser</span><span class="sxs-lookup"><span data-stu-id="3bdcc-115">DelegateUser</span></span>](delegateuser.md) <br/> |<span data-ttu-id="3bdcc-116">标识要添加或更新的邮箱中的单个委托。</span><span class="sxs-lookup"><span data-stu-id="3bdcc-116">Identifies a single delegate to add or update in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="3bdcc-117">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="3bdcc-117">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="3bdcc-p101">包含客户端的权利基础的项或文件夹的权限设置。此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="3bdcc-p101">Contains the client's rights based on the permission settings for the item or folder. This element is read-only.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3bdcc-120">文本值</span><span class="sxs-lookup"><span data-stu-id="3bdcc-120">Text value</span></span>

<span data-ttu-id="3bdcc-121">值为**true**指示委托或客户端可以的主体的邮箱中查看的私有项目。</span><span class="sxs-lookup"><span data-stu-id="3bdcc-121">A value of **true** indicates that the delegate or client can view private items in the principal's mailbox.</span></span> <span data-ttu-id="3bdcc-122">如果值为**false**指示的专用项目看不到委托或客户端。</span><span class="sxs-lookup"><span data-stu-id="3bdcc-122">A value of **false** indicates that private items are not visible to a delegate or client.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3bdcc-123">备注</span><span class="sxs-lookup"><span data-stu-id="3bdcc-123">Remarks</span></span>

<span data-ttu-id="3bdcc-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="3bdcc-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3bdcc-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="3bdcc-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3bdcc-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="3bdcc-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3bdcc-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="3bdcc-127">Schema Name</span></span>  <br/> |<span data-ttu-id="3bdcc-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="3bdcc-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="3bdcc-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="3bdcc-129">Validation File</span></span>  <br/> |<span data-ttu-id="3bdcc-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3bdcc-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3bdcc-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="3bdcc-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="3bdcc-132">False</span><span class="sxs-lookup"><span data-stu-id="3bdcc-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3bdcc-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3bdcc-133">See also</span></span>



[<span data-ttu-id="3bdcc-134">AddDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="3bdcc-134">AddDelegate operation</span></span>](adddelegate-operation.md)
  
[<span data-ttu-id="3bdcc-135">UpdateDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="3bdcc-135">UpdateDelegate operation</span></span>](updatedelegate-operation.md)


- [<span data-ttu-id="3bdcc-136">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="3bdcc-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="3bdcc-137">添加代理人</span><span class="sxs-lookup"><span data-stu-id="3bdcc-137">Adding Delegates</span></span>](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

