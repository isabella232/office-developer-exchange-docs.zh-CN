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
description: String 元素表示项目、联系人、任务和对话使用的字符串。
ms.openlocfilehash: fbb4219d35c4acdc2c80b21b73e6479a2ef317f7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463102"
---
# <a name="string"></a>String

**String**元素表示项目、联系人、任务和对话使用的字符串。 
  
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
|[Categories](categories-ex15websvcsotherref.md) <br/> |包含一个字符串集合，这些字符串标识邮箱中的项目所属的类别。  <br/> |
|[子女](children.md) <br/> |包含联系人的子项的名称。  <br/> |
|[Companies](companies.md) <br/> |表示与某个联系人或任务相关联的公司的集合。  <br/> |
|[联系人](contacts-ex15websvcsotherref.md) <br/> |包含与任务相关联的联系人的列表。  <br/> |
|[GlobalCategories](globalcategories.md) <br/> |包含邮箱中所有会话项目的类别列表。  <br/> |
|[GlobalUniqueRecipients](globaluniquerecipients.md) <br/> |包含在邮箱中聚合的对话的收件人列表。  <br/> |
|[GlobalUniqueSenders](globaluniquesenders.md) <br/> |包含邮箱中对话项目的所有发件人的列表。  <br/> |
|[GlobalUniqueUnreadSenders](globaluniqueunreadsenders.md) <br/> |包含所有已在此对话中的所有文件夹中发送当前未读邮件的人员的列表。  <br/> |
|[ItemClasses](itemclasses.md) <br/> |包含必须在传入的邮件上标记的项目类的列表，以便条件或例外情况适用。  <br/> |
|[MessageClassifications](messageclassifications.md) <br/> |包含必须在传入的邮件上标记的邮件分类的列表，以便条件或例外情况适用。  <br/> |
|[UniqueRecipients](uniquerecipients.md) <br/> |包含对话的收件人列表。 此元素是只读的。  <br/> |
|[UniqueSenders](uniquesenders.md) <br/> |包含当前文件夹中会话项目的所有发件人的列表。 此元素是只读的。  <br/> |
|[UniqueUnreadSenders](uniqueunreadsenders.md) <br/> |包含已发送当前文件夹中此对话中当前未读邮件的所有人员的列表。  <br/> |
   
## <a name="text-value"></a>文本值

此元素的文本值是一个字符串，表示类别、联系人的子女、公司、对话的唯一收件人或与任务相关联的联系人。
  
## <a name="remarks"></a>备注

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

