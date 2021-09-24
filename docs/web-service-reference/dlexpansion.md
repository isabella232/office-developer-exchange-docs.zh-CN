---
title: DLExpansion
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DLExpansion
api_type:
- schema
ms.assetid: 9e50278d-fe6a-45e2-a72b-0fb06809e128
description: DLExpansion 元素包含一组包含在通讯组列表中的邮箱。
ms.openlocfilehash: 7c214948b133ea2f30a47b2321c27b555b90e2fa
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517208"
---
# <a name="dlexpansion"></a>DLExpansion

**DLExpansion** 元素包含一组包含在通讯组列表中的邮箱。 
  
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

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**IndexedPagingOffset** <br/> |表示应在使用索引页面视图时用于下一个请求的下一个索引。  <br/> |
|**NumeratorOffset** <br/> |表示使用分数页面视图时用于下一个请求的新分子值。  <br/> |
|**AbsoluteDenominator** <br/> |表示在使用分数页面视图时用于下一个请求的下一个分母。  <br/> |
|**IncludesLastItemInRange** <br/> |指示当前结果是否包含查询中的最后一项，以便不需要其他分页。  <br/> |
|**TotalItemsInView** <br/> |表示视图中的项目总数。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Mailbox](mailbox.md) <br/> |标识已启用邮件的Active Directory目录服务对象。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ExpandDLResponseMessage](expanddlresponsemessage.md) <br/> |包含单个 ExpandDL 请求的状态和结果。  <br/> |
   
## <a name="remarks"></a>说明

描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [ExpandDL 操作](expanddl-operation.md)
- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md) 
- [Exchange 的 EWS 引用](ews-reference-for-exchange.md)

