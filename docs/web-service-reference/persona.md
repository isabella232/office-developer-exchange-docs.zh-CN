---
title: 角色
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b115c990-3a2d-4536-9af3-ac1fd06d00dc
description: Persona 元素指定 GetPersona 请求返回的一组角色数据。
ms.openlocfilehash: 093b346300b5fdcbfb31f2e1240d57d9476e250a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465875"
---
# <a name="persona"></a><span data-ttu-id="2ea25-103">角色</span><span class="sxs-lookup"><span data-stu-id="2ea25-103">Persona</span></span>

<span data-ttu-id="2ea25-104">**Persona**元素指定**GetPersona**请求返回的一组角色数据。</span><span class="sxs-lookup"><span data-stu-id="2ea25-104">The **Persona** element specifies a set of persona data returned by a **GetPersona** request.</span></span> 
  
```XML
<Persona>
   <PersonaId/>
   <PersonaType/>
   <PersonaObjectStatus/>
   <CreationTime/>
   <Bodies/>
   <DisplayNameFirstLastSortKey/>
   <DisplayNameLastFirstSortKey/>
   <CompanyNameSortKey/>
   <HomeCitySortKey/>
   <WorkCitySortKey/>
   <DisplayNameFirstLastHeader/>
   <DisplayNameLastFirstHeader/>
   <FileAsHeader/>
   <DisplayName/>
   <DisplayNameFirstLast/>
   <DisplayNameLastFirst/>
   <FileAs/>
   <FileAsId/>
   <DisplayNamePrefix/>
   <GivenName/>
   <MiddleName/>
   <Surname/>
   <Generation/>
   <Nickname/>
   <YomiCompanyName/>
   <YomiFirstName/>
   <YomiLastName/>
   <Title/>
   <Department/>
   <CompanyName/>
   <Location/>
   <EmailAddress/>
   <EmailAddresses/>
   <PhoneNumber/>
   <ImAddress/>
   <HomeCity/>
   <WorkCity/>
   <RelevanceScore/>
   <FolderIds/>
   <Attributions/>
   <DisplayNames/>
   <FileAses/>
   <FileAsIds/>
   <DisplayNamePrefixes/>
   <GivenNames/>
   <MiddleNames/>
   <Surnames/>
   <Generations/>
   <Nicknames/>
   <Initials/>
   <YomiCompanyNames/>
   <YomiFirstNames/>
   <YomiLastNames/>
   <BusinessPhoneNumbers/>
   <BusinessPhoneNumbers2/>
   <HomePhones/>
   <HomePhones2/>
   <MobilePhones/>
   <MobilePhones2/>
   <AssistantPhoneNumbers/>
   <CallbackPhones/>
   <CarPhones/>
   <HomeFaxes/>
   <OrganizationMainPhones/>
   <OtherFaxes/>
   <OtherTelephones/>
   <OtherPhones2/>
   <Pagers/>
   <RadioPhones/>
   <TelexNumbers/>
   <TTYTDDPhoneNumbers/>
   <WorkFaxes/>
   <Emails1/>
   <Emails2/>
   <Emails3/>
   <BusinessHomePages/>
   <PersonalHomePages/>
   <OfficeLocations/>
   <ImAddresses/>
   <ImAddresses2/>
   <ImAddresses3/>
   <BusinessAddresses/>
   <HomeAddresses/>
   <OtherAddresses/>
   <Titles/>
   <Departments/>
   <CompanyNames/>
   <Managers/>
   <AssistantNames/>
   <Professions/>
   <SpouseNames/>
   <Children/>
   <Schools/>
   <Hobbies/>
   <WeddingAnniversaries/>
   <Birthdays/>
   <Locations/>
   <ExtendedProperties/>
</Persona>

```

 <span data-ttu-id="2ea25-105">**PersonaType**</span><span class="sxs-lookup"><span data-stu-id="2ea25-105">**PersonaType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2ea25-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2ea25-106">Attributes and elements</span></span>

<span data-ttu-id="2ea25-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2ea25-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2ea25-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="2ea25-108">Attributes</span></span>

