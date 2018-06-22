---
title: Exchange 产品版本中的 EWS 功能
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 186c51dc-ec33-4a5d-b739-c9fcb1d4cdd3
description: EWS 实现新产品版本中的新功能。 使用本文中的信息来确定的设定的 Exchange 版本是否包括支持的数据或需要访问的功能。
ms.openlocfilehash: 6b676781f25eeeb90fd9ab075fbe63198766bd99
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19752715"
---
# <a name="ews-functionality-in-exchange-product-versions"></a>Exchange 产品版本中的 EWS 功能

EWS 实现新产品版本中的新功能。 使用本文中的信息来确定的设定的 Exchange 版本是否包括支持的数据或需要访问的功能。 
  
下表列出的每个版本中包括 EWS 和主要功能的引入 Exchange 版本。
  
## <a name="ews-features-by-product-version"></a>按产品版本的 EWS 功能

|**产品版本**|**功能**|
|:-----|:-----|
|Office 365 和 Exchange Online |除了新功能才会为联机客户端添加当前版本的 Exchange 中包括所有功能。  |
|Exchange 2013 SP1 | 包含在 Exchange 2013 中引入的所有功能。 Exchange 2013 SP1 中引入了以下功能：<ul><li>已读回执现已暂停的更新和删除。</li><li>您可以获取[仲裁传输](http://msdn.microsoft.com/library/43a89f71-8002-4cb0-b3c8-1c2b2597f227%28Office.15%29.aspx)审批信息。</li><li>可以查看投票响应。</li><li>[SetHoldOnMailboxes](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.setholdonmailboxes%28v=exchg.80%29.aspx)方法和[SetHoldOnMailboxes](http://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx)操作接受单个对象中的所有参数。</li><li>电子数据展示搜索可以指定搜索查询的语言和日期范围的区域性特定格式。</li><li>[StreamingSubscriptionConnection](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.streamingsubscriptionconnection%28v=exchg.80%29.aspx)对象现在即可访问[StreamingSubscription](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.streamingsubscription%28v=exchg.80%29.aspx)对象。</li><li>对话有一个设置，以指示它们是否包含受 IRM 保护的邮件。</li><li>与会者可以建议新的开始和结束时间的会议，并将它们包括在其会议响应。</li><li>使用[GroupingInformation](http://msdn.microsoft.com/EN-US/library/office/dn529149%28v=exchg.150%29.aspx)设置 SOAP 自动发现[GetUserSettings](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.autodiscover.autodiscoverservice.getusersettings%28v=exchg.80%29.aspx)方法立即返回维护多个邮箱事件订阅关联。</li></ul> |
|Exchange 2013  | 包含在 Exchange 2010 SP2 中引入的所有功能。 Exchange 2013 中引入了以下功能：  <ul><li>  存档</li><li>电子数据展示</li><li>角色</li><li>保留策略</li><li>统一的联系人存储库</li><li>用户照片</li></ul> |
|Exchange 2010 SP2  | 包含在 Exchange 2010 SP1 中引入的所有功能。 Exchange 2010 SP2 中引入了以下功能：  <ul><li>  获取密码过期</li><li>DateTime 精度</li><li>联系人的更新的属性标识符</li><li>新模拟方案</li></ul> |
|Exchange 2010 SP1  | 包含在 Exchange 2010 中引入的所有功能。 Exchange 2010 SP1 中引入了以下功能：  <ul><li>  创建、 检索和修改收件箱规则</li><li>对存档邮箱的编程访问</li><li>对话操作</li><li>防火墙遍历通知</li><li>改进的管理功能</li><li>改进的混合的版本支持</li><li>限制保护支持</li><li>应用程序访问 EWS 的控制权</li><li>客户端证书身份验证支持</li></ul> |
|Exchange 2010  | 包含在 Exchange 2007 SP1 中引入的所有功能。 初始发行版的 Exchange 2010 中引入了以下功能： <ul> <li>  完整的私有通讯组列表</li><li>用户配置对象</li><li>文件夹关联的项目</li><li>邮件跟踪</li><li>统一消息</li><li>SOAP 自动发现  </li><li>所在的时区的增强的支持</li><li>会议室资源可用性信息</li><li>索引的搜索</li><li>转储程序访问</li><li>邮件提示信息</li></ul> |
|Exchange 2007 SP1  | 包括所有 Exchange 2007 中引入的功能。 Exchange 2007 SP1 中引入了以下功能：  <ul><li>  管理工作委派给</li><li>文件夹权限</li><li>公用文件夹</li><li>发布项目</li><li>ID 转换</li></ul> |
|Exchange 2007  | 初始发行版 Exchange 2007 中引入了以下功能：  <ul><li>  对项目、 文件夹和附件 （创建、 获取、 更新和删除） 完全访问权限</li><li>可用性</li><li>利用 Office 设置</li><li>通知</li><li>Synchronization</li><li>名称解析</li><li>通讯组列表 (DL) 扩展</li><li>搜索</li></ul> |
   
## <a name="see-also"></a>另请参阅

- [Start using web services in Exchange](start-using-web-services-in-exchange.md)
- [迁移到 Exchange 技术](../migrating-to-exchange-online-and-exchange-2013-technologies.md)
- [在 Exchange 中浏览 EWS 托管 API、EWS 和 Web 服务](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)  
    

