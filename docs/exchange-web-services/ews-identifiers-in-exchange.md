---
title: Exchange 中的 EWS 标识符
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 39b6b20b-e081-4347-9e15-9b8cf829fdf0
description: 了解 Exchange 中的标识符以及如何在 EWS 托管 API 和 EWS 应用程序中使用它们。
localization_priority: Priority
ms.openlocfilehash: 9fa2e31a3c67b0b4291b1e3f32a775655e2bf80a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528424"
---
# <a name="ews-identifiers-in-exchange"></a>Exchange 中的 EWS 标识符

了解 Exchange 中的标识符以及如何在 EWS 托管 API 和 EWS 应用程序中使用它们。
  
Exchange 存储中的每个对象都有一个唯一的标识符。 您可以使用对象的标识符引用该对象，并将其与其他对象进行区分。 您可以使用的两个最常见的标识符是文件夹和项目标识符。 
  
为了了解标识符以及它们对您的应用程序的重要性，了解 Exchange 中的对象之间的关系非常有用。 当您的 EWS 托管 API 或 EWS 应用程序与 Exchange 进行通信时，您可以使用包含邮箱、文件夹和项目对象的对象层次结构。 一个存储区可以是这些对象类型中的任何一种。 通常情况下，它是 Exchange 服务器上的邮箱，但也可以是 Exchange 服务器上的公用文件夹。 （请注意，在 Exchange Online 中，作为 Office 365 的一部分的 exchange Online 和从 Exchange 2013 开始的 Exchange 版本中，公用文件夹只是另一种类型的邮箱，而不是其他类型的存储。存储区包含文件夹，文件夹包含项目，其中每个文件夹和项目都具有标识符，如下图所示。 
  
**图1。邮箱、文件夹和项目层次结构**

![此插图显示邮箱对象的层次结构。邮箱在最顶层，下一层是收件箱文件夹。该图显示了一个包含电子邮件的文件夹。标识符和更改密钥已针对每个对象列出，并进行了缩短。](media/Ex15_Identifier_diagram.png)
  
## <a name="ews-identifiers"></a>EWS 标识符
<a name="bk_CommonIdentifiers"> </a>

EWS 对文件夹和项目使用的标识符称为 EWS 标识符或 EwsIds。 EwsIds 可在 EWS 中的许多不同对象中找到，但对于不同的对象，它们被称为不同的对象。 由于您可以在应用程序中使用这些对象，因此您需要了解这些对象的标识符与 EwsId 的关系。 
  
EWS 中的标识符也适用于 EWS 托管 API。 在 EWS 托管 API 中，标识符是对象的属性，并在内部进行管理以映射到 EWS 元素。
  
**表1。EWS 中的对象标识符**

