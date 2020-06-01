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
description: SyncScope 元素指定是否仅在同步响应中返回项目或项目和文件夹相关信息。
ms.openlocfilehash: 5ede26204c823a452189222075c784f24e98d188
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463032"
---
# <a name="syncscope"></a>SyncScope

**SyncScope**元素指定是否仅在同步响应中返回项目或项目和文件夹相关信息。 
  
```xml
<SyncScope>NormalItems or NormalAndAssociatedItems</SyncScope>
```

 **SyncFolderItemsScopeType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**描述**|
|:-----|:-----|
|[SyncFolderItems](syncfolderitems.md) <br/> |定义对 Exchange 存储文件夹中的项目的同步的请求的元素。  <br/> 下面是此元素的 XPath 表达式：   <br/> /SyncFolderItems  <br/> |
   
## <a name="text-value"></a>文本值

下表列出了**SyncScope**元素的可能值。 
  
**SyncScope 元素值**

|**值**|**说明**|
|:-----|:-----|
|NormalItems  <br/> |指定在同步响应中仅返回文件夹中的项目。  <br/> |
|NormalAndAssociatedItems  <br/> |指定在同步响应中返回与文件夹和文件夹相关联的信息中的两个项目。  <br/> |
   
## <a name="remarks"></a>备注

描述此元素的架构位于运行 Microsoft Exchange Server 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[SyncFolderItems 操作](syncfolderitems-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

