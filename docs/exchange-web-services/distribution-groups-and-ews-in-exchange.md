---
title: 通讯组和 Exchange 中的 EWS
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fe08c2e3-92a0-43ec-bc61-69b14caee8fe
description: 了解有关可在 Exchange 中的通讯组的不同类型以及如何 EWS 托管 API 或 EWS 应用程序中管理它们。
ms.openlocfilehash: 725b02c69f004a58c7216763d3c44f1e9d2df2ab
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353957"
---
# <a name="distribution-groups-and-ews-in-exchange"></a>通讯组和 Exchange 中的 EWS

了解有关可在 Exchange 中的通讯组的不同类型以及如何 EWS 托管 API 或 EWS 应用程序中管理它们。
  
通讯组是与单个别名或电子邮件地址关联的电子邮件地址的集合。 通讯组 （有时也称为通讯组列表） 使用户能够通过使用单个收件人地址向多个联系人发送电子邮件。 因为通讯组成员身份，因此邮件的收件人，可以管理个人电子邮件线程之外，通讯组提供极好的方法，以启用到一组用户的邮件的通讯组。 您可以编程方式创建和使用 EWS 托管 API 和 EWS，Exchange 命令行管理程序来管理通讯组。 在开始编程之前，我们将介绍不同类型的可用的通讯组和管理这些选项。
  
## <a name="types-of-distribution-groups"></a>通讯组类型

Exchange 支持三种类型的通讯组：
  
