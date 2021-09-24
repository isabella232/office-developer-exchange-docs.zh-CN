---
title: Exchange 2013 的 SOAP 自动发现 XML 元素
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: ae18a5b3-ae44-4cff-8654-db8028565e01
description: 查找 SOAP 自动发现 Web 服务的 XML 元素参考信息Exchange。
ms.openlocfilehash: 5dcf4d6cd7a2b0b2987e59530dfbaae7b9993242
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59539092"
---
# <a name="soap-autodiscover-xml-elements-for-exchange-2013"></a>Exchange 2013 的 SOAP 自动发现 XML 元素

查找 SOAP 自动发现 Web 服务的 XML 元素参考信息Exchange。
  
本节中的文档基于在客户端和服务器之间发送的 SOAP Autodiscover XML 元素实例。 此 XML 实例文档基于位于承载 SOAP 自动发现服务的虚拟目录中的 WSDL 和架构文件。 经过身份验证的用户可以使用与以下 URL 类似的 URL 浏览到 WSDL 和架构文件：
  
- WSDL 文件的位置： `http://<yourclientaccessserver>.com/autodiscover/services.wsdl` 或 `http://autodiscover.<yourclientaccessserver>.com/autodiscover/services.wsdl`
    
- 邮件架构的位置： `http://<yourclientaccessserver>.com/autodiscover/messages.xsd` 或 `http://autodiscover.<yourclientaccessserver>.com/autodiscover/messages.xsd` 
    
SOAP 自动发现 WSDL 和架构文件的位置因安装Exchange而异。
  
messages.xsd 架构文件介绍可在自动发现 SOAP 标头和 SOAP 正文中发送的 XML 元素。 此文件提供 XML 结构可用于给定请求-响应消息交互的一般路线图。 在客户端和服务器之间发送的实际 XML 结构基于选项及其使用上下文。 架构文件定义可能的 XML。 通过线路发送的实际 XML 范围基于调用的操作、请求的信息和服务器端设置。 
  
## <a name="related-sections"></a>相关章节

- [SOAP 自动发现 Web 服务参考Exchange](soap-autodiscover-web-service-reference-for-exchange.md)    
- [Exchange 的 EWS 引用](ews-reference-for-exchange.md)    
- [统一消息 Web 服务参考Exchange](unified-messaging-web-service-reference-for-exchange.md)
    
## <a name="see-also"></a>另请参阅

- [自动发现 Web 服务引用Exchange](autodiscover-web-service-reference-for-exchange.md)
- [Exchange 自动发现](../exchange-web-services/autodiscover-for-exchange.md)
- [开始使用 Exchange 中的 Web 服务](../exchange-web-services/start-using-web-services-in-exchange.md)
    

