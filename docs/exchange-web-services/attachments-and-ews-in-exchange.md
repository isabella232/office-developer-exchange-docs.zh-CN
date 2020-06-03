---
title: 附件和 EWS Exchange 中
manager: sethgros
ms.date: 7/11/2016
ms.audience: Developer
ms.assetid: 8e4289a4-ec9d-4502-9854-c593c95d5f98
description: 了解附件以及你的 EWS 托管 API 或 Exchange 客户端中的 EWS 如何表示这些附件。
localization_priority: Priority
ms.openlocfilehash: d37fef9ea14a3b42a0eed0240724fe69c8531c93
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528487"
---
# <a name="attachments-and-ews-in-exchange"></a>附件和 EWS Exchange 中

了解附件以及你的 EWS 托管 API 或 Exchange 客户端中的 EWS 如何表示这些附件。
  
通常情况下，附件与电子邮件项目相关联，但实际上，所有 EWS 项目（电子邮件、日历项目、联系人、任务）都可以包含附件。
  
## <a name="types-of-attachments"></a>附件类型

EWS 将附件分类为两个组：文件附件和项目附件。
  
- **项目附件：** 附加到另一个强类型 EWS 项的强类型[ews 项](folders-and-items-in-ews-in-exchange.md)，如电子邮件和日历项。 可以使用 EWS 托管 API 或 EWS 创建的任何强类型项目都可用作项目附件。 项目附件的内容是强类型的项目，它提供了对其所有属性的轻松访问。 项目附件可以拥有自己的项目附件，因此可能会有项目附件（或附件的嵌套）的层次结构。
    
- **文件附件：** 任何文件，如 .txt、.jpg、.zip、.pdf，甚至是 .msg 文件。 文件附件仅具有几个属性，其中一个属性是文件的以64为基础的编码内容。 
    
- **引用附件：** 由文件提供程序引用的任何附件，如位于云中的文件。 附件可以来自多个提供程序。 
    
