---
title: Inbox management and EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 3dfa0fc9-64bb-4d18-bff7-bf6b3bed4a0d
description: 了解如何使用收件箱规则和阻止的发件人列表在 EWS 托管 API 或 EWS 应用程序中管理收件箱。
ms.openlocfilehash: 6dddb8d462276c4983fd04a0206d4d4a9be32df8
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522213"
---
# <a name="inbox-management-and-ews-in-exchange"></a>Inbox management and EWS in Exchange

了解如何使用收件箱规则和阻止的发件人列表在 EWS 托管 API 或 EWS 应用程序中管理收件箱。
  
Exchange邮箱配备了可帮助用户自动组织传入邮件的功能。 这些功能均在服务器上运行，无需用户干预，但它们满足不同的需求。 EWS 托管 API 和 EWS 提供对这些功能的访问权限，使用户可以管理其收件箱。
  
**表 1.收件箱管理功能**

|**如果你想要...**|**使用...**|
|:-----|:-----|
|根据发件人、主题或附件 (等特定条件) 传入的邮件或邮件 (移动至另一个文件夹)   <br/> |收件箱规则  <br/> |
|删除来自特定发件人的所有传入邮件  <br/> |阻止发件人列表  <br/> |
   
## <a name="inbox-rules"></a>收件箱规则
<a name="bk_InboxRules"> </a>

让我们面对这一点：不是每个电子邮件都创建一样。 对于用户从其经理处获取的每封电子邮件，他（她）在几年前加入的 Internet cat 视频通讯组列表中都有一个电子邮件，并且从不离开。 虽然 Internet cat 视频很有趣，但通讯组列表获取的流量量可能会失去控制，并且重要的消息很容易在收件箱的通讯组列表邮件的其中丢失。 许多用户都转向收件箱规则以帮助减少这些邮件，并让他们的收件箱更友好。 通过Exchange EWS (EWS) ，应用程序可以承担规则的能力。
  
