---
title: 导出和导入在 Exchange 中使用 EWS 的项目
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: ad5f75f9-47c3-4f51-a535-80cba4243683
description: 了解如何导出和导入在 Exchange 使用 EWS 托管 API 或 EWS 的约会、 电子邮件、 联系人、 任务和其他邮箱项目。
ms.openlocfilehash: 00c72806b95c162077733f77a52c4ea4da03631f
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353649"
---
# <a name="exporting-and-importing-items-by-using-ews-in-exchange"></a>导出和导入在 Exchange 中使用 EWS 的项目

了解如何导出和导入在 Exchange 使用 EWS 托管 API 或 EWS 的约会、 电子邮件、 联系人、 任务和其他邮箱项目。 
  
Exchange 是金色挖掘重要信息： 电子邮件、 联系人、 任务和日历的核心组织的函数。 EWS 使您能够导出和导入通过三种不同方法的核心项目类型：
  
- Exchange 项目类型。 我们建议使用此方法用于导入和导出项目与其他系统和文件。
    
- 项目级功能 (仅限 EWS)。 我们建议导出或从一个 Exchange 服务器或邮箱复制和导入到另一个此选项。
    
- MIME 等 iCalendar 电子名片的常见标准文件格式的窗体中的流。 由于有限的属性集并 MIME 的转换会消耗大量资金，我们建议仅用于导入或导出的少量数据的方法。
    
