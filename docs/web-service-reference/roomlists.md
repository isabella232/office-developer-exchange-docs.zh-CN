---
title: RoomLists
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- RoomLists
api_type:
- schema
ms.assetid: 2b190823-b11e-4635-97e4-3aba5865fd05
description: RoomLists 元素是表示会议室列表的一个或多个地址的列表。
ms.openlocfilehash: e2825ccf5f660e00da61a605282613c07678a74b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523487"
---
# <a name="roomlists"></a>RoomLists

**RoomLists** 元素是表示会议室列表的一个或多个地址的列表。 
  
[GetRoomListsResponse](getroomlistsresponse.md)
  
[RoomLists](roomlists.md)
  
```xml
<RoomLists>   <Address/></RoomLists>
```

 **ArrayOfEmailAddressesType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[地址 (EmailAddressType)](address-emailaddresstype.md) <br/> |定义代表会议室列表显示名称和电子邮件地址。 此元素为可选。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetRoomListsResponse](getroomlistsresponse.md) <br/> |包含 [GetRoomLists](getroomlists-operation.md) 操作请求的状态和结果。  <br/> |
   
## <a name="remarks"></a>注解

描述此元素的架构位于在安装了客户端访问服务器角色Exchange Server运行的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetRoomLists 操作](getroomlists-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

