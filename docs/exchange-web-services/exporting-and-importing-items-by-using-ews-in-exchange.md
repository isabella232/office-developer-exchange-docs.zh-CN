---
title: 使用 Exchange 中的 EWS 导出和导入项目
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.assetid: ad5f75f9-47c3-4f51-a535-80cba4243683
description: 了解如何使用 Exchange 中的 EWS 托管 API 或 EWS 导出和导入约会、电子邮件、联系人、任务和其他邮箱项目。
localization_priority: Priority
ms.openlocfilehash: 1bd36cec5c26f79de96b1506a52d297d2edc051a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528417"
---
# <a name="exporting-and-importing-items-by-using-ews-in-exchange"></a>使用 Exchange 中的 EWS 导出和导入项目

了解如何使用 Exchange 中的 EWS 托管 API 或 EWS 导出和导入约会、电子邮件、联系人、任务和其他邮箱项目。 
  
Exchange 是重要信息的金牌中的金牌：电子邮件、联系人、任务和日历是组织的职能的核心。 EWS 使您能够通过三种不同的方法导出和导入核心项目类型：
  
- Exchange 项目类型。 我们建议将项目导入和导出到其他系统和文件，这种方法。
    
- 项目级功能（仅限 EWS）。 建议从一个 Exchange 服务器或邮箱导出或复制该选项，然后导入到另一个。
    
- 采用常用标准文件格式（例如 iCalendar 和 vCard）形式的 MIME 流。 由于属性集受到限制，并且 MIME 转换成本较高，因此我们建议仅在导入或导出少量数据时使用方法。
    
