---
title: SyncFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncFolderId
api_type:
- schema
ms.assetid: 3645fa03-236d-4e5f-b8b9-5d98f7f35fa2
description: SyncFolderId 元素表示包含要同步的项的文件夹。
ms.openlocfilehash: 45a4a62c7d269861555089019db259eacab26ef0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838171"
---
# <a name="syncfolderid"></a>SyncFolderId

**SyncFolderId**元素表示包含要同步的项的文件夹。 
  
```xml
<SyncFolderId>
   <FolderId/>
</SyncFolderId>
```

 **TargetFolderIdType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[文件夹 Id](folderid.md) <br/> |包含一个文件夹的标识符和更改键。  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |标识可以通过名称引用的 MicrosoftExchange Server 2007 文件夹。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[SyncFolderHierarchy](syncfolderhierarchy.md) <br/> |定义同步 Exchange 存储中的文件夹层次结构的请求。  <br/> |
|[SyncFolderItems](syncfolderitems.md) <br/> |定义同步 Exchange 存储区文件夹中的项目的请求。  <br/> |
   
## <a name="remarks"></a>备注

描述此元素的架构位于运行 Exchange Server 2007 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[SyncFolderItems 操作](syncfolderitems-operation.md)


- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

