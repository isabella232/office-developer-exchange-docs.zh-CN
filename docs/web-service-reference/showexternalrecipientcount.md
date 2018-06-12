---
title: ShowExternalRecipientCount
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ShowExternalRecipientCount
api_type:
- schema
ms.assetid: db28dbcb-d051-4e5c-a9c2-4b8d5149b4e1
description: ShowExternalRecipientCount 元素指示是否 GetMailTips 操作的使用者具有显示邮件提示指示邮件要发送到外部收件人的数量。
ms.openlocfilehash: 1fd3ceb629689c560dc60afe01f0413602f79a0d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827491"
---
# <a name="showexternalrecipientcount"></a>ShowExternalRecipientCount

**ShowExternalRecipientCount**元素指示是否[GetMailTips 操作](getmailtips-operation.md)的使用者具有显示邮件提示指示邮件要发送到外部收件人的数量。 
  
```XML
<ShowExternalRecipientCount>true | false</ShowExternalRecipientCount>
```

 **Boolean**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[MailTipsConfiguration (MailTipsServiceConfiguration)](mailtipsconfiguration-mailtipsserviceconfiguration.md) <br/> |包含邮件提示服务的服务配置信息。  <br/> |
   
## <a name="text-value"></a>文本值

此元素的文本值为**true** ，如果[GetMailTips 操作](getmailtips-operation.md)的使用者必须显示邮件提示指示邮件要发送到外部收件人的数量。 如果[GetMailTips 操作](getmailtips-operation.md)的使用者没有显示指示邮件要发送到外部收件人数的邮件提示，则值为**false** 。 
  
## <a name="remarks"></a>备注

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetMailTips 操作](getmailtips-operation.md)


- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

