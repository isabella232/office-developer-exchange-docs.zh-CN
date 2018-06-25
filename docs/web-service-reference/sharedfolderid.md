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
description: SharedFolderId 元素表示的本地文件夹标识符应返回 GetSharingFolder 操作请求的共享文件夹的标识符。
ms.openlocfilehash: 6d4e541ef3cae89e413efa8cc5f1beaf651dc4dd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827477"
---
# <a name="sharedfolderid"></a>SharedFolderId

**SharedFolderId**元素表示的本地文件夹标识符应返回[GetSharingFolder 操作](getsharingfolder-operation.md)请求的共享文件夹的标识符。 
  
```xml
<SharedFolderId/>
```

 **NonEmptyStringType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetSharingFolder](getsharingfolder.md) <br/> |定义一个请求以获取指定的共享文件夹的本地文件夹标识符。  <br/> |
   
## <a name="text-value"></a>文本值

文本值是一个字符串，表示为其的本地文件夹标识符应返回[GetSharingFolder 操作](getsharingfolder-operation.md)请求的共享文件夹的标识符。 
  
## <a name="remarks"></a>备注

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetSharingFolder 操作](getsharingfolder-operation.md)


- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

