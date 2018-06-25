---
title: SyncScope
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncScope
api_type:
- schema
ms.assetid: e0ca231f-0374-4844-8d4c-ada8da167920
description: SyncScope 元素指定是否同步响应中返回项目或项目和文件夹的相关信息。
ms.openlocfilehash: 847c0244a8847364e29ea584b0c0b721f00d3064
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838178"
---
# <a name="syncscope"></a>SyncScope

**SyncScope**元素指定是否同步响应中返回项目或项目和文件夹的相关信息。 
  
```xml
<SyncScope>NormalItems or NormalAndAssociatedItems</SyncScope>
```

 **SyncFolderItemsScopeType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[SyncFolderItems](syncfolderitems.md) <br/> |定义同步 Exchange 存储区文件夹中的项目的请求的元素。  <br/> 以下是此元素的 XPath 表达式：  <br/> / SyncFolderItems  <br/> |
   
## <a name="text-value"></a>文本值

下表列出了**SyncScope**元素的可能值。 
  
**SyncScope 元素的值**

|**值**|**说明**|
|:-----|:-----|
|NormalItems  <br/> |指定同步响应中返回的仅文件夹中的项目。  <br/> |
|NormalAndAssociatedItems  <br/> |指定同步响应中返回的两个项目中的文件夹和文件夹的相关信息。  <br/> |
   
## <a name="remarks"></a>注解

描述此元素的架构位于运行 Microsoft Exchange Server 已安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[SyncFolderItems 操作](syncfolderitems-operation.md)


- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

