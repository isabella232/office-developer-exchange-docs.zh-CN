---
title: GetPasswordExpirationDateResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3d3fff1f-ef13-46d5-bd7f-ef535eb80c72
description: GetPasswordExpirationDateResponse 元素定义 GetPasswordExpirationDate 操作操作请求的响应。
ms.openlocfilehash: 3754a53da53c12479f11c2e32cd15a08cba665fb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754656"
---
# <a name="getpasswordexpirationdateresponse"></a><span data-ttu-id="33c0c-103">GetPasswordExpirationDateResponse</span><span class="sxs-lookup"><span data-stu-id="33c0c-103">GetPasswordExpirationDateResponse</span></span>

<span data-ttu-id="33c0c-104">**GetPasswordExpirationDateResponse**元素定义[GetPasswordExpirationDate 操作](getpasswordexpirationdate-operation.md)操作请求的响应。</span><span class="sxs-lookup"><span data-stu-id="33c0c-104">The **GetPasswordExpirationDateResponse** element defines the response to a [GetPasswordExpirationDate operation](getpasswordexpirationdate-operation.md) operation request.</span></span> 
  
- [<span data-ttu-id="33c0c-105">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="33c0c-105">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="33c0c-106">GetPasswordExpirationDateResponse</span><span class="sxs-lookup"><span data-stu-id="33c0c-106">GetPasswordExpirationDateResponse</span></span>](getpasswordexpirationdateresponse.md)
  
```XML
<GetPasswordExpirationDateResponse>
    <PasswordExpirationDate />
</GetPasswordExpirationDateResponse>
```

 <span data-ttu-id="33c0c-107">**GetPasswordExpirationDateResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="33c0c-107">**GetPasswordExpirationDateResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="33c0c-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="33c0c-108">Attributes and elements</span></span>

<span data-ttu-id="33c0c-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="33c0c-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="33c0c-110">属性</span><span class="sxs-lookup"><span data-stu-id="33c0c-110">Attributes</span></span>

|<span data-ttu-id="33c0c-111">**属性**</span><span class="sxs-lookup"><span data-stu-id="33c0c-111">**Attribute**</span></span>|<span data-ttu-id="33c0c-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="33c0c-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="33c0c-113">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="33c0c-113">**ResponseClass**</span></span> <br/> | <span data-ttu-id="33c0c-114">介绍响应的状态。</span><span class="sxs-lookup"><span data-stu-id="33c0c-114">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="33c0c-115">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="33c0c-115">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="33c0c-116">-成功</span><span class="sxs-lookup"><span data-stu-id="33c0c-116">-  Success</span></span>  <br/><span data-ttu-id="33c0c-117">-警告</span><span class="sxs-lookup"><span data-stu-id="33c0c-117">-  Warning</span></span>  <br/><span data-ttu-id="33c0c-118">-错误</span><span class="sxs-lookup"><span data-stu-id="33c0c-118">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="33c0c-119">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="33c0c-119">ResponseClass attribute values</span></span>

|<span data-ttu-id="33c0c-120">**值**</span><span class="sxs-lookup"><span data-stu-id="33c0c-120">**Value**</span></span>|<span data-ttu-id="33c0c-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="33c0c-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="33c0c-122">**成功**</span><span class="sxs-lookup"><span data-stu-id="33c0c-122">**Success**</span></span> <br/> |<span data-ttu-id="33c0c-123">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="33c0c-123">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="33c0c-124">**Warning**</span><span class="sxs-lookup"><span data-stu-id="33c0c-124">**Warning**</span></span> <br/> | <span data-ttu-id="33c0c-125">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="33c0c-125">Describes a request that was not processed.</span></span> <span data-ttu-id="33c0c-126">如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="33c0c-126">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="33c0c-127">以下是源的警告的示例：</span><span class="sxs-lookup"><span data-stu-id="33c0c-127">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="33c0c-128">-在 Exchange 存储过程批次中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="33c0c-128">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="33c0c-129">-Active Directory 域服务 (AD DS) 处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="33c0c-129">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="33c0c-130">的已移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="33c0c-130">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="33c0c-131">(MDB)-邮件数据库处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="33c0c-131">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="33c0c-132">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="33c0c-132">-  A password is expired.</span></span>  <br/><span data-ttu-id="33c0c-133">已超出-配额。</span><span class="sxs-lookup"><span data-stu-id="33c0c-133">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="33c0c-134">**Error**</span><span class="sxs-lookup"><span data-stu-id="33c0c-134">**Error**</span></span> <br/> | <span data-ttu-id="33c0c-135">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="33c0c-135">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="33c0c-136">错误的来源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="33c0c-136">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="33c0c-137">-无效属性或元素。</span><span class="sxs-lookup"><span data-stu-id="33c0c-137">-  Invalid attributes or elements.</span></span>  <br/><span data-ttu-id="33c0c-138">-属性或超出范围的元素。</span><span class="sxs-lookup"><span data-stu-id="33c0c-138">-  Attributes or elements that are out of range.</span></span>  <br/><span data-ttu-id="33c0c-139">-未知的标记。</span><span class="sxs-lookup"><span data-stu-id="33c0c-139">-  An unknown tag.</span></span>  <br/><span data-ttu-id="33c0c-140">-属性或上下文中无效的元素。</span><span class="sxs-lookup"><span data-stu-id="33c0c-140">-  An attribute or element that is not valid in the context.</span></span>  <br/><span data-ttu-id="33c0c-141">的由任何客户端未经授权的访问尝试。</span><span class="sxs-lookup"><span data-stu-id="33c0c-141">-  An unauthorized access attempt by any client.</span></span>  <br/><span data-ttu-id="33c0c-142">的中到有效的客户端的呼叫的响应服务器端出现故障。</span><span class="sxs-lookup"><span data-stu-id="33c0c-142">-  A server-side failure in response to a valid client-side call.</span></span>  <br/><br/>  <span data-ttu-id="33c0c-143">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="33c0c-143">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="33c0c-144">子元素</span><span class="sxs-lookup"><span data-stu-id="33c0c-144">Child elements</span></span>

