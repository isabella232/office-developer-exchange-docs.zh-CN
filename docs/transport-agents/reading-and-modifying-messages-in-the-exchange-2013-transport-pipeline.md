---
title: 读取和修改 Exchange 2013 传输管道中的邮件
manager: sethgros
ms.date: 09/17/2021
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: b53ed47a-3d01-4c4e-ad32-fb0532872aad
description: 了解 .NET Framework 2013 传输代理中可用于读取、Exchange和修改邮件的类。
ms.openlocfilehash: 5bf4406f7ca82512bb55388e0865e0d343cae66e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59537234"
---
# <a name="reading-and-modifying-messages-in-the-exchange-2013-transport-pipeline"></a>读取和修改 Exchange 2013 传输管道中的邮件

了解 .NET Framework 2013 传输代理中可用于读取、Exchange和修改邮件的类。
  
**适用于：Exchange Server** 2013
  
- 用于读取、写入或修改邮件的类
- 编码器命名空间
- iCalendar 命名空间
- MIME 命名空间
- TextConverters 命名空间
- Tnef 命名空间
- vCard 命名空间
  
当邮件通过传输管道时，传输代理可以在不同的数据格式之间读取、写入和转换邮件内容。 例如，您可以读取和写入 MIME 数据，标识采用 Uuencoded 或 Quoted-printable (qp) 格式的传入邮件，然后将这些邮件转换为组织使用的标准，或者读取然后保存与传入邮件关联的日历或联系人信息。 
  
您还可以标识存在安全威胁的内容，并移动或删除内容或包含这些内容的邮件;例如，通过删除 HTML 邮件中的链接。
  
本文提供有关可用于.NET Framework、写入和修改邮件的类的信息。
  
> [!CAUTION]
> 内容转换 API 中的许多属性和参数允许值足够大，导致性能问题，包括拒绝服务。 在传输代理中使用内容转换 API 时，应该对读取或写入时支持的属性和参数值大小实施限制，以便限制代理的资源消耗。 

<a name="Namespaces"> </a>

## <a name="classes-used-to-read-write-or-modify-messages"></a>用于读取、写入或修改邮件的类

下表列出了可用于.NET Framework、写入和修改电子邮件的类。
  
**.NET Framework邮件处理命名空间**

|**.NET Framework命名空间**|**课程**|
|:-----|:-----|
|[Microsoft。Exchange。Data.Mime.Encoders](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.aspx) <br/> |包含用于内存中编码和解码的类、接受关联枚举中包含的编码器或解码器类之一的编码器流类，以及用于编码器和解码器的 [ByteEncoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.ByteEncoder.aspx) 基类和 [ByteEncoderException](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.ByteEncoderException.aspx) 异常类。  <br/> |
|[Microsoft。Exchange。Data.ContentTypes.iCalendar](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.aspx) <br/> |包含使您能够读取和写入包含日历信息的数据流的类型。 包括日历阅读器和编写器、异常对象、定期对象以及可帮助您返回有关日历项目的属性信息的结构和枚举。  <br/> |
|[Microsoft。Exchange。Data.Mime](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.aspx) <br/> |包含可用于创建、读取、写入、遍历、编码和解码 MIME 数据的类、结构、枚举和委托。 包括基于流的阅读器和编写器，可为你提供对 MIME 数据流的仅向前读取和写入访问权限，以及可用于 MIME 文档的基于 DOM 的方法和类。  <br/> |
|[Microsoft。Exchange。Data.TextConverters](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.aspx) <br/> |包含允许您读取和写入数据流以及执行特定数据类型之间的转换的类、结构、枚举和委托;例如，HTML 到 RTF 格式 (RTF) 。 文本转换器使您能够将文档流的格式从一个表单更改为另一个表单，并有选择地删除可能构成安全风险的文档元素。  <br/> |
|[Microsoft。Exchange。Data.ContentTypes.Tnef](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.aspx) <br/> |包含仅向前流阅读器和编写器、异常类以及有助于读取和写入传输中性封装格式的结构和枚举 (TNEF) 数据。  <br/> |
|[Microsoft。Exchange。Data.ContentTypes.vCard](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.vCard.aspx) <br/> |包含仅向前流阅读器和编写器、异常类以及有助于读取和写入 vCard 格式的联系人数据的结构和枚举。  <br/> |
   
