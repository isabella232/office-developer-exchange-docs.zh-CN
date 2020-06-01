---
title: HasQuota
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HasQuota
api_type:
- schema
ms.assetid: b6e4fef0-92a9-415f-81ae-0c5ecb7c12ad
description: HasQuota 元素指示托管文件夹是否具有配额。
ms.openlocfilehash: 6e32aa4c69943774be928339936cca5016c58d85
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462750"
---
# <a name="hasquota"></a><span data-ttu-id="8d72f-103">HasQuota</span><span class="sxs-lookup"><span data-stu-id="8d72f-103">HasQuota</span></span>

<span data-ttu-id="8d72f-104">**HasQuota**元素指示托管文件夹是否具有配额。</span><span class="sxs-lookup"><span data-stu-id="8d72f-104">The **HasQuota** element indicates whether the managed folder has a quota.</span></span> 
  
```xml
<HasQuota/>
```

 <span data-ttu-id="8d72f-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="8d72f-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8d72f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8d72f-106">Attributes and elements</span></span>

<span data-ttu-id="8d72f-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8d72f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8d72f-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="8d72f-108">Attributes</span></span>

<span data-ttu-id="8d72f-109">无。</span><span class="sxs-lookup"><span data-stu-id="8d72f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8d72f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="8d72f-110">Child elements</span></span>

<span data-ttu-id="8d72f-111">无。</span><span class="sxs-lookup"><span data-stu-id="8d72f-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8d72f-112">父元素</span><span class="sxs-lookup"><span data-stu-id="8d72f-112">Parent elements</span></span>

|<span data-ttu-id="8d72f-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="8d72f-113">**Element**</span></span>|<span data-ttu-id="8d72f-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="8d72f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8d72f-115">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="8d72f-115">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="8d72f-116">包含有关托管文件夹的信息。</span><span class="sxs-lookup"><span data-stu-id="8d72f-116">Contains information about a managed folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8d72f-117">文本值</span><span class="sxs-lookup"><span data-stu-id="8d72f-117">Text value</span></span>

<span data-ttu-id="8d72f-118">该文本值表示一个布尔值。</span><span class="sxs-lookup"><span data-stu-id="8d72f-118">The text value represents a Boolean value.</span></span> <span data-ttu-id="8d72f-119">**如果值为 true** ，则表示文件夹具有配额;**如果值为 false** ，则表示文件夹没有配额。</span><span class="sxs-lookup"><span data-stu-id="8d72f-119">A value of **true** indicates that the folder has a quota; a value of **false** indicates that the folder does not have a quota.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8d72f-120">说明</span><span class="sxs-lookup"><span data-stu-id="8d72f-120">Remarks</span></span>

<span data-ttu-id="8d72f-121">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8d72f-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8d72f-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="8d72f-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8d72f-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="8d72f-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8d72f-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="8d72f-124">Schema name</span></span>  <br/> |<span data-ttu-id="8d72f-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="8d72f-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="8d72f-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="8d72f-126">Validation file</span></span>  <br/> |<span data-ttu-id="8d72f-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8d72f-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8d72f-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="8d72f-128">Can be empty</span></span>  <br/> |<span data-ttu-id="8d72f-129">False</span><span class="sxs-lookup"><span data-stu-id="8d72f-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8d72f-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8d72f-130">See also</span></span>



- [<span data-ttu-id="8d72f-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="8d72f-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