EWS 托管 API 提供 [ExchangeService.GetInboxRules](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getinboxrules%28v=exchg.80%29.aspx) 和 [ExchangeService.UpdateInboxRules](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.updateinboxrules%28v=exchg.80%29.aspx) 方法，用于处理规则。 EWS 提供 [GetInboxRules](https://msdn.microsoft.com/library/b4b2701a-4a23-4acc-8c75-19f7955ad7ae%28Office.15%29.aspx) 和 [UpdateInboxRules](https://msdn.microsoft.com/library/f982a237-471e-45c5-a2b5-468cfc53150b%28Office.15%29.aspx) 操作以使用规则。 但是请注意，在使用收件箱规则时，EWS 托管 API 和 EWS 具有以下限制： 
  
- EWS 无法访问或创建"仅客户端"规则或 Outlook设置为"仅在此计算机上运行"的规则。
    
- 若要使用 EWS 更改当前规则集，必须删除Outlook BLOB（如果存在）。 这意味着，使用 EWS 修改规则会删除以前使用 EWS (禁用) 规则Outlook。 
    
### <a name="how-do-rules-work"></a>规则如何工作？
<a name="bk_HowRulesWork"> </a>

规则引擎充当用户邮箱的网关守卫。 当邮件到达用户邮箱时，但在该邮件出现在收件箱中之前，会根据规则顺序列表评估该邮件。 请注意，这仅在到达时发生，并且仅在收件箱中发生。 这些规则由三部分组成：[条件、](#bk_Conditions)[操作](#bk_Actions)和[例外](#bk_Exceptions)。
  
从规则列表顶部的规则开始，规则引擎将执行以下步骤，直到到达规则列表的末尾：
  
1. 检查邮件以确定它是否满足规则中指定的所有条件。
    
1. 如果它满足所有条件，则继续执行步骤 2 的评估。
    
2. 如果规则引擎不满足所有条件，则它会加载规则列表中的下一个规则，然后从步骤 1 开始。
    
2. 检查邮件以确定它是否满足规则中指定的任何例外。
    
1. 如果规则引擎满足任何例外，则规则引擎将加载规则列表中的下一个规则，然后从步骤 1 开始。
    
2. 如果它不满足任何例外，则继续执行步骤 3 的评估。
    
3. 对邮件执行规则中指定的操作。
    
1. 如果指定了"停止处理更多规则"操作，则规则引擎对邮件执行所有其他操作，然后退出而不针对邮件评估任何其他规则。
    
2. 如果未指定"停止处理更多规则"操作，则规则引擎将加载规则列表中的下一个规则，然后从步骤 1 开始。
    
下图显示了规则引擎遵循的过程。
  
**图 1：规则引擎概述**

![此图说明规则引擎使用的步骤：首先评估规则，然后确定是否满足规则条件，再执行操作或移动到下一个规则，直到完成。](media/Ex15_Rules_EngineOverview.png)
  
### <a name="putting-the-pieces-together---parts-of-a-rule"></a>将片段放在一起 - 规则的一部分
<a name="bk_Pieces"> </a>

可视化规则部分的一个方法就是想象你正在向负责组织传入电子邮件的人提供说明。 您可能会对此人说："当邮件到达时，请执行 \<insert conditions here\> \<insert actions here\> ，除非邮件 \<insert exceptions here\> 。 让我们进一步了解一下每个部分。
  
#### <a name="conditions"></a>条件
<a name="bk_Conditions"> </a>

[条件](https://msdn.microsoft.com/library/f049a48c-9585-43f7-8549-0b8cb19a5eea%28Office.15%29.aspx) 描述应何时应用规则。 虽然可以省略规则的条件， (产生应用于收到) 的每封邮件的规则，但规则具有适用于传入邮件子集的条件更为常见。 一些示例包括"当邮件来自一个通讯组列表时"或"当邮件发送到'Cat Video Lovers'通讯组列表时"。 规则可以有多个条件。 当规则具有多个条件时，必须满足所有条件，规则引擎才能执行指定的操作。 
  
#### <a name="actions"></a>操作
<a name="bk_Actions"> </a>

[操作](https://msdn.microsoft.com/library/c5aa96b1-2d8b-422f-8c2f-f118572ab23f%28Office.15%29.aspx) 描述在应用规则时会发生什么情况。 示例包括"将邮件移动到'猫'文件夹"或"将邮件标记为'低'重要性"。 规则可以有多个操作。 为规则指定多个操作时，所有操作在应用规则时执行。 
  
#### <a name="exceptions"></a>例外
<a name="bk_Exceptions"> </a>

[例外](https://msdn.microsoft.com/library/7cd63ac2-3441-4ed4-915b-6f90af4b28fc%28Office.15%29.aspx) 描述了何时不应应用规则，即使满足条件中指定的条件也不例外。 示例包括"邮件仅发送给我时除外"或"邮件来自 Mom 时除外"。 规则可以有多个例外。 如果规则具有多个例外，并且满足任何例外，则不应用该规则。 
  
### <a name="example-herding-those-cats"></a>示例：为这些动物提供一些支持
<a name="bk_Example"> </a>

我们来看看用户如何使用规则消除来自该 Internet cat 视频通讯组列表的流量。 假设以下内容：
  
- 这些消息将发送到名为"Internet Cat Video Enthusiasts"的通讯组列表。
    
- 你的用户最终想要阅读这些邮件，只是不希望他们使收件箱变得混乱。 他们更希望将它们放在名为"猫"的文件夹中。
    
- 你的用户想要立即阅读由他们的用户发送到此通讯组列表的邮件，因为 Mom 发送了最有趣的视频。
    
这将告知规则引擎以下内容："当发送到"Internet Cat Video Enthusiasts"通讯组列表的邮件到达时，请将其移动到"猫"文件夹，除非邮件来自 Mom。" 
  
**表 2.规则定义**

|**规则部分**|**值**|
|:-----|:-----|
|条件  <br/> |发送到"Internet Cat Video Enthusiasts"通讯组列表  <br/> |
|操作  <br/> |将邮件移动到"猫"文件夹  <br/> 并停止处理更多规则  <br/> |
|例外  <br/> |From 'Mom'  <br/> |
   
> [!NOTE]
> 请注意，"停止处理更多规则"是生成的规则中的操作之一。 通常，包含此操作是一个好主意，以避免混淆哪个规则作用于任何给定邮件。 但是，通过省略此操作并正确排序规则，可以实现对传入邮件的更高级处理。 在这种情况下，Internet cat 视频消息不需要太多高级处理，这很可能是一个安全匹配。 
  
创建此规则后，将出现一条新消息。 同事希望向通讯组列表发送消息。 如果我们从心上执行规则引擎的工作，则邮件满足所有条件 (它将发送到"Internet Cat Videos Enthusiasts") ，并且它未满足任何例外 (它不是从"Mom") 发送，因此规则适用，邮件将移动到"猫"文件夹。
  
下图显示了如何将规则应用于传入的邮件。
  
**图 2.传入邮件由规则处理**

![此说明显示同事发送到通讯组列表的新消息。此消息满足规则中定义的所有条件，且无任何异常，并且将移动到“Cats”文件夹。](media/Ex15_Rules_RuleEvaluationSample.png)
  
## <a name="blocking-senders"></a>阻止发件人
<a name="bk_Blocking"> </a>

虽然您可以创建一个规则，将所有邮件从特定发件人移动到"垃圾邮件"文件夹，但您也可以使用"垃圾邮件"选项中的"阻止的发件人名单"来这样做。 由于用户具有的规则数存在限制，因此使用阻止的发件人列表是有意义的。 您可以使用[](how-to-add-and-remove-email-addresses-from-blocked-senders-list-by-using-ews.md)[ExchangeService.MarkAsJunk](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.markasjunk%28v=exchg.80%29.aspx) EWS 托管 API 方法或[MarkAsJunk](https://msdn.microsoft.com/library/1f71f04d-56a9-4fee-a4e7-d1034438329e%28Office.15%29.aspx) EWS 操作在阻止的发件人列表中添加或删除特定电子邮件地址。 请注意，为了让 EWS 访问阻止的发件人列表，用户的邮箱必须包含一封来自要添加或删除的电子邮件地址的电子邮件。 
  
## <a name="in-this-section"></a>本节内容
<a name="bk_InThisSection"> </a>

- [在收件箱中通过使用 EWS 管理Exchange](how-to-manage-inbox-rules-by-using-ews-in-exchange.md)
    
- [使用"阻止的发件人列表"中的 EWS 添加和删除Exchange](how-to-add-and-remove-email-addresses-from-blocked-senders-list-by-using-ews.md)
    
## <a name="see-also"></a>另请参阅


- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)
    
- [GetInboxRules 操作](https://msdn.microsoft.com/library/b4b2701a-4a23-4acc-8c75-19f7955ad7ae%28Office.15%29.aspx)
    
- [UpdateInboxRules 操作](https://msdn.microsoft.com/library/f982a237-471e-45c5-a2b5-468cfc53150b%28Office.15%29.aspx)
    
- [MarkAsJunk 操作](https://msdn.microsoft.com/library/1f71f04d-56a9-4fee-a4e7-d1034438329e%28Office.15%29.aspx)
    

