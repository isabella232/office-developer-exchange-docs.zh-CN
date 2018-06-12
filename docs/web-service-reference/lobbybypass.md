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
# <a name="lobbybypass"></a><span data-ttu-id="c6671-103">LobbyBypass</span><span class="sxs-lookup"><span data-stu-id="c6671-103">LobbyBypass</span></span>

<span data-ttu-id="c6671-104">**LobbyBypass**元素指定的设置以绕过虚拟会议厅的联机会议。</span><span class="sxs-lookup"><span data-stu-id="c6671-104">The **LobbyBypass** element specifies the online meeting setting to bypass the virtual lobby.</span></span> 
  
```XML
<LobbyBypass> Disabled | EnabledForGatewayParticipants </LobbyBypass>
```

 <span data-ttu-id="c6671-105">**LobbyBypassType**</span><span class="sxs-lookup"><span data-stu-id="c6671-105">**LobbyBypassType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c6671-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c6671-106">Attributes and elements</span></span>

<span data-ttu-id="c6671-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c6671-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c6671-108">属性</span><span class="sxs-lookup"><span data-stu-id="c6671-108">Attributes</span></span>

<span data-ttu-id="c6671-109">无。</span><span class="sxs-lookup"><span data-stu-id="c6671-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c6671-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c6671-110">Child elements</span></span>

<span data-ttu-id="c6671-111">无。</span><span class="sxs-lookup"><span data-stu-id="c6671-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c6671-112">父元素</span><span class="sxs-lookup"><span data-stu-id="c6671-112">Parent elements</span></span>

[<span data-ttu-id="c6671-113">OnlineMeetingSettings</span><span class="sxs-lookup"><span data-stu-id="c6671-113">OnlineMeetingSettings</span></span>](onlinemeetingsettings.md)
  
## <a name="text-value"></a><span data-ttu-id="c6671-114">文本值</span><span class="sxs-lookup"><span data-stu-id="c6671-114">Text value</span></span>

<span data-ttu-id="c6671-115">**LobbyBypass**元素的文本值可以是**已禁用**或**EnabledForGatewayParticipants**。</span><span class="sxs-lookup"><span data-stu-id="c6671-115">The text value of the **LobbyBypass** element can be either **Disabled** or **EnabledForGatewayParticipants**.</span></span> <span data-ttu-id="c6671-116">**禁用**值指示，以便通过虚拟会议厅中访问所有与会者必须禁用会议厅绕过。</span><span class="sxs-lookup"><span data-stu-id="c6671-116">The **Disabled** value indicates that the lobby bypass is disabled so all meeting attendees must access through the virtual lobby.</span></span> <span data-ttu-id="c6671-117">**EnabledForGatewayParticipants**值指示已为电话参与者启用会议厅绕过。</span><span class="sxs-lookup"><span data-stu-id="c6671-117">The **EnabledForGatewayParticipants** value indicates that the lobby bypass is enabled for telephone participants.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c6671-118">备注</span><span class="sxs-lookup"><span data-stu-id="c6671-118">Remarks</span></span>

<span data-ttu-id="c6671-119">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="c6671-119">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c6671-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c6671-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  

