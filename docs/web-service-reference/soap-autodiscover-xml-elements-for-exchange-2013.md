---
title: Exchange 2013 的 SOAP 自动发现 XML 元素
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: ae18a5b3-ae44-4cff-8654-db8028565e01
description: 在 Exchange 中查找 SOAP 自动发现 web 服务的 XML 元素引用信息。
ms.openlocfilehash: 3b88429488dbecd4ed7c3adf56462f34fa0d4b17
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465182"
---
# <a name="soap-autodiscover-xml-elements-for-exchange-2013"></a>Exchange 2013 的 SOAP 自动发现 XML 元素

在 Exchange 中查找 SOAP 自动发现 web 服务的 XML 元素引用信息。
  
本节中的文档基于在客户端和服务器之间发送的 SOAP 自动发现 XML 元素实例。 此 XML 实例文档基于承载 SOAP 自动发现服务的虚拟目录中的 WSDL 和架构文件。 经过身份验证的用户可以使用类似于以下内容之一的 URL 来浏览 WSDL 和 schema 文件：
  
- WSDL 文件的位置： `http://<yourclientaccessserver>.com/autodiscover/services.wsdl` 或`http://autodiscover.<yourclientaccessserver>.com/autodiscover/services.wsdl`
    
- 邮件架构的位置： `http://<yourclientaccessserver>.com/autodiscover/messages.xsd` 或`http://autodiscover.<yourclientaccessserver>.com/autodiscover/messages.xsd` 
    
SOAP 自动发现 WSDL 和架构文件的位置根据 Exchange 安装的不同而有所不同。
  
消息 .xsd 架构文件描述可在自动发现 SOAP 标头和 SOAP 正文中发送的 XML 元素。 此文件提供了可用于给定请求-响应消息交互的 XML 结构的常规路线图。 在客户端和服务器之间发送的实际 XML 结构基于所用的选项和上下文。 架构文件定义了可能的 XML。 通过网络发送的实际 XML 范围取决于调用的操作、请求的信息和服务器端设置。 
  
## <a name="related-sections"></a>相关部分

- [Exchange 的 SOAP 自动发现 web 服务参考](soap-autodiscover-web-service-reference-for-exchange.md)    
- [Exchange 的 EWS 引用](ews-reference-for-exchange.md)    
- [Exchange 的统一消息 web 服务参考](unified-messaging-web-service-reference-for-exchange.md)
    
## <a name="see-also"></a>另请参阅

- [Exchange 的自动发现 web 服务参考](autodiscover-web-service-reference-for-exchange.md)
- [Exchange 自动发现](../exchange-web-services/autodiscover-for-exchange.md)
- [开始使用 Exchange 中的 Web 服务](../exchange-web-services/start-using-web-services-in-exchange.md)
    

