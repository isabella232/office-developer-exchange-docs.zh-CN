---
title: String
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- String
api_type:
- schema
ms.assetid: e6e362b1-4526-49e1-b283-1c4bc4295874
description: String 元素表示项目、联系人、任务和对话使用的字符串。
ms.openlocfilehash: dd85cae34ddf829f00660c8b87feb9331505183c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59509292"
---
# <a name="string"></a>String

**String** 元素表示项目、联系人、任务和对话使用的字符串。 
  
```XML
<String/>
```

 **string**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Categories](categories-ex15websvcsotherref.md) <br/> |包含标识邮箱中项目属于哪些类别的字符串集合。  <br/> |
|[子女](children.md) <br/> |包含联系人的子项的名称。  <br/> |
|[Companies](companies.md) <br/> |表示与联系人或任务关联的公司的集合。  <br/> |
|[联系人](contacts-ex15websvcsotherref.md) <br/> |包含与任务关联的联系人列表。  <br/> |
|[GlobalCategories](globalcategories.md) <br/> |包含邮箱中所有会话项目的类别列表。  <br/> |
|[GlobalUniqueRecipients](globaluniquerecipients.md) <br/> |包含跨邮箱聚合的对话的收件人列表。  <br/> |
|[GlobalUniqueSenders](globaluniquesenders.md) <br/> |包含邮箱中会话项目的所有发件人的列表。  <br/> |
|[GlobalUniqueUnreadSenders](globaluniqueunreadsenders.md) <br/> |包含邮箱中所有文件夹之间发送了当前在此对话中未读的邮件的所有人员的列表。  <br/> |
|[ItemClasses](itemclasses.md) <br/> |包含必须标记在传入邮件上才能应用条件或例外的项目类的列表。  <br/> |
|[MessageClassifications](messageclassifications.md) <br/> |包含必须在传入邮件上标记才能应用条件或例外的邮件分类列表。  <br/> |
|[UniqueRecipients](uniquerecipients.md) <br/> |包含对话的收件人列表。 此元素是只读的。  <br/> |
|[UniqueSenders](uniquesenders.md) <br/> |包含当前文件夹中对话项目的所有发件人的列表。 此元素是只读的。  <br/> |
|[UniqueUnreadSenders](uniqueunreadsenders.md) <br/> |包含当前文件夹中的此对话中当前未读邮件的所有发送者的列表。  <br/> |
   
## <a name="text-value"></a>文本值

此元素的文本值是一个字符串，表示类别、联系人的子级、公司、对话的唯一收件人或与任务关联的联系人。
  
## <a name="remarks"></a>注解

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[FindConversation 操作](findconversation-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

