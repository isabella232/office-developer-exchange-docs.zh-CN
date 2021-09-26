---
title: SizeRequested
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: e86f98b6-83b5-4530-80eb-dc5df42e2c62
description: SizeRequested 元素包含 GetUserPhoto 操作请求的照片大小。
ms.openlocfilehash: 799869a85d7f72e79753a73f9c259388a2702bf5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59545914"
---
# <a name="sizerequested"></a>SizeRequested

**SizeRequested** 元素包含 **GetUserPhoto** 操作请求的照片大小。 
  
```XML
<SizeRequested>HR48x48 | HR64x64 | HR96X96 | HR120X120 | HR240X240 | HR360X360 | HR432X432 | HR504X504 | HR648X648</SizeRequested>
```

 **UserPhotoSizeType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[GetUserPhoto](getuserphoto.md)
  
## <a name="text-value"></a>文本值

**SizeRequested** 元素的文本值是从服务器返回的数字图像请求的照片大小。 下表标识 **SizeRequested** 元素的文本值。 
  
|**值**|**含义**|
|:-----|:-----|
|HR48x48  <br/> |图像高 48 像素，宽 48 像素。  <br/> |
|HR64x64  <br/> |图像高 64 像素，宽 64 像素。  <br/> |
|HR96x96  <br/> |图像高 96 像素，宽 96 像素。  <br/> |
|HR120x120  <br/> |图像高 120 像素，宽 120 像素。  <br/> |
|HR240x240  <br/> |图像高 240 像素，宽 240 像素。  <br/> |
|HR360x360  <br/> |图像高 360 像素，宽 360 像素。  <br/> |
|HR432x432  <br/> |图像高 432 像素，宽 432 像素。  <br/> |
|HR504x504  <br/> |图像高 504 像素，宽 504 像素。  <br/> |
|HR648x648  <br/> |图像高 648 像素，宽 648 像素。  <br/> |
   
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> ||
   

