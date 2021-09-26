---
title: ExpandDL
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ExpandDL
api_type:
- schema
ms.assetid: affe84a5-ad98-4aba-83f4-8732938b763d
description: ExpandDL 元素定义展开通讯组列表的请求。
ms.openlocfilehash: 53c713ac21204be3d49e909bebd0bc8927856476
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59545158"
---
# <a name="expanddl"></a>ExpandDL

**ExpandDL** 元素定义展开通讯组列表的请求。 
  
```xml
<ExpandDL>
   <Mailbox/>
</ExpandDL>
```

 **ExpandDLType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Mailbox](mailbox.md) <br/> |标识完全解析的电子邮件地址或通讯组列表。 此邮箱表示要展开的通讯组列表。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>注解

通讯组列表扩展将仅对单个通讯组列表执行。 通讯组列表扩展不是递归的。
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[ExpandDL 操作](expanddl-operation.md)

