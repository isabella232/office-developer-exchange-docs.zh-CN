---
title: Exchange Web 服务 (EWS) 生成的 Exchange 对象模型
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 67d7d831-9c53-46da-80e4-18f562e71284
description: 若要根据 EWS 生成的对象模型参考来开发 Exchange 应用程序，请了解其他 EWS 开发选项。
ms.openlocfilehash: 94735a205748116457cb74efc2a75b0b2aa2c9ec
ms.sourcegitcommit: 4221fd619bc309d2f8ab0497ec780b427acc6530
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/08/2018
ms.locfileid: "25441531"
---
# <a name="ews-generated-object-models-for-exchange"></a>EWS 生成的 Exchange 对象模型

**适用于**：Exchange Online | Exchange Server 2013 | Office 365

最初，由 wsdl.exe 生成的 Exchange Web 服务 (EWS) 对象模型提供了可用于 Exchange 2007 的便捷对象模型。 不过，推出的 EWS 托管 API 为使用托管代码的开发人员带来了许多优势。 

EWS 托管 API：

- 提供更直观的对象模型。

- 包含客户端业务逻辑和数据验证。

- 完全受支持且定期更新。

- 包含自动发现客户端。

- 在 Exchange 中重新实现日志记录、Cookie 管理和诊断报告等客户端功能。

基于 EWS wsdl.exe 的托管参考文档已停用，因为 EWS 托管 API 取代生成的对象模型提供的大部分功能。 同时，众所周知，EWS 托管 API 并不适合所有人。 大多数情况下，这是为 .NET 创建 EWS 客户端的最佳方式，但也存在一些例外情况；例如：

- 要使用的功能[未在 EWS 托管 API 中实现](../exchange-web-services/web-service-api-feature-availability-in-exchange-and-the-ews-managed-api.md#bk_apifeatures)。

- 使用的是除 .NET 以外的其他开发平台。

如果无法使用 EWS 托管 API 开发应用程序，可以：

- 使用第三方 EWS 客户端 API。

- 创建你自己的 EWS 客户端对象模型。

- 使用对象模型生成器。 预期可找到支持大多数主要平台和语言的对象模型生成器。

如果打算使用对象模型生成器，可访问有助于了解生成的对象模型的 XML 参考。 对象模型是通过架构中描述的 XML 结构生成。 通常情况下，对象模型生成器创建的类映射到架构中的复杂类型。 属性通常映射到 XML 元素。

查看 [ExchangeWebServices 命名空间](https://docs.microsoft.com/dotnet/api/exchangewebservices?view=exchange-ews-proxy)。

## <a name="see-also"></a>另请参阅

- [Exchange Web 服务参考](web-services-reference-for-exchange.md)
- [探索 Exchange 中 EWS 托管 API、EWS 和 Web 服务](../exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)
- [Exchange 中 EWS 和其他 Web 服务的最近更新](../exchange-web-services/whats-new-in-ews-and-other-web-services-in-exchange.md)
