---
title: ExtendedFieldURI
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ExtendedFieldURI
api_type:
- schema
ms.assetid: b3c6ea3a-9ead-44b9-9d99-64ecf12bde23
description: ExtendedFieldURI 元素标识扩展的 MAPI 属性。
ms.openlocfilehash: 0cf3926c900e1b1f35018c6706cfe99ebefbe76f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542314"
---
# <a name="extendedfielduri"></a>ExtendedFieldURI

**ExtendedFieldURI** 元素标识扩展的 MAPI 属性。 
  
```xml
<ExtendedFieldURI DistinguishedPropertySetId="" PropertySetId="" PropertyTag="" PropertyName="" PropertyId="" PropertyType="" />
```

**PathToExtendedFieldType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**DistinguishedPropertySetId** <br/> |定义扩展 MAPI 属性的已知属性集 ID。<br/><br/>如果使用此属性，则 **不能使用 PropertySetId** 和 **PropertyTag** 属性。 此属性必须与 **PropertyId** 或 **PropertyName** 属性以及 **PropertyType** 属性一同使用。<br/><br/>本主题 **稍后介绍的 DistinguishedPropertySetId** 属性表列出了此属性的可能值。<br/><br/>此特性是可选的。  <br/> |
|**PropertySetId** <br/> |通过 MAPI 扩展属性集或命名空间的标识 GUID 来标识该属性集或命名空间。<br/><br/>如果使用此属性，则 **不能使用 DistinguishedPropertySetId** 和 **PropertyTag** 属性。 此属性必须与 **PropertyId** 或 **PropertyName** 属性以及 **PropertyType** 属性一同使用。<br/><br/>此特性是可选的。  <br/> |
|**PropertyTag** <br/> |标识不带标记类型部分的属性标记。 **PropertyTag** 可以表示为十六进制或短整数。<br/><br/>属性和0x8000之间的0xFFFE表示属性的自定义范围。 当邮箱数据库首次遇到自定义属性时，它会向该自定义属性分配一个属性标记，该标记位于 0x8000-0xFFFE。 给定的自定义属性标记很可能因数据库不同而不同。 因此，按属性标记的自定义属性请求可返回不同数据库上的不同属性。 自定义属性禁止使用 **PropertyTag** 属性。 请改为使用 **PropertySetId** 属性和 **PropertyName 或** **PropertyId** 属性。<br/><br/>**重要** 提示：使用 GUID + 名称/ID 访问 0x8000 和 0xFFFE 之间的任何自定义属性。 如果使用 **PropertyTag** 属性，则 **不能使用 DistinguishedPropertySetId、PropertySetId、PropertyName** 和 **PropertyId** 属性。  <br/><br/>此特性是可选的。<br/><br/>**注意**：不能将属性标记属性用于自定义范围内 0x8000-0xFFFE。 在这种情况下，必须使用命名属性。           |
|**PropertyName** <br/> |按名称标识扩展属性。 此属性必须与 **DistinguishedPropertySetId** 或 **PropertySetId 结合**。<br/><br/>如果使用此属性，则 **不能使用 PropertyId** 和 **PropertyTag** 属性。<br/><br/>此特性是可选的。  <br/> |
|**PropertyId** <br/> |按其调度 ID 标识扩展属性。 调度 ID 可以使用十进制或十六进制格式进行标识。 此属性必须与 **DistinguishedPropertySetId** 或 **PropertySetId 结合**。<br/><br/>如果使用此属性，则 **不能使用 PropertyName** 和 **PropertyTag** 属性。<br/><br/>此特性是可选的。  <br/> |
|**PropertyType** <br/> |表示属性标记的属性类型。 这与属性标记中最不重要的单词相对应。<br/><br/>本主题稍后介绍的 PropertyType 属性表包含此属性的可能值。<br/><br/>此特性是必需的。  <br/> |
   
#### <a name="distinguishedpropertysetid-attribute"></a>DistinguishedPropertySetId 属性

