---
title: 电话（PhoneEntityType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f6925cc9-7f22-478f-b9ba-b77575772471
description: Phone 元素指定通过电话号码实体提取产生的单个电话号码。
ms.openlocfilehash: eec05fbb1cbbfa5c9b47cdb3cef1af6085ab51b6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457555"
---
# <a name="phone-phoneentitytype"></a><span data-ttu-id="2ff3a-103">电话（PhoneEntityType）</span><span class="sxs-lookup"><span data-stu-id="2ff3a-103">Phone (PhoneEntityType)</span></span>

<span data-ttu-id="2ff3a-104">**Phone**元素指定通过电话号码实体提取产生的单个电话号码。</span><span class="sxs-lookup"><span data-stu-id="2ff3a-104">The **Phone** element specifies a single phone number that results from a phone number entity extraction.</span></span> 
  
```XML
<Phone>
   <Position/>
   <OriginalPhoneString/>
   <PhoneString/>
   <Type/>
</Phone>
```

 <span data-ttu-id="2ff3a-105">**PhoneEntityType**</span><span class="sxs-lookup"><span data-stu-id="2ff3a-105">**PhoneEntityType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2ff3a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2ff3a-106">Attributes and elements</span></span>

<span data-ttu-id="2ff3a-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2ff3a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2ff3a-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="2ff3a-108">Attributes</span></span>

<span data-ttu-id="2ff3a-109">无。</span><span class="sxs-lookup"><span data-stu-id="2ff3a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2ff3a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2ff3a-110">Child elements</span></span>

<span data-ttu-id="2ff3a-111">[位置](position.md)  | [Phonenumber.originalphonestring](originalphonestring.md)  | [Phonenumber.phonestring](phonestring.md)  | [类型（字符串）](type-string.md)</span><span class="sxs-lookup"><span data-stu-id="2ff3a-111">[Position](position.md) | [OriginalPhoneString](originalphonestring.md) | [PhoneString](phonestring.md) | [Type (string)](type-string.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2ff3a-112">父元素</span><span class="sxs-lookup"><span data-stu-id="2ff3a-112">Parent elements</span></span>

[<span data-ttu-id="2ff3a-113">PhoneNumbers （ArrayOfPhoneEntitiesType）</span><span class="sxs-lookup"><span data-stu-id="2ff3a-113">PhoneNumbers (ArrayOfPhoneEntitiesType)</span></span>](phonenumbers-arrayofphoneentitiestype.md)
  
## <a name="remarks"></a><span data-ttu-id="2ff3a-114">备注</span><span class="sxs-lookup"><span data-stu-id="2ff3a-114">Remarks</span></span>

<span data-ttu-id="2ff3a-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="2ff3a-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2ff3a-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2ff3a-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2ff3a-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="2ff3a-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2ff3a-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="2ff3a-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2ff3a-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="2ff3a-119">Schema name</span></span>  <br/> |<span data-ttu-id="2ff3a-120">类型架构</span><span class="sxs-lookup"><span data-stu-id="2ff3a-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="2ff3a-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="2ff3a-121">Validation file</span></span>  <br/> |<span data-ttu-id="2ff3a-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2ff3a-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2ff3a-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="2ff3a-123">Can be empty</span></span>  <br/> ||
   

