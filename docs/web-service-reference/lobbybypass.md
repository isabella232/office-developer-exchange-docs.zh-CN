---
title: LobbyBypass
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e05ed6eb-00ae-49c8-8341-43f6e0d728ff
description: LobbyBypass 元素指定的设置以绕过虚拟会议厅的联机会议。
ms.openlocfilehash: 9ecc920acd9e1aea3476ad1194d6c7d0529b21c7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826246"
---
# <a name="lobbybypass"></a>LobbyBypass

**LobbyBypass**元素指定的设置以绕过虚拟会议厅的联机会议。 
  
```XML
<LobbyBypass> Disabled | EnabledForGatewayParticipants </LobbyBypass>
```

 **LobbyBypassType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[OnlineMeetingSettings](onlinemeetingsettings.md)
  
## <a name="text-value"></a>文本值

**LobbyBypass**元素的文本值可以是**已禁用**或**EnabledForGatewayParticipants**。 **禁用**值指示，以便通过虚拟会议厅中访问所有与会者必须禁用会议厅绕过。 **EnabledForGatewayParticipants**值指示已为电话参与者启用会议厅绕过。 
  
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  

