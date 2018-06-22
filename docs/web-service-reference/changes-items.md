---
title: 更改 （项）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Changes
api_type:
- schema
ms.assetid: d3139fef-0455-4b89-babd-5d6783b50a58
description: 更改元素包含序列的数组的更改类型表示客户端上的项目和 Exchange 服务器上的项目之间的差异的类型。
ms.openlocfilehash: 8e38597276e3e3051a5c1494619d3220280e401f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753445"
---
# <a name="changes-items"></a>更改 （项）

**更改**元素包含序列的数组的更改类型表示客户端上的项目和 Exchange 服务器上的项目之间的差异的类型。 
  
[SyncFolderItemsResponse](syncfolderitemsresponse.md)
  
[ResponseMessages](responsemessages.md)
  
[SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md)
  
[更改 （项）](changes-items.md)
  
```xml
<Changes>
   <Create/>
   <Update/>
   <Delete/>
</Changes>
```

 **SyncFolderItemsChangesType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[创建 (ItemSync)](create-itemsync.md) <br/> |标识在本地客户端库中创建的单个项。  <br/> |
|[更新 (ItemSync)](update-itemsync.md) <br/> |标识要更新本地客户端存储中的单个项。  <br/> |
|[删除 (ItemSync)](delete-itemsync.md) <br/> |标识要删除在本地客户端库中的单个项。  <br/> |
|[ReadFlagChange](readflagchange.md) <br/> |读取项目后，在[SyncFolderItems 操作](syncfolderitems-operation.md)响应中返回。 此属性是只读的。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md) <br/> |包含状态和[SyncFolderItems 操作](syncfolderitems-operation.md)请求的结果。  <br/> |
   
## <a name="remarks"></a>备注

描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。
  
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