## <a name="encoders-namespace"></a>编码器命名空间
<a name="Encoders"> </a>

Encoders 命名空间包含用于内存中编码和解码的类。 这些类继承自 [ByteEncoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.ByteEncoder.aspx) 基类。 Base64、BinHex、Quoted-printable (qp) 和 Unix-to-Unix (Uu) 的类进行编码和解码。 以下类用于内存中编码和解码： 
  
- [Base64Encoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.Base64Encoder.aspx)
    
- [Base64Decoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.Base64Decoder.aspx)
    
- [BinHexEncoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.BinHexEncoder.aspx)
    
- [BinHexDecoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.BinHexDecoder.aspx)
    
- [QPEncoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.QPEncoder.aspx)
    
- [QPDecoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.QPDecoder.aspx)
    
- [UUEncoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.UUEncoder.aspx)
    
- [UUDecoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.UUDecoder.aspx)
    
编码器和解码器继承自 [ByteEncoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.ByteEncoder.aspx) 基类，并使用 [ByteEncoderException](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.ByteEncoderException.aspx) 异常类进行错误处理。 
  
此外，命名空间包含 [MacBinaryHeader](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.MacBinaryHeader.aspx) 类，该类标识 MacBinary 编码的文件并读取其关联的文件头。 
  
最后 [，EncoderStream](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.EncoderStream.aspx) 类对数据流而不是内存中对象执行转换。 此类接受其中一个编码器或解码器类，并且根据关联的 [EncoderStreamAccess](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.EncoderStreamAccess.aspx) 枚举读取或写入。 
  
## <a name="icalendar-namespace"></a>iCalendar 命名空间
<a name="iCalendar"> </a>

除了支持用于创建、访问和修改 iCalendar 流的结构和类之外，iCalendar 命名空间还为 iCalendar 数据提供仅向前型阅读器和编写器。
  
[CalendarReader 和](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.CalendarReader.aspx) [CalendarWriter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.CalendarWriter.aspx)类用于读取和写入 iCalendar 流数据。 
  
