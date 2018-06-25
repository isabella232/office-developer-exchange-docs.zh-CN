---
title: SizeRequested
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e86f98b6-83b5-4530-80eb-dc5df42e2c62
description: SizeRequested 元素包含 GetUserPhoto 操作的请求的照片大小。
ms.openlocfilehash: 43e422512b1e8f06e410e533e9ae1dc49283d5f6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827504"
---
# <a name="sizerequested"></a>SizeRequested

**SizeRequested**元素包含**GetUserPhoto**操作的请求的照片大小。 
  
```XML
<SizeRequested>HR48x48 | HR64x64 | HR96X96 | HR120X120 | HR240X240 | HR360X360 | HR432X432 | HR504X504 | HR648X648</SizeRequested>
```

 **UserPhotoSizeType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[GetUserPhoto](getuserphoto.md)
  
## <a name="text-value"></a>文本值

**SizeRequested**元素的文本值是从服务器返回的数字图像请求的照片大小。 下表标识**SizeRequested**元素的文本值。 
  
|**值**|**含义**|
|:-----|:-----|
|HR48x48  <br/> |48 像素高并 48 像素宽，图像。  <br/> |
|HR64x64  <br/> |64 像素高并 64 像素宽，图像。  <br/> |
|HR96x96  <br/> |96 像素高并 96 像素宽，图像。  <br/> |
|HR120x120  <br/> |120 像素高并 120 像素宽，图像。  <br/> |
|HR240x240  <br/> |240 像素高并 240 像素宽，图像。  <br/> |
|HR360x360  <br/> |360 像素高并 360 像素宽，图像。  <br/> |
|HR432x432  <br/> |432 像素高并 432 像素宽，图像。  <br/> |
|HR504x504  <br/> |504 像素高并 504 像素宽，图像。  <br/> |
|HR648x648  <br/> |648 像素 x 高并 648 像素宽，图像。  <br/> |
   
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> ||
   