> [!IMPORTANT]
> EWS 不适用于邮箱备份和还原。 若要备份和还原数据库，请使用[备份和还原 API](../backup-restore/backup-and-restore-for-exchange-2013.md)。 请参阅 TechNet 上的[备份、 还原和灾难恢复](http://technet.microsoft.com/en-us/library/dd876874%28v=exchg.150%29.aspx)。 
  
**表 1。导出和导入联系人、 电子邮件和日历项目**

|任务|EWS 托管的 API 方法|EWS 操作|笔记|
|:-----|:-----|:-----|:-----|
|导出联系人、 电子邮件、 任务或日历项目的[指定的属性设置](properties-and-extended-properties-in-ews-in-exchange.md)的副本。  <br/> |[Contact.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) <br/> [EmailMessage.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) <br/> [Appointment.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) <br/> [Task.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.task.bind%28v=exchg.80%29.aspx) <br/> |[GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> |如果您将邮箱项目导出到另一个非 Exchange 系统或 （包括电子名片和 iCal 文件类型） 文件，我们建议此选项。<br/>因为您可以控制导出的属性集，并且性能更佳的 Exchange 服务器，这通常是最佳选项。<br/><br/>根据属性设置邮箱的项，并注意可能在项目设置的非架构化属性标识符 （扩展属性） 的所有应用程序是否，此选项可能不会产生完全保真的副本。<br/><br/>这些方法和操作提供项目的属性以及任何请求的扩展的属性架构化的的集。<br/>**绑定**方法或**GetItem**操作只能提供完全保真的导出的项目如果您知道项目设置的扩展的属性。<br/>您可以请求的所有已知的[扩展的属性](properties-and-extended-properties-in-ews-in-exchange.md)启用全保真方式。<br/><br/>**提示**： 可以使用 EWS 托管 API 中的跟踪功能要获取的 XML 表示形式导出的项目。           有关详细信息，请参阅[导出一项插入自定义格式](how-to-export-items-by-using-ews-in-exchange.md#bk_exportcustom)。  <br/> |
|导入联系人、 电子邮件、 任务中或[指定的属性设置](properties-and-extended-properties-in-ews-in-exchange.md)的日历项目的副本。  <br/> |[Contact.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contact.save%28v=exchg.80%29.aspx) <br/> [EmailMessage.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.save%28v=exchg.80%29.aspx) <br/> [Appointment.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) <br/> [Task.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.task.save%28v=exchg.80%29.aspx) <br/> |[CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/> |我们建议将邮箱项目导入到 Exchange 此选项。<br/>您可能需要对一些项目类型的特殊属性设置为了维护导入的项的状态。<br/>由 Exchange 而非客户端仅设置某些属性，因为它并不总是可能需要完全保真的导入。<br/><br/>例如，您无法导入与与会者的会议邮箱因为 Exchange 将组织者和与会者之间的关系。 <br/>仅可以通过发送组织者和与会者接收和响应会议请求中建立这种关系。<br/><br/>Exchange 中的**约会**对象可以具有复杂的关系和设置。<br/> 有与会者 （会议） 的约会具有会议组织者和与会者将联系在一起的设置。<br/>导出和导入约会时，不会保留这些设置。<br/>以编程方式重新建立会议组织者/attendee 关系直接对约会不支持。<br/>您具有的重新建立这些关系执行选项然后后处理导入后，具有管理器重新发送会议并已接受会议的与会者。<br/>您可以使用 Exchange 模拟组织者和与会者发起呼叫。<br/>若要避免错误地与邮箱中的其他会议的会议导入前，您应更改**Appointment**对象的 UID 属性。  <br/> |
|导出联系人、 电子邮件、 任务或日历项完全保真的的副本。  <br/> |不适用  <br/> |[ExportItems](http://msdn.microsoft.com/library/e2846abb-0b16-4732-bbd8-038a674672f6%28Office.15%29.aspx) <br/> |这是用于导出要导入回 Exchange 邮箱的邮箱项目的最佳选项。<br/>您可以使用此选项可邮箱之间复制项。<br/><br/>**ExportItems**操作提供不透明的数据流，代表可用于邮箱之间移动信息的项目。<br/>您可以使用[GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx)操作**ExportItems**使查找另一个系统中的项的索引。<br/>不能更改导出流。  <br/> 有关详细信息，请参阅[导出全保真方式项目](how-to-export-items-by-using-ews-in-exchange.md#bk_exportfullfidelity)。  <br/> |
|导入联系人、 电子邮件、 任务或完全保真的中的日历项目的副本。  <br/> |不适用  <br/> |[UploadItems](http://msdn.microsoft.com/library/a88cbe99-7968-454d-a545-4f92c330909f%28Office.15%29.aspx) <br/> |这是唯一的选项的导入**ExportItems**操作已导出的项目。  <br/> |
|将一个联系人、 电子邮件或日历项一份导出为 MIME 流常见的文件类型。  <br/> |[Contact.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) <br/> [EmailMessage.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) <br/> [Appointment.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) <br/> |**GetItem** <br/> |[MimeContent](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.mimecontent%28v=exchg.80%29.aspx)属性可用于获取项目的 MIME 流表示形式。<br/><br/>这将在项目上提供基本的所有属性的子集。<br/>作为最佳实践，只能使用一次性操作 MIME 流。<br/>不依赖于 MIME 的较大且常用导入/导出的项目，因为 Exchange 执行内容转换为 MIME，这会影响性能。<br/><br/>**联系人**MIME 流是一个[vCard](http://www.faqs.org/rfcs/rfc2426.html) (.vcf) 文件。<br/>根据联系人设置的属性，这可能不会产生完全保真的副本。<br/>请注意，您无法使用该电子名片 MIME 流来导入联系人。<br/>若要了解详细信息，请参阅[导出到一个 vCard 文件联系人](how-to-export-items-by-using-ews-in-exchange.md#bk_exportvcardmime)。<br/><br/>**EmailMessage** MIME 流是一个.eml 文件。<br/>.Eml 格式是方便，因为 Outlook 和其他电子邮件客户端可以发现它。<br/>MIME 流还可用于创建.mht 文件，这是因为许多浏览器可以使用该文件类型方便。<br/>EWS 不用于导出到的.msg 文件的电子邮件提供.msg 文件流。<br/>用于导出.msg 文件的选项是为[构造。MSG 文件](http://msdn.microsoft.com/en-us/library/cc463912%28v=EXCHG.80%29.aspx)从**EmailMessage.Bind**方法或**GetItem**操作的结果呼叫，或使用第三方 API 调用 EWS 和构造从结果.msg 文件。<br/>有关详细信息，请参阅[导出电子邮件以.eml 文件](how-to-export-items-by-using-ews-in-exchange.md#bk_exportemailmime)。<br/><br/>**约会**MIME 流是一个 iCal (.ics) 文件。<br/>.Ics 格式是方便，因为 Outlook 和其他电子邮件客户端可以发现它。<br/>这不是因为 MIME 用于将 stream 中不提供与会者信息导出会议的可行选项。 <br/>附件和其他属性可能不会包含 MIME 用于将 stream 中。<br/>请考虑构建 iCal 格式从[Appointment](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx)对象或从由**GetItem**操作返回的 XML。<br/>这种方式，您可以捕获多个 Exchange 属性与扩展属性 ("x 属性) iCal 文件中。<br/>您还可以导出的 XML 表单中的约会。<br/>调用**GetItem**操作并保存在您的系统的 XML。<br/>您可以使用 EWS 托管 API 中的[跟踪功能](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md)捕获的 XML，置于 XML 数据库。<br/>有关详细信息，请参阅[导出 iCal 文件形式的约会](how-to-export-items-by-using-ews-in-exchange.md#bk_exporticalmime)。  <br/> |
|导入作为 MIME 流常见的文件类型的电子邮件或日历项目的副本。  <br/> |[EmailMessage.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.save%28v=exchg.80%29.aspx) <br/> [Appointment.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) <br/> |**CreateItem** <br/> |您可以通过**EmailMessage**或**约会**对象上使用**MimeContent**属性导入.eml 或.ics 文件。<br/>您需要设置[PidTagMessageFlags (0x0E07)](http://msdn.microsoft.com/en-us/library/office/cc839733%28v=office.15%29.aspx)如果电子邮件不是草稿扩展属性。<br/><br/>此方法不能用于导入会议。  <br/> |
   
## <a name="alternatives-to-exporting-and-importing-items-by-using-ews"></a>替代项为导出和导入使用 EWS 的项目
<a name="alternatives"> </a>

其他选项供 exporing 和导入项目与 Exchange 邮箱。 设计导入和导出策略的时要考虑的一些方法如下：
  
- 使用 PowerShell 调用 EWS 和设置输出格式到.csv 文件。
    
- 使用实现 MAPI 导出和导入项目的第三方库。 第三方库的转换为.msg 文件的 EWS 太均可用。
    
- 使用 Exchange 命令行管理程序和[MailboxImportRequest](http://technet.microsoft.com/en-us/library/ff607310%28v=exchg.150%29.aspx)和[MailboxExportRequest](http://technet.microsoft.com/en-us/library/ff607299%28v=exchg.150%29.aspx) cmdlet 为[满足邮箱导入和导出请求](http://technet.microsoft.com/en-us/library/ee633455%28v=exchg.150%29.aspx)。 
    
- 使用[Outlook 的导入选项](http://office.microsoft.com/en-us/outlook-help/import-outlook-items-from-an-outlook-data-file-pst-HA102505743.aspx)导入和导出的项目。 
    
## <a name="in-this-section"></a>本节内容
<a name="alternatives"> </a>

- [在 Exchange 使用 EWS 导出项目](how-to-export-items-by-using-ews-in-exchange.md)    
- [在 Exchange 使用 EWS 导入项目](how-to-import-items-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a>另请参阅

- [备份、 还原和灾难恢复](http://technet.microsoft.com/en-us/library/dd876874%28v=exchg.150%29.aspx)  
- [日记功能](http://technet.microsoft.com/en-us/library/aa998649%28v=exchg.150%29.aspx)    
- [Internet 日历和计划核心对象规范 (RFC 5545)](http://tools.ietf.org/html/rfc5545)   
- [邮箱同步和交换中的 EWS](mailbox-synchronization-and-ews-in-exchange.md)
    

