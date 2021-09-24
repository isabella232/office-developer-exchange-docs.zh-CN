---
title: ParentItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ParentItemId
api_type:
- schema
ms.assetid: 72dc4391-72db-44d2-85d9-4718d59886a7
description: ParentItemId 元素标识链接到关联附件的父项。
ms.openlocfilehash: d8072e86d8bd989d4baf6b0f29385dc955b83de8
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515360"
---
# <a name="parentitemid"></a>ParentItemId

**ParentItemId** 元素标识链接到关联附件的父项。 
  
- [CreateAttachment](createattachment.md)
  
- [ParentItemId](parentitemid.md)
  
```xml
<ParentItemId Id="" ChangeKey="" />
```

**ItemIdType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**Id** <br/> |标识要与附件Exchange存储中的单个项目。 此值为字符串。 此特性是必需的。  <br/> |
|**ChangeKey** <br/> |标识由项目存储中的 **Id** 属性标识的未指定Exchange版本。 这用于确保使用附件更新当前项目。 此值为字符串。 此特性是可选的。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[CreateAttachment](createattachment.md) <br/> |定义创建邮箱中项目的附件的请求。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/CreateAttachment` <br/> |
   
## <a name="remarks"></a>注解

[CreateAttachment](createattachment-operation.md)操作 中需要此元素。 此元素基本上与 [ItemId 元素](itemid.md) 相同。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |[https://schemas.microsoft.com/exchange/services/2006/messages](https://schemas.microsoft.com/exchange/services/2006/messages) <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [CreateAttachment 操作](createattachment-operation.md)

