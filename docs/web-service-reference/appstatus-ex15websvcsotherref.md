---
title: AppStatus
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f3ab8bf1-abc5-45cf-a2e1-d7602f2c24ec
description: AppStatus 元素的值指示邮件应用程序的状态。
ms.openlocfilehash: cf213fc3d7be02c411e9c2e83a4ff153dbefe098
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753253"
---
# <a name="appstatus"></a><span data-ttu-id="5c787-103">AppStatus</span><span class="sxs-lookup"><span data-stu-id="5c787-103">AppStatus</span></span>

<span data-ttu-id="5c787-104">**AppStatus**元素的值指示邮件应用程序的状态。</span><span class="sxs-lookup"><span data-stu-id="5c787-104">The **AppStatus** element value indicates the status of the mail app.</span></span> 
  
```XML
<AppStatus/>
```

 <span data-ttu-id="5c787-105">**string**</span><span class="sxs-lookup"><span data-stu-id="5c787-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5c787-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5c787-106">Attributes and elements</span></span>

<span data-ttu-id="5c787-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5c787-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5c787-108">属性</span><span class="sxs-lookup"><span data-stu-id="5c787-108">Attributes</span></span>

<span data-ttu-id="5c787-109">无。</span><span class="sxs-lookup"><span data-stu-id="5c787-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5c787-110">子元素</span><span class="sxs-lookup"><span data-stu-id="5c787-110">Child elements</span></span>

<span data-ttu-id="5c787-111">无。</span><span class="sxs-lookup"><span data-stu-id="5c787-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5c787-112">父元素</span><span class="sxs-lookup"><span data-stu-id="5c787-112">Parent elements</span></span>

[<span data-ttu-id="5c787-113">元数据</span><span class="sxs-lookup"><span data-stu-id="5c787-113">Metadata</span></span>](metadata-ex15websvcsotherref.md)
  
## <a name="text-value"></a><span data-ttu-id="5c787-114">文本值</span><span class="sxs-lookup"><span data-stu-id="5c787-114">Text value</span></span>

<span data-ttu-id="5c787-115">**AppStatus**元素的文本值指示邮件应用程序的状态。</span><span class="sxs-lookup"><span data-stu-id="5c787-115">The text value of the **AppStatus** element indicates the status of the mail app.</span></span> <span data-ttu-id="5c787-116">如果用户可以解决的邮件应用程序状态的问题， [ActionUrl](actionurl.md)元素提供了执行该修补程序的 URL。</span><span class="sxs-lookup"><span data-stu-id="5c787-116">If the user can fix an issue related to the status of the mail app, the [ActionUrl](actionurl.md) element provides the URL to perform the fix.</span></span> 
  
<span data-ttu-id="5c787-117">**表 1。AppStatus 值**</span><span class="sxs-lookup"><span data-stu-id="5c787-117">**Table 1. AppStatus values**</span></span>

