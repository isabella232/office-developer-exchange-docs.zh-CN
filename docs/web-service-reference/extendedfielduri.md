---
title: ExtendedFieldURI
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExtendedFieldURI
api_type:
- schema
ms.assetid: b3c6ea3a-9ead-44b9-9d99-64ecf12bde23
description: ExtendedFieldURI 元素标识一个扩展的 MAPI 属性。
ms.openlocfilehash: fd365010016c68236107991717ed538c97dc0d50
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526030"
---
# <a name="extendedfielduri"></a>ExtendedFieldURI

**ExtendedFieldURI**元素标识一个扩展的 MAPI 属性。 
  
```xml
<ExtendedFieldURI DistinguishedPropertySetId="" PropertySetId="" PropertyTag="" PropertyName="" PropertyId="" PropertyType="" />
```

**PathToExtendedFieldType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**DistinguishedPropertySetId** <br/> |定义扩展 MAPI 属性的已知属性集 Id。<br/><br/>如果使用此属性，则不能使用**PropertySetId**和**PropertyTag**属性。 此属性必须与**PropertyId**或**PropertyName**属性一起使用，并且必须与**recordtype**属性一起使用。<br/><br/>本主题后面的**DistinguishedPropertySetId**属性表列出了此属性的可能值。<br/><br/>此特性是可选的。  <br/> |
|**PropertySetId** <br/> |通过识别 GUID 标识 MAPI 扩展属性集或命名空间。<br/><br/>如果使用此属性，则不能使用**DistinguishedPropertySetId**和**PropertyTag**属性。 此属性必须与**PropertyId**或**PropertyName**属性一起使用，并且必须与**recordtype**属性一起使用。<br/><br/>此特性是可选的。  <br/> |
|**PropertyTag** <br/> |标识不包含类型部分标记的属性标记。 **PropertyTag**可以表示为十六进制或短整型。<br/><br/>0x8000 和0xFFFE 之间的范围表示属性的自定义范围。 当邮箱数据库首次遇到自定义属性时，它会将该自定义属性分配给0xFFFE 的自定义属性范围内的属性标记。 给定的自定义属性标记很可能在不同的数据库中。 因此，按属性标记的自定义属性请求可能会在不同的数据库上返回不同的属性。 对自定义属性禁止使用**PropertyTag**属性。 而是使用**PropertySetId**属性和**PropertyName**或**PropertyId**属性。<br/><br/>**重要说明**：使用 GUID + 名称/ID 访问0X8000 和0xFFFE 之间的任何自定义属性。 如果使用了**PropertyTag**属性，则不能使用**DistinguishedPropertySetId**、 **PropertySetId**、 **PropertyName**和**PropertyId**属性。<br/><br/>此特性是可选的。<br/><br/>**注意**：不能对自定义范围0x8000 中的属性使用属性 Tag 属性0xFFFE。 在这种情况下，您必须使用命名属性。           |
|**PropertyName** <br/> |按其名称标识扩展属性。 此属性必须与**DistinguishedPropertySetId**或**PropertySetId**结合使用。<br/><br/>如果使用此属性，则不能使用**PropertyId**和**PropertyTag**属性。<br/><br/>此特性是可选的。  <br/> |
|**PropertyId** <br/> |按其调度 ID 标识扩展属性。 可以通过十进制或十六进制格式标识调度 ID。 此属性必须与**DistinguishedPropertySetId**或**PropertySetId**结合使用。<br/><br/>如果使用此属性，则不能使用**PropertyName**和**PropertyTag**属性。<br/><br/>此特性是可选的。  <br/> |
|**Recordtype** <br/> |表示属性标记的属性类型。 这对应于属性标记中的最不重要的单词。<br/><br/>本主题后面的 Recordtype 属性表包含此属性的可能值。<br/><br/>此特性是必需的。  <br/> |
   
#### <a name="distinguishedpropertysetid-attribute"></a>DistinguishedPropertySetId 属性

|**值**|**说明**|
|:-----|:-----|
|地址  <br/> |按名称标识 address 属性集 ID。  <br/> |
|Appointment  <br/> |按名称标识约会属性集 ID。  <br/> |
|CalendarAssistant  <br/> |按名称标识日历助理属性集 ID。  <br/> |
|常见  <br/> |按名称标识通用属性集 ID。  <br/> |
|InternetHeaders  <br/> |按名称标识 Internet 标头属性集 ID。  <br/> |
|要求  <br/> |按名称标识会议属性集 ID。  <br/> |
|共享  <br/> | <br/> |
|PublicStrings  <br/> |按名称标识公共字符串属性集 ID。  <br/> |
|任务  <br/> |按名称标识任务属性集 ID。  <br/> |
|UnifiedMessaging  <br/> |按名称标识统一消息属性集 ID。  <br/> |
   
