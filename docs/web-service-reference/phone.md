---
title: 电话
manager: sethgros
ms.date: 09/17/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9381d8e0-b705-49fd-a822-00fb485bdbab
description: Phone 元素指定通过联系人实体提取产生的单个电话号码。
ms.openlocfilehash: 7b0047eda90f2e2bb94fd7d0b8d317715ac5d2c9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459705"
---
# <a name="phone"></a><span data-ttu-id="1fd9f-103">电话</span><span class="sxs-lookup"><span data-stu-id="1fd9f-103">Phone</span></span>

<span data-ttu-id="1fd9f-104">**Phone**元素指定通过联系人实体提取产生的单个电话号码。</span><span class="sxs-lookup"><span data-stu-id="1fd9f-104">The **Phone** element specifies a single phone number that results from a contact entity extraction.</span></span> 
  
```XML
<Phone>
   <OriginalPhoneString/>
   <PhoneString/>
   <Type/>
</Phone>
```

 <span data-ttu-id="1fd9f-105">**PhoneType**</span><span class="sxs-lookup"><span data-stu-id="1fd9f-105">**PhoneType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1fd9f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1fd9f-106">Attributes and elements</span></span>

<span data-ttu-id="1fd9f-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1fd9f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1fd9f-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="1fd9f-108">Attributes</span></span>

<span data-ttu-id="1fd9f-109">无。</span><span class="sxs-lookup"><span data-stu-id="1fd9f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1fd9f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="1fd9f-110">Child elements</span></span>

<span data-ttu-id="1fd9f-111">[Phonenumber.originalphonestring](originalphonestring.md)  | [Phonenumber.phonestring](phonestring.md)  | [类型（字符串）](type-string.md)</span><span class="sxs-lookup"><span data-stu-id="1fd9f-111">[OriginalPhoneString](originalphonestring.md) | [PhoneString](phonestring.md) | [Type (string)](type-string.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1fd9f-112">父元素</span><span class="sxs-lookup"><span data-stu-id="1fd9f-112">Parent elements</span></span>

[<span data-ttu-id="1fd9f-113">PhoneNumbers （ArrayOfPhonesType）</span><span class="sxs-lookup"><span data-stu-id="1fd9f-113">PhoneNumbers (ArrayOfPhonesType)</span></span>](phonenumbers-arrayofphonestype.md)
  
## <a name="remarks"></a><span data-ttu-id="1fd9f-114">备注</span><span class="sxs-lookup"><span data-stu-id="1fd9f-114">Remarks</span></span>

<span data-ttu-id="1fd9f-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="1fd9f-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="1fd9f-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1fd9f-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1fd9f-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="1fd9f-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1fd9f-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="1fd9f-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1fd9f-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="1fd9f-119">Schema name</span></span>  <br/> |<span data-ttu-id="1fd9f-120">类型架构</span><span class="sxs-lookup"><span data-stu-id="1fd9f-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="1fd9f-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="1fd9f-121">Validation file</span></span>  <br/> |<span data-ttu-id="1fd9f-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1fd9f-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1fd9f-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="1fd9f-123">Can be empty</span></span>  <br/> ||
   

