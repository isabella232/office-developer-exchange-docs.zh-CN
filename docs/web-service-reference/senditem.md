---
title: SendItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SendItem
api_type:
- schema
ms.assetid: a966da19-b05a-4504-ac98-91acc1667b9a
description: SendItem 元素是请求发送 Exchange 存储中的项中的根元素。
ms.openlocfilehash: c5ce52ee4643219aa31ae59e8b7d40d7a904c8ab
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827340"
---
# <a name="senditem"></a>SendItem

**SendItem**元素是请求发送 Exchange 存储中的项中的根元素。 
  
```xml
<SendItem SaveItemToFolder="">
   <ItemIds/>
   <SavedItemFolderId/>
</SendItem>
```

 **SendItemType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|**SaveItemToFolder** <br/> |标识是否保存一份发送项目。 保存操作取决于**SaveItemToFolder**和[SavedItemFolderId](saveditemfolderid.md)元素是否存在于请求中的值。 此元素是必需的。  <br/> |
   
#### <a name="saveitemtofolder-attribute"></a>SaveItemToFolder 属性

|**值**|**说明**|
|:-----|:-----|
|**true** <br/> |如果不存在的[SavedItemFolderId](saveditemfolderid.md)元素，则在已发送邮件文件夹中保存项目。 如果[SavedItemFolderId](saveditemfolderid.md)元素存在，由[SavedItemFolderId](saveditemfolderid.md)元素指定的文件夹中保存项目。  <br/> |
|**false** <br/> |如果[SavedItemFolderId](saveditemfolderid.md)元素不存在，则不会保存项目。 如果[SavedItemFolderId](saveditemfolderid.md)元素存在，将返回错误响应与[ResponseCode](responsecode.md)元素包含**ErrorInvalidSendItemSaveSettings**值。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ItemIds](itemids.md) <br/> |包含唯一标识的项目和匹配项，用于删除、 发送、 获取、 移动或在 Exchange 存储中复制项的定期主项目。  <br/> |
|[SavedItemFolderId](saveditemfolderid.md) <br/> |标识用于更新、 发送和在 Exchange 存储中创建项目的操作的目标文件夹。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>备注

如果发送发送邮件文件夹中的项目，删除发送的项目并将它的一个副本置于发送邮件文件夹。
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[SendItem 操作](senditem-operation.md)

