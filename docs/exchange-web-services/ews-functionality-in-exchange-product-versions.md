---
title: Exchange 产品版本中的 EWS 功能
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 186c51dc-ec33-4a5d-b739-c9fcb1d4cdd3
description: EWS 在新产品版本中实现新功能。 使用本文中的信息可确定Exchange目标版本是否包含对需要访问的数据或功能的支持。
ms.openlocfilehash: bccd0e84fc28f8a7366f0463e555cceec71aa181
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512280"
---
# <a name="ews-functionality-in-exchange-product-versions"></a>Exchange 产品版本中的 EWS 功能

EWS 在新产品版本中实现新功能。 使用本文中的信息可确定Exchange目标版本是否包含对需要访问的数据或功能的支持。 
  
下表列出了包含 EWS 的 Exchange以及每个版本中引入的主要功能。
  
## <a name="ews-features-by-product-version"></a>按产品版本表示的 EWS 功能

|**产品版本**|**功能**|
|:-----|:-----|
|Office 365 和 Exchange Online |除了为联机客户端添加的任何新功能外，Exchange当前版本的所有功能。  |
|Exchange 2013 SP1 | 包括 2013 年 Exchange 引入的所有功能。 2013 SP1 Exchange引入了以下功能：<ul><li>已读回执现在可以因更新和删除而暂停。</li><li>您可以获取 [经过审核的传输](https://msdn.microsoft.com/library/43a89f71-8002-4cb0-b3c8-1c2b2597f227%28Office.15%29.aspx) 审批信息。</li><li>可以查看投票响应。</li><li>[SetHoldOnMailboxes](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.setholdonmailboxes%28v=exchg.80%29.aspx)方法和[SetHoldOnMailboxes](https://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx)操作接受单个对象中的所有参数。</li><li>电子数据展示搜索可以指定搜索查询的语言和日期范围的区域性特定格式。</li><li>[StreamingSubscriptionConnection](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.streamingsubscriptionconnection%28v=exchg.80%29.aspx)对象现在可以访问[StreamingSubscription](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.streamingsubscription%28v=exchg.80%29.aspx)对象。</li><li>对话具有一个设置，用于指示它们是否包含受 IRM 保护的电子邮件。</li><li>与会者可以建议新的会议开始时间和结束时间，并包括到会议响应中。</li><li>SOAP Autodiscover [GetUserSettings](https://msdn.microsoft.com/library/microsoft.exchange.webservices.autodiscover.autodiscoverservice.getusersettings%28v=exchg.80%29.aspx) 方法现在返回用于维护多邮箱事件订阅相关性的 [GroupingInformation](https://msdn.microsoft.com/library/office/dn529149%28v=exchg.150%29.aspx) 设置。</li></ul> |
|Exchange 2013  | 包括 2010 SP2 Exchange引入的所有功能。 2013 年 Exchange引入了以下功能：  <ul><li>  存档</li><li>电子数据展示</li><li>Personas</li><li>保留策略</li><li>统一联系人存储</li><li>用户照片</li></ul> |
|Exchange 2010 SP2  | 包括 Exchange 2010 SP1 中引入的所有功能。 2010 SP2 Exchange引入了以下功能：  <ul><li>  获取密码过期</li><li>DateTime 精度</li><li>更新了联系人的属性标识符</li><li>新的模拟方案</li></ul> |
|Exchange 2010 SP1  | 包括 2010 年 Exchange 引入的所有功能。 2010 SP1 Exchange引入了以下功能：  <ul><li>  创建、检索和修改收件箱规则</li><li>以编程方式访问存档邮箱</li><li>对话操作</li><li>防火墙遍历通知</li><li>改进的安全功能</li><li>改进的混合版本支持</li><li>限制保护支持</li><li>控制应用程序对 EWS 的访问</li><li>客户端证书身份验证支持</li></ul> |
|Exchange 2010  | 包括 2007 SP1 Exchange引入的所有功能。 2010 年 10 月的初始Exchange引入了以下功能： <ul> <li>  完整的专用通讯组列表</li><li>用户配置对象</li><li>文件夹关联项目</li><li>邮件跟踪</li><li>统一消息</li><li>SOAP 自动发现  </li><li>增强的时区支持</li><li>会议室资源可用性信息</li><li>索引搜索</li><li>垃圾站访问</li><li>邮件提示信息</li></ul> |
|Exchange 2007 SP1  | 包括 2007 年 Exchange 引入的所有功能。 2007 SP1 Exchange引入了以下功能：  <ul><li>  委派管理</li><li>文件夹权限</li><li>公用文件夹</li><li>发布项目</li><li>ID 转换</li></ul> |
|Exchange 2007  | 2007 年 10 月的初始Exchange引入了以下功能：  <ul><li>  对项目、文件夹和附件的完全访问权限 (创建、获取、更新、删除) </li><li>可用性</li><li>Out of Office settings</li><li>通知</li><li>同步</li><li>名称解析</li><li>DL (扩展) 通讯组列表</li><li>搜索</li></ul> |
   
## <a name="see-also"></a>另请参阅

- [开始使用 Exchange 中的 Web 服务](start-using-web-services-in-exchange.md)
- [迁移到 Exchange 技术](../migrating-to-exchange-online-and-exchange-2013-technologies.md)
- [在 Exchange 中浏览 EWS 托管 API、EWS 和 Web 服务](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)  
    

