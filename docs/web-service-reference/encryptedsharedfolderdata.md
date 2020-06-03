---
title: EncryptedSharedFolderData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EncryptedSharedFolderData
api_type:
- schema
ms.assetid: c1d4ca18-c5ce-41ff-bab4-f75e358c8b9f
description: EncryptedSharedFolderData 元素包含加密的数据，客户端可以使用这些数据来授权与其他客户端共享其日历或联系人数据。
ms.openlocfilehash: 52e91eaf1ded31602b11e50c1b62159f72c101cd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530661"
---
# <a name="encryptedsharedfolderdata"></a>EncryptedSharedFolderData

**EncryptedSharedFolderData**元素包含加密的数据，客户端可以使用这些数据来授权与其他客户端共享其日历或联系人数据。 
  
```xml
<EncryptedSharedFolderData>   <Token/>   <Data/></EncryptedSharedFolderData>
```

 **EncryptedSharedFolderDataType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[标记](token.md) <br/> |包含表示共享数据标识令牌的加密数据。  <br/> |
|[Data](data.md) <br/> |包含表示共享数据的加密数据。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[EncryptedSharedFolderDataCollection](encryptedsharedfolderdatacollection.md) <br/> |表示一组数据结构，客户端可以使用这些结构来授权与其他客户端共享其日历或联系人数据。  <br/> |
   
## <a name="remarks"></a>说明

描述该元素的架构位于 IIS 虚拟目录正在运行 Microsoft Exchange Server 的计算机的主机交换 Web 服务已安装了客户端访问服务器角色。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [GetSharingMetadata 操作](getsharingmetadata-operation.md)
- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

