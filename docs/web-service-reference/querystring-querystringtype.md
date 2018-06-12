---
title: 查询字符串 (QueryStringType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- QueryString
api_type:
- schema
ms.assetid: cadbf9a5-b87e-4d7f-b488-b76fb0ee7150
description: QueryString 元素包含基于上高级查询语法 (AQS) 邮箱查询字符串。
ms.openlocfilehash: 410405638b3f8628dc589049873cfea1f153310c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826943"
---
# <a name="querystring-querystringtype"></a>查询字符串 (QueryStringType)

**QueryString**元素包含基于上高级查询语法 (AQS) 邮箱查询字符串。 
  
```XML
<QueryString/>
```

 **QueryStringType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|ResetCache  <br/> |指示应重置缓存。  <br/> |
|ReturnDeletedItems  <br/> |指示应返回已删除的项目。  <br/> |
|ReturnHighlightTerms  <br/> |指示应返回突出显示的术语。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |定义查找邮箱中的项目的请求。  <br/> 下面是此元素的 XPath 表达式： /FindItem。  <br/> |
   
## <a name="text-value"></a>文本值

**QueryString**元素文本值表示由使用[高级查询语法 (AQS)](http://msdn.microsoft.com/en-us/library/aa965711%28VS.85%29.aspx)的子集的邮箱查询。 请参阅备注部分的有关支持的语法查询字符串选项的信息。
  
## <a name="remarks"></a>备注

在 Exchange Server 2010 中，此元素是 XML 架构 string 类型。 在版本的 Exchange 开头 Exchange Server 2013，包括 Exchange Online，此元素的类型是**QueryStringType**。 此更改不会将任何现有的客户端，因为它将添加三个新的可选属性。 
  
**QueryString**元素不包括使用 EWS 限制。 Ews AQS 支持三种类型的限制： word 阶段限制、 日期范围限制和消息类型限制。 下表列出了每种限制类型的支持的搜索属性。 
  
**Word 阶段限制**

|**属性**|**示例**|**函数**|
|:-----|:-----|:-----|
|发件人  <br/> |从： Dean  <br/> 从:"Dean Halstead"  <br/> |搜索从 Dean 发送的项目。  <br/> 搜索从 Dean Halstead 发送项目。 发件人必须完全"Dean Halstead"。  <br/> |
|更改为  <br/> |到： Dean  <br/> |搜索发送给 Dean 项目。  <br/> |
|cc  <br/> |Cc:Dean  <br/> |搜索与 Dean Cc 行上的项目。  <br/> |
|bcc  <br/> |Bcc:Dean  <br/> |搜索与 Dean 密件抄送行上的项目。  <br/> |
|参与者  <br/> |参与者： Dean  <br/> |搜索 Dean 项目中的收件人、 抄送或密件抄送字段。  <br/> |
|主题  <br/> |主题： 产品  <br/> 主题:(product development)  <br/> 使用者:"产品开发"  <br/> |搜索项目的主题中的产品。  <br/> 搜索与产品开发主题中的项目。  <br/> |
|正文  <br/> 内容  <br/> |正文： 进度  <br/> 内容： 进度  <br/> |搜索项目的正文中的进度。  <br/> |
|附件  <br/> |附件： 报告  <br/> |搜索项目的附件文件的名称或文件正文中的报告。  <br/> |
|（未指定属性）  <br/> |产品开发  <br/> |搜索的项目包含产品和所有 word 阶段属性中的开发。  <br/> |
   
始终 Word 阶段限制匹配是区分大小写。 Word 阶段限制支持两种匹配类型： 前缀匹配或完全匹配。 前缀匹配是默认匹配行为。 如果您希望完全匹配，则使用双引号。 例如，使用者:"产品"匹配产品但不是生产主题中的。 用双引号括起来的多个词语限制 word 阶段和它们的顺序。 例如"产品 win"匹配仅 win 产品，不 win95 产品或产品的 win。 您可以使用星号 (\*) 定义与受限制的订单的前缀匹配。 例如，"win 产品"\*匹配 win95 产品、 windows 生产线但不是 windows 新产品或产品的 win。 您可以搜索来自或发送到域的所有邮件。 例如，from:"@hotmail.com"返回从 hotmail.com 发送的所有邮件。
  
下表介绍日期范围限制。
  
**日期范围限制**

|**属性**|**示例**|**函数**|
|:-----|:-----|:-----|
|发送时间  <br/> |发送： 上周  <br/> 发送： 2001-01-01  <br/> Sent:01/01/2001..01/15/2001  <br/> |搜索项目发送最后一个星期。  <br/> 搜索 2001 年 1 月 1st，发送项目。  <br/> 搜索 2001 年 1 月 1 日和 2001 年 1 月 15 日之间发送的项目。  <br/> |
|接收时间  <br/> |接收： 立即  <br/> 接收： 2001-01-01  <br/> |搜索收到今天的项目。  <br/> 搜索 2001 年 1 月 1st，收到的项目。  <br/> |
   
两个点 （.） 是一个范围运算符。 它可以用于定义开始和结束日期范围。 若要指定的日期，您可以使用相对日期。 支持以下相对日期：
  
- 相对日期： 今天、 明天、 昨天
    
- 多词相对日期： 本周下个月，过去的月或明年上周
    
- 天数： 星期日和星期一、 星期二、 星期三、 星期四和星期五和星期六
    
- 年 1 月、 年 2 月、 March、 April、 May，年 6 月、 年 7 月、 年 8 月、 年 9 月、 年 10 月、 年 11 月、 年 12 月
    
下表描述了消息类型限制。 
  
**消息类型限制**

|**属性**|**示例**|**函数**|
|:-----|:-----|:-----|
|类型  <br/> |类型： 任务  <br/> |搜索所有任务项目。  <br/> |
   
AQS EWS 中的使用的**类型**属性来指定消息类型。 Kind 属性可用于以下类型的项： 
  
- email
    
- 会议
    
- tasks
    
- notes
    
- 文档
    
- 日志
    
- contacts
    
- im
    
下表介绍分组逻辑连接器。
  
**分组逻辑连接器**

|**连接器**|**示例**|**函数**|
|:-----|:-----|:-----|
|AND  <br/> |主题： 产品和主题： 开发  <br/> 主题:(product AND development)  <br/> 主题:(product development)  <br/> |搜索主题中的产品和开发项目。  <br/> |
|OR  <br/> |正文： 项目或项目正文的建议：  <br/> 正文:(project OR proposal)  <br/> |搜索项目产品或在正文中的开发。  <br/> |
|NOT  <br/> |不建议正文：  <br/> 正文:(NOT proposal)  <br/> |搜索不建议在正文中的邮件。  <br/> |
   
并且始终是默认连接器。 例如，主题： project AND body： 建议是主题： 项目正文： 建议相同。 逻辑连接器是区分大小写。 例如，正文:(project Or proposal) 搜索邮件的项目，或，和而不是项目或建议在正文中的建议。 加号 （+） 等同于成和。 连字符符号 （-） 相当于不。 例如，正文:(project-proposal) 正文中搜索项目但不包含建议的消息。 
  
查询字符串还可以包含用于搜索的非索引属性。 如果查询字符串中包含非索引属性，搜索可能执行 Exchange 搜索索引的属性和存储搜索索引的属性。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="example"></a>示例

下面的示例演示请求来搜索使用自动发现收件箱中主题中的邮件。
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="1" Offset="0" BasePoint="Beginning" />
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox" />
      </m:ParentFolderIds>
      <m:QueryString>subject:Autodiscover</m:QueryString>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

下面的示例演示请求的成功响应。
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="20" 
                         Version="Exchange2010" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="1" 
                        TotalItemsInView="5" 
                        IncludesLastItemInRange="false">
            <t:Items>
              <t:Message>
                <t:ItemId Id="AAMkADEzOTExYjJkLTYx" ChangeKey="CQAAABY" />
                <t:Subject>How to use Autodiscover</t:Subject>
              </t:Message>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>

```

## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[FindItem 操作](finditem-operation.md)
  
[FindConversation Operation](findconversation-operation.md)


- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

