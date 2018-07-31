---
title: Exchange 中的 EWS 标识符
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 39b6b20b-e081-4347-9e15-9b8cf829fdf0
description: 了解有关 Exchange 和如何您 EWS 托管 API 和 EWS 应用程序中使用它们的标识符。
ms.openlocfilehash: fbf6d7756f73b1c5d345f3b34deeb7ea8a347986
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353971"
---
# <a name="ews-identifiers-in-exchange"></a>Exchange 中的 EWS 标识符

了解有关 Exchange 和如何您 EWS 托管 API 和 EWS 应用程序中使用它们的标识符。
  
Exchange 存储中的每个对象具有唯一标识符。 若要引用对象，并以区别于其他对象，可以使用对象的标识符。 您可能会使用两个最常见标识符是文件夹和项标识符。 
  
若要了解标识符和如何它们对您的应用程序，是有助于在 Exchange 了解对象之间的关系。 与 Exchange，您 EWS 托管 API 或 EWS 应用程序进行通信，您使用对象层次结构，其中包含邮箱、 文件夹和项目对象。 存储可以是任何一种这些对象类型。 大多数情况下，它是在 Exchange 服务器上，邮箱，但也可以是 Exchange 服务器上的公用文件夹。 （请记住，在 Exchange Online，Exchange Online 作为 Office 365 的一部分和版本的 Exchange 开头 Exchange 2013、 公用文件夹是刚其他类型的邮箱和不不同类型的存储）存储区包含文件夹和文件夹中包含的项目，每个这些文件夹和项目都有一个标识符，如下图所示。 
  
**图 1。邮箱、 文件夹和项目层次结构**

![此插图显示邮箱对象的层次结构。邮箱在最顶层，下一层是收件箱文件夹。该图显示了一个包含电子邮件的文件夹。标识符和更改密钥已针对每个对象列出，并进行了缩短。](media/Ex15_Identifier_diagram.png)
  
## <a name="ews-identifiers"></a>EWS 标识符
<a name="bk_CommonIdentifiers"> </a>

EWS 标识符或 EwsIds 称为 EWS 使用文件夹和项目的标识符。 EwsIds 可以找到位于内 EWS，许多不同的对象，但调用其他对于不同的对象。 因为您可能在您的应用程序中使用这些对象，您需要了解 EwsId 这些对象的标识符的关联方式。 
  
EWS 中的标识符是不适用于 EWS 托管 API 以及。 EWS 托管 API 中标识符是对象的属性和内部托管将映射到 EWS 元素。
  
**表 1。EWS 中的对象标识符**

