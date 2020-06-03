---
title: GetPasswordExpirationDateResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3d3fff1f-ef13-46d5-bd7f-ef535eb80c72
description: GetPasswordExpirationDateResponse 元素定义对 GetPasswordExpirationDate 操作操作请求的响应。
ms.openlocfilehash: c925b2b37879ba0f8f25b2dd73737ed2f3202555
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530202"
---
# <a name="getpasswordexpirationdateresponse"></a><span data-ttu-id="79efb-103">GetPasswordExpirationDateResponse</span><span class="sxs-lookup"><span data-stu-id="79efb-103">GetPasswordExpirationDateResponse</span></span>

<span data-ttu-id="79efb-104">**GetPasswordExpirationDateResponse**元素定义对[GetPasswordExpirationDate 操作](getpasswordexpirationdate-operation.md)操作请求的响应。</span><span class="sxs-lookup"><span data-stu-id="79efb-104">The **GetPasswordExpirationDateResponse** element defines the response to a [GetPasswordExpirationDate operation](getpasswordexpirationdate-operation.md) operation request.</span></span> 
  
- [<span data-ttu-id="79efb-105">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="79efb-105">ResponseMessages</span></span>](responsemessages.md)
- [<span data-ttu-id="79efb-106">GetPasswordExpirationDateResponse</span><span class="sxs-lookup"><span data-stu-id="79efb-106">GetPasswordExpirationDateResponse</span></span>](getpasswordexpirationdateresponse.md)
  
```XML
<GetPasswordExpirationDateResponse>
    <PasswordExpirationDate />
</GetPasswordExpirationDateResponse>
```

 <span data-ttu-id="79efb-107">**GetPasswordExpirationDateResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="79efb-107">**GetPasswordExpirationDateResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="79efb-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="79efb-108">Attributes and elements</span></span>

<span data-ttu-id="79efb-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="79efb-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="79efb-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="79efb-110">Attributes</span></span>

|<span data-ttu-id="79efb-111">**属性**</span><span class="sxs-lookup"><span data-stu-id="79efb-111">**Attribute**</span></span>|<span data-ttu-id="79efb-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="79efb-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="79efb-113">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="79efb-113">**ResponseClass**</span></span> <br/> | <span data-ttu-id="79efb-114">描述响应的状态。</span><span class="sxs-lookup"><span data-stu-id="79efb-114">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="79efb-115">以下值对此属性有效：</span><span class="sxs-lookup"><span data-stu-id="79efb-115">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="79efb-116">-成功</span><span class="sxs-lookup"><span data-stu-id="79efb-116">-  Success</span></span>  <br/><span data-ttu-id="79efb-117">-警告</span><span class="sxs-lookup"><span data-stu-id="79efb-117">-  Warning</span></span>  <br/><span data-ttu-id="79efb-118">-错误</span><span class="sxs-lookup"><span data-stu-id="79efb-118">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="79efb-119">ResponseClass 属性值</span><span class="sxs-lookup"><span data-stu-id="79efb-119">ResponseClass attribute values</span></span>

|<span data-ttu-id="79efb-120">**值**</span><span class="sxs-lookup"><span data-stu-id="79efb-120">**Value**</span></span>|<span data-ttu-id="79efb-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="79efb-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="79efb-122">**Success**</span><span class="sxs-lookup"><span data-stu-id="79efb-122">**Success**</span></span> <br/> |<span data-ttu-id="79efb-123">描述已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="79efb-123">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="79efb-124">**警告**</span><span class="sxs-lookup"><span data-stu-id="79efb-124">**Warning**</span></span> <br/> | <span data-ttu-id="79efb-125">介绍未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="79efb-125">Describes a request that was not processed.</span></span> <span data-ttu-id="79efb-126">如果在处理请求中的项目时出现错误，并且无法处理后续项目，则可能会返回一个警告。</span><span class="sxs-lookup"><span data-stu-id="79efb-126">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="79efb-127">以下是警告源的示例：</span><span class="sxs-lookup"><span data-stu-id="79efb-127">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="79efb-128">-Exchange 存储在批处理过程中处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="79efb-128">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="79efb-129">-Active Directory 域服务（AD DS）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="79efb-129">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="79efb-130">-邮箱已移动。</span><span class="sxs-lookup"><span data-stu-id="79efb-130">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="79efb-131">-邮件数据库（MDB）处于脱机状态。</span><span class="sxs-lookup"><span data-stu-id="79efb-131">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="79efb-132">-密码已过期。</span><span class="sxs-lookup"><span data-stu-id="79efb-132">-  A password is expired.</span></span>  <br/><span data-ttu-id="79efb-133">-已超出配额。</span><span class="sxs-lookup"><span data-stu-id="79efb-133">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="79efb-134">**Error**</span><span class="sxs-lookup"><span data-stu-id="79efb-134">**Error**</span></span> <br/> | <span data-ttu-id="79efb-135">介绍无法满足的请求。</span><span class="sxs-lookup"><span data-stu-id="79efb-135">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="79efb-136">以下是错误源的示例：</span><span class="sxs-lookup"><span data-stu-id="79efb-136">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="79efb-137">-属性或元素无效。</span><span class="sxs-lookup"><span data-stu-id="79efb-137">-  Invalid attributes or elements.</span></span>  <br/><span data-ttu-id="79efb-138">-超出范围的属性或元素。</span><span class="sxs-lookup"><span data-stu-id="79efb-138">-  Attributes or elements that are out of range.</span></span>  <br/><span data-ttu-id="79efb-139">-未知标记。</span><span class="sxs-lookup"><span data-stu-id="79efb-139">-  An unknown tag.</span></span>  <br/><span data-ttu-id="79efb-140">-上下文中无效的属性或元素。</span><span class="sxs-lookup"><span data-stu-id="79efb-140">-  An attribute or element that is not valid in the context.</span></span>  <br/><span data-ttu-id="79efb-141">-任何客户端进行未经授权的访问尝试。</span><span class="sxs-lookup"><span data-stu-id="79efb-141">-  An unauthorized access attempt by any client.</span></span>  <br/><span data-ttu-id="79efb-142">-响应有效客户端调用的服务器端故障。</span><span class="sxs-lookup"><span data-stu-id="79efb-142">-  A server-side failure in response to a valid client-side call.</span></span>  <br/><br/>  <span data-ttu-id="79efb-143">有关错误的信息可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中找到。</span><span class="sxs-lookup"><span data-stu-id="79efb-143">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="79efb-144">子元素</span><span class="sxs-lookup"><span data-stu-id="79efb-144">Child elements</span></span>

