---
title: OofSettings
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OofSettings
api_type:
- schema
ms.assetid: 8f37d174-db11-427c-bbed-fdde754a60c7
description: OofSettings 元素包含外出（OOF）设置。
ms.openlocfilehash: c1b214fd8bfab5b7a82d41a5187cf6e0fc4ba79c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467191"
---
# <a name="oofsettings"></a><span data-ttu-id="01811-103">OofSettings</span><span class="sxs-lookup"><span data-stu-id="01811-103">OofSettings</span></span>

<span data-ttu-id="01811-104">**OofSettings**元素包含外出（OOF）设置。</span><span class="sxs-lookup"><span data-stu-id="01811-104">The **OofSettings** element contains the Out of Office (OOF) settings.</span></span> 
  
[<span data-ttu-id="01811-105">GetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="01811-105">GetUserOofSettingsResponse</span></span>](getuseroofsettingsresponse.md)
  
[<span data-ttu-id="01811-106">OofSettings</span><span class="sxs-lookup"><span data-stu-id="01811-106">OofSettings</span></span>](oofsettings.md)
  
```xml
<OofSettings>
   <OofState>...</OofState>
   <ExternalAudience>...</ExternalAudience>
   <Duration>...</Duration>
   <InternalReply>...</InternalReply>
   <ExternalReply>...</ExternalReply>
</OofSettings>
```

 <span data-ttu-id="01811-107">**UserOofSettings**</span><span class="sxs-lookup"><span data-stu-id="01811-107">**UserOofSettings**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="01811-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="01811-108">Attributes and elements</span></span>

<span data-ttu-id="01811-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="01811-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="01811-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="01811-110">Attributes</span></span>

<span data-ttu-id="01811-111">无。</span><span class="sxs-lookup"><span data-stu-id="01811-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="01811-112">子元素</span><span class="sxs-lookup"><span data-stu-id="01811-112">Child elements</span></span>

|<span data-ttu-id="01811-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="01811-113">**Element**</span></span>|<span data-ttu-id="01811-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="01811-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="01811-115">OofState</span><span class="sxs-lookup"><span data-stu-id="01811-115">OofState</span></span>](oofstate.md) <br/> |<span data-ttu-id="01811-116">包含用户的 OOF 状态。</span><span class="sxs-lookup"><span data-stu-id="01811-116">Contains the user's OOF state.</span></span>  <br/> |
|[<span data-ttu-id="01811-117">ExternalAudience</span><span class="sxs-lookup"><span data-stu-id="01811-117">ExternalAudience</span></span>](externalaudience.md) <br/> |<span data-ttu-id="01811-118">包含一个值，该值确定要向其发送外部 OOF 邮件的人员。</span><span class="sxs-lookup"><span data-stu-id="01811-118">Contains a value that determines to whom external OOF messages are sent.</span></span>  <br/> |
|[<span data-ttu-id="01811-119">持续时间（UserOofSettings）</span><span class="sxs-lookup"><span data-stu-id="01811-119">Duration (UserOofSettings)</span></span>](duration-useroofsettings.md) <br/> |<span data-ttu-id="01811-120">包含在[OofState](oofstate.md)元素设置为 "已**计划**" 时启用了 OOF 状态的持续时间。</span><span class="sxs-lookup"><span data-stu-id="01811-120">Contains the duration for which the OOF status is enabled if the [OofState](oofstate.md) element is set to **Scheduled**.</span></span> <span data-ttu-id="01811-121">如果将[OofState](oofstate.md)元素设置为 "**启用**" 或 "**禁用**"，则忽略此元素的值。</span><span class="sxs-lookup"><span data-stu-id="01811-121">If the [OofState](oofstate.md) element is set to **Enabled** or **Disabled**, the value of this element is ignored.</span></span>  <br/> |
|[<span data-ttu-id="01811-122">InternalReply</span><span class="sxs-lookup"><span data-stu-id="01811-122">InternalReply</span></span>](internalreply.md) <br/> |<span data-ttu-id="01811-123">包含发送给用户域或受信任域中的其他用户的 OOF 响应。</span><span class="sxs-lookup"><span data-stu-id="01811-123">Contains the OOF response sent to other users in the user's domain or trusted domain.</span></span>  <br/> |
|[<span data-ttu-id="01811-124">ExternalReply</span><span class="sxs-lookup"><span data-stu-id="01811-124">ExternalReply</span></span>](externalreply.md) <br/> |<span data-ttu-id="01811-125">包含发送给收件人域或受信任域外部的地址的 OOF 响应。</span><span class="sxs-lookup"><span data-stu-id="01811-125">Contains the OOF response sent to addresses outside the recipient's domain or trusted domains.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="01811-126">父元素</span><span class="sxs-lookup"><span data-stu-id="01811-126">Parent elements</span></span>

|<span data-ttu-id="01811-127">**元素**</span><span class="sxs-lookup"><span data-stu-id="01811-127">**Element**</span></span>|<span data-ttu-id="01811-128">**说明**</span><span class="sxs-lookup"><span data-stu-id="01811-128">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="01811-129">GetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="01811-129">GetUserOofSettingsResponse</span></span>](getuseroofsettingsresponse.md) <br/> |<span data-ttu-id="01811-130">包含用户的响应结果和 OOF 设置。</span><span class="sxs-lookup"><span data-stu-id="01811-130">Contains the response results and the OOF settings for a user.</span></span>  <br/> <span data-ttu-id="01811-131">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="01811-131">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserOofSettingsResponse` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="01811-132">说明</span><span class="sxs-lookup"><span data-stu-id="01811-132">Remarks</span></span>

<span data-ttu-id="01811-133">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="01811-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="01811-134">元素信息</span><span class="sxs-lookup"><span data-stu-id="01811-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="01811-135">命名空间</span><span class="sxs-lookup"><span data-stu-id="01811-135">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="01811-136">架构名称</span><span class="sxs-lookup"><span data-stu-id="01811-136">Schema Name</span></span>  <br/> |<span data-ttu-id="01811-137">消息架构</span><span class="sxs-lookup"><span data-stu-id="01811-137">Messages schema</span></span>  <br/> |
|<span data-ttu-id="01811-138">验证文件</span><span class="sxs-lookup"><span data-stu-id="01811-138">Validation File</span></span>  <br/> |<span data-ttu-id="01811-139">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="01811-139">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="01811-140">可以为空</span><span class="sxs-lookup"><span data-stu-id="01811-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="01811-141">False</span><span class="sxs-lookup"><span data-stu-id="01811-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="01811-142">另请参阅</span><span class="sxs-lookup"><span data-stu-id="01811-142">See also</span></span>



[<span data-ttu-id="01811-143">GetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="01811-143">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)
  
[<span data-ttu-id="01811-144">SetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="01811-144">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

