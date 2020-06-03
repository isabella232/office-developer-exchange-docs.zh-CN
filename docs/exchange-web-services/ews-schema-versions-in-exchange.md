---
title: Exchange 中的 EWS 架构版本
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.assetid: d1ab6f9c-ea91-4022-830d-7f7b759e3935
description: 了解 EWS 架构以及如何设计应用程序以使用它，以及每个架构版本可用的功能，以及架构与 Exchange 服务版本的关联方式。
localization_priority: Priority
ms.openlocfilehash: 6afef658e747b11d9aa5fb7d7a88ba8f5c57ac82
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456009"
---
# <a name="ews-schema-versions-in-exchange"></a>Exchange 中的 EWS 架构版本

了解 EWS 架构以及如何设计应用程序以使用它，以及每个架构版本可用的功能，以及架构与 Exchange 服务版本的关联方式。
  
EWS 架构定义可以发送到 Exchange 并由其返回的数据结构。 包含对 EWS 功能的重大更改的每个新版本的 Exchange 都将包含一个新架构。 EWS 和 EWS 架构都是反向的，在某些情况下，针对早期版本的 EWS 设计的前向兼容应用程序将正常运行，在大多数情况下，在使用更高版本的 ews 的情况下，如果早期版本中包含相同的功能，则将使用面向 EWS 的更高版本的应用程序。 本文将帮助您了解 EWS 架构的角色、架构版本控制的工作原理、架构版本和服务版本之间的关系，以及如何将应用程序设计为使用 EWS 架构。 
  
## <a name="role-of-the-ews-schema"></a>EWS 架构的角色

EWS 架构执行以下操作：
  
