---
title: Value （PersonaPostalAddressType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: be838fc2-cfcb-4856-b095-a8e5366bb6c6
description: Value 元素指定与通信地址相关联的信息。
ms.openlocfilehash: 2d644ff45fe89061ccd90279773f3a5a5b7fe7cc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466470"
---
# <a name="value-personapostaladdresstype"></a><span data-ttu-id="cd3bf-103">Value （PersonaPostalAddressType）</span><span class="sxs-lookup"><span data-stu-id="cd3bf-103">Value (PersonaPostalAddressType)</span></span>

<span data-ttu-id="cd3bf-104">**Value**元素指定与通信地址相关联的信息。</span><span class="sxs-lookup"><span data-stu-id="cd3bf-104">The **Value** element specifies information associated with a postal address.</span></span> 
  
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

<span data-ttu-id="cd3bf-105">**PersonaPostalAddressType**</span><span class="sxs-lookup"><span data-stu-id="cd3bf-105">**PersonaPostalAddressType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="cd3bf-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="cd3bf-106">Attributes and elements</span></span>

<span data-ttu-id="cd3bf-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="cd3bf-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cd3bf-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="cd3bf-108">Attributes</span></span>

<span data-ttu-id="cd3bf-109">无。</span><span class="sxs-lookup"><span data-stu-id="cd3bf-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cd3bf-110">子元素</span><span class="sxs-lookup"><span data-stu-id="cd3bf-110">Child elements</span></span>

<span data-ttu-id="cd3bf-111">[街道](street.md)  | [城市](city.md)  | [状态](state-ex15websvcsotherref.md)  | [国家/地区](country.md)  | [邮政编码](postalcode.md)  | [PostOfficeBox](postofficebox.md)  | [类型（字符串）](type-string.md)  | [纬度](latitude.md)  | [经度](longitude.md)  | [准确性](accuracy.md)  | [海拔](altitude.md)  | [AltitudeAccuracy](altitudeaccuracy.md)  | [FormattedAddress](formattedaddress.md)  | [LocationUri](locationuri.md)  | [LocationSource](locationsource.md)</span><span class="sxs-lookup"><span data-stu-id="cd3bf-111">[Street](street.md) | [City](city.md) | [State](state-ex15websvcsotherref.md) | [Country](country.md) | [PostalCode](postalcode.md) | [PostOfficeBox](postofficebox.md) | [Type (string)](type-string.md) | [Latitude](latitude.md) | [Longitude](longitude.md) | [Accuracy](accuracy.md) | [Altitude](altitude.md) | [AltitudeAccuracy](altitudeaccuracy.md) | [FormattedAddress](formattedaddress.md) | [LocationUri](locationuri.md) | [LocationSource](locationsource.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cd3bf-112">父元素</span><span class="sxs-lookup"><span data-stu-id="cd3bf-112">Parent elements</span></span>

[<span data-ttu-id="cd3bf-113">PostalAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="cd3bf-113">PostalAddressAttributedValue</span></span>](postaladdressattributedvalue.md)
  
## <a name="remarks"></a><span data-ttu-id="cd3bf-114">备注</span><span class="sxs-lookup"><span data-stu-id="cd3bf-114">Remarks</span></span>

<span data-ttu-id="cd3bf-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="cd3bf-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="cd3bf-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="cd3bf-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cd3bf-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="cd3bf-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cd3bf-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="cd3bf-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cd3bf-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="cd3bf-119">Schema name</span></span>  <br/> |<span data-ttu-id="cd3bf-120">类型架构</span><span class="sxs-lookup"><span data-stu-id="cd3bf-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="cd3bf-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="cd3bf-121">Validation file</span></span>  <br/> |<span data-ttu-id="cd3bf-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="cd3bf-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cd3bf-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="cd3bf-123">Can be empty</span></span>  <br/> ||
   

