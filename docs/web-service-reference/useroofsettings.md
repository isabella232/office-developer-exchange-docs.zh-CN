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
description: UserOofSettings 元素指定 "外出" （OOF）设置。
ms.openlocfilehash: 417c3d5061a6229d41eb57f72e89f03213acf460
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461903"
---
# <a name="useroofsettings"></a><span data-ttu-id="d1f73-103">UserOofSettings</span><span class="sxs-lookup"><span data-stu-id="d1f73-103">UserOofSettings</span></span>

<span data-ttu-id="d1f73-104">**UserOofSettings**元素指定 "外出" （OOF）设置。</span><span class="sxs-lookup"><span data-stu-id="d1f73-104">The **UserOofSettings** element specifies the Out of Office (OOF) settings.</span></span> 
  
[<span data-ttu-id="d1f73-105">SetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="d1f73-105">SetUserOofSettingsRequest</span></span>](setuseroofsettingsrequest.md)
  
[<span data-ttu-id="d1f73-106">UserOofSettings</span><span class="sxs-lookup"><span data-stu-id="d1f73-106">UserOofSettings</span></span>](useroofsettings.md)
  
```xml
<UserOofSettings>
   <OofState>...</OofState>
   <ExternalAudience>...</ExternalAudience>
   <Duration>...</Duration>
   <InternalReply>...</InternalReply>
   <ExternalReply>...</ExternalReply>
</UserOofSettings>
```

 <span data-ttu-id="d1f73-107">**UserOofSettings**</span><span class="sxs-lookup"><span data-stu-id="d1f73-107">**UserOofSettings**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d1f73-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d1f73-108">Attributes and elements</span></span>

<span data-ttu-id="d1f73-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d1f73-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d1f73-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="d1f73-110">Attributes</span></span>

<span data-ttu-id="d1f73-111">无。</span><span class="sxs-lookup"><span data-stu-id="d1f73-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d1f73-112">子元素</span><span class="sxs-lookup"><span data-stu-id="d1f73-112">Child elements</span></span>

|<span data-ttu-id="d1f73-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="d1f73-113">**Element**</span></span>|<span data-ttu-id="d1f73-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="d1f73-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d1f73-115">OofState</span><span class="sxs-lookup"><span data-stu-id="d1f73-115">OofState</span></span>](oofstate.md) <br/> |<span data-ttu-id="d1f73-116">设置用户的 OOF 状态。</span><span class="sxs-lookup"><span data-stu-id="d1f73-116">Sets the user's OOF state.</span></span>  <br/> |
|[<span data-ttu-id="d1f73-117">ExternalAudience</span><span class="sxs-lookup"><span data-stu-id="d1f73-117">ExternalAudience</span></span>](externalaudience.md) <br/> |<span data-ttu-id="d1f73-118">设置或包含一个值，该值确定要向其发送外部 OOF 邮件的人员。</span><span class="sxs-lookup"><span data-stu-id="d1f73-118">Sets or contains a value that determines to whom external OOF messages are sent.</span></span>  <br/> |
|[<span data-ttu-id="d1f73-119">持续时间（UserOofSettings）</span><span class="sxs-lookup"><span data-stu-id="d1f73-119">Duration (UserOofSettings)</span></span>](duration-useroofsettings.md) <br/> |<span data-ttu-id="d1f73-120">如果将[OofState](oofstate.md)元素设置为 "**计划**"，则指定启用了 OOF 状态的持续时间。</span><span class="sxs-lookup"><span data-stu-id="d1f73-120">Specifies the duration for which the OOF status is enabled if the [OofState](oofstate.md) element is set to **Scheduled**.</span></span> <span data-ttu-id="d1f73-121">如果将[OofState](oofstate.md)元素设置为 "**启用**" 或 "**禁用**"，则忽略此元素的值。</span><span class="sxs-lookup"><span data-stu-id="d1f73-121">If the [OofState](oofstate.md) element is set to **Enabled** or **Disabled**, the value of this element is ignored.</span></span>  <br/> |
|[<span data-ttu-id="d1f73-122">InternalReply</span><span class="sxs-lookup"><span data-stu-id="d1f73-122">InternalReply</span></span>](internalreply.md) <br/> |<span data-ttu-id="d1f73-123">包含发送给用户域或受信任域中的其他用户的 OOF 响应。</span><span class="sxs-lookup"><span data-stu-id="d1f73-123">Contains the OOF response sent to other users in the user's domain or trusted domains.</span></span>  <br/> |
|[<span data-ttu-id="d1f73-124">ExternalReply</span><span class="sxs-lookup"><span data-stu-id="d1f73-124">ExternalReply</span></span>](externalreply.md) <br/> |<span data-ttu-id="d1f73-125">包含发送给收件人域或受信任域外部的地址的 OOF 响应。</span><span class="sxs-lookup"><span data-stu-id="d1f73-125">Contains the OOF response sent to addresses outside the recipient's domain or trusted domains.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d1f73-126">父元素</span><span class="sxs-lookup"><span data-stu-id="d1f73-126">Parent elements</span></span>

