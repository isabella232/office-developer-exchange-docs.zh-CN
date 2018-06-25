---
title: 值 (PersonaPostalAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: be838fc2-cfcb-4856-b095-a8e5366bb6c6
description: Value 元素指定关联邮政地址的信息。
ms.openlocfilehash: 048d3a49552f1a9e89744e4cd16ec1745417e923
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838510"
---
# <a name="value-personapostaladdresstype"></a><span data-ttu-id="cd8e6-103">值 (PersonaPostalAddressType)</span><span class="sxs-lookup"><span data-stu-id="cd8e6-103">Value (PersonaPostalAddressType)</span></span>

<span data-ttu-id="cd8e6-104">**Value**元素指定关联的邮政地址的信息。</span><span class="sxs-lookup"><span data-stu-id="cd8e6-104">The **Value** element specifies information associated with a postal address.</span></span> 
  
```XML
<Value>
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
</Value>
```

<span data-ttu-id="cd8e6-105">**PersonaPostalAddressType**</span><span class="sxs-lookup"><span data-stu-id="cd8e6-105">**PersonaPostalAddressType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="cd8e6-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="cd8e6-106">Attributes and elements</span></span>

<span data-ttu-id="cd8e6-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="cd8e6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cd8e6-108">属性</span><span class="sxs-lookup"><span data-stu-id="cd8e6-108">Attributes</span></span>

<span data-ttu-id="cd8e6-109">无。</span><span class="sxs-lookup"><span data-stu-id="cd8e6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cd8e6-110">子元素</span><span class="sxs-lookup"><span data-stu-id="cd8e6-110">Child elements</span></span>

<span data-ttu-id="cd8e6-111">[街道](street.md) | [市/县](city.md) | [状态](state-ex15websvcsotherref.md) | [国家/地区](country.md) | [PostalCode](postalcode.md) | [PostOfficeBox](postofficebox.md) | [类型 （字符串）](type-string.md) | [纬度](latitude.md) |  [经度](longitude.md) | [准确性](accuracy.md) | [海拔](altitude.md) | [AltitudeAccuracy](altitudeaccuracy.md) | [FormattedAddress](formattedaddress.md) | [LocationUri](locationuri.md) | [LocationSource](locationsource.md)</span><span class="sxs-lookup"><span data-stu-id="cd8e6-111">[Street](street.md) | [City](city.md) | [State](state-ex15websvcsotherref.md) | [Country](country.md) | [PostalCode](postalcode.md) | [PostOfficeBox](postofficebox.md) | [Type (string)](type-string.md) | [Latitude](latitude.md) | [Longitude](longitude.md) | [Accuracy](accuracy.md) | [Altitude](altitude.md) | [AltitudeAccuracy](altitudeaccuracy.md) | [FormattedAddress](formattedaddress.md) | [LocationUri](locationuri.md) | [LocationSource](locationsource.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cd8e6-112">父元素</span><span class="sxs-lookup"><span data-stu-id="cd8e6-112">Parent elements</span></span>

[<span data-ttu-id="cd8e6-113">PostalAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="cd8e6-113">PostalAddressAttributedValue</span></span>](postaladdressattributedvalue.md)
  
## <a name="remarks"></a><span data-ttu-id="cd8e6-114">备注</span><span class="sxs-lookup"><span data-stu-id="cd8e6-114">Remarks</span></span>

<span data-ttu-id="cd8e6-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="cd8e6-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="cd8e6-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="cd8e6-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cd8e6-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="cd8e6-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cd8e6-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="cd8e6-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cd8e6-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="cd8e6-119">Schema name</span></span>  <br/> |<span data-ttu-id="cd8e6-120">类型架构</span><span class="sxs-lookup"><span data-stu-id="cd8e6-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="cd8e6-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="cd8e6-121">Validation file</span></span>  <br/> |<span data-ttu-id="cd8e6-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="cd8e6-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cd8e6-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="cd8e6-123">Can be empty</span></span>  <br/> ||
   

