---
title: CreateUserConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateUserConfiguration
api_type:
- schema
ms.assetid: 43e12e8b-5629-4f5f-9cbd-a99084d8460f
description: CreateUserConfiguration 元素均表示一个要创建用户配置对象的请求。
ms.openlocfilehash: dcf3acc356110b993bdb7f4f83245753835f299f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753691"
---
# <a name="createuserconfiguration"></a><span data-ttu-id="a6e4f-103">CreateUserConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6e4f-103">CreateUserConfiguration</span></span>

<span data-ttu-id="a6e4f-104">**CreateUserConfiguration**元素均表示一个要创建用户配置对象的请求。</span><span class="sxs-lookup"><span data-stu-id="a6e4f-104">The **CreateUserConfiguration** element represents a request to create a user configuration object.</span></span> 
  
```xml
<CreateUserConfiguration>
   <UserConfiguration/>
</CreateUserConfiguration>
```

 <span data-ttu-id="a6e4f-105">**CreateUserConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="a6e4f-105">**CreateUserConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a6e4f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a6e4f-106">Attributes and elements</span></span>

<span data-ttu-id="a6e4f-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a6e4f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a6e4f-108">属性</span><span class="sxs-lookup"><span data-stu-id="a6e4f-108">Attributes</span></span>

<span data-ttu-id="a6e4f-109">无。</span><span class="sxs-lookup"><span data-stu-id="a6e4f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a6e4f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a6e4f-110">Child elements</span></span>

|<span data-ttu-id="a6e4f-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="a6e4f-111">**Element**</span></span>|<span data-ttu-id="a6e4f-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="a6e4f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a6e4f-113">UserConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6e4f-113">UserConfiguration</span></span>](userconfiguration.md) <br/> |<span data-ttu-id="a6e4f-114">代表单个用户配置对象。</span><span class="sxs-lookup"><span data-stu-id="a6e4f-114">Represents a single user configuration object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a6e4f-115">父元素</span><span class="sxs-lookup"><span data-stu-id="a6e4f-115">Parent elements</span></span>

<span data-ttu-id="a6e4f-116">无。</span><span class="sxs-lookup"><span data-stu-id="a6e4f-116">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="a6e4f-117">文本值</span><span class="sxs-lookup"><span data-stu-id="a6e4f-117">Text value</span></span>

<span data-ttu-id="a6e4f-118">无。</span><span class="sxs-lookup"><span data-stu-id="a6e4f-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a6e4f-119">备注</span><span class="sxs-lookup"><span data-stu-id="a6e4f-119">Remarks</span></span>

<span data-ttu-id="a6e4f-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a6e4f-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a6e4f-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="a6e4f-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a6e4f-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="a6e4f-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a6e4f-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="a6e4f-123">Schema Name</span></span>  <br/> |<span data-ttu-id="a6e4f-124">消息架构</span><span class="sxs-lookup"><span data-stu-id="a6e4f-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a6e4f-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="a6e4f-125">Validation File</span></span>  <br/> |<span data-ttu-id="a6e4f-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a6e4f-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a6e4f-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="a6e4f-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="a6e4f-128">False</span><span class="sxs-lookup"><span data-stu-id="a6e4f-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a6e4f-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a6e4f-129">See also</span></span>



- [<span data-ttu-id="a6e4f-130">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a6e4f-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

