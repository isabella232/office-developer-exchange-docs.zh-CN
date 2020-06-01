---
title: InternalReply
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- InternalReply
api_type:
- schema
ms.assetid: 1d784ded-b874-4eb1-8f6d-2e0e03330e1e
description: InternalReply 元素包含向用户域或受信任域中的其他用户发送的外出（OOF）响应。
ms.openlocfilehash: 24c278ebd3acf83e87fbf72650eb3d5d438d5c22
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465581"
---
# <a name="internalreply"></a><span data-ttu-id="4e9f9-103">InternalReply</span><span class="sxs-lookup"><span data-stu-id="4e9f9-103">InternalReply</span></span>

<span data-ttu-id="4e9f9-104">**InternalReply**元素包含向用户域或受信任域中的其他用户发送的外出（OOF）响应。</span><span class="sxs-lookup"><span data-stu-id="4e9f9-104">The **InternalReply** element contains the out of office (OOF) response sent to other users in the user's domain or trusted domains.</span></span> 
  
```XML
<InternalReply>
   <Message/> 
</InternalReply>
```

 <span data-ttu-id="4e9f9-105">**ReplyBody**</span><span class="sxs-lookup"><span data-stu-id="4e9f9-105">**ReplyBody**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4e9f9-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4e9f9-106">Attributes and elements</span></span>

<span data-ttu-id="4e9f9-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4e9f9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4e9f9-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="4e9f9-108">Attributes</span></span>

|<span data-ttu-id="4e9f9-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="4e9f9-109">**Attribute**</span></span>|<span data-ttu-id="4e9f9-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="4e9f9-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4e9f9-111">xml： lang</span><span class="sxs-lookup"><span data-stu-id="4e9f9-111">xml:lang</span></span>  <br/> |<span data-ttu-id="4e9f9-112">指定在**InternalReply**消息中使用的语言。</span><span class="sxs-lookup"><span data-stu-id="4e9f9-112">Specifies the language used in the **InternalReply** message.</span></span> <span data-ttu-id="4e9f9-113">此属性的可能值由 IETF RFC 3066 定义。</span><span class="sxs-lookup"><span data-stu-id="4e9f9-113">The possible values of this attribute are defined by IETF RFC 3066.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4e9f9-114">子元素</span><span class="sxs-lookup"><span data-stu-id="4e9f9-114">Child elements</span></span>

|<span data-ttu-id="4e9f9-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="4e9f9-115">**Element**</span></span>|<span data-ttu-id="4e9f9-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="4e9f9-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4e9f9-117">邮件（可用性）</span><span class="sxs-lookup"><span data-stu-id="4e9f9-117">Message (Availability)</span></span>](message-availability.md) <br/> |<span data-ttu-id="4e9f9-118">包含 OOF 响应。</span><span class="sxs-lookup"><span data-stu-id="4e9f9-118">Contains the OOF response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4e9f9-119">父元素</span><span class="sxs-lookup"><span data-stu-id="4e9f9-119">Parent elements</span></span>

|<span data-ttu-id="4e9f9-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="4e9f9-120">**Element**</span></span>|<span data-ttu-id="4e9f9-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="4e9f9-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4e9f9-122">UserOofSettings</span><span class="sxs-lookup"><span data-stu-id="4e9f9-122">UserOofSettings</span></span>](useroofsettings.md) <br/> |<span data-ttu-id="4e9f9-123">指定 OOF 设置。</span><span class="sxs-lookup"><span data-stu-id="4e9f9-123">Specifies the OOF settings.</span></span>  <br/> <span data-ttu-id="4e9f9-124">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="4e9f9-124">The following is the XPath expression to this element:</span></span>  <br/>  `/SetUserOofSettingsRequest/UserOofSettings` <br/> |
|[<span data-ttu-id="4e9f9-125">OofSettings</span><span class="sxs-lookup"><span data-stu-id="4e9f9-125">OofSettings</span></span>](oofsettings.md) <br/> |<span data-ttu-id="4e9f9-126">包含 OOF 设置。</span><span class="sxs-lookup"><span data-stu-id="4e9f9-126">Contains the OOF settings.</span></span>  <br/> <span data-ttu-id="4e9f9-127">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="4e9f9-127">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserOofSettingsResponse/OofSettings` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4e9f9-128">说明</span><span class="sxs-lookup"><span data-stu-id="4e9f9-128">Remarks</span></span>

<span data-ttu-id="4e9f9-129">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="4e9f9-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="example"></a><span data-ttu-id="4e9f9-130">示例</span><span class="sxs-lookup"><span data-stu-id="4e9f9-130">Example</span></span>

<span data-ttu-id="4e9f9-131">以下示例的 SetUserOofSettings 请求将[OofState](oofstate.md)设置为 "**启用**"，将 "OOF" 的持续时间设置为10天，并设置内部和外部 OOF 邮件。</span><span class="sxs-lookup"><span data-stu-id="4e9f9-131">The following example of a SetUserOofSettings request sets the [OofState](oofstate.md) to **Enabled**, sets the duration of OOF for 10 days, and sets the internal and external OOF messages.</span></span>
  
```XML
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

## <a name="element-information"></a><span data-ttu-id="4e9f9-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="4e9f9-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4e9f9-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="4e9f9-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4e9f9-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="4e9f9-134">Schema Name</span></span>  <br/> |<span data-ttu-id="4e9f9-135">类型架构</span><span class="sxs-lookup"><span data-stu-id="4e9f9-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="4e9f9-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="4e9f9-136">Validation File</span></span>  <br/> |<span data-ttu-id="4e9f9-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4e9f9-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4e9f9-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="4e9f9-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="4e9f9-139">False</span><span class="sxs-lookup"><span data-stu-id="4e9f9-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4e9f9-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4e9f9-140">See also</span></span>



[<span data-ttu-id="4e9f9-141">GetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="4e9f9-141">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)
  
[<span data-ttu-id="4e9f9-142">SetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="4e9f9-142">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

