---
title: ReferenceItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ReferenceItemId
api_type:
- schema
ms.assetid: 8fd4bb12-a94b-43f5-be3b-f435684e311d
description: ReferenceItemId 元素标识响应对象引用的项。
ms.openlocfilehash: b6ddb59eb3f266aff6400429ac8178f5640bf06b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542854"
---
# <a name="referenceitemid"></a>ReferenceItemId

**ReferenceItemId** 元素标识响应对象引用的项。 
  
```xml
<ReferenceItemId Id="" ChangeKey="" />
```

 **ItemIdType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**Id** <br/> |标识数据存储区中的Exchange项。  <br/> |
|**ChangeKey** <br/> |标识项目的特定版本。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[AcceptItem](acceptitem.md) <br/> |表示接受答复会议要求。  <br/> |
|[AcceptSharingInvitation](acceptsharinginvitation.md) <br/> |代表"接受"对共享邀请的答复。  <br/> |
|[CancelCalendarItem](cancelcalendaritem.md) <br/> |表示用于取消会议的响应对象。  <br/> |
|[DeclineItem](declineitem.md) <br/> |表示谢绝答复会议要求。  <br/> |
|[ForwardItem](forwarditem.md) <br/> |包含要转发给收件人的 Exchange 存储区项。  <br/> |
|[RemoveItem](removeitem.md) <br/> |从 Exchange 存储中删除一个项目。  <br/> |
|[ReplyAllToItem](replyalltoitem.md) <br/> |包含对所有确定收件人的 Exchange 存储中的项的答复。  <br/> |
|[ReplyToItem](replytoitem.md) <br/> |包含对 Exchange 存储中的项的创建者的答复。  <br/> |
|[SuppressReadReceipt](suppressreadreceipt.md) <br/> |用于响应已读回执请求。  <br/> |
|[TentativelyAcceptItem](tentativelyacceptitem.md) <br/> |表示一个暂定答复会议要求。  <br/> |
   
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



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