> [!IMPORTANT]
> EWS 不是为邮箱备份和还原而设计的。 若要备份和还原数据库，请使用[备份和还原 API](../backup-restore/backup-and-restore-for-exchange-2013.md)。 另请参阅 TechNet 上的[备份、还原和灾难恢复](https://technet.microsoft.com/library/dd876874%28v=exchg.150%29.aspx)。 
  
**表1。导出和导入联系人、电子邮件和日历项目**

|任务|EWS 托管的 API 方法|EWS 操作|注释|
|:-----|:-----|:-----|:-----|
|使用[指定的属性集](properties-and-extended-properties-in-ews-in-exchange.md)导出联系人、电子邮件、任务或日历项目的副本。  <br/> |[Contact。绑定](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) <br/> [EmailMessage.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) <br/> [约会. 绑定](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) <br/> [任务。绑定](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.task.bind%28v=exchg.80%29.aspx) <br/> |[GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> |如果要将邮箱项目导出到另一个非 Exchange 系统或文件（包括 vCard 和 iCal 文件类型），我们建议您选择此选项。<br/>由于您可以控制导出的属性集，并且对于 Exchange 服务器而言性能更好，这通常是最佳选择。<br/><br/>根据邮箱项目上设置的属性，以及您的应用程序是否了解可能在项目上设置的所有非架构化属性标识符（扩展属性），此选项可能不会产生完全保真副本。<br/><br/>这些方法和操作提供项目的架构化属性集以及任何请求的扩展属性。<br/>如果您知道在项上设置的扩展属性，则**Bind**方法或**GetItem**操作只能提供项的完全保真导出。<br/>您可以请求所有已知的[扩展属性](properties-and-extended-properties-in-ews-in-exchange.md)以实现全保真。<br/><br/>**提示**：您可以使用 EWS 托管 API 中的跟踪功能来获取导出项的 XML 表示形式。           有关详细信息，请参阅[将项目导出为自定义格式](how-to-export-items-by-using-ews-in-exchange.md#bk_exportcustom)。  <br/> |
|导入具有[指定属性集](properties-and-extended-properties-in-ews-in-exchange.md)的联系人、电子邮件、任务或日历项目的副本。  <br/> |[联系人。保存](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact.save%28v=exchg.80%29.aspx) <br/> [EmailMessage.Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.save%28v=exchg.80%29.aspx) <br/> [约会. 保存](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) <br/> [任务。保存](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.task.save%28v=exchg.80%29.aspx) <br/> |[CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/> |建议将邮箱项目导入 Exchange 中的此选项。<br/>您可能需要在某些项目类型上设置特殊属性，以便维护导入项目的状态。<br/>由于某些属性仅由 Exchange 而不是由客户端设置，因此并不总是可以进行高保真导入。<br/><br/>例如，无法将与会者的会议导入到邮箱中，因为 Exchange 会设置组织者和与会者之间的关系。 <br/>这种关系只能由组织者发送和响应会议请求的参与者建立。<br/><br/>Exchange 中的**约会**对象可以有复杂的关系和设置。<br/> 具有与会者（会议）的约会具有将会议组织者和会议与会者联系在一起的设置。<br/>在导出和导入约会时，不会保留这些设置。<br/>不支持以编程方式直接在约会上重新建立会议组织者/与会者关系。<br/>重新建立这些关系的一个选项是，在导入后执行后续处理，然后让组织者重新发送会议并让与会者接受会议。<br/>您可以使用 Exchange 模拟对组织者和与会者进行呼叫。<br/>在导入之前，应更改**约会**对象的 UID 属性，以避免将会议与邮箱中的其他会议错误相关。  <br/> |
|以全保真方式导出联系人、电子邮件、任务或日历项目的副本。  <br/> |不适用  <br/> |[ExportItems](https://msdn.microsoft.com/library/e2846abb-0b16-4732-bbd8-038a674672f6%28Office.15%29.aspx) <br/> |这是导出要导入到 Exchange 邮箱中的邮箱项目的最佳选项。<br/>您还可以使用此选项在邮箱之间复制项目。<br/><br/>**ExportItems**操作提供了一个不透明的流，表示可用于在邮箱之间移动信息的项目。<br/>可以将**ExportItems**与[GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx)操作一起使用，以创建用于查找另一个系统中的项的索引。<br/>您不能更改导出流。  <br/> 有关详细信息，请参阅[使用完全保真导出项目](how-to-export-items-by-using-ews-in-exchange.md#bk_exportfullfidelity)。  <br/> |
|以全保真方式导入联系人、电子邮件、任务或日历项目的副本。  <br/> |不适用  <br/> |[UploadItems](https://msdn.microsoft.com/library/a88cbe99-7968-454d-a545-4f92c330909f%28Office.15%29.aspx) <br/> |这是导入由**ExportItems**操作导出的项目的唯一选项。  <br/> |
|将联系人、电子邮件或日历项目的副本导出为常见文件类型的 MIME 流。  <br/> |[Contact。绑定](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) <br/> [EmailMessage.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) <br/> [约会. 绑定](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) <br/> |**GetItem** <br/> |您可以使用[MimeContent](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.mimecontent%28v=exchg.80%29.aspx)属性来获取项目的 MIME 流表示形式。<br/><br/>这将提供项的所有属性的基本子集。<br/>最佳做法是，仅将 MIME 流用于一次性操作。<br/>不要依赖于 MIME 对较大和频繁的项进行导入/导出，因为 Exchange 会对 MIME 执行内容转换，这可能会影响性能。<br/><br/>**联系人**MIME 流是一个[vCard](http://www.faqs.org/rfcs/rfc2426.html) （.vcf）文件。<br/>这可能不会产生完全保真副本，具体取决于在联系人上设置的属性。<br/>请注意，不能使用 vCard MIME 流导入联系人。<br/>若要了解详细信息，请参阅将[联系人导出到 vCard 文件](how-to-export-items-by-using-ews-in-exchange.md#bk_exportvcardmime)中。<br/><br/>**EmailMessage** MIME 流是一个 .eml 文件。<br/>.Eml 格式非常方便，因为 Outlook 和其他电子邮件客户端可以识别它。<br/>您还可以使用 MIME 流创建 .mht 文件，这是很方便的，因为很多浏览器都可以使用该文件类型。<br/>EWS 不提供用于将电子邮件导出到 .msg 文件的 .msg 文件流。<br/>用于导出 .msg 文件的选项是[：构造。](https://msdn.microsoft.com/library/cc463912%28v=EXCHG.80%29.aspx)从**EmailMessage**方法或**GetItem**操作的结果中调用的 MSG 文件，或使用调用 EWS 的第三方 API，并从结果中构造 .msg 文件。<br/>有关详细信息，请参阅[将电子邮件导出为 .eml 文件](how-to-export-items-by-using-ews-in-exchange.md#bk_exportemailmime)。<br/><br/>**约会**MIME 流是 iCal （ics）文件。<br/>由于 Outlook 和其他电子邮件客户端可以识别它，因此可以方便地进行 ics 格式。<br/>这不是导出会议的可行选项，因为 MIME 流中未提供与会者信息。 <br/>MIME 流中可能不包含附件和其他属性。<br/>请考虑从[约会](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx)对象或由**GetItem**操作返回的 XML 构造 iCal 格式。<br/>通过这种方式，您可以使用 iCal 文件中的扩展属性（"X-" 属性）捕获更多的 Exchange 属性。<br/>您还可以导出 XML 表单中的约会。<br/>调用**GetItem**操作，并将 XML 保存在您的系统中。<br/>您还可以使用 EWS 托管 API 中的[跟踪功能](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md)来捕获要放入 xml 数据库的 xml。<br/>有关详细信息，请参阅将[约会导出为 iCal 文件](how-to-export-items-by-using-ews-in-exchange.md#bk_exporticalmime)。  <br/> |
|将电子邮件或日历项目的副本导入为常见文件类型的 MIME 流。  <br/> |[EmailMessage.Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.save%28v=exchg.80%29.aspx) <br/> [约会. 保存](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) <br/> |**CreateItem** <br/> |您可以使用**EmailMessage**或**约会**对象上的**MimeContent**属性导入 .eml 或文件。<br/>如果电子邮件不是草稿，您将需要设置[PidTagMessageFlags （0x0E07）](https://msdn.microsoft.com/library/office/cc839733%28v=office.15%29.aspx)扩展属性。<br/><br/>您不能使用此方法导入会议。  <br/> |
   
## <a name="alternatives-to-exporting-and-importing-items-by-using-ews"></a>使用 EWS 导出和导入项目的替代方法
<a name="alternatives"> </a>

其他选项可用于 exporing，并可从 Exchange 邮箱中导入和导出项目。 以下是在设计导入和导出策略时要考虑的一些建议：
  
- 使用 PowerShell 调用 EWS 并将输出格式设置为 .csv 文件。
    
- 使用实现 MAPI 的第三方库来导出和导入项目。 将 EWS 转换为 .msg 文件的第三方库也可用。
    
- 使用 Exchange 命令行管理程序和[new-mailboximportrequest](https://technet.microsoft.com/library/ff607310%28v=exchg.150%29.aspx)和[new-mailboxexportrequest](https://technet.microsoft.com/library/ff607299%28v=exchg.150%29.aspx) cmdlet 来[实现邮箱导入和导出请求](https://technet.microsoft.com/library/ee633455%28v=exchg.150%29.aspx)。 
    
- 使用[Outlook 的导入选项](https://office.microsoft.com/outlook-help/import-outlook-items-from-an-outlook-data-file-pst-HA102505743.aspx)导入和导出项目。 

    
## <a name="in-this-section"></a>本节内容
<a name="alternatives"> </a>

- [使用 Exchange 中的 EWS 导出项目](how-to-export-items-by-using-ews-in-exchange.md)    
- [使用 Exchange 中的 EWS 导入项目](how-to-import-items-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a>另请参阅

- [备份、还原和灾难恢复](https://technet.microsoft.com/library/dd876874%28v=exchg.150%29.aspx)  
- [日记](https://technet.microsoft.com/library/aa998649%28v=exchg.150%29.aspx)    
- [Internet 日历和计划核心对象规范（RFC 5545）](http://tools.ietf.org/html/rfc5545)   
- [邮箱同步和交换中的 EWS](mailbox-synchronization-and-ews-in-exchange.md)
    