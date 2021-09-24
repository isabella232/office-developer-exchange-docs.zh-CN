---
title: Account (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 488fdbdc-e9d9-4301-91ab-e22eb42e549e
description: Account 元素指定用户的帐户设置或包含错误响应。
ms.openlocfilehash: 89799ab62a2aa4945b0e8f3209ab1fbc7d2fa2e6
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59534051"
---
# <a name="account-pox"></a>Account (POX)

**Account** 元素指定用户的帐户设置或包含错误响应。 
  
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
|[AccountType (POX)](accounttype-pox.md) <br/> |表示帐户类型。  <br/> |
|[Action (POX)](action-pox.md) <br/> |提供用于确定是否需要其他自动发现请求才能返回用户配置信息的信息。  <br/> |
|[MicrosoftOnline (POX)](microsoftonline-pox.md) <br/> |包含一个值，该值指示用户的邮箱是托管在 Exchange Online 中Exchange Online还是Office 365。  <br/> |
|[RedirectUrl (POX)](redirecturl-pox.md) <br/> |包含运行已安装客户端访问Exchange Server角色的计算机的 URL，该 URL 应该用于获取自动发现设置。  <br/> |
|[RedirectAddr (POX)](redirectaddr-pox.md) <br/> |指定应用于后续自动发现请求的电子邮件地址。  <br/> |
|[Image (POX)](image-pox.md) <br/> |包含用于打造配置体验品牌的图像的路径。  <br/> |
|[ServiceHome (POX)](servicehome-pox.md) <br/> |包含 INTERNET 服务提供商的主页的 URL (ISP) 。  <br/> |
|[Protocol (POX)](protocol-pox.md) <br/> |包含用于将客户端连接到客户端访问服务器的规范。  <br/> |
|[PublicFolderInformation (POX)](publicfolderinformation-pox.md) <br/> |包含客户端可用于发送自动发现请求以发现用户的公用文件夹信息的信息。  <br/> |
|[Error (POX)](error-pox.md) <br/> |包含自动发现错误响应。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Response (POX)](response-pox.md) <br/> |包含来自自动发现服务的响应。  <br/> |
   
## <a name="see-also"></a>另请参阅

- [用于存储的 POX 自动发现 XML Exchange](pox-autodiscover-xml-elements-for-exchange.md)

