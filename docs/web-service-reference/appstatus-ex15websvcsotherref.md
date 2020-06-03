---
title: AppStatus
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f3ab8bf1-abc5-45cf-a2e1-d7602f2c24ec
description: AppStatus 元素值指示邮件应用程序的状态。
ms.openlocfilehash: d833947fd62d500418f257829d241a2e0b3bca9c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464775"
---
# <a name="appstatus"></a><span data-ttu-id="d84da-103">AppStatus</span><span class="sxs-lookup"><span data-stu-id="d84da-103">AppStatus</span></span>

<span data-ttu-id="d84da-104">**AppStatus**元素值指示邮件应用程序的状态。</span><span class="sxs-lookup"><span data-stu-id="d84da-104">The **AppStatus** element value indicates the status of the mail app.</span></span> 
  
```XML
<AppStatus/>
```

 <span data-ttu-id="d84da-105">**string**</span><span class="sxs-lookup"><span data-stu-id="d84da-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d84da-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d84da-106">Attributes and elements</span></span>

<span data-ttu-id="d84da-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d84da-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d84da-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="d84da-108">Attributes</span></span>

<span data-ttu-id="d84da-109">无。</span><span class="sxs-lookup"><span data-stu-id="d84da-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d84da-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d84da-110">Child elements</span></span>

<span data-ttu-id="d84da-111">无。</span><span class="sxs-lookup"><span data-stu-id="d84da-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d84da-112">父元素</span><span class="sxs-lookup"><span data-stu-id="d84da-112">Parent elements</span></span>

[<span data-ttu-id="d84da-113">元数据</span><span class="sxs-lookup"><span data-stu-id="d84da-113">Metadata</span></span>](metadata-ex15websvcsotherref.md)
  
## <a name="text-value"></a><span data-ttu-id="d84da-114">文本值</span><span class="sxs-lookup"><span data-stu-id="d84da-114">Text value</span></span>

<span data-ttu-id="d84da-115">**AppStatus**元素的文本值指示邮件应用程序的状态。</span><span class="sxs-lookup"><span data-stu-id="d84da-115">The text value of the **AppStatus** element indicates the status of the mail app.</span></span> <span data-ttu-id="d84da-116">如果用户可以修复与邮件应用程序状态相关的问题， [ActionUrl](actionurl.md)元素将提供用于执行修补程序的 URL。</span><span class="sxs-lookup"><span data-stu-id="d84da-116">If the user can fix an issue related to the status of the mail app, the [ActionUrl](actionurl.md) element provides the URL to perform the fix.</span></span> 
  
<span data-ttu-id="d84da-117">**表1。AppStatus 值**</span><span class="sxs-lookup"><span data-stu-id="d84da-117">**Table 1. AppStatus values**</span></span>

