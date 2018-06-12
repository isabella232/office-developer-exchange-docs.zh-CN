---
title: GetInboxRulesResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetInboxRulesResponse
api_type:
- schema
ms.assetid: 6d6c1950-c328-489a-94bf-a250fdbd5cd9
description: GetInboxRulesResponse 元素定义 GetInboxRules 操作请求的响应。
ms.openlocfilehash: d84064ab777fe13ded7727381842ddd1ee9d047d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754599"
---
# <a name="getinboxrulesresponse"></a><span data-ttu-id="9b232-103">GetInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="9b232-103">GetInboxRulesResponse</span></span>

<span data-ttu-id="9b232-104">**GetInboxRulesResponse**元素定义[GetInboxRules 操作](getinboxrules-operation.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="9b232-104">The **GetInboxRulesResponse** element defines a response to a [GetInboxRules operation](getinboxrules-operation.md) request.</span></span> 
  
```XML
<GetInboxRulesResponse ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <OutlookRuleBlobExists/>
   <InboxRules/>
</GetInboxRulesResponse>
```

 <span data-ttu-id="9b232-105">**GetInboxRulesResponseType**</span><span class="sxs-lookup"><span data-stu-id="9b232-105">**GetInboxRulesResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9b232-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9b232-106">Attributes and elements</span></span>

<span data-ttu-id="9b232-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9b232-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9b232-108">属性</span><span class="sxs-lookup"><span data-stu-id="9b232-108">Attributes</span></span>

|<span data-ttu-id="9b232-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="9b232-109">**Attribute**</span></span>|<span data-ttu-id="9b232-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="9b232-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9b232-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="9b232-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="9b232-112">描述[GetInboxRules 操作](getinboxrules-operation.md)的响应的状态。</span><span class="sxs-lookup"><span data-stu-id="9b232-112">Describes the status of a [GetInboxRules operation](getinboxrules-operation.md) response.</span></span> <br/><br/><span data-ttu-id="9b232-113">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="9b232-113">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="9b232-114">-成功</span><span class="sxs-lookup"><span data-stu-id="9b232-114">-  Success</span></span>  <br/><span data-ttu-id="9b232-115">-警告</span><span class="sxs-lookup"><span data-stu-id="9b232-115">-  Warning</span></span>  <br/><span data-ttu-id="9b232-116">-错误</span><span class="sxs-lookup"><span data-stu-id="9b232-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="9b232-117">ResponseClass 属性</span><span class="sxs-lookup"><span data-stu-id="9b232-117">ResponseClass Attribute</span></span>

|<span data-ttu-id="9b232-118">**值**</span><span class="sxs-lookup"><span data-stu-id="9b232-118">**Value**</span></span>|<span data-ttu-id="9b232-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="9b232-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9b232-120">**成功**</span><span class="sxs-lookup"><span data-stu-id="9b232-120">**Success**</span></span> <br/> |<span data-ttu-id="9b232-121">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="9b232-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="9b232-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="9b232-122">**Warning**</span></span> <br/> | <span data-ttu-id="9b232-123">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="9b232-123">Describes a request that was not processed.</span></span> <span data-ttu-id="9b232-124">如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="9b232-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="9b232-125">以下是源的警告的示例：</span><span class="sxs-lookup"><span data-stu-id="9b232-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="9b232-126">-在 Exchange 存储过程批次中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="9b232-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="9b232-127">-Active Directory 域服务 (AD DS) 处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="9b232-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="9b232-128">的移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="9b232-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="9b232-129">(MDB)-邮件数据库处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="9b232-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="9b232-130">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="9b232-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="9b232-131">超出了-配额。</span><span class="sxs-lookup"><span data-stu-id="9b232-131">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="9b232-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="9b232-132">**Error**</span></span> <br/> | <span data-ttu-id="9b232-133">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="9b232-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="9b232-134">错误的来源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="9b232-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="9b232-135">-无效属性或元素</span><span class="sxs-lookup"><span data-stu-id="9b232-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="9b232-136">-属性或超出范围的元素</span><span class="sxs-lookup"><span data-stu-id="9b232-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="9b232-137">-未知的标记</span><span class="sxs-lookup"><span data-stu-id="9b232-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="9b232-138">-属性或上下文中无效的元素</span><span class="sxs-lookup"><span data-stu-id="9b232-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="9b232-139">-由任何客户端尝试未经授权的访问</span><span class="sxs-lookup"><span data-stu-id="9b232-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="9b232-140">的有效的客户端的呼叫的响应中服务器端失败</span><span class="sxs-lookup"><span data-stu-id="9b232-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="9b232-141">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="9b232-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9b232-142">子元素</span><span class="sxs-lookup"><span data-stu-id="9b232-142">Child elements</span></span>

|<span data-ttu-id="9b232-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="9b232-143">**Element**</span></span>|<span data-ttu-id="9b232-144">**说明**</span><span class="sxs-lookup"><span data-stu-id="9b232-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9b232-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="9b232-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="9b232-146">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="9b232-146">Provides text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="9b232-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="9b232-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="9b232-148">提供有关请求的状态信息。</span><span class="sxs-lookup"><span data-stu-id="9b232-148">Provides status information about the request.</span></span>  <br/> |
|[<span data-ttu-id="9b232-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="9b232-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="9b232-150">当前未使用，供将来使用。</span><span class="sxs-lookup"><span data-stu-id="9b232-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="9b232-151">它包含的值为 0。</span><span class="sxs-lookup"><span data-stu-id="9b232-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="9b232-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="9b232-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="9b232-153">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="9b232-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="9b232-154">OutlookRuleBlobExists</span><span class="sxs-lookup"><span data-stu-id="9b232-154">OutlookRuleBlobExists</span></span>](outlookruleblobexists.md) <br/> |<span data-ttu-id="9b232-155">指示 Microsoft Outlook 规则 blob 是否存在用户的邮箱中。</span><span class="sxs-lookup"><span data-stu-id="9b232-155">Indicates whether a Microsoft Outlook rule blob exists in the user's mailbox.</span></span>  <br/> |
|[<span data-ttu-id="9b232-156">InboxRules</span><span class="sxs-lookup"><span data-stu-id="9b232-156">InboxRules</span></span>](inboxrules.md) <br/> |<span data-ttu-id="9b232-157">代表用户的邮箱中的规则的数组。</span><span class="sxs-lookup"><span data-stu-id="9b232-157">Represents an array of the rules in the user's mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9b232-158">父元素</span><span class="sxs-lookup"><span data-stu-id="9b232-158">Parent elements</span></span>

<span data-ttu-id="9b232-159">无。</span><span class="sxs-lookup"><span data-stu-id="9b232-159">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="9b232-160">文本值</span><span class="sxs-lookup"><span data-stu-id="9b232-160">Text value</span></span>

<span data-ttu-id="9b232-161">无。</span><span class="sxs-lookup"><span data-stu-id="9b232-161">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9b232-162">备注</span><span class="sxs-lookup"><span data-stu-id="9b232-162">Remarks</span></span>

<span data-ttu-id="9b232-163">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9b232-163">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9b232-164">元素信息</span><span class="sxs-lookup"><span data-stu-id="9b232-164">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9b232-165">命名空间</span><span class="sxs-lookup"><span data-stu-id="9b232-165">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9b232-166">架构名称</span><span class="sxs-lookup"><span data-stu-id="9b232-166">Schema name</span></span>  <br/> |<span data-ttu-id="9b232-167">消息架构</span><span class="sxs-lookup"><span data-stu-id="9b232-167">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9b232-168">验证文件</span><span class="sxs-lookup"><span data-stu-id="9b232-168">Validation file</span></span>  <br/> |<span data-ttu-id="9b232-169">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9b232-169">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9b232-170">可以为空</span><span class="sxs-lookup"><span data-stu-id="9b232-170">Can be empty</span></span>  <br/> |<span data-ttu-id="9b232-171">False</span><span class="sxs-lookup"><span data-stu-id="9b232-171">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9b232-172">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9b232-172">See also</span></span>

- [<span data-ttu-id="9b232-173">GetInboxRules</span><span class="sxs-lookup"><span data-stu-id="9b232-173">GetInboxRules</span></span>](getinboxrules.md)
- [<span data-ttu-id="9b232-174">GetInboxRules 操作</span><span class="sxs-lookup"><span data-stu-id="9b232-174">GetInboxRules operation</span></span>](getinboxrules-operation.md)