|<span data-ttu-id="d1f73-127">**元素**</span><span class="sxs-lookup"><span data-stu-id="d1f73-127">**Element**</span></span>|<span data-ttu-id="d1f73-128">**说明**</span><span class="sxs-lookup"><span data-stu-id="d1f73-128">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d1f73-129">SetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="d1f73-129">SetUserOofSettingsRequest</span></span>](setuseroofsettingsrequest.md) <br/> |<span data-ttu-id="d1f73-130">包含用于设置邮箱用户的 OOF 设置和邮件的参数。</span><span class="sxs-lookup"><span data-stu-id="d1f73-130">Contains the arguments used to set a mailbox user's OOF settings and messages.</span></span>  <br/> <span data-ttu-id="d1f73-131">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="d1f73-131">The following is the XPath expression to this element:</span></span>  <br/>  `/SetUserOofSettingsRequest` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d1f73-132">说明</span><span class="sxs-lookup"><span data-stu-id="d1f73-132">Remarks</span></span>

<span data-ttu-id="d1f73-133">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d1f73-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="d1f73-134">示例</span><span class="sxs-lookup"><span data-stu-id="d1f73-134">Example</span></span>

<span data-ttu-id="d1f73-135">以下示例的 SetUserOofSettings 请求将 OoFState 设置为 "**启用**"，将 "OOF" 的持续时间设置为10天，并设置内部和外部 OOF 邮件。</span><span class="sxs-lookup"><span data-stu-id="d1f73-135">The following example of a SetUserOofSettings request sets the OoFState to **Enabled**, sets the duration of OOF for 10 days, and sets the internal and external OOF messages.</span></span>
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetUserOofSettingsRequest xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <Mailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
        <Name>David Alexander</Name>
        <Address>someone@example.com</Address>
        <RoutingType>SMTP</RoutingType>
      </Mailbox>
      <UserOofSettings xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="element-information"></a><span data-ttu-id="d1f73-136">元素信息</span><span class="sxs-lookup"><span data-stu-id="d1f73-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d1f73-137">命名空间</span><span class="sxs-lookup"><span data-stu-id="d1f73-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d1f73-138">架构名称</span><span class="sxs-lookup"><span data-stu-id="d1f73-138">Schema Name</span></span>  <br/> |<span data-ttu-id="d1f73-139">邮件架构</span><span class="sxs-lookup"><span data-stu-id="d1f73-139">messages schema</span></span>  <br/> |
|<span data-ttu-id="d1f73-140">验证文件</span><span class="sxs-lookup"><span data-stu-id="d1f73-140">Validation File</span></span>  <br/> |<span data-ttu-id="d1f73-141">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d1f73-141">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d1f73-142">可以为空</span><span class="sxs-lookup"><span data-stu-id="d1f73-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="d1f73-143">False</span><span class="sxs-lookup"><span data-stu-id="d1f73-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d1f73-144">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d1f73-144">See also</span></span>

- [<span data-ttu-id="d1f73-145">SetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="d1f73-145">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

