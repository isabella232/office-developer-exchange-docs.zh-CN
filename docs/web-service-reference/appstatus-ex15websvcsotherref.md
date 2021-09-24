---
title: AppStatus
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f3ab8bf1-abc5-45cf-a2e1-d7602f2c24ec
description: AppStatus 元素值指示邮件应用程序的状态。
ms.openlocfilehash: 69f481b197db513761b97d4fbba38452bbb4a9a1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59525314"
---
# <a name="appstatus"></a>AppStatus

**AppStatus** 元素值指示邮件应用程序的状态。 
  
```XML
<AppStatus/>
```

 **string**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[元数据](metadata-ex15websvcsotherref.md)
  
## <a name="text-value"></a>文本值

**AppStatus 元素** 的文本值指示邮件应用程序的状态。 如果用户可以修复与邮件应用程序状态相关的问题， [则 ActionUrl](actionurl.md) 元素将提供用于执行修复的 URL。 
  
**表 1.AppStatus 值**

|**值**|**说明**|
|:-----|:-----|
|Null 或 0  <br/> |邮件应用程序状态正常。  <br/> |
|1.0  <br/> |邮件应用程序无法自动更新。 需要从应用商店中重新安装Office应用程序。  <br/> |
|1.1  <br/> |邮件应用程序无法自动更新。 邮件应用程序需要增加权限，这要求您进行审阅和确认才能安装。  <br/> |
|1.2  <br/> |邮件应用程序无法自动更新。 当前许可证已过期或无效。 请从应用商店更新Office应用程序。  <br/> |
|2.0  <br/> |无法自动更新邮件应用程序许可证。 需要从邮件应用商店恢复邮件Office许可证。  <br/> |
|2.1  <br/> |无法自动更新邮件应用程序许可证。 当前许可证已过期。 需要从应用商店安装此应用的新Office许可证。  <br/> |
|3.0  <br/> |邮件Office的"应用商店"状态已更改。 这可能表示邮件应用程序存在问题。 有关详细信息，请转到 Office 应用商店中的邮件应用程序页面。  <br/> |
|3.1  <br/> |邮件应用程序已从应用商店Office中删除。  <br/> |
|3.2  <br/> |发现邮件应用程序存在问题，已从应用商店临时Office问题。  <br/> |
|3.3  <br/> |邮件应用程序将在 30 天内从 Office 应用商店中删除。  <br/> |
|4.0  <br/> |邮件客户端已自动禁用邮件应用程序。  <br/> |
|4.1  <br/> |由于性能原因，邮件Outlook已禁用。  <br/> |
   
## <a name="remarks"></a>说明

Exchange Server 2013 Service Pack 1 (SP1) 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> | https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |不适用  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [元数据](metadata-ex15websvcsotherref.md)
- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

