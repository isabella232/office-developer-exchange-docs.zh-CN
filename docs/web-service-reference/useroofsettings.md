---
title: UserOofSettings
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UserOofSettings
api_type:
- schema
ms.assetid: 0a95ca63-660e-4cc0-82e4-3f74fb4ae21c
description: UserOofSettings 元素指定的外出 (OOF) 设置。
ms.openlocfilehash: a035fd89387ece632d83f5f72a564e4896bc6753
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838481"
---
# <a name="useroofsettings"></a><span data-ttu-id="fa99c-103">UserOofSettings</span><span class="sxs-lookup"><span data-stu-id="fa99c-103">UserOofSettings</span></span>

<span data-ttu-id="fa99c-104">**UserOofSettings**元素指定的外出 (OOF) 设置。</span><span class="sxs-lookup"><span data-stu-id="fa99c-104">The **UserOofSettings** element specifies the Out of Office (OOF) settings.</span></span> 
  
[<span data-ttu-id="fa99c-105">SetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="fa99c-105">SetUserOofSettingsRequest</span></span>](setuseroofsettingsrequest.md)
  
[<span data-ttu-id="fa99c-106">UserOofSettings</span><span class="sxs-lookup"><span data-stu-id="fa99c-106">UserOofSettings</span></span>](useroofsettings.md)
  
```xml
<UserOofSettings>
   <OofState>...</OofState>
   <ExternalAudience>...</ExternalAudience>
   <Duration>...</Duration>
   <InternalReply>...</InternalReply>
   <ExternalReply>...</ExternalReply>
</UserOofSettings>
```

 <span data-ttu-id="fa99c-107">**UserOofSettings**</span><span class="sxs-lookup"><span data-stu-id="fa99c-107">**UserOofSettings**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fa99c-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fa99c-108">Attributes and elements</span></span>

<span data-ttu-id="fa99c-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fa99c-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fa99c-110">属性</span><span class="sxs-lookup"><span data-stu-id="fa99c-110">Attributes</span></span>

<span data-ttu-id="fa99c-111">无。</span><span class="sxs-lookup"><span data-stu-id="fa99c-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fa99c-112">子元素</span><span class="sxs-lookup"><span data-stu-id="fa99c-112">Child elements</span></span>

|<span data-ttu-id="fa99c-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="fa99c-113">**Element**</span></span>|<span data-ttu-id="fa99c-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="fa99c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fa99c-115">OofState</span><span class="sxs-lookup"><span data-stu-id="fa99c-115">OofState</span></span>](oofstate.md) <br/> |<span data-ttu-id="fa99c-116">设置用户的 OOF 状态。</span><span class="sxs-lookup"><span data-stu-id="fa99c-116">Sets the user's OOF state.</span></span>  <br/> |
|[<span data-ttu-id="fa99c-117">ExternalAudience</span><span class="sxs-lookup"><span data-stu-id="fa99c-117">ExternalAudience</span></span>](externalaudience.md) <br/> |<span data-ttu-id="fa99c-118">设置或包含一个值，确定外部 OOF 邮件发送到其。</span><span class="sxs-lookup"><span data-stu-id="fa99c-118">Sets or contains a value that determines to whom external OOF messages are sent.</span></span>  <br/> |
|[<span data-ttu-id="fa99c-119">持续时间 (UserOofSettings)</span><span class="sxs-lookup"><span data-stu-id="fa99c-119">Duration (UserOofSettings)</span></span>](duration-useroofsettings.md) <br/> |<span data-ttu-id="fa99c-120">指定如果[OofState](oofstate.md)元素设置为**计划**为其启用 OOF 状态的持续时间。</span><span class="sxs-lookup"><span data-stu-id="fa99c-120">Specifies the duration for which the OOF status is enabled if the [OofState](oofstate.md) element is set to **Scheduled**.</span></span> <span data-ttu-id="fa99c-121">如果[OofState](oofstate.md)元素设置为**已启用**或**禁用**，则忽略此元素的值。</span><span class="sxs-lookup"><span data-stu-id="fa99c-121">If the [OofState](oofstate.md) element is set to **Enabled** or **Disabled**, the value of this element is ignored.</span></span>  <br/> |
|[<span data-ttu-id="fa99c-122">InternalReply</span><span class="sxs-lookup"><span data-stu-id="fa99c-122">InternalReply</span></span>](internalreply.md) <br/> |<span data-ttu-id="fa99c-123">包含 OOF 响应发送给用户的域或受信任的域中的其他用户。</span><span class="sxs-lookup"><span data-stu-id="fa99c-123">Contains the OOF response sent to other users in the user's domain or trusted domains.</span></span>  <br/> |
|[<span data-ttu-id="fa99c-124">ExternalReply</span><span class="sxs-lookup"><span data-stu-id="fa99c-124">ExternalReply</span></span>](externalreply.md) <br/> |<span data-ttu-id="fa99c-125">包含 OOF 响应发送给外部收件人的域或受信任的域的地址。</span><span class="sxs-lookup"><span data-stu-id="fa99c-125">Contains the OOF response sent to addresses outside the recipient's domain or trusted domains.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fa99c-126">父元素</span><span class="sxs-lookup"><span data-stu-id="fa99c-126">Parent elements</span></span>