|**对象**|**标示符**|**它与 EwsId 有何关系？**|
|:-----|:-----|:-----|
|[CalendarItem](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) <br/> |[ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)子元素包含的日历项目的唯一标识符。  <br/> |针对此项目 EwsId 相同的[ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)子元素。  <br/> |
|[ConversationId](http://msdn.microsoft.com/library/d5f1ddb3-9af3-4677-a6ba-111b304a951e%28Office.15%29.aspx) <br/> |**Id**属性包含此项是的一部分的会话的标识符。  <br/> |针对此项目 EwsId 相同的**Id**属性。  <br/> |
|[AttachmentId](http://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) <br/> |提供的附件的唯一标识符。 [RootItemId](http://msdn.microsoft.com/library/f613c705-17ce-48ce-aa64-4dc2cea25e31%28Office.15%29.aspx)属性包含附件附加到根存储项的唯一标识符。  <br/> |附件可案例[AttachmentId](http://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx)是 EwsId 相同的 Exchange 存储中的其他项。 在所有情况下， [RootItemId](http://msdn.microsoft.com/library/f613c705-17ce-48ce-aa64-4dc2cea25e31%28Office.15%29.aspx)是 EwsId，因为它引用存储中的项。  <br/> |
|[PersonaId](http://msdn.microsoft.com/library/eec3a468-afd5-4d72-a61e-cd1964fb686c%28Office.15%29.aspx) <br/> |**Id**属性返回一个字符串，包含角色的标识符。  <br/> |为该角色 EwsId 相同的**Id**属性。  <br/> |
|[ContactId](http://msdn.microsoft.com/library/86f66275-1e39-48ed-bd89-ac3bffc465a7%28Office.15%29.aspx) <br/> |**Id**属性返回一个字符串，包含该联系人的标识符。  <br/> |为该联系人 EwsId 相同的**Id**属性。  <br/> |
|[GroupId](http://msdn.microsoft.com/library/656d9b9a-8a65-4a75-8466-5b0d96512dab%28Office.15%29.aspx) <br/> |**Id**属性返回一个字符串，包含组的标识符。  <br/> |组 EwsId 相同的**Id**属性。  <br/> |
|[AssociatedCalendarItemId](http://msdn.microsoft.com/library/5b29898c-ea59-4e6a-914c-c011ec754032%28Office.15%29.aspx) <br/> |**Id**属性标识与[MeetingMessage](http://msdn.microsoft.com/library/c95956a8-7505-44b4-bea4-11d1f5182796%28Office.15%29.aspx)、 [MeetingRequest](http://msdn.microsoft.com/library/c44f8804-a355-473d-a837-48cc91617251%28Office.15%29.aspx)、 [MeetingResponse](http://msdn.microsoft.com/library/9f798e79-dafd-4d4d-9967-95fd8e5c0502%28Office.15%29.aspx)或[MeetingCancellation](http://msdn.microsoft.com/library/a9c61f7f-2ecd-4b21-9dce-24d9f61aeeea%28Office.15%29.aspx)相关联的日历项。  <br/> |对于日历项 EwsId 相同的**Id**属性。  <br/> |
|[UserConfigurationProperties](http://msdn.microsoft.com/library/c143a6ec-62ad-4d48-b844-b1ad88054bc1%28Office.15%29.aspx) <br/> |此元素的**Id**值指定的 identifier 属性。  <br/> |此标识符没有直接映射到 EwsId 以来属性标识符和不项目。  <br/> |
|[OccurrenceItemId](http://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) <br/> |**RecurringMasterId**属性标识定期项目的母的版。  <br/> |**OccurrenceItemId**值不直接映射到 EwsId，但**RecurringMasterId**原因是它引用定期项目的顶级对象。  <br/> |
|[StoreEntryId](http://msdn.microsoft.com/library/f536e264-8c4d-4cc5-bab8-22a4fa38de39%28Office.15%29.aspx) <br/> |包含项目的 Exchange 存储区标识符。  <br/> |**StoreEntryId**值没有映射到 EwsId，但它确实为提供了保留项的位置的存储的标识符。  <br/> |
   
## <a name="working-with-identifiers"></a>使用标识符
<a name="bk_WorkingWithIdentifiers"> </a>

Exchange server 处理大量的不同方法中的标识符。 开发您的 EWS 托管 API 或 EWS 应用程序时，考虑以下事项：
  
- 文件夹和项目的**ItemID**元素值区分大小写。 如果您看一下文件夹或由[FindItem 操作](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)（或[FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) EWS 托管 API 方法） 返回的项的项 ID，您可能会认为，它是重复的另一个项目 ID;但是，在两个项目的项 Id 中的一个或多个字符将具有不同的案例。 
    
- 如果您打算在以后要检索的数据库中存储的项 ID，我们建议该字段大小是 512 字节，以使它位于足以容纳 GUID。
    
- 不要假设您的 ID 将始终为有效的如果您需要在以后检索项目。 如果将项目移动存储区中，ID 可以更改由于移动的处理的方式。 项目实际复制，并生成新的 ID，然后[删除原始项目](deleting-items-by-using-ews-in-exchange.md)。
    
- Exchange 中的标识符是不透明的。 例如，从以下几条信息不是作为开发人员，对您重要但重要 Exchange 中创建 EwsId。
    
- 在 Exchange 处理项，另一个值，请记住时**更改密钥**属性。 除了项目 ID，此值，用于跟踪的项的状态。 生成的随时更改项目，新更改密钥。 执行[UpdateItem 操作](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)时，例如，可以使用**更改密钥**属性来让服务器了解正在更新应用于项目的最新版本。 如果另一个应用程序对您要更新的项目进行更改，更改密钥不匹配，您将无法执行更新。 
    
## <a name="distinguished-folder-ids"></a>可分辨的文件夹 Id
<a name="bk_DistinguishedFolderIds"> </a>

Exchange 包括的多个预定义的邮箱文件夹，其中每个分配的标识符，称为可分辨的文件夹 id。 这些[WellKnownFolderName](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) EWS 托管 API 枚举和[DistinguishedFolderId](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) EWS 元素来定义。 您可以使用这些可分辨的文件夹 Id 以更轻松地引用某个预定义的文件夹。 例如，对于收件箱文件夹中，您可以只使用"收件箱"的标识符，而不是确定文件夹标识符。 
  
创建组织电子邮件项目的其他文件夹还可以对该文件夹是唯一的 ID。 即使您更改文件夹上的其他属性，该 ID 将不会更改。
  
您可以使用可分辨的文件夹 Id 作为的入口点代理访问。 在启动代理访问时，您的项目或文件夹搜索，并提供要指定搜索位置的可分辨的文件夹 ID。 当代理用户访问的服务器时， **DistinguishedFolderId**元素的子元素的[邮箱](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx)元素用于明确指定的代理访问的邮箱。 
  
## <a name="handling-errors"></a>处理错误
<a name="bk_DealingWithErrors"> </a>

每个程序绑定和不时，获取错误和基于 EWS 的应用程序 （这适用于） 不例外。 [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) EWS 元素中或作为的一部分，您可能会收到一些标识符相关错误 EWS 托管 API 枚举的[服务错误](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.serviceerror%28v=exchg.80%29.aspx)。 
  
EWS 托管 API 或 EWS 应用程序中发生以下错误。 如果您正在使用 EWS 托管 API 应用程序，这些错误通常属性值; 问题对于 EWS 应用程序，错误是与 XML 元素的值或操作关联。
  
**表 2。与标识符相关的错误**

|**Error**|**发生此事件时...**|**说明**|
|:-----|:-----|:-----|
|ErrorCalendarCannotUseIdForOccurrenceId  <br/> |**OccurenceID**的值不对应于有效的定期日历项目。  <br/> |**OccurenceId**请求中指定的值可能是有效的结构，但请求未能匹配它到现有定期主控形状。 定期项目可能会移除从日历。 确保项目仍存在并且正在使用的正确的标识符。  <br/> |
|ErrorCalendarCannotUseIdForRecurringMasterId  <br/> |**RecurringMasterId**属性不对应于**OccurrenceId**元素有效匹配项。  <br/> |**RecurringMasterId**请求中指定的值可能是有效的结构，但请求未能匹配它到现有项目的事件。 日历中，可能会删除项的匹配项。 确保项目仍存在并且正在使用的正确的标识符。  <br/> |
|ErrorCannotUseFolderIdForItemId  <br/> |**ID**传递表示而不是项目的文件夹。  <br/> |该标识符可能是有效的格式，但不是什么服务器所需要的操作。 确认您引用的正确操作的标识符。  <br/> |
|ErrorCannotUseItemIdForFolderId  <br/> |中传递**ID**表示项目而不是一个文件夹。  <br/> |该标识符可能是有效的格式，但不是什么服务器所需要的操作。 确认您引用的操作正确的**ID** 。  <br/> |
|ErrorChangeKeyRequiredForWriteOperations  <br/> |执行某些更新操作时，必须提供有效的更改键。  <br/> |可以请求进行更新，或更改密钥不正确时省略**更改密钥**值。 验证已正确更改密钥时执行的 update 操作。  <br/> |
|ErrorInvalidAttachmentId  <br/> |项目的 attachments 集合中找不到该附件。  <br/> |如果您有附件**ID**然后删除附件并尝试对附件 id。 调用[GetAttachment 操作](http://msdn.microsoft.com/library/24d10a15-b942-415e-9024-a6375708f326%28Office.15%29.aspx)，您可能会收到此响应代码 验证附件的附件集合中存在。  <br/> |
|ErrorInvalidChangeKey  <br/> |无效的更改密钥传递了。  <br/> |请注意，许多操作和方法不需要更改密钥传递。 但是，如果提供更改密钥，它必须是有效的但它不一定是最新。  <br/> |
|ErrorInvalidFolderId  <br/> |文件夹**ID**已损坏。  <br/> |确保正确格式化且有效的标识符。  <br/> |
|ErrorInvalidId  <br/> |内部不一致的**ID**和/或更改密钥的结构。  <br/> |它已分析后，Exchange 遇到**ID**问题。 有可能已错误转换中。 此问题，例如，如果您有项目**IdFormatType.HexEntryId**在 Outlook 中，但将其转换为 EwsId 考虑过**IdFormatType.EntryId**格式。 请确保使用正确的转换类型。  <br/> |
|ErrorInvalidIdEmpty  <br/> |指定的应用程序的**ID**为空。  <br/> |您的应用程序中为空字符串传递为标识符。 确保正确格式化且有效的标识符。  <br/> |
|ErrorInvalidIdMalformed  <br/> |内部不一致的**ID**的结构。  <br/> |它已分析后，Exchange 遇到**ID**问题。 可能不正确转换 ID。 请确保使用正确的转换类型。  <br/> |
|ErrorInvalidIdMalformedEwsLegacyIdFormat  <br/> |版本的 Exchange 2007 SP1 或更高版本请求指定的文件夹或项目使用的 Exchange 2007 格式的**ID** 。  <br/> |不能使用 Exchange 2007 SP1 或更高版本的请求中的 Exchange 2007 Id。 您必须使用[ConvertId](http://msdn.microsoft.com/library/47d96cf6-9e2f-4fc0-9682-7258d3fbf918%28Office.15%29.aspx) EWS 操作或[ConvertId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.convertid%28v=exchg.80%29.aspx) EWS 托管 API 方法首先将转换。  <br/> |
|ErrorInvalidIdNotAnItemAttachmentId  <br/> |**AttachmentId**属性不引用项目附件。  <br/> |该标识符可能是有效的格式，但不是什么服务器所需要的操作。 确认您引用的正确操作的标识符。  <br/> |
|ErrorInvalidIdReturnedByResolveNames  <br/> |您的邮箱中的联系人已损坏。  <br/> |[ResolveNames](http://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) EWS 操作或[ResolveName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) EWS 托管 API 方法返回一个或多个标识符，但它们不是有效。 您可能需要重新创建联系人。  <br/> |
|ErrorInvalidIdStoreObjectIdTooLong  <br/> |内部不一致的**ID**的结构。  <br/> |它已分析后，Exchange 遇到**ID**问题。 可能不正确转换**ID** 。 请确保使用正确的转换类型。  <br/> |
|ErrorInvalidIdTooManyAttachmentLevels  <br/> |附件层次结构超过 255 个深度的最大。  <br/> |已请求中指定**AttachmentId**属性的值可能是有效的结构，但请求的附件太深层次结构中。 您的代码可能尝试附加超过 255 层的限制的项目。  <br/> |
|ErrorInvalidImContactId  <br/> |使用[RemoveImContactFromGroup 操作](http://msdn.microsoft.com/library/a190bbec-c71b-4e6a-880b-55854c724d8c%28Office.15%29.aspx)时，不能在 IM 组中找到该联系人时，可以返回此错误。 此错误适用于 Exchange Online 和 Exchange 开头 Exchange 2013 版本的目标设定的客户端。  <br/> |已请求中指定**ContactId**属性的值可能是有效的结构，但没有邮箱中的联系人匹配此结构。 联系人可能已被已删除。  <br/> |
|ErrorInvalidImGroupId  <br/> |组不能发现邮箱中，当您使用[RemoveImGroup 操作](http://msdn.microsoft.com/library/5e788016-68e0-4a3f-9243-03f6b6c6b389%28Office.15%29.aspx)时，可以返回此错误。 此错误适用于 Exchange Online 和 Exchange 开头 Exchange 2013 版本的目标设定的客户端。  <br/> |已请求中指定**GroupId**属性的值可能是有效的结构，但没有邮箱中的组匹配此结构。 组可能已被已删除。  <br/> |
|ErrorInvalidReferenceItem  <br/> |**MessageType**或**ExchangeWebServices.CalendarItemTypeType**，或其后代之一，该引用的项标识符不是。 引用的项标识符是**CalendarItemType**对象，组织者尝试向答复或全部答复。  <br/> |该标识符可能是有效的格式，但不是什么服务器所需要的操作。 确认您引用的正确操作的标识符。  <br/> |
|ErrorMissingManagedFolderId  <br/> |Id 属性的策略，该文件夹的属性标记 0x6732 遗漏。  <br/> |文件夹已损坏。 请考虑重新创建它。  <br/> |
   
## <a name="converting-identifiers"></a>转换标识符
<a name="bk_ConvertingIdentifiers"> </a>

您可能需要将标识符从一种格式转换为另一个。 例如，您可能需要将标识符转换从外部 EWS，如来自的 MAPI 连接，为您的应用程序可以使用的格式的标识符。 要执行此操作，您可以使用[ConvertId](http://msdn.microsoft.com/library/47d96cf6-9e2f-4fc0-9682-7258d3fbf918%28Office.15%29.aspx) EWS 操作或[ConvertId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.convertid%28v=exchg.80%29.aspx) EWS 托管 API 方法。 
  
例如，EntryID 是由时保存项目分配由存储的 MAPI 邮件存储区生成的唯一标识符。 若要在您的应用程序中使用 EntryID，首先需要将其转换为 EwsId。 
  
Outlook Web 应用程序使用它自己的标识符，在 Url 以访问文件夹和项目中称为 OwaId，版本。 如果您的应用程序需要访问 Outlook Web App 中的项，您需要 OwaId 转换 EwsId。
  
您可以使用**ConvertId**操作或方法将几种不同的标识符格式转换。 
  
**表 3。在 Exchange 兑换标识符格式**

|**Format**|**说明**|
|:-----|:-----|
|EwsLegacyId  <br/> |适用于 Exchange 2007 EwsId。  <br/> |
|EwsId  <br/> |适用于 Exchange Online 和 Exchange 2007 sp1 开始的 Exchange 版本 EwsId。  <br/> |
|StoreId  <br/> |Exchange 存储区标识符的文件夹和项目的存储位置。  <br/> |
|OwaId  <br/> |使用与 Exchange 2007 和 Exchange 2010 中的 Outlook Web App 的 Outlook Web App 标识符。 <br/><br/>**注意**： Exchange Online 和 Exchange 开头 Exchange 2013 版本使用 EwsId 适用于 Outlook Web App。           |
|EntryId  <br/> |通常被称为 MAPI 邮件的**PR_ENTRYID**属性 MAPI 标识符。  <br/> |
|HexEntryId  <br/> |**PR_ENTRYID**属性用于可用性日历事件标识符的十六进制编码表示形式。 这也是 Outlook 使用标识符格式。  <br/> |
   
## <a name="see-also"></a>另请参阅

- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)  
- [ConvertId 操作](http://msdn.microsoft.com/library/47d96cf6-9e2f-4fc0-9682-7258d3fbf918%28Office.15%29.aspx)  
- [服务错误枚举](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.serviceerror%28v=exchg.80%29.aspx) 
- [通过在 Exchange 使用 EWS 中删除项目](deleting-items-by-using-ews-in-exchange.md)
    