|**值**|**说明**|
|:-----|:-----|
|地址  <br/> |按名称标识地址属性集 ID。  <br/> |
|Appointment  <br/> |按名称标识约会属性集 ID。  <br/> |
|CalendarAssistant  <br/> |按名称标识日历助理属性集 ID。  <br/> |
|常见  <br/> |按名称标识公共属性集 ID。  <br/> |
|InternetHeaders  <br/> |按名称标识 Internet 标头属性集 ID。  <br/> |
|会议  <br/> |按名称标识会议属性集 ID。  <br/> |
|共享  <br/> | <br/> |
|PublicStrings  <br/> |按名称标识公共字符串属性集 ID。  <br/> |
|任务  <br/> |按名称标识任务属性集 ID。  <br/> |
|UnifiedMessaging  <br/> |按名称标识统一消息属性集 ID。  <br/> |
   
#### <a name="propertytype-attribute"></a>PropertyType 属性

|**值**|**说明**|
|:-----|:-----|
|ApplicationTime  <br/> |解释为日期和时间的双精度值。 整数部分为日期，小数部分为时间。  <br/> |
|ApplicationTimeArray  <br/> |解释为日期和时间的双值数组。  <br/> |
|二进制  <br/> |Base64 编码的二进制值。  <br/> |
|BinaryArray  <br/> |Base64 编码的二进制值的数组。  <br/> |
|Boolean  <br/> |Boolean **true 或** **false**。  <br/> |
|CLSID  <br/> |GUID 字符串。  <br/> |
|CLSIDArray  <br/> |GUID 字符串数组。  <br/> |
|货币  <br/> |解释为分数的 64 位整数。  <br/> |
|CurrencyArray  <br/> |解释为分数的 64 位整数数组。  <br/> |
|双精度  <br/> |64 位浮点值。  <br/> |
|DoubleArray  <br/> |64 位浮点值的数组。  <br/> |
|错误  <br/> |SCODE 值;32 位无符号整数。  <br/> 不用于限制或获取/设置值。 这仅针对报告存在。  <br/> |
|浮点  <br/> |32 位浮点值。  <br/> |
|FloatArray  <br/> |一个 32 位浮点值的数组。  <br/> |
|整数  <br/> |有符号的 32 位 (Int32) 整数。  <br/> |
|IntegerArray  <br/> |由 32 位和 Int32 (有符号) 数组。  <br/> |
|长型  <br/> |有符号或无符号的 64 位 (Int64) 整数。  <br/> |
|LongArray  <br/> |由 64 位或无符号的 64 位 (Int64) 数组。  <br/> |
|NULL  <br/> |指示没有属性值。  <br/> 不用于限制或获取/设置值。 这仅针对报告存在。  <br/> |
|Object  <br/> |指向实现 IUnknown 接口的对象的指针。  <br/> 不用于限制或获取/设置值。 这仅针对报告存在。  <br/> |
|ObjectArray  <br/> |指向实现 IUnknown 接口的对象的指针数组。  <br/> 不用于限制或获取/设置值。 这仅针对报告存在。  <br/> |
|短  <br/> |有符号 16 位整数。  <br/> |
|ShortArray  <br/> |一个包含 16 位有符号整数的数组。  <br/> |
|SystemTime  <br/> |64 位整数数据和时间值，格式为 FILETIME 结构。  <br/> |
|SystemTimeArray  <br/> |FILETIME 结构形式的 64 位整数数据和时间值的数组。  <br/> |
|String  <br/> |Unicode 字符串。  <br/> |
|StringArray  <br/> |Unicode 字符串数组。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ExtendedProperty](extendedproperty.md) <br/> |标识文件夹和项目的扩展属性。  <br/> |
|[AdditionalProperties](additionalproperties.md) <br/> | 标识其他属性。<br/><br/>下面是此元素的 XPath 表达式：<br/><br/>`/FindFolder/FolderShape/AdditionalProperties` <br/>  `/GetFolder/FolderShape/AdditionalProperties` <br/>  `/SyncFolderHierarchy/FolderShape/AdditionalProperties` <br/>  `/GetItem/ItemShape/AdditionalProperties` <br/>  `/FindItem/ItemShape/AdditionalProperties` <br/>  `/SyncFolderItems/ItemShape/AdditionalProperties` <br/>  `/GetAttachment/AttachmentShape/AdditionalProperties` <br/> |
|[SetItemField](setitemfield.md) <br/> |表示对 [UpdateItem](updateitem-operation.md)操作中某个项目的单个属性的更新。  <br/> |
|[SetFolderField](setfolderfield.md) <br/> |表示对[UpdateFolder Operation](updatefolder-operation.md)中的文件夹上的单个属性的更新。  <br/> |
|[DeleteItemField](deleteitemfield.md) <br/> |表示在 UpdateItem 操作期间从项中删除给定属性 [的删除操作](updateitem-operation.md)。  <br/> |
|[DeleteFolderField](deletefolderfield.md) <br/> |表示在 UpdateFolder 调用期间从文件夹中删除给定属性的删除操作。  <br/> |
|[AppendToItemField](appendtoitemfield.md) <br/> |标识要追加到 [UpdateItem](updateitem-operation.md)操作期间项的单个属性的数据。  <br/> |
|[AppendToFolderField](appendtofolderfield.md) <br/> |指定要在[UpdateFolder Operation](updatefolder-operation.md)期间追加到文件夹属性数据。  <br/> |
|[Exists](exists.md) <br/> |表示一个搜索 **表达式，如果** 提供的属性存在于项目上，则返回 true。  <br/> |
|[FieldURIOrConstant](fielduriorconstant.md) <br/> |表示与另一个属性比较时所使用的属性或常量值。  <br/> |
|[IsEqualTo](isequalto.md) <br/> |表示一个搜索表达式，该表达式将属性与常量值或其他属性进行比较，如果相等，则计算结果为 true。  <br/> |
|[IsGreaterThan](isgreaterthan.md) <br/> |表示一个搜索表达式，该表达式将属性与常量值或另一个属性进行比较，如果第一个属性更大，则返回 true。  <br/> |
|[IsGreaterThanOrEqualTo](isgreaterthanorequalto.md) <br/> |表示一个搜索表达式，该表达式将属性与常量值或其他属性进行比较，如果第一个属性大于或等于第二个属性，则返回 true。  <br/> |
|[IsLessThan](islessthan.md) <br/> |表示一个搜索表达式，该表达式将属性与常量值或其他属性进行比较，如果第一个属性小于第二个，则返回 true。  <br/> |
|[IsLessThanOrEqualTo](islessthanorequalto.md) <br/> |表示一个搜索表达式，该表达式将属性与常量值或其他属性进行比较，如果第一个属性小于第二个，则返回 true。  <br/> |
|[IsNotEqualTo](isnotequalto.md) <br/> |表示一个搜索表达式，该表达式将属性与常量值或其他属性进行比较，如果值不同，则返回 true。  <br/> |
|[不包括](excludes.md) <br/> |执行这些属性的位掩码。  <br/> |
|[Contains](contains.md) <br/> |表示一个搜索表达式，该表达式确定给定属性是否包含提供的常量字符串值。  <br/> |
|[FieldOrder](fieldorder.md) <br/> |表示用于对结果进行排序并指示排序方向的单个字段。  <br/> |
   
## <a name="remarks"></a>注解

某些属性不能与其他属性一同使用。 任何带有无效扩展属性组合的请求都将生成一条错误消息。
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
> [!NOTE]
> 在 Microsoft .NET 中，Long 是一个 64 位有符号整数，而在 MAPI 和 COM 中，Long 是 32 位整数。 大多数开发人员将使用 Microsoft.NET Framework Exchange Web 服务客户端应用程序。 因此，使用 .NET 命名，而不是 MAPI 命名。
> 
> 例如，MAPI PR_MESSAGE_FLAGS类型0x0E07 PT \_ LONG 类型。 在 .NET 中，这被视为整数。 属性的扩展属性PR_MESSAGE_FLAGS定义为 `<t:ExtendedFieldURI PropertyTag="0x0E07" PropertyType="Integer"/>` 。 
  
## <a name="example"></a>示例

请求的以下示例创建一个具有两个自定义属性的项。 第一个自定义属性名为 **IsMyHouse，** 其布尔值设置为 **true**。 第二个自定义扩展属性名为 **HousePrices**。 它包含 Currency 值的数组。 
  
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

