---
title: SendItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SendItem
api_type:
- schema
ms.assetid: a966da19-b05a-4504-ac98-91acc1667b9a
description: SendItem 元素是请求发送活动存储中的项的根Exchange元素。
ms.openlocfilehash: 2d1613451e7f876f0b612a3249570412e40b4764
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521618"
---
# <a name="senditem"></a>SendItem

**SendItem** 元素是请求发送活动存储中的项的根Exchange元素。 
  
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
|**SaveItemToFolder** <br/> |标识是否已保存已发送项目的副本。 保存操作取决于 **SaveItemToFolder** 的值以及请求中是否包含 [SavedItemFolderId](saveditemfolderid.md) 元素。 此元素是必需的。  <br/> |
   
#### <a name="saveitemtofolder-attribute"></a>SaveItemToFolder 属性

|**值**|**说明**|
|:-----|:-----|
|**true** <br/> |如果 [SavedItemFolderId](saveditemfolderid.md) 元素不存在，该项目将保存在"已发送项目"文件夹中。 如果存在 [SavedItemFolderId](saveditemfolderid.md) 元素，则项目保存在 [SavedItemFolderId](saveditemfolderid.md) 元素指定的文件夹中。  <br/> |
|**false** <br/> |如果 [SavedItemFolderId](saveditemfolderid.md) 元素不存在，则不保存该项目。 如果存在 [SavedItemFolderId](saveditemfolderid.md)元素，则返回一个错误响应，其中包含 **ErrorInvalidSendItemSaveSettings** 值的 [ResponseCode](responsecode.md)元素。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ItemIds](itemids.md) <br/> |包含项目、发生项和定期主项目的唯一标识，这些项用于删除、发送、获取、移动或复制 Exchange 项。  <br/> |
|[SavedItemFolderId](saveditemfolderid.md) <br/> |标识用于更新、发送和创建邮件存储中项目的操作Exchange文件夹。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>注解

如果已发送"已发送项目"文件夹中的某个项目，则删除已发送的项目，并且该项目的副本将放入"已发送项目"文件夹中。
  
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

