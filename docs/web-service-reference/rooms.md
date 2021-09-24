---
title: Rooms
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Rooms
api_type:
- schema
ms.assetid: 57b6079a-3d83-4429-861e-c551e9e1a991
description: Rooms 元素是表示会议室的一个或多个元素的列表。
ms.openlocfilehash: bcefa1fb380599e556b7c3e99235afc2057b1017
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524481"
---
# <a name="rooms"></a>Rooms

Rooms 元素是表示会议室的一个或多个元素的列表。 
  
[GetRoomsResponse](getroomsresponse.md)
  
[Rooms](rooms.md)
  
```xml
<Rooms>   <Room/></Rooms>
```

 **ArrayOfRoomsType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Room](room.md) <br/> |定义一个代表会议室显示名称电子邮件地址和电子邮件地址。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetRoomsResponse](getroomsresponse.md) <br/> ||
   
## <a name="remarks"></a>注解

描述此元素的架构位于运行安装了客户端访问服务器角色Microsoft Exchange Server的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetRooms 操作](getrooms-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

