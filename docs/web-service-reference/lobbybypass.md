---
title: LobbyBypass
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: e05ed6eb-00ae-49c8-8341-43f6e0d728ff
description: LobbyBypass 元素指定绕过虚拟会议厅的联机会议设置。
ms.openlocfilehash: 41ab9c3f846112d2b679bbb477a0de355a477ffa
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540781"
---
# <a name="lobbybypass"></a>LobbyBypass

**LobbyBypass** 元素指定绕过虚拟会议厅的联机会议设置。 
  
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

**LobbyBypass** 元素的文本值可以是 **Disabled** 或 **EnabledForGatewayParticipants**。 **Disabled** 值指示大厅旁路处于禁用状态，因此所有与会者都必须通过虚拟会议厅访问。 **EnabledForGatewayParticipants** 值指示为电话参与者启用了会议厅旁路功能。 
  
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  

