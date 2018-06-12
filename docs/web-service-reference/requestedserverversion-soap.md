---
title: RequestedServerVersion (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: cf3f9d7a-2add-4457-b009-2929220f90b5
description: RequestedServerVersion元素指定一个Autodiscover 方法调用的目标的服务器版本。
ms.openlocfilehash: 6b9d31f3b7bca087652f04e4943becc5ac4e68e7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827132"
---
# <a name="requestedserverversion-soap"></a>RequestedServerVersion (SOAP)

本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **RequestedServerVersion**元素指定一个 **Autodiscover** 方法调用的目标的服务器版本。 
  
```XML
<RequestedServerVersion/>
```

 **ExchangeVersion**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

无。
  
## <a name="text-value"></a>文本值

**RequestedServerVersion**元素的文本值指定一个 **Autodiscover** 方法调用的目标的服务器版本。下表列出了有效的服务器版本。 
  
|**文本值**|**说明**|
|:-----|:-----|
|Exchange2007_SP1  <br/> |Exchange Server 2007 Service Pack 1 (SP1)。  <br/> |
|Exchange2010  <br/> |Exchange Server 2010  <br/> |
|Exchange2010_SP1  <br/> |Exchange Server 2010 Service Pack 1 (SP1)。  <br/> |
|Exchange2010_SP2  <br/> |Exchange Server 2010 Service Pack 2 (SP2)。  <br/> |
|Exchange2013  <br/> |Exchange Server 2013年。Exchange2013 字段是适用于目标 Exchange 联机和使用 Exchange Server 2013年启动 Exchange 版本的客户端。  <br/> |
|Exchange2013_SP1  <br/> |Exchange Server 2013 Service Pack 1 (SP1)。Exchange2013_SP1 字段是适用于目标 Exchange 联机和开始使用 Exchange Server 2013 SP1 的 Exchange 的版本的客户端。  <br/> |
   
## <a name="remarks"></a>备注

在 SOAP 标头中设置了 **RequestedServerVersion**元素。 
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|架构名称  <br/> |自动发现架构  <br/> |
|验证文件  <br/> |messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   

