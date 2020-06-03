---
title: MarkAllItemsAsRead
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 22244afb-99ec-41b4-8f73-3fbccd56d1ab
description: MarkAllItemsAsRead 元素包含将文件夹中的所有项目标记为已读的请求。
ms.openlocfilehash: 0338b2a1eed503b7e8fb0ec8b4a8ebcf12b6dbd6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530886"
---
# <a name="markallitemsasread"></a>MarkAllItemsAsRead

**MarkAllItemsAsRead**元素包含将文件夹中的所有项目标记为已读的请求。 
  
```XML
<MarkAllItemsAsRead>
   <ReadFlag/>
   <SuppressReadReceipts/>
   <FolderIds/>
</MarkAllItemsAsRead>
```

 **MarkAllItemsAsReadType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

[ReadFlag](readflag.md)  | [SuppressReadReceipts](suppressreadreceipts.md)  | [FolderIds](folderids.md)
  
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>说明

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> ||
   

