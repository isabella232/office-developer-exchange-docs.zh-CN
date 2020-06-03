---
title: SyncFolderItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncFolderItems
api_type:
- schema
ms.assetid: 463ed78c-bf82-4cd8-971a-d18425e9e7be
description: SyncFolderItems 元素定义对 Exchange 存储文件夹中的项目进行同步的请求。
ms.openlocfilehash: 0fa5b1544d5627d1423287369e72f97662c28d12
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465147"
---
# <a name="syncfolderitems"></a>SyncFolderItems

**SyncFolderItems**元素定义对 Exchange 存储文件夹中的项目进行同步的请求。 
  
```xml
<SyncFolderItems>
   <ItemShape/>
   <SyncFolderId/>
   <SyncState/>
   <Ignore/>
   <MaxChangesReturned/>   <SyncScope/>
</SyncFolderItems>
```

 **SyncFolderItemsType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ItemShape](itemshape.md) <br/> |标识要包含在 SyncFolderItems 响应中的项目属性和内容。 此元素是必需的。  <br/> |
|[SyncFolderId](syncfolderid.md) <br/> |表示包含要同步的项目的文件夹。 此元素是必需的。  <br/> |
|[SyncState](syncstate-ex15websvcsotherref.md) <br/> |包含在每次成功请求后更新的、base64 编码的格式的同步数据。 这用于标识同步状态。 此元素为可选。  <br/> |
|[忽略](ignore.md) <br/> |确定在同步过程中要跳过的项。 此元素为可选。  <br/> |
|[MaxChangesReturned](maxchangesreturned.md) <br/> |描述同步响应中可返回的最大更改数。 此元素是必需的。  <br/> |
|[SyncScope](syncscope.md) <br/> |指定是否在同步响应中仅返回项目或项目和文件夹相关信息。 此元素为可选。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>说明

描述此元素的架构位于运行 Microsoft Exchange Server 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |邮件架构  <br/> |
|验证文件  <br/> |消息 .xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[SyncFolderItems 操作](syncfolderitems-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

