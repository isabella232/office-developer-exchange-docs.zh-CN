---
title: DeleteUserConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteUserConfiguration
api_type:
- schema
ms.assetid: 91b18b6a-d904-476c-996d-b041e859da1e
description: DeleteUserConfiguration 元素表示一个删除用户配置对象的请求。
ms.openlocfilehash: 04668ead48e7c321ed7e91cbbeb67c6154c02283
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460755"
---
# <a name="deleteuserconfiguration"></a><span data-ttu-id="c0c41-103">DeleteUserConfiguration</span><span class="sxs-lookup"><span data-stu-id="c0c41-103">DeleteUserConfiguration</span></span>

<span data-ttu-id="c0c41-104">**DeleteUserConfiguration**元素表示一个删除用户配置对象的请求。</span><span class="sxs-lookup"><span data-stu-id="c0c41-104">The **DeleteUserConfiguration** element represents a request to delete a user configuration object.</span></span> 
  
```xml
<DeleteUserConfiguration>
   <UserConfigurationName/>
</DeleteUserConfiguration>
```

 <span data-ttu-id="c0c41-105">**DeleteUserConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="c0c41-105">**DeleteUserConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c0c41-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c0c41-106">Attributes and elements</span></span>

<span data-ttu-id="c0c41-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c0c41-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c0c41-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="c0c41-108">Attributes</span></span>

<span data-ttu-id="c0c41-109">无。</span><span class="sxs-lookup"><span data-stu-id="c0c41-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c0c41-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c0c41-110">Child elements</span></span>

|<span data-ttu-id="c0c41-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="c0c41-111">**Element**</span></span>|<span data-ttu-id="c0c41-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="c0c41-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c0c41-113">UserConfigurationName</span><span class="sxs-lookup"><span data-stu-id="c0c41-113">UserConfigurationName</span></span>](userconfigurationname.md) <br/> |<span data-ttu-id="c0c41-114">表示要删除的用户配置对象的名称。</span><span class="sxs-lookup"><span data-stu-id="c0c41-114">Represents the name of the user configuration object to delete.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c0c41-115">父元素</span><span class="sxs-lookup"><span data-stu-id="c0c41-115">Parent elements</span></span>

<span data-ttu-id="c0c41-116">无。</span><span class="sxs-lookup"><span data-stu-id="c0c41-116">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="c0c41-117">文本值</span><span class="sxs-lookup"><span data-stu-id="c0c41-117">Text value</span></span>

<span data-ttu-id="c0c41-118">无。</span><span class="sxs-lookup"><span data-stu-id="c0c41-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c0c41-119">说明</span><span class="sxs-lookup"><span data-stu-id="c0c41-119">Remarks</span></span>

<span data-ttu-id="c0c41-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c0c41-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c0c41-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="c0c41-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c0c41-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="c0c41-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c0c41-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="c0c41-123">Schema Name</span></span>  <br/> |<span data-ttu-id="c0c41-124">消息架构</span><span class="sxs-lookup"><span data-stu-id="c0c41-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c0c41-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="c0c41-125">Validation File</span></span>  <br/> |<span data-ttu-id="c0c41-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c0c41-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c0c41-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="c0c41-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="c0c41-128">False</span><span class="sxs-lookup"><span data-stu-id="c0c41-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c0c41-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c0c41-129">See also</span></span>

- [<span data-ttu-id="c0c41-130">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c0c41-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

