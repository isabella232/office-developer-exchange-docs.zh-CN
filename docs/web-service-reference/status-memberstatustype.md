---
title: Status (MemberStatusType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Status
api_type:
- schema
ms.assetid: 4f8a860b-0a48-4a0d-9a7a-69a0304aa747
description: Status 元素提供有关服务器上通讯组列表成员的状态的信息。
ms.openlocfilehash: 0142ac1fa88c4cc4e513f23bbfad2869e7df32e7
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544596"
---
# <a name="status-memberstatustype"></a>Status (MemberStatusType)

**Status** 元素提供有关服务器上通讯组列表成员的状态的信息。 
  
```
<Status>Unrecognized or Normal or Demoted</Status>
```

 **MemberStatusType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Member](member-ex15websvcsotherref.md) <br/> |表示一个通讯组列表的成员。  <br/> |
   
## <a name="text-value"></a>文本值

下表列出了 **Status** 元素的可能值。 
  
**Status 元素值**

|**值**|**说明**|
|:-----|:-----|
|无法识别  <br/> |成员信息无效或无法识别。  <br/> |
|一般  <br/> |通讯组列表中的成员信息与引用的对象同步。  <br/> |
|降级  <br/> |引用的对象不可用。  <br/> |
   
## <a name="remarks"></a>注解

描述此元素的架构位于运行已安装客户端访问服务器角色Microsoft Exchange Server的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

