---
title: ReadFlagChange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ReadFlagChange
api_type:
- schema
ms.assetid: 527bfe90-63d0-4b2f-97f7-7875b3a516b2
description: 读取项目后，在 SyncFolderItems 操作响应中返回 ReadFlagChange 元素。 此属性是只读的。
ms.openlocfilehash: 8a03f32a54b2e9dd7e84bf77a01092f6bb3cbf19
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542909"
---
# <a name="readflagchange"></a>ReadFlagChange

读取项目后，[在 SyncFolderItems](syncfolderitems-operation.md)操作响应中返回 **ReadFlagChange** 元素。 此属性是只读的。 
  
```xml
<ReadFlagChange>
   <ItemId/>
   <IsRead/>
</ReadFlagChange>
```

 **SyncFolderItemsReadFlagType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ItemId](itemid.md) <br/> |标识已更改其读取标志的项。  <br/> |
|[IsRead](isread.md) <br/> |指示是否已将读取标志设置为 **true**。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Changes (Items)](changes-items.md) <br/> |包含一个变更类型的序列数组，这些更改类型表示客户端上的项目与客户端服务器上项目Exchange类型。  <br/> |
   
## <a name="remarks"></a>注解

描述此元素的架构位于运行 Microsoft Exchange Server 2010（已安装客户端访问服务器角色）的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

