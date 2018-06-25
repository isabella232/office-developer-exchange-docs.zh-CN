---
title: 在 Exchange 拉 EWS 删除相关邮箱事件通知
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 83511eea-e0b5-4ef0-83b1-0c5434e6d3ab
description: 了解当您使用 EWS 在 Exchange 中删除项目时引发哪些邮箱事件。
ms.openlocfilehash: b12d6a16cc539f36b6b4dcd7274529e9def3c247
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753006"
---
# <a name="pull-notifications-for-ews-deletion-related-mailbox-events-in-exchange"></a>在 Exchange 拉 EWS 删除相关邮箱事件通知

了解当您使用 EWS 在 Exchange 中删除项目时引发哪些邮箱事件。
  
当[删除项目和邮箱文件夹](deleting-items-by-using-ews-in-exchange.md)，这会触发邮箱事件。 不同版本的 Exchange 到邮箱中项目和文件夹返回以响应更改的不同邮箱事件。 下表标识删除使用拉通知订阅邮箱事件时返回的邮箱事件。 
  
**表 1： 删除相关邮箱事件拉通知**

|**删除和 EWS 操作的类型**|**Exchange 2010 通知时指定每个文件夹标识符**|**当指定所有文件夹的 Exchange 2010 通知**|**Exchange Online 和 Exchange 2013 通知时指定每个文件夹标识符**|**当指定所有文件夹的 exchange Online 和 Exchange 2013**|
|:-----|:-----|:-----|:-----|:-----|
|通过[删除项操作](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx)软删除 <br/> |项目的 DeletedEvent。  <br/> 项目的父文件夹的 ModifiedEvent。  <br/> |项目的 DeletedEvent。  <br/> 项目的父文件夹的 ModifiedEvent。  <br/> |项目的 MovedEvent。 此选项指定旧和新的父文件夹标识符。 项目移动到中的删除文件夹转储程序。  <br/> 项目的父文件夹的 ModifiedEvent。  <br/> |项目的 DeletedEvent。  <br/> DeletedEvent AllItems 默认搜索文件夹中的项目。  <br/> 项目的父文件夹的 ModifiedEvent。  <br/> |
|硬通过[删除项操作](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx)删除 <br/> |项目的 DeletedEvent。  <br/> 项目的父文件夹的 ModifiedEvent。  <br/> |项目的 DeletedEvent。  <br/> 项目的父文件夹的 ModifiedEvent。  <br/> |项目的 DeletedEvent。  <br/> 项目的父文件夹的 ModifiedEvent。  <br/> |项目的 DeletedEvent。  <br/> DeletedEvent AllItems 默认搜索文件夹中的项目。  <br/> 项目的父文件夹的 ModifiedEvent。  <br/> |
|通过[删除项操作](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx)将移动到已删除邮件文件夹 <br/> |项目的 MovedEvent。 此选项指定这两个旧和新的父文件夹标识符。  <br/> 项目的旧的父文件夹的 ModifiedEvent。  <br/> 项目的新父文件夹，即已删除邮件文件夹的 ModifiedEvent。  <br/> |项目的 MovedEvent。 此选项指定这两个旧和新的父文件夹标识符。  <br/> 项目的旧的父文件夹的 ModifiedEvent。  <br/> 项目的新父文件夹，即已删除邮件文件夹的 ModifiedEvent。  <br/> |项目的 MovedEvent。 此选项指定这两个旧和新的父文件夹标识符。  <br/> 项目的旧的父文件夹的 ModifiedEvent。  <br/> 项目的新父文件夹，即已删除邮件文件夹的 ModifiedEvent。  <br/> |DeletedEvent AllItems 默认搜索文件夹中。  <br/> CreatedEvent AllItems 文件夹中的项目。  <br/> 项目的原始父文件夹的 ModifiedEvent。  <br/> 已删除邮件文件夹的 ModifiedEvent。  <br/> |
|软删除通过[DeleteFolder 操作](http://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |DeletedEvent 文件夹。  <br/> 文件夹的父文件夹的 ModifiedEvent。  <br/> |DeletedEvent 文件夹。  <br/> 文件夹的父文件夹的 ModifiedEvent。  <br/> |DeletedEvent 文件夹。  <br/> 文件夹的父文件夹的 ModifiedEvent。  <br/> |DeletedEvent 文件夹。  <br/> 文件夹的父文件夹的 ModifiedEvent。  <br/> |
|硬删除通过[DeleteFolder 操作](http://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |DeletedEvent 文件夹。  <br/> 文件夹的父文件夹的 ModifiedEvent。  <br/> |DeletedEvent 文件夹。  <br/> 文件夹的父文件夹的 ModifiedEvent。  <br/> |DeletedEvent 文件夹。  <br/> 文件夹的父文件夹的 ModifiedEvent。  <br/> |DeletedEvent 文件夹。  <br/> 文件夹的父文件夹的 ModifiedEvent。  <br/> |
|通过[DeleteFolder 操作](http://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx)将移动到已删除邮件文件夹 <br/> |MovedEvent 文件夹。 此选项指定这两个旧和新的父文件夹标识符。  <br/> 文件夹的旧的父文件夹的 ModifiedEvent。  <br/> ModifiedEvent 文件夹的新父文件夹，即已删除邮件文件夹。  <br/> |MovedEvent 文件夹。 此选项指定这两个旧和新的父文件夹标识符。  <br/> 文件夹的旧的父文件夹的 ModifiedEvent。  <br/> ModifiedEvent 文件夹的新父文件夹，即已删除邮件文件夹。  <br/> |MovedEvent 文件夹。 此选项指定这两个旧和新的父文件夹标识符。  <br/> 文件夹的旧的父文件夹的 ModifiedEvent。  <br/> ModifiedEvent 文件夹的新父文件夹，即已删除邮件文件夹。  <br/> |文件夹的旧的父文件夹的 ModifiedEvent。  <br/> 为已删除邮件文件夹的文件夹的新父文件夹的 ModifiedEvent。  <br/> |
   
## <a name="see-also"></a>另请参阅


- [Notification subscriptions, mailbox events, and EWS in Exchange](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)
    
- [通过在 Exchange 使用 EWS 中删除项目](deleting-items-by-using-ews-in-exchange.md)
    
- [在 Exchange 处理删除相关 EWS 中的错误](handling-deletion-related-errors-in-ews-in-exchange.md)
    

