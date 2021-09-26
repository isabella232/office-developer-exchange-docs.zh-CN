---
title: DeleteFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DeleteFolder
api_type:
- schema
ms.assetid: e37963f4-af9e-4481-b389-16175711e66d
description: DeleteFolder元素定义删除从 Exchange 存储中的邮箱文件夹的请求。
ms.openlocfilehash: d1d64b84604acec54d9153144e5bfd7abaece94c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542475"
---
# <a name="deletefolder"></a>DeleteFolder

本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **DeleteFolder** 元素定义删除从 Exchange 存储中的邮箱文件夹的请求。 
  
```XML
<DeleteFolder DeleteType="">
   <FolderIds/>
</DeleteFolder>
```

 **DeleteFolderType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**DeleteType** <br/> |描述如何删除一个文件夹。此属性是必需的。  <br/> |
   
#### <a name="deletetype-attribute"></a>DeleteType 属性

|**值**|**说明**|
|:-----|:-----|
|HardDelete  <br/> |从存储区中永久移除文件夹。  <br/> |
|SoftDelete  <br/> |一个文件夹移动到垃圾站如果转储程序已启用。  <br/> |
|MoveToDeletedItems  <br/> |文件夹被移动到已删除邮件文件夹中。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[FolderIds](folderids.md) <br/> |包含用于标识要删除的文件夹的文件夹标识符的数组。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>注解

**MoveToDeletedItems** 和 **HardDelete** 选项是事务性的这意味着，Web 服务调用完成时，数据库将邮件移至已删除邮件文件夹或从Exchange数据库中永久删除该项目。这种行为是相同的MicrosoftExchange Server 2007和Exchange Server 2010。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [DeleteFolder 操作](deletefolder-operation.md)

