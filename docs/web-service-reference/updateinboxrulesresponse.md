---
title: UpdateInboxRulesResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateInboxRulesResponse
api_type:
- schema
ms.assetid: 0947b6aa-0d95-421b-aebb-d03021ecc110
description: UpdateInboxRulesResponse 元素定义 UpdateInboxRules 请求的响应。
ms.openlocfilehash: cd64e4546f8d9bf573062d9c982477be3fa4d925
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838394"
---
# <a name="updateinboxrulesresponse"></a><span data-ttu-id="ef3da-103">UpdateInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="ef3da-103">UpdateInboxRulesResponse</span></span>

<span data-ttu-id="ef3da-104">**UpdateInboxRulesResponse**元素定义 UpdateInboxRules 请求的响应。</span><span class="sxs-lookup"><span data-stu-id="ef3da-104">The **UpdateInboxRulesResponse** element defines a response to an UpdateInboxRules request.</span></span> 
  
```XML
<UpdateInboxRulesResponse>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <RuleOperationErrors/>
</UpdateInboxRulesResponse>
```

 <span data-ttu-id="ef3da-105">**UpdateInboxRulesResponseType**</span><span class="sxs-lookup"><span data-stu-id="ef3da-105">**UpdateInboxRulesResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ef3da-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ef3da-106">Attributes and elements</span></span>

<span data-ttu-id="ef3da-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ef3da-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ef3da-108">属性</span><span class="sxs-lookup"><span data-stu-id="ef3da-108">Attributes</span></span>

|<span data-ttu-id="ef3da-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="ef3da-109">**Attribute**</span></span>|<span data-ttu-id="ef3da-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="ef3da-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ef3da-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="ef3da-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="ef3da-112">介绍[取消操作](unsubscribe-operation.md)响应的状态。</span><span class="sxs-lookup"><span data-stu-id="ef3da-112">Describes the status of an [Unsubscribe operation](unsubscribe-operation.md) response.</span></span><br/><br/> <span data-ttu-id="ef3da-113">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="ef3da-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="ef3da-114">-成功</span><span class="sxs-lookup"><span data-stu-id="ef3da-114">-  Success</span></span>  <br/><span data-ttu-id="ef3da-115">-警告</span><span class="sxs-lookup"><span data-stu-id="ef3da-115">-  Warning</span></span>  <br/><span data-ttu-id="ef3da-116">-错误</span><span class="sxs-lookup"><span data-stu-id="ef3da-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="ef3da-117">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="ef3da-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="ef3da-118">**值**</span><span class="sxs-lookup"><span data-stu-id="ef3da-118">**Value**</span></span>|<span data-ttu-id="ef3da-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="ef3da-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ef3da-120">**成功**</span><span class="sxs-lookup"><span data-stu-id="ef3da-120">**Success**</span></span> <br/> |<span data-ttu-id="ef3da-121">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="ef3da-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="ef3da-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="ef3da-122">**Warning**</span></span> <br/> | <span data-ttu-id="ef3da-123">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="ef3da-123">Describes a request that was not processed.</span></span> <span data-ttu-id="ef3da-124">如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="ef3da-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="ef3da-125">以下是源的警告的示例：</span><span class="sxs-lookup"><span data-stu-id="ef3da-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="ef3da-126">-在 Exchange 存储过程批次中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="ef3da-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="ef3da-127">-Active Directory 域服务 (AD DS) 处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="ef3da-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="ef3da-128">的移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="ef3da-128">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="ef3da-129">(MDB)-邮件数据库处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="ef3da-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="ef3da-130">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="ef3da-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="ef3da-131">超出了-配额。</span><span class="sxs-lookup"><span data-stu-id="ef3da-131">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="ef3da-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="ef3da-132">**Error**</span></span> <br/> | <span data-ttu-id="ef3da-133">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="ef3da-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="ef3da-134">错误的来源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="ef3da-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="ef3da-135">-无效属性或元素</span><span class="sxs-lookup"><span data-stu-id="ef3da-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="ef3da-136">-属性或超出范围的元素</span><span class="sxs-lookup"><span data-stu-id="ef3da-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="ef3da-137">-未知的标记</span><span class="sxs-lookup"><span data-stu-id="ef3da-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="ef3da-138">-属性或上下文中无效的元素</span><span class="sxs-lookup"><span data-stu-id="ef3da-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="ef3da-139">-由任何客户端尝试未经授权的访问</span><span class="sxs-lookup"><span data-stu-id="ef3da-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="ef3da-140">的有效的客户端的呼叫的响应中服务器端失败</span><span class="sxs-lookup"><span data-stu-id="ef3da-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/> <br/> <span data-ttu-id="ef3da-141">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="ef3da-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ef3da-142">子元素</span><span class="sxs-lookup"><span data-stu-id="ef3da-142">Child elements</span></span>

