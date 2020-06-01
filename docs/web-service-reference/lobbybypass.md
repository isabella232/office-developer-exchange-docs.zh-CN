---
title: LobbyBypass
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e05ed6eb-00ae-49c8-8341-43f6e0d728ff
description: LobbyBypass 元素指定 "联机会议" 设置以绕过虚拟大厅。
ms.openlocfilehash: 6940428c944b9d4d64acc6dbbf3993576e1932eb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458094"
---
# <a name="lobbybypass"></a>LobbyBypass

**LobbyBypass**元素指定 "联机会议" 设置以绕过虚拟大厅。 
  
```XML
<LobbyBypass> Disabled | EnabledForGatewayParticipants </LobbyBypass>
```

 **LobbyBypassType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[OnlineMeetingSettings](onlinemeetingsettings.md)
  
## <a name="text-value"></a>文本值

**LobbyBypass**元素的文本值可以是**Disabled**或**EnabledForGatewayParticipants**。 **禁用**的值指示已禁用会议厅旁路，以便所有与会者都必须通过虚拟大厅访问。 **EnabledForGatewayParticipants**值指示已为电话参与者启用会议厅旁路。 
  
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  

