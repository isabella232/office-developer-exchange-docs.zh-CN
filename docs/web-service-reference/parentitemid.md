---
title: ParentItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ParentItemId
api_type:
- schema
ms.assetid: 72dc4391-72db-44d2-85d9-4718d59886a7
description: ParentItemId 元素标识链接到关联的附件的父项。
ms.openlocfilehash: 9bd875ee5ead8b87996288a640e1bb14e3a5e8b8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826703"
---
# <a name="parentitemid"></a><span data-ttu-id="5d1ac-103">ParentItemId</span><span class="sxs-lookup"><span data-stu-id="5d1ac-103">ParentItemId</span></span>

<span data-ttu-id="5d1ac-104">**ParentItemId**元素标识链接到关联的附件的父项。</span><span class="sxs-lookup"><span data-stu-id="5d1ac-104">The **ParentItemId** element identifies the parent item that links to an associated attachment.</span></span> 
  
- [<span data-ttu-id="5d1ac-105">CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="5d1ac-105">CreateAttachment</span></span>](createattachment.md)
  
- [<span data-ttu-id="5d1ac-106">ParentItemId</span><span class="sxs-lookup"><span data-stu-id="5d1ac-106">ParentItemId</span></span>](parentitemid.md)
  
```xml
<ParentItemId Id="" ChangeKey="" />
```

<span data-ttu-id="5d1ac-107">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="5d1ac-107">**ItemIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="5d1ac-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5d1ac-108">Attributes and elements</span></span>

<span data-ttu-id="5d1ac-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5d1ac-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5d1ac-110">属性</span><span class="sxs-lookup"><span data-stu-id="5d1ac-110">Attributes</span></span>

|<span data-ttu-id="5d1ac-111">**属性**</span><span class="sxs-lookup"><span data-stu-id="5d1ac-111">**Attribute**</span></span>|<span data-ttu-id="5d1ac-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="5d1ac-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5d1ac-113">
  **Id**</span><span class="sxs-lookup"><span data-stu-id="5d1ac-113">**Id**</span></span> <br/> |<span data-ttu-id="5d1ac-114">标识要关联带附件的 Exchange 存储中的单个项。</span><span class="sxs-lookup"><span data-stu-id="5d1ac-114">Identifies a single item in the Exchange store to associate with an attachment.</span></span> <span data-ttu-id="5d1ac-115">此值是一个字符串。</span><span class="sxs-lookup"><span data-stu-id="5d1ac-115">This value is a string.</span></span> <span data-ttu-id="5d1ac-116">此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="5d1ac-116">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="5d1ac-117">**更改密钥**</span><span class="sxs-lookup"><span data-stu-id="5d1ac-117">**ChangeKey**</span></span> <br/> |<span data-ttu-id="5d1ac-118">标识未指定由 Exchange 存储中的**Id**属性标识的项目的版本。</span><span class="sxs-lookup"><span data-stu-id="5d1ac-118">Identifies an unspecified version of an item that is identified by the **Id** attribute in the Exchange store.</span></span> <span data-ttu-id="5d1ac-119">这用于确保更新带附件时，使用当前项目。</span><span class="sxs-lookup"><span data-stu-id="5d1ac-119">This is used to make sure that a current item is used when it is updated with an attachment.</span></span> <span data-ttu-id="5d1ac-120">此值是一个字符串。</span><span class="sxs-lookup"><span data-stu-id="5d1ac-120">This value is a string.</span></span> <span data-ttu-id="5d1ac-121">此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="5d1ac-121">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5d1ac-122">子元素</span><span class="sxs-lookup"><span data-stu-id="5d1ac-122">Child elements</span></span>

<span data-ttu-id="5d1ac-123">无。</span><span class="sxs-lookup"><span data-stu-id="5d1ac-123">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5d1ac-124">父元素</span><span class="sxs-lookup"><span data-stu-id="5d1ac-124">Parent elements</span></span>

|<span data-ttu-id="5d1ac-125">**元素**</span><span class="sxs-lookup"><span data-stu-id="5d1ac-125">**Element**</span></span>|<span data-ttu-id="5d1ac-126">**说明**</span><span class="sxs-lookup"><span data-stu-id="5d1ac-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5d1ac-127">CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="5d1ac-127">CreateAttachment</span></span>](createattachment.md) <br/> |<span data-ttu-id="5d1ac-128">定义在邮箱中创建项目附件的请求。</span><span class="sxs-lookup"><span data-stu-id="5d1ac-128">Defines a request to create an attachment to an item in a mailbox.</span></span>  <br/> <span data-ttu-id="5d1ac-129">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="5d1ac-129">The following is the XPath expression to this element:</span></span>  <br/>  `/CreateAttachment` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5d1ac-130">注解</span><span class="sxs-lookup"><span data-stu-id="5d1ac-130">Remarks</span></span>

<span data-ttu-id="5d1ac-131">此元素是[CreateAttachment 操作](createattachment-operation.md)中必需的。</span><span class="sxs-lookup"><span data-stu-id="5d1ac-131">This element is required in the [CreateAttachment operation](createattachment-operation.md).</span></span> <span data-ttu-id="5d1ac-132">此元素基本上是[ItemId](itemid.md)元素相同。</span><span class="sxs-lookup"><span data-stu-id="5d1ac-132">This element is basically the same as the [ItemId](itemid.md) element.</span></span> 
  
<span data-ttu-id="5d1ac-133">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="5d1ac-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5d1ac-134">元素信息</span><span class="sxs-lookup"><span data-stu-id="5d1ac-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5d1ac-135">命名空间</span><span class="sxs-lookup"><span data-stu-id="5d1ac-135">Namespace</span></span>  <br/> |[http://schemas.microsoft.com/exchange/services/2006/messages](http://schemas.microsoft.com/exchange/services/2006/messages) <br/> |
|<span data-ttu-id="5d1ac-136">架构名称</span><span class="sxs-lookup"><span data-stu-id="5d1ac-136">Schema Name</span></span>  <br/> |<span data-ttu-id="5d1ac-137">消息架构</span><span class="sxs-lookup"><span data-stu-id="5d1ac-137">Messages schema</span></span>  <br/> |
|<span data-ttu-id="5d1ac-138">验证文件</span><span class="sxs-lookup"><span data-stu-id="5d1ac-138">Validation File</span></span>  <br/> |<span data-ttu-id="5d1ac-139">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="5d1ac-139">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5d1ac-140">可以为空</span><span class="sxs-lookup"><span data-stu-id="5d1ac-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="5d1ac-141">False</span><span class="sxs-lookup"><span data-stu-id="5d1ac-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5d1ac-142">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5d1ac-142">See also</span></span>

- [<span data-ttu-id="5d1ac-143">CreateAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="5d1ac-143">CreateAttachment operation</span></span>](createattachment-operation.md)

