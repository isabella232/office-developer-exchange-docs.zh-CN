---
title: Persona
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: b115c990-3a2d-4536-9af3-ac1fd06d00dc
description: Persona 元素指定由 GetPersona 请求返回的一组 persona 数据。
ms.openlocfilehash: 0bbab94b7767b19a3b27bd240151c2abd42f3e6f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519238"
---
# <a name="persona"></a>Persona

**Persona** 元素指定由 **GetPersona** 请求返回的一组 persona 数据。 
  
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

 **PersonaType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

[PersonaId](personaid.md)  | [PersonaType](personatype.md)  | [PersonaObjectStatus](personaobjectstatus.md)  | [CreationTime](creationtime.md)  | [主体](bodies.md)  | [DisplayNameFirstLastSortKey](displaynamefirstlastsortkey.md)  | [DisplayNameLastFirstSortKey](displaynamelastfirstsortkey.md)  | [CompanyNameSortKey](companynamesortkey.md)  | [HomeCitySortKey](homecitysortkey.md)  | [WorkCitySortKey](workcitysortkey.md)  | [DisplayNameFirstLastHeader](displaynamefirstlastheader.md)  | [DisplayNameLastFirstHeader](displaynamelastfirstheader.md)  | [FileAsHeader](fileasheader.md)  | [DisplayName (字符串) ](displayname-string.md)  | [DisplayNameFirstLast](displaynamefirstlast.md)  | [DisplayNameLastFirst](displaynamelastfirst.md)  | [FileAs](fileas.md)  | [FileAsId](fileasid.md)  | [DisplayNamePrefix](displaynameprefix.md)  | [GivenName](givenname.md)  | [MiddleName](middlename.md)  | [Surname](surname.md)  | [生成](generation.md)  | [Nickname](nickname.md)  | [YomiCompanyName](yomicompanyname.md)  | [YomiFirstName](yomifirstname.md)  | [YomiLastName](yomilastname.md)  | [标题](title.md)  | [部门](department.md)  | [CompanyName](companyname.md)  | [位置](location.md)  | [EmailAddress (EmailAddressType) ](emailaddress-emailaddresstype.md)  | [EmailAddresses (ArrayOfEmailAddressesType) ](emailaddresses-arrayofemailaddressestype.md)  | [PhoneNumber](phonenumber.md)  | [ImAddress (String) ](imaddress-string.md)  | [HomeCity](homecity.md)  | [WorkCity](workcity.md)  | [RelevanceScore](relevancescore.md)  | [FolderIds (ArrayOfFolderIdType) ](folderids-arrayoffolderidtype.md)  | [ArrayOfPersonaAttributionsType () ](attributions-arrayofpersonaattributionstype.md)  |  属性[DisplayNames](displaynames.md)  | [FileAses](fileases.md)  | [FileAsIds](fileasids.md)  | [DisplayNamePrefixes](displaynameprefixes.md)  | [GivenNames](givennames.md)  | [MiddleNames](middlenames.md)  | [姓](surnames.md)  | [代数](generations.md)  | [昵称](nicknames.md)  | [ArrayOfStringAttributedValuesType (的缩写) ](initials-arrayofstringattributedvaluestype.md)  | [YomiCompanyNames](yomicompanynames.md)  | [YomiFirstNames](yomifirstnames.md)  | [YomiLastNames](yomilastnames.md)  | [BusinessPhoneNumbers](businessphonenumbers.md)  | [BusinessPhoneNumbers2](businessphonenumbers2.md)  | [HomePhones](homephones.md)  | [HomePhones2](homephones2.md)  | [MobilePhones](mobilephones.md)  | [MobilePhones2](mobilephones2.md)  | [AssistantPhoneNumbers](assistantphonenumbers.md)  | [CallbackPhones](callbackphones.md)  | [CarPhones](carphones.md)  | [HomeFaxes](homefaxes.md)  | [OrganizationMainPhones](organizationmainphones.md)  | [OtherFaxes](otherfaxes.md)  | [OtherTelephones](othertelephones.md)  | [OtherPhones2](otherphones2.md)  | [寻呼机](pagers.md)  | [RadioPhones](radiophones.md)  | [TelexNumbers](telexnumbers.md)  | [TTYTDDPhoneNumbers](ttytddphonenumbers.md)  | [WorkFaxes](workfaxes.md)  | [Emails1](emails1.md)  | [Emails2](emails2.md)  | [Emails3](emails3.md)  | [BusinessHomePages](businesshomepages.md)  | [PersonalHomePages](personalhomepages.md)  | [OfficeLocations](officelocations.md)  | [ImAddresses (ArrayOfStringAttributedValuesType) ](imaddresses-arrayofstringattributedvaluestype.md)  | [ImAddresses2](imaddresses2.md)  | [ImAddresses3](imaddresses3.md)  | [BusinessAddresses](businessaddresses.md)  | [HomeAddresses](homeaddresses.md)  | [OtherAddresses](otheraddresses.md)  | [标题](titles.md)  | [部门](departments.md)  | [CompanyNames](companynames.md)  | [经理](managers.md)  | [AssistantNames](assistantnames.md)  | [专业](professions.md)  | [SpouseNames](spousenames.md)  | [ (ArrayOfStringArrayAttributedValuesType 属性的子) ](children-arrayofstringarrayattributedvaluestype.md)  | [学校](schools.md)  | [爱好](hobbies.md)  | [AriesAnniversaries](weddinganniversaries.md)  | [生日](birthdays.md)  | [位置](locations.md)  | [ExtendedProperties (ArrayOfExtendedPropertyAttributedValueType) ](extendedproperties-arrayofextendedpropertyattributedvaluetype.md)
  
### <a name="parent-elements"></a>父元素

[AddNewImContactToGroupResponse](addnewimcontacttogroupresponse.md)  | [AddNewTelUriContactToGroupResponse](addnewteluricontacttogroupresponse.md)  | [GetPersonaResponseMessage](getpersonaresponsemessage.md)  | [人员](people.md)  | [角色](personas-ex15websvcsotherref.md)
  
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |false  <br/> |
   

