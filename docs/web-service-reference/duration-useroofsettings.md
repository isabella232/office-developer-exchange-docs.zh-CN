---
title: 持续时间（UserOofSettings）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Duration
api_type:
- schema
ms.assetid: 01d67af3-658e-4acd-93e3-441ae827fdd3
description: Duration 元素指定将 OofState 元素设置为 "计划" 时，"外出" （OOF）状态为 "已启用" 的持续时间。
ms.openlocfilehash: 0ba0f1ea7498781c0cccb072c7ea0fa05414764c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457296"
---
# <a name="duration-useroofsettings"></a><span data-ttu-id="84c5f-103">持续时间（UserOofSettings）</span><span class="sxs-lookup"><span data-stu-id="84c5f-103">Duration (UserOofSettings)</span></span>

<span data-ttu-id="84c5f-104">**Duration**元素指定将[OofState](oofstate.md)元素设置为 "**计划**" 时，"外出" （OOF）状态为 "已启用" 的持续时间。</span><span class="sxs-lookup"><span data-stu-id="84c5f-104">The **Duration** element specifies the duration that the out of office (OOF) status is enabled if the [OofState](oofstate.md) element is set to **Scheduled**.</span></span>
  
```XML
<Duration>
   <StartTime/>
   <EndTime/> 
</Duration>
```

 <span data-ttu-id="84c5f-105">**Duration**</span><span class="sxs-lookup"><span data-stu-id="84c5f-105">**Duration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="84c5f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="84c5f-106">Attributes and elements</span></span>

<span data-ttu-id="84c5f-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="84c5f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="84c5f-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="84c5f-108">Attributes</span></span>

<span data-ttu-id="84c5f-109">无。</span><span class="sxs-lookup"><span data-stu-id="84c5f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="84c5f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="84c5f-110">Child elements</span></span>

|<span data-ttu-id="84c5f-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="84c5f-111">**Element**</span></span>|<span data-ttu-id="84c5f-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="84c5f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="84c5f-113">StartTime</span><span class="sxs-lookup"><span data-stu-id="84c5f-113">StartTime</span></span>](starttime.md) <br/> |<span data-ttu-id="84c5f-114">表示具有 OOF 状态的时间范围集的开始时间。</span><span class="sxs-lookup"><span data-stu-id="84c5f-114">Represents the start of the time span set with an OOF status.</span></span> <span data-ttu-id="84c5f-115">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="84c5f-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="84c5f-116">EndTime</span><span class="sxs-lookup"><span data-stu-id="84c5f-116">EndTime</span></span>](endtime.md) <br/> |<span data-ttu-id="84c5f-117">表示具有 OOF 状态的时间范围设置的结束时间。</span><span class="sxs-lookup"><span data-stu-id="84c5f-117">Represents the end of the time span set with an OOF status.</span></span> <span data-ttu-id="84c5f-118">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="84c5f-118">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="84c5f-119">父元素</span><span class="sxs-lookup"><span data-stu-id="84c5f-119">Parent elements</span></span>

|<span data-ttu-id="84c5f-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="84c5f-120">**Element**</span></span>|<span data-ttu-id="84c5f-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="84c5f-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="84c5f-122">UserOofSettings</span><span class="sxs-lookup"><span data-stu-id="84c5f-122">UserOofSettings</span></span>](useroofsettings.md) <br/> |<span data-ttu-id="84c5f-123">指定 OOF 设置。</span><span class="sxs-lookup"><span data-stu-id="84c5f-123">Specifies the OOF settings.</span></span>  <br/><br/><span data-ttu-id="84c5f-124">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="84c5f-124">The following is the XPath expression to this element:</span></span><br/><br/>`/SetUserOofSettingsRequest/UserOofSettings` <br/> |
|[<span data-ttu-id="84c5f-125">OofSettings</span><span class="sxs-lookup"><span data-stu-id="84c5f-125">OofSettings</span></span>](oofsettings.md) <br/> |<span data-ttu-id="84c5f-126">包含 OOF 设置。</span><span class="sxs-lookup"><span data-stu-id="84c5f-126">Contains the OOF settings.</span></span><br/><br/><span data-ttu-id="84c5f-127">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="84c5f-127">The following is the XPath expression to this element:</span></span><br/><br/>`/GetUserOofSettingsResponse/OofSettings` <br/> |
|[<span data-ttu-id="84c5f-128">外出</span><span class="sxs-lookup"><span data-stu-id="84c5f-128">OutOfOffice</span></span>](outofoffice.md) <br/> |<span data-ttu-id="84c5f-129">定义 "外出（OOF）" 响应消息和发送邮箱响应邮件的持续时间。</span><span class="sxs-lookup"><span data-stu-id="84c5f-129">Defines the Out of Office (OOF) response message and a duration time for sending the response message for a mailbox.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="84c5f-130">备注</span><span class="sxs-lookup"><span data-stu-id="84c5f-130">Remarks</span></span>

<span data-ttu-id="84c5f-131">**持续时间**类型也是[DetailedSuggestionsWindow](detailedsuggestionswindow.md)、 [TimeWindow](timewindow.md)和[外出](outofoffice.md)元素的类型。</span><span class="sxs-lookup"><span data-stu-id="84c5f-131">The **Duration** type is also the type for the [DetailedSuggestionsWindow](detailedsuggestionswindow.md), [TimeWindow](timewindow.md), and [OutOfOffice](outofoffice.md) elements.</span></span> 
  
<span data-ttu-id="84c5f-132">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="84c5f-132">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="example"></a><span data-ttu-id="84c5f-133">示例</span><span class="sxs-lookup"><span data-stu-id="84c5f-133">Example</span></span>

<span data-ttu-id="84c5f-134">以下示例的[SetUserOofSettings 操作](setuseroofsettings-operation.md)请求将[OofState](oofstate.md)设置为 "**启用**"、"内部和外部 OOF" 邮件，并将 "oof" 的持续时间设置为10天。</span><span class="sxs-lookup"><span data-stu-id="84c5f-134">The following example of a [SetUserOofSettings operation](setuseroofsettings-operation.md) request sets the [OofState](oofstate.md) to **Enabled**, the internal and external OOF messages, and sets the duration of OOF for 10 days.</span></span>
  
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
        <SetByLegacyClient>false</SetByLegacyClient>
      </UserOofSettings>
    </SetUserOofSettingsRequest>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a><span data-ttu-id="84c5f-135">元素信息</span><span class="sxs-lookup"><span data-stu-id="84c5f-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="84c5f-136">命名空间</span><span class="sxs-lookup"><span data-stu-id="84c5f-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="84c5f-137">架构名称</span><span class="sxs-lookup"><span data-stu-id="84c5f-137">Schema Name</span></span>  <br/> |<span data-ttu-id="84c5f-138">类型架构</span><span class="sxs-lookup"><span data-stu-id="84c5f-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="84c5f-139">验证文件</span><span class="sxs-lookup"><span data-stu-id="84c5f-139">Validation File</span></span>  <br/> |<span data-ttu-id="84c5f-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="84c5f-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="84c5f-141">可以为空</span><span class="sxs-lookup"><span data-stu-id="84c5f-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="84c5f-142">False</span><span class="sxs-lookup"><span data-stu-id="84c5f-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="84c5f-143">另请参阅</span><span class="sxs-lookup"><span data-stu-id="84c5f-143">See also</span></span>

- [<span data-ttu-id="84c5f-144">GetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="84c5f-144">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)  
- [<span data-ttu-id="84c5f-145">SetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="84c5f-145">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

