---
title: UserConfigurationName
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UserConfigurationName
api_type:
- schema
ms.assetid: 6947dd03-9727-4379-9b9d-42373fa120c7
description: UserConfigurationName 元素表示用户配置对象的名称。 "用户配置" 对象名称是 "用户配置" 对象的标识符。
ms.openlocfilehash: 020b55919f7f81602a5eb072652d82168607d306
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466029"
---
# <a name="userconfigurationname"></a>UserConfigurationName

**UserConfigurationName**元素表示用户配置对象的名称。 "用户配置" 对象名称是 "用户配置" 对象的标识符。 
  
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
|**名称** <br/> |包含一个 string 值，它代表用户配置对象的名称。 此特性是必需的。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |表示包含用户配置对象的文件夹的文件夹标识符。  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |表示包含用户配置对象的文件夹的可分辨文件夹名称。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[DeleteUserConfiguration](deleteuserconfiguration.md) <br/> |表示一个删除用户配置对象的请求。  <br/> |
|[GetUserConfiguration](getuserconfiguration.md) <br/> |表示获取用户配置对象的请求。  <br/> |
|[UserConfiguration](userconfiguration.md) <br/> |定义单个用户配置对象。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>说明

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