|**Object**|**标识符**|**它与 EwsId 有何关系？**|
|:-----|:-----|:-----|
|[CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) <br/> |[ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)子元素包含日历项目的唯一标识符。  <br/> |[ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)子元素与此项的 EwsId 相同。  <br/> |
|[ConversationId](https://msdn.microsoft.com/library/d5f1ddb3-9af3-4677-a6ba-111b304a951e%28Office.15%29.aspx) <br/> |**Id**属性包含此项目所属的会话的标识符。  <br/> |**Id**属性与此项的 EwsId 相同。  <br/> |
|[AttachmentId](https://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) <br/> |提供附件的唯一标识符。 [RootItemId](https://msdn.microsoft.com/library/f613c705-17ce-48ce-aa64-4dc2cea25e31%28Office.15%29.aspx)属性包含附件所附加到的根存储项的唯一标识符。  <br/> |附件可以是 Exchange 存储中的其他项目，在这种情况下， [AttachmentId](https://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx)与 EwsId 相同。 在所有情况下， [RootItemId](https://msdn.microsoft.com/library/f613c705-17ce-48ce-aa64-4dc2cea25e31%28Office.15%29.aspx)都是 EwsId，因为它引用存储中的项目。  <br/> |
|[PersonaId](https://msdn.microsoft.com/library/eec3a468-afd5-4d72-a61e-cd1964fb686c%28Office.15%29.aspx) <br/> |**Id**属性返回一个字符串，其中包含角色的标识符。  <br/> |**Id**属性与角色的 EwsId 相同。  <br/> |
|[ContactId](https://msdn.microsoft.com/library/86f66275-1e39-48ed-bd89-ac3bffc465a7%28Office.15%29.aspx) <br/> |**Id**属性返回一个包含联系人标识符的字符串。  <br/> |**Id**属性与联系人的 EwsId 相同。  <br/> |
|[GroupId](https://msdn.microsoft.com/library/656d9b9a-8a65-4a75-8466-5b0d96512dab%28Office.15%29.aspx) <br/> |**Id**属性返回一个字符串，其中包含组的标识符。  <br/> |**Id**属性与组的 EwsId 相同。  <br/> |
|[AssociatedCalendarItemId](https://msdn.microsoft.com/library/5b29898c-ea59-4e6a-914c-c011ec754032%28Office.15%29.aspx) <br/> |**Id**属性标识与[MeetingMessage](https://msdn.microsoft.com/library/c95956a8-7505-44b4-bea4-11d1f5182796%28Office.15%29.aspx)、 [MeetingRequest](https://msdn.microsoft.com/library/c44f8804-a355-473d-a837-48cc91617251%28Office.15%29.aspx)、 [MeetingResponse](https://msdn.microsoft.com/library/9f798e79-dafd-4d4d-9967-95fd8e5c0502%28Office.15%29.aspx)或[MeetingCancellation](https://msdn.microsoft.com/library/a9c61f7f-2ecd-4b21-9dce-24d9f61aeeea%28Office.15%29.aspx)相关联的日历项目。  <br/> |**Id**属性与日历项目的 EwsId 相同。  <br/> |
|[UserConfigurationProperties](https://msdn.microsoft.com/library/c143a6ec-62ad-4d48-b844-b1ad88054bc1%28Office.15%29.aspx) <br/> |此元素的**Id**值指定了标识符属性。  <br/> |此标识符不直接映射到 EwsId，因为它是一个属性标识符，而不是一个项目。  <br/> |
|[OccurrenceItemId](https://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) <br/> |**RecurringMasterId**属性标识定期项目的主控形状。  <br/> |**OccurrenceItemId**值不直接映射到 EwsId，而是由于它引用定期项目的顶级对象而**RecurringMasterId** 。  <br/> |
|[StoreEntryId](https://msdn.microsoft.com/library/f536e264-8c4d-4cc5-bab8-22a4fa38de39%28Office.15%29.aspx) <br/> |包含项目的 Exchange 存储标识符。  <br/> |**StoreEntryId**值不映射到 EwsId，但它确实提供保存项的存储区的标识符。  <br/> |
   
## <a name="working-with-identifiers"></a>使用标识符
<a name="bk_WorkingWithIdentifiers"> </a>

Exchange 服务器以多种不同的方式处理标识符。 在开发 EWS 托管 API 或 EWS 应用程序时，请考虑以下几点：
  
- 文件夹和项目的**ItemID**元素值区分大小写。 如果您查看[FindItem 操作](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)（或[FINDITEMS](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) EWS 托管 API 方法）返回的文件夹或项目的项目 ID，您可能会认为它与另一个项目 id 重复;但是，这两个项目的项目 Id 中的一个或多个字符将具有不同的大小写。 
    
- 如果要将项目 ID 存储在数据库中以供以后检索，建议将字段大小设为512字节，使其足够大以容纳 GUID。
    
- 不要假设您的项目 ID 将始终有效，前提是您需要稍后检索该项目。 如果将某个项目移动到存储区中，则该 ID 会因处理移动的方式而变化。 实际复制一个项目，并生成一个新的 ID，然后[删除原始项目](deleting-items-by-using-ews-in-exchange.md)。 请注意，文件夹 Id 是不可变的，并且在应用商店中移动时不会更改。
    
- Exchange 中的标识符是不透明的。 例如，EwsId 是从一些信息中创建的，这些信息并不像开发人员那样重要，但对 Exchange 很重要。
    
- 当您使用 Exchange 中的项目时，另一个要记住的值是**ChangeKey**属性。 除项目 ID 之外，此值还用于跟踪项的状态。 任何时候更改项目时，都会生成新的更改密钥。 例如，在执行[UpdateItem 操作](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)时，可以使用**ChangeKey**属性让服务器知道您的更新将应用于项目的最新版本。 如果另一个应用程序对要更新的项目进行了更改，则更改密钥将不匹配，并且您将无法执行更新。 
    
## <a name="distinguished-folder-ids"></a>可分辨文件夹 Id
<a name="bk_DistinguishedFolderIds"> </a>

Exchange 包含许多预定义邮箱文件夹，每个文件夹都分配有一个标识符，称为可分辨文件夹 ID。 这些由[WellKnownFolderName](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) EWS 托管 API 枚举和[DistinguishedFolderId](https://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) EWS 元素定义。 可以使用这些可分辨文件夹 Id 更轻松地引用其中一个预定义的文件夹。 例如，对于 "收件箱" 文件夹，您可以简单地将 "收件箱" 用于标识符，而不是确定文件夹标识符。 
  
您创建的用于组织电子邮件项目的其他文件夹也具有该文件夹独有的 ID。 即使您更改了该文件夹的其他属性，该 ID 也不会更改。
  
可以使用可分辨文件夹 Id 作为代理访问的入口点。 当您启动代理访问时，您可以搜索项目或文件夹，并提供可分辨文件夹 ID 以指定搜索的位置。 当代理用户访问服务器时，将使用一个[邮箱](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx)元素作为**DistinguishedFolderId**元素的子元素，以明确指定要访问的代理的邮箱。 
  
## <a name="handling-errors"></a>处理错误
<a name="bk_DealingWithErrors"> </a>

每个程序都绑定到 "立即" 每隔一个错误，而基于 EWS 的应用程序则不会出现异常（pun）。 您可能会在[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) ews 元素中或作为[SERVICEERROR](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.serviceerror%28v=exchg.80%29.aspx) EWS 托管 API 枚举的一部分收到一些与标识符相关的错误。 
  
在 EWS 托管 API 或 EWS 应用程序中可能会发生以下错误。 如果您正在使用 EWS 托管 API 应用程序，则这些错误通常是属性值的问题;对于 EWS 应用程序，错误与 XML 元素值或操作相关联。
  
**表2。与标识符相关的错误**

|**Error**|**时发生 .。。**|**说明**|
|:-----|:-----|:-----|
|ErrorCalendarCannotUseIdForOccurrenceId  <br/> |**OccurenceID**的值不对应于有效的定期日历项目。  <br/> |在请求中指定的**OccurenceId**的值可能在结构中有效，但请求无法将其与现有的定期主服务器匹配。 定期项目可能会从日历中删除。 验证该项目是否仍然存在以及是否使用了正确的标识符。  <br/> |
|ErrorCalendarCannotUseIdForRecurringMasterId  <br/> |**RecurringMasterId**属性与**OccurrenceId**元素的有效匹配项不对应。  <br/> |在请求中指定的**RecurringMasterId**的值可能在结构中有效，但请求无法将其与项目的现有匹配项相匹配。 项目的出现可能会从日历中删除。 验证该项目是否仍然存在以及是否使用了正确的标识符。  <br/> |
|ErrorCannotUseFolderIdForItemId  <br/> |传递的**ID**代表一个文件夹，而不是一个项目。  <br/> |标识符的格式可能是有效的，但不是服务器预期的操作的目标。 确认您引用的是正确的操作标识符。  <br/> |
|ErrorCannotUseItemIdForFolderId  <br/> |传入的**ID**代表项目而不是文件夹。  <br/> |标识符的格式可能是有效的，但不是服务器预期的操作的目标。 确认您引用的是正确的操作**ID** 。  <br/> |
|ErrorChangeKeyRequiredForWriteOperations  <br/> |执行某些更新操作时必须提供有效的更改密钥。  <br/> |您在请求更新时省略了**ChangeKey**值，或者更改键不正确。 在执行更新操作时，请验证您是否具有正确的更改密钥。  <br/> |
|ErrorInvalidAttachmentId  <br/> |在项目的附件集合中找不到附件。  <br/> |如果你有附件**id** ，然后删除了附件并尝试在附件 id 上调用[GetAttachment 操作](https://msdn.microsoft.com/library/24d10a15-b942-415e-9024-a6375708f326%28Office.15%29.aspx)，则可能会收到此响应代码。 验证附件集合中是否存在附件。  <br/> |
|ErrorInvalidChangeKey  <br/> |传入了无效的更改密钥。  <br/> |请注意，许多操作和方法不需要传递更改密钥。 但是，如果您确实提供了更改密钥，则它必须有效，尽管它并不一定必须是最新的。  <br/> |
|ErrorInvalidFolderId  <br/> |文件夹**ID**已损坏。  <br/> |请确保您的标识符格式正确且有效。  <br/> |
|ErrorInvalidId  <br/> |**ID**和/或更改键的结构在内部不一致。  <br/> |在分析后，Exchange 遇到**ID**问题。 转换过程中可能存在错误。 例如，如果您在 Outlook 中有一个项目的**IdFormatType** ，但您将其转换为**IdFormatType**格式的 EwsId，则可能会发生这种情况。 请确保使用正确的转换类型。  <br/> |
|ErrorInvalidIdEmpty  <br/> |应用程序指定了一个为空的**ID** 。  <br/> |您的应用程序在标识符的空字符串中传递。 请确保您的标识符格式正确且有效。  <br/> |
|ErrorInvalidIdMalformed  <br/> |**ID**的结构在内部不一致。  <br/> |在分析后，Exchange 遇到**ID**问题。 该 ID 可能未正确转换。 请确保使用正确的转换类型。  <br/> |
|ErrorInvalidIdMalformedEwsLegacyIdFormat  <br/> |为具有 Exchange 2007 SP1 版本或更高版本的请求指定了使用 Exchange 2007 格式的文件夹或项目**ID** 。  <br/> |您不能在 Exchange 2007 SP1 或更高版本请求中使用 Exchange 2007 Id。 必须使用[ConvertId](https://msdn.microsoft.com/library/47d96cf6-9e2f-4fc0-9682-7258d3fbf918%28Office.15%29.aspx) ews 操作或[CONVERTID](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.convertid%28v=exchg.80%29.aspx) ews 托管 API 方法先转换它们。  <br/> |
|ErrorInvalidIdNotAnItemAttachmentId  <br/> |**AttachmentId**属性不引用项目附件。  <br/> |标识符的格式可能是有效的，但不是服务器预期的操作的目标。 确认您引用的是正确的操作标识符。  <br/> |
|ErrorInvalidIdReturnedByResolveNames  <br/> |邮箱中的联系人已损坏。  <br/> |[ResolveNames](https://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) ews 操作或[RESOLVENAME](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) ews 托管 API 方法返回一个或多个标识符，但它们无效。 您可能需要重新创建该联系人。  <br/> |
|ErrorInvalidIdStoreObjectIdTooLong  <br/> |**ID**的结构在内部不一致。  <br/> |在分析后，Exchange 遇到**ID**问题。 该**ID**可能未正确转换。 请确保使用正确的转换类型。  <br/> |
|ErrorInvalidIdTooManyAttachmentLevels  <br/> |附件层次结构超过了最大值（深度为255层）。  <br/> |在请求中指定的**AttachmentId**属性的值可能在结构中有效，但请求的附件在层次结构中太深。 您的代码可能已尝试附加超出255级别限制的项。  <br/> |
|ErrorInvalidImContactId  <br/> |当您使用[RemoveImContactFromGroup 操作](https://msdn.microsoft.com/library/a190bbec-c71b-4e6a-880b-55854c724d8c%28Office.15%29.aspx)时，在 IM 组中找不到联系人时，可能会返回此错误。 此错误适用于面向 Exchange Online 的客户端和从 Exchange 2013 开始的 Exchange 版本。  <br/> |在请求中指定的**ContactId**属性的值可能在结构中有效，但邮箱中的联系人与此结构不匹配。 该联系人可能已被删除。  <br/> |
|ErrorInvalidImGroupId  <br/> |当您使用[RemoveImGroup 操作](https://msdn.microsoft.com/library/5e788016-68e0-4a3f-9243-03f6b6c6b389%28Office.15%29.aspx)时，在邮箱中找不到该组时，可能会返回此错误。 此错误适用于面向 Exchange Online 的客户端和从 Exchange 2013 开始的 Exchange 版本。  <br/> |在请求中指定的**GroupId**属性值可能在结构中有效，但邮箱中没有与此结构匹配的组。 该组可能已被删除。  <br/> |
|ErrorInvalidReferenceItem  <br/> |引用的项标识符不是**MessageType**或 CalendarItemTypeType，也不是其一个后代的**ExchangeWebServices**。 引用项目标识符适用于**CalendarItemType**对象，并且组织者正在尝试答复或 ReplyAll。  <br/> |标识符的格式可能是有效的，但不是服务器预期的操作的目标。 确认您引用的是正确的操作标识符。  <br/> |
|ErrorMissingManagedFolderId  <br/> |缺少文件夹的策略 Id 属性，property 标记0x6732。  <br/> |文件夹已损坏。 请考虑重新创建它。  <br/> |
   
## <a name="converting-identifiers"></a>转换标识符
<a name="bk_ConvertingIdentifiers"> </a>

您可能需要将标识符从一种格式转换为另一种格式。 例如，您可能需要将来自外部 EWS 的标识符（如来自 MAPI 连接的标识符）转换为您的应用程序可以使用的格式。 若要执行此操作，您可以使用[ConvertId](https://msdn.microsoft.com/library/47d96cf6-9e2f-4fc0-9682-7258d3fbf918%28Office.15%29.aspx) ews 操作或[CONVERTID](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.convertid%28v=exchg.80%29.aspx) ews 托管 API 方法。 
  
例如，在保存项目时，EntryID 是由存储分配的 MAPI 邮件存储生成的唯一标识符。 若要在应用程序中使用 EntryID，首先需要将其转换为 EwsId。 
  
Outlook Web App 使用其自己的标识符版本（称为 "OwaId"），在 Url 中访问文件夹和项目。 如果您的应用程序需要访问 Outlook Web App 中的项，则需要将 OwaId 转换为 EwsId。
  
您可以使用**ConvertId**操作或方法来转换几种不同的标识符格式。 
  
**表3。Exchange 中的可转换标识符格式**

|**格式**|**描述**|
|:-----|:-----|
|EwsLegacyId  <br/> |适用于 Exchange 2007 的 EwsId。  <br/> |
|EwsId  <br/> |适用于 Exchange Online 和从 Exchange 2007 SP1 开始的 Exchange 版本的 EwsId。  <br/> |
|StoreId  <br/> |存储文件夹和项目的 Exchange 存储标识符。  <br/> |
|OwaId  <br/> |Outlook web app 标识符用于 Exchange 2007 和 Exchange 2010 中的 outlook web app。 <br/><br/>**注意**：从 exchange 2013 开始的 exchange Online 和 exchange 版本使用适用于 Outlook Web App 的 EwsId。           |
|EntryId  <br/> |MAPI 标识符，通常称为 MAPI 邮件的 " **PR_ENTRYID** " 属性。  <br/> |
|HexEntryId  <br/> |用于可用性日历事件标识符的**PR_ENTRYID**属性的十六进制编码表示形式。 这也是 Outlook 使用的标识符格式。  <br/> |
   
## <a name="see-also"></a>另请参阅

- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)  
- [ConvertId 操作](https://msdn.microsoft.com/library/47d96cf6-9e2f-4fc0-9682-7258d3fbf918%28Office.15%29.aspx)  
- [ServiceError 枚举](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.serviceerror%28v=exchg.80%29.aspx) 
- [使用 Exchange 中的 EWS 删除项目](deleting-items-by-using-ews-in-exchange.md)
    

