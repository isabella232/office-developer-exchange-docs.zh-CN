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
description: ExtendedFieldURI 元素标识扩展的 MAPI 属性。
ms.openlocfilehash: 8d946aec8ae2c5e6bb4ca3f1d8ee74250262d373
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754229"
---
# <a name="extendedfielduri"></a>ExtendedFieldURI

**ExtendedFieldURI**元素标识扩展的 MAPI 属性。 
  
```xml
<ExtendedFieldURI DistinguishedPropertySetId="" PropertySetId="" PropertyTag="" PropertyName="" PropertyId="" PropertyType="" />
```

 **PathToExtendedFieldType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|**DistinguishedPropertySetId** <br/> |定义的已知属性设置为扩展的 MAPI 属性的 Id。  <br/> 如果使用此属性，则不能使用**PropertySetId**和**PropertyTag**属性。 **PropertyId**或**PropertyName**属性，并具有**PropertyType**属性，必须使用此属性。  <br/> 本主题后面**DistinguishedPropertySetId**属性表列出了此属性的可能值。  <br/> 此属性是可选的。  <br/> |
|**PropertySetId** <br/> |标识通过其标识 GUID 扩展属性集或命名空间的 MAPI。  <br/> 如果使用此属性，则不能使用**DistinguishedPropertySetId**和**PropertyTag**属性。 **PropertyId**或**PropertyName**属性，并具有**PropertyType**属性，必须使用此属性。  <br/> 此属性是可选的。  <br/> |
|**PropertyTag** <br/> |标识不带标记的类型部分的属性标记。 可以为十六进制数或一个简短的整数表示**PropertyTag** 。  <br/> 1 到 999 之间 0x8000 和 0xFFFE 表示自定义范围的属性。 当邮箱数据库首次遇到的自定义属性时，它会将该自定义属性分配 0x8000 0xFFFE 自定义属性范围内的属性标记。 给定的自定义属性标记将很可能数据库而异。 因此，按属性标记的自定义属性请求可能返回不同的属性在不同的数据库。 自定义属性禁止**PropertyTag**属性的使用。 而是使用**PropertySetId**属性和**PropertyName**或**PropertyId**属性。  <br/> > [!IMPORTANT]> 访问 0x8000 和 0xFFFE 之间的任何自定义属性，通过使用 GUID + 名称/id。           如果使用**PropertyTag**属性，则不能使用**DistinguishedPropertySetId**、 **PropertySetId**、 **PropertyName**、 和**PropertyId**属性。  <br/> 此属性是可选的。  <br/> > [!NOTE]> 不能在自定义范围内 0x8000 0xFFFE 属性使用属性标记属性。 您必须在这种情况下使用的命名的属性。           |
|**PropertyName** <br/> |按其名称中标识的扩展的属性。 此属性必须在使用**DistinguishedPropertySetId**或**PropertySetId**加以。  <br/> 如果使用此属性，则不能使用**PropertyId**和**PropertyTag**属性。  <br/> 此属性是可选的。  <br/> |
|**PropertyId** <br/> |用于标识其调度 id 扩展的属性 十进制或十六进制格式可以标识调度 ID。 此属性必须在使用**DistinguishedPropertySetId**或**PropertySetId**加以。  <br/> 如果使用此属性，则不能使用**PropertyName**和**PropertyTag**属性。  <br/> 此属性是可选的。  <br/> |
|**PropertyType** <br/> |表示一个属性标记的属性类型。 这对应于属性标记中的最低有效字。  <br/> 本主题后面的 PropertyType 属性表包含此属性的可能值。  <br/> 此属性是必需的。  <br/> |
   
#### <a name="distinguishedpropertysetid-attribute"></a>DistinguishedPropertySetId 属性

