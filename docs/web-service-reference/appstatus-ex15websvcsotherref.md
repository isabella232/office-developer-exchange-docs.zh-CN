---
title: AppStatus
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f3ab8bf1-abc5-45cf-a2e1-d7602f2c24ec
description: AppStatus 元素的值指示邮件应用程序的状态。
ms.openlocfilehash: cf213fc3d7be02c411e9c2e83a4ff153dbefe098
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753253"
---
# <a name="appstatus"></a>AppStatus

**AppStatus**元素的值指示邮件应用程序的状态。 
  
```XML
<AppStatus/>
```

 **string**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[元数据](metadata-ex15websvcsotherref.md)
  
## <a name="text-value"></a>文本值

**AppStatus**元素的文本值指示邮件应用程序的状态。 如果用户可以解决的邮件应用程序状态的问题， [ActionUrl](actionurl.md)元素提供了执行该修补程序的 URL。 
  
**表 1。AppStatus 值**

|**值**|**说明**|
|:-----|:-----|
|Null 或 0  <br/> |邮件应用程序具有正常运行状态。  <br/> |
|1.0  <br/> |邮件应用程序可能不会自动更新。 邮件应用程序需要能够从 Office 商店重新安装。  <br/> |
|1.1  <br/> |邮件应用程序可能不会自动更新。 邮件应用程序需要增加的权限，并且这需要您查看和确认安装。  <br/> |
|1.2  <br/> |邮件应用程序无法自动更新。 当前许可证已到期或无效。 请更新 Office 商店中的邮件应用程序。  <br/> |
|2.0  <br/> |无法自动更新的邮件应用程序许可证。 邮件应用程序许可证需要从 Office 商店中恢复。  <br/> |
|2.1  <br/> |无法自动更新的邮件应用程序许可证。 当前许可证已到期。 新的许可此应用程序需要从 Office 商店安装。  <br/> |
|3.0  <br/> |邮件应用程序的 Office 应用商店状态已更改。 这可能表示存在问题的邮件应用程序。 转到 Office 商店的详细信息中的邮件应用程序页。  <br/> |
|3.1  <br/> |从 Office 商店中已被删除的邮件应用程序。  <br/> |
|3.2  <br/> |使用邮件应用程序已发现的问题和它已经暂时已选撤消从 Office 商店。  <br/> |
|3.3  <br/> |将删除从 Office 商店 30 天内的邮件应用程序。  <br/> |
|4.0  <br/> |您的邮件客户端已被自动禁用邮件应用程序。  <br/> |
|4.1  <br/> |出于性能原因的 Outlook 邮件应用程序已禁用。  <br/> |
   
## <a name="remarks"></a>备注

Exchange Server 2013 Service Pack 1 (SP1) 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> | http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |不适用  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [元数据](metadata-ex15websvcsotherref.md)
- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