- [通用通讯组](distribution-groups-and-ews-in-exchange.md#bk_DistributionGroup)-已启用邮件的 Active Directory 通用通讯组对象。 通用通讯组用于分发到一组收件人的邮件。 
    
- [安全组](distribution-groups-and-ews-in-exchange.md#bk_SecurityGroup)— 已启用邮件的; 的 Active Directory 对象也称为通用安全组。 安全组可以用来向 Active Directory 域服务 (AD DS) 中的资源分配访问权限，以及分发邮件。 
    
- [联系人组](distribution-groups-and-ews-in-exchange.md#bk_ContactGroup)— 位于用户邮箱的私有通讯组。 
    
您选择的通讯组的类型将取决于打算存储的通讯组中，将使用它，和哪些它将使用的。

<a name="bk_DistributionGroup"> </a>

### <a name="universal-distribution-groups"></a>通用通讯组

您可以使用通用通讯组的收件人组合并到单个别名或电子邮件地址。 因为通用通讯组存储在 AD DS 中，任何人都可以使用它们发送电子邮件，包括组织外部的用户。 您可以使用 EWS 托管 API 或 EWS 展开通讯组，但创建和管理通讯组，您需要使用[Exchange 命令行管理程序 cmdlet](#bk_UsingEMS)。
  
您可以使用通用通讯组来包含的聊天室; 集合例如，若要使用户更轻松地查找会议室的会议。 用户可以添加会议室列表 — 包含会议室资源邮箱的通用通讯组 — 对可用会议室查找而无需逐个添加每个会议室的会议请求。
  
您可以创建之前可以更新成员资格，保持不变的静态通用通讯组，也可以创建动态的通用通讯组。 动态通用通讯组查询 Active Directory 已启用邮件的对象，并构建基于结果的组成员身份。 向组发送电子邮件时，重新计算的组成员身份。 

<a name="bk_SecurityGroup"> </a>

### <a name="security-groups"></a>安全组

通用通讯组和安全组是大多数方式相同。 但是，与通用通讯组，您可以使用安全组分配对 AD DS 中的网络资源的权限。 不能使用 EWS 托管 API 或 EWS 创建和管理安全组;相反，您可以使用[Exchange 命令行管理程序 cmdlet](#bk_UsingEMS)。 但是，就像通用通讯组，您可以使用 EWS 托管 API 或 EWS 扩展安全组。

<a name="bk_ContactGroup"> </a>

### <a name="contact-groups"></a>联系人组

如果不想让服务器创建通讯组的每个用户管理访问，但您想要使用户能够向大型集合的人员发送一条消息，可以使用联系人组来执行此操作。 联系人组没有与其关联的电子邮件地址，只在一个用户的邮箱; 存在其他用户不会有权访问它。 您可以[使用 EWS 托管 API 或 EWS 创建联系人组](how-to-create-contact-groups-by-using-ews-in-exchange.md)。
  
## <a name="managing-distribution-groups-by-using-the-ews-managed-api-or-ews"></a>使用 EWS 托管 API 或 EWS 管理通讯组

您可以使用 EWS 托管 API 或 EWS 以展开通用通讯组或安全组和控制的创建和管理联系人组;但是，不能使用这些技术来创建或编辑这些组的成员。 
  
**表 1。EWS 托管 API 方法和管理通讯组的 EWS 操作**

|**EWS 托管的 API 方法**|**EWS 操作**|**用于...**|
|:-----|:-----|:-----|
|[ContactGroup 类](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.contactgroup%28v=exchg.80%29.aspx)方法  <br/> |[CreatItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/> |在 Exchange 存储中创建联系人组。<br/><br/>**注意**： 您无法使用 EWS 托管 API 或 EWS 中创建的通用通讯组或安全组。           |
|[ExpandGroup](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.expandgroup%28v=exchg.80%29.aspx) <br/> |[ExpandDL](http://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) <br/> |通过检索其成员的列表中展开通用通讯组、 安全组或联系人组。  <br/> |
|[FindItems](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) <br/> |[FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) <br/> |搜索的邮箱中的联系人组。  <br/> |
|[GetRooms](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.getrooms%28v=exchg.80%29.aspx) <br/> |[GetRooms](http://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) <br/> |检索组织中指定的会议室列表中的所有聊天室的集合。 通讯组，其中仅包含会议室资源邮箱会议室列表。  <br/> |
|[ResolveName](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) <br/> |[ResolveNames](http://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) <br/> |搜索并返回可能要与模糊名称匹配的候选项。 候选项可以是通讯组。  <br/> |
   
返回[ExpandGroup](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.expandgroup%28v=exchg.80%29.aspx)方法或[ExpandDL](http://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx)操作的信息可用于确定成员的类型是组中。 由[MailboxType](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.mailboxtype%28v=exchg.80%29.aspx) EWS 托管 API 枚举和[MailboxType](http://msdn.microsoft.com/library/696e5fdb-d8c5-40f0-9e79-885eae65dfa4%28Office.15%29.aspx) EWS 元素定义成员类型。 
  
**表 2。通讯组成员类型**

|**MailboxType 枚举值**|**MailboxType 元素的值**|**说明**|
|:-----|:-----|:-----|
|Mailbox  <br/> |Mailbox  <br/> |已启用邮件的 Active Directory 对象。  <br/> |
|PublicGroup  <br/> |PublicDL  <br/> |包含在您刚刚扩展组通讯组。 若要获取的成员的完整列表，请展开以及此组。  <br/> |
|ContactGroup  <br/> |PrivateDL  <br/> |一组联系人的位于邮箱，并且只可供该邮箱的用户。  <br/> |
|联系人  <br/> |联系人  <br/> |Exchange 数据库联系人或 Active Directory 邮件联系人。  <br/> |

<a name="bk_UsingEMS"> </a>

## <a name="managing-distribution-groups-by-using-the-exchange-management-shell"></a>使用 Exchange 命令行管理程序来管理通讯组

您可以[使用 Exchange 命令行管理程序 cmdlet](http://msdn.microsoft.com/en-us/library/ff326159%28v=exchg.140%29.aspx)可以创建和管理通用通讯组和在代码中的安全组。 
  
> [!NOTE]
> 不能使用 Exchange 命令行管理程序 cmdlet 来管理联系人组。 
  
**表 3。有关使用通讯组的 Exchange 命令行管理程序 cmdlet**

|**Cmdlet**|**用于...**|
|:-----|:-----|
|[Disable-distributiongroup](http://technet.microsoft.com/en-us/library/aa997942%28v=exchg.150%29.aspx) <br/> |从已启用邮件的通讯组中删除邮件功能。  <br/> |
|[Enable-distributiongroup](http://technet.microsoft.com/en-us/library/aa998916%28v=exchg.150%29.aspx) <br/> |邮件启用对现有通用组。  <br/> |
|[Get-distributiongroup](http://technet.microsoft.com/en-us/library/bb124755%28v=exchg.150%29.aspx) <br/> |查询现有通讯组。  <br/> |
|[新 DistributionGroup](http://technet.microsoft.com/en-us/library/aa998856%28v=exchg.150%29.aspx) <br/> |创建通讯组。  <br/> |
|[Remove-distributiongroup](http://technet.microsoft.com/en-us/library/aa997627%28v=exchg.150%29.aspx) <br/> |从 AD DS 中删除现有通讯组。  <br/> |
|[Set-distributiongroup](http://technet.microsoft.com/en-us/library/bb124955%28v=exchg.150%29.aspx) <br/> |修改现有通讯组的设置。  <br/> |
|[添加 DistributionGroupMember](http://technet.microsoft.com/en-us/library/bb124340%28v=exchg.150%29.aspx) <br/> |将收件人添加到通讯组。  <br/> |
|[Get-distributiongroupmember](http://technet.microsoft.com/en-us/library/aa996367%28v=exchg.150%29.aspx) <br/> |查找现有通讯组的成员。  <br/> |
|[Remove-distributiongroupmember](http://technet.microsoft.com/en-us/library/aa998016%28v=exchg.150%29.aspx) <br/> |从通讯组中删除现有收件人。  <br/> |
|[Update-distributiongroupmember](http://technet.microsoft.com/en-us/library/dd335049%28v=exchg.150%29.aspx) <br/> |更新指定的通讯组的成员。  <br/> |
|[Get-dynamicdistributiongroup](http://technet.microsoft.com/en-us/library/bb124762%28v=exchg.150%29.aspx) <br/> |检索现有动态通讯组上的设置。  <br/> |
|[新 DynamicDistributionGroup](http://technet.microsoft.com/en-us/library/bb125127%28v=exchg.150%29.aspx) <br/> |创建动态通讯组。  <br/> |
|[删除 DynamicDistributionGroup](http://technet.microsoft.com/en-us/library/bb125038%28v=exchg.150%29.aspx) <br/> |删除现有动态通讯组。 此 cmdlet 从 AD DS 中删除动态通讯组。  <br/> |
|[Set-dynamicdistributiongroup](http://technet.microsoft.com/en-us/library/bb123796%28v=exchg.150%29.aspx) <br/> |修改现有动态通讯组的设置。  <br/> |

<a name="bk_UsingEMS"> </a>

## <a name="in-this-section"></a>本节内容

- [使用 EWS 在 Exchange 中创建联系人组](how-to-create-contact-groups-by-using-ews-in-exchange.md)   
- [通过使用 EWS 在 Exchange 2013 中展开通讯组](how-to-expand-distribution-groups-by-using-ews-in-exchange-2013.md)
    
## <a name="see-also"></a>另请参阅

- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)   
- [从托管代码调用 Exchange 管理命令行管理程序 Cmdlet](http://msdn.microsoft.com/en-us/library/ff326159%28v=exchg.140%29.aspx)
    