#### <a name="propertytype-attribute"></a>Recordtype 属性

|**值**|**说明**|
|:-----|:-----|
|ApplicationTime  <br/> |一个被解释为日期和时间的双精度值。 整数部分是日期，小数部分是时间。  <br/> |
|ApplicationTimeArray  <br/> |将被解释为日期和时间的双精度型值组成的数组。  <br/> |
|Binary  <br/> |Base64 编码的二进制值。  <br/> |
|BinaryArray  <br/> |一个由 Base64 编码的二进制值组成的数组。  <br/> |
|Boolean  <br/> |布尔值**true**或**false**。  <br/> |
|CLSID  <br/> |一个 GUID 字符串。  <br/> |
|CLSIDArray  <br/> |GUID 字符串的数组。  <br/> |
|货币  <br/> |一个64位整数，它被解释为美分数。  <br/> |
|CurrencyArray  <br/> |一个由64位整数组成的数组，该数组被解释为美分数。  <br/> |
|双精度  <br/> |64位浮点值。  <br/> |
|DoubleArray  <br/> |64位浮点值的数组。  <br/> |
|错误  <br/> |SCODE 值;32位无符号整数。  <br/> 不用于限制或获取/设置值。 这仅适用于报告。  <br/> |
|浮点  <br/> |32位浮点值。  <br/> |
|FloatArray  <br/> |32位浮点值的数组。  <br/> |
|Integer  <br/> |一个已签名的32位（Int32）整数。  <br/> |
|IntegerArray  <br/> |一个由已签名的32位（Int32）整数组成的数组。  <br/> |
|长型  <br/> |一个已签名或未签名的64位（Int64）整数。  <br/> |
|LongArray  <br/> |已签名或未签名的64位（Int64）整数的数组。  <br/> |
|NULL  <br/> |指示无属性值。  <br/> 不用于限制或获取/设置值。 这仅适用于报告。  <br/> |
|对象  <br/> |指向实现 IUnknown 接口的对象的指针。  <br/> 不用于限制或获取/设置值。 这仅适用于报告。  <br/> |
|ObjectArray  <br/> |指向实现 IUnknown 接口的对象的指针数组。  <br/> 不用于限制或获取/设置值。 这仅适用于报告。  <br/> |
|短  <br/> |一个有符号的16位整数。  <br/> |
|ShortArray  <br/> |一个由带符号的16位整数组成的数组。  <br/> |
|SystemTime  <br/> |一个以 FILETIME 结构形式表示的64位整数数据和时间值。  <br/> |
|SystemTimeArray  <br/> |以 FILETIME 结构形式的64位整数数据和时间值的数组。  <br/> |
|String  <br/> |一个 Unicode 字符串。  <br/> |
|StringArray  <br/> |Unicode 字符串的数组。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ExtendedProperty](extendedproperty.md) <br/> |标识文件夹和项的扩展属性。  <br/> |
|[AdditionalProperties](additionalproperties.md) <br/> | 标识其他属性。<br/><br/>下面是此元素的 XPath 表达式：<br/><br/>`/FindFolder/FolderShape/AdditionalProperties` <br/>  `/GetFolder/FolderShape/AdditionalProperties` <br/>  `/SyncFolderHierarchy/FolderShape/AdditionalProperties` <br/>  `/GetItem/ItemShape/AdditionalProperties` <br/>  `/FindItem/ItemShape/AdditionalProperties` <br/>  `/SyncFolderItems/ItemShape/AdditionalProperties` <br/>  `/GetAttachment/AttachmentShape/AdditionalProperties` <br/> |
|[SetItemField](setitemfield.md) <br/> |表示对[UpdateItem 操作](updateitem-operation.md)中项的单个属性的更新。  <br/> |
|[SetFolderField](setfolderfield.md) <br/> |表示对[UpdateFolder Operation](updatefolder-operation.md)中的文件夹上的单个属性的更新。  <br/> |
|[DeleteItemField](deleteitemfield.md) <br/> |表示在[UpdateItem 操作](updateitem-operation.md)过程中从项中删除给定属性的删除操作。  <br/> |
|[DeleteFolderField](deletefolderfield.md) <br/> |表示在 UpdateFolder 调用过程中从文件夹中删除给定属性的删除操作。  <br/> |
|[AppendToItemField](appendtoitemfield.md) <br/> |标识在[UpdateItem 操作](updateitem-operation.md)过程中追加到项的单个属性的数据。  <br/> |
|[AppendToFolderField](appendtofolderfield.md) <br/> |指定要在[UpdateFolder Operation](updatefolder-operation.md)期间追加到文件夹属性数据。  <br/> |
|[Exists](exists.md) <br/> |表示在项上存在提供的属性时返回**true**的搜索表达式。  <br/> |
|[FieldURIOrConstant](fielduriorconstant.md) <br/> |表示与其他属性进行比较时要使用的属性或常数值。  <br/> |
|[IsEqualTo](isequalto.md) <br/> |表示搜索表达式，该表达式将属性与常数值或其他属性进行比较，如果它们相等，则计算结果为**true** 。  <br/> |
|[IsGreaterThan](isgreaterthan.md) <br/> |表示用于将属性与常数值或其他属性进行比较的搜索表达式，如果第一个属性较大，则返回**true** 。  <br/> |
|[IsGreaterThanOrEqualTo](isgreaterthanorequalto.md) <br/> |表示一个搜索表达式，该表达式将属性与一个常数值或另一个属性进行比较，如果第一个属性大于或等于第二个属性，**则返回 true** 。  <br/> |
|[IsLessThan](islessthan.md) <br/> |表示一个搜索表达式，该表达式将属性与一个常量值或另一个属性进行比较，如果第一个属性小于第二个属性，则返回**true** 。  <br/> |
|[IsLessThanOrEqualTo](islessthanorequalto.md) <br/> |表示一个搜索表达式，该表达式将属性与一个常量值或另一个属性进行比较，如果第一个属性小于第二个属性，则返回**true** 。  <br/> |
|[IsNotEqualTo](isnotequalto.md) <br/> |表示用于将属性与常量值或其他属性进行比较的搜索表达式，如果值不相同，**则返回 true** 。  <br/> |
|[不包括](excludes.md) <br/> |执行这些属性的位掩码。  <br/> |
|[Contains](contains.md) <br/> |表示一个搜索表达式，该表达式确定给定属性是否包含提供的常量字符串值。  <br/> |
|[FieldOrder](fieldorder.md) <br/> |代表对结果进行排序所依据的单个字段，并指示排序的方向。  <br/> |
   
