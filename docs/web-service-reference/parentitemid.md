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
description: ParentItemId 元素标识链接到相关联的附件的父项目。
ms.openlocfilehash: 4f3e33da0af2438948313f0e335cd03e076d135a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465742"
---
# <a name="parentitemid"></a><span data-ttu-id="2a037-103">ParentItemId</span><span class="sxs-lookup"><span data-stu-id="2a037-103">ParentItemId</span></span>

<span data-ttu-id="2a037-104">**ParentItemId**元素标识链接到相关联的附件的父项目。</span><span class="sxs-lookup"><span data-stu-id="2a037-104">The **ParentItemId** element identifies the parent item that links to an associated attachment.</span></span> 
  
- [<span data-ttu-id="2a037-105">CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="2a037-105">CreateAttachment</span></span>](createattachment.md)
  
- [<span data-ttu-id="2a037-106">ParentItemId</span><span class="sxs-lookup"><span data-stu-id="2a037-106">ParentItemId</span></span>](parentitemid.md)
  
```xml
<ParentItemId Id="" ChangeKey="" />
```

<span data-ttu-id="2a037-107">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="2a037-107">**ItemIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="2a037-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2a037-108">Attributes and elements</span></span>

<span data-ttu-id="2a037-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2a037-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2a037-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="2a037-110">Attributes</span></span>

|<span data-ttu-id="2a037-111">**属性**</span><span class="sxs-lookup"><span data-stu-id="2a037-111">**Attribute**</span></span>|<span data-ttu-id="2a037-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="2a037-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2a037-113">**Id**</span><span class="sxs-lookup"><span data-stu-id="2a037-113">**Id**</span></span> <br/> |<span data-ttu-id="2a037-114">标识与附件关联的 Exchange 存储中的单个项目。</span><span class="sxs-lookup"><span data-stu-id="2a037-114">Identifies a single item in the Exchange store to associate with an attachment.</span></span> <span data-ttu-id="2a037-115">此值为字符串。</span><span class="sxs-lookup"><span data-stu-id="2a037-115">This value is a string.</span></span> <span data-ttu-id="2a037-116">此特性是必需的。</span><span class="sxs-lookup"><span data-stu-id="2a037-116">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="2a037-117">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="2a037-117">**ChangeKey**</span></span> <br/> |<span data-ttu-id="2a037-118">标识由 Exchange 存储中的**Id**属性标识的项目的未指定版本。</span><span class="sxs-lookup"><span data-stu-id="2a037-118">Identifies an unspecified version of an item that is identified by the **Id** attribute in the Exchange store.</span></span> <span data-ttu-id="2a037-119">这用于确保在使用附件更新当前项时使用它。</span><span class="sxs-lookup"><span data-stu-id="2a037-119">This is used to make sure that a current item is used when it is updated with an attachment.</span></span> <span data-ttu-id="2a037-120">此值为字符串。</span><span class="sxs-lookup"><span data-stu-id="2a037-120">This value is a string.</span></span> <span data-ttu-id="2a037-121">此特性是可选的。</span><span class="sxs-lookup"><span data-stu-id="2a037-121">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2a037-122">子元素</span><span class="sxs-lookup"><span data-stu-id="2a037-122">Child elements</span></span>

<span data-ttu-id="2a037-123">无。</span><span class="sxs-lookup"><span data-stu-id="2a037-123">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2a037-124">父元素</span><span class="sxs-lookup"><span data-stu-id="2a037-124">Parent elements</span></span>

|<span data-ttu-id="2a037-125">**元素**</span><span class="sxs-lookup"><span data-stu-id="2a037-125">**Element**</span></span>|<span data-ttu-id="2a037-126">**说明**</span><span class="sxs-lookup"><span data-stu-id="2a037-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2a037-127">CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="2a037-127">CreateAttachment</span></span>](createattachment.md) <br/> |<span data-ttu-id="2a037-128">定义在邮箱中创建项目附件的请求。</span><span class="sxs-lookup"><span data-stu-id="2a037-128">Defines a request to create an attachment to an item in a mailbox.</span></span>  <br/> <span data-ttu-id="2a037-129">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="2a037-129">The following is the XPath expression to this element:</span></span>  <br/>  `/CreateAttachment` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2a037-130">备注</span><span class="sxs-lookup"><span data-stu-id="2a037-130">Remarks</span></span>

<span data-ttu-id="2a037-131">在[CreateAttachment 操作](createattachment-operation.md)中，此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="2a037-131">This element is required in the [CreateAttachment operation](createattachment-operation.md).</span></span> <span data-ttu-id="2a037-132">此元素基本上与[ItemId](itemid.md)元素相同。</span><span class="sxs-lookup"><span data-stu-id="2a037-132">This element is basically the same as the [ItemId](itemid.md) element.</span></span> 
  
<span data-ttu-id="2a037-133">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2a037-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2a037-134">元素信息</span><span class="sxs-lookup"><span data-stu-id="2a037-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2a037-135">命名空间</span><span class="sxs-lookup"><span data-stu-id="2a037-135">Namespace</span></span>  <br/> |[https://schemas.microsoft.com/exchange/services/2006/messages](https://schemas.microsoft.com/exchange/services/2006/messages) <br/> |
|<span data-ttu-id="2a037-136">架构名称</span><span class="sxs-lookup"><span data-stu-id="2a037-136">Schema Name</span></span>  <br/> |<span data-ttu-id="2a037-137">消息架构</span><span class="sxs-lookup"><span data-stu-id="2a037-137">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2a037-138">验证文件</span><span class="sxs-lookup"><span data-stu-id="2a037-138">Validation File</span></span>  <br/> |<span data-ttu-id="2a037-139">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2a037-139">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2a037-140">可以为空</span><span class="sxs-lookup"><span data-stu-id="2a037-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="2a037-141">False</span><span class="sxs-lookup"><span data-stu-id="2a037-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2a037-142">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2a037-142">See also</span></span>

- [<span data-ttu-id="2a037-143">CreateAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="2a037-143">CreateAttachment operation</span></span>](createattachment-operation.md)

