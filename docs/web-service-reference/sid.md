---
title: SID
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SID
api_type:
- schema
ms.assetid: 2f33b29b-163b-4106-a74d-6fb76ec38951
description: SID 元素表示用于模拟或委派访问权限的帐户的安全描述符定义语言 (SDDL) 窗体的安全标识符 (SID)。
ms.openlocfilehash: efcea42c12ec1d26ea31fdb8de337c37a2338a96
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827492"
---
# <a name="sid"></a>SID

**SID**元素表示用于模拟或委派访问权限的帐户的安全描述符定义语言 (SDDL) 窗体的安全标识符 (SID)。 
  
```xml
<SID/>
```

 **SIDType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ConnectingSID](connectingsid.md) <br/> |代表用于模拟使用 ExchangeImpersonation SOAP 标头时的帐户。  <br/> 以下是此元素的 XPath 表达式：  <br/>  `/ExchangeImpersonation/ConnectingSID` <br/> |
|[用户 Id](userid.md) <br/> |标识委派用户与文件夹访问权限。  <br/> |
   
## <a name="text-value"></a>文本值

文本值的字符串表示形式 SID。
  
## <a name="remarks"></a>备注

描述此元素的架构位于安装了客户端访问服务器角色与运行 Exchange Server 的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

