---
title: Exchange 中有关与 EWS 删除相关邮箱事件的拉取通知
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 83511eea-e0b5-4ef0-83b1-0c5434e6d3ab
description: 发现在 Exchange 中使用 EWS 删除项目时引发的邮箱事件。
ms.openlocfilehash: c3d98ff798e3d0f6d214111d51da2c81278fd17d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457653"
---
# <a name="pull-notifications-for-ews-deletion-related-mailbox-events-in-exchange"></a>Exchange 中有关与 EWS 删除相关邮箱事件的拉取通知

发现在 Exchange 中使用 EWS 删除项目时引发的邮箱事件。
  
[从邮箱中删除项目和文件夹](deleting-items-by-using-ews-in-exchange.md)时，会触发邮箱事件。 不同版本的 Exchange 返回不同的邮箱事件，以响应对邮箱中的项目和文件夹所做的更改。 下表列出了使用拉取通知订阅邮箱事件时返回的删除的邮箱事件。 
  
**表1：请求通知的与删除相关的邮箱事件**

|**删除类型和 EWS 操作**|**指定每个文件夹标识符时的 Exchange 2010 通知**|**指定所有文件夹时的 Exchange 2010 通知**|**当您指定每个文件夹标识符时，exchange Online 和 Exchange 2013 通知**|**指定所有文件夹时的 exchange Online 和 Exchange 2013**|
|:-----|:-----|:-----|:-----|:-----|
|通过[DeleteItem 操作](https://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx)进行软删除 <br/> |项目的 DeletedEvent。  <br/> 项目的父文件夹的 ModifiedEvent。  <br/> |项目的 DeletedEvent。  <br/> 项目的父文件夹的 ModifiedEvent。  <br/> |项目的 MovedEvent。 这将指定旧的和新的父文件夹标识符。 将项目移动到转储程序中的 "删除" 文件夹。  <br/> 项目的父文件夹的 ModifiedEvent。  <br/> |项目的 DeletedEvent。  <br/> Allitems.aspx 默认搜索文件夹中的项目的 DeletedEvent。  <br/> 项目的父文件夹的 ModifiedEvent。  <br/> |
|通过[DeleteItem 操作](https://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx)进行硬删除 <br/> |项目的 DeletedEvent。  <br/> 项目的父文件夹的 ModifiedEvent。  <br/> |项目的 DeletedEvent。  <br/> 项目的父文件夹的 ModifiedEvent。  <br/> |项目的 DeletedEvent。  <br/> 项目的父文件夹的 ModifiedEvent。  <br/> |项目的 DeletedEvent。  <br/> Allitems.aspx 默认搜索文件夹中的项目的 DeletedEvent。  <br/> 项目的父文件夹的 ModifiedEvent。  <br/> |
|通过[DeleteItem 操作](https://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx)移动到 "已删除邮件" 文件夹 <br/> |项目的 MovedEvent。 这将指定旧的和新的父文件夹标识符。  <br/> 项目的旧父文件夹的 ModifiedEvent。  <br/> ModifiedEvent 项目的新父文件夹，即 "已删除邮件" 文件夹。  <br/> |项目的 MovedEvent。 这将指定旧的和新的父文件夹标识符。  <br/> 项目的旧父文件夹的 ModifiedEvent。  <br/> ModifiedEvent 项目的新父文件夹，即 "已删除邮件" 文件夹。  <br/> |项目的 MovedEvent。 这将指定旧的和新的父文件夹标识符。  <br/> 项目的旧父文件夹的 ModifiedEvent。  <br/> ModifiedEvent 项目的新父文件夹，即 "已删除邮件" 文件夹。  <br/> |Allitems.aspx 默认搜索文件夹中的 DeletedEvent。  <br/> Allitems.aspx 文件夹中的项目的 CreatedEvent。  <br/> 项目的原始父文件夹的 ModifiedEvent。  <br/> "已删除邮件" 文件夹的 ModifiedEvent。  <br/> |
|通过[DeleteFolder 操作](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx)进行软删除 <br/> |文件夹的 DeletedEvent。  <br/> 文件夹的父文件夹的 ModifiedEvent。  <br/> |文件夹的 DeletedEvent。  <br/> 文件夹的父文件夹的 ModifiedEvent。  <br/> |文件夹的 DeletedEvent。  <br/> 文件夹的父文件夹的 ModifiedEvent。  <br/> |文件夹的 DeletedEvent。  <br/> 文件夹的父文件夹的 ModifiedEvent。  <br/> |
|通过[DeleteFolder 操作](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx)进行硬删除 <br/> |文件夹的 DeletedEvent。  <br/> 文件夹的父文件夹的 ModifiedEvent。  <br/> |文件夹的 DeletedEvent。  <br/> 文件夹的父文件夹的 ModifiedEvent。  <br/> |文件夹的 DeletedEvent。  <br/> 文件夹的父文件夹的 ModifiedEvent。  <br/> |文件夹的 DeletedEvent。  <br/> 文件夹的父文件夹的 ModifiedEvent。  <br/> |
|通过[DeleteFolder 操作](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx)移动到 "已删除邮件" 文件夹 <br/> |文件夹的 MovedEvent。 这将指定旧的和新的父文件夹标识符。  <br/> ModifiedEvent 为文件夹的旧父文件夹。  <br/> ModifiedEvent 文件夹的新父文件夹，即 "已删除邮件" 文件夹。  <br/> |文件夹的 MovedEvent。 这将指定旧的和新的父文件夹标识符。  <br/> ModifiedEvent 为文件夹的旧父文件夹。  <br/> ModifiedEvent 文件夹的新父文件夹，即 "已删除邮件" 文件夹。  <br/> |文件夹的 MovedEvent。 这将指定旧的和新的父文件夹标识符。  <br/> ModifiedEvent 为文件夹的旧父文件夹。  <br/> ModifiedEvent 文件夹的新父文件夹，即 "已删除邮件" 文件夹。  <br/> |ModifiedEvent 为文件夹的旧父文件夹。  <br/> ModifiedEvent 的文件夹的新父文件夹，它是 "已删除邮件" 文件夹。  <br/> |
   
## <a name="see-also"></a>另请参阅


- [Notification subscriptions, mailbox events, and EWS in Exchange](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)
    
- [使用 Exchange 中的 EWS 删除项目](deleting-items-by-using-ews-in-exchange.md)
    
- [在 Exchange 中处理 EWS 中的与删除相关的错误](handling-deletion-related-errors-in-ews-in-exchange.md)
    

