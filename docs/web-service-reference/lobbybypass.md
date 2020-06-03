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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458094"
---
# <a name="lobbybypass"></a><span data-ttu-id="80deb-103">LobbyBypass</span><span class="sxs-lookup"><span data-stu-id="80deb-103">LobbyBypass</span></span>

<span data-ttu-id="80deb-104">**LobbyBypass**元素指定 "联机会议" 设置以绕过虚拟大厅。</span><span class="sxs-lookup"><span data-stu-id="80deb-104">The **LobbyBypass** element specifies the online meeting setting to bypass the virtual lobby.</span></span> 
  
```XML
<LobbyBypass> Disabled | EnabledForGatewayParticipants </LobbyBypass>
```

 <span data-ttu-id="80deb-105">**LobbyBypassType**</span><span class="sxs-lookup"><span data-stu-id="80deb-105">**LobbyBypassType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="80deb-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="80deb-106">Attributes and elements</span></span>

<span data-ttu-id="80deb-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="80deb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="80deb-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="80deb-108">Attributes</span></span>

<span data-ttu-id="80deb-109">无。</span><span class="sxs-lookup"><span data-stu-id="80deb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="80deb-110">子元素</span><span class="sxs-lookup"><span data-stu-id="80deb-110">Child elements</span></span>

<span data-ttu-id="80deb-111">无。</span><span class="sxs-lookup"><span data-stu-id="80deb-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="80deb-112">父元素</span><span class="sxs-lookup"><span data-stu-id="80deb-112">Parent elements</span></span>

[<span data-ttu-id="80deb-113">OnlineMeetingSettings</span><span class="sxs-lookup"><span data-stu-id="80deb-113">OnlineMeetingSettings</span></span>](onlinemeetingsettings.md)
  
## <a name="text-value"></a><span data-ttu-id="80deb-114">文本值</span><span class="sxs-lookup"><span data-stu-id="80deb-114">Text value</span></span>

<span data-ttu-id="80deb-115">**LobbyBypass**元素的文本值可以是**Disabled**或**EnabledForGatewayParticipants**。</span><span class="sxs-lookup"><span data-stu-id="80deb-115">The text value of the **LobbyBypass** element can be either **Disabled** or **EnabledForGatewayParticipants**.</span></span> <span data-ttu-id="80deb-116">**禁用**的值指示已禁用会议厅旁路，以便所有与会者都必须通过虚拟大厅访问。</span><span class="sxs-lookup"><span data-stu-id="80deb-116">The **Disabled** value indicates that the lobby bypass is disabled so all meeting attendees must access through the virtual lobby.</span></span> <span data-ttu-id="80deb-117">**EnabledForGatewayParticipants**值指示已为电话参与者启用会议厅旁路。</span><span class="sxs-lookup"><span data-stu-id="80deb-117">The **EnabledForGatewayParticipants** value indicates that the lobby bypass is enabled for telephone participants.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="80deb-118">备注</span><span class="sxs-lookup"><span data-stu-id="80deb-118">Remarks</span></span>

<span data-ttu-id="80deb-119">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="80deb-119">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="80deb-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="80deb-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  

