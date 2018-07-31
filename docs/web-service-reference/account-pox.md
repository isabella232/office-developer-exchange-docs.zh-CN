---
title: Account (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 488fdbdc-e9d9-4301-91ab-e22eb42e549e
description: 帐户元素指定的用户帐户设置，或包含错误响应。
ms.openlocfilehash: 6cd87e678b3a524a69f6dca4d6999a3cff22fa57
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353341"
---
# <a name="account-pox"></a>Account (POX)

**帐户**元素指定的用户帐户设置，或包含错误响应。 
  
- [AutoDiscover (POX)](autodiscover-pox.md)
- [Response (POX)](response-pox.md)
- [Account (POX)](account-pox.md)
  
```XML
<Account>
   <AccountType/>
   <Action/>
   <MicrosoftOnline/>
   <RedirectURL/>
   <RedirectAddr/>
   <Image/>
   <ServiceHome/>
   <Protocol/>
   <PublicFolderInformation/>
</Account>
```

<br/>

```XML
<Account> 
    <Error/> 
</Account>
```

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[AccountType (POX)](accounttype-pox.md) <br/> |表示的帐户类型。  <br/> |
|[Action (POX)](action-pox.md) <br/> |提供用于确定是否需要返回用户配置信息的另一个自动发现请求的信息。  <br/> |
|[MicrosoftOnline (POX)](microsoftonline-pox.md) <br/> |包含一个值，指示是否在用户邮箱位于 Exchange Online 或 Exchange Online 作为 Office 365 的一部分。  <br/> |
|[RedirectUrl (POX)](redirecturl-pox.md) <br/> |包含正在运行了客户端访问服务器角色安装的用于获取自动发现设置的 Exchange Server 的计算机的 URL。  <br/> |
|[RedirectAddr (POX)](redirectaddr-pox.md) <br/> |指定应用于后续的自动发现请求的电子邮件地址。  <br/> |
|[Image (POX)](image-pox.md) <br/> |包含用于打造品牌的配置体验的图像的路径。  <br/> |
|[ServiceHome (POX)](servicehome-pox.md) <br/> |包含主页上的 Internet 服务提供商 (ISP) 的 URL。  <br/> |
|[Protocol (POX)](protocol-pox.md) <br/> |包含客户端连接到客户端访问服务器的规范。  <br/> |
|[PublicFolderInformation (POX)](publicfolderinformation-pox.md) <br/> |包含客户端可以使用发送发现用户的公用文件夹信息的自动发现请求的信息。  <br/> |
|[Error (POX)](error-pox.md) <br/> |包含自动发现错误响应。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Response (POX)](response-pox.md) <br/> |包含来自自动发现服务的响应。  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

