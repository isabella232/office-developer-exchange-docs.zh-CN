---
title: RetentionPolicyType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: abce5b3e-971d-42fc-aeea-caa7202214de
description: RetentionPolicyType 元素指定应用于对话中的项目的保留策略类型。
ms.openlocfilehash: 961f72c35443e9f265e9313166fa77c8cd93d654
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59509383"
---
# <a name="retentionpolicytype"></a>RetentionPolicyType

**RetentionPolicyType** 元素指定应用于对话中的项目的保留策略类型。 
  
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

**RetentionPolicyType 元素** 的文本值是应用于对话中的项目的保留类型。 Delete **的文本值指示** 在保留保留到期时删除对话中的项目。 Archive **的文本值指示** 保留保留到期时，对话中的项目将移动到存档邮箱。 
  
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> ||
   

