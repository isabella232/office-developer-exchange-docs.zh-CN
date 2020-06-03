---
title: ResponseMessages (ArrayOfDelegateUserResponseMessageType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResponseMessages
api_type:
- schema
ms.assetid: 14819975-ce54-4f0e-9f90-d4b275895ea0
description: ResponseMessages 元素包含 Exchange Web 服务委派管理请求的响应消息。
ms.openlocfilehash: 6b035f4ee46af1750a275e2c61b2cddea06b37a1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465455"
---
# <a name="responsemessages-arrayofdelegateuserresponsemessagetype"></a>ResponseMessages (ArrayOfDelegateUserResponseMessageType)

**ResponseMessages**元素包含 Exchange Web 服务委派管理请求的响应消息。 
  
```
<ResponseMessages>
   <DelegateUserResponseMessageType/>
</ResponseMessages>
```

 **ArrayOfDelegateUserResponseMessageType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[DelegateUserResponseMessageType](delegateuserresponsemessagetype.md) <br/> |包含用于委派管理操作的响应消息。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[AddDelegateResponse](adddelegateresponse.md) <br/> |包含[AddDelegate 操作](adddelegate-operation.md)请求的状态和结果。  <br/> |
|[GetDelegateResponse](getdelegateresponse.md) <br/> |包含[GetDelegate 操作](getdelegate-operation.md)请求的状态和结果。  <br/> |
|[UpdateDelegateResponse](updatedelegateresponse.md) <br/> |包含[UpdateDelegate 操作](updatedelegate-operation.md)请求的状态和结果。  <br/> |
|[RemoveDelegateResponse](removedelegateresponse.md) <br/> |包含[RemoveDelegate 操作](removedelegate-operation.md)请求的状态和结果。  <br/> |
   
## <a name="remarks"></a>备注

此元素在[AddDelegate 操作](adddelegate-operation.md)、 [GetDelegate 操作](getdelegate-operation.md)、 [UpdateDelegate 操作](updatedelegate-operation.md)和[RemoveDelegate 操作](removedelegate-operation.md)中使用。 委派管理操作响应的结构不同于其他响应。 委托管理响应消息是强类型的。
  
描述此元素的架构位于运行 Exchange Server 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[AddDelegate 操作](adddelegate-operation.md)
  
[GetDelegate 操作](getdelegate-operation.md)
  
[UpdateDelegate 操作](updatedelegate-operation.md)
  
[RemoveDelegate 操作](removedelegate-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

