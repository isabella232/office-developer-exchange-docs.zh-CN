---
title: GetImItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 455e5709-6c06-49fd-bfb2-403fc912287c
description: GetImItems 请求元素定义一个请求以获取有关指定的即时消息组和即时消息联系人角色的信息。
ms.openlocfilehash: ff7d520dde44fac6e9278633c1ad46b07b38d6c4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754581"
---
# <a name="getimitems"></a><span data-ttu-id="6027a-103">GetImItems</span><span class="sxs-lookup"><span data-stu-id="6027a-103">GetImItems</span></span>

<span data-ttu-id="6027a-104">**GetImItems**请求元素定义一个请求以获取有关指定的即时消息组和即时消息联系人角色的信息。</span><span class="sxs-lookup"><span data-stu-id="6027a-104">The **GetImItems** request element defines a request to get information about the specified instant messaging groups and instant messaging contact personas.</span></span> 
  
```XML
<GetImItems>
   <ContactIds/>
   <GroupIds/>
   <ExtendedProperties/>
</GetImItems>
```

 <span data-ttu-id="6027a-105">**GetImItemsType**</span><span class="sxs-lookup"><span data-stu-id="6027a-105">**GetImItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6027a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6027a-106">Attributes and elements</span></span>

<span data-ttu-id="6027a-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6027a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6027a-108">属性</span><span class="sxs-lookup"><span data-stu-id="6027a-108">Attributes</span></span>

<span data-ttu-id="6027a-109">无。</span><span class="sxs-lookup"><span data-stu-id="6027a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6027a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="6027a-110">Child elements</span></span>

<span data-ttu-id="6027a-111">[ContactIds](contactids.md) | [GroupIds](groupids.md) | [ExtendedProperties (NonEmptyArrayOfExtendedFieldURIs)](extendedproperties-nonemptyarrayofextendedfielduris.md)</span><span class="sxs-lookup"><span data-stu-id="6027a-111">[ContactIds](contactids.md) | [GroupIds](groupids.md) | [ExtendedProperties (NonEmptyArrayOfExtendedFieldURIs)](extendedproperties-nonemptyarrayofextendedfielduris.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6027a-112">父元素</span><span class="sxs-lookup"><span data-stu-id="6027a-112">Parent elements</span></span>

<span data-ttu-id="6027a-113">无。</span><span class="sxs-lookup"><span data-stu-id="6027a-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6027a-114">备注</span><span class="sxs-lookup"><span data-stu-id="6027a-114">Remarks</span></span>

<span data-ttu-id="6027a-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="6027a-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="6027a-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="6027a-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6027a-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="6027a-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6027a-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="6027a-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6027a-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="6027a-119">Schema name</span></span>  <br/> |<span data-ttu-id="6027a-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="6027a-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6027a-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="6027a-121">Validation file</span></span>  <br/> |<span data-ttu-id="6027a-122">messages.xsd</span><span class="sxs-lookup"><span data-stu-id="6027a-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6027a-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="6027a-123">Can be empty</span></span>  <br/> ||
   

