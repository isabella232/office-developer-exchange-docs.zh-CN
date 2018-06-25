---
title: DLExpansion
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DLExpansion
api_type:
- schema
ms.assetid: 9e50278d-fe6a-45e2-a72b-0fb06809e128
description: DLExpansion 元素包含一个数组包含通讯组列表中的邮箱。
ms.openlocfilehash: 06081b4aba761a7137f921b3bc1c8d6b2afab88c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753967"
---
# <a name="dlexpansion"></a>DLExpansion

**DLExpansion**元素包含一个数组包含通讯组列表中的邮箱。 
  
- [ExpandDLResponse](expanddlresponse.md) 
- [ResponseMessages](responsemessages.md) 
- [ExpandDLResponseMessage](expanddlresponsemessage.md)
- [DLExpansion](dlexpansion.md)
  
```xml
<DLExpansion AbsoluteDenominator"" IncludesLastItemInRange="" IndexedPagingOffset="" NumeratorOffset="" TotalItemsInView="">
   <Mailbox/>
</DLExpansion>
```

 **ArrayOfDLExpansionType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|**IndexedPagingOffset** <br/> |表示使用索引的页面视图时，则在下一个请求时应使用的下一个索引。  <br/> |
|**NumeratorOffset** <br/> |代表要使用分数页面视图时使用的下一个请求的新分子值。  <br/> |
|**AbsoluteDenominator** <br/> |代表下一个分母使用分数页面视图时用于下一个请求。  <br/> |
|**IncludesLastItemInRange** <br/> |指示当前结果是否包含在查询中的最后一项，以便不需要其他分页。  <br/> |
|**TotalItemsInView** <br/> |代表视图中的项目的总数。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Mailbox](mailbox.md) <br/> |标识已启用邮件的Active Directory目录服务对象。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ExpandDLResponseMessage](expanddlresponsemessage.md) <br/> |包含状态和单个 ExpandDL 请求的结果。  <br/> |
   
## <a name="remarks"></a>备注

描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [ExpandDL 操作](expanddl-operation.md)
- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md) 
- [Exchange 的 EWS 引用](ews-reference-for-exchange.md)

