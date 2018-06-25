---
title: SourceIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SourceIds
api_type:
- schema
ms.assetid: 0043abd5-ba9c-4d67-8832-325f32bf7651
description: SourceIds 元素包含要转换的源标识符。
ms.openlocfilehash: c9ee9fd01367f714e1cb3770e2be5161cb45d98f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827522"
---
# <a name="sourceids"></a><span data-ttu-id="da60c-103">SourceIds</span><span class="sxs-lookup"><span data-stu-id="da60c-103">SourceIds</span></span>

<span data-ttu-id="da60c-104">**SourceIds**元素包含要转换的源标识符。</span><span class="sxs-lookup"><span data-stu-id="da60c-104">The **SourceIds** element contains the source identifiers to convert.</span></span> 
  
[<span data-ttu-id="da60c-105">ConvertId</span><span class="sxs-lookup"><span data-stu-id="da60c-105">ConvertId</span></span>](convertid.md)
  
[<span data-ttu-id="da60c-106">SourceIds</span><span class="sxs-lookup"><span data-stu-id="da60c-106">SourceIds</span></span>](sourceids.md)
  
```xml
<SourceIds>
   <AlternateId/>
   <AlternatePublicFolderId/>
   <AlternatePublicFolderItemId/>
</SourceIds>
```

 <span data-ttu-id="da60c-107">**NonEmptyArrayOfAlternateIdsType**</span><span class="sxs-lookup"><span data-stu-id="da60c-107">**NonEmptyArrayOfAlternateIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="da60c-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="da60c-108">Attributes and elements</span></span>

<span data-ttu-id="da60c-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="da60c-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="da60c-110">属性</span><span class="sxs-lookup"><span data-stu-id="da60c-110">Attributes</span></span>

<span data-ttu-id="da60c-111">无。</span><span class="sxs-lookup"><span data-stu-id="da60c-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="da60c-112">子元素</span><span class="sxs-lookup"><span data-stu-id="da60c-112">Child elements</span></span>

|<span data-ttu-id="da60c-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="da60c-113">**Element**</span></span>|<span data-ttu-id="da60c-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="da60c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="da60c-115">AlternateId</span><span class="sxs-lookup"><span data-stu-id="da60c-115">AlternateId</span></span>](alternateid.md) <br/> |<span data-ttu-id="da60c-116">描述要转换的项目或文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="da60c-116">Describes an item or folder identifier to convert.</span></span>  <br/> |
|[<span data-ttu-id="da60c-117">AlternatePublicFolderId</span><span class="sxs-lookup"><span data-stu-id="da60c-117">AlternatePublicFolderId</span></span>](alternatepublicfolderid.md) <br/> |<span data-ttu-id="da60c-118">描述要转换的公用文件夹标识符。</span><span class="sxs-lookup"><span data-stu-id="da60c-118">Describes a public folder identifier to convert.</span></span>  <br/> |
|[<span data-ttu-id="da60c-119">AlternatePublicFolderItemId</span><span class="sxs-lookup"><span data-stu-id="da60c-119">AlternatePublicFolderItemId</span></span>](alternatepublicfolderitemid.md) <br/> |<span data-ttu-id="da60c-120">描述要转换的公用文件夹项标识符。</span><span class="sxs-lookup"><span data-stu-id="da60c-120">Describes a public folder item identifier to convert.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="da60c-121">父元素</span><span class="sxs-lookup"><span data-stu-id="da60c-121">Parent elements</span></span>

|<span data-ttu-id="da60c-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="da60c-122">**Element**</span></span>|<span data-ttu-id="da60c-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="da60c-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="da60c-124">ConvertId</span><span class="sxs-lookup"><span data-stu-id="da60c-124">ConvertId</span></span>](convertid.md) <br/> |<span data-ttu-id="da60c-125">定义转换 Exchange 支持格式之间的项目和文件夹标识符的请求。</span><span class="sxs-lookup"><span data-stu-id="da60c-125">Defines a request to convert item and folder identifiers between Exchange supported formats.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="da60c-126">注解</span><span class="sxs-lookup"><span data-stu-id="da60c-126">Remarks</span></span>

<span data-ttu-id="da60c-127">描述此元素的架构位于运行 Exchange Server 已安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="da60c-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="da60c-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="da60c-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="da60c-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="da60c-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="da60c-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="da60c-130">Schema Name</span></span>  <br/> |<span data-ttu-id="da60c-131">消息架构</span><span class="sxs-lookup"><span data-stu-id="da60c-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="da60c-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="da60c-132">Validation File</span></span>  <br/> |<span data-ttu-id="da60c-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="da60c-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="da60c-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="da60c-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="da60c-135">False</span><span class="sxs-lookup"><span data-stu-id="da60c-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="da60c-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="da60c-136">See also</span></span>



[<span data-ttu-id="da60c-137">ConvertId 操作</span><span class="sxs-lookup"><span data-stu-id="da60c-137">ConvertId operation</span></span>](convertid-operation.md)


- [<span data-ttu-id="da60c-138">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="da60c-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="da60c-139">转换标识符</span><span class="sxs-lookup"><span data-stu-id="da60c-139">Converting Identifiers</span></span>](http://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