|<span data-ttu-id="fa99c-127">**元素**</span><span class="sxs-lookup"><span data-stu-id="fa99c-127">**Element**</span></span>|<span data-ttu-id="fa99c-128">**说明**</span><span class="sxs-lookup"><span data-stu-id="fa99c-128">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fa99c-129">SetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="fa99c-129">SetUserOofSettingsRequest</span></span>](setuseroofsettingsrequest.md) <br/> |<span data-ttu-id="fa99c-130">包含用于设置邮箱用户的 OOF 设置和消息的参数。</span><span class="sxs-lookup"><span data-stu-id="fa99c-130">Contains the arguments used to set a mailbox user's OOF settings and messages.</span></span>  <br/> <span data-ttu-id="fa99c-131">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="fa99c-131">The following is the XPath expression to this element:</span></span>  <br/>  `/SetUserOofSettingsRequest` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fa99c-132">备注</span><span class="sxs-lookup"><span data-stu-id="fa99c-132">Remarks</span></span>

<span data-ttu-id="fa99c-133">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="fa99c-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="fa99c-134">示例</span><span class="sxs-lookup"><span data-stu-id="fa99c-134">Example</span></span>

<span data-ttu-id="fa99c-135">SetUserOofSettings 请求的下面的示例将 OoFState 设置为**已启用**，将 OOF 的持续时间设置为 10 天，并设置内部和外部 OOF 邮件。</span><span class="sxs-lookup"><span data-stu-id="fa99c-135">The following example of a SetUserOofSettings request sets the OoFState to **Enabled**, sets the duration of OOF for 10 days, and sets the internal and external OOF messages.</span></span>
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetUserOofSettingsRequest xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <Mailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
        <Name>David Alexander</Name>
        <Address>someone@example.com</Address>
        <RoutingType>SMTP</RoutingType>
      </Mailbox>
      <UserOofSettings xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
        <OofState>Enabled</OofState>
        <ExternalAudience>All</ExternalAudience>
        <Duration>
          <StartTime>2005-10-05T00:00:00</StartTime>
          <EndTime>2005-10-25T00:00:00</EndTime>
        </Duration>
        <InternalReply>
          <Message>I am out of office.  This is my internal reply.</Message>
        </InternalReply>
        <ExternalReply>
          <Message>I am out of office. This is my external reply.</Message>
        </ExternalReply>
      </UserOofSettings>
    </SetUserOofSettingsRequest>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a><span data-ttu-id="fa99c-136">元素信息</span><span class="sxs-lookup"><span data-stu-id="fa99c-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fa99c-137">命名空间</span><span class="sxs-lookup"><span data-stu-id="fa99c-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="fa99c-138">架构名称</span><span class="sxs-lookup"><span data-stu-id="fa99c-138">Schema Name</span></span>  <br/> |<span data-ttu-id="fa99c-139">邮件架构</span><span class="sxs-lookup"><span data-stu-id="fa99c-139">messages schema</span></span>  <br/> |
|<span data-ttu-id="fa99c-140">验证文件</span><span class="sxs-lookup"><span data-stu-id="fa99c-140">Validation File</span></span>  <br/> |<span data-ttu-id="fa99c-141">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="fa99c-141">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="fa99c-142">可以为空</span><span class="sxs-lookup"><span data-stu-id="fa99c-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="fa99c-143">False</span><span class="sxs-lookup"><span data-stu-id="fa99c-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fa99c-144">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fa99c-144">See also</span></span>

- [<span data-ttu-id="fa99c-145">SetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="fa99c-145">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

