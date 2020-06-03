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
description: SendItem 元素是在 Exchange 存储中发送项目的请求中的根元素。
ms.openlocfilehash: 28f0d484dd079146c998cb7317bd2d80c6739e19
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530563"
---
# <a name="senditem"></a>SendItem

**SendItem**元素是在 Exchange 存储中发送项目的请求中的根元素。 
  
```xml
<SendItem SaveItemToFolder="">
   <ItemIds/>
   <SavedItemFolderId/>
</SendItem>
```

 **SendItemType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**SaveItemToFolder** <br/> |标识是否保存已发送项目的副本。 Save 操作取决于**SaveItemToFolder**的值，以及请求中是否存在[SavedItemFolderId](saveditemfolderid.md)元素。 此元素是必需的。  <br/> |
   
#### <a name="saveitemtofolder-attribute"></a>SaveItemToFolder 属性

|**值**|**说明**|
|:-----|:-----|
|**true** <br/> |如果[SavedItemFolderId](saveditemfolderid.md)元素不存在，则会将该项目保存在 "已发送邮件" 文件夹中。 如果存在[SavedItemFolderId](saveditemfolderid.md)元素，则会将该项目保存在由[SavedItemFolderId](saveditemfolderid.md)元素指定的文件夹中。  <br/> |
|**该值** <br/> |如果不存在[SavedItemFolderId](saveditemfolderid.md)元素，则不会保存项目。 如果存在[SavedItemFolderId](saveditemfolderid.md)元素，则将返回一个包含**ErrorInvalidSendItemSaveSettings**值的[ResponseCode](responsecode.md)元素的错误响应。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**描述**|
|:-----|:-----|
|[ItemIds](itemids.md) <br/> |包含项目、具体值项目和定期主项目的唯一标识，这些标识用于删除、发送、获取、移动或复制 Exchange 存储中的项目。  <br/> |
|[SavedItemFolderId](saveditemfolderid.md) <br/> |标识在 Exchange 存储中更新、发送和创建项目的操作的目标文件夹。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>说明

如果发送了 "已发送邮件" 文件夹中的项目，则会删除已发送邮件，并将其副本放在 "已发送邮件" 文件夹中。
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[SendItem 操作](senditem-operation.md)

