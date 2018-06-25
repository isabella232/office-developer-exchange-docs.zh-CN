---
title: UserConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UserConfiguration
api_type:
- schema
ms.assetid: 1811df99-ca5b-48a3-b160-b3fd70320c34
description: UserConfiguration 元素定义的单个用户配置对象。
ms.openlocfilehash: ce3eaa470ef592c5a8e5a7ef24c377bb2feeca2e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838461"
---
# <a name="userconfiguration"></a><span data-ttu-id="e0015-103">UserConfiguration</span><span class="sxs-lookup"><span data-stu-id="e0015-103">UserConfiguration</span></span>

<span data-ttu-id="e0015-104">**UserConfiguration**元素定义的单个用户配置对象。</span><span class="sxs-lookup"><span data-stu-id="e0015-104">The **UserConfiguration** element defines a single user configuration object.</span></span> 
  
```XML
<UserConfiguration>
   <UserConfigurationName/>
   <ItemId/>
   <Dictionary/>
   <XmlData/>
  <BinaryData/>
</UserConfiguration>
```

 <span data-ttu-id="e0015-105">**UserConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="e0015-105">**UserConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e0015-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e0015-106">Attributes and elements</span></span>

<span data-ttu-id="e0015-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e0015-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e0015-108">属性</span><span class="sxs-lookup"><span data-stu-id="e0015-108">Attributes</span></span>

<span data-ttu-id="e0015-109">无。</span><span class="sxs-lookup"><span data-stu-id="e0015-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e0015-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e0015-110">Child elements</span></span>

|<span data-ttu-id="e0015-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="e0015-111">**Element**</span></span>|<span data-ttu-id="e0015-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="e0015-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e0015-113">UserConfigurationName</span><span class="sxs-lookup"><span data-stu-id="e0015-113">UserConfigurationName</span></span>](userconfigurationname.md) <br/> |<span data-ttu-id="e0015-114">代表用户配置对象的名称。</span><span class="sxs-lookup"><span data-stu-id="e0015-114">Represents the name of a user configuration object.</span></span> <span data-ttu-id="e0015-115">创建用户配置对象时，必须使用此元素。</span><span class="sxs-lookup"><span data-stu-id="e0015-115">This element must be used when you create a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="e0015-116">ItemId</span><span class="sxs-lookup"><span data-stu-id="e0015-116">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="e0015-117">定义的用户配置对象项标识符。</span><span class="sxs-lookup"><span data-stu-id="e0015-117">Defines the user configuration object item identifier.</span></span>  <br/> |
|<span data-ttu-id="e0015-118">"词典"</span><span class="sxs-lookup"><span data-stu-id="e0015-118">[Dictionary](dictionary.md)</span></span> <br/> |<span data-ttu-id="e0015-119">定义一组用户配置对象的词典属性条目。</span><span class="sxs-lookup"><span data-stu-id="e0015-119">Defines a set of dictionary property entries for a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="e0015-120">XmlData</span><span class="sxs-lookup"><span data-stu-id="e0015-120">XmlData</span></span>](xmldata.md) <br/> |<span data-ttu-id="e0015-121">包含 XML 数据属性的用户配置对象的新内容。</span><span class="sxs-lookup"><span data-stu-id="e0015-121">Contains XML data property content for a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="e0015-122">BinaryData</span><span class="sxs-lookup"><span data-stu-id="e0015-122">BinaryData</span></span>](binarydata.md) <br/> |<span data-ttu-id="e0015-123">包含二进制数据属性的用户配置对象的新内容。</span><span class="sxs-lookup"><span data-stu-id="e0015-123">Contains binary data property content for a user configuration object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e0015-124">父元素</span><span class="sxs-lookup"><span data-stu-id="e0015-124">Parent elements</span></span>

|<span data-ttu-id="e0015-125">**元素**</span><span class="sxs-lookup"><span data-stu-id="e0015-125">**Element**</span></span>|<span data-ttu-id="e0015-126">**说明**</span><span class="sxs-lookup"><span data-stu-id="e0015-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e0015-127">CreateUserConfiguration</span><span class="sxs-lookup"><span data-stu-id="e0015-127">CreateUserConfiguration</span></span>](createuserconfiguration.md) <br/> |<span data-ttu-id="e0015-128">表示要创建用户配置对象的请求。</span><span class="sxs-lookup"><span data-stu-id="e0015-128">Represents a request to create a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="e0015-129">GetUserConfigurationResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e0015-129">GetUserConfigurationResponseMessage</span></span>](getuserconfigurationresponsemessage.md) <br/> |<span data-ttu-id="e0015-130">代表一个响应，其中返回的用户配置对象。</span><span class="sxs-lookup"><span data-stu-id="e0015-130">Represents a response that returns a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="e0015-131">UpdateUserConfiguration</span><span class="sxs-lookup"><span data-stu-id="e0015-131">UpdateUserConfiguration</span></span>](updateuserconfiguration.md) <br/> |<span data-ttu-id="e0015-132">表示要更新的用户配置对象的请求。</span><span class="sxs-lookup"><span data-stu-id="e0015-132">Represents a request to update a user configuration object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e0015-133">备注</span><span class="sxs-lookup"><span data-stu-id="e0015-133">Remarks</span></span>

<span data-ttu-id="e0015-134">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e0015-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e0015-135">元素信息</span><span class="sxs-lookup"><span data-stu-id="e0015-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e0015-136">命名空间</span><span class="sxs-lookup"><span data-stu-id="e0015-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e0015-137">架构名称</span><span class="sxs-lookup"><span data-stu-id="e0015-137">Schema Name</span></span>  <br/> |<span data-ttu-id="e0015-138">消息架构</span><span class="sxs-lookup"><span data-stu-id="e0015-138">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e0015-139">验证文件</span><span class="sxs-lookup"><span data-stu-id="e0015-139">Validation File</span></span>  <br/> |<span data-ttu-id="e0015-140">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e0015-140">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e0015-141">可以为空</span><span class="sxs-lookup"><span data-stu-id="e0015-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="e0015-142">False</span><span class="sxs-lookup"><span data-stu-id="e0015-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e0015-143">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e0015-143">See also</span></span>



- [<span data-ttu-id="e0015-144">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e0015-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

