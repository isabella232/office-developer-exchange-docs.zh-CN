---
title: SettingName （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 8bcb0411-58b0-4e37-b97e-00c07dcbecb1
description: SettingName 元素表示响应中的设置的名称。
ms.openlocfilehash: d492b82b7385d6403f15c08356db5d0503792d54
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466722"
---
# <a name="settingname-soap"></a>SettingName （SOAP）

**SettingName**元素表示响应中的设置的名称。 
  
```XML
<SettingName/>
```

 **string**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[UserSettingError （SOAP）](usersettingerror-soap.md) <br/> |表示检索用户设置时返回的错误。  <br/> |
|[DomainSettingError （SOAP）](domainsettingerror-soap.md) <br/> |表示检索域设置时发生的错误。 这表示来自**GetDomainSettings**请求的一个错误。  <br/> |
   
## <a name="text-value"></a>文本值

**SettingName**元素的值表示响应中的设置的名称。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|架构名称  <br/> |自动发现架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   

