---
title: SharedFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SharedFolderId
api_type:
- schema
ms.assetid: 21181ba3-9626-4284-9717-0b1c16948e8f
description: SharedFolderId 元素表示共享文件夹的标识符，该标识符是应由 GetSharingFolder 操作请求返回的本地文件夹标识符。
ms.openlocfilehash: 546e148540708725bcf335f39bf69d193124d210
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466120"
---
# <a name="sharedfolderid"></a>SharedFolderId

**SharedFolderId**元素表示共享文件夹的标识符，该标识符是应由[GetSharingFolder 操作](getsharingfolder-operation.md)请求返回的本地文件夹标识符。 
  
```xml
<SharedFolderId/>
```

 **NonEmptyStringType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetSharingFolder](getsharingfolder.md) <br/> |定义获取指定共享文件夹的本地文件夹标识符的请求。  <br/> |
   
## <a name="text-value"></a>文本值

Text 值是一个字符串，表示共享文件夹的标识符，该标识符是应由[GetSharingFolder 操作](getsharingfolder-operation.md)请求返回的本地文件夹标识符。 
  
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetSharingFolder 操作](getsharingfolder-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

