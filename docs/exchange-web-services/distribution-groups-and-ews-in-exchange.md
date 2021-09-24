---
title: 通讯组和 Exchange 中的 EWS
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: fe08c2e3-92a0-43ec-bc61-69b14caee8fe
description: 了解 EWS 托管 API 或 EWS 应用程序中提供的不同类型的Exchange以及如何管理这些通讯组。
ms.openlocfilehash: 71dc1a1e4c71310943eb19f8a5d6b3f470ab7ccb
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512301"
---
# <a name="distribution-groups-and-ews-in-exchange"></a>通讯组和 Exchange 中的 EWS

了解 EWS 托管 API 或 EWS 应用程序中提供的不同类型的Exchange以及如何管理这些通讯组。
  
通讯组是与单个别名或电子邮件地址相关联的电子邮件地址的集合。 通讯 (有时也称为通讯) 列表，允许用户使用单个收件人地址向多个用户发送电子邮件。 由于通讯组成员身份以及邮件收件人可以在单个电子邮件线程之外进行管理，因此通讯组提供了一种非常出色的方法，可以将邮件分发到一组用户。 您可以使用 EWS 托管 API、EWS 和命令行管理程序以编程方式Exchange通讯组。 在开始编程之前，让我们了解一下可用的不同类型的通讯组以及用于管理这些通讯组的选项。
  
## <a name="types-of-distribution-groups"></a>通讯组类型

Exchange支持三种类型的通讯组：
  
