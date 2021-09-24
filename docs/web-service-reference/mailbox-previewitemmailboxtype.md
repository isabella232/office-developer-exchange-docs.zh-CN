---
title: Mailbox (PreviewItemMailboxType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: e898d737-b6e4-4403-9c2c-aec52a48a83d
description: Mailbox 元素包含邮箱标识符和用户的主简单邮件传输协议 (SMTP) 地址。
ms.openlocfilehash: 1a2dcc08d3e1595aede21e6982b36a60e6efafb5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59514296"
---
# <a name="mailbox-previewitemmailboxtype"></a>Mailbox (PreviewItemMailboxType)

Mailbox 元素包含邮箱标识符和用户的主简单邮件传输协议 (SMTP) 地址。 
  
```XML
<Mailbox>
   <MailboxId/>
   <PrimarySmtpAddress/>
</Mailbox>
```

**PreviewItemMailboxType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

[MailboxId](mailboxid.md)  | [PrimarySmtpAddress (字符串) ](primarysmtpaddress-string.md)
  
### <a name="parent-elements"></a>父元素

[SearchPreviewItem](searchpreviewitem.md)
  
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |false  <br/> |
   

