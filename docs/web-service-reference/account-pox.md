---
title: 帐户（POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 488fdbdc-e9d9-4301-91ab-e22eb42e549e
description: Account 元素指定用户的帐户设置或包含错误响应。
ms.openlocfilehash: ffd8ebe4b7bd9d4b3f6a9b42fc557ac6189a068d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462316"
---
# <a name="account-pox"></a>帐户（POX）

**Account**元素指定用户的帐户设置或包含错误响应。 
  
- [自动发现（POX）](autodiscover-pox.md)
- [响应（POX）](response-pox.md)
- [帐户（POX）](account-pox.md)
  
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
|[AccountType （POX）](accounttype-pox.md) <br/> |代表帐户类型。  <br/> |
|[Action （POX）](action-pox.md) <br/> |提供用于确定是否需要其他自动发现请求来返回用户配置信息的信息。  <br/> |
|[MicrosoftOnline （POX）](microsoftonline-pox.md) <br/> |包含一个值，该值指示用户的邮箱是托管在 Exchange Online 中还是 Exchange Online 中作为 Office 365 的一部分承载。  <br/> |
|[RedirectUrl （POX）](redirecturl-pox.md) <br/> |包含运行 Exchange Server 且安装了应用于获取自动发现设置的客户端访问服务器角色的计算机的 URL。  <br/> |
|[RedirectAddr （POX）](redirectaddr-pox.md) <br/> |指定应用于后续自动发现请求的电子邮件地址。  <br/> |
|[Image （POX）](image-pox.md) <br/> |包含用于标记配置体验的图像的路径。  <br/> |
|[ServiceHome （POX）](servicehome-pox.md) <br/> |包含 Internet 服务提供商（ISP）主页的 URL。  <br/> |
|[协议（POX）](protocol-pox.md) <br/> |包含用于将客户端连接到客户端访问服务器的规范。  <br/> |
|[PublicFolderInformation （POX）](publicfolderinformation-pox.md) <br/> |包含客户端可用于发送自动发现请求以发现用户公用文件夹信息的信息。  <br/> |
|[错误（POX）](error-pox.md) <br/> |包含自动发现错误响应。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[响应（POX）](response-pox.md) <br/> |包含来自自动发现服务的响应。  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 的 POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