## <a name="remarks"></a>备注

有些属性不能与其他属性结合使用。 任何传入的扩展属性属性组合无效的请求都将生成错误消息。
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
> [!NOTE]
> 在 Microsoft .NET 中，Long 是一个64位带符号整数，而在 MAPI 和 COM 中，Long 为32位整数。 大多数开发人员将使用 Microsoft.NET 框架开发 Exchange Web 服务客户端应用程序。 因此，使用的是 .NET 命名，而不是 MAPI 命名。
> 
> 例如，PR_MESSAGE_FLAGS MAPI 属性0x0E07 是 \_ LONG 类型。 在 .NET 中，这被视为一个整数。 PR_MESSAGE_FLAGS 的扩展属性定义为 `<t:ExtendedFieldURI PropertyTag="0x0E07" PropertyType="Integer"/>` 。 
  
## <a name="example"></a>示例

下面的请求示例将创建一个具有两个自定义属性的项。 第一个自定义属性的名称为**IsMyHouse** ，其布尔值设置为**true**。 第二个自定义扩展属性名为**HousePrices**。 它包含一个货币值数组。 
  
```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" 
                  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
    MessageDisposition="SaveOnly">
      <SavedItemFolderId>
        <t:DistinguishedFolderId Id="inbox"/>
      </SavedItemFolderId>
      <Items>
        <t:Item>
          <t:ItemClass>IPM.Note</t:ItemClass>
          <t:Subject>Create an extended property</t:Subject>
          <t:Body BodyType="Text">Added info to extended props</t:Body>
          <t:ExtendedProperty>
            <t:ExtendedFieldURI DistinguishedPropertySetId="PublicStrings" 
                                PropertyName="IsMyHouse" 
                                PropertyType="Boolean"/>
            <t:Value>true</t:Value>
          </t:ExtendedProperty>
          <t:ExtendedProperty>
            <t:ExtendedFieldURI DistinguishedPropertySetId="PublicStrings" 
                                PropertyName="HousePrices" 
                                PropertyType="CurrencyArray"/>
            <t:Values>
              <t:Value>30000000</t:Value>
              <t:Value>40000000</t:Value>
              <t:Value>50000000</t:Value>
            </t:Values>
          </t:ExtendedProperty>
        </t:Item>
      </Items>
    </CreateItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [FieldURI](fielduri.md)
- [IndexedFieldURI](indexedfielduri.md)
- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

