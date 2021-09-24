---
title: Data
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Data
api_type:
- schema
ms.assetid: f875e6c2-be18-439a-a7b1-bb49a149b538
description: Data 元素包含表示共享数据的加密数据。
ms.openlocfilehash: 1c28790467674e3ef44c9f0dc9e1fd706f880641
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59535861"
---
# <a name="data"></a>Data

**Data** 元素包含表示共享数据的加密数据。 
  
- [EncryptedSharedFolderData](encryptedsharedfolderdata.md)  
- [Data](data.md)
  
```xml
<Data/>
```

**EncryptedDataContainerType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[EncryptedSharedFolderData](encryptedsharedfolderdata.md) <br/> |包含客户端用于授权与其他客户端共享其日历或联系人数据的加密数据。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>注解

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
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

