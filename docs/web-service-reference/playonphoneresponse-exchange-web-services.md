---
title: PlayOnPhoneResponse （Exchange Web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PlayOnPhoneResponse
api_type:
- schema
ms.assetid: 578b70d1-dc9d-4bce-b859-0109b2d2bcec
description: PlayOnPhoneResponse 元素指定在电话上播放语音邮件的请求的响应。
ms.openlocfilehash: 203309bdd6d17b1c78054e673f8a340c2f069b38
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826831"
---
# <a name="playonphoneresponse-exchange-web-services"></a><span data-ttu-id="31c10-103">PlayOnPhoneResponse （Exchange Web 服务）</span><span class="sxs-lookup"><span data-stu-id="31c10-103">PlayOnPhoneResponse (Exchange Web Services)</span></span>

<span data-ttu-id="31c10-104">**PlayOnPhoneResponse**元素指定在电话上播放语音邮件的请求的响应。</span><span class="sxs-lookup"><span data-stu-id="31c10-104">The **PlayOnPhoneResponse** element specifies the response to a request to play a voice mail over the telephone.</span></span> 
  
```xml
<PlayOnPhoneResponse ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <PhoneCallId/>
</PlayOnPhoneResponse>
```

 <span data-ttu-id="31c10-105">**PlayOnPhoneResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="31c10-105">**PlayOnPhoneResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="31c10-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="31c10-106">Attributes and elements</span></span>

<span data-ttu-id="31c10-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="31c10-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="31c10-108">属性</span><span class="sxs-lookup"><span data-stu-id="31c10-108">Attributes</span></span>

|<span data-ttu-id="31c10-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="31c10-109">**Attribute**</span></span>|<span data-ttu-id="31c10-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="31c10-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="31c10-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="31c10-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="31c10-112">介绍响应的状态。</span><span class="sxs-lookup"><span data-stu-id="31c10-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="31c10-113">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="31c10-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="31c10-114">-成功</span><span class="sxs-lookup"><span data-stu-id="31c10-114">-  Success</span></span>  <br/><span data-ttu-id="31c10-115">-警告</span><span class="sxs-lookup"><span data-stu-id="31c10-115">-  Warning</span></span>  <br/><span data-ttu-id="31c10-116">-错误</span><span class="sxs-lookup"><span data-stu-id="31c10-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="31c10-117">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="31c10-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="31c10-118">**值**</span><span class="sxs-lookup"><span data-stu-id="31c10-118">**Value**</span></span>|<span data-ttu-id="31c10-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="31c10-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="31c10-120">**成功**</span><span class="sxs-lookup"><span data-stu-id="31c10-120">**Success**</span></span> <br/> |<span data-ttu-id="31c10-121">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="31c10-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="31c10-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="31c10-122">**Warning**</span></span> <br/> | <span data-ttu-id="31c10-123">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="31c10-123">Describes a request that was not processed.</span></span> <span data-ttu-id="31c10-124">如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="31c10-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="31c10-125">以下是源的警告的示例：</span><span class="sxs-lookup"><span data-stu-id="31c10-125">The following are examples of sources of warnings:</span></span> <br/><br/><span data-ttu-id="31c10-126">-在 Exchange 存储过程批次中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="31c10-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="31c10-127">-Active Directory 域服务 (AD DS) 处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="31c10-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="31c10-128">的已移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="31c10-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="31c10-129">(MDB)-邮件数据库处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="31c10-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="31c10-130">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="31c10-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="31c10-131">已超出-配额。</span><span class="sxs-lookup"><span data-stu-id="31c10-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="31c10-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="31c10-132">**Error**</span></span> <br/> | <span data-ttu-id="31c10-133">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="31c10-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="31c10-134">错误的来源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="31c10-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="31c10-135">-无效属性或元素。</span><span class="sxs-lookup"><span data-stu-id="31c10-135">-  Invalid attributes or elements.</span></span>  <br/><span data-ttu-id="31c10-136">-属性或超出范围的元素</span><span class="sxs-lookup"><span data-stu-id="31c10-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="31c10-137">-未知的标记。</span><span class="sxs-lookup"><span data-stu-id="31c10-137">-  An unknown tag.</span></span>  <br/><span data-ttu-id="31c10-138">-属性或上下文中无效的元素。</span><span class="sxs-lookup"><span data-stu-id="31c10-138">-  An attribute or element that is not valid in the context.</span></span>  <br/><span data-ttu-id="31c10-139">的由任何客户端未经授权的访问尝试。</span><span class="sxs-lookup"><span data-stu-id="31c10-139">-  An unauthorized access attempt by any client.</span></span>  <br/><span data-ttu-id="31c10-140">的中到有效的客户端的呼叫的响应服务器端出现故障。</span><span class="sxs-lookup"><span data-stu-id="31c10-140">-  A server-side failure in response to a valid client-side call.</span></span>  <br/><br/>  <span data-ttu-id="31c10-141">可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素主题中找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="31c10-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) element topics.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="31c10-142">子元素</span><span class="sxs-lookup"><span data-stu-id="31c10-142">Child elements</span></span>

|<span data-ttu-id="31c10-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="31c10-143">**Element**</span></span>|<span data-ttu-id="31c10-144">**说明**</span><span class="sxs-lookup"><span data-stu-id="31c10-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="31c10-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="31c10-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="31c10-146">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="31c10-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="31c10-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="31c10-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="31c10-148">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="31c10-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="31c10-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="31c10-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="31c10-150">当前未使用，保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="31c10-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="31c10-151">此元素包含一个值为 0。</span><span class="sxs-lookup"><span data-stu-id="31c10-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="31c10-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="31c10-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="31c10-153">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="31c10-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="31c10-154">PhoneCallId</span><span class="sxs-lookup"><span data-stu-id="31c10-154">PhoneCallId</span></span>](phonecallid.md) <br/> |<span data-ttu-id="31c10-155">指定的电话呼叫标识符。</span><span class="sxs-lookup"><span data-stu-id="31c10-155">Specifies the telephone call identifier.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="31c10-156">父元素</span><span class="sxs-lookup"><span data-stu-id="31c10-156">Parent elements</span></span>

<span data-ttu-id="31c10-157">无。</span><span class="sxs-lookup"><span data-stu-id="31c10-157">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="31c10-158">备注</span><span class="sxs-lookup"><span data-stu-id="31c10-158">Remarks</span></span>

<span data-ttu-id="31c10-159">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="31c10-159">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="31c10-160">元素信息</span><span class="sxs-lookup"><span data-stu-id="31c10-160">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="31c10-161">命名空间</span><span class="sxs-lookup"><span data-stu-id="31c10-161">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="31c10-162">架构名称</span><span class="sxs-lookup"><span data-stu-id="31c10-162">Schema Name</span></span>  <br/> |<span data-ttu-id="31c10-163">消息架构</span><span class="sxs-lookup"><span data-stu-id="31c10-163">Messages schema</span></span>  <br/> |
|<span data-ttu-id="31c10-164">验证文件</span><span class="sxs-lookup"><span data-stu-id="31c10-164">Validation File</span></span>  <br/> |<span data-ttu-id="31c10-165">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="31c10-165">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="31c10-166">可以为空</span><span class="sxs-lookup"><span data-stu-id="31c10-166">Can be Empty</span></span>  <br/> |<span data-ttu-id="31c10-167">False</span><span class="sxs-lookup"><span data-stu-id="31c10-167">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="31c10-168">另请参阅</span><span class="sxs-lookup"><span data-stu-id="31c10-168">See also</span></span>

- [<span data-ttu-id="31c10-169">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="31c10-169">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

