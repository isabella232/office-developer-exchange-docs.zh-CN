---
title: Room
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Room
api_type:
- schema
ms.assetid: a2cde8b8-2d31-4ebf-8171-f4dfd650d079
description: Room 元素表示会议室。
ms.openlocfilehash: 062b89652ba809f245c1ac3ccee1005cbf0eabbd
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523536"
---
# <a name="room"></a>Room

**Room** 元素表示会议室。 
  
[Rooms](rooms.md)
  
[Room](room.md)
  
```XML
<Room>
   <Id/>
</Room>
```

 **RoomType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Id (EmailAddressType)](id-emailaddresstype.md) <br/> |包含电子邮件地址和代表会议室显示名称标识符。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Rooms](rooms.md) <br/> |定义与常见功能（如位于同一大楼）关联的会议室列表。  <br/> |
   
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetRooms 操作](getrooms-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

