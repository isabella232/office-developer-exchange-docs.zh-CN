---
title: DeleteItemResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteItemResponseMessage
api_type:
- schema
ms.assetid: c3d34c4d-8d83-4612-aa9e-66f9cc7314df
description: DeleteItemResponseMessage 元素包含状态和单个删除项操作请求的结果。
ms.openlocfilehash: 1f0cc3d49bfa5fba6da32cf65df6b6718ccfbded
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753823"
---
# <a name="deleteitemresponsemessage"></a><span data-ttu-id="5a63b-103">DeleteItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="5a63b-103">DeleteItemResponseMessage</span></span>

<span data-ttu-id="5a63b-104">**DeleteItemResponseMessage**元素包含的状态和结果的一个[删除项操作](deleteitem-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="5a63b-104">The **DeleteItemResponseMessage** element contains the status and result of a single [DeleteItem operation](deleteitem-operation.md) request.</span></span> 
  
- [<span data-ttu-id="5a63b-105">DeleteItemResponse</span><span class="sxs-lookup"><span data-stu-id="5a63b-105">DeleteItemResponse</span></span>](deleteitemresponse.md) 
- [<span data-ttu-id="5a63b-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="5a63b-106">ResponseMessages</span></span>](responsemessages.md)  
- [<span data-ttu-id="5a63b-107">DeleteItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="5a63b-107">DeleteItemResponseMessage</span></span>](deleteitemresponsemessage.md)
  
```xml
<DeleteItemResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</DeleteItemResponseMessage>
```

 <span data-ttu-id="5a63b-108">**DeleteItemResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="5a63b-108">**DeleteItemResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5a63b-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5a63b-109">Attributes and elements</span></span>

<span data-ttu-id="5a63b-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5a63b-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5a63b-111">属性</span><span class="sxs-lookup"><span data-stu-id="5a63b-111">Attributes</span></span>

|<span data-ttu-id="5a63b-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="5a63b-112">**Attribute**</span></span>|<span data-ttu-id="5a63b-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="5a63b-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5a63b-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="5a63b-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="5a63b-115">介绍了在[删除项操作](deleteitem-operation.md)的响应的状态。</span><span class="sxs-lookup"><span data-stu-id="5a63b-115">Describes the status of a [DeleteItem operation](deleteitem-operation.md) response.</span></span><br/><br/><span data-ttu-id="5a63b-116">下面是此属性有效值：</span><span class="sxs-lookup"><span data-stu-id="5a63b-116">The following values are valid for this attribute:</span></span><br/><br/><span data-ttu-id="5a63b-117">-成功</span><span class="sxs-lookup"><span data-stu-id="5a63b-117">- Success</span></span>  <br/><span data-ttu-id="5a63b-118">-警告</span><span class="sxs-lookup"><span data-stu-id="5a63b-118">-  Warning</span></span>  <br/><span data-ttu-id="5a63b-119">-错误</span><span class="sxs-lookup"><span data-stu-id="5a63b-119">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute"></a><span data-ttu-id="5a63b-120">ResponseClass 属性</span><span class="sxs-lookup"><span data-stu-id="5a63b-120">ResponseClass attribute</span></span>

|<span data-ttu-id="5a63b-121">**值**</span><span class="sxs-lookup"><span data-stu-id="5a63b-121">**Value**</span></span>|<span data-ttu-id="5a63b-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="5a63b-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5a63b-123">**成功**</span><span class="sxs-lookup"><span data-stu-id="5a63b-123">**Success**</span></span> <br/> |<span data-ttu-id="5a63b-124">介绍的已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="5a63b-124">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="5a63b-125">**Warning**</span><span class="sxs-lookup"><span data-stu-id="5a63b-125">**Warning**</span></span> <br/> | <span data-ttu-id="5a63b-126">介绍了未处理的请求。</span><span class="sxs-lookup"><span data-stu-id="5a63b-126">Describes a request that was not processed.</span></span> <span data-ttu-id="5a63b-127">如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。</span><span class="sxs-lookup"><span data-stu-id="5a63b-127">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/><span data-ttu-id="5a63b-128">以下是源的警告的示例：</span><span class="sxs-lookup"><span data-stu-id="5a63b-128">The following are examples of sources of warnings:</span></span><br/><br/><span data-ttu-id="5a63b-129">在批处理期间脱机-Exchange 存储。</span><span class="sxs-lookup"><span data-stu-id="5a63b-129">-  The Exchange store goes offline during the batch.</span></span>  <br/><span data-ttu-id="5a63b-130">-Active Directory 域服务 (AD DS) 将脱机。</span><span class="sxs-lookup"><span data-stu-id="5a63b-130">-  Active Directory Domain Services (AD DS) goes offline.</span></span>  <br/><span data-ttu-id="5a63b-131">的移动邮箱。</span><span class="sxs-lookup"><span data-stu-id="5a63b-131">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="5a63b-132">(MDB)-邮件数据库脱机。</span><span class="sxs-lookup"><span data-stu-id="5a63b-132">-  The message database (MDB) goes offline.</span></span>  <br/><span data-ttu-id="5a63b-133">的已过期密码。</span><span class="sxs-lookup"><span data-stu-id="5a63b-133">-  A password is expired.</span></span>  <br/><span data-ttu-id="5a63b-134">超出了-配额。</span><span class="sxs-lookup"><span data-stu-id="5a63b-134">-  A quota is exceeded.</span></span>  <br/> |
|<span data-ttu-id="5a63b-135">**Error**</span><span class="sxs-lookup"><span data-stu-id="5a63b-135">**Error**</span></span> <br/> | <span data-ttu-id="5a63b-136">描述无法满足请求。</span><span class="sxs-lookup"><span data-stu-id="5a63b-136">Describes a request that cannot be fulfilled.</span></span><br/><br/><span data-ttu-id="5a63b-137">错误的来源的示例如下：</span><span class="sxs-lookup"><span data-stu-id="5a63b-137">The following are examples of sources of errors:</span></span><br/><br/><span data-ttu-id="5a63b-138">-无效属性或元素</span><span class="sxs-lookup"><span data-stu-id="5a63b-138">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="5a63b-139">-属性或超出范围的元素</span><span class="sxs-lookup"><span data-stu-id="5a63b-139">-  Attributes or elements out of range</span></span>  <br/><span data-ttu-id="5a63b-140">-未知标记</span><span class="sxs-lookup"><span data-stu-id="5a63b-140">-  Unknown tag</span></span>  <br/><span data-ttu-id="5a63b-141">-属性或元素在上下文中无效</span><span class="sxs-lookup"><span data-stu-id="5a63b-141">-  Attribute or element not valid in the context</span></span>  <br/><span data-ttu-id="5a63b-142">-客户端尝试上方由管理员允许的最大级别设置的错误日志记录级别</span><span class="sxs-lookup"><span data-stu-id="5a63b-142">-  A client attempt to set the error logging level above the maximum level that is permitted by the administrator</span></span>  <br/><span data-ttu-id="5a63b-143">-客户端尝试设置为低于默认级别的管理员指定的严重故障级别</span><span class="sxs-lookup"><span data-stu-id="5a63b-143">-  A client attempt to set the severity failure level below the default level that is specified by the administrator</span></span>  <br/><span data-ttu-id="5a63b-144">-未授权访问尝试的任何客户端</span><span class="sxs-lookup"><span data-stu-id="5a63b-144">-  Unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="5a63b-145">的有效的客户端的呼叫的响应中服务器端失败</span><span class="sxs-lookup"><span data-stu-id="5a63b-145">-  Server-side failure in response to a valid client-side call</span></span><br/><br/>  <span data-ttu-id="5a63b-146">[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素中，可以找到有关错误的信息。</span><span class="sxs-lookup"><span data-stu-id="5a63b-146">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5a63b-147">子元素</span><span class="sxs-lookup"><span data-stu-id="5a63b-147">Child elements</span></span>

|<span data-ttu-id="5a63b-148">**元素**</span><span class="sxs-lookup"><span data-stu-id="5a63b-148">**Element**</span></span>|<span data-ttu-id="5a63b-149">**说明**</span><span class="sxs-lookup"><span data-stu-id="5a63b-149">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5a63b-150">MessageText</span><span class="sxs-lookup"><span data-stu-id="5a63b-150">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="5a63b-151">提供的响应状态的文本说明。</span><span class="sxs-lookup"><span data-stu-id="5a63b-151">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="5a63b-152">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="5a63b-152">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="5a63b-153">提供标识的特定错误的请求时遇到的错误代码。</span><span class="sxs-lookup"><span data-stu-id="5a63b-153">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="5a63b-154">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="5a63b-154">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="5a63b-155">当前未使用，供将来使用。</span><span class="sxs-lookup"><span data-stu-id="5a63b-155">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="5a63b-156">它包含的值为 0。</span><span class="sxs-lookup"><span data-stu-id="5a63b-156">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="5a63b-157">MessageXml</span><span class="sxs-lookup"><span data-stu-id="5a63b-157">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="5a63b-158">提供了其他错误响应信息。</span><span class="sxs-lookup"><span data-stu-id="5a63b-158">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5a63b-159">父元素</span><span class="sxs-lookup"><span data-stu-id="5a63b-159">Parent elements</span></span>

|<span data-ttu-id="5a63b-160">**元素**</span><span class="sxs-lookup"><span data-stu-id="5a63b-160">**Element**</span></span>|<span data-ttu-id="5a63b-161">**说明**</span><span class="sxs-lookup"><span data-stu-id="5a63b-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5a63b-162">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="5a63b-162">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="5a63b-163">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="5a63b-163">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5a63b-164">注解</span><span class="sxs-lookup"><span data-stu-id="5a63b-164">Remarks</span></span>

<span data-ttu-id="5a63b-165">描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="5a63b-165">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="5a63b-166">版本差异</span><span class="sxs-lookup"><span data-stu-id="5a63b-166">Version differences</span></span>

<span data-ttu-id="5a63b-167">在版本的 Exchange 开头生成 15.00.0986.00， **DeleteItemResponseMessage**元素是类型**DeleteItemResponseMessageType**。</span><span class="sxs-lookup"><span data-stu-id="5a63b-167">In versions of Exchange starting with build 15.00.0986.00, the **DeleteItemResponseMessage** element is of type **DeleteItemResponseMessageType**.</span></span> <span data-ttu-id="5a63b-168">在早期版本，该元素是类型**ResponseMessageType**。</span><span class="sxs-lookup"><span data-stu-id="5a63b-168">In previous versions, the element is of type **ResponseMessageType**.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5a63b-169">元素信息</span><span class="sxs-lookup"><span data-stu-id="5a63b-169">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5a63b-170">命名空间</span><span class="sxs-lookup"><span data-stu-id="5a63b-170">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5a63b-171">架构名称</span><span class="sxs-lookup"><span data-stu-id="5a63b-171">Schema Name</span></span>  <br/> |<span data-ttu-id="5a63b-172">消息架构</span><span class="sxs-lookup"><span data-stu-id="5a63b-172">Messages schema</span></span>  <br/> |
|<span data-ttu-id="5a63b-173">验证文件</span><span class="sxs-lookup"><span data-stu-id="5a63b-173">Validation File</span></span>  <br/> |<span data-ttu-id="5a63b-174">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="5a63b-174">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5a63b-175">可以为空</span><span class="sxs-lookup"><span data-stu-id="5a63b-175">Can be Empty</span></span>  <br/> |<span data-ttu-id="5a63b-176">False</span><span class="sxs-lookup"><span data-stu-id="5a63b-176">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5a63b-177">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5a63b-177">See also</span></span>

- [<span data-ttu-id="5a63b-178">删除项操作</span><span class="sxs-lookup"><span data-stu-id="5a63b-178">DeleteItem operation</span></span>](deleteitem-operation.md)
- [<span data-ttu-id="5a63b-179">Exchange 的 EWS 引用</span><span class="sxs-lookup"><span data-stu-id="5a63b-179">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)
- [<span data-ttu-id="5a63b-180">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="5a63b-180">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="5a63b-181">删除项 （Exchange Web 服务）</span><span class="sxs-lookup"><span data-stu-id="5a63b-181">Deleting Items (Exchange Web Services)</span></span>](http://msdn.microsoft.com/library/9bfc39e6-d944-4eb6-8aee-cbaf1e37c67d%28Office.15%29.aspx)

