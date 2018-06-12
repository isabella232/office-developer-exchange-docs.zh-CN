---
title: MailTipsResponseMessageType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailTipsResponseMessageType
api_type:
- schema
ms.assetid: 532cb9d9-1232-4e88-80aa-4cf163eb05da
description: MailTipsResponseMessageType 元素均表示邮件提示设置。
ms.openlocfilehash: 76a1e33ae189b96a96a41d1bc7a8f79116761c4f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826334"
---
# <a name="mailtipsresponsemessagetype"></a><span data-ttu-id="fe9b8-103">MailTipsResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="fe9b8-103">MailTipsResponseMessageType</span></span>

<span data-ttu-id="fe9b8-104">**MailTipsResponseMessageType**元素均表示邮件提示设置。</span><span class="sxs-lookup"><span data-stu-id="fe9b8-104">The **MailTipsResponseMessageType** element represents mail tips settings.</span></span> 
  
```XML
<MailTipsResponseMessageType ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <MailTips/>
</MailTipsResponseMessageType>
```

 <span data-ttu-id="fe9b8-105">**MailTipsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="fe9b8-105">**MailTipsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fe9b8-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fe9b8-106">Attributes and elements</span></span>

<span data-ttu-id="fe9b8-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fe9b8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fe9b8-108">属性</span><span class="sxs-lookup"><span data-stu-id="fe9b8-108">Attributes</span></span>

|<span data-ttu-id="fe9b8-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="fe9b8-109">**Attribute**</span></span>|<span data-ttu-id="fe9b8-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="fe9b8-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fe9b8-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="fe9b8-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="fe9b8-112">介绍响应的状态。</span><span class="sxs-lookup"><span data-stu-id="fe9b8-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="fe9b8-113">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="fe9b8-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="fe9b8-114">-成功</span><span class="sxs-lookup"><span data-stu-id="fe9b8-114">-  Success</span></span>  <br/><span data-ttu-id="fe9b8-115">-警告</span><span class="sxs-lookup"><span data-stu-id="fe9b8-115">-  Warning</span></span>  <br/><span data-ttu-id="fe9b8-116">-错误</span><span class="sxs-lookup"><span data-stu-id="fe9b8-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="fe9b8-117">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="fe9b8-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="fe9b8-118">**值**</span><span class="sxs-lookup"><span data-stu-id="fe9b8-118">**Value**</span></span>|<span data-ttu-id="fe9b8-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="fe9b8-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fe9b8-120">**成功**</span><span class="sxs-lookup"><span data-stu-id="fe9b8-120">**Success**</span></span> <br/> |<span data-ttu-id="fe9b8-121">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="fe9b8-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="fe9b8-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="fe9b8-122">**Warning**</span></span> <br/> | <span data-ttu-id="fe9b8-123">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="fe9b8-123">Describes a request that was not processed.</span></span> <span data-ttu-id="fe9b8-124">如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="fe9b8-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="fe9b8-125">以下是源的警告的示例：</span><span class="sxs-lookup"><span data-stu-id="fe9b8-125">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="fe9b8-126">-在 Exchange 存储过程批次中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="fe9b8-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="fe9b8-127">-Active Directory 域服务 (AD DS) 处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="fe9b8-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="fe9b8-128">的已移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="fe9b8-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="fe9b8-129">(MDB)-邮件数据库处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="fe9b8-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="fe9b8-130">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="fe9b8-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="fe9b8-131">已超出-配额。</span><span class="sxs-lookup"><span data-stu-id="fe9b8-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="fe9b8-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="fe9b8-132">**Error**</span></span> <br/> | <span data-ttu-id="fe9b8-133">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="fe9b8-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="fe9b8-134">错误的来源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="fe9b8-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="fe9b8-135">-无效属性或元素</span><span class="sxs-lookup"><span data-stu-id="fe9b8-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="fe9b8-136">-属性或超出范围的元素</span><span class="sxs-lookup"><span data-stu-id="fe9b8-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="fe9b8-137">-未知的标记</span><span class="sxs-lookup"><span data-stu-id="fe9b8-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="fe9b8-138">-属性或上下文中无效的元素</span><span class="sxs-lookup"><span data-stu-id="fe9b8-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="fe9b8-139">-由任何客户端尝试未经授权的访问</span><span class="sxs-lookup"><span data-stu-id="fe9b8-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="fe9b8-140">的有效的客户端的呼叫的响应中服务器端失败</span><span class="sxs-lookup"><span data-stu-id="fe9b8-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="fe9b8-141">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="fe9b8-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="fe9b8-142">子元素</span><span class="sxs-lookup"><span data-stu-id="fe9b8-142">Child elements</span></span>

