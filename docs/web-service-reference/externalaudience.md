---
title: ExternalAudience
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExternalAudience
api_type:
- schema
ms.assetid: 79dc2a4c-f7dd-46d1-8f31-149116e1f76e
description: ExternalAudience 元素设置，或包含一个值，确定向其发送外部外出 (OOF) 邮件。
ms.openlocfilehash: 836b0f6a5140a37e1584f571cb8e26534fe7a25f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754252"
---
# <a name="externalaudience"></a><span data-ttu-id="52882-103">ExternalAudience</span><span class="sxs-lookup"><span data-stu-id="52882-103">ExternalAudience</span></span>

<span data-ttu-id="52882-104">**ExternalAudience**元素设置，或包含一个值，确定向其发送外部外出 (OOF) 邮件。</span><span class="sxs-lookup"><span data-stu-id="52882-104">The **ExternalAudience** element sets or contains a value that determines to whom external Out of Office (OOF) messages are sent.</span></span> 
  
```xml
<ExternalAudience>None or Known or All</ExternalAudience>
```

 <span data-ttu-id="52882-105">**ExternalAudience**</span><span class="sxs-lookup"><span data-stu-id="52882-105">**ExternalAudience**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="52882-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="52882-106">Attributes and elements</span></span>

<span data-ttu-id="52882-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="52882-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="52882-108">属性</span><span class="sxs-lookup"><span data-stu-id="52882-108">Attributes</span></span>

<span data-ttu-id="52882-109">无。</span><span class="sxs-lookup"><span data-stu-id="52882-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="52882-110">子元素</span><span class="sxs-lookup"><span data-stu-id="52882-110">Child elements</span></span>

<span data-ttu-id="52882-111">无。</span><span class="sxs-lookup"><span data-stu-id="52882-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="52882-112">父元素</span><span class="sxs-lookup"><span data-stu-id="52882-112">Parent elements</span></span>

|<span data-ttu-id="52882-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="52882-113">**Element**</span></span>|<span data-ttu-id="52882-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="52882-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="52882-115">UserOofSettings</span><span class="sxs-lookup"><span data-stu-id="52882-115">UserOofSettings</span></span>](useroofsettings.md) <br/> |<span data-ttu-id="52882-116">指定 OOF 设置。</span><span class="sxs-lookup"><span data-stu-id="52882-116">Specifies the OOF settings.</span></span>  <br/> <span data-ttu-id="52882-117">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="52882-117">The following is the XPath expression to this element:</span></span>  <br/>  `/SetUserOofSettingsRequest/UserOofSettings` <br/> |
|[<span data-ttu-id="52882-118">OofSettings</span><span class="sxs-lookup"><span data-stu-id="52882-118">OofSettings</span></span>](oofsettings.md) <br/> |<span data-ttu-id="52882-119">包含 OOF 设置。</span><span class="sxs-lookup"><span data-stu-id="52882-119">Contains the OOF settings.</span></span>  <br/> <span data-ttu-id="52882-120">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="52882-120">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserOofSettingsResponse/OofSettings` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="52882-121">文本值</span><span class="sxs-lookup"><span data-stu-id="52882-121">Text value</span></span>

<span data-ttu-id="52882-122">需要为此元素的文本值。</span><span class="sxs-lookup"><span data-stu-id="52882-122">A text value is required for this element.</span></span> <span data-ttu-id="52882-123">下表列出了此元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="52882-123">The following table lists the possible values for this element.</span></span>
  
|<span data-ttu-id="52882-124">**值**</span><span class="sxs-lookup"><span data-stu-id="52882-124">**Value**</span></span>|<span data-ttu-id="52882-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="52882-125">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="52882-126">**None**</span><span class="sxs-lookup"><span data-stu-id="52882-126">**None**</span></span> <br/> |<span data-ttu-id="52882-127">邮箱用户的组织外部的电子邮件发件人将邮件发送到用户不会收到外部 OOF 消息响应。</span><span class="sxs-lookup"><span data-stu-id="52882-127">E-mail senders outside the mailbox user's organization who send messages to the user will not receive an external OOF message response.</span></span>  <br/> |
|<span data-ttu-id="52882-128">**已知**</span><span class="sxs-lookup"><span data-stu-id="52882-128">**Known**</span></span> <br/> |<span data-ttu-id="52882-129">邮箱用户的组织外部的电子邮件发件人发送给用户的消息将仅接收外部 OOF 消息响应如果发件人是用户的 Exchange 中存储的联系人列表。</span><span class="sxs-lookup"><span data-stu-id="52882-129">E-mail senders outside the mailbox user's organization who send messages to the user will only receive an external OOF message response if the sender is in the user's Exchange store contact list.</span></span>  <br/> |
|<span data-ttu-id="52882-130">**All**</span><span class="sxs-lookup"><span data-stu-id="52882-130">**All**</span></span> <br/> |<span data-ttu-id="52882-131">邮箱用户的组织外部的电子邮件发件人将邮件发送到用户将收到外部 OOF 消息响应。</span><span class="sxs-lookup"><span data-stu-id="52882-131">E-mail senders outside the mailbox user's organization who send messages to the user will receive an external OOF message response.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="52882-132">备注</span><span class="sxs-lookup"><span data-stu-id="52882-132">Remarks</span></span>

<span data-ttu-id="52882-133">此元素共享[AllowExternalOof](allowexternaloof.md)元素类型相同。</span><span class="sxs-lookup"><span data-stu-id="52882-133">This element shares the same type as the [AllowExternalOof](allowexternaloof.md) element.</span></span> 
  
<span data-ttu-id="52882-134">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="52882-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="52882-135">示例</span><span class="sxs-lookup"><span data-stu-id="52882-135">Example</span></span>

<span data-ttu-id="52882-136">下面的示例的 SetUserOofSettings 请求将 OoFState 设置为**已启用**，将外部访问群体设置为**所有**、 将 OOF 的持续时间设置为 10 天，并设置内部和外部 OOF 邮件。</span><span class="sxs-lookup"><span data-stu-id="52882-136">The following example of a SetUserOofSettings request sets the OoFState to **Enabled**, sets the external audience to **All**, sets the duration of OOF to 10 days, and sets the internal and external OOF messages.</span></span>
  
```
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

## <a name="element-information"></a><span data-ttu-id="52882-137">元素信息</span><span class="sxs-lookup"><span data-stu-id="52882-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="52882-138">命名空间</span><span class="sxs-lookup"><span data-stu-id="52882-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="52882-139">架构名称</span><span class="sxs-lookup"><span data-stu-id="52882-139">Schema Name</span></span>  <br/> |<span data-ttu-id="52882-140">类型架构</span><span class="sxs-lookup"><span data-stu-id="52882-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="52882-141">验证文件</span><span class="sxs-lookup"><span data-stu-id="52882-141">Validation File</span></span>  <br/> |<span data-ttu-id="52882-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="52882-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="52882-143">可以为空</span><span class="sxs-lookup"><span data-stu-id="52882-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="52882-144">False</span><span class="sxs-lookup"><span data-stu-id="52882-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="52882-145">另请参阅</span><span class="sxs-lookup"><span data-stu-id="52882-145">See also</span></span>



[<span data-ttu-id="52882-146">GetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="52882-146">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)
  
[<span data-ttu-id="52882-147">SetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="52882-147">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

