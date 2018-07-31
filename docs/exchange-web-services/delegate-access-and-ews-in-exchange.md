---
title: 代理访问和 Exchange 中的 EWS
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 240d1776-7adc-46cd-9099-88ffeba0a8aa
description: 了解如何使用 EWS 托管 API 和 EWS 在 Exchange 提供对用户邮箱的代理访问。
ms.openlocfilehash: 344255d86a51e13b21f1eda5113d292395d7cb8f
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354048"
---
# <a name="delegate-access-and-ews-in-exchange"></a>代理访问和 Exchange 中的 EWS

了解如何使用 EWS 托管 API 和 EWS 在 Exchange 提供对用户邮箱的代理访问。
  
您可以让用户能够访问其他用户的邮箱的三种方式之一： 
  
- 添加代理人，并指定每个代理人的权限。
    
- 通过直接修改文件夹权限。
    
- 使用模拟。
    
委派和文件夹权限是最佳时要仅对少数用户授权访问因为您需要为每个邮箱单独添加权限。 模拟是最佳选择当您处理的数量的邮箱，因为您可以轻松地启用一个服务帐户以访问数据库中的每个邮箱。 图 1 显示了一些每种类型的访问之间的差异。
  
**图 1。方式访问其他用户的邮箱**

![显示邮箱访问类型、邮箱所有者与每种类型的委派之间的关系以及权限类型的图表。代表委派权限和/或文件夹权限发送。用于模拟的发送身份权限。](media/Ex15_Delegate_Overview.png)
  
当谈到发送邮件或安排会议时，代理人可授予"代表发送"权限，因此收件人的电子邮件或会议要求已发送的代理人将看到"代表*邮箱所有者*的*委派*"时其接收e 在 Outlook 中的电子邮件或会议请求。 包括"代表发送"文本是客户端实现的详细信息的并且可以创建使用"从"和"发件人"值。 将"从"值指示邮箱所有者，并"发件人"值指示已发送邮件的代理人。 如果模拟用户的服务帐户发送电子邮件，或为邮箱所有者安排会议，"发送邮件作为"邮箱所有者。 没有要了解的服务帐户已发送邮件的收件人方法。 授予文件夹权限以及不委派访问权限的用户将不能以"代理发送"或"代表发送"的邮箱所有者。 他们有权访问邮箱文件夹，并可能能够在文件夹中创建项目，但他们不能发送项目。 
  
