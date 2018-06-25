---
title: RightsManagementLicenseData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 38f0b7f4-2338-4e90-af67-e0951e8edfa3
description: RightsManagementLicenseData 元素指定有关项目的权限管理许可证信息。
ms.openlocfilehash: ec2ba1dc155afe239c499246095f86fc621910a9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827234"
---
# <a name="rightsmanagementlicensedata"></a><span data-ttu-id="239f3-103">RightsManagementLicenseData</span><span class="sxs-lookup"><span data-stu-id="239f3-103">RightsManagementLicenseData</span></span>

<span data-ttu-id="239f3-104">**RightsManagementLicenseData**元素指定有关项目的权限管理许可证信息。</span><span class="sxs-lookup"><span data-stu-id="239f3-104">The **RightsManagementLicenseData** element specifies information about the rights management license for an item.</span></span> 
  
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

 <span data-ttu-id="239f3-105">**RightsManagementLicenseDataType**</span><span class="sxs-lookup"><span data-stu-id="239f3-105">**RightsManagementLicenseDataType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="239f3-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="239f3-106">Attributes and elements</span></span>

<span data-ttu-id="239f3-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="239f3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="239f3-108">属性</span><span class="sxs-lookup"><span data-stu-id="239f3-108">Attributes</span></span>

<span data-ttu-id="239f3-109">无。</span><span class="sxs-lookup"><span data-stu-id="239f3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="239f3-110">子元素</span><span class="sxs-lookup"><span data-stu-id="239f3-110">Child elements</span></span>

<span data-ttu-id="239f3-111">[RightsManagedMessageDecryptionStatus](rightsmanagedmessagedecryptionstatus.md) | [RMSTemplateId](rmstemplateid.md) | [TemplateName](templatename.md) | [TemplateDescription](templatedescription.md) | [EditAllowed](editallowed.md) | [ReplyAllowed](replyallowed.md)  |  [ReplyAllAllowed](replyallallowed.md) | [ForwardAllowed](forwardallowed.md) | [ModifyRecipientsAllowed](modifyrecipientsallowed.md) | [ExtractAllowed](extractallowed.md) | [PrintAllowed](printallowed.md) | [ExportAllowed](exportallowed.md)  |  [ProgrammaticAccessAllowed](programmaticaccessallowed.md) | [IsOwner](isowner.md) | [ContentOwner](contentowner.md) | [ContentExpiryDate](contentexpirydate.md)</span><span class="sxs-lookup"><span data-stu-id="239f3-111">[RightsManagedMessageDecryptionStatus](rightsmanagedmessagedecryptionstatus.md) | [RMSTemplateId](rmstemplateid.md) | [TemplateName](templatename.md) | [TemplateDescription](templatedescription.md) | [EditAllowed](editallowed.md) | [ReplyAllowed](replyallowed.md) | [ReplyAllAllowed](replyallallowed.md) | [ForwardAllowed](forwardallowed.md) | [ModifyRecipientsAllowed](modifyrecipientsallowed.md) | [ExtractAllowed](extractallowed.md) | [PrintAllowed](printallowed.md) | [ExportAllowed](exportallowed.md) | [ProgrammaticAccessAllowed](programmaticaccessallowed.md) | [IsOwner](isowner.md) | [ContentOwner](contentowner.md) | [ContentExpiryDate](contentexpirydate.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="239f3-112">父元素</span><span class="sxs-lookup"><span data-stu-id="239f3-112">Parent elements</span></span>

<span data-ttu-id="239f3-113">[项目](item.md) | [消息](message-ex15websvcsotherref.md) | [MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md) | [MeetingResponse](meetingresponse.md) | [MeetingCancellation](meetingcancellation.md) | [任务](task.md) | [PostItem](postitem.md)  | [日历项目](calendaritem.md) | [联系人](contact.md) | [DistributionList](distributionlist.md)</span><span class="sxs-lookup"><span data-stu-id="239f3-113">[Item](item.md) | [Message](message-ex15websvcsotherref.md) | [MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md) | [MeetingResponse](meetingresponse.md) | [MeetingCancellation](meetingcancellation.md) | [Task](task.md) | [PostItem](postitem.md) | [CalendarItem](calendaritem.md) | [Contact](contact.md) | [DistributionList](distributionlist.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="239f3-114">备注</span><span class="sxs-lookup"><span data-stu-id="239f3-114">Remarks</span></span>

<span data-ttu-id="239f3-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="239f3-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="239f3-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="239f3-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="239f3-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="239f3-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="239f3-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="239f3-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="239f3-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="239f3-119">Schema name</span></span>  <br/> |<span data-ttu-id="239f3-120">类型架构</span><span class="sxs-lookup"><span data-stu-id="239f3-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="239f3-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="239f3-121">Validation file</span></span>  <br/> |<span data-ttu-id="239f3-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="239f3-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="239f3-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="239f3-123">Can be empty</span></span>  <br/> ||
   