|<span data-ttu-id="d84da-118">**值**</span><span class="sxs-lookup"><span data-stu-id="d84da-118">**Value**</span></span>|<span data-ttu-id="d84da-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="d84da-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d84da-120">Null 或0</span><span class="sxs-lookup"><span data-stu-id="d84da-120">Null or 0</span></span>  <br/> |<span data-ttu-id="d84da-121">邮件应用程序的状态为 "正常"。</span><span class="sxs-lookup"><span data-stu-id="d84da-121">The mail app has a healthy status.</span></span>  <br/> |
|<span data-ttu-id="d84da-122">1.0</span><span class="sxs-lookup"><span data-stu-id="d84da-122">1.0</span></span>  <br/> |<span data-ttu-id="d84da-123">无法自动更新邮件应用程序。</span><span class="sxs-lookup"><span data-stu-id="d84da-123">The mail app could not be automatically updated.</span></span> <span data-ttu-id="d84da-124">需要从 Office 应用商店重新安装邮件应用程序。</span><span class="sxs-lookup"><span data-stu-id="d84da-124">The mail app needs to be re-installed from the Office Store.</span></span>  <br/> |
|<span data-ttu-id="d84da-125">1.1</span><span class="sxs-lookup"><span data-stu-id="d84da-125">1.1</span></span>  <br/> |<span data-ttu-id="d84da-126">无法自动更新邮件应用程序。</span><span class="sxs-lookup"><span data-stu-id="d84da-126">The mail app could not be automatically updated.</span></span> <span data-ttu-id="d84da-127">邮件应用程序需要增加权限，这需要您的审阅和确认才能安装。</span><span class="sxs-lookup"><span data-stu-id="d84da-127">The mail app requires increased permissions, and this requires your review and confirmation to install.</span></span>  <br/> |
|<span data-ttu-id="d84da-128">1.2</span><span class="sxs-lookup"><span data-stu-id="d84da-128">1.2</span></span>  <br/> |<span data-ttu-id="d84da-129">无法自动更新邮件应用程序。</span><span class="sxs-lookup"><span data-stu-id="d84da-129">The mail app couldn't be updated automatically.</span></span> <span data-ttu-id="d84da-130">当前许可证已过期或无效。</span><span class="sxs-lookup"><span data-stu-id="d84da-130">The current license has expired or is invalid.</span></span> <span data-ttu-id="d84da-131">请从 Office 应用商店更新邮件应用程序。</span><span class="sxs-lookup"><span data-stu-id="d84da-131">Please update the mail app from the Office Store.</span></span>  <br/> |
|<span data-ttu-id="d84da-132">2.0</span><span class="sxs-lookup"><span data-stu-id="d84da-132">2.0</span></span>  <br/> |<span data-ttu-id="d84da-133">无法自动更新邮件应用程序许可证。</span><span class="sxs-lookup"><span data-stu-id="d84da-133">The mail app license could not be automatically updated.</span></span> <span data-ttu-id="d84da-134">需要从 Office 应用商店恢复邮件应用程序的许可证。</span><span class="sxs-lookup"><span data-stu-id="d84da-134">The license for the mail app needs to be recovered from the Office Store.</span></span>  <br/> |
|<span data-ttu-id="d84da-135">2.1</span><span class="sxs-lookup"><span data-stu-id="d84da-135">2.1</span></span>  <br/> |<span data-ttu-id="d84da-136">无法自动更新邮件应用程序许可证。</span><span class="sxs-lookup"><span data-stu-id="d84da-136">The mail app license could not be automatically updated.</span></span> <span data-ttu-id="d84da-137">当前许可证已过期。</span><span class="sxs-lookup"><span data-stu-id="d84da-137">The current license has expired.</span></span> <span data-ttu-id="d84da-138">需要从 Office 应用商店安装此应用程序的新许可证。</span><span class="sxs-lookup"><span data-stu-id="d84da-138">A new license for this app needs to be installed from the Office Store.</span></span>  <br/> |
|<span data-ttu-id="d84da-139">3.0</span><span class="sxs-lookup"><span data-stu-id="d84da-139">3.0</span></span>  <br/> |<span data-ttu-id="d84da-140">邮件应用程序的 Office 应用商店状态已更改。</span><span class="sxs-lookup"><span data-stu-id="d84da-140">The Office Store status for the mail app has changed.</span></span> <span data-ttu-id="d84da-141">这可能表示邮件应用程序出现问题。</span><span class="sxs-lookup"><span data-stu-id="d84da-141">This may indicate that there is a problem with the mail app.</span></span> <span data-ttu-id="d84da-142">有关详细信息，请转到 Office 应用商店中的 "邮件应用程序" 页面。</span><span class="sxs-lookup"><span data-stu-id="d84da-142">Go to the mail app page in the Office Store for more information.</span></span>  <br/> |
|<span data-ttu-id="d84da-143">3.1</span><span class="sxs-lookup"><span data-stu-id="d84da-143">3.1</span></span>  <br/> |<span data-ttu-id="d84da-144">邮件应用程序已从 Office 应用商店中删除。</span><span class="sxs-lookup"><span data-stu-id="d84da-144">The mail app has been removed from the Office Store.</span></span>  <br/> |
|<span data-ttu-id="d84da-145">3.2</span><span class="sxs-lookup"><span data-stu-id="d84da-145">3.2</span></span>  <br/> |<span data-ttu-id="d84da-146">已发现邮件应用程序的问题，并且已从 Office 应用商店中暂时提取了该问题。</span><span class="sxs-lookup"><span data-stu-id="d84da-146">A problem has been discovered with the mail app and it has temporarily been withdrawn from the Office Store.</span></span>  <br/> |
|<span data-ttu-id="d84da-147">3.3</span><span class="sxs-lookup"><span data-stu-id="d84da-147">3.3</span></span>  <br/> |<span data-ttu-id="d84da-148">将在30天内从 Office 应用商店中删除邮件应用程序。</span><span class="sxs-lookup"><span data-stu-id="d84da-148">The mail app will be removed from the Office Store within 30 days.</span></span>  <br/> |
|<span data-ttu-id="d84da-149">4.0</span><span class="sxs-lookup"><span data-stu-id="d84da-149">4.0</span></span>  <br/> |<span data-ttu-id="d84da-150">邮件客户端已自动禁用邮件应用程序。</span><span class="sxs-lookup"><span data-stu-id="d84da-150">The mail app has been automatically disabled by your mail client.</span></span>  <br/> |
|<span data-ttu-id="d84da-151">4.1</span><span class="sxs-lookup"><span data-stu-id="d84da-151">4.1</span></span>  <br/> |<span data-ttu-id="d84da-152">由于性能原因，Outlook 禁用了邮件应用程序。</span><span class="sxs-lookup"><span data-stu-id="d84da-152">The mail app has been disabled by Outlook for performance reasons.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d84da-153">说明</span><span class="sxs-lookup"><span data-stu-id="d84da-153">Remarks</span></span>

<span data-ttu-id="d84da-154">Exchange Server 2013 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="d84da-154">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="d84da-155">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d84da-155">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d84da-156">元素信息</span><span class="sxs-lookup"><span data-stu-id="d84da-156">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d84da-157">命名空间</span><span class="sxs-lookup"><span data-stu-id="d84da-157">Namespace</span></span>  <br/> | https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d84da-158">架构名称</span><span class="sxs-lookup"><span data-stu-id="d84da-158">Schema Name</span></span>  <br/> |<span data-ttu-id="d84da-159">类型架构</span><span class="sxs-lookup"><span data-stu-id="d84da-159">Types schema</span></span>  <br/> |
|<span data-ttu-id="d84da-160">验证文件</span><span class="sxs-lookup"><span data-stu-id="d84da-160">Validation File</span></span>  <br/> |<span data-ttu-id="d84da-161">不适用</span><span class="sxs-lookup"><span data-stu-id="d84da-161">Not applicable</span></span>  <br/> |
|<span data-ttu-id="d84da-162">可以为空</span><span class="sxs-lookup"><span data-stu-id="d84da-162">Can be Empty</span></span>  <br/> |<span data-ttu-id="d84da-163">False</span><span class="sxs-lookup"><span data-stu-id="d84da-163">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d84da-164">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d84da-164">See also</span></span>

- [<span data-ttu-id="d84da-165">元数据</span><span class="sxs-lookup"><span data-stu-id="d84da-165">Metadata</span></span>](metadata-ex15websvcsotherref.md)
- [<span data-ttu-id="d84da-166">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d84da-166">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

