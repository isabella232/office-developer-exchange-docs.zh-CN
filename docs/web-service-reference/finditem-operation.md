---
title: FindItem Operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindItem
api_type:
- schema
ms.assetid: ebad6aae-16e7-44de-ae63-a95b24539729
description: 查找信息 FindItem EWS 操作。
ms.openlocfilehash: b033ac2930981819a20f1336d40058a5f7c03b89
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754347"
---
# <a name="finditem-operation"></a>FindItem Operation

查找有关**FindItem** EWS 操作的信息。 
  
**FindItem**操作搜索位于用户的邮箱中的项目。 此操作提供了许多方式来筛选和搜索结果如何返回到呼叫者的格式。 
  
## <a name="using-the-finditem-operation"></a>使用 FindItem 操作

**FindItem**操作请求提供了许多方法，用于搜索的邮箱和如何响应中返回的数据的格式。 您可以指定以下**FindItem**请求中： 
  
- 搜索是否浅表或软删除遍历。 指定这是必需的。 请注意，再加上搜索限制软删除遍历将导致返回零项，即使有匹配的项目的搜索条件。
    
- 项目响应形状。 这标识响应中返回的属性。 指定这是必需的。
    
- 要从中执行搜索文件夹。 指定这是必需的。
    
- 用于返回分页机制和视图类型页中查看数据。 指定这是可选的。
    
- 分组和对返回的项排序选项。 指定这是可选的。
    
- 搜索限制或高级查询语法 (AQS) 字符串用于筛选返回的项目。 有关使用 AQS 内容索引的搜索的详细信息，请参阅[QueryString （字符串）](querystring-string.md)。 指定这是可选的。
    
- 响应中返回的项的排序顺序。 指定这是可选的。
    
**FindItem**操作返回仅第一个 512 个字节的任何流式属性。 对于 Unicode，它使用以 null 结尾的 Unicode 字符串中返回的前 255 个字符。 它并不返回任何邮件正文格式或收件人列表。 **FindItem**将返回收件人摘要。 可以使用[GetItem 操作](getitem-operation.md)获取项目的详细信息。 
  
 **FindItem**返回仅[Name (EmailAddressType)](name-emailaddresstype.md)元素，并不会返回以下字段的[邮箱](mailbox.md)元素中的[电子邮件地址 (NonEmptyStringType)](emailaddress-nonemptystringtype.md)元素： 
  
- 邮件[从](from.md)字段 
    
- 邮件[发件人](sender.md)字段 
    
- 日历项目的[组织者](organizer.md)字段 
    
> [!NOTE]
> **FindItem**操作可以[CalendarView](calendarview.md)元素中返回结果。 **CalendarView**元素可返回单个日历项和定期会议的所有匹配项。 如果未使用的**CalendarView**元素，则返回单个日历项和定期母版日历项。 如果未使用的**CalendarView**元素，必须从定期主扩展发生次数。 
  
**FindItem**操作可以使用下表中列出的 SOAP 标头。 
  
**表 1。FindItem 操作 SOAP 标头**

|**Header**|**元素**|**说明**|
|:-----|:-----|:-----|
|**DateTimePrecision** <br/> |[DateTimePrecision](datetimeprecision.md) <br/> |指定在从服务器中，以秒为单位，或以毫秒为单位的响应中的数据/时间值的分辨率。 这是适用于请求。  <br/> |
|**模拟** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |标识模拟客户端应用程序的用户。 这是适用于请求。  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |标识用于访问邮箱的 RFC3066 区域性。 这是适用于请求。  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |标识操作请求的架构版本。 这是适用于请求。  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |标识响应该请求的服务器的版本。 这是适用于响应。  <br/> |
|**TimeZoneContext** <br/> |[TimeZoneContext](timezonecontext.md) <br/> |确定要用于来自服务器的所有响应的时区。 这是适用于请求。  <br/> |
   
## <a name="finditem-operation-request-example"></a>FindItem 操作请求示例

**FindItem**请求的下面的示例演示如何获取由位于已删除邮件文件夹的项目的[BaseShape](baseshape.md)元素**IdOnly**枚举定义的项标识符。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
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
    
对于**FindItem**请求消息的更多选项，浏览的架构层次结构。 启动[FindItem](finditem.md)元素。 
  
## <a name="successful-finditem-operation-response"></a>成功 FindItem 操作响应

下面的示例演示对**FindItem**请求成功响应。 
  
[消息](message-ex15websvcsotherref.md)元素表示电子邮件和非通过 EWS 架构强类型的所有其他项目。 如 IPM 的项目。共享和[消息](message-ex15websvcsotherref.md)元素以返回 IPM.InfoPath。 Exchange 不在响应中返回基本的[Item](item.md)元素。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

在响应中使用以下元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [FindItemResponse](finditemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [FindItemResponseMessage](finditemresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [RootFolder (FindItemResponseMessage)](rootfolder-finditemresponsemessage.md)
    
- [Items](items.md)
    
- [Message](message-ex15websvcsotherref.md)
    
- [ItemId](itemid.md)
    
**FindItem**响应消息的更多选项，浏览的架构层次结构。 启动[FindItemResponse](finditemresponse.md)元素。 
  
## <a name="finditem-operation-error-response"></a>FindItem 操作错误响应

下面的示例演示对**FindItem**请求错误响应。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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
    
**FindItem**错误响应消息的更多选项，浏览的架构层次结构。 启动[FindItemResponse](finditemresponse.md)元素。 
  
## <a name="version-differences"></a>版本差异

主要版本 15 开头和结尾的 Exchange 版本生成 15.0.898.11 返回**FindItem**操作用于存档邮箱中搜索多个文件夹时，此 ErrorInvalidOperation 值[ResponseCode](responsecode.md)元素中。 
  
## <a name="see-also"></a>另请参阅

- [查找项目](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)
    
- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)
    
- **FindItemType**
    

