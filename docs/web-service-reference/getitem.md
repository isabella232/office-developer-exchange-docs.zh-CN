---
title: GetItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GetItem
api_type:
- schema
ms.assetid: 769df8eb-9c72-48b5-a49f-82c6b86bc5fc
description: GetItem 元素定义从邮件存储中的邮箱获取Exchange请求。
ms.openlocfilehash: 7d5a7253db54fd67bb8e8772c2a5aedb86abdeee
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546229"
---
# <a name="getitem"></a>GetItem

**GetItem** 元素定义从邮件存储中的邮箱获取Exchange请求。 
  
```xml
<GetItem>
   <ItemShape/>
   <ItemIds/>
</GetItem>
```

 **GetItemType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ItemShape](itemshape.md) <br/> |标识要包括在 **GetItem** 响应中的项目属性和内容。  <br/> |
|[ItemIds](itemids.md) <br/> |包含项目、发生项和定期主项目的唯一标识，这些项用于从项目存储Exchange项。 这些项目表示邮箱中的联系人、任务、邮件、日历项目、会议请求和其他有效项目。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>注解

描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetItem 操作](getitem-operation.md)

