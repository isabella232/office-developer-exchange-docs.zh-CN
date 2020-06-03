---
title: OofState
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OofState
api_type:
- schema
ms.assetid: 3c486a38-06da-4382-ad20-664d067d76ac
description: OofState 元素用于获取或设置用户的外出（OOF）状态。
ms.openlocfilehash: 6aef7d989ee6978019a483f2673895e68a88a7c5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459733"
---
# <a name="oofstate"></a><span data-ttu-id="a022a-103">OofState</span><span class="sxs-lookup"><span data-stu-id="a022a-103">OofState</span></span>

<span data-ttu-id="a022a-104">**OofState**元素用于获取或设置用户的外出（OOF）状态。</span><span class="sxs-lookup"><span data-stu-id="a022a-104">The **OofState** element is used to get or set the user's Out of Office (OOF) state.</span></span> 
  
```xml
<OofState>Disabled or Enabled or Scheduled</OofState>
```

 <span data-ttu-id="a022a-105">**OofState**</span><span class="sxs-lookup"><span data-stu-id="a022a-105">**OofState**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a022a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a022a-106">Attributes and elements</span></span>

<span data-ttu-id="a022a-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a022a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a022a-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="a022a-108">Attributes</span></span>

<span data-ttu-id="a022a-109">无。</span><span class="sxs-lookup"><span data-stu-id="a022a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a022a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a022a-110">Child elements</span></span>

<span data-ttu-id="a022a-111">无。</span><span class="sxs-lookup"><span data-stu-id="a022a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a022a-112">父元素</span><span class="sxs-lookup"><span data-stu-id="a022a-112">Parent elements</span></span>

|<span data-ttu-id="a022a-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="a022a-113">**Element**</span></span>|<span data-ttu-id="a022a-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="a022a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a022a-115">UserOofSettings</span><span class="sxs-lookup"><span data-stu-id="a022a-115">UserOofSettings</span></span>](useroofsettings.md) <br/> |<span data-ttu-id="a022a-116">指定 OOF 设置。</span><span class="sxs-lookup"><span data-stu-id="a022a-116">Specifies the OOF settings.</span></span>  <br/> <span data-ttu-id="a022a-117">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="a022a-117">The following is the XPath expression to this element:</span></span>  <br/>  `/SetUserOofSettingsRequest/UserOofSettings` <br/> |
|[<span data-ttu-id="a022a-118">OofSettings</span><span class="sxs-lookup"><span data-stu-id="a022a-118">OofSettings</span></span>](oofsettings.md) <br/> |<span data-ttu-id="a022a-119">包含 OOF 设置。</span><span class="sxs-lookup"><span data-stu-id="a022a-119">Contains the OOF settings.</span></span>  <br/> <span data-ttu-id="a022a-120">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="a022a-120">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserOofSettingsResponse/OofSettings` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a022a-121">文本值</span><span class="sxs-lookup"><span data-stu-id="a022a-121">Text value</span></span>

<span data-ttu-id="a022a-122">**OofState**元素需要 text 值。</span><span class="sxs-lookup"><span data-stu-id="a022a-122">A text value is required for the **OofState** element.</span></span> <span data-ttu-id="a022a-123">以下列表包含此元素的可能值：</span><span class="sxs-lookup"><span data-stu-id="a022a-123">The following list contains the possible values for this element:</span></span> 
  
- <span data-ttu-id="a022a-124">**Disabled**</span><span class="sxs-lookup"><span data-stu-id="a022a-124">**Disabled**</span></span>
    
- <span data-ttu-id="a022a-125">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="a022a-125">**Enabled**</span></span>
    
- <span data-ttu-id="a022a-126">**Scheduled**</span><span class="sxs-lookup"><span data-stu-id="a022a-126">**Scheduled**</span></span>
    
<span data-ttu-id="a022a-127">"**计划**的值" 表示将 OOF 状态设置为 "[持续时间（UserOofSettings）](duration-useroofsettings.md) " 元素所标识的时间段内的 "**已启用**"。</span><span class="sxs-lookup"><span data-stu-id="a022a-127">A value of **Scheduled** indicates that the OOF status is set to **Enabled** during a time period identified by the [Duration (UserOofSettings)](duration-useroofsettings.md) element.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a022a-128">备注</span><span class="sxs-lookup"><span data-stu-id="a022a-128">Remarks</span></span>

<span data-ttu-id="a022a-129">SetUsersOofSettingRequest 消息和 GetUserOofSettingResponse 消息中都需要此元素。</span><span class="sxs-lookup"><span data-stu-id="a022a-129">This element is required in both the SetUsersOofSettingRequest message and the GetUserOofSettingResponse message.</span></span>
  
<span data-ttu-id="a022a-130">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a022a-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="a022a-131">示例</span><span class="sxs-lookup"><span data-stu-id="a022a-131">Example</span></span>

<span data-ttu-id="a022a-132">下面的 SetUserOofSettings 请求示例启用**OofState**。</span><span class="sxs-lookup"><span data-stu-id="a022a-132">The following example of a SetUserOofSettings request enables the **OofState**.</span></span>
  
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

## <a name="element-information"></a><span data-ttu-id="a022a-133">元素信息</span><span class="sxs-lookup"><span data-stu-id="a022a-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a022a-134">命名空间</span><span class="sxs-lookup"><span data-stu-id="a022a-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a022a-135">架构名称</span><span class="sxs-lookup"><span data-stu-id="a022a-135">Schema Name</span></span>  <br/> |<span data-ttu-id="a022a-136">类型架构</span><span class="sxs-lookup"><span data-stu-id="a022a-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="a022a-137">验证文件</span><span class="sxs-lookup"><span data-stu-id="a022a-137">Validation File</span></span>  <br/> |<span data-ttu-id="a022a-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a022a-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a022a-139">可以为空</span><span class="sxs-lookup"><span data-stu-id="a022a-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="a022a-140">False</span><span class="sxs-lookup"><span data-stu-id="a022a-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a022a-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a022a-141">See also</span></span>



[<span data-ttu-id="a022a-142">GetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="a022a-142">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)
  
[<span data-ttu-id="a022a-143">SetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="a022a-143">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