<span data-ttu-id="2ea25-109">无。</span><span class="sxs-lookup"><span data-stu-id="2ea25-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2ea25-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2ea25-110">Child elements</span></span>

<span data-ttu-id="2ea25-111">[PersonaId](personaid.md)  | [PersonaType](personatype.md)  | [PersonaObjectStatus](personaobjectstatus.md)  | [CreationTime](creationtime.md)  | [正文](bodies.md)  | [DisplayNameFirstLastSortKey](displaynamefirstlastsortkey.md)  | [DisplayNameLastFirstSortKey](displaynamelastfirstsortkey.md)  | [CompanyNameSortKey](companynamesortkey.md)  | [HomeCitySortKey](homecitysortkey.md)  | [WorkCitySortKey](workcitysortkey.md)  | [DisplayNameFirstLastHeader](displaynamefirstlastheader.md)  | [DisplayNameLastFirstHeader](displaynamelastfirstheader.md)  | [FileAsHeader](fileasheader.md)  | [DisplayName （string）](displayname-string.md)  | [DisplayNameFirstLast](displaynamefirstlast.md)  | [DisplayNameLastFirst](displaynamelastfirst.md)  | [FileAs](fileas.md)  | [FileAsId](fileasid.md)  | [DisplayNamePrefix](displaynameprefix.md)  | [GivenName](givenname.md)  | [称谓](middlename.md)  | [姓](surname.md)  | [生成](generation.md)  | [昵称](nickname.md)  | [YomiCompanyName](yomicompanyname.md)  | [YomiFirstName](yomifirstname.md)  | [YomiLastName](yomilastname.md)  | [标题](title.md)  | [部门](department.md)  | [公司名称](companyname.md)  | [位置](location.md)  | [EmailAddress （EmailAddressType）](emailaddress-emailaddresstype.md)  | [EmailAddresses （ArrayOfEmailAddressesType）](emailaddresses-arrayofemailaddressestype.md)  | [PhoneNumber](phonenumber.md)  | [ImAddress （字符串）](imaddress-string.md)  | [HomeCity](homecity.md)  | [WorkCity](workcity.md)  | [RelevanceScore](relevancescore.md)  | [FolderIds （ArrayOfFolderIdType）](folderids-arrayoffolderidtype.md)  | [归属（ArrayOfPersonaAttributionsType）](attributions-arrayofpersonaattributionstype.md)  | [DisplayNames](displaynames.md)  | [FileAses](fileases.md)  | [FileAsIds](fileasids.md)  | [DisplayNamePrefixes](displaynameprefixes.md)  | [GivenNames](givennames.md)  | [MiddleNames](middlenames.md)  | [Surnames](surnames.md)  | [生成](generations.md)  | [昵称](nicknames.md)  | [缩写（ArrayOfStringAttributedValuesType）](initials-arrayofstringattributedvaluestype.md)  | [YomiCompanyNames](yomicompanynames.md)  | [YomiFirstNames](yomifirstnames.md)  | [YomiLastNames](yomilastnames.md)  | [BusinessPhoneNumbers](businessphonenumbers.md)  | [BusinessPhoneNumbers2](businessphonenumbers2.md)  | [HomePhones](homephones.md)  | [HomePhones2](homephones2.md)  | [MobilePhones](mobilephones.md)  | [MobilePhones2](mobilephones2.md)  | [AssistantPhoneNumbers](assistantphonenumbers.md)  | [CallbackPhones](callbackphones.md)  | [CarPhones](carphones.md)  | [HomeFaxes](homefaxes.md)  | [OrganizationMainPhones](organizationmainphones.md)  | [OtherFaxes](otherfaxes.md)  | [OtherTelephones](othertelephones.md)  | [OtherPhones2](otherphones2.md)  | [呼机](pagers.md)  | [RadioPhones](radiophones.md)  | [TelexNumbers](telexnumbers.md)  | [TTYTDDPhoneNumbers](ttytddphonenumbers.md)  | [WorkFaxes](workfaxes.md)  | [Emails1](emails1.md)  | [Emails2](emails2.md)  | [Emails3](emails3.md)  | [BusinessHomePages](businesshomepages.md)  | [PersonalHomePages](personalhomepages.md)  | [OfficeLocations](officelocations.md)  | [ImAddresses （ArrayOfStringAttributedValuesType）](imaddresses-arrayofstringattributedvaluestype.md)  | [ImAddresses2](imaddresses2.md)  | [ImAddresses3](imaddresses3.md)  | [BusinessAddresses](businessaddresses.md)  | [HomeAddresses](homeaddresses.md)  | [OtherAddresses](otheraddresses.md)  | [标题](titles.md)  | [部门](departments.md)  | [CompanyNames](companynames.md)  | [经理](managers.md)  | [AssistantNames](assistantnames.md)  | [Professions](professions.md)  | [SpouseNames](spousenames.md)  | [子级（ArrayOfStringArrayAttributedValuesType）](children-arrayofstringarrayattributedvaluestype.md)  | [学校](schools.md)  | [业余爱好](hobbies.md)  | [WeddingAnniversaries](weddinganniversaries.md)  | [生日](birthdays.md)  | [位置](locations.md)  | [ExtendedProperties （ArrayOfExtendedPropertyAttributedValueType）](extendedproperties-arrayofextendedpropertyattributedvaluetype.md)</span><span class="sxs-lookup"><span data-stu-id="2ea25-111">[PersonaId](personaid.md) | [PersonaType](personatype.md) | [PersonaObjectStatus](personaobjectstatus.md) | [CreationTime](creationtime.md) | [Bodies](bodies.md) | [DisplayNameFirstLastSortKey](displaynamefirstlastsortkey.md) | [DisplayNameLastFirstSortKey](displaynamelastfirstsortkey.md) | [CompanyNameSortKey](companynamesortkey.md) | [HomeCitySortKey](homecitysortkey.md) | [WorkCitySortKey](workcitysortkey.md) | [DisplayNameFirstLastHeader](displaynamefirstlastheader.md) | [DisplayNameLastFirstHeader](displaynamelastfirstheader.md) | [FileAsHeader](fileasheader.md) | [DisplayName (string)](displayname-string.md) | [DisplayNameFirstLast](displaynamefirstlast.md) | [DisplayNameLastFirst](displaynamelastfirst.md) | [FileAs](fileas.md) | [FileAsId](fileasid.md) | [DisplayNamePrefix](displaynameprefix.md) | [GivenName](givenname.md) | [MiddleName](middlename.md) | [Surname](surname.md) | [Generation](generation.md) | [Nickname](nickname.md) | [YomiCompanyName](yomicompanyname.md) | [YomiFirstName](yomifirstname.md) | [YomiLastName](yomilastname.md) | [Title](title.md) | [Department](department.md) | [CompanyName](companyname.md) | [Location](location.md) | [EmailAddress (EmailAddressType)](emailaddress-emailaddresstype.md) | [EmailAddresses (ArrayOfEmailAddressesType)](emailaddresses-arrayofemailaddressestype.md) | [PhoneNumber](phonenumber.md) | [ImAddress (String)](imaddress-string.md) | [HomeCity](homecity.md) | [WorkCity](workcity.md) | [RelevanceScore](relevancescore.md) | [FolderIds (ArrayOfFolderIdType)](folderids-arrayoffolderidtype.md) | [Attributions (ArrayOfPersonaAttributionsType)](attributions-arrayofpersonaattributionstype.md) | [DisplayNames](displaynames.md) | [FileAses](fileases.md) | [FileAsIds](fileasids.md) | [DisplayNamePrefixes](displaynameprefixes.md) | [GivenNames](givennames.md) | [MiddleNames](middlenames.md) | [Surnames](surnames.md) | [Generations](generations.md) | [Nicknames](nicknames.md) | [Initials (ArrayOfStringAttributedValuesType)](initials-arrayofstringattributedvaluestype.md) | [YomiCompanyNames](yomicompanynames.md) | [YomiFirstNames](yomifirstnames.md) | [YomiLastNames](yomilastnames.md) | [BusinessPhoneNumbers](businessphonenumbers.md) | [BusinessPhoneNumbers2](businessphonenumbers2.md) | [HomePhones](homephones.md) | [HomePhones2](homephones2.md) | [MobilePhones](mobilephones.md) | [MobilePhones2](mobilephones2.md) | [AssistantPhoneNumbers](assistantphonenumbers.md) | [CallbackPhones](callbackphones.md) | [CarPhones](carphones.md) | [HomeFaxes](homefaxes.md) | [OrganizationMainPhones](organizationmainphones.md) | [OtherFaxes](otherfaxes.md) | [OtherTelephones](othertelephones.md) | [OtherPhones2](otherphones2.md) | [Pagers](pagers.md) | [RadioPhones](radiophones.md) | [TelexNumbers](telexnumbers.md) | [TTYTDDPhoneNumbers](ttytddphonenumbers.md) | [WorkFaxes](workfaxes.md) | [Emails1](emails1.md) | [Emails2](emails2.md) | [Emails3](emails3.md) | [BusinessHomePages](businesshomepages.md) | [PersonalHomePages](personalhomepages.md) | [OfficeLocations](officelocations.md) | [ImAddresses (ArrayOfStringAttributedValuesType)](imaddresses-arrayofstringattributedvaluestype.md) | [ImAddresses2](imaddresses2.md) | [ImAddresses3](imaddresses3.md) | [BusinessAddresses](businessaddresses.md) | [HomeAddresses](homeaddresses.md) | [OtherAddresses](otheraddresses.md) | [Titles](titles.md) | [Departments](departments.md) | [CompanyNames](companynames.md) | [Managers](managers.md) | [AssistantNames](assistantnames.md) | [Professions](professions.md) | [SpouseNames](spousenames.md) | [Children (ArrayOfStringArrayAttributedValuesType)](children-arrayofstringarrayattributedvaluestype.md) | [Schools](schools.md) | [Hobbies](hobbies.md) | [WeddingAnniversaries](weddinganniversaries.md) | [Birthdays](birthdays.md) | [Locations](locations.md) | [ExtendedProperties (ArrayOfExtendedPropertyAttributedValueType)](extendedproperties-arrayofextendedpropertyattributedvaluetype.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2ea25-112">父元素</span><span class="sxs-lookup"><span data-stu-id="2ea25-112">Parent elements</span></span>

<span data-ttu-id="2ea25-113">[AddNewImContactToGroupResponse](addnewimcontacttogroupresponse.md)  | [AddNewTelUriContactToGroupResponse](addnewteluricontacttogroupresponse.md)  | [GetPersonaResponseMessage](getpersonaresponsemessage.md)  | [人员](people.md)  | [角色](personas-ex15websvcsotherref.md)</span><span class="sxs-lookup"><span data-stu-id="2ea25-113">[AddNewImContactToGroupResponse](addnewimcontacttogroupresponse.md) | [AddNewTelUriContactToGroupResponse](addnewteluricontacttogroupresponse.md) | [GetPersonaResponseMessage](getpersonaresponsemessage.md) | [People](people.md) | [Personas](personas-ex15websvcsotherref.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2ea25-114">备注</span><span class="sxs-lookup"><span data-stu-id="2ea25-114">Remarks</span></span>

<span data-ttu-id="2ea25-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="2ea25-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2ea25-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2ea25-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2ea25-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="2ea25-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2ea25-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="2ea25-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2ea25-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="2ea25-119">Schema name</span></span>  <br/> |<span data-ttu-id="2ea25-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="2ea25-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2ea25-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="2ea25-121">Validation file</span></span>  <br/> |<span data-ttu-id="2ea25-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2ea25-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2ea25-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="2ea25-123">Can be empty</span></span>  <br/> |<span data-ttu-id="2ea25-124">false</span><span class="sxs-lookup"><span data-stu-id="2ea25-124">false</span></span>  <br/> |
   

