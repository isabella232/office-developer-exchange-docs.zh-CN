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
description: SyncFolderItems 元素定义同步 Exchange 存储区文件夹中的项目的请求。
ms.openlocfilehash: 368e19babfccaeab40380103495c63d30647905c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838174"
---
# <a name="syncfolderitems"></a>SyncFolderItems

**SyncFolderItems**元素定义同步 Exchange 存储区文件夹中的项目的请求。 
  
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

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ItemShape](itemshape.md) <br/> |标识项目属性和 SyncFolderItems 响应中包括的内容。 此元素是必需的。  <br/> |
|[SyncFolderId](syncfolderid.md) <br/> |代表包含要同步的项的文件夹。 此元素是必需的。  <br/> |
|[SyncState](syncstate-ex15websvcsotherref.md) <br/> |包含 base64 编码的同步数据的每个请求成功后都会更新窗体。 这用于标识的同步状态。 此元素是可选的。  <br/> |
|[忽略](ignore.md) <br/> |标识同步过程中跳过的项目。 此元素是可选的。  <br/> |
|[MaxChangesReturned](maxchangesreturned.md) <br/> |介绍可以同步响应中返回的更改的最大数量。 此元素是必需的。  <br/> |
|[SyncScope](syncscope.md) <br/> |指定是否同步响应中返回项目或项目和文件夹的相关信息。 此元素是可选的。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>注解

描述此元素的架构位于运行 Microsoft Exchange Server 已安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |邮件架构  <br/> |
|验证文件  <br/> |messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[SyncFolderItems 操作](syncfolderitems-operation.md)


- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

