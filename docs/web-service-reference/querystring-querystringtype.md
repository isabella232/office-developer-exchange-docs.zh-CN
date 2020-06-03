---
title: QueryString （QueryStringType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
api_name:
- QueryString
api_type:
- schema
ms.assetid: cadbf9a5-b87e-4d7f-b488-b76fb0ee7150
description: QueryString 元素包含基于高级查询语法（AQS）的邮箱查询字符串。
localization_priority: Priority
ms.openlocfilehash: eafbbab6de8d191197fb4b80e2b8e3cea80ab800
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459186"
---
# <a name="querystring-querystringtype"></a>QueryString （QueryStringType）

**QueryString**元素包含基于高级查询语法（AQS）的邮箱查询字符串。 
  
```XML
<QueryString/>
```

 **QueryStringType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

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
|[FindItem](finditem.md) <br/> |定义在邮箱中查找项目的请求。  <br/> 以下是此元素的 XPath 表达式：/FindItem。  <br/> |
   
## <a name="text-value"></a>文本值

**QueryString**元素 text 值代表使用[高级查询语法（AQS）](https://msdn.microsoft.com/library/aa965711%28VS.85%29.aspx)的子集进行的邮箱查询。 有关查询字符串支持的语法选项的信息，请参阅 "备注" 部分。
  
## <a name="remarks"></a>备注

在 Exchange Server 2010 中，此元素是 XML 架构字符串类型。 在从 Exchange Server 2013 开始的 Exchange 版本（包括 Exchange Online）中，此元素的类型为**QueryStringType**。 此更改不会中断任何现有客户端，因为它会添加三个新的可选属性。 
  
**QueryString**元素不包括使用 EWS 限制。 EWS 中的 AQS 支持三种类型的限制：单词阶段限制、日期范围限制和邮件类型限制。 下表列出了每种限制类型支持的搜索属性。 
  
**Word 阶段限制**

|**Property**|**示例**|**Function**|
|:-----|:-----|:-----|
|发件人  <br/> |发件人： Dean  <br/> 发件人： "Dean Halstead"  <br/> |搜索从 Dean 发送的项目。  <br/> 从 Dean Halstead 发送的搜索项目。 发件人必须正好是 "Dean Halstead"。  <br/> |
|更改为  <br/> |To： Dean  <br/> |搜索发送到 Dean 的项目。  <br/> |
|cc  <br/> |抄送： Dean  <br/> |在 "抄送" 行中搜索带有 Dean 的项目。  <br/> |
|bcc  <br/> |密件抄送： Dean  <br/> |搜索 "密件抄送" 行中带有 Dean 的项目。  <br/> |
|Participants  <br/> |参与者： Dean  <br/> |在 "收件人"、"抄送" 或 "密件抄送" 字段中搜索带有 Dean 的项目。  <br/> |
|Subject  <br/> |Subject： product  <br/> 主题：（产品开发）  <br/> 主题： "产品开发"  <br/> |在主题中搜索带有产品的项目。  <br/> 在主题中搜索带有产品和开发的项目。  <br/> |
|正文  <br/> 内容  <br/> |正文：进度  <br/> 内容：进度  <br/> |在正文中搜索具有进度的项目。  <br/> |
|Attachment  <br/> |附件：报表  <br/> |在附件文件名或文件正文中搜索带有报告的项目。  <br/> |
|（未指定属性）  <br/> |产品开发  <br/> |在所有 word 阶段属性中搜索包含产品和开发的项目。  <br/> |
   
Word 阶段限制匹配始终不区分大小写。 Word 阶段限制支持两种匹配类型：前缀匹配或完全匹配。 前缀 match 是默认的匹配行为。 如果需要完全匹配，请使用双引号。 例如，subject： "product" 与主题中的 "product" 匹配，而不是 "生产"。 双引号中的多个单词将同时限制 word 阶段及其顺序。 例如 "win product" 仅与 "win product" 匹配，而不是 "win95 产品" 或 "获奖的产品"。 您可以使用星号（ \* ）来定义带限制顺序的前缀匹配项。 例如，"win product" \* 与 "win95 产品"、"windows 生产订单行" 而不是 "windows 新产品" 或 "胜产品" 相匹配。 您可以搜索从或发送到域的所有邮件。 例如，从： "@hotmail" 返回从 hotmail.com 发送的所有邮件。
  
下表介绍了日期范围限制。
  
**日期范围限制**

|**Property**|**示例**|**Function**|
|:-----|:-----|:-----|
|发件箱  <br/> |已发送：上周  <br/> 已发送： 01/01/2001  <br/> 发送： 01/01/2001. 01/15/2001  <br/> |搜索上一周发送的项目。  <br/> 搜索在1月1日（2001）发送的项目。  <br/> 搜索在1月1日、2001和1月 2001 15 日之间发送的项目。  <br/> |
|接收时间  <br/> |已接收：今天  <br/> 已接收： 01/01/2001  <br/> |搜索今天收到的项目。  <br/> 搜索在1月1日（2001）收到的项目。  <br/> |
   
这两个点（...）是一个区域运算符。 它可用于定义具有开始日期和结束日期的范围。 若要指定日期，可以使用相对日期。 支持以下相对日期：
  
- 相对日期：今天、明天、昨天
    
- Multiword 相对日期：本周、下个月、上一周、上月或明年
    
- 天：星期日、星期一、星期二、星期三、星期四、星期五、星期六
    
- 一月份、二月、三月份、四月、六月、六月、七月、八月、九月、十月、十一月、十二月
    
下表介绍了邮件类型限制。 
  
**邮件类型限制**

|**Property**|**示例**|**Function**|
|:-----|:-----|:-----|
|Kind  <br/> |种类：任务  <br/> |搜索所有任务项目。  <br/> |
   
EWS 中的 AQS 使用**Kind**属性指定邮件类型。 Kind 属性可以与以下项目类型一起使用： 
  
- email
    
- 会议
    
- tasks
    
- 注释
    
- 文档
    
- 日志
    
- contacts
    
- 即时消息
    
下表介绍了分组逻辑连接器。
  
**分组逻辑连接器**

|**Connector**|**示例**|**Function**|
|:-----|:-----|:-----|
|AND  <br/> |主题：产品和主题：开发  <br/> 主题：（产品和开发）  <br/> 主题：（产品开发）  <br/> |在主题的产品和开发中搜索项目。  <br/> |
|OR  <br/> |正文：项目或正文：建议  <br/> 正文：（项目或建议）  <br/> |使用正文中的产品或开发搜索项目。  <br/> |
|NOT  <br/> |非正文：建议  <br/> 正文：（不建议）  <br/> |搜索正文中没有建议的邮件。  <br/> |
   
始终是默认的连接器。 例如，subject： project 和 body：提案与 subject： project body：提案。 逻辑连接器区分大小写。 例如，body：（项目或建议）在正文中搜索带有 "项目"、"或" 和 "建议" 的邮件，而不是 "项目" 或 "建议"。 加号符号（+）等效于和。 连字符符号（-）等效于 NOT。 例如，body：（项目建议）在正文中搜索 "project" 但不包含 "提案" 的邮件。 
  
查询字符串还可以包含用于搜索的非索引属性。 如果查询字符串中包含非索引属性，则搜索可能会对索引属性执行 Exchange 搜索，并对非索引属性执行存储搜索。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="example"></a>示例

下面的示例演示使用主题中的自动发现在收件箱中搜索邮件的请求。
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
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

下面的示例演示对请求的成功响应。
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="20" 
                         Version="Exchange2010" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[FindItem 操作](finditem-operation.md)
  
[FindConversation 操作](findconversation-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