|**值**|**说明**|
|:-----|:-----|
|会议  <br/> |标识会议属性按名称设置 ID。  <br/> |
|Appointment  <br/> |按名称标识约会属性集 ID。  <br/> |
|Common  <br/> |按名称标识常见属性集 ID。  <br/> |
|PublicStrings  <br/> |按名称标识公共字符串属性集 ID。  <br/> |
|Address  <br/> |按名称标识地址属性集 ID。  <br/> |
|InternetHeaders  <br/> |按名称标识 Internet 头属性集 ID。  <br/> |
|CalendarAssistant  <br/> |按名称标识日历助理属性集 ID。  <br/> |
|UnifiedMessaging  <br/> |按名称标识统一消息的属性集 ID。  <br/> |
   
#### <a name="propertytype-attribute"></a>PropertyType 属性

|**值**|**说明**|
|:-----|:-----|
|ApplicationTime  <br/> |一个 double 值，它将被解释为日期和时间。 整数部分是日期，小数部分是时间。  <br/> |
|ApplicationTimeArray  <br/> |解释为日期和时间的双精度值的数组。  <br/> |
|二进制  <br/> |Base64 编码的二进制值。  <br/> |
|BinaryArray  <br/> |Base64 编码的二进制值的数组。  <br/> |
|Boolean  <br/> |布尔值**true**或**false**。  <br/> |
|CLSID  <br/> |一个 GUID 的字符串。  <br/> |
|CLSIDArray  <br/> |一个 GUID 的字符串数组。  <br/> |
|货币  <br/> |64 位整数，它被解释为分的数量。  <br/> |
|CurrencyArray  <br/> |解释为分的数量的 64 位整数的数组。  <br/> |
|双精度数  <br/> |64 位浮点值。  <br/> |
|DoubleArray  <br/> |64 位浮点值的数组。  <br/> |
|Error  <br/> |SCODE 值;32 位无符号的整数。  <br/> 不使用限制或获取设置值。 这仅用于报告已存在。  <br/> |
|Float  <br/> |32 位的浮点值。  <br/> |
|FloatArray  <br/> |32 位浮点值的数组。  <br/> |
|整数  <br/> |带符号的 32 位 (Int32) 整数。  <br/> |
|IntegerArray  <br/> |有符号整数，32 位 (Int32) 数组。  <br/> |
|Long  <br/> |签名或无符号 64 位 (Int64) 之间的整数。  <br/> |
|LongArray  <br/> |签名或无符号的 64 位 (Int64) 整数的数组。  <br/> |
|Null  <br/> |指示没有属性值。  <br/> 不使用限制或获取设置值。 这仅用于报告已存在。  <br/> |
|对象  <br/> |指向实现 IUnknown 接口的对象的指针。  <br/> 不使用限制或获取设置值。 这仅用于报告已存在。  <br/> |
|ObjectArray  <br/> |指向实现 IUnknown 接口的对象数组。  <br/> 不使用限制或获取设置值。 这仅用于报告已存在。  <br/> |
|短  <br/> |带符号的 16 位整数。  <br/> |
|ShortArray  <br/> |签名 16 位整数的数组。  <br/> |
|SystemTime  <br/> |一个 FILETIME 结构的窗体中的 64 位整数日期和时间值。  <br/> |
|SystemTimeArray  <br/> |一个 FILETIME 结构的窗体中的 64 位整数日期和时间值的数组。  <br/> |
|String  <br/> |Unicode 字符串。  <br/> |
|StringArray  <br/> |Unicode 字符串数组。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ExtendedProperty](extendedproperty.md) <br/> |标识文件夹和项扩展的属性。  <br/> |
|[AdditionalProperties](additionalproperties.md) <br/> | 标识其他属性。  <br/>  下面是此元素的 XPath 表达式：  <br/>  `/FindFolder/FolderShape/AdditionalProperties` <br/>  `/GetFolder/FolderShape/AdditionalProperties` <br/>  `/SyncFolderHierarchy/FolderShape/AdditionalProperties` <br/>  `/GetItem/ItemShape/AdditionalProperties` <br/>  `/FindItem/ItemShape/AdditionalProperties` <br/>  `/SyncFolderItems/ItemShape/AdditionalProperties` <br/>  `/GetAttachment/AttachmentShape/AdditionalProperties` <br/> |
|[SetItemField](setitemfield.md) <br/> |表示更新到单个[UpdateItem 操作](updateitem-operation.md)中的项目的属性。  <br/> |
|[SetFolderField](setfolderfield.md) <br/> |表示对[UpdateFolder Operation](updatefolder-operation.md)中的文件夹上的单个属性的更新。  <br/> |
|[DeleteItemField](deleteitemfield.md) <br/> |代表[UpdateItem 操作](updateitem-operation.md)期间，从项目中删除给定的属性删除操作。  <br/> |
|[DeleteFolderField](deletefolderfield.md) <br/> |代表用于从文件夹 UpdateFolder 呼叫过程中删除给定的属性删除操作。  <br/> |
|[AppendToItemField](appendtoitemfield.md) <br/> |标识要追加到的项目的单个属性[UpdateItem 操作](updateitem-operation.md)期间数据。  <br/> |
|[AppendToFolderField](appendtofolderfield.md) <br/> |指定要在[UpdateFolder Operation](updatefolder-operation.md)期间追加到文件夹属性数据。  <br/> |
|[Exists](exists.md) <br/> |代表返回**true**如果所提供的属性存在项目的搜索表达式。  <br/> |
|[FieldURIOrConstant](fielduriorconstant.md) <br/> |代表属性或以常量值，用于比较与另一个属性。  <br/> |
|[IsEqualTo](isequalto.md) <br/> |代表一个搜索表达式的比较一个常数值的属性或另一个属性，并计算结果为**true** ，如果二者相等。  <br/> |
|[IsGreaterThan](isgreaterthan.md) <br/> |代表一个搜索表达式，如果第一个属性大于比较常量值或另一个属性，返回**true**的属性。  <br/> |
|[IsGreaterThanOrEqualTo](isgreaterthanorequalto.md) <br/> |代表一个搜索表达式，如果第一个属性是大于或等于第二个比较常量值或另一个属性，返回**true**的属性。  <br/> |
|[IsLessThan](islessthan.md) <br/> |表示搜索表达式的比较一个常数值的属性或另一个属性，并返回**true** ，如果第一个属性小于第二个。  <br/> |
|[IsLessThanOrEqualTo](islessthanorequalto.md) <br/> |表示搜索表达式的比较一个常数值的属性或另一个属性，并返回**true** ，如果第一个属性小于第二个。  <br/> |
|[IsNotEqualTo](isnotequalto.md) <br/> |表示搜索表达式的比较常量值或另一个属性，返回**true**的属性，如果值不相同。  <br/> |
|[不包括](excludes.md) <br/> |执行这些属性的位掩码。  <br/> |
|[Contains](contains.md) <br/> |代表一个搜索表达式，确定给定的属性是否包含提供常量的字符串值。  <br/> |
|[FieldOrder](fieldorder.md) <br/> |代表用于对结果进行排序的单个字段，并指示排序的方向。  <br/> |
   
## <a name="remarks"></a>备注

与其他属性结合使用，不能使用某些属性。 使用了无效的扩展的属性属性组合中的任何请求将生成一条错误消息。
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
> [!NOTE]
> 在 Microsoft.NET long 类型的值是 64 位有符号的整数，而在 MAPI 和 COM、 long 类型的值是 32 位整数。 大多数开发人员将使用 Microsoft.NET Framework 开发 Exchange Web 服务客户端应用程序。 因此，.NET 命名使用而不是 MAPI 命名。 例如，PR_MESSAGE_FLAGS MAPI 属性 0x0E07，为 PT_LONG 类型。 在.NET 中，则被视为一个整数。 PR_MESSAGE_FLAGS 扩展的属性定义为\<t:ExtendedFieldURI PropertyTag ="0x0E07"PropertyType ="整数"/\>。 
  
## <a name="example"></a>示例

请求的下面的示例创建具有两个自定义属性的项。 第一个自定义属性设置为**true**的布尔值名为**IsMyHouse** 。 第二个自定义扩展的属性名为**HousePrices**。 它包含的货币值的数组。 
  
```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" 
                  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
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
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[FieldURI](fielduri.md)
  
[IndexedFieldURI](indexedfielduri.md)


- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

