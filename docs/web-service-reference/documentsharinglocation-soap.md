---
title: DocumentSharingLocation （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21bc388c-33be-422b-a89d-30ade0fae8f1
description: DocumentSharingLocation 元素包含文档共享位置的位置和元数据信息。
ms.openlocfilehash: 6fed933da979ab3e3fca51ba606127b7f0a4e3f8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457058"
---
# <a name="documentsharinglocation-soap"></a><span data-ttu-id="3cce2-103">DocumentSharingLocation （SOAP）</span><span class="sxs-lookup"><span data-stu-id="3cce2-103">DocumentSharingLocation (SOAP)</span></span>

<span data-ttu-id="3cce2-104">**DocumentSharingLocation**元素包含文档共享位置的位置和元数据信息。</span><span class="sxs-lookup"><span data-stu-id="3cce2-104">The **DocumentSharingLocation** element contains location and metadata information for a document sharing location.</span></span> 
  
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

 <span data-ttu-id="3cce2-105">**DocumentSharingLocation**</span><span class="sxs-lookup"><span data-stu-id="3cce2-105">**DocumentSharingLocation**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3cce2-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="3cce2-106">Attributes and elements</span></span>

<span data-ttu-id="3cce2-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3cce2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3cce2-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="3cce2-108">Attributes</span></span>

<span data-ttu-id="3cce2-109">无。</span><span class="sxs-lookup"><span data-stu-id="3cce2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3cce2-110">子元素</span><span class="sxs-lookup"><span data-stu-id="3cce2-110">Child elements</span></span>

|<span data-ttu-id="3cce2-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="3cce2-111">**Element**</span></span>|<span data-ttu-id="3cce2-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="3cce2-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3cce2-113">ServiceUrl （SOAP）</span><span class="sxs-lookup"><span data-stu-id="3cce2-113">ServiceUrl (SOAP)</span></span>](serviceurl-soap.md) <br/> |<span data-ttu-id="3cce2-114">表示文档共享 web 服务的 URL。</span><span class="sxs-lookup"><span data-stu-id="3cce2-114">Represents the URL of the document sharing web service.</span></span>  <br/> |
|[<span data-ttu-id="3cce2-115">LocationUrl （SOAP）</span><span class="sxs-lookup"><span data-stu-id="3cce2-115">LocationUrl (SOAP)</span></span>](locationurl-soap.md) <br/> |<span data-ttu-id="3cce2-116">表示文档共享位置的 URL。</span><span class="sxs-lookup"><span data-stu-id="3cce2-116">Represents the URL of the document sharing location.</span></span>  <br/> |
|[<span data-ttu-id="3cce2-117">DisplayName （SOAP）</span><span class="sxs-lookup"><span data-stu-id="3cce2-117">DisplayName (SOAP)</span></span>](displayname-soap.md) <br/> |<span data-ttu-id="3cce2-118">表示要在 UI 中使用的文档共享位置的名称。</span><span class="sxs-lookup"><span data-stu-id="3cce2-118">Represents the name of the document sharing location to use in the UI.</span></span>  <br/> |
|[<span data-ttu-id="3cce2-119">SupportedFileExtensions （SOAP）</span><span class="sxs-lookup"><span data-stu-id="3cce2-119">SupportedFileExtensions (SOAP)</span></span>](supportedfileextensions-soap.md) <br/> |<span data-ttu-id="3cce2-120">表示可存储在文档共享位置的文件扩展名。</span><span class="sxs-lookup"><span data-stu-id="3cce2-120">Represents the file extensions that can be stored in the document sharing location.</span></span>  <br/> |
|[<span data-ttu-id="3cce2-121">ExternalAccessAllowed （SOAP）</span><span class="sxs-lookup"><span data-stu-id="3cce2-121">ExternalAccessAllowed (SOAP)</span></span>](externalaccessallowed-soap.md) <br/> |<span data-ttu-id="3cce2-122">指示文档共享位置是否可用于外部连接。</span><span class="sxs-lookup"><span data-stu-id="3cce2-122">Indicates whether the document sharing location is available to outside connections.</span></span>  <br/> |
|[<span data-ttu-id="3cce2-123">AnonymousAccessAllowed （SOAP）</span><span class="sxs-lookup"><span data-stu-id="3cce2-123">AnonymousAccessAllowed (SOAP)</span></span>](anonymousaccessallowed-soap.md) <br/> |<span data-ttu-id="3cce2-124">指示对共享位置的访问是否需要经过身份验证的用户。</span><span class="sxs-lookup"><span data-stu-id="3cce2-124">Indicates whether access to the sharing location requires an authenticated user.</span></span>  <br/> |
|[<span data-ttu-id="3cce2-125">CanModifyPermissions （SOAP）</span><span class="sxs-lookup"><span data-stu-id="3cce2-125">CanModifyPermissions (SOAP)</span></span>](canmodifypermissions-soap.md) <br/> |<span data-ttu-id="3cce2-126">指示用户是否可以修改文档共享位置的访问权限。</span><span class="sxs-lookup"><span data-stu-id="3cce2-126">Indicates whether the user can modify access permissions to the document sharing location.</span></span>  <br/> |
|[<span data-ttu-id="3cce2-127">IsDefault （SOAP）</span><span class="sxs-lookup"><span data-stu-id="3cce2-127">IsDefault (SOAP)</span></span>](isdefault-soap.md) <br/> |<span data-ttu-id="3cce2-128">指示文档共享位置是否为用户的默认共享位置。</span><span class="sxs-lookup"><span data-stu-id="3cce2-128">Indicates whether the document sharing location is the user's default sharing location.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3cce2-129">父元素</span><span class="sxs-lookup"><span data-stu-id="3cce2-129">Parent elements</span></span>

