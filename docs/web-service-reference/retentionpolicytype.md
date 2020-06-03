---
title: RetentionPolicyType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: abce5b3e-971d-42fc-aeea-caa7202214de
description: RetentionPolicyType 元素指定应用于会话中的项目的保留策略类型。
ms.openlocfilehash: 3900718f10e1e11d5864ebf7e64a3e1e22aa45c7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462869"
---
# <a name="retentionpolicytype"></a>RetentionPolicyType

**RetentionPolicyType**元素指定应用于会话中的项目的保留策略类型。 
  
```XML
<RetentionPolicyType> Delete | Archive </RetentionPolicyType>
```

 **RetentionType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[ConversationAction](conversationaction.md)
  
## <a name="text-value"></a>文本值

**RetentionPolicyType**元素的文本值是应用于会话中的项目的保留类型。 "**删除**" 的文本值表示当保留挂起过期时，会话中的项目将被删除。 **存档**的文本值表示在保留挂起过期时，会话中的项目将移动到存档邮箱中。 
  
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> ||
   

