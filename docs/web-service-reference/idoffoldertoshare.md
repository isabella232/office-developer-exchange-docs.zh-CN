---
title: IdOfFolderToShare
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IdOfFolderToShare
api_type:
- schema
ms.assetid: 199d1839-f061-4070-a977-874b0c08e5be
description: IdOfFolderToShare 元素表示要共享的服务器上文件夹的标识符。
ms.openlocfilehash: fdacd9c5f9e3c5c2ad55164bcd3abedeb1650f3d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516697"
---
# <a name="idoffoldertoshare"></a>IdOfFolderToShare

**IdOfFolderToShare** 元素表示要共享的服务器上文件夹的标识符。 
  
```
<IdOfFolderToShare Id="" ChangeKey="" />
```

 **FolderIdType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|Id  <br/> |包含一个字符串，用于标识 Exchange 存储区中的文件夹。 此特性是必需的。  <br/> |
|ChangeKey  <br/> |包含一个标识由 Id 属性标识的文件夹版本的字符串。 此特性是可选的。 使用此属性确保使用正确版本的文件夹。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetSharingMetadata](getsharingmetadata.md) <br/> |定义获取标识共享邀请的不透明身份验证令牌的请求。  <br/> |
   
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



[GetSharingMetadata 操作](getsharingmetadata-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

