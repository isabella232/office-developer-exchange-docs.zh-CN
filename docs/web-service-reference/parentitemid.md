---
title: ParentItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ParentItemId
api_type:
- schema
ms.assetid: 72dc4391-72db-44d2-85d9-4718d59886a7
description: ParentItemId 元素标识链接到相关联的附件的父项目。
ms.openlocfilehash: 4f3e33da0af2438948313f0e335cd03e076d135a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465742"
---
# <a name="parentitemid"></a>ParentItemId

**ParentItemId**元素标识链接到相关联的附件的父项目。 
  
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
|**Id** <br/> |标识与附件关联的 Exchange 存储中的单个项目。 此值为字符串。 此特性是必需的。  <br/> |
|**ChangeKey** <br/> |标识由 Exchange 存储中的**Id**属性标识的项目的未指定版本。 这用于确保在使用附件更新当前项时使用它。 此值为字符串。 此特性是可选的。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[CreateAttachment](createattachment.md) <br/> |定义在邮箱中创建项目附件的请求。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/CreateAttachment` <br/> |
   
## <a name="remarks"></a>备注

在[CreateAttachment 操作](createattachment-operation.md)中，此元素是必需的。 此元素基本上与[ItemId](itemid.md)元素相同。 
  
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