时，适合直接修改文件夹权限？ 一般情况下，您想要提供用户访问的文件夹，但不是想授予用户权限要求未映射到[DelegateFolderPermissionLevel](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.delegatefolderpermissionlevel%28v=exchg.80%29.aspx) EWS 托管 API 枚举值时"代表发送"权限，或[PermissionLevel](http://msdn.microsoft.com/library/87978600-3523-451e-a725-ef092c543e2a%28Office.15%29.aspx)EWS 元素的值，或当您想要提供对一个自定义文件夹的用户访问。 
  
如果您只需修改文件夹权限，以实现您的目标，并不需要添加代理 （即，不需要"代表发送"权限），请参阅[设置文件夹在 Exchange 使用 EWS 的另一个用户的权限](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md)。 
  
请注意，您可以还使用[Outlook](http://office.microsoft.com/en-us/outlook-help/allow-someone-else-to-manage-your-mail-and-calendar-HA102749417.aspx)或[Exchange Server PowerShell (Exchange Management Shell)](https://docs.microsoft.com/en-us/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)设置代理访问权限。 
  
## <a name="how-does-delegate-access-work"></a>如何执行委派访问工作？

代理访问使用户能够访问邮箱所有者的文件夹的部分或全部和代表邮箱所有者操作。 邮箱所有者可以是用户或资源，如会议室。 例如，前台接待员可授予对会议室的日历文件夹的委派权限以处理预定请求。 您可以使用 EWS 托管 API 或 EWS 允许邮箱所有者或管理员添加代理时，指定哪些代理人可以访问，请然后指定该文件夹的权限的文件夹。 代理人可以被授予访问权限的以下文件夹： 
  
- 日历
    
- 任务
    
- Inbox
    
- 联系人
    
- 笔记
    
- 日记
    
当用户具有代理访问到一个或多个这些文件夹时，他们可以创建、 获取、 更新、 删除、 复制和搜索项目中的文件夹和所有子文件夹，根据文件夹上设置的[权限](#bk_delegateperms)。 应用程序中执行这些操作的方式取决于是否需要[显式](#bk_explicit)或[隐式](#bk_implicit)访问。 
  
## <a name="delegate-permissions"></a>委派权限
<a name="bk_delegateperms"> </a>

当管理员或邮箱所有者代理人添加到邮箱时，他们还可以设置为一个或多个文件夹的权限级别。 如果未设置文件夹的权限级别，权限值默认为无。 多个用户可以对文件夹中，具有相同权限级别和用户可以具有不同权限级别的不同的文件夹。 如果您正在使用 EWS 托管 API，您将使用[DelegateUser.Permissions](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.delegateuser.permissions%28v=exchg.80%29.aspx)属性，其中包含每个文件夹[DelegateFolderPermissionLevel](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.delegatefolderpermissionlevel%28v=exchg.80%29.aspx)枚举值之一，文件夹上设置委派权限。 如果您正在使用 EWS，使用设置委派权限[DelegatePermissions](http://msdn.microsoft.com/library/292badc7-bab3-4368-9d7c-9a8b7edb279b%28Office.15%29.aspx)元素和[PermissionLevel](http://msdn.microsoft.com/library/87978600-3523-451e-a725-ef092c543e2a%28Office.15%29.aspx)元素来定义权限级别。 
  
**表 2。委派权限级别**

|**权限级别**|**说明**|
|:-----|:-----|
|无  <br/> |这是所有文件夹的默认值。  <br/> |
|作者  <br/> |代理人可以读取和创建项目，并修改和删除他们创建的项目。 例如，代理人可以直接在邮箱所有者的任务或日历文件夹中创建任务请求和会议请求，然后邮箱所有者的代表发送任何一项。  <br/> |
|Editor  <br/> |代理人可以执行所有内容作者可以执行操作，并修改和删除邮箱所有者创建的项目。  <br/> |
|Reviewer  <br/> |代理人可以阅读项目;例如具有审阅者权限代理人可以读取其他人的收件箱中的邮件。  <br/> |
|自定义  <br/> |邮箱所有者授予权限的组自定义委托。  <br/> |
   
[DelgateUser.ViewPrivateItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.delegateuser.viewprivateitems%28v=exchg.80%29.aspx) EWS 托管 API 属性和[ViewPrivateItems](http://msdn.microsoft.com/library/80b949ac-440c-4a01-b428-ebafb5b1b802%28Office.15%29.aspx) EWS 元素是影响邮箱所有者的所有文件夹，包括所有邮件、 联系人、 日历、 任务、 注释和日记文件夹的全局设置。 您不能允许访问私有只有一个文件夹中的项目。 
  
## <a name="explicit-access"></a>显式访问
<a name="bk_explicit"> </a>

只需 put、 显式访问是代理人邮箱所有者的文件夹或项目上执行操作的条目的方式。 显式访问权限授予代理人到服务器的请求中包含邮箱所有者的 SMTP 地址以及邮箱所有者的文件夹的已知文件夹名称。 因为代理的请求明确说明方法或操作的上下文是邮箱所有者的邮箱，并不代理邮箱访问显式。
  
显式访问定义的所有方法或文件夹或项目向前移动执行的操作的上下文。 唯一设置显式访问时返回的所有项目和文件夹 Id 都标识自身为属于邮箱所有者 （但不在任何可读格式）。 这种方式，应用程序不需要指定邮箱所有者的 SMTP 地址反复;identifiers 中隐藏上下文。 标识项目或文件夹后，代理人实际使用[隐式访问](#bk_implicit)修改项。 下图显示显式和隐式访问的过程。 
  
**图 2。请求显式和隐式访问项目或文件夹**

![显示应用程序发送显式访问请求并从服务器获得响应，然后发送隐式访问请求并从服务器获得响应的图表。](media/Ex15_Delegate_ExplictImplicit.png)
  
您可以在许多不同的情况下设置显式访问。 实际上，的随时您发送文件夹 ID 中的方法或操作，您可以设置显式访问。 这可以包括查找文件夹，查找约会，获取项目，查找对话，等等。
  
### <a name="explicit-access-and-the-ews-managed-api"></a>显式访问和 EWS 托管 API
<a name="bk_explicitewsma"> </a>

您可以通过使用下面的重载方法采取[文件夹 Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx)输入的参数标识的目标文件夹的任一发起显式代理访问： 
  
- [Folder.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx)
    
- [ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
    
- [ExchangeService.FindAppointments](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx)
    
- [ExchangeService.FindFolders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)
    
- 更多 ！
    
可以在每个这些方法使用**文件夹 Id**参数来标识邮箱所有者的目标文件夹，如下所示。 
  
```cs
new FolderId(WellKnownFolderName.Calendar, "primary@contoso.com");
```

例如，要绑定到日历文件夹，在此**绑定**方法**文件夹 Id**指定已知文件夹名称和邮箱所有者的 SMTP 地址。 
  
```cs
CalendarFolder calendar = CalendarFolder.Bind(service, new FolderId(WellKnownFolderName.Calendar, "primary@contoso.com"), new PropertySet());
```

通过指定的已知文件夹名称和 SMTP 地址，代理人可以绑定到邮箱所有者的日历文件夹，从而获得对文件夹显式访问权限。 [隐式访问](#bk_implicit)文件夹中的项目的所有后续请求然后依赖于的上下文 Id 和文件夹 Id 返回在项目中。 实际上，标识符包含暗示的委派访问呼叫的上下文。 或者，若要检索满足特定条件的项目的项 ID，请使用以下。 
  
```cs
FindItemsResults<Item> results = service.FindItems(new FolderId(WellKnownFolderName.Calendar, "primary@contoso.com"), filter, view);
```

在这种情况下返回的项 ID，然后委托然后可以使用隐式访问对项目进行更改，使用项目 id。
  
您不必再次启动显式访问，直到您需要项目 ID 或未访问通过现有的显式访问文件夹 ID。 
  
### <a name="explicit-access-and-ews"></a>显式访问和 EWS
<a name="bk_explicitewsma"> </a>

您可以通过使用[GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx)、 [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)或[FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)操作启动显式访问。 这些操作提供[DistinguishedFolderId](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx)元素用于标识目标文件夹的选项。 **DistinguishedFolderId**元素都有一个可选子元素，[邮箱](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx)元素。 **邮箱**元素，用作**DistinguishedFolderId**元素的子时指定的代理访问的邮箱。 如果呼叫用户有权访问邮箱所有者的文件夹，响应将包含对该邮箱中的文件夹或项目的标识符的集合。 响应中返回的项和文件夹标识符可用于隐式代理访问。 
  
## <a name="implicit-access"></a>隐式访问
<a name="bk_implicit"> </a>

代理人已检索到一个项目或邮箱所有者的邮箱文件夹中的 ID 和委托想要更新、 删除或复制项后，将使用隐式访问权限。 如果代理请求中使用该项目或文件夹的 ID，对邮箱所有者的邮箱中的项目进行更改。 该委托不需要包含邮箱所有者的 SMTP 地址。 
  
例如，当代理人具有一个邮箱所有者的文件夹的 ID，代理可以通过使用文件夹 ID，而显式标识邮箱所有者的邮箱执行该文件夹**FindItem**操作。 此时，代理人可以执行操作邮箱所有者的文件夹使用在响应中返回的 Id。 
  
### <a name="implicit-access-and-the-ews-managed-api"></a>隐式访问和 EWS 托管 API

如果项目 ID 检索到[FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)方法，该项目 ID 可用于在后续[Item.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx)方法调用绑定到项。 然后，您可以调用[Item.Update](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.item.update%28v=exchg.80%29.aspx)、 [Item.Delete](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx)或[Item.Copy](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.item.copy%28v=exchg.80%29.aspx)方法 — 或需要项目 ID 的任何方法调用 — 根据需要完成您的任务。 只要委派到的文件夹包含的项目具有适当的权限 （和，如果适用，文件夹项目将移至），代理人可以根据其权限级别进行更改。 
  
### <a name="implicit-access-and-ews"></a>隐式访问和 EWS

如果项目 ID 检索到[FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)操作，该项目 ID 可用于在后续[GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx)操作中绑定到项。 然后，您可以调用[UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)、[删除项](../web-service-reference/deleteitem-operation.md)或[CopyItem](http://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx)操作 — 或需要项目 ID 的任何操作，根据需要完成您的任务。 只要委派到的文件夹包含的项目具有适当的权限 （和，如果适用，文件夹项目将移至），代理人可以根据其权限级别进行更改。 
  
## <a name="in-this-section"></a>本节内容
<a name="bk_implicit"> </a>

- [添加和删除代理人，在 Exchange 使用 EWS](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)
    
- [在 Exchange 中使用 EWS 作为代理人访问日历](how-to-access-a-calendar-as-a-delegate-by-using-ews-in-exchange.md)
    
- [作为代理人在 Exchange 使用 EWS 访问联系人](how-to-access-contacts-as-a-delegate-by-using-ews-in-exchange.md)
    
- [作为 Exchange 中使用 EWS 代理人的访问电子邮件](how-to-access-email-as-a-delegate-by-using-ews-in-exchange.md)
    
- [在 Exchange 使用 EWS 设置另一个用户的文件夹权限](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md)
    
- [在 Exchange 处理委派相关 EWS 中的错误](handling-delegation-related-errors-in-ews-in-exchange.md)
    
## <a name="see-also"></a>另请参阅


- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)
    
- [允许其他人来管理您的邮件和日历](http://office.microsoft.com/en-us/outlook-help/allow-someone-else-to-manage-your-mail-and-calendar-HA102749417.aspx)
    
- [添加 MailboxPermission](http://technet.microsoft.com/en-us/library/bb124097%28v=exchg.150%29.aspx)
    

