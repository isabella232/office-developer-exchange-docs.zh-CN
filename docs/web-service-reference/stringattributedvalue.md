---
title: StringAttributedValue
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 911fec52-bde7-44a3-9231-04f327a42107
description: StringAttributedValue 元素指定与 persona 元素相关联的属性数组中的一个实例。
ms.openlocfilehash: bf4f5cd67bb254bd61f293cbef3699e588c6075b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463081"
---
# <a name="stringattributedvalue"></a><span data-ttu-id="8e114-103">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="8e114-103">StringAttributedValue</span></span>

<span data-ttu-id="8e114-104">**StringAttributedValue**元素指定与 persona 元素相关联的属性数组中的一个实例。</span><span class="sxs-lookup"><span data-stu-id="8e114-104">The **StringAttributedValue** element specifies an instance in an array of attributes associated with a persona element.</span></span> 
  
```XML
<StringAttributedValue>
   <Value/>
   <Attributions/>
</StringAttributedValue>
```

 <span data-ttu-id="8e114-105">**StringAttributedValueType**</span><span class="sxs-lookup"><span data-stu-id="8e114-105">**StringAttributedValueType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8e114-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8e114-106">Attributes and elements</span></span>

<span data-ttu-id="8e114-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8e114-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8e114-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="8e114-108">Attributes</span></span>

<span data-ttu-id="8e114-109">无。</span><span class="sxs-lookup"><span data-stu-id="8e114-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8e114-110">子元素</span><span class="sxs-lookup"><span data-stu-id="8e114-110">Child elements</span></span>

<span data-ttu-id="8e114-111">[值](value.md)  | [归属（ArrayOfValueAttributionsType）](attributions-arrayofvalueattributionstype.md)</span><span class="sxs-lookup"><span data-stu-id="8e114-111">[Value](value.md) | [Attributions (ArrayOfValueAttributionsType)](attributions-arrayofvalueattributionstype.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8e114-112">父元素</span><span class="sxs-lookup"><span data-stu-id="8e114-112">Parent elements</span></span>

<span data-ttu-id="8e114-113">[DisplayNames](displaynames.md)  | [FileAses](fileases.md)  | [FileAsIds](fileasids.md)  | [DisplayNamePrefixes](displaynameprefixes.md)  | [GivenNames](givennames.md)  | [MiddleNames](middlenames.md)  | [Surnames](surnames.md)  | [生成](generations.md)  | [昵称](nicknames.md)  | [缩写](initials.md)  | [YomiCompanyNames](yomicompanynames.md)  | [YomiFirstNames](yomifirstnames.md)  | [YomiLastNames](yomilastnames.md)  | [BusinessHomePages](businesshomepages.md)  | [PersonalHomePages](personalhomepages.md)  | [OfficeLocations](officelocations.md)  | [ImAddresses](imaddresses.md)  | [ImAddresses2](imaddresses2.md)  | [ImAddresses3](imaddresses3.md)  | [标题](titles.md)  | [部门](departments.md)  | [CompanyNames](companynames.md)  | [经理](managers.md)  | [AssistantNames](assistantnames.md)  | [Professions](professions.md)  | [SpouseNames](spousenames.md)  | [学校](schools.md)  | [业余爱好](hobbies.md)  | [WeddingAnniversaries](weddinganniversaries.md)  | [生日](birthdays.md)  | [位置](locations.md)</span><span class="sxs-lookup"><span data-stu-id="8e114-113">[DisplayNames](displaynames.md) | [FileAses](fileases.md) | [FileAsIds](fileasids.md) | [DisplayNamePrefixes](displaynameprefixes.md) | [GivenNames](givennames.md) | [MiddleNames](middlenames.md) | [Surnames](surnames.md) | [Generations](generations.md) | [Nicknames](nicknames.md) | [Initials](initials.md) | [YomiCompanyNames](yomicompanynames.md) | [YomiFirstNames](yomifirstnames.md) | [YomiLastNames](yomilastnames.md) | [BusinessHomePages](businesshomepages.md) | [PersonalHomePages](personalhomepages.md) | [OfficeLocations](officelocations.md) | [ImAddresses](imaddresses.md) | [ImAddresses2](imaddresses2.md) | [ImAddresses3](imaddresses3.md) | [Titles](titles.md) | [Departments](departments.md) | [CompanyNames](companynames.md) | [Managers](managers.md) | [AssistantNames](assistantnames.md) | [Professions](professions.md) | [SpouseNames](spousenames.md) | [Schools](schools.md) | [Hobbies](hobbies.md) | [WeddingAnniversaries](weddinganniversaries.md) | [Birthdays](birthdays.md) | [Locations](locations.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8e114-114">备注</span><span class="sxs-lookup"><span data-stu-id="8e114-114">Remarks</span></span>

<span data-ttu-id="8e114-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="8e114-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="8e114-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8e114-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8e114-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="8e114-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8e114-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="8e114-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8e114-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="8e114-119">Schema name</span></span>  <br/> |<span data-ttu-id="8e114-120">类型架构</span><span class="sxs-lookup"><span data-stu-id="8e114-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="8e114-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="8e114-121">Validation file</span></span>  <br/> |<span data-ttu-id="8e114-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8e114-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8e114-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="8e114-123">Can be empty</span></span>  <br/> ||
   

