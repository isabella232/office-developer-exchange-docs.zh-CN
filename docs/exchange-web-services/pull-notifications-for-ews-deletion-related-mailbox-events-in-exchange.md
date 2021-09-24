---
title: 拉取与 EWS 删除相关的邮箱事件Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 83511eea-e0b5-4ef0-83b1-0c5434e6d3ab
description: 发现当您使用邮箱中的 EWS 删除项目时，将引发哪些Exchange。
ms.openlocfilehash: fa04d49f02cfec621f00a9b51b121cff22ca393b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510412"
---
# <a name="pull-notifications-for-ews-deletion-related-mailbox-events-in-exchange"></a>拉取与 EWS 删除相关的邮箱事件Exchange

发现当您使用邮箱中的 EWS 删除项目时，将引发哪些Exchange。
  
从 [邮箱中删除项目和文件夹时](deleting-items-by-using-ews-in-exchange.md)，将触发邮箱事件。 不同版本的邮箱Exchange返回不同的邮箱事件，以响应对邮箱中的项目和文件夹的更改。 下表标识使用拉取通知订阅邮箱事件时返回删除的邮箱事件。 
  
**表 1：拉取通知的与删除相关的邮箱事件**

|**删除类型和 EWS 操作**|**Exchange每个文件夹标识符时发送 2010 通知**|**Exchange所有文件夹时发送 2010 通知**|**Exchange Online每个Exchange标识符时显示 2013 通知和 2013 通知**|**Exchange Online所有文件夹Exchange 2013 和 2013**|
|:-----|:-----|:-----|:-----|:-----|
|通过 [DeleteItem 操作软删除](https://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> |项目的 DeletedEvent。  <br/> ModifiedEvent 项的父文件夹。  <br/> |项目的 DeletedEvent。  <br/> ModifiedEvent 项的父文件夹。  <br/> |项目的 MovedEvent。 这将指定旧的和新的父文件夹标识符。 该项目将移动到垃圾站中的"删除"文件夹。  <br/> ModifiedEvent 项的父文件夹。  <br/> |项目的 DeletedEvent。  <br/> AllItems 默认搜索文件夹中项目的 DeletedEvent。  <br/> ModifiedEvent 项的父文件夹。  <br/> |
|通过 [DeleteItem 操作硬删除](https://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> |项目的 DeletedEvent。  <br/> ModifiedEvent 项的父文件夹。  <br/> |项目的 DeletedEvent。  <br/> ModifiedEvent 项的父文件夹。  <br/> |项目的 DeletedEvent。  <br/> ModifiedEvent 项的父文件夹。  <br/> |项目的 DeletedEvent。  <br/> AllItems 默认搜索文件夹中项目的 DeletedEvent。  <br/> ModifiedEvent 项的父文件夹。  <br/> |
|通过 [DeleteItem 操作移动到"已删除邮件"文件夹](https://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> |项目的 MovedEvent。 这将指定旧父文件夹标识符和新父文件夹标识符。  <br/> ModifiedEvent 项的旧父文件夹。  <br/> ModifiedEvent 用于项目的新父文件夹，即"已删除邮件"文件夹。  <br/> |项目的 MovedEvent。 这将指定旧父文件夹标识符和新父文件夹标识符。  <br/> ModifiedEvent 项的旧父文件夹。  <br/> ModifiedEvent 用于项目的新父文件夹，即"已删除邮件"文件夹。  <br/> |项目的 MovedEvent。 这将指定旧父文件夹标识符和新父文件夹标识符。  <br/> ModifiedEvent 项的旧父文件夹。  <br/> ModifiedEvent 用于项目的新父文件夹，即"已删除邮件"文件夹。  <br/> |DeletedEvent From the AllItems default search folder.  <br/> AllItems 文件夹中项目的 CreatedEvent。  <br/> ModifiedEvent 项目的原始父文件夹。  <br/> ModifiedEvent 用于"已删除邮件"文件夹。  <br/> |
|通过 [DeleteFolder 操作软删除](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |文件夹的 DeletedEvent。  <br/> ModifiedEvent 文件夹的父文件夹。  <br/> |文件夹的 DeletedEvent。  <br/> ModifiedEvent 文件夹的父文件夹。  <br/> |文件夹的 DeletedEvent。  <br/> ModifiedEvent 文件夹的父文件夹。  <br/> |文件夹的 DeletedEvent。  <br/> ModifiedEvent 文件夹的父文件夹。  <br/> |
|通过 [DeleteFolder 操作硬删除](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |文件夹的 DeletedEvent。  <br/> ModifiedEvent 文件夹的父文件夹。  <br/> |文件夹的 DeletedEvent。  <br/> ModifiedEvent 文件夹的父文件夹。  <br/> |文件夹的 DeletedEvent。  <br/> ModifiedEvent 文件夹的父文件夹。  <br/> |文件夹的 DeletedEvent。  <br/> ModifiedEvent 文件夹的父文件夹。  <br/> |
|通过 [DeleteFolder 操作移动到"已删除邮件"文件夹](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |文件夹的 MovedEvent。 这将指定旧父文件夹标识符和新父文件夹标识符。  <br/> ModifiedEvent 文件夹的旧父文件夹。  <br/> ModifiedEvent 用于文件夹的新父文件夹，即"已删除邮件"文件夹。  <br/> |文件夹的 MovedEvent。 这将指定旧父文件夹标识符和新父文件夹标识符。  <br/> ModifiedEvent 文件夹的旧父文件夹。  <br/> ModifiedEvent 用于文件夹的新父文件夹，即"已删除邮件"文件夹。  <br/> |文件夹的 MovedEvent。 这将指定旧父文件夹标识符和新父文件夹标识符。  <br/> ModifiedEvent 文件夹的旧父文件夹。  <br/> ModifiedEvent 用于文件夹的新父文件夹，即"已删除邮件"文件夹。  <br/> |ModifiedEvent 文件夹的旧父文件夹。  <br/> ModifiedEvent 用于文件夹的新父文件夹，即"已删除邮件"文件夹。  <br/> |
   
## <a name="see-also"></a>另请参阅


- [Notification subscriptions, mailbox events, and EWS in Exchange](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)
    
- [使用 Exchange 中的 EWS 删除项目](deleting-items-by-using-ews-in-exchange.md)
    
- [处理 EWS 中与删除相关的Exchange](handling-deletion-related-errors-in-ews-in-exchange.md)
    

