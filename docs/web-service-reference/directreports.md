---
title: DirectReports
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: ab88739f-9018-4887-ae46-f1471242628c
description: DirectReports 元素包含标识联系人的直接下属的 SMTP 信息。
ms.openlocfilehash: a84e37836b645ec679208094ed893d04793f01d2
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542349"
---
# <a name="directreports"></a>DirectReports

**DirectReports** 元素包含标识联系人的直接下属的 SMTP 信息。 
  
```XML
<DirectReports>
   <Mailbox/>
</DirectReports>
```

 **SingleRecipientType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Mailbox](mailbox.md) <br/> |标识已启用邮件的Active Directory目录服务对象。  <br/> |
     
### <a name="parent-elements"></a>父元素

|**元素名**|**说明**|
|:-----|:-----|
|[Contact](contact.md) <br/> |表示应用商店中的联系人Exchange项。  <br/> |
   
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
Exchange Server 2010 Service Pack 2 (SP2) 中引入了此元素。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)
- [创建联系人（Exchange Web 服务）](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)

