---
title: RemoveOutlookRuleBlob
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RemoveOutlookRuleBlob
api_type:
- schema
ms.assetid: 69614475-8bd3-4475-b988-614fe9cad8ef
description: RemoveOutlookRuleBlob 元素指示是否删除 Microsoft Outlook 规则 blob。
ms.openlocfilehash: b4202ab52bf16d1ad1546ec963cd8b9dacd2bd63
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467667"
---
# <a name="removeoutlookruleblob"></a>RemoveOutlookRuleBlob

**RemoveOutlookRuleBlob**元素指示是否删除 Microsoft Outlook 规则 blob。 
  
[UpdateInboxRules](updateinboxrules.md)
  
[RemoveOutlookRuleBlob](removeoutlookruleblob.md)
  
```XML
<RemoveOutlookRuleBlob>true | false</RemoveOutlookRuleBlob>
```

 **Boolean**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[UpdateInboxRules](updateinboxrules.md) <br/> |定义更新服务器存储中的邮箱的收件箱规则的请求。  <br/> |
   
## <a name="text-value"></a>文本值

如果文本值为**true** ，则表示应删除 Outlook 规则 blob。 如果文本值为**false** ，则表示不应删除 Outlook 规则 blob。 
  
## <a name="remarks"></a>备注

将此元素设置为**true**以允许使用收件箱规则更新。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[UpdateInboxRules 操作](updateinboxrules-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

