---
title: UserConfigurationName
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- UserConfigurationName
api_type:
- schema
ms.assetid: 6947dd03-9727-4379-9b9d-42373fa120c7
description: UserConfigurationName 元素表示用户配置对象的名称。 用户配置对象名称是用户配置对象的标识符。
ms.openlocfilehash: 7563435f25a5307aa908a64baceffb3c81138149
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517383"
---
# <a name="userconfigurationname"></a>UserConfigurationName

**UserConfigurationName** 元素表示用户配置对象的名称。 用户配置对象名称是用户配置对象的标识符。 
  
```XML
<UserConfigurationName Name="">
   <FolderId/>
</UserConfigurationName>
```

```XML
<UserConfigurationName Name="">
   <DistinguishedFolderId/> 
</UserConfigurationName>
```

**UserConfigurationNameType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**名称** <br/> |包含一个字符串值，它代表用户配置对象的名称。 此特性是必需的。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |表示包含用户配置对象的文件夹的文件夹标识符。  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |表示包含用户配置对象的文件夹的可分辨文件夹名称。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[DeleteUserConfiguration](deleteuserconfiguration.md) <br/> |表示删除用户配置对象的请求。  <br/> |
|[GetUserConfiguration](getuserconfiguration.md) <br/> |表示获取用户配置对象的请求。  <br/> |
|[UserConfiguration](userconfiguration.md) <br/> |定义单个用户配置对象。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>注解

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

