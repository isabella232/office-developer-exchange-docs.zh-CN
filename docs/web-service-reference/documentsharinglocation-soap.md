---
title: DocumentSharingLocation (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21bc388c-33be-422b-a89d-30ade0fae8f1
description: DocumentSharingLocation 元素包含位置和文档共享位置的元数据信息。
ms.openlocfilehash: d258efecb46d570138c7c2c78ed9d2fa9a275103
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753966"
---
# <a name="documentsharinglocation-soap"></a><span data-ttu-id="6b047-103">DocumentSharingLocation (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6b047-103">DocumentSharingLocation (SOAP)</span></span>

<span data-ttu-id="6b047-104">**DocumentSharingLocation**元素包含位置和文档共享位置的元数据信息。</span><span class="sxs-lookup"><span data-stu-id="6b047-104">The **DocumentSharingLocation** element contains location and metadata information for a document sharing location.</span></span> 
  
```XML
<DocumentSharingLocation>
   <ServiceUrl />
   <LocationUrl />
   <DisplayName />
   <SupportedFileExtensions />
   <ExternalAccessAllowed />
   <AnonymousAccessAllowed />
   <CanModifyPermissions />
   <IsDefault />
</DocumentSharingLocation>
```

 <span data-ttu-id="6b047-105">**DocumentSharingLocation**</span><span class="sxs-lookup"><span data-stu-id="6b047-105">**DocumentSharingLocation**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6b047-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6b047-106">Attributes and elements</span></span>

<span data-ttu-id="6b047-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6b047-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6b047-108">属性</span><span class="sxs-lookup"><span data-stu-id="6b047-108">Attributes</span></span>

<span data-ttu-id="6b047-109">无。</span><span class="sxs-lookup"><span data-stu-id="6b047-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6b047-110">子元素</span><span class="sxs-lookup"><span data-stu-id="6b047-110">Child elements</span></span>

|<span data-ttu-id="6b047-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="6b047-111">**Element**</span></span>|<span data-ttu-id="6b047-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="6b047-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6b047-113">ServiceUrl (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6b047-113">ServiceUrl (SOAP)</span></span>](serviceurl-soap.md) <br/> |<span data-ttu-id="6b047-114">代表共享 web 服务的文档的 URL。</span><span class="sxs-lookup"><span data-stu-id="6b047-114">Represents the URL of the document sharing web service.</span></span>  <br/> |
|[<span data-ttu-id="6b047-115">LocationUrl (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6b047-115">LocationUrl (SOAP)</span></span>](locationurl-soap.md) <br/> |<span data-ttu-id="6b047-116">代表共享位置的文档的 URL。</span><span class="sxs-lookup"><span data-stu-id="6b047-116">Represents the URL of the document sharing location.</span></span>  <br/> |
|[<span data-ttu-id="6b047-117">DisplayName (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6b047-117">DisplayName (SOAP)</span></span>](displayname-soap.md) <br/> |<span data-ttu-id="6b047-118">代表共享位置，用于在 UI 中的文档的名称。</span><span class="sxs-lookup"><span data-stu-id="6b047-118">Represents the name of the document sharing location to use in the UI.</span></span>  <br/> |
|[<span data-ttu-id="6b047-119">SupportedFileExtensions (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6b047-119">SupportedFileExtensions (SOAP)</span></span>](supportedfileextensions-soap.md) <br/> |<span data-ttu-id="6b047-120">表示可以共享位置在文档中存储的文件扩展名。</span><span class="sxs-lookup"><span data-stu-id="6b047-120">Represents the file extensions that can be stored in the document sharing location.</span></span>  <br/> |
|[<span data-ttu-id="6b047-121">ExternalAccessAllowed (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6b047-121">ExternalAccessAllowed (SOAP)</span></span>](externalaccessallowed-soap.md) <br/> |<span data-ttu-id="6b047-122">指示是否可用于外部连接共享位置的文档。</span><span class="sxs-lookup"><span data-stu-id="6b047-122">Indicates whether the document sharing location is available to outside connections.</span></span>  <br/> |
|[<span data-ttu-id="6b047-123">AnonymousAccessAllowed (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6b047-123">AnonymousAccessAllowed (SOAP)</span></span>](anonymousaccessallowed-soap.md) <br/> |<span data-ttu-id="6b047-124">指示访问共享位置是否需要身份验证的用户。</span><span class="sxs-lookup"><span data-stu-id="6b047-124">Indicates whether access to the sharing location requires an authenticated user.</span></span>  <br/> |
|[<span data-ttu-id="6b047-125">CanModifyPermissions (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6b047-125">CanModifyPermissions (SOAP)</span></span>](canmodifypermissions-soap.md) <br/> |<span data-ttu-id="6b047-126">指示用户是否可以修改到文档共享位置的访问权限。</span><span class="sxs-lookup"><span data-stu-id="6b047-126">Indicates whether the user can modify access permissions to the document sharing location.</span></span>  <br/> |
|[<span data-ttu-id="6b047-127">IsDefault (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6b047-127">IsDefault (SOAP)</span></span>](isdefault-soap.md) <br/> |<span data-ttu-id="6b047-128">指示文档共享位置是否为用户的默认共享位置。</span><span class="sxs-lookup"><span data-stu-id="6b047-128">Indicates whether the document sharing location is the user's default sharing location.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6b047-129">父元素</span><span class="sxs-lookup"><span data-stu-id="6b047-129">Parent elements</span></span>

|<span data-ttu-id="6b047-130">**元素**</span><span class="sxs-lookup"><span data-stu-id="6b047-130">**Element**</span></span>|<span data-ttu-id="6b047-131">**说明**</span><span class="sxs-lookup"><span data-stu-id="6b047-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6b047-132">DocumentSharingLocations (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6b047-132">DocumentSharingLocations (SOAP)</span></span>](documentsharinglocations-soap.md) <br/> |<span data-ttu-id="6b047-133">包含共享位置和元数据文档的列表。</span><span class="sxs-lookup"><span data-stu-id="6b047-133">Contains a list of document sharing locations and metadata.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6b047-134">文本值</span><span class="sxs-lookup"><span data-stu-id="6b047-134">Text value</span></span>

<span data-ttu-id="6b047-135">无。</span><span class="sxs-lookup"><span data-stu-id="6b047-135">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6b047-136">元素信息</span><span class="sxs-lookup"><span data-stu-id="6b047-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6b047-137">命名空间</span><span class="sxs-lookup"><span data-stu-id="6b047-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="6b047-138">架构名称</span><span class="sxs-lookup"><span data-stu-id="6b047-138">Schema Name</span></span>  <br/> |<span data-ttu-id="6b047-139">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="6b047-139">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="6b047-140">验证文件</span><span class="sxs-lookup"><span data-stu-id="6b047-140">Validation File</span></span>  <br/> |<span data-ttu-id="6b047-141">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="6b047-141">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6b047-142">可以为空</span><span class="sxs-lookup"><span data-stu-id="6b047-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="6b047-143">True</span><span class="sxs-lookup"><span data-stu-id="6b047-143">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6b047-144">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6b047-144">See also</span></span>

- [<span data-ttu-id="6b047-145">GetUserSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6b047-145">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
- [<span data-ttu-id="6b047-146">Exchange 的自动发现 web 服务引用</span><span class="sxs-lookup"><span data-stu-id="6b047-146">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
- [<span data-ttu-id="6b047-147">SOAP Exchange 2013 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="6b047-147">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