- 定义可用于客户端的功能集。 客户端可以使用 SOAP[自动发现服务](autodiscover-for-exchange.md)获取受支持的架构版本的列表。 然后，客户端可以确定它可以访问的功能，因为每个架构版本都代表[EWS 功能集](ews-schema-versions-in-exchange.md#bk_features)。 为 EWS 发布的每个新架构都包含早期版本中的架构实体以及任何新功能的架构定义。 通过这种方式，EWS 支持面向 EWS 的早期版本的应用程序。
    
- 提供 API 约定的一般说明。 您可以使用此约定来确定可发送到 Exchange 和从 Exchange 接收的数据结构。
    
- 提供用于发送请求的版本控制机制。 Exchange 服务器包含其虚拟目录中的所有受支持的 EWS 架构版本。 
    
## <a name="designing-your-application-with-schema-version-in-mind"></a>设计具有架构版本的应用程序，请注意

设计应用程序以使用不同版本的 EWS 架构时，请记住以下几点：
  
- 打开/关闭基于架构版本的功能。 您需要将客户端功能映射到架构版本，在某些情况下，将其映射到服务的版本。 下面的示例将根据架构和服务的版本返回[PropertySet](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) 。 
    
  ```cs
  private static PropertySet InitPropertySetByVersion(ExchangeService service)
  {
      PropertySet props;
      // The schema version to target to access the NormalizedBody property 
      // is Exchange2013 or later. The server version to target to access the 
      // NormalizedBody property on an email is 15 or later, which 
      // equates to Exchange 2013.
      if (service.RequestedServerVersion >= ExchangeVersion.Exchange2013 &amp;&amp;
          service.ServerInfo.MajorVersion >= 15)
      {
          props = new PropertySet(EmailMessageSchema.NormalizedBody);
      }
      else
      {
          props = new PropertySet(EmailMessageSchema.Body);
      }
      return props;
  }
  ```

- 使用支持您要使用的功能的最早版本的 EWS 架构版本请求。 这将使您的客户端适用于大量的潜在 Exchange 服务器。 如果要开发业务线应用程序以仅面向组织的服务器，则这一点不太重要，但如果要为更广泛的 Exchange 受众构建应用程序，这一点非常重要。
    
## <a name="features-by-schema-version"></a>按架构版本的功能
<a name="bk_features"> </a>

可用于客户端的架构版本在**ExchangeVersionType**中的类型为 .xsd 架构的简单类型中进行标识。 **ExchangeVersionType**由[RequestServerVersion](https://msdn.microsoft.com/library/af4032d5-42b3-463e-9d0a-8236d78e5b75%28Office.15%29.aspx)元素实现。 **RequestServerVersion**元素在所有 EWS 请求中发送，以向服务器指示客户端所针对的架构版本。 这反过来又标识了可用于客户端的功能集。 
  
**表1：按产品和架构版本的 EWS 功能**

|**产品版本**|**关联架构版本**|**功能**|
|:-----|:-----|:-----|
|Exchange Online  |最新的架构版本。  |除了为联机客户端添加的任何新功能之外，还包括当前 Exchange 版本中的所有功能。 |
|Exchange 2013 SP1 |Exchange2013_SP1 | 包含 Exchange 2013 中的所有功能。<br/><br/>Exchange 2013 SP1 中引入了以下功能： <ul><li>[邮箱保留策略](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.setholdonmailboxes%28v=exchg.80%29.aspx) </li><li> [建议新时间](how-to-propose-a-new-meeting-time-by-using-ews-in-exchange.md) </li><li>  读取[更新](https://msdn.microsoft.com/library/office/dn600559%28v=exchg.80%29.aspx)和[删除](https://msdn.microsoft.com/library/office/dn600557%28v=exchg.80%29.aspx)项目的回执更新  </li><li> 对话的[IRM 信息](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.conversation.hasirm%28v=exchg.80%29.aspx)更新  </li></ul> |
|Exchange 2013   |Exchange2013   | 包括 Exchange 2007 和 Exchange 2010 中引入的所有功能。 <br/><br/>Exchange 2013 中引入了以下功能：<ul><li>存档  </li><li>  电子数据展示  </li><li>  人数  </li><li>  保留策略  </li><li>  统一联系人存储  </li><li>  用户照片  </li></ul> |
|Exchange 2010 SP2   |Exchange2010_SP2 | 包括 Exchange 2010 SP1 中引入的所有功能。 <br/><br/>Exchange 2010 SP2 中引入了以下功能：<ul><li>获取密码过期  </li><li>  日期时间精度  </li><li>  更新了联系人的属性标识符  </li><li>  新的模拟方案  </li></ul> |
|Exchange 2010 SP1  |Exchange2010_SP1   | 包括 Exchange 2010 中引入的所有功能。 <br/><br/>Exchange 2010 SP1 中引入了以下功能：<ul><li>创建、检索和修改收件箱规则  </li><li>  以编程方式访问存档邮箱  </li><li>  对话操作  </li><li>  防火墙遍历通知  </li><li>  改进的管理功能  </li><li>  改进了混合版本支持  </li><li>  限制保护支持  </li><li>  控制对 EWS 的应用程序访问  </li><li>  客户端证书身份验证支持  </li></ul> |
|Exchange 2010  |Exchange2010   | 包括 Exchange 2007 SP1 中引入的所有功能。 <br/><br/>Exchange 2010 的初始发布版本中引入了以下功能：<ul><li>完整私有通讯组列表  </li><li>  用户配置对象  </li><li>  文件夹关联的项目  </li><li>  邮件跟踪  </li><li>  统一消息  </li><li>  SOAP 自动发现  </li><li>  增强时区支持  </li><li>  会议室资源可用性信息  </li><li>  索引搜索  </li><li>  转储程序访问  </li><li>  邮件提示信息  </li></ul> |
|Exchange 2007 SP1   |Exchange2007_SP1  | 包括 Exchange 2007 中引入的所有功能。 <br/><br/>Exchange 2007 SP1 中引入了以下功能：<ul><li>委派管理  </li><li>  文件夹权限  </li><li>  公用文件夹  </li><li>  发布项目  </li><li>  ID 转换  </li></ul>|
|Exchange 2007  |Exchange2007 | Exchange 2007 的初始发布版本中引入了以下功能：<ul><li>对项目、文件夹和附件的完全访问权限（创建、获取、更新、删除）  </li><li>  供应情况  </li><li>  "外出" 设置  </li><li>  通知  </li><li>  同步  </li><li>  名称解析  </li><li>  通讯组列表（DL）扩展  </li><li>  搜索  </li></ul> |
   
## <a name="relationship-between-the-ews-schema-and-the-service-version"></a>EWS 架构和服务版本之间的关系
<a name="bk_features"> </a>

EWS 架构版本与服务器正在运行的 EWS 服务的版本相关。 EWS 架构的命名模式与 Exchange 的内部部署版本相关。 例如，Exchange 2013 的初始版本具有15.00.0516.032 的服务版本和架构名称**Exchange2013**。 由于架构是为 Exchange 2013 更新的，因此 Exchange 2013 和 Exchange Online 的服务版本15.00.0516.032 和更高版本的最新架构的版本名称相同。 在早期版本的 Exchange 中，EWS 架构未更新为累积更新（以前称为汇总）。 但是，因为 Exchange 更新频率更高，以支持 Exchange Online，所以累积更新现在包含 EWS 的架构更新。 架构文件名称和关联的架构版本名称仅使用 Exchange 本地 Exchange 的 service pack 或主要版本进行更新。
  
虽然 EWS 架构定义了合同，但在某些情况下，服务版本是客户端确定应如何与服务进行交互的唯一方法。 不会反映在架构中的服务行为更改只能由在所有 EWS 响应中返回的服务版本确定。 例如，在 Exchange 2013 中对[公用文件夹](public-folder-access-with-ews-in-exchange.md)进行重新设计时，用于移动和复制公用文件夹的操作也会发生更改。 如果您设计了一个客户端来复制 Exchange 2010 中的公用文件夹，则需要将其更新为使用不同的操作，以便在 Exchange 2013 中获得相同的结果。 
  
## <a name="how-the-ews-schema-is-updated"></a>如何更新 EWS 架构
<a name="bk_features"> </a>

运行 Exchange 版本（从 Exchange 2007 开始）的 exchange 服务器在承载 EWS 服务的虚拟目录中包含 EWS 架构。 当前架构版本始终由类型 .xsd 和消息 .xsd 文件表示。 图1显示了在开发新版本的架构时，消息 .xsd 架构是如何分叉的。 在添加新功能之前，原始邮件的副本。 xsd 架构被包含并重命名以表示以前版本的架构。 随后，将使用新版本的服务说明更新这些 .xsd 文件。
  
**图1。如何更新 EWS 架构**

![显示如何更新 EWS 架构的示意图。分离最新的架构版本，以便对之前版本重命名，且最新文件名显示当前版本。](media/Ex15_EWS_Schema_Update1.png)
  
在更新新版本的 EWS 架构之前，将使用以下约定分叉和重命名架构的当前版本：
  
`<schemaname>-<majorserverversion><servicepack>.xsd`
  
然后，原始文件名表示最新架构。 除了更新和修补程序对架构的早期版本之外，所有新功能都将添加到最新架构中。 
  
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS 架构版本](ews-schema-versions-in-exchange.md) 
- [Exchange 自动发现](autodiscover-for-exchange.md) 
- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)
    