|<span data-ttu-id="ef3da-143">**元素**</span><span class="sxs-lookup"><span data-stu-id="ef3da-143">**Element**</span></span>|<span data-ttu-id="ef3da-144">**说明**</span><span class="sxs-lookup"><span data-stu-id="ef3da-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ef3da-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="ef3da-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="ef3da-146">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="ef3da-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="ef3da-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ef3da-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="ef3da-148">提供有关请求的状态信息。</span><span class="sxs-lookup"><span data-stu-id="ef3da-148">Provides status information about the request.</span></span>  <br/> |
|[<span data-ttu-id="ef3da-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="ef3da-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="ef3da-150">当前未使用，供将来使用。</span><span class="sxs-lookup"><span data-stu-id="ef3da-150">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="ef3da-151">它包含的值为 0。</span><span class="sxs-lookup"><span data-stu-id="ef3da-151">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="ef3da-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="ef3da-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="ef3da-153">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="ef3da-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="ef3da-154">RuleOperationErrors</span><span class="sxs-lookup"><span data-stu-id="ef3da-154">RuleOperationErrors</span></span>](ruleoperationerrors.md) <br/> |<span data-ttu-id="ef3da-155">表示一个数组的规则上有一个错误的每个规则字段的验证错误。</span><span class="sxs-lookup"><span data-stu-id="ef3da-155">Represents an array of rule validation errors on each rule field that has an error.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ef3da-156">父元素</span><span class="sxs-lookup"><span data-stu-id="ef3da-156">Parent elements</span></span>

<span data-ttu-id="ef3da-157">无。</span><span class="sxs-lookup"><span data-stu-id="ef3da-157">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="ef3da-158">文本值</span><span class="sxs-lookup"><span data-stu-id="ef3da-158">Text value</span></span>

<span data-ttu-id="ef3da-159">无。</span><span class="sxs-lookup"><span data-stu-id="ef3da-159">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ef3da-160">备注</span><span class="sxs-lookup"><span data-stu-id="ef3da-160">Remarks</span></span>

<span data-ttu-id="ef3da-161">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ef3da-161">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ef3da-162">元素信息</span><span class="sxs-lookup"><span data-stu-id="ef3da-162">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ef3da-163">命名空间</span><span class="sxs-lookup"><span data-stu-id="ef3da-163">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ef3da-164">架构名称</span><span class="sxs-lookup"><span data-stu-id="ef3da-164">Schema name</span></span>  <br/> |<span data-ttu-id="ef3da-165">消息架构</span><span class="sxs-lookup"><span data-stu-id="ef3da-165">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ef3da-166">验证文件</span><span class="sxs-lookup"><span data-stu-id="ef3da-166">Validation file</span></span>  <br/> |<span data-ttu-id="ef3da-167">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ef3da-167">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ef3da-168">可以为空</span><span class="sxs-lookup"><span data-stu-id="ef3da-168">Can be empty</span></span>  <br/> |<span data-ttu-id="ef3da-169">False</span><span class="sxs-lookup"><span data-stu-id="ef3da-169">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ef3da-170">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ef3da-170">See also</span></span>

- [<span data-ttu-id="ef3da-171">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="ef3da-171">UpdateInboxRules</span></span>](updateinboxrules.md)
- [<span data-ttu-id="ef3da-172">UpdateInboxRules 操作</span><span class="sxs-lookup"><span data-stu-id="ef3da-172">UpdateInboxRules operation</span></span>](updateinboxrules-operation.md)
- [<span data-ttu-id="ef3da-173">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="ef3da-173">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

