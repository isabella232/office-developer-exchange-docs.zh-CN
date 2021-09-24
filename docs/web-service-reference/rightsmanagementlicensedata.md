---
title: RightsManagementLicenseData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 38f0b7f4-2338-4e90-af67-e0951e8edfa3
description: RightsManagementLicenseData 元素指定有关项目权限管理许可证的信息。
ms.openlocfilehash: 8875e9bad425224f86b6de5149f87a36c2a2581e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523466"
---
# <a name="rightsmanagementlicensedata"></a>RightsManagementLicenseData

**RightsManagementLicenseData** 元素指定有关项目权限管理许可证的信息。 
  
```XML
<RightsManagementLicenseData>
   <RightsManagedMessageDecryptionStatus/>
   <RmsTemplateId/>
   <TemplateName/>
   <TemplateDescription/>
   <EditAllowed/>
   <ReplyAllowed/>
   <ReplyAllAllowed/>
   <ForwardAllowed/>
   <ModifyRecipientsAllowed/>
   <ExtractAllowed/>
   <PrintAllowed/>
   <ExportAllowed/>
   <ProgrammaticAccessAllowed/>
   <IsOwner/>
   <ContentOwner/>
   <ContentExpiryDate/>
</RightsManagementLicenseData>
```

 **RightsManagementLicenseDataType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

[RightsManagedMessageDecryptionStatus](rightsmanagedmessagedecryptionstatus.md)  | [RMSTemplateId](rmstemplateid.md)  | [TemplateName](templatename.md)  | [TemplateDescription](templatedescription.md)  | [EditAllowed](editallowed.md)  | [ReplyAllowed](replyallowed.md)  | [ReplyAllAllowed](replyallallowed.md)  | [ForwardAllowed](forwardallowed.md)  | [ModifyRecipientsAllowed](modifyrecipientsallowed.md)  | [ExtractAllowed](extractallowed.md)  | [PrintAllowed](printallowed.md)  | [ExportAllowed](exportallowed.md)  | [ProgrammaticAccessAllowed](programmaticaccessallowed.md)  | [IsOwner](isowner.md)  | [ContentOwner](contentowner.md)  | [ContentExpiryDate](contentexpirydate.md)
  
### <a name="parent-elements"></a>父元素

[Item](item.md)  | [邮件](message-ex15websvcsotherref.md)  | [MeetingMessage](meetingmessage.md)  | [MeetingRequest](meetingrequest.md)  | [MeetingResponse](meetingresponse.md)  | [MeetingCancellation](meetingcancellation.md)  | [任务](task.md)  | [PostItem](postitem.md)  | [CalendarItem](calendaritem.md)  | [联系人](contact.md)  | [DistributionList](distributionlist.md)
  
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> ||
   