|<span data-ttu-id="79efb-145">**元素名**</span><span class="sxs-lookup"><span data-stu-id="79efb-145">**Element name**</span></span>|<span data-ttu-id="79efb-146">**说明**</span><span class="sxs-lookup"><span data-stu-id="79efb-146">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="79efb-147">PasswordExpirationDate</span><span class="sxs-lookup"><span data-stu-id="79efb-147">PasswordExpirationDate</span></span>](passwordexpirationdate.md) <br/> |<span data-ttu-id="79efb-148">为请求中指定的电子邮件帐户提供密码到期日期。</span><span class="sxs-lookup"><span data-stu-id="79efb-148">Provides the password expiration date for the email account specified in the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="79efb-149">父元素</span><span class="sxs-lookup"><span data-stu-id="79efb-149">Parent elements</span></span>

|<span data-ttu-id="79efb-150">**元素名**</span><span class="sxs-lookup"><span data-stu-id="79efb-150">**Element name**</span></span>|<span data-ttu-id="79efb-151">**说明**</span><span class="sxs-lookup"><span data-stu-id="79efb-151">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="79efb-152">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="79efb-152">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="79efb-153">包含 Exchange Web 服务（EWS）请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="79efb-153">Contains the response messages for an Exchange Web Services (EWS) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="79efb-154">说明</span><span class="sxs-lookup"><span data-stu-id="79efb-154">Remarks</span></span>

<span data-ttu-id="79efb-155">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="79efb-155">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="79efb-156">Exchange Server 2010 Service Pack 2 (SP2) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="79efb-156">This element was introduced in Exchange Server 2010 Service Pack 2 (SP2).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="79efb-157">元素信息</span><span class="sxs-lookup"><span data-stu-id="79efb-157">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="79efb-158">命名空间</span><span class="sxs-lookup"><span data-stu-id="79efb-158">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="79efb-159">架构名称</span><span class="sxs-lookup"><span data-stu-id="79efb-159">Schema Name</span></span>  <br/> |<span data-ttu-id="79efb-160">消息架构</span><span class="sxs-lookup"><span data-stu-id="79efb-160">Messages schema</span></span>  <br/> |
|<span data-ttu-id="79efb-161">验证文件</span><span class="sxs-lookup"><span data-stu-id="79efb-161">Validation File</span></span>  <br/> |<span data-ttu-id="79efb-162">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="79efb-162">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="79efb-163">可以为空</span><span class="sxs-lookup"><span data-stu-id="79efb-163">Can be Empty</span></span>  <br/> |<span data-ttu-id="79efb-164">False</span><span class="sxs-lookup"><span data-stu-id="79efb-164">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="79efb-165">另请参阅</span><span class="sxs-lookup"><span data-stu-id="79efb-165">See also</span></span>

- [<span data-ttu-id="79efb-166">GetPasswordExpirationDate 操作</span><span class="sxs-lookup"><span data-stu-id="79efb-166">GetPasswordExpirationDate operation</span></span>](getpasswordexpirationdate-operation.md)
- [<span data-ttu-id="79efb-167">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="79efb-167">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

