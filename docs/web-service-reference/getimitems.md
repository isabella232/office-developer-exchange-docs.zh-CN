---
title: GetImItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 455e5709-6c06-49fd-bfb2-403fc912287c
description: GetImItems request 元素定义一个请求，以获取有关指定的即时消息组和即时消息联系人角色的信息。
ms.openlocfilehash: e3973cbbf800ffe91472b9c733c4d4a927b91c9f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456449"
---
# <a name="getimitems"></a><span data-ttu-id="3723d-103">GetImItems</span><span class="sxs-lookup"><span data-stu-id="3723d-103">GetImItems</span></span>

<span data-ttu-id="3723d-104">**GetImItems** request 元素定义一个请求，以获取有关指定的即时消息组和即时消息联系人角色的信息。</span><span class="sxs-lookup"><span data-stu-id="3723d-104">The **GetImItems** request element defines a request to get information about the specified instant messaging groups and instant messaging contact personas.</span></span> 
  
```XML
<GetImItems>
   <ContactIds/>
   <GroupIds/>
   <ExtendedProperties/>
</GetImItems>
```

 <span data-ttu-id="3723d-105">**GetImItemsType**</span><span class="sxs-lookup"><span data-stu-id="3723d-105">**GetImItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3723d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="3723d-106">Attributes and elements</span></span>

<span data-ttu-id="3723d-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3723d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3723d-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="3723d-108">Attributes</span></span>

<span data-ttu-id="3723d-109">无。</span><span class="sxs-lookup"><span data-stu-id="3723d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3723d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="3723d-110">Child elements</span></span>

<span data-ttu-id="3723d-111">[ContactIds](contactids.md)  | [Groupid](groupids.md)  | [ExtendedProperties （NonEmptyArrayOfExtendedFieldURIs）](extendedproperties-nonemptyarrayofextendedfielduris.md)</span><span class="sxs-lookup"><span data-stu-id="3723d-111">[ContactIds](contactids.md) | [GroupIds](groupids.md) | [ExtendedProperties (NonEmptyArrayOfExtendedFieldURIs)](extendedproperties-nonemptyarrayofextendedfielduris.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3723d-112">父元素</span><span class="sxs-lookup"><span data-stu-id="3723d-112">Parent elements</span></span>

<span data-ttu-id="3723d-113">无。</span><span class="sxs-lookup"><span data-stu-id="3723d-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3723d-114">说明</span><span class="sxs-lookup"><span data-stu-id="3723d-114">Remarks</span></span>

<span data-ttu-id="3723d-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="3723d-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="3723d-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="3723d-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3723d-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="3723d-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3723d-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="3723d-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3723d-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="3723d-119">Schema name</span></span>  <br/> |<span data-ttu-id="3723d-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="3723d-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3723d-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="3723d-121">Validation file</span></span>  <br/> |<span data-ttu-id="3723d-122">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="3723d-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3723d-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="3723d-123">Can be empty</span></span>  <br/> ||
   

