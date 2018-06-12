---
title: String
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- String
api_type:
- schema
ms.assetid: e6e362b1-4526-49e1-b283-1c4bc4295874
description: 字符串元素表示由项目、 联系人、 任务和对话的字符串。
ms.openlocfilehash: 66260c7ebcb56049a78c5eddbe057dfa8d61f193
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827607"
---
# <a name="string"></a>String

**字符串**元素表示由项目、 联系人、 任务和对话的字符串。 
  
```XML
<String/>
```

 **string**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Categories](categories-ex15websvcsotherref.md) <br/> |包含标识的邮箱中项目所属的类别的字符串的集合。  <br/> |
|[子女](children.md) <br/> |包含联系人的子项的名称。  <br/> |
|[公司](companies.md) <br/> |代表与一个联系人或任务相关联的公司的集合。  <br/> |
|[联系人](contacts-ex15websvcsotherref.md) <br/> |包含与任务相关联的联系人的列表。  <br/> |
|[GlobalCategories](globalcategories.md) <br/> |包含在邮箱中的所有对话项目类别列表。  <br/> |
|[GlobalUniqueRecipients](globaluniquerecipients.md) <br/> |包含跨邮箱聚合对话的收件人列表。  <br/> |
|[GlobalUniqueSenders](globaluniquesenders.md) <br/> |包含所有发件人的邮箱中的会话项目的列表。  <br/> |
|[GlobalUniqueUnreadSenders](globaluniqueunreadsenders.md) <br/> |包含所有已发送邮件的邮箱中的所有文件夹中的当前未读此对话中的人员列表。  <br/> |
|[ItemClasses](itemclasses.md) <br/> |包含必须在应用的条件或例外顺序中的传入邮件标记的项类的列表。  <br/> |
|[MessageClassifications](messageclassifications.md) <br/> |包含必须在应用的条件或例外顺序中的传入邮件标记邮件分类的列表。  <br/> |
|[UniqueRecipients](uniquerecipients.md) <br/> |包含收件人对话的列表。 此元素是只读的。  <br/> |
|[UniqueSenders](uniquesenders.md) <br/> |包含当前文件夹中的会话项目的所有发件人的列表。 此元素是只读的。  <br/> |
|[UniqueUnreadSenders](uniqueunreadsenders.md) <br/> |包含所有已发送邮件的当前文件夹中的此对话中当前未读的人员列表。  <br/> |
   
## <a name="text-value"></a>文本值

此元素的文本值是一个字符串，表示一个类别的子级的联系人、 公司、 唯一收件人的对话或与任务相关联的联系人。
  
## <a name="remarks"></a>备注

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[FindConversation Operation](findconversation-operation.md)


- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

