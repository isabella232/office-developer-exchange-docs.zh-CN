---
title: FindItem 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
api_name:
- FindItem
api_type:
- schema
ms.assetid: ebad6aae-16e7-44de-ae63-a95b24539729
description: 查找有关 FindItem EWS 操作的信息。
localization_priority: Priority
ms.openlocfilehash: 499d1ee80ef323c883fa86eb125d8c037fb37d4e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462554"
---
# <a name="finditem-operation"></a>FindItem 操作

查找有关**FindItem** EWS 操作的信息。 
  
**FindItem**操作将搜索位于用户邮箱中的项目。 此操作提供了多种方法来筛选和设置搜索结果返回给呼叫者的方式。 
  
## <a name="using-the-finditem-operation"></a>使用 FindItem 操作

**FindItem**操作请求提供了多种方法来搜索邮箱并设置数据在响应中的返回方式。 您可以在**FindItem**请求中指定以下内容： 
  
- 搜索是浅表遍历还是软删除遍历。 指定此属性是必需的。 请注意，与搜索限制组合在一起的软删除的遍历将导致返回零个项目，即使存在与搜索条件匹配的项目也是如此。
    
- 项目的响应形状。 这标识响应中返回的属性。 指定此属性是必需的。
    
- 要从中执行搜索的文件夹。 指定此属性是必需的。
    
- 页面中返回视图数据的分页机制和视图类型。 指定此参数是可选的。
    
- 用于对返回的项进行分组和排序的选项。 指定此参数是可选的。
    
- 用于筛选返回的项目的搜索限制或高级查询语法（AQS）字符串。 有关使用 AQS 进行内容索引搜索的详细信息，请参阅[QueryString （String）](querystring-string.md)。 指定此参数是可选的。
    
- 响应中返回的项目的排序顺序。 指定此参数是可选的。
    
**FindItem**操作仅返回任何 streamable 属性的前512个字节。 对于 Unicode，它通过使用以 null 结尾的 Unicode 字符串返回前255个字符。 它不会返回任何邮件正文格式或收件人列表。 **FindItem**将返回收件人摘要。 您可以使用[GetItem 操作](getitem-operation.md)来获取项目的详细信息。 
  
 **FindItem**仅返回[Name （EmailAddressType）](name-emailaddresstype.md)元素，并且不会返回以下字段的[邮箱](mailbox.md)元素中的[EmailAddress （NonEmptyStringType）](emailaddress-nonemptystringtype.md)元素： 
  
- 邮件的 "[发件人](from.md)" 字段 
    
- 邮件的 "[发件人](sender.md)" 字段 
    
- 日历项目的 "[组织者](organizer.md)" 字段 
    
> [!NOTE]
> **FindItem**操作可以返回[CalendarView](calendarview.md)元素中的结果。 **CalendarView**元素返回单个日历项目和定期会议的所有事件。 如果未使用**CalendarView**元素，则将返回单个日历项目和定期主日历项目。 如果未使用**CalendarView**元素，则必须从定期母版展开此事件。 
  
**FindItem**操作可以使用下表中列出的 SOAP 标头。 
  
**表1。FindItem 操作 SOAP 标头**

|**Header**|**元素**|**说明**|
|:-----|:-----|:-----|
|**DateTimePrecision** <br/> |[DateTimePrecision](datetimeprecision.md) <br/> |指定对来自服务器的响应中的数据/时间值的解析（以秒或毫秒为单位）。 这适用于请求。  <br/> |
|**模拟** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |标识客户端应用程序模拟的用户。 这适用于请求。  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |标识要用于访问邮箱的 RFC3066 区域性。 这适用于请求。  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |标识操作请求的架构版本。 这适用于请求。  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |标识响应请求的服务器版本。 这适用于响应。  <br/> |
|**TimeZoneContext** <br/> |[TimeZoneContext](timezonecontext.md) <br/> |标识要用于来自服务器的所有响应的时区。 这适用于请求。  <br/> |
   
## <a name="finditem-operation-request-example"></a>FindItem 操作请求示例

下面的**FindItem**请求示例演示如何获取由[BaseShape](baseshape.md)元素的**IdOnly**枚举定义的项标识符，这些项是在 "已删除的项目" 文件夹中找到的项。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
              Traversal="Shallow">
      <ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
      </ItemShape>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="deleteditems"/>
      </ParentFolderIds>
    </FindItem>
  </soap:Body>
</soap:Envelope>
```

请求中使用以下元素： 
  
- [FindItem](finditem.md)
    
- [ItemShape](itemshape.md)
    
- [BaseShape](baseshape.md)
    
- [ParentFolderIds](parentfolderids.md)
    
- [DistinguishedFolderId](distinguishedfolderid.md)
    
有关**FindItem**请求消息的更多选项，请浏览架构层次结构。 从[FindItem](finditem.md)元素开始。 
  
## <a name="successful-finditem-operation-response"></a>成功的 FindItem 操作响应

下面的示例演示对**FindItem**请求的成功响应。 
  
[Message](message-ex15websvcsotherref.md)元素表示由 EWS 架构不强类型化的电子邮件和其他所有项目。 项目，如 IPM。共享和 IPM. InfoPath 以[邮件](message-ex15websvcsotherref.md)元素的形式返回。 Exchange 不会在响应中返回基本[项目](item.md)元素。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder TotalItemsInView="10" IncludesLastItemInRange="true">
            <t:Items>
              <t:Message>
                <t:ItemId Id="AS4AUn=" ChangeKey="fsVU4==" />
              </t:Message>
              <t:Message>
                <t:ItemId Id="AS4AUM=" ChangeKey="fsVUA==" />
              </t:Message>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </FindItemResponse>
  </soap:Body>
</soap:Envelope>
```

响应中使用以下元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [FindItemResponse](finditemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [FindItemResponseMessage](finditemresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [RootFolder （FindItemResponseMessage）](rootfolder-finditemresponsemessage.md)
    
- [Items](items.md)
    
- [消息](message-ex15websvcsotherref.md)
    
- [ItemId](itemid.md)
    
有关**FindItem**响应消息的更多选项，请浏览架构层次结构。 从[FindItemResponse](finditemresponse.md)元素开始。 
  
## <a name="finditem-operation-error-response"></a>FindItem 操作错误响应

下面的示例演示对**FindItem**请求的错误响应。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Error">
          <m:MessageText>Id is malformed.</m:MessageText>
          <m:ResponseCode>ErrorInvalidIdMalformed</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </FindItemResponse>
  </soap:Body>
</soap:Envelope>
```

错误响应中使用以下元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [FindItemResponse](finditemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [FindItemResponseMessage](finditemresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
有关**FindItem**错误响应消息的更多选项，请浏览架构层次结构。 从[FindItemResponse](finditemresponse.md)元素开始。 
  
## <a name="version-differences"></a>版本差异

如果使用**FindItem**操作在存档邮箱中搜索多个文件夹，则在[ResponseCode](responsecode.md)元素中，从主要版本15开始并以 "生成 15.0.898.11" 结尾的 Exchange 版本将返回 ErrorInvalidOperation 值。 
  
## <a name="see-also"></a>另请参阅

- [查找项目](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)
    
- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)
    
- **FindItemType**
    

