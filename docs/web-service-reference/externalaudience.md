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
description: ExternalAudience 元素设置或包含一个值，该值确定外部外出（OOF）邮件的发件人。
ms.openlocfilehash: b3fcebd9042b07bb9a8294196799ef2a13d78bdd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530598"
---
# <a name="externalaudience"></a><span data-ttu-id="0de94-103">ExternalAudience</span><span class="sxs-lookup"><span data-stu-id="0de94-103">ExternalAudience</span></span>

<span data-ttu-id="0de94-104">**ExternalAudience**元素设置或包含一个值，该值确定外部外出（OOF）邮件的发件人。</span><span class="sxs-lookup"><span data-stu-id="0de94-104">The **ExternalAudience** element sets or contains a value that determines to whom external Out of Office (OOF) messages are sent.</span></span> 
  
```xml
<ExternalAudience>None or Known or All</ExternalAudience>
```

 <span data-ttu-id="0de94-105">**ExternalAudience**</span><span class="sxs-lookup"><span data-stu-id="0de94-105">**ExternalAudience**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0de94-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0de94-106">Attributes and elements</span></span>

<span data-ttu-id="0de94-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0de94-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0de94-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="0de94-108">Attributes</span></span>

<span data-ttu-id="0de94-109">无。</span><span class="sxs-lookup"><span data-stu-id="0de94-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0de94-110">子元素</span><span class="sxs-lookup"><span data-stu-id="0de94-110">Child elements</span></span>

<span data-ttu-id="0de94-111">无。</span><span class="sxs-lookup"><span data-stu-id="0de94-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0de94-112">父元素</span><span class="sxs-lookup"><span data-stu-id="0de94-112">Parent elements</span></span>

|<span data-ttu-id="0de94-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="0de94-113">**Element**</span></span>|<span data-ttu-id="0de94-114">**描述**</span><span class="sxs-lookup"><span data-stu-id="0de94-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0de94-115">UserOofSettings</span><span class="sxs-lookup"><span data-stu-id="0de94-115">UserOofSettings</span></span>](useroofsettings.md) <br/> |<span data-ttu-id="0de94-116">指定 OOF 设置。</span><span class="sxs-lookup"><span data-stu-id="0de94-116">Specifies the OOF settings.</span></span>  <br/> <span data-ttu-id="0de94-117">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="0de94-117">The following is the XPath expression to this element:</span></span>  <br/>  `/SetUserOofSettingsRequest/UserOofSettings` <br/> |
|[<span data-ttu-id="0de94-118">OofSettings</span><span class="sxs-lookup"><span data-stu-id="0de94-118">OofSettings</span></span>](oofsettings.md) <br/> |<span data-ttu-id="0de94-119">包含 OOF 设置。</span><span class="sxs-lookup"><span data-stu-id="0de94-119">Contains the OOF settings.</span></span>  <br/> <span data-ttu-id="0de94-120">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="0de94-120">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserOofSettingsResponse/OofSettings` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0de94-121">文本值</span><span class="sxs-lookup"><span data-stu-id="0de94-121">Text value</span></span>

<span data-ttu-id="0de94-122">此元素需要一个文本值。</span><span class="sxs-lookup"><span data-stu-id="0de94-122">A text value is required for this element.</span></span> <span data-ttu-id="0de94-123">下表列出了此元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="0de94-123">The following table lists the possible values for this element.</span></span>
  
|<span data-ttu-id="0de94-124">**值**</span><span class="sxs-lookup"><span data-stu-id="0de94-124">**Value**</span></span>|<span data-ttu-id="0de94-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="0de94-125">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0de94-126">**无**</span><span class="sxs-lookup"><span data-stu-id="0de94-126">**None**</span></span> <br/> |<span data-ttu-id="0de94-127">向用户发送邮件的邮箱用户组织外部的电子邮件发件人将不会收到外部 OOF 邮件响应。</span><span class="sxs-lookup"><span data-stu-id="0de94-127">E-mail senders outside the mailbox user's organization who send messages to the user will not receive an external OOF message response.</span></span>  <br/> |
|<span data-ttu-id="0de94-128">**叫做**</span><span class="sxs-lookup"><span data-stu-id="0de94-128">**Known**</span></span> <br/> |<span data-ttu-id="0de94-129">如果邮箱用户的组织外部的电子邮件发件人向用户发送邮件，则仅会收到外部 OOF 邮件响应（如果发件人位于用户的 Exchange 存储联系人列表中）。</span><span class="sxs-lookup"><span data-stu-id="0de94-129">E-mail senders outside the mailbox user's organization who send messages to the user will only receive an external OOF message response if the sender is in the user's Exchange store contact list.</span></span>  <br/> |
|<span data-ttu-id="0de94-130">**All**</span><span class="sxs-lookup"><span data-stu-id="0de94-130">**All**</span></span> <br/> |<span data-ttu-id="0de94-131">将邮件发送给用户的邮箱用户的组织外部的电子邮件发件人将收到外部 OOF 邮件响应。</span><span class="sxs-lookup"><span data-stu-id="0de94-131">E-mail senders outside the mailbox user's organization who send messages to the user will receive an external OOF message response.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0de94-132">备注</span><span class="sxs-lookup"><span data-stu-id="0de94-132">Remarks</span></span>

<span data-ttu-id="0de94-133">此元素与[AllowExternalOof](allowexternaloof.md)元素共享相同的类型。</span><span class="sxs-lookup"><span data-stu-id="0de94-133">This element shares the same type as the [AllowExternalOof](allowexternaloof.md) element.</span></span> 
  
<span data-ttu-id="0de94-134">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="0de94-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="0de94-135">示例</span><span class="sxs-lookup"><span data-stu-id="0de94-135">Example</span></span>

<span data-ttu-id="0de94-136">以下示例的 SetUserOofSettings 请求将 OoFState 设置为 "**启用**"，将外部受众设置为 "**所有**"，将 "OOF" 的持续时间设置为 "10 天"，并设置内部和外部 OOF 邮件。</span><span class="sxs-lookup"><span data-stu-id="0de94-136">The following example of a SetUserOofSettings request sets the OoFState to **Enabled**, sets the external audience to **All**, sets the duration of OOF to 10 days, and sets the internal and external OOF messages.</span></span>
  
```
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

## <a name="element-information"></a><span data-ttu-id="0de94-137">元素信息</span><span class="sxs-lookup"><span data-stu-id="0de94-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0de94-138">命名空间</span><span class="sxs-lookup"><span data-stu-id="0de94-138">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0de94-139">架构名称</span><span class="sxs-lookup"><span data-stu-id="0de94-139">Schema Name</span></span>  <br/> |<span data-ttu-id="0de94-140">类型架构</span><span class="sxs-lookup"><span data-stu-id="0de94-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="0de94-141">验证文件</span><span class="sxs-lookup"><span data-stu-id="0de94-141">Validation File</span></span>  <br/> |<span data-ttu-id="0de94-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0de94-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0de94-143">可以为空</span><span class="sxs-lookup"><span data-stu-id="0de94-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="0de94-144">False</span><span class="sxs-lookup"><span data-stu-id="0de94-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0de94-145">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0de94-145">See also</span></span>



[<span data-ttu-id="0de94-146">GetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="0de94-146">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)
  
[<span data-ttu-id="0de94-147">SetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="0de94-147">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