|<span data-ttu-id="5c787-118">**值**</span><span class="sxs-lookup"><span data-stu-id="5c787-118">**Value**</span></span>|<span data-ttu-id="5c787-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="5c787-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5c787-120">Null 或 0</span><span class="sxs-lookup"><span data-stu-id="5c787-120">Null or 0</span></span>  <br/> |<span data-ttu-id="5c787-121">邮件应用程序具有正常运行状态。</span><span class="sxs-lookup"><span data-stu-id="5c787-121">The mail app has a healthy status.</span></span>  <br/> |
|<span data-ttu-id="5c787-122">1.0</span><span class="sxs-lookup"><span data-stu-id="5c787-122">1.0</span></span>  <br/> |<span data-ttu-id="5c787-123">邮件应用程序可能不会自动更新。</span><span class="sxs-lookup"><span data-stu-id="5c787-123">The mail app could not be automatically updated.</span></span> <span data-ttu-id="5c787-124">邮件应用程序需要能够从 Office 商店重新安装。</span><span class="sxs-lookup"><span data-stu-id="5c787-124">The mail app needs to be re-installed from the Office Store.</span></span>  <br/> |
|<span data-ttu-id="5c787-125">1.1</span><span class="sxs-lookup"><span data-stu-id="5c787-125">1.1</span></span>  <br/> |<span data-ttu-id="5c787-126">邮件应用程序可能不会自动更新。</span><span class="sxs-lookup"><span data-stu-id="5c787-126">The mail app could not be automatically updated.</span></span> <span data-ttu-id="5c787-127">邮件应用程序需要增加的权限，并且这需要您查看和确认安装。</span><span class="sxs-lookup"><span data-stu-id="5c787-127">The mail app requires increased permissions, and this requires your review and confirmation to install.</span></span>  <br/> |
|<span data-ttu-id="5c787-128">1.2</span><span class="sxs-lookup"><span data-stu-id="5c787-128">1.2</span></span>  <br/> |<span data-ttu-id="5c787-129">邮件应用程序无法自动更新。</span><span class="sxs-lookup"><span data-stu-id="5c787-129">The mail app couldn't be updated automatically.</span></span> <span data-ttu-id="5c787-130">当前许可证已到期或无效。</span><span class="sxs-lookup"><span data-stu-id="5c787-130">The current license has expired or is invalid.</span></span> <span data-ttu-id="5c787-131">请更新 Office 商店中的邮件应用程序。</span><span class="sxs-lookup"><span data-stu-id="5c787-131">Please update the mail app from the Office Store.</span></span>  <br/> |
|<span data-ttu-id="5c787-132">2.0</span><span class="sxs-lookup"><span data-stu-id="5c787-132">2.0</span></span>  <br/> |<span data-ttu-id="5c787-133">无法自动更新的邮件应用程序许可证。</span><span class="sxs-lookup"><span data-stu-id="5c787-133">The mail app license could not be automatically updated.</span></span> <span data-ttu-id="5c787-134">邮件应用程序许可证需要从 Office 商店中恢复。</span><span class="sxs-lookup"><span data-stu-id="5c787-134">The license for the mail app needs to be recovered from the Office Store.</span></span>  <br/> |
|<span data-ttu-id="5c787-135">2.1</span><span class="sxs-lookup"><span data-stu-id="5c787-135">2.1</span></span>  <br/> |<span data-ttu-id="5c787-136">无法自动更新的邮件应用程序许可证。</span><span class="sxs-lookup"><span data-stu-id="5c787-136">The mail app license could not be automatically updated.</span></span> <span data-ttu-id="5c787-137">当前许可证已到期。</span><span class="sxs-lookup"><span data-stu-id="5c787-137">The current license has expired.</span></span> <span data-ttu-id="5c787-138">新的许可此应用程序需要从 Office 商店安装。</span><span class="sxs-lookup"><span data-stu-id="5c787-138">A new license for this app needs to be installed from the Office Store.</span></span>  <br/> |
|<span data-ttu-id="5c787-139">3.0</span><span class="sxs-lookup"><span data-stu-id="5c787-139">3.0</span></span>  <br/> |<span data-ttu-id="5c787-140">邮件应用程序的 Office 应用商店状态已更改。</span><span class="sxs-lookup"><span data-stu-id="5c787-140">The Office Store status for the mail app has changed.</span></span> <span data-ttu-id="5c787-141">这可能表示存在问题的邮件应用程序。</span><span class="sxs-lookup"><span data-stu-id="5c787-141">This may indicate that there is a problem with the mail app.</span></span> <span data-ttu-id="5c787-142">转到 Office 商店的详细信息中的邮件应用程序页。</span><span class="sxs-lookup"><span data-stu-id="5c787-142">Go to the mail app page in the Office Store for more information.</span></span>  <br/> |
|<span data-ttu-id="5c787-143">3.1</span><span class="sxs-lookup"><span data-stu-id="5c787-143">3.1</span></span>  <br/> |<span data-ttu-id="5c787-144">从 Office 商店中已被删除的邮件应用程序。</span><span class="sxs-lookup"><span data-stu-id="5c787-144">The mail app has been removed from the Office Store.</span></span>  <br/> |
|<span data-ttu-id="5c787-145">3.2</span><span class="sxs-lookup"><span data-stu-id="5c787-145">3.2</span></span>  <br/> |<span data-ttu-id="5c787-146">使用邮件应用程序已发现的问题和它已经暂时已选撤消从 Office 商店。</span><span class="sxs-lookup"><span data-stu-id="5c787-146">A problem has been discovered with the mail app and it has temporarily been withdrawn from the Office Store.</span></span>  <br/> |
|<span data-ttu-id="5c787-147">3.3</span><span class="sxs-lookup"><span data-stu-id="5c787-147">3.3</span></span>  <br/> |<span data-ttu-id="5c787-148">将删除从 Office 商店 30 天内的邮件应用程序。</span><span class="sxs-lookup"><span data-stu-id="5c787-148">The mail app will be removed from the Office Store within 30 days.</span></span>  <br/> |
|<span data-ttu-id="5c787-149">4.0</span><span class="sxs-lookup"><span data-stu-id="5c787-149">4.0</span></span>  <br/> |<span data-ttu-id="5c787-150">您的邮件客户端已被自动禁用邮件应用程序。</span><span class="sxs-lookup"><span data-stu-id="5c787-150">The mail app has been automatically disabled by your mail client.</span></span>  <br/> |
|<span data-ttu-id="5c787-151">4.1</span><span class="sxs-lookup"><span data-stu-id="5c787-151">4.1</span></span>  <br/> |<span data-ttu-id="5c787-152">出于性能原因的 Outlook 邮件应用程序已禁用。</span><span class="sxs-lookup"><span data-stu-id="5c787-152">The mail app has been disabled by Outlook for performance reasons.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5c787-153">备注</span><span class="sxs-lookup"><span data-stu-id="5c787-153">Remarks</span></span>

<span data-ttu-id="5c787-154">Exchange Server 2013 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="5c787-154">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="5c787-155">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="5c787-155">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5c787-156">元素信息</span><span class="sxs-lookup"><span data-stu-id="5c787-156">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5c787-157">命名空间</span><span class="sxs-lookup"><span data-stu-id="5c787-157">Namespace</span></span>  <br/> | http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5c787-158">架构名称</span><span class="sxs-lookup"><span data-stu-id="5c787-158">Schema Name</span></span>  <br/> |<span data-ttu-id="5c787-159">类型架构</span><span class="sxs-lookup"><span data-stu-id="5c787-159">Types schema</span></span>  <br/> |
|<span data-ttu-id="5c787-160">验证文件</span><span class="sxs-lookup"><span data-stu-id="5c787-160">Validation File</span></span>  <br/> |<span data-ttu-id="5c787-161">不适用</span><span class="sxs-lookup"><span data-stu-id="5c787-161">Not applicable</span></span>  <br/> |
|<span data-ttu-id="5c787-162">可以为空</span><span class="sxs-lookup"><span data-stu-id="5c787-162">Can be Empty</span></span>  <br/> |<span data-ttu-id="5c787-163">False</span><span class="sxs-lookup"><span data-stu-id="5c787-163">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5c787-164">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5c787-164">See also</span></span>

- [<span data-ttu-id="5c787-165">元数据</span><span class="sxs-lookup"><span data-stu-id="5c787-165">Metadata</span></span>](metadata-ex15websvcsotherref.md)
- [<span data-ttu-id="5c787-166">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="5c787-166">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