当您在项目中添加或检索附件时，您将根据它是文件附件还是项目附件以不同的方式执行此操作。 例如，若要将文件附件添加到项目中，只需传入文件的位置即可。 若要将现有项目添加为项目附件，您必须将现有项目的属性或 MIME 内容复制到新项目附件中。您不能只绑定到现有项。 因此，区分这两种类型的附件非常重要。 [本节中](#bk_inthissection)的文章讨论了有关项目附件和文件附件之间的差异的更多详细信息。
  
## <a name="how-are-attachments-represented-programmatically"></a>附件是如何以编程方式表示的？

附件存储在 EWS 项的集合中。 附件集合由文件附件和/或项目附件组成。 使用 EWS 托管 API Item 获取项目时，将提供有关附件集合的元数据[。 Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx)方法或 EWS [GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx)操作，但需要进行额外的调用以实际检索附件的内容。 
  
**表1。有关附件的项元数据**

|**元数据实体**|**EWS 托管 API 属性**|**EWS 元素**|
|:-----|:-----|:-----|
|附件指示器（不标记内嵌附件）  <br/> |[HasAttachments](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.hasattachments%28v=exchg.80%29.aspx) <br/> |[HasAttachments](https://msdn.microsoft.com/library/538b7a85-11d7-4daa-8458-09b540760e8b%28Office.15%29.aspx) <br/> |
|附件集合  <br/> |[项附件](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.attachments%28v=exchg.80%29.aspx) <br/> |[附件](https://msdn.microsoft.com/library/b470e614-34bb-44f0-8790-7ddbdcbbd29d%28Office.15%29.aspx) <br/> |
|附件 ID  <br/> |[Attachment.Id](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachment.id%28v=exchg.80%29.aspx) <br/> |[AttachmentId](https://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) <br/> |
   
**表2。附件实体**

|**附件类型**|**EWS 托管 API 类**|**EWS 元素**|
|:-----|:-----|:-----|
|文件附件  <br/> |[FileAttachment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.fileattachment%28v=exchg.80%29.aspx) <br/> |[FileAttachment](https://msdn.microsoft.com/library/3ecea174-73d1-47fd-8917-6065cef1d565%28Office.15%29.aspx) <br/> |
|项目附件  <br/> |[ItemAttachment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemattachment%28v=exchg.80%29.aspx) <br/> [ItemAttachment\<TItem\>](https://msdn.microsoft.com/library/dd635165%28v=exchg.80%29.aspx) <br/> |[ItemAttachment](https://msdn.microsoft.com/library/089ee599-f45e-46f5-a18a-5cfb3d2851ff%28Office.15%29.aspx) <br/> |
|参考附件  <br/> |[ReferenceAttachmentType 复杂类型（EWS）](https://msdn.microsoft.com/library/18bfa012-e903-d7f3-528a-31ccceb65463%28Office.15%29.aspx) <br/> |[ReferenceAttachment](https://msdn.microsoft.com/library/b9bde862-6b75-4a81-8033-00a47be4dc2f%28Office.15%29.aspx) <br/> |
   
## <a name="inline-attachments"></a>内嵌附件

内嵌附件是一种特殊的附件。 文件附件和项目附件都可以是内嵌附件。 内联附件显示为正文内容的一部分，并保持其相对于项目中其余内容的位置。 
  
如果 EWS Managed API [IsInline](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachment.isinline%28v=exchg.80%29.aspx)属性或 ews [IsInline](https://msdn.microsoft.com/library/5e7712c8-372a-4a16-be64-360c5ff3961a%28Office.15%29.aspx)元素设置为 true，则附件是内嵌附件。 内联附件使用以下可选属性和元素来标识内嵌附件的位置： 
  
- EWS 托管 API — [ContentId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachment.contentid%28v=exchg.80%29.aspx)或[ContentLocation](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachment.contentlocation%28v=exchg.80%29.aspx)属性。 
    
- EWS — [ContentId](https://msdn.microsoft.com/library/bc59100d-6079-414b-a6e0-7c15feaa3184%28Office.15%29.aspx)或[ContentLocation](https://msdn.microsoft.com/library/d91cf587-24e3-4c13-8784-5ca29787cca7%28Office.15%29.aspx)元素。 
    
请注意，EWS Managed API [HasAttachments](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.hasattachments%28v=exchg.80%29.aspx)属性和 ews [HasAttachments](https://msdn.microsoft.com/library/538b7a85-11d7-4daa-8458-09b540760e8b%28Office.15%29.aspx)元素不反映内联附件的存在，这就是为什么嵌入式附件也称为隐藏附件的原因所在。 因此，如果您将 EWS Managed API [IsInline](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachment.isinline%28v=exchg.80%29.aspx)属性或 ews [IsInline](https://msdn.microsoft.com/library/5e7712c8-372a-4a16-be64-360c5ff3961a%28Office.15%29.aspx)元素设置为 true，并且该项目没有其他附件，则**HasAttachments**将设置为 false。 如果您的客户端使用**HasAttachments**填充电子邮件上的附件指示器或图标，请注意，带有内嵌附件的电子邮件不会显示该图标。 
  
## <a name="in-this-section"></a>本节内容
<a name="bk_inthissection"> </a>

- [使用 Exchange 中的 EWS 添加附件](how-to-add-attachments-by-using-ews-in-exchange.md)
    
- [使用 Exchange 中的 EWS 获取附件](how-to-get-attachments-by-using-ews-in-exchange.md)
    
- [使用 Exchange 中的 EWS 删除附件](how-to-delete-attachments-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a>另请参阅
<a name="bk_additionalresources"> </a>

- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)
    
- [文件夹和交换中的 EWS 中的项目](folders-and-items-in-ews-in-exchange.md)
    
- [电子邮件和 Exchange 中的 EWS](email-and-ews-in-exchange.md)
    

