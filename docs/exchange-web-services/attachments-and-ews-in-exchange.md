---
title: 附件和 Exchange 中的 EWS
manager: sethgros
ms.date: 7/11/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8e4289a4-ec9d-4502-9854-c593c95d5f98
description: 了解附件，以及如何您 EWS 托管 API 或 EWS 在 Exchange 客户端代表它们。
ms.openlocfilehash: e4a97873798b8252e6fc14003519ce8a0eab7ec8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752705"
---
# <a name="attachments-and-ews-in-exchange"></a>附件和 Exchange 中的 EWS

了解附件，以及如何您 EWS 托管 API 或 EWS 在 Exchange 客户端代表它们。
  
通常，附件是与电子邮件项目，但实际上，所有 EWS 项目相关联 — 电子邮件、 日历项、 联系人、 任务 — 可以包含附件。
  
## <a name="types-of-attachments"></a>类型的附件

EWS 分类附件分为两组： 文件附件和项附件。
  
- **项目附件：** 强类型[EWS 项目](folders-and-items-in-ews-in-exchange.md)，如电子邮件和附加到另一个强类型 EWS 项的日历项目。 可以通过使用 EWS 托管 API 或 EWS 创建的任何强类型的项目可用作项目附件。 项目附件的内容是强类型项目，可以轻松访问其所有属性。 项附件可以具有自己的项目附件，因此项附件 （或嵌套附件） 的层次结构是可能。
    
- **文件附件：** 任何文件，如.txt、.jpg、.zip、.pdf 或甚至.msg 文件。 文件附件仅有几个属性，其中之一是 base64 编码的文件的内容。 
    
- **引用附件：** 任何附件的文件提供程序，例如文件位于云引用。 附件可从多个提供程序。 
    
当您添加或从项目中检索附件时，将根据是否的文件附件或项目附件不同执行。 例如，若要添加到项目的文件附件，您可以仅传递中文件的位置。 若要作为项目附件添加现有项，实际上需要将现有项目的 MIME 内容或属性复制到一个新的项目附件;您不能只需绑定到现有的项。 因此，区分两种类型的附件非常重要。 [本节中](#bk_inthissection)的文章讨论有关项目附件和文件附件之间的差异的详细信息。
  
## <a name="how-are-attachments-represented-programmatically"></a>附件的表示方式以编程方式？

附件存储在 EWS 项集合中。 Attachments 集合的文件附件和/或项附件组成。 有关附件集合的元数据时，可使用 EWS 托管 API [Item.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx)方法或 EWS [GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx)操作获取项目，但其他呼叫需要实际检索附件的内容。 
  
**表 1。有关附件项元数据**

|**元数据实体**|**EWS 托管 API 属性**|**EWS 元素**|
|:-----|:-----|:-----|
|附件指示器 （将不标记内嵌附件）  <br/> |[Item.HasAttachments](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.hasattachments%28v=exchg.80%29.aspx) <br/> |[HasAttachments](http://msdn.microsoft.com/library/538b7a85-11d7-4daa-8458-09b540760e8b%28Office.15%29.aspx) <br/> |
|附件集合  <br/> |[Item.Attachments](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.attachments%28v=exchg.80%29.aspx) <br/> |[附件](http://msdn.microsoft.com/library/b470e614-34bb-44f0-8790-7ddbdcbbd29d%28Office.15%29.aspx) <br/> |
|附件 ID  <br/> |[Attachment.Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.attachment.id%28v=exchg.80%29.aspx) <br/> |[AttachmentId](http://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) <br/> |
   
**表 2。Attachment 实体**

|**附件类型**|**EWS 托管 API 类**|**EWS 元素**|
|:-----|:-----|:-----|
|文件附件  <br/> |[FileAttachment](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.fileattachment%28v=exchg.80%29.aspx) <br/> |[FileAttachment](http://msdn.microsoft.com/library/3ecea174-73d1-47fd-8917-6065cef1d565%28Office.15%29.aspx) <br/> |
|项目附件  <br/> |[ItemAttachment](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemattachment%28v=exchg.80%29.aspx) <br/> [ItemAttachment\<TItem\>](http://msdn.microsoft.com/en-us/library/dd635165%28v=exchg.80%29.aspx) <br/> |[ItemAttachment](http://msdn.microsoft.com/library/089ee599-f45e-46f5-a18a-5cfb3d2851ff%28Office.15%29.aspx) <br/> |
|参考附件  <br/> |[ReferenceAttachmentType 复杂类型 (EWS)](http://msdn.microsoft.com/library/18bfa012-e903-d7f3-528a-31ccceb65463%28Office.15%29.aspx) <br/> |[ReferenceAttachment](http://msdn.microsoft.com/library/b9bde862-6b75-4a81-8033-00a47be4dc2f%28Office.15%29.aspx) <br/> |
   
## <a name="inline-attachments"></a>内嵌附件

内嵌附件的附件的特殊同类。 同时文件附件，项附件可以是内嵌附件。 内嵌附件的正文内容的一部分显示，并保持其相对于其余的内容项中的位置。 
  
附件是内嵌附件，如果 EWS 托管 API [IsInline](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.attachment.isinline%28v=exchg.80%29.aspx)属性或 EWS [IsInline](http://msdn.microsoft.com/library/5e7712c8-372a-4a16-be64-360c5ff3961a%28Office.15%29.aspx)元素设置为 true。 内嵌附件使用下列可选属性和元素标识内嵌附件的位置： 
  
- EWS 托管 API — [ContentId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.attachment.contentid%28v=exchg.80%29.aspx)或[ContentLocation](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.attachment.contentlocation%28v=exchg.80%29.aspx)属性。 
    
- EWS — [ContentId](http://msdn.microsoft.com/library/bc59100d-6079-414b-a6e0-7c15feaa3184%28Office.15%29.aspx)或[ContentLocation](http://msdn.microsoft.com/library/d91cf587-24e3-4c13-8784-5ca29787cca7%28Office.15%29.aspx)元素。 
    
EWS 托管 API [HasAttachments](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.hasattachments%28v=exchg.80%29.aspx)属性和 EWS [HasAttachments](http://msdn.microsoft.com/library/538b7a85-11d7-4daa-8458-09b540760e8b%28Office.15%29.aspx)元素不反映存在的注释的内嵌附件，并具有也称为内嵌附件为什么隐藏附件。 因此，如果 EWS 托管 API [IsInline](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.attachment.isinline%28v=exchg.80%29.aspx)属性或 EWS [IsInline](http://msdn.microsoft.com/library/5e7712c8-372a-4a16-be64-360c5ff3961a%28Office.15%29.aspx)元素设置为 true，并且项目中有无其他附件， **HasAttachments**将设置为 false。 如果您的客户端使用**HasAttachments**填充附件标记或电子邮件上的图标，请注意，图标将不会显示为与内嵌附件的电子邮件。 
  
## <a name="in-this-section"></a>本节内容
<a name="bk_inthissection"> </a>

- [在 Exchange 使用 EWS 添加附件](how-to-add-attachments-by-using-ews-in-exchange.md)
    
- [使用 EWS 在 Exchange 服务器获取附件](how-to-get-attachments-by-using-ews-in-exchange.md)
    
- [使用 EWS 在 Exchange 中删除附件](how-to-delete-attachments-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a>另请参阅
<a name="bk_additionalresources"> </a>

- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)
    
- [文件夹和交换中的 EWS 中的项目](folders-and-items-in-ews-in-exchange.md)
    
- [电子邮件和 Exchange 中的 EWS](email-and-ews-in-exchange.md)
    