CalendarReader 将可读 [Stream](https://msdn.microsoft.com/library/System.IO.Stream.aspx) 用作其构造函数的参数。 然后，可以使用[ReadFirstChildComponent、ReadNextSiblingComponent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.CalendarReader.ReadFirstChildComponent.aspx)和[](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.CalendarReader.ReadNextSiblingComponent.aspx) [ReadNextComponent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.CalendarReader.ReadNextComponent.aspx)方法按顺序访问数据流中的 iCalendar 组件。 根据为 [ComplianceMode](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.CalendarReader.ComplianceMode.aspx) 属性设置的值，iCalendar 流中的错误将导致引发异常，或会导致 [ComplianceStatus](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.CalendarReader.ComplianceStatus.aspx) 属性设置为 [Compliant](https://msdn.microsoft.com/library/microsoft.exchange.data.contenttypes.icalendar.calendarcompliancestatus.aspx)之外的值。 你可以检查此属性以发现传入 iCalendar 数据的任何问题。 
  
[CalendarWriter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.CalendarWriter.aspx)类将可写入的[Stream](https://msdn.microsoft.com/library/System.IO.Stream.aspx)用作其构造函数的参数。 
  
## <a name="mime-namespace"></a>MIME 命名空间
<a name="MIME"> </a>

MIME 命名空间提供的类使您能够创建、访问和修改 MIME 文档。 可以使用基于流或基于 DOM 的方法处理 MIME 文档。
  
### <a name="mimedocument-class-and-the-mime-dom"></a>MimeDocument 类和 MIME DOM

[MimeDocument](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeDocument.aspx)类允许 DOM 访问 MIME 文档。 当您具有可加载整个 DOM 的可用内存，并且必须随机访问邮件头和内容时，请使用此类型的对象。 
  
使用[GetLoadStream](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeDocument.GetLoadStream.aspx)或 Load 方法将数据加载到[MimeDocument](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeDocument.aspx) [对象](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeDocument.Load.aspx)中。 然后，你可以演练 DOM 层次结构并创建、修改或删除 MIME 数据。 修改 MIME 数据后，可以使用 [WriteTo](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeNode.WriteTo.aspx) 方法之一将该数据写入流。 
  
下图显示了 [MimeDocument](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeDocument.aspx) 对象中的数据结构。 
  
**图 1.MimeDocument 对象的结构**

![MIME DOM 体系结构](media/MimeDomArchitecture.gif)
  
### <a name="mimereader-and-mimewriter-classes-and-stream-based-mime-parsing"></a>MimeReader 和 MimeWriter 类以及基于流的 MIME 分析

[MimeReader 和](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeReader.aspx) [MimeWriter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeWriter.aspx)类支持对 MIME 流的仅向前访问。 无需更改需要已读或写数据的 MIME 数据时，请使用这些类。 例如，如果你想要打印符合预定义格式的邮件 [，MimeWriter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeWriter.aspx) 类可能很理想。 
  
[MimeDocument](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeDocument.aspx)类封装 DOM。 [MimeReader 和](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeReader.aspx) [MimeWriter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeWriter.aspx)类表示状态计算机。 它们状态根据收到的输入和调用的方法而更改。 图 2 到图 5 是简化的状态转换图，显示 [MimeReader](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeReader.aspx) 对象，哪些方法从每个状态调用有效以及将产生的状态。 
  
若要使用这些图表，请遵循从一个状态到下一个状态箭头，并请注意方法调用或返回导致状态更改的值。 例如，第一个图表中，假定您位于属于已创建的 MimeReader 的流的起始位置。 若要进入部件标头状态，请按该顺序调用 [ReadNextPart](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeReader.ReadNextPart.aspx) 或 [ReadFirstChildPart](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeReader.ReadFirstChildPart.aspx)之一。 如果存在标头 (，即，如果 MIME 格式) ，您将进入"部件标头"状态。 否则，将引发异常。 
  
**图 2.MimeReader 对象的简化状态转换图**

![MimeReader 状态图表](media/MimeReader_StateDiagram_01.gif)
  
> [!NOTE]
> 图 3、4 和 5 展开以上各图中所示状态。 
  
**图 3.图 2 中的部件标头状态扩展**

![“部件标题”状态扩展](media/MimeReader_StateDiagram_02.gif)
  
**图 4.在标头中遇到参数时，展开图 3 中的标头状态**

![在标头中遇到参数时展开"部件标头"状态](media/MimeReader_StateDiagram_03.gif)
  
> [!NOTE]
> 图 5 表示的状态是递归的，如果遇到地址组，可以使用 [GroupRecipientReader](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeAddressReader.GroupRecipientReader.aspx) 属性读取该组中的地址。 
  
**图 5.在遇到地址或地址组时，从图 3 展开头状态**

![用于地址或组的“标题”状态扩展](media/MimeReader_StateDiagram_04.gif)
  
图 6 和图 7 显示了 [MimeWriter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeWriter.aspx) 对象的简化状态转换图。 
  
> [!NOTE]
> 图 7 展开图 6 中所示的部件标头状态。 
  
**图 6.MimeWriter 对象的简化状态转换图**

![用于 MimeWriter 的状态切换图表](media/MimeWriter_TopLevel.gif)
  
**图 7.图 6 中的部件标头状态扩展**

![用于 MimeWriter 的状态切换图表扩展](media/MimeWriter_Diagram_Expansion.gif)
  
## <a name="textconverters-namespace"></a>TextConverters 命名空间
<a name="TextConverters"> </a>

TextConverters 命名空间包含支持电子邮件内容的转换的类型。 这些类型可以执行代码页转换、删除不安全 HTML，以及对电子邮件正文执行其他转换。 [Microsoft.Exchange。Data.TextConverters](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.aspx)命名空间包括从[TextConverter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.TextConverter.aspx)抽象类派生的以下类： 
  
- [EnrichedToHtml](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.EnrichedToHtml.aspx)
    
- [EnrichedToText](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.EnrichedToText.aspx)
    
- [HtmlToEnriched](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.HtmlToEnriched.aspx)
    
- [HtmlToHtml](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.HtmlToHtml.aspx)
    
- [HtmlToRtf](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.HtmlToRtf.aspx)
    
- [HtmlToText](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.HtmlToText.aspx)
    
- [RtfCompressedToRtf](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.RtfCompressedToRtf.aspx)
    
- [RtfToHtml](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.RtfToHtml.aspx)
    
- [RtfToRtf](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.RtfToRtf.aspx)
    
- [RtfToRtfCompressed](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.RtfToRtfCompressed.aspx)
    
- [RtfToText](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.RtfToText.aspx)
    
- [TextToHtml](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.TextToHtml.aspx)
    
- [TextToRtf](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.TextToRtf.aspx)
    
- [TextToText](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.TextToText.aspx)
    
这些文本转换器使您能够更改文档流的格式或删除非 HTML 文档安全的元素。 这些类本身可用于通过使用对 [TextConverter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.TextConverter.aspx) 基类中的 Convert 方法之一的单个调用来执行转换，也可以将它们传递给转换器的构造函数，转换器使用该构造函数执行转换读取或写入。 
  
当您有足够的空间来存储原始文档及其转换的输出时，或者当您希望存储转换结果时，从基类继承的功能对于执行转换非常有用。 **Convert** 方法采用输入和输出流、文本阅读器或文本编写器，并将输入的内容转换为关联的输出。 
  
命名空间中还包括以下文本阅读器、编写器以及流类：
  
- [ConverterReader](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.ConverterReader.aspx) — 派生自 **System.IO.TextReader**。 
    
- [ConverterWriter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.ConverterWriter.aspx) — 派生自 **System.IO.TextWriter**。 
    
- [ConverterStream](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.ConverterStream.aspx) — 派生自 **System.IO.Stream**。 
    
当你没有空间来存储原始或转换的输出时，当你从流接收输入或将输出发送到流时，或者当你希望输出仅用于索引或搜索目的，因此不希望存储转换结果时，它们用于执行转换。
  
## <a name="tnef-namespace"></a>Tnef 命名空间
<a name="TNEF"> </a>

Tnef 命名空间包含一些类和类型，这些类和类型支持对 TNEF 数据进行仅向前流读取和写入。 TNEF 是一种数据格式，用于封装无法解释 MAPI 的客户端的 MAPI 属性。
  
[TnefReader](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefReader.aspx)和[TnefWriter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefWriter.aspx)类提供[Microsoft.Exchange 中的核心Exchange。Data.ContentTypes.Tnef](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.aspx)命名空间。 
  
[TnefReader](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefReader.aspx)类将可读流用作其构造函数的参数。 然后，使用 [ReadNextAttribute](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefReader.ReadNextAttribute.aspx) 方法按顺序读取 TNEF 流中的属性。 读取属性后，除了获取[TnefPropertyReader](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefPropertyReader.aspx)读取当前属性外，您还可以使用[TnefReader](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefReader.aspx)对象的任何只读属性访问有关该属性的信息。 您还可以使用 [ReadAttributeRawValue](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefReader.ReadAttributeRawValue.aspx) 方法直接访问当前属性。 
  
[TnefWriter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefWriter.aspx)类将可写入的[Stream](https://msdn.microsoft.com/library/System.IO.Stream.aspx)用作其构造函数的参数。 [TnefWriter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefWriter.aspx)类提供了多种将数据写入此流的方法。 
  
## <a name="vcard-namespace"></a>vCard 命名空间
<a name="vCard"> </a>

vCard 命名空间包含用于读取和写入电子邮件中以 vCard 数据格式包含的联系人信息的类、结构和枚举。 命名空间包含联系人读者和编写器、异常类、属性读取器、参数读取器和支持枚举，这些枚举允许您读取与电子邮件关联的 vCard 数据。
  
## <a name="see-also"></a>另请参阅

- [Exchange 中的传输代理](transport-agents-in-exchange-2013.md)  
- [Exchange 2013 中的传输代理概念](transport-agent-concepts-in-exchange-2013.md) 
- [Exchange 2013 的传输代理参考](transport-agent-reference-for-exchange-2013.md)
- [MIME 媒体类型](http://www.iana.org/assignments/media-types)
    

