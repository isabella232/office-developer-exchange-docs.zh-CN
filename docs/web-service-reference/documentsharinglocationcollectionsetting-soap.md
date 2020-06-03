---
title: DocumentSharingLocationCollectionSetting （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e3346f9-7a55-4e87-b121-9b1ee7f227f4
description: DocumentSharingLocationCollectionSetting 元素表示一个用户设置，该设置是文档共享位置和元数据的集合。
ms.openlocfilehash: 2a52f639a1f1bf638aacc78666c58aed1fae0fa0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457051"
---
# <a name="documentsharinglocationcollectionsetting-soap"></a><span data-ttu-id="19193-103">DocumentSharingLocationCollectionSetting （SOAP）</span><span class="sxs-lookup"><span data-stu-id="19193-103">DocumentSharingLocationCollectionSetting (SOAP)</span></span>

<span data-ttu-id="19193-104">**DocumentSharingLocationCollectionSetting**元素表示一个用户设置，该设置是文档共享位置和元数据的集合。</span><span class="sxs-lookup"><span data-stu-id="19193-104">The **DocumentSharingLocationCollectionSetting** element represents a user setting that is a collection of documentation sharing locations and metadata.</span></span> 
  
[<span data-ttu-id="19193-105">DocumentSharingLocationCollectionSetting （SOAP）</span><span class="sxs-lookup"><span data-stu-id="19193-105">DocumentSharingLocationCollectionSetting (SOAP)</span></span>](documentsharinglocationcollectionsetting-soap.md)
  
```XML
<DocumentSharingLocationCollectionSetting>
    <DocumentSharingLocations />
</DocumentSharingLocationCollectionSetting>
```

 <span data-ttu-id="19193-106">**DocumentSharingLocationCollectionSetting**</span><span class="sxs-lookup"><span data-stu-id="19193-106">**DocumentSharingLocationCollectionSetting**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="19193-107">属性和元素</span><span class="sxs-lookup"><span data-stu-id="19193-107">Attributes and elements</span></span>

<span data-ttu-id="19193-108">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="19193-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="19193-109">Attributes</span><span class="sxs-lookup"><span data-stu-id="19193-109">Attributes</span></span>

<span data-ttu-id="19193-110">无。</span><span class="sxs-lookup"><span data-stu-id="19193-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="19193-111">子元素</span><span class="sxs-lookup"><span data-stu-id="19193-111">Child elements</span></span>

|<span data-ttu-id="19193-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="19193-112">**Element**</span></span>|<span data-ttu-id="19193-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="19193-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="19193-114">DocumentSharingLocations （SOAP）</span><span class="sxs-lookup"><span data-stu-id="19193-114">DocumentSharingLocations (SOAP)</span></span>](documentsharinglocations-soap.md) <br/> |<span data-ttu-id="19193-115">表示文档共享位置列表的位置和元数据。</span><span class="sxs-lookup"><span data-stu-id="19193-115">Represents the location and metadata for a list of document sharing locations.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="19193-116">父元素</span><span class="sxs-lookup"><span data-stu-id="19193-116">Parent elements</span></span>

|<span data-ttu-id="19193-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="19193-117">**Element**</span></span>|<span data-ttu-id="19193-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="19193-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="19193-119">UserSettings （SOAP）</span><span class="sxs-lookup"><span data-stu-id="19193-119">UserSettings (SOAP)</span></span>](usersettings-soap.md) <br/> |<span data-ttu-id="19193-120">表示用户设置的集合。</span><span class="sxs-lookup"><span data-stu-id="19193-120">Represents a collection of user settings.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="19193-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="19193-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="19193-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="19193-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="19193-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="19193-123">Schema Name</span></span>  <br/> |<span data-ttu-id="19193-124">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="19193-124">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="19193-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="19193-125">Validation File</span></span>  <br/> |<span data-ttu-id="19193-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="19193-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="19193-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="19193-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="19193-128">True</span><span class="sxs-lookup"><span data-stu-id="19193-128">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="19193-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="19193-129">See also</span></span>

- [<span data-ttu-id="19193-130">GetUserSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="19193-130">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
- [<span data-ttu-id="19193-131">Exchange 的自动发现 web 服务参考</span><span class="sxs-lookup"><span data-stu-id="19193-131">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
- [<span data-ttu-id="19193-132">Exchange 2013 的 SOAP 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="19193-132">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