- [通用通讯组](distribution-groups-and-ews-in-exchange.md#bk_DistributionGroup) - 启用邮件的 Active Directory 通用通讯组对象。 通用通讯组用于将邮件分发给一组收件人。 
    
- [安全组](distribution-groups-and-ews-in-exchange.md#bk_SecurityGroup) — 启用邮件的 Active Directory 对象;也称为通用安全组。 安全组用于向 Active Directory 域服务中的资源分配 (AD DS) 以及分发邮件。 
    
- [联系人](distribution-groups-and-ews-in-exchange.md#bk_ContactGroup) 组 — 位于用户邮箱中的专用通讯组。 
    
您选择的通讯组类型取决于您计划存储通讯组的位置、将使用通讯组的人及其用途。

<a name="bk_DistributionGroup"> </a>

### <a name="universal-distribution-groups"></a>通用通讯组

可以使用通用通讯组将收件人组合并为单个别名或电子邮件地址。 由于通用通讯组存储在 AD DS 中，因此任何人都可以使用它们发送电子邮件，包括组织外部的用户。 您可以使用 EWS 托管 API 或 EWS 展开通讯组，但若要创建和管理通讯组，您需要使用 Exchange 命令行管理程序[cmdlet。](#bk_UsingEMS)
  
您还可以使用通用通讯组来包含会议室的集合;例如，为了使用户能够更轻松地查找会议的会议室。 用户可以向会议请求添加会议室列表（包含会议室资源邮箱的通用通讯组）以查找可用会议室，而无需单独添加每个会议室。
  
可以创建在更新成员身份之前保持不变的静态通用通讯组，也可以创建动态通用通讯组。 动态通用通讯组查询 Active Directory 启用邮件的对象，并基于结果构建组成员身份。 只要向组发送了电子邮件，就会重新计算组成员身份。 

<a name="bk_SecurityGroup"> </a>

### <a name="security-groups"></a>安全组

通用通讯组和安全组在大多数情况下是相同的。 但是，与通用通讯组不同，您可以使用安全组向 AD DS 中的网络资源分配权限。 不能使用 EWS 托管 API 或 EWS 创建和管理安全组;而是使用命令行[Exchange cmdlet。](#bk_UsingEMS) 但是，就像通用通讯组一样，您可以使用 EWS 托管 API 或 EWS 扩展安全组。

<a name="bk_ContactGroup"> </a>

### <a name="contact-groups"></a>联系人组

如果不希望向每个用户授予对服务器的管理访问权限以创建通讯组，但希望允许他们向大量人员发送单个邮件，可以使用联系人组来这样做。 联系人组没有与之关联的电子邮件地址，并且仅存在于一个用户的邮箱中;其他用户将无法访问它。 您可以使用 [EWS 托管 API 或 EWS 创建联系人组](how-to-create-contact-groups-by-using-ews-in-exchange.md)。
  
## <a name="managing-distribution-groups-by-using-the-ews-managed-api-or-ews"></a>使用 EWS 托管 API 或 EWS 管理通讯组

您可以使用 EWS 托管 API 或 EWS 扩展通用通讯组或安全组，并控制联系人组的创建和管理;但是，不能使用这些技术创建或编辑这些组的成员。 
  
**表 1.用于管理通讯组的 EWS 托管 API 方法和 EWS 操作**

|**EWS 托管的 API 方法**|**EWS 操作**|**用于...**|
|:-----|:-----|:-----|
|[ContactGroup 类](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.contactgroup%28v=exchg.80%29.aspx) 方法  <br/> |[CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/> |在应用商店中创建Exchange组。<br/><br/>**注意**：不能使用 EWS 托管 API 或 EWS 创建通用通讯组或安全组。           |
|[ExpandGroup](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.expandgroup%28v=exchg.80%29.aspx) <br/> |[ExpandDL](https://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) <br/> |通过检索通用通讯组、安全组或联系人组的成员列表展开该通讯组。  <br/> |
|[FindItems](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) <br/> |[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) <br/> |搜索邮箱中的联系人组。  <br/> |
|[GetRooms](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.getrooms%28v=exchg.80%29.aspx) <br/> |[GetRooms](https://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) <br/> |检索组织中指定会议室列表中所有会议室的集合。 会议室列表是仅包含会议室资源邮箱的通讯组。  <br/> |
|[ResolveName](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) <br/> |[ResolveNames](https://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) <br/> |搜索并返回可能匹配不明确名称的候选项。 候选人可以是通讯组。  <br/> |
   
可以使用 [ExpandGroup](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.expandgroup%28v=exchg.80%29.aspx) 方法或 [ExpandDL](https://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) 操作返回的信息来确定组中成员的类型。 成员类型由 [MailboxType](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.mailboxtype%28v=exchg.80%29.aspx) EWS 托管 API 枚举和 [MailboxType](https://msdn.microsoft.com/library/696e5fdb-d8c5-40f0-9e79-885eae65dfa4%28Office.15%29.aspx) EWS 元素定义。 
  
**表 2.通讯组的成员类型**

|**MailboxType 枚举值**|**MailboxType 元素值**|**说明**|
|:-----|:-----|:-----|
|邮箱  <br/> |邮箱  <br/> |启用邮件的 Active Directory 对象。  <br/> |
|PublicGroup  <br/> |PublicDL  <br/> |您刚刚展开的组中包含的通讯组。 若要获取成员的完整列表，请同时展开此组。  <br/> |
|ContactGroup  <br/> |PrivateDL  <br/> |一组位于邮箱中且仅对邮箱用户可用的联系人。  <br/> |
|联系人  <br/> |联系人  <br/> |一Exchange数据库联系人或 Active Directory 邮件联系人。  <br/> |

<a name="bk_UsingEMS"> </a>

## <a name="managing-distribution-groups-by-using-the-exchange-management-shell"></a>使用命令行管理程序管理Exchange通讯组

可以使用[命令行Exchange cmdlet](https://msdn.microsoft.com/library/ff326159%28v=exchg.140%29.aspx)在代码中创建和管理通用通讯组和安全组。 
  
> [!NOTE]
> 不能使用命令行Exchange cmdlet 管理联系人组。 
  
**表 3.Exchange用于通讯组的命令行管理程序 cmdlet**

|**Cmdlet**|**用于...**|
|:-----|:-----|
|[Disable-DistributionGroup](https://technet.microsoft.com/library/aa997942%28v=exchg.150%29.aspx) <br/> |从已启用邮件的通讯组中删除邮件功能。  <br/> |
|[Enable-DistributionGroup](https://technet.microsoft.com/library/aa998916%28v=exchg.150%29.aspx) <br/> |对现有通用组启用邮件。  <br/> |
|[Get-DistributionGroup](https://technet.microsoft.com/library/bb124755%28v=exchg.150%29.aspx) <br/> |查询现有通讯组。  <br/> |
|[New-DistributionGroup](https://technet.microsoft.com/library/aa998856%28v=exchg.150%29.aspx) <br/> |创建通讯组。  <br/> |
|[Remove-DistributionGroup](https://technet.microsoft.com/library/aa997627%28v=exchg.150%29.aspx) <br/> |从 AD DS 中删除现有通讯组。  <br/> |
|[Set-DistributionGroup](https://technet.microsoft.com/library/bb124955%28v=exchg.150%29.aspx) <br/> |修改现有通讯组的设置。  <br/> |
|[Add-DistributionGroupMember](https://technet.microsoft.com/library/bb124340%28v=exchg.150%29.aspx) <br/> |将收件人添加到通讯组。  <br/> |
|[Get-DistributionGroupMember](https://technet.microsoft.com/library/aa996367%28v=exchg.150%29.aspx) <br/> |查找现有通讯组的成员。  <br/> |
|[Remove-DistributionGroupMember](https://technet.microsoft.com/library/aa998016%28v=exchg.150%29.aspx) <br/> |从通讯组中删除现有收件人。  <br/> |
|[Update-DistributionGroupMember](https://technet.microsoft.com/library/dd335049%28v=exchg.150%29.aspx) <br/> |更新指定通讯组的成员。  <br/> |
|[Get-DynamicDistributionGroup](https://technet.microsoft.com/library/bb124762%28v=exchg.150%29.aspx) <br/> |检索现有动态通讯组上的设置。  <br/> |
|[New-DynamicDistributionGroup](https://technet.microsoft.com/library/bb125127%28v=exchg.150%29.aspx) <br/> |创建动态通讯组。  <br/> |
|[Remove-DynamicDistributionGroup](https://technet.microsoft.com/library/bb125038%28v=exchg.150%29.aspx) <br/> |删除现有的动态通讯组。 此 cmdlet 从 AD DS 中删除动态通讯组。  <br/> |
|[Set-DynamicDistributionGroup](https://technet.microsoft.com/library/bb123796%28v=exchg.150%29.aspx) <br/> |修改现有动态通讯组的设置。  <br/> |

<a name="bk_UsingEMS"> </a>

## <a name="in-this-section"></a>本节内容

- [在联系人组中使用 EWS 创建Exchange](how-to-create-contact-groups-by-using-ews-in-exchange.md)   
- [在 2013 年 10 月Exchange EWS 展开通讯组](how-to-expand-distribution-groups-by-using-ews-in-exchange-2013.md)
    
## <a name="see-also"></a>另请参阅

- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)   
- [从Exchange代码调用命令行管理程序 Cmdlet](https://msdn.microsoft.com/library/ff326159%28v=exchg.140%29.aspx)
    