|<span data-ttu-id="33c0c-145">**元素名**</span><span class="sxs-lookup"><span data-stu-id="33c0c-145">**Element name**</span></span>|<span data-ttu-id="33c0c-146">**说明**</span><span class="sxs-lookup"><span data-stu-id="33c0c-146">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="33c0c-147">PasswordExpirationDate</span><span class="sxs-lookup"><span data-stu-id="33c0c-147">PasswordExpirationDate</span></span>](passwordexpirationdate.md) <br/> |<span data-ttu-id="33c0c-148">提供请求中指定的电子邮件帐户的密码到期日期。</span><span class="sxs-lookup"><span data-stu-id="33c0c-148">Provides the password expiration date for the email account specified in the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="33c0c-149">父元素</span><span class="sxs-lookup"><span data-stu-id="33c0c-149">Parent elements</span></span>

|<span data-ttu-id="33c0c-150">**元素名**</span><span class="sxs-lookup"><span data-stu-id="33c0c-150">**Element name**</span></span>|<span data-ttu-id="33c0c-151">**说明**</span><span class="sxs-lookup"><span data-stu-id="33c0c-151">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="33c0c-152">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="33c0c-152">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="33c0c-153">包含为 Exchange Web Services (EWS) 请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="33c0c-153">Contains the response messages for an Exchange Web Services (EWS) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="33c0c-154">备注</span><span class="sxs-lookup"><span data-stu-id="33c0c-154">Remarks</span></span>

<span data-ttu-id="33c0c-155">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="33c0c-155">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="33c0c-156">Exchange Server 2010 Service Pack 2 (SP2) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="33c0c-156">This element was introduced in Exchange Server 2010 Service Pack 2 (SP2).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="33c0c-157">元素信息</span><span class="sxs-lookup"><span data-stu-id="33c0c-157">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="33c0c-158">命名空间</span><span class="sxs-lookup"><span data-stu-id="33c0c-158">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="33c0c-159">架构名称</span><span class="sxs-lookup"><span data-stu-id="33c0c-159">Schema Name</span></span>  <br/> |<span data-ttu-id="33c0c-160">消息架构</span><span class="sxs-lookup"><span data-stu-id="33c0c-160">Messages schema</span></span>  <br/> |
|<span data-ttu-id="33c0c-161">验证文件</span><span class="sxs-lookup"><span data-stu-id="33c0c-161">Validation File</span></span>  <br/> |<span data-ttu-id="33c0c-162">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="33c0c-162">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="33c0c-163">可以为空</span><span class="sxs-lookup"><span data-stu-id="33c0c-163">Can be Empty</span></span>  <br/> |<span data-ttu-id="33c0c-164">False</span><span class="sxs-lookup"><span data-stu-id="33c0c-164">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="33c0c-165">另请参阅</span><span class="sxs-lookup"><span data-stu-id="33c0c-165">See also</span></span>

- [<span data-ttu-id="33c0c-166">GetPasswordExpirationDate 操作</span><span class="sxs-lookup"><span data-stu-id="33c0c-166">GetPasswordExpirationDate operation</span></span>](getpasswordexpirationdate-operation.md)
- [<span data-ttu-id="33c0c-167">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="33c0c-167">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

