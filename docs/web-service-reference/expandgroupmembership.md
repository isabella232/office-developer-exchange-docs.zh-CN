---
title: ExpandGroupMembership
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8989e96b-8fa1-4858-93b2-2cbdb30b9ca9
description: ExpandGroupMembership 元素指示是否展开 GetSearchableMailboxes 请求返回的组的成员身份。
ms.openlocfilehash: 8a94aa3da165ecc13282127e75c8d166f3972ead
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456904"
---
# <a name="expandgroupmembership"></a>ExpandGroupMembership

**ExpandGroupMembership**元素指示是否展开**GetSearchableMailboxes**请求返回的组的成员身份。 
  
```XML
<ExpandGroupMembership>true | false</ExpandGroupMembership>
```

 **Boolean**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[GetDiscoverySearchConfiguration](getdiscoverysearchconfiguration.md)  | [GetSearchableMailboxes](getsearchablemailboxes.md)
  
## <a name="text-value"></a>文本值

如果**ExpandGroupElement**元素的文本值为**true** ，则表明组成员身份已展开。 **如果值为 false** ，则表示不展开组成员身份以显示组的成员。 
  
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |消息 .xsd  <br/> |
|可以为空  <br/> |false  <br/> |
   

