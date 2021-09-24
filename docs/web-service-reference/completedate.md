---
title: CompleteDate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CompleteDate
api_type:
- schema
ms.assetid: b2b53b87-6a0b-4a55-bcfc-3bf67d3c1700
description: CompleteDate 元素表示项目的完成日期。
ms.openlocfilehash: 07f6034b4fd91d22ad07167d931bcd02a74782f9
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518776"
---
# <a name="completedate"></a>CompleteDate

**CompleteDate** 元素表示项目的完成日期。 
  
```xml
<CompleteDate/>
```

 **DateTime**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[任务](task.md) <br/> |表示 Exchange 存储中的任务。  <br/> |
|[Flag](flag.md) <br/> |指定邮箱项目的标志。  <br/> |
   
## <a name="text-value"></a>文本值

如果此元素已使用，则代表日期和时间的文本值是必需的。
  
## <a name="remarks"></a>注解

设置 **CompleteDate** 与将 [PercentComplete](percentcomplete.md) 设置为 100 或 [将 Status](status.md) 设置为 **Completed 的效果相同**。 在至少设置其中两个属性的请求中，最后处理的属性将确定为这些元素设置的值。 例如，如果 [PercentComplete](percentcomplete.md)为 100，CompleteDate 为 2007 年 1 月 1 日 [，Status](status.md)为 **NotStarted，** 并且属性按该顺序流式传输，则效果将为将任务的 [Status](status.md)设置为 **NotStarted，**[将 CompleteDate](completedate.md)设置为 **null，** 将 [PercentComplete](percentcomplete.md)设置为 0。  
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)


[创建任务](https://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[删除任务](https://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

