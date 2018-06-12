---
title: PlayOnPhoneResponse （Exchange Web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PlayOnPhoneResponse
api_type:
- schema
ms.assetid: 578b70d1-dc9d-4bce-b859-0109b2d2bcec
description: PlayOnPhoneResponse 元素指定在电话上播放语音邮件的请求的响应。
ms.openlocfilehash: 203309bdd6d17b1c78054e673f8a340c2f069b38
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826831"
---
# <a name="playonphoneresponse-exchange-web-services"></a>PlayOnPhoneResponse （Exchange Web 服务）

**PlayOnPhoneResponse**元素指定在电话上播放语音邮件的请求的响应。 
  
```xml
<PlayOnPhoneResponse ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <PhoneCallId/>
</PlayOnPhoneResponse>
```

 **PlayOnPhoneResponseMessageType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|**ResponseClass** <br/> | 介绍响应的状态。 <br/><br/>下面是此属性有效值：  <br/><br/>-成功  <br/>-警告  <br/>-错误  <br/> |
   
#### <a name="responseclass-attribute-values"></a>ResponseClass 属性值

|**值**|**说明**|
|:-----|:-----|
|**成功** <br/> |介绍的已完成的请求。  <br/> |
|**Warning** <br/> | 介绍了未处理的请求。 如果请求中的项目处理和无法处理后续项时出错，则可能会返回一条警告。<br/><br/> 以下是源的警告的示例： <br/><br/>-在 Exchange 存储过程批次中处于脱机状态。  <br/>-Active Directory 域服务 (AD DS) 处于脱机状态。  <br/>的已移动邮箱。  <br/>(MDB)-邮件数据库处于脱机状态。  <br/>的已过期密码。  <br/>已超出-配额。  <br/> |
|**Error** <br/> | 描述无法满足请求。 <br/><br/>错误的来源的示例如下：  <br/><br/>-无效属性或元素。  <br/>-属性或超出范围的元素  <br/>-未知的标记。  <br/>-属性或上下文中无效的元素。  <br/>的由任何客户端未经授权的访问尝试。  <br/>的中到有效的客户端的呼叫的响应服务器端出现故障。  <br/><br/>  可以在[ResponseCode](responsecode.md)和[MessageText](messagetext.md)元素主题中找到有关错误的信息。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |提供的响应状态的文本说明。  <br/> |
|[ResponseCode](responsecode.md) <br/> |提供标识的特定错误的请求时遇到的错误代码。  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |当前未使用，保留以供将来使用。 此元素包含一个值为 0。  <br/> |
|[MessageXml](messagexml.md) <br/> |提供了其他错误响应信息。  <br/> |
|[PhoneCallId](phonecallid.md) <br/> |指定的电话呼叫标识符。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>备注

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