|<span data-ttu-id="3cce2-130">**元素**</span><span class="sxs-lookup"><span data-stu-id="3cce2-130">**Element**</span></span>|<span data-ttu-id="3cce2-131">**说明**</span><span class="sxs-lookup"><span data-stu-id="3cce2-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3cce2-132">DocumentSharingLocations （SOAP）</span><span class="sxs-lookup"><span data-stu-id="3cce2-132">DocumentSharingLocations (SOAP)</span></span>](documentsharinglocations-soap.md) <br/> |<span data-ttu-id="3cce2-133">包含文档共享位置和元数据的列表。</span><span class="sxs-lookup"><span data-stu-id="3cce2-133">Contains a list of document sharing locations and metadata.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3cce2-134">文本值</span><span class="sxs-lookup"><span data-stu-id="3cce2-134">Text value</span></span>

<span data-ttu-id="3cce2-135">无。</span><span class="sxs-lookup"><span data-stu-id="3cce2-135">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3cce2-136">元素信息</span><span class="sxs-lookup"><span data-stu-id="3cce2-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3cce2-137">命名空间</span><span class="sxs-lookup"><span data-stu-id="3cce2-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="3cce2-138">架构名称</span><span class="sxs-lookup"><span data-stu-id="3cce2-138">Schema Name</span></span>  <br/> |<span data-ttu-id="3cce2-139">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="3cce2-139">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="3cce2-140">验证文件</span><span class="sxs-lookup"><span data-stu-id="3cce2-140">Validation File</span></span>  <br/> |<span data-ttu-id="3cce2-141">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3cce2-141">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3cce2-142">可以为空</span><span class="sxs-lookup"><span data-stu-id="3cce2-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="3cce2-143">True</span><span class="sxs-lookup"><span data-stu-id="3cce2-143">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3cce2-144">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3cce2-144">See also</span></span>

- [<span data-ttu-id="3cce2-145">GetUserSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3cce2-145">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
- [<span data-ttu-id="3cce2-146">Exchange 的自动发现 web 服务参考</span><span class="sxs-lookup"><span data-stu-id="3cce2-146">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
- [<span data-ttu-id="3cce2-147">Exchange 2013 的 SOAP 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="3cce2-147">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

