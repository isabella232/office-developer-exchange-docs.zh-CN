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
description: OofSettings 元素包含的外出 (OOF) 设置。
ms.openlocfilehash: d71f068ff24af22da98b6b4de090ab26d3f74f26
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826649"
---
# <a name="oofsettings"></a><span data-ttu-id="07e07-103">OofSettings</span><span class="sxs-lookup"><span data-stu-id="07e07-103">OofSettings</span></span>

<span data-ttu-id="07e07-104">**OofSettings**元素包含的外出 (OOF) 设置。</span><span class="sxs-lookup"><span data-stu-id="07e07-104">The **OofSettings** element contains the Out of Office (OOF) settings.</span></span> 
  
[<span data-ttu-id="07e07-105">GetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="07e07-105">GetUserOofSettingsResponse</span></span>](getuseroofsettingsresponse.md)
  
[<span data-ttu-id="07e07-106">OofSettings</span><span class="sxs-lookup"><span data-stu-id="07e07-106">OofSettings</span></span>](oofsettings.md)
  
```xml
<OofSettings>
   <OofState>...</OofState>
   <ExternalAudience>...</ExternalAudience>
   <Duration>...</Duration>
   <InternalReply>...</InternalReply>
   <ExternalReply>...</ExternalReply>
</OofSettings>
```

 <span data-ttu-id="07e07-107">**UserOofSettings**</span><span class="sxs-lookup"><span data-stu-id="07e07-107">**UserOofSettings**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="07e07-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="07e07-108">Attributes and elements</span></span>

<span data-ttu-id="07e07-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="07e07-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="07e07-110">属性</span><span class="sxs-lookup"><span data-stu-id="07e07-110">Attributes</span></span>

<span data-ttu-id="07e07-111">无。</span><span class="sxs-lookup"><span data-stu-id="07e07-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="07e07-112">子元素</span><span class="sxs-lookup"><span data-stu-id="07e07-112">Child elements</span></span>

|<span data-ttu-id="07e07-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="07e07-113">**Element**</span></span>|<span data-ttu-id="07e07-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="07e07-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="07e07-115">OofState</span><span class="sxs-lookup"><span data-stu-id="07e07-115">OofState</span></span>](oofstate.md) <br/> |<span data-ttu-id="07e07-116">包含用户的 OOF 状态。</span><span class="sxs-lookup"><span data-stu-id="07e07-116">Contains the user's OOF state.</span></span>  <br/> |
|[<span data-ttu-id="07e07-117">ExternalAudience</span><span class="sxs-lookup"><span data-stu-id="07e07-117">ExternalAudience</span></span>](externalaudience.md) <br/> |<span data-ttu-id="07e07-118">包含一个值，确定外部 OOF 邮件发送到其。</span><span class="sxs-lookup"><span data-stu-id="07e07-118">Contains a value that determines to whom external OOF messages are sent.</span></span>  <br/> |
|[<span data-ttu-id="07e07-119">持续时间 (UserOofSettings)</span><span class="sxs-lookup"><span data-stu-id="07e07-119">Duration (UserOofSettings)</span></span>](duration-useroofsettings.md) <br/> |<span data-ttu-id="07e07-120">包含如果[OofState](oofstate.md)元素设置为**计划**为其启用 OOF 状态的工期。</span><span class="sxs-lookup"><span data-stu-id="07e07-120">Contains the duration for which the OOF status is enabled if the [OofState](oofstate.md) element is set to **Scheduled**.</span></span> <span data-ttu-id="07e07-121">如果[OofState](oofstate.md)元素设置为**已启用**或**禁用**，则忽略此元素的值。</span><span class="sxs-lookup"><span data-stu-id="07e07-121">If the [OofState](oofstate.md) element is set to **Enabled** or **Disabled**, the value of this element is ignored.</span></span>  <br/> |
|[<span data-ttu-id="07e07-122">InternalReply</span><span class="sxs-lookup"><span data-stu-id="07e07-122">InternalReply</span></span>](internalreply.md) <br/> |<span data-ttu-id="07e07-123">包含 OOF 响应发送给用户的域或受信任的域中其他用户。</span><span class="sxs-lookup"><span data-stu-id="07e07-123">Contains the OOF response sent to other users in the user's domain or trusted domain.</span></span>  <br/> |
|[<span data-ttu-id="07e07-124">ExternalReply</span><span class="sxs-lookup"><span data-stu-id="07e07-124">ExternalReply</span></span>](externalreply.md) <br/> |<span data-ttu-id="07e07-125">包含 OOF 响应发送给外部收件人的域或受信任的域的地址。</span><span class="sxs-lookup"><span data-stu-id="07e07-125">Contains the OOF response sent to addresses outside the recipient's domain or trusted domains.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="07e07-126">父元素</span><span class="sxs-lookup"><span data-stu-id="07e07-126">Parent elements</span></span>

|<span data-ttu-id="07e07-127">**元素**</span><span class="sxs-lookup"><span data-stu-id="07e07-127">**Element**</span></span>|<span data-ttu-id="07e07-128">**说明**</span><span class="sxs-lookup"><span data-stu-id="07e07-128">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="07e07-129">GetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="07e07-129">GetUserOofSettingsResponse</span></span>](getuseroofsettingsresponse.md) <br/> |<span data-ttu-id="07e07-130">包含响应结果和用户的 OOF 设置。</span><span class="sxs-lookup"><span data-stu-id="07e07-130">Contains the response results and the OOF settings for a user.</span></span>  <br/> <span data-ttu-id="07e07-131">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="07e07-131">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserOofSettingsResponse` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="07e07-132">备注</span><span class="sxs-lookup"><span data-stu-id="07e07-132">Remarks</span></span>

<span data-ttu-id="07e07-133">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="07e07-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="07e07-134">元素信息</span><span class="sxs-lookup"><span data-stu-id="07e07-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="07e07-135">命名空间</span><span class="sxs-lookup"><span data-stu-id="07e07-135">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="07e07-136">架构名称</span><span class="sxs-lookup"><span data-stu-id="07e07-136">Schema Name</span></span>  <br/> |<span data-ttu-id="07e07-137">消息架构</span><span class="sxs-lookup"><span data-stu-id="07e07-137">Messages schema</span></span>  <br/> |
|<span data-ttu-id="07e07-138">验证文件</span><span class="sxs-lookup"><span data-stu-id="07e07-138">Validation File</span></span>  <br/> |<span data-ttu-id="07e07-139">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="07e07-139">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="07e07-140">可以为空</span><span class="sxs-lookup"><span data-stu-id="07e07-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="07e07-141">False</span><span class="sxs-lookup"><span data-stu-id="07e07-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="07e07-142">另请参阅</span><span class="sxs-lookup"><span data-stu-id="07e07-142">See also</span></span>



[<span data-ttu-id="07e07-143">GetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="07e07-143">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)
  
[<span data-ttu-id="07e07-144">SetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="07e07-144">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

