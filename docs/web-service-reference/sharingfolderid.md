---
title: SharingFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SharingFolderId
api_type:
- schema
ms.assetid: 5ad37ceb-2922-4420-9051-c29d0d57c420
description: SharingFolderId 元素表示共享关系中的本地文件夹的标识符。
ms.openlocfilehash: 02780251639ee651ca65d8eadded43260852aaf8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526576"
---
# <a name="sharingfolderid"></a>SharingFolderId

**SharingFolderId**元素表示共享关系中的本地文件夹的标识符。 
  
```xml
<SharingFolderId Id="" ChangeKey="" />
```

 **FolderIdType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|Id  <br/> |包含标识 Exchange 存储中的文件夹的字符串。 此特性是必需的。  <br/> |
|ChangeKey  <br/> |包含标识由 Id 属性标识的文件夹版本的字符串。 此特性是可选的。 使用此属性可确保使用的是正确的文件夹版本。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[RefreshSharingFolder](refreshsharingfolder.md) <br/> |定义刷新指定的本地文件夹的请求。  <br/> |
|[GetSharingFolderResponse](getsharingfolderresponse.md) <br/> |定义对[GetSharingFolder 操作](getsharingfolder-operation.md)请求的响应。  <br/> |
|[GetSharingFolderResponseMessage](getsharingfolderresponsemessage.md) <br/> |包含单个[GetSharingFolder 操作](getsharingfolder-operation.md)请求的状态和结果。  <br/> |
   
## <a name="remarks"></a>说明

描述该元素的架构位于 IIS 虚拟目录正在运行 Microsoft Exchange Server 的计算机的主机交换 Web 服务已安装了客户端访问服务器角色。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

