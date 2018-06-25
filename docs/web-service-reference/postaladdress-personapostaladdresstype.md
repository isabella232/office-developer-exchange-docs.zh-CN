---
title: PostalAddress (PersonaPostalAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 075f7d65-9d05-47cb-af26-0dd6d5593439
description: PostalAddress 元素指定的角色的邮政地址。
ms.openlocfilehash: fb418154867aebb4d284e75be579003c0ddc88f6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826855"
---
# <a name="postaladdress-personapostaladdresstype"></a><span data-ttu-id="db2c3-103">PostalAddress (PersonaPostalAddressType)</span><span class="sxs-lookup"><span data-stu-id="db2c3-103">PostalAddress (PersonaPostalAddressType)</span></span>

<span data-ttu-id="db2c3-104">**PostalAddress**元素指定的角色的邮政地址。</span><span class="sxs-lookup"><span data-stu-id="db2c3-104">The **PostalAddress** element specifies the postal address for a persona.</span></span> 
  
```XML
<PostalAddress>
   <Street/>
   <City/>
   <State/>
   <Country/>
   <PostalCode/>
   <PostOfficeBox/>
   <Type/>
   <Latitude/>
   <Longitude/>
   <Accuracy/>
   <Altitude/>
   <AltitudeAccuracy/>
   <FormattedAddress/>
   <LocationUri/>
   <LocationSource/>
</PostalAddress>
```

 <span data-ttu-id="db2c3-105">**PersonaPostalAddressType**</span><span class="sxs-lookup"><span data-stu-id="db2c3-105">**PersonaPostalAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="db2c3-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="db2c3-106">Attributes and elements</span></span>

<span data-ttu-id="db2c3-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="db2c3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="db2c3-108">属性</span><span class="sxs-lookup"><span data-stu-id="db2c3-108">Attributes</span></span>

<span data-ttu-id="db2c3-109">无。</span><span class="sxs-lookup"><span data-stu-id="db2c3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="db2c3-110">子元素</span><span class="sxs-lookup"><span data-stu-id="db2c3-110">Child elements</span></span>

<span data-ttu-id="db2c3-111">[街道](street.md) | [市/县](city.md) | [状态](state-ex15websvcsotherref.md) | [国家/地区](country.md) | [PostalCode](postalcode.md) | [PostOfficeBox](postofficebox.md) | [类型 （字符串）](type-string.md) | [纬度](latitude.md) |  [经度](longitude.md) | [准确性](accuracy.md) | [海拔](altitude.md) | [AltitudeAccuracy](altitudeaccuracy.md) | [FormattedAddress](formattedaddress.md) | [LocationUri](locationuri.md) | [LocationSource](locationsource.md)</span><span class="sxs-lookup"><span data-stu-id="db2c3-111">[Street](street.md) | [City](city.md) | [State](state-ex15websvcsotherref.md) | [Country](country.md) | [PostalCode](postalcode.md) | [PostOfficeBox](postofficebox.md) | [Type (string)](type-string.md) | [Latitude](latitude.md) | [Longitude](longitude.md) | [Accuracy](accuracy.md) | [Altitude](altitude.md) | [AltitudeAccuracy](altitudeaccuracy.md) | [FormattedAddress](formattedaddress.md) | [LocationUri](locationuri.md) | [LocationSource](locationsource.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="db2c3-112">父元素</span><span class="sxs-lookup"><span data-stu-id="db2c3-112">Parent elements</span></span>

[<span data-ttu-id="db2c3-113">EnhancedLocation</span><span class="sxs-lookup"><span data-stu-id="db2c3-113">EnhancedLocation</span></span>](enhancedlocation.md)
  
## <a name="remarks"></a><span data-ttu-id="db2c3-114">备注</span><span class="sxs-lookup"><span data-stu-id="db2c3-114">Remarks</span></span>

<span data-ttu-id="db2c3-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="db2c3-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="db2c3-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="db2c3-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="db2c3-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="db2c3-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="db2c3-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="db2c3-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="db2c3-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="db2c3-119">Schema name</span></span>  <br/> |<span data-ttu-id="db2c3-120">类型架构</span><span class="sxs-lookup"><span data-stu-id="db2c3-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="db2c3-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="db2c3-121">Validation file</span></span>  <br/> |<span data-ttu-id="db2c3-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="db2c3-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="db2c3-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="db2c3-123">Can be empty</span></span>  <br/> ||
   

