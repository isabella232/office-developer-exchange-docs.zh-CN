---
title: SOAP Exchange 2013 自动发现 XML 元素
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: ae18a5b3-ae44-4cff-8654-db8028565e01
description: 在 Exchange 查找 SOAP 自动发现 web 服务的 XML 元素引用信息。
ms.openlocfilehash: 7201ef33060691df70b63d06b2045e1120b0610f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827517"
---
# <a name="soap-autodiscover-xml-elements-for-exchange-2013"></a>SOAP Exchange 2013 自动发现 XML 元素

在 Exchange 查找 SOAP 自动发现 web 服务的 XML 元素引用信息。
  
本节中的文档基于客户端和服务器之间发送的 SOAP 自动发现 XML 元素实例。 此 XML 实例文档基于位于虚拟目录承载 SOAP 自动发现服务的 WSDL 和架构文件。 通过使用的 URL 类似于以下任一情况下，经过身份验证的用户可以浏览到所 WSDL 和架构文件：
  
- http://\<yourclientaccessserver\>.com/autodiscover/services.wsdl 或http://autodiscover.\<yourclientaccessserver\>.com/autodiscover/services.wsdl— WSDL 文件的位置。
    
- http://\<yourclientaccessserver\>.com/autodiscover/messages.xsd 或http://autodiscover.\<yourclientaccessserver\>.com/autodiscover/messages.xsd— 消息架构的位置。
    
SOAP 自动发现 WSDL 和架构文件的位置而异 Exchange 安装。
  
Messages.xsd 架构文件描述可自动发现 SOAP 标头和 SOAP 正文中发送的 XML 元素。 此文件提供什么 XML 结构可为给定的请求响应消息交互的常规路线图。 客户端和服务器之间发送的实际 XML 结构基于选项和使用它的上下文。 架构文件定义 XML 是可能。 实际范围的 XML，并通过线路发送基于调用的操作，将请求的信息和服务器端设置。 
  
## <a name="related-sections"></a>相关部分
<a name="bk_RelatedSections"> </a>

- [Exchange SOAP 自动发现 web 服务引用](soap-autodiscover-web-service-reference-for-exchange.md)
    
- [Exchange 的 EWS 引用](ews-reference-for-exchange.md)
    
- [Exchange 统一的消息 web 服务引用](unified-messaging-web-service-reference-for-exchange.md)
    
## <a name="see-also"></a>另请参阅

- [Exchange 的自动发现 web 服务引用](autodiscover-web-service-reference-for-exchange.md)
- [Exchange 自动发现](../exchange-web-services/autodiscover-for-exchange.md)
- [Start using web services in Exchange](../exchange-web-services/start-using-web-services-in-exchange.md)
    

