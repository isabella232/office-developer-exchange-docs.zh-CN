---
title: UserParameters
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bad7311f-7ecd-4f0c-b8e7-dd8f7d378f55
description: UserParameters 元素包含已启用和已禁用的客户端扩展的列表。
ms.openlocfilehash: 76bf858adfb6d2ef76a25c234117131752c60d7b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526751"
---
# <a name="userparameters"></a><span data-ttu-id="2cd76-103">UserParameters</span><span class="sxs-lookup"><span data-stu-id="2cd76-103">UserParameters</span></span>

<span data-ttu-id="2cd76-104">**UserParameters**元素包含已启用和已禁用的客户端扩展的列表。</span><span class="sxs-lookup"><span data-stu-id="2cd76-104">The **UserParameters** element contains a list of enabled and disabled client extensions.</span></span> 
  
```XML
<UserParameters UserId="" EnabledOnly="">
   <UserEnabledExtensions/>
   <UserDisabledExtensions/>
</UserParameters>
```

 <span data-ttu-id="2cd76-105">**GetClientExtensionUserParametersType**</span><span class="sxs-lookup"><span data-stu-id="2cd76-105">**GetClientExtensionUserParametersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2cd76-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2cd76-106">Attributes and elements</span></span>

<span data-ttu-id="2cd76-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2cd76-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2cd76-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="2cd76-108">Attributes</span></span>

|<span data-ttu-id="2cd76-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="2cd76-109">**Attribute**</span></span>|<span data-ttu-id="2cd76-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="2cd76-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2cd76-111">UserID</span><span class="sxs-lookup"><span data-stu-id="2cd76-111">UserId</span></span>  <br/> |<span data-ttu-id="2cd76-112">**UserId**属性的文本值是用户的标识符。</span><span class="sxs-lookup"><span data-stu-id="2cd76-112">The text value of the **UserId** attribute is the identifier of the user.</span></span>  <br/> |
|<span data-ttu-id="2cd76-113">EnabledOnly</span><span class="sxs-lookup"><span data-stu-id="2cd76-113">EnabledOnly</span></span>  <br/> |<span data-ttu-id="2cd76-114">**EnabledOnly**的文本值指示响应是否仅包含已启用的扩展。</span><span class="sxs-lookup"><span data-stu-id="2cd76-114">The text value of the **EnabledOnly** indicates whether the response only contains the enabled extensions.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2cd76-115">子元素</span><span class="sxs-lookup"><span data-stu-id="2cd76-115">Child elements</span></span>

<span data-ttu-id="2cd76-116">[UserEnabledExtensions](userenabledextensions.md)  | [UserDisabledExtensions](userdisabledextensions.md)</span><span class="sxs-lookup"><span data-stu-id="2cd76-116">[UserEnabledExtensions](userenabledextensions.md) | [UserDisabledExtensions](userdisabledextensions.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2cd76-117">父元素</span><span class="sxs-lookup"><span data-stu-id="2cd76-117">Parent elements</span></span>

[<span data-ttu-id="2cd76-118">GetClientExtension</span><span class="sxs-lookup"><span data-stu-id="2cd76-118">GetClientExtension</span></span>](getclientextension.md)
  
## <a name="remarks"></a><span data-ttu-id="2cd76-119">备注</span><span class="sxs-lookup"><span data-stu-id="2cd76-119">Remarks</span></span>

<span data-ttu-id="2cd76-120">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="2cd76-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2cd76-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2cd76-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2cd76-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="2cd76-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2cd76-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="2cd76-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2cd76-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="2cd76-124">Schema name</span></span>  <br/> |<span data-ttu-id="2cd76-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="2cd76-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="2cd76-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="2cd76-126">Validation file</span></span>  <br/> |<span data-ttu-id="2cd76-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2cd76-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2cd76-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="2cd76-128">Can be empty</span></span>  <br/> ||
   