|<span data-ttu-id="fe9b8-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="fe9b8-143">**Element**</span></span>|<span data-ttu-id="fe9b8-144">**说明**</span><span class="sxs-lookup"><span data-stu-id="fe9b8-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fe9b8-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="fe9b8-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="fe9b8-146">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="fe9b8-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="fe9b8-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="fe9b8-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="fe9b8-148">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="fe9b8-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="fe9b8-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="fe9b8-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="fe9b8-150">当前未使用，保留以供将来使用。</span><span class="sxs-lookup"><span data-stu-id="fe9b8-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="fe9b8-151">此元素包含一个值为 0。</span><span class="sxs-lookup"><span data-stu-id="fe9b8-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="fe9b8-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="fe9b8-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="fe9b8-153">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="fe9b8-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="fe9b8-154">邮件提示</span><span class="sxs-lookup"><span data-stu-id="fe9b8-154">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="fe9b8-155">表示的邮件提示的各种类型的值。</span><span class="sxs-lookup"><span data-stu-id="fe9b8-155">Represents values for various types of mail tips.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fe9b8-156">父元素</span><span class="sxs-lookup"><span data-stu-id="fe9b8-156">Parent elements</span></span>

|<span data-ttu-id="fe9b8-157">**元素**</span><span class="sxs-lookup"><span data-stu-id="fe9b8-157">**Element**</span></span>|<span data-ttu-id="fe9b8-158">**说明**</span><span class="sxs-lookup"><span data-stu-id="fe9b8-158">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fe9b8-159">ResponseMessages (ArrayOfMailTipsResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="fe9b8-159">ResponseMessages (ArrayOfMailTipsResponseMessageType)</span></span>](responsemessages-arrayofmailtipsresponsemessagetype.md) <br/> |<span data-ttu-id="fe9b8-160">代表一个邮件提示响应的列表。</span><span class="sxs-lookup"><span data-stu-id="fe9b8-160">Represents a list of mail tips response messages.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fe9b8-161">文本值</span><span class="sxs-lookup"><span data-stu-id="fe9b8-161">Text value</span></span>

<span data-ttu-id="fe9b8-162">无。</span><span class="sxs-lookup"><span data-stu-id="fe9b8-162">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fe9b8-163">备注</span><span class="sxs-lookup"><span data-stu-id="fe9b8-163">Remarks</span></span>

<span data-ttu-id="fe9b8-164">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="fe9b8-164">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fe9b8-165">元素信息</span><span class="sxs-lookup"><span data-stu-id="fe9b8-165">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fe9b8-166">命名空间</span><span class="sxs-lookup"><span data-stu-id="fe9b8-166">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="fe9b8-167">架构名称</span><span class="sxs-lookup"><span data-stu-id="fe9b8-167">Schema Name</span></span>  <br/> |<span data-ttu-id="fe9b8-168">消息架构</span><span class="sxs-lookup"><span data-stu-id="fe9b8-168">Messages schema</span></span>  <br/> |
|<span data-ttu-id="fe9b8-169">验证文件</span><span class="sxs-lookup"><span data-stu-id="fe9b8-169">Validation File</span></span>  <br/> |<span data-ttu-id="fe9b8-170">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="fe9b8-170">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="fe9b8-171">可以为空</span><span class="sxs-lookup"><span data-stu-id="fe9b8-171">Can be Empty</span></span>  <br/> |<span data-ttu-id="fe9b8-172">False</span><span class="sxs-lookup"><span data-stu-id="fe9b8-172">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fe9b8-173">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fe9b8-173">See also</span></span>

- [<span data-ttu-id="fe9b8-174">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="fe9b8-174">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

