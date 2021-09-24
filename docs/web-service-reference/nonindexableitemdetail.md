---
title: NonIndexableItemDetail
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: a26d4c02-f1bd-40c4-9257-5db45e839f17
description: NonIndexableItemDetail 元素指定有关无法编制索引的项目的详细信息。
ms.openlocfilehash: 2c3dae9276bee4800352c74acca37fe85ddbf223
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515437"
---
# <a name="nonindexableitemdetail"></a>NonIndexableItemDetail

**NonIndexableItemDetail** 元素指定有关无法编制索引的项目的详细信息。 
  
```XML
<NonIndexableItemDetail>
   <ItemId/>
   <ErrorCode/>
   <ErrorDescription/>
   <IsPartiallyIndexed/>
   <IsPermanentFailure/>
   <SortValue/>
   <AttemptCount/>
   <LastAttemptTime/>
   <AdditionalInfo/>
</NonIndexableItemDetail>
```

 **NonIndexableItemDetailType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

[ItemId](itemid.md)  | [ErrorCode (ItemIndexErrorType) ](errorcode-itemindexerrortype.md)  | [ErrorDescription](errordescription.md)  | [IsPartiallyIndexed](ispartiallyindexed.md)  | [IsPermanentFailure](ispermanentfailure.md)  | [SortValue](sortvalue.md)  | [AttemptCount](attemptcount.md)  | [LastAttemptTime](lastattempttime.md)  | [AdditionalInfo](additionalinfo.md)
  
### <a name="parent-elements"></a>父元素

[Items (ArrayOfNonIndexableItemDetailsType)](items-arrayofnonindexableitemdetailstype.md)
  
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
   

