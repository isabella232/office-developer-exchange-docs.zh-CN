---
title: PhoneNumberAttributedValue
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8bf16552-b672-424a-91b6-6470e20a49ad
description: PhoneNumberAttributedValue 元素指定实例及其关联的归属和数组的电话号码。
ms.openlocfilehash: a2cc2685e804b3bf6dd5f9083b31a4bd137f8aac
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826771"
---
# <a name="phonenumberattributedvalue"></a><span data-ttu-id="9a322-103">PhoneNumberAttributedValue</span><span class="sxs-lookup"><span data-stu-id="9a322-103">PhoneNumberAttributedValue</span></span>

<span data-ttu-id="9a322-104">**PhoneNumberAttributedValue**元素指定实例及其关联的归属和数组的电话号码。</span><span class="sxs-lookup"><span data-stu-id="9a322-104">The **PhoneNumberAttributedValue** element specifies an instance of an array of phone numbers and their associated attributions.</span></span> 
  
```XML
<PhoneNumberAttributedValue>
   <Value/>
   <Attributions/>
</PhoneNumberAttributedValue>
```

 <span data-ttu-id="9a322-105">**PhoneNumberAttributedValueType**</span><span class="sxs-lookup"><span data-stu-id="9a322-105">**PhoneNumberAttributedValueType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9a322-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9a322-106">Attributes and elements</span></span>

<span data-ttu-id="9a322-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9a322-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9a322-108">属性</span><span class="sxs-lookup"><span data-stu-id="9a322-108">Attributes</span></span>

<span data-ttu-id="9a322-109">无。</span><span class="sxs-lookup"><span data-stu-id="9a322-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9a322-110">子元素</span><span class="sxs-lookup"><span data-stu-id="9a322-110">Child elements</span></span>

<span data-ttu-id="9a322-111">[值 (PersonaPhoneNumberType)](value-personaphonenumbertype.md) | [归属 (ArrayOfValueAttributionsType)](attributions-arrayofvalueattributionstype.md)</span><span class="sxs-lookup"><span data-stu-id="9a322-111">[Value (PersonaPhoneNumberType)](value-personaphonenumbertype.md) | [Attributions (ArrayOfValueAttributionsType)](attributions-arrayofvalueattributionstype.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9a322-112">父元素</span><span class="sxs-lookup"><span data-stu-id="9a322-112">Parent elements</span></span>

<span data-ttu-id="9a322-113">[BusinessPhoneNumbers](businessphonenumbers.md) | [BusinessPhoneNumbers2](businessphonenumbers2.md) | [HomePhones](homephones.md) | [HomePhones2](homephones2.md) | [MobilePhones](mobilephones.md) | [MobilePhones2](mobilephones2.md) | [AssistantPhoneNumbers](assistantphonenumbers.md)  |  [CallbackPhones](callbackphones.md) | [CarPhones](carphones.md) | [HomeFaxes](homefaxes.md) | [OrganizationMainPhones](organizationmainphones.md) | [OtherFaxes](otherfaxes.md) | [OtherTelephones](othertelephones.md)  |  [OtherPhones2](otherphones2.md) | [寻呼机](pagers.md) | [RadioPhones](radiophones.md) | [TelexNumbers](telexnumbers.md) | [TTYTDDPhoneNumbers](ttytddphonenumbers.md) | [WorkFaxes](workfaxes.md)</span><span class="sxs-lookup"><span data-stu-id="9a322-113">[BusinessPhoneNumbers](businessphonenumbers.md) | [BusinessPhoneNumbers2](businessphonenumbers2.md) | [HomePhones](homephones.md) | [HomePhones2](homephones2.md) | [MobilePhones](mobilephones.md) | [MobilePhones2](mobilephones2.md) | [AssistantPhoneNumbers](assistantphonenumbers.md) | [CallbackPhones](callbackphones.md) | [CarPhones](carphones.md) | [HomeFaxes](homefaxes.md) | [OrganizationMainPhones](organizationmainphones.md) | [OtherFaxes](otherfaxes.md) | [OtherTelephones](othertelephones.md) | [OtherPhones2](otherphones2.md) | [Pagers](pagers.md) | [RadioPhones](radiophones.md) | [TelexNumbers](telexnumbers.md) | [TTYTDDPhoneNumbers](ttytddphonenumbers.md) | [WorkFaxes](workfaxes.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9a322-114">备注</span><span class="sxs-lookup"><span data-stu-id="9a322-114">Remarks</span></span>

<span data-ttu-id="9a322-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="9a322-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="9a322-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9a322-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9a322-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="9a322-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9a322-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="9a322-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9a322-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="9a322-119">Schema name</span></span>  <br/> |<span data-ttu-id="9a322-120">类型架构</span><span class="sxs-lookup"><span data-stu-id="9a322-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="9a322-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="9a322-121">Validation file</span></span>  <br/> |<span data-ttu-id="9a322-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9a322-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9a322-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="9a322-123">Can be empty</span></span>  <br/> ||
   

