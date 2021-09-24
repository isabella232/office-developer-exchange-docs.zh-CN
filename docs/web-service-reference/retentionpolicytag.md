---
title: RetentionPolicyTag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f46679d0-9236-41e2-8624-72300079c67c
description: RetentionPolicyTag 元素指定邮箱项目的保留策略。
ms.openlocfilehash: 58ca3016bed0be625b213a57e5ead1b38a301bfa
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524544"
---
# <a name="retentionpolicytag"></a>RetentionPolicyTag

**RetentionPolicyTag** 元素指定邮箱项目的保留策略。 
  
```XML
<RetentionPolicyTag>
   <DisplayName/>
   <RetentionId/>
   <RetentionPeriod/>
   <Type/>
   <RetentionAction/>
   <Description/>
   <IsVisible/>
   <OptedInto/>
   <IsArchive/>
</RetentionPolicyTag>
```

 **RetentionPolicyTagType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

[DisplayName (字符串) ](displayname-string.md)  | [RetentionId](retentionid.md)  | [RetentionPeriod](retentionperiod.md)  | [键入 (ElcFolderType) ](type-elcfoldertype.md)  | [RetentionAction](retentionaction.md)  | [说明](description.md)  | [IsVisible](isvisible.md)  | [OptedInto](optedinto.md)  | [IsArchive](isarchive.md)
  
### <a name="parent-elements"></a>父元素

[RetentionPolicyTags](retentionpolicytags.md)
  
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
   

