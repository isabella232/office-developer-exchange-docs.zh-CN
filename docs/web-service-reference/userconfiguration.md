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
description: UserConfiguration 元素定义单个用户配置对象。
ms.openlocfilehash: 1217f5d591570c2d8df49a116b6bf35c243d1e0e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468906"
---
# <a name="userconfiguration"></a><span data-ttu-id="ef39d-103">UserConfiguration</span><span class="sxs-lookup"><span data-stu-id="ef39d-103">UserConfiguration</span></span>

<span data-ttu-id="ef39d-104">**UserConfiguration**元素定义单个用户配置对象。</span><span class="sxs-lookup"><span data-stu-id="ef39d-104">The **UserConfiguration** element defines a single user configuration object.</span></span> 
  
```XML
<UserConfiguration>
   <UserConfigurationName/>
   <ItemId/>
   <Dictionary/>
   <XmlData/>
  <BinaryData/>
</UserConfiguration>
```

 <span data-ttu-id="ef39d-105">**UserConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="ef39d-105">**UserConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ef39d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ef39d-106">Attributes and elements</span></span>

<span data-ttu-id="ef39d-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ef39d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ef39d-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="ef39d-108">Attributes</span></span>

<span data-ttu-id="ef39d-109">无。</span><span class="sxs-lookup"><span data-stu-id="ef39d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ef39d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ef39d-110">Child elements</span></span>

|<span data-ttu-id="ef39d-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="ef39d-111">**Element**</span></span>|<span data-ttu-id="ef39d-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="ef39d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ef39d-113">UserConfigurationName</span><span class="sxs-lookup"><span data-stu-id="ef39d-113">UserConfigurationName</span></span>](userconfigurationname.md) <br/> |<span data-ttu-id="ef39d-114">表示用户配置对象的名称。</span><span class="sxs-lookup"><span data-stu-id="ef39d-114">Represents the name of a user configuration object.</span></span> <span data-ttu-id="ef39d-115">创建用户配置对象时，必须使用此元素。</span><span class="sxs-lookup"><span data-stu-id="ef39d-115">This element must be used when you create a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="ef39d-116">ItemId</span><span class="sxs-lookup"><span data-stu-id="ef39d-116">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="ef39d-117">定义 "用户配置对象" 项标识符。</span><span class="sxs-lookup"><span data-stu-id="ef39d-117">Defines the user configuration object item identifier.</span></span>  <br/> |
|<span data-ttu-id="ef39d-118">"词典"</span><span class="sxs-lookup"><span data-stu-id="ef39d-118">[Dictionary](dictionary.md)</span></span> <br/> |<span data-ttu-id="ef39d-119">为用户配置对象定义一组字典属性项。</span><span class="sxs-lookup"><span data-stu-id="ef39d-119">Defines a set of dictionary property entries for a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="ef39d-120">XmlData</span><span class="sxs-lookup"><span data-stu-id="ef39d-120">XmlData</span></span>](xmldata.md) <br/> |<span data-ttu-id="ef39d-121">包含用户配置对象的 XML 数据属性内容。</span><span class="sxs-lookup"><span data-stu-id="ef39d-121">Contains XML data property content for a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="ef39d-122">BinaryData</span><span class="sxs-lookup"><span data-stu-id="ef39d-122">BinaryData</span></span>](binarydata.md) <br/> |<span data-ttu-id="ef39d-123">包含用户配置对象的二进制数据属性内容。</span><span class="sxs-lookup"><span data-stu-id="ef39d-123">Contains binary data property content for a user configuration object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ef39d-124">父元素</span><span class="sxs-lookup"><span data-stu-id="ef39d-124">Parent elements</span></span>

|<span data-ttu-id="ef39d-125">**元素**</span><span class="sxs-lookup"><span data-stu-id="ef39d-125">**Element**</span></span>|<span data-ttu-id="ef39d-126">**说明**</span><span class="sxs-lookup"><span data-stu-id="ef39d-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ef39d-127">CreateUserConfiguration</span><span class="sxs-lookup"><span data-stu-id="ef39d-127">CreateUserConfiguration</span></span>](createuserconfiguration.md) <br/> |<span data-ttu-id="ef39d-128">表示创建用户配置对象的请求。</span><span class="sxs-lookup"><span data-stu-id="ef39d-128">Represents a request to create a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="ef39d-129">GetUserConfigurationResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ef39d-129">GetUserConfigurationResponseMessage</span></span>](getuserconfigurationresponsemessage.md) <br/> |<span data-ttu-id="ef39d-130">表示返回用户配置对象的响应。</span><span class="sxs-lookup"><span data-stu-id="ef39d-130">Represents a response that returns a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="ef39d-131">UpdateUserConfiguration</span><span class="sxs-lookup"><span data-stu-id="ef39d-131">UpdateUserConfiguration</span></span>](updateuserconfiguration.md) <br/> |<span data-ttu-id="ef39d-132">表示一个更新用户配置对象的请求。</span><span class="sxs-lookup"><span data-stu-id="ef39d-132">Represents a request to update a user configuration object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ef39d-133">说明</span><span class="sxs-lookup"><span data-stu-id="ef39d-133">Remarks</span></span>

<span data-ttu-id="ef39d-134">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ef39d-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ef39d-135">元素信息</span><span class="sxs-lookup"><span data-stu-id="ef39d-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ef39d-136">命名空间</span><span class="sxs-lookup"><span data-stu-id="ef39d-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ef39d-137">架构名称</span><span class="sxs-lookup"><span data-stu-id="ef39d-137">Schema Name</span></span>  <br/> |<span data-ttu-id="ef39d-138">消息架构</span><span class="sxs-lookup"><span data-stu-id="ef39d-138">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ef39d-139">验证文件</span><span class="sxs-lookup"><span data-stu-id="ef39d-139">Validation File</span></span>  <br/> |<span data-ttu-id="ef39d-140">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ef39d-140">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ef39d-141">可以为空</span><span class="sxs-lookup"><span data-stu-id="ef39d-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="ef39d-142">False</span><span class="sxs-lookup"><span data-stu-id="ef39d-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ef39d-143">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ef39d-143">See also</span></span>



- [<span data-ttu-id="ef39d-144">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="ef39d-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

