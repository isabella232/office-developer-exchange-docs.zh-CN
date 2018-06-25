---
title: 收件箱管理和 Exchange 中的 EWS
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3dfa0fc9-64bb-4d18-bff7-bf6b3bed4a0d
description: 了解如何通过使用收件箱规则和阻止发件人列表可以管理 EWS 托管 API 或 EWS 应用程序中的收件箱。
ms.openlocfilehash: fe06c5ee87e2679506ca7247c5fc2c96912dee86
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752903"
---
# <a name="inbox-management-and-ews-in-exchange"></a>收件箱管理和 Exchange 中的 EWS

了解如何通过使用收件箱规则和阻止发件人列表可以管理 EWS 托管 API 或 EWS 应用程序中的收件箱。
  
Exchange 邮箱配备功能来帮助自动组织其传入邮件的用户。 无需用户干预的服务器上运行的所有这些功能，但它们提供不同的需求。 EWS 托管 API 和 EWS 提供访问这些功能，使您的用户可以管理其收件箱。
  
**表 1。收件箱管理功能**

|**如果您希望...**|**使用...**|
|:-----|:-----|
|执行操作 （如将它们移动到另一个文件夹，或删除这些） 的传入邮件上基于特定条件 （如发件人、 主题或附件）  <br/> |收件箱规则  <br/> |
|删除所有传入邮件来自特定发件人  <br/> |阻止发件人列表  <br/> |
   
## <a name="inbox-rules"></a>收件箱规则
<a name="bk_InboxRules"> </a>

面对事实吧： 不是每个电子邮件创建相等。 对于从他/她的管理器中获取用户的每封电子邮件，没有从他/她加入年以前，但从未考虑到离开 Internet cat 视频通讯组列表。 有趣 Internet cat 视频时，可以轻松地在收件箱中的通讯组列表邮件 sea 丢失的通讯组列表获取可以变得的通信和重要邮件量。 许多用户到收件箱规则，以帮助减这些邮件中，打开，并使其收件箱多代码好地方。 使用 Exchange Web Services (EWS)，您的应用程序可以将承担的规则的功能引入。
  
EWS 托管 API 提供用于处理规则[ExchangeService.GetInboxRules](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getinboxrules%28v=exchg.80%29.aspx)和[ExchangeService.UpdateInboxRules](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.updateinboxrules%28v=exchg.80%29.aspx)方法。 EWS 提供用于处理规则[GetInboxRules](http://msdn.microsoft.com/library/b4b2701a-4a23-4acc-8c75-19f7955ad7ae%28Office.15%29.aspx)和[UpdateInboxRules](http://msdn.microsoft.com/library/f982a237-471e-45c5-a2b5-468cfc53150b%28Office.15%29.aspx)操作。 但是，请注意，EWS 托管 API 和 EWS 有以下限制使用收件箱规则时： 
  
- EWS 无法访问或创建"仅限客户端"规则或运行"此计算机上只"在 Outlook 中设置的规则。
    
- 若要使用 EWS 更改当前的规则集，您必须删除 Outlook 规则 BLOB，如果存在。 这意味着，使用 EWS 修改规则删除将通过使用 Outlook 先前已关闭 （禁用） 的任何规则。 
    
### <a name="how-do-rules-work"></a>规则如何工作？
<a name="bk_HowRulesWork"> </a>

规则引擎充当网关守卫到用户的邮箱。 邮件到达用户的邮箱，但在收件箱中将显示以下消息之前，计算该邮件所依据的规则的一个已排序列表。 请注意，这仅会在到达时间，且只能在收件箱。 这些规则将由三个部分组成：[条件](#bk_Conditions)、[操作](#bk_Actions)和[例外](#bk_Exceptions)。
  
直至到达的规则列表末尾，从开始顶部的规则列表的规则，规则引擎执行以下步骤：
  
1. 检查邮件以确定其是否符合规则中指定的所有条件。
    
1. 如果符合所有条件，评估继续执行步骤 2。
    
2. 如果它不满足所有条件，则规则引擎加载规则列表中的下一个规则，并在第 1 步启动。
    
2. 检查邮件以确定是否满足任一规则中指定的例外。
    
1. 如果符合任何异常，规则引擎加载规则列表中的下一个规则，并在第 1 步启动。
    
2. 如果不满足任何异常，评估继续执行步骤 3。
    
3. 执行邮件在规则中指定的操作。
    
1. 如果指定的"停止处理其他规则"操作，则规则引擎执行其他操作在的消息，然后退出而不计算邮件针对任何其他规则。
    
2. 如果未指定的"停止处理其他规则"操作，则规则引擎加载规则列表中的下一个规则，并在第 1 步启动。
    
下图显示了规则引擎下面的过程。
  
**图 1： 规则引擎概述**

![此图说明规则引擎使用的步骤：首先评估规则，然后确定是否满足规则条件，再执行操作或移动到下一个规则，直到完成。](media/Ex15_Rules_EngineOverview.png)
  
### <a name="putting-the-pieces-together---parts-of-a-rule"></a>将部分放置在一起的部件的规则
<a name="bk_Pieces"> </a>

一种方法来可视化规则的部分是假设您向某人将您的传入电子邮件组织需要提供说明。 您可能会向此人说:"时的邮件到达\<插入条件此处\>，执行\<插入操作此处\>，除非消息\<插入例外此处\>。 我们来看更详尽介绍了每个部件。
  
#### <a name="conditions"></a>条件
<a name="bk_Conditions"> </a>

[条件](http://msdn.microsoft.com/library/f049a48c-9585-43f7-8549-0b8cb19a5eea%28Office.15%29.aspx)描述应时应用规则。 时可以省略 （导致适用于每个收到邮件的规则） 的规则的条件，最多的很常见规则设置了适用于传入消息的子集的条件。 一些示例是"时从 Sadie 是一条消息"或"当邮件发送到 Cat 视频情人通讯组列表"。 规则可以有多个条件。 如果规则有多个条件，必须按顺序执行指定的操作的规则引擎满足所有条件。 
  
#### <a name="actions"></a>操作
<a name="bk_Actions"> </a>

[操作](http://msdn.microsoft.com/library/c5aa96b1-2d8b-422f-8c2f-f118572ab23f%28Office.15%29.aspx)描述应用规则时，会发生什么情况。 示例是"将邮件移动到猫文件夹"或者"为低重要性标记邮件"。 规则可以有多个操作。 指定规则的多个操作时，应用该规则时执行所有操作。 
  
#### <a name="exceptions"></a>异常
<a name="bk_Exceptions"> </a>

[异常](http://msdn.microsoft.com/library/7cd63ac2-3441-4ed4-915b-6f90af4b28fc%28Office.15%29.aspx)描述时不应该应用规则，即使满足指定条件中的条件。 例如，"除如果邮件仅发送给我"或"除如果邮件是从 Mom"。 规则可以有多个例外项。 规则具有多个例外，以及任何异常满足时不应用该规则。 
  
### <a name="example-herding-those-cats"></a>示例： 收集这些猫
<a name="bk_Example"> </a>

我们来看看您的用户如何使用规则以消除从 Internet cat 视频通讯组列表的流量。 我们假设以下各项：
  
- 这些邮件发送到一个名为"Internet Cat 视频爱好者"的通讯组列表。
    
- 您的用户想要最终阅读这些消息，它们只是不希望他们会干扰其收件箱。 它们将而文件它们在名为"猫"的文件夹中。
    
- 您的用户想要读取立即，发送给此通讯组列表的母语消息，因为 Mom 发送有趣的视频。
    
这会告诉以下规则引擎:"的邮件时，它是到达发送到 Internet Cat 视频爱好者通讯组列表，将其移到猫文件夹，除非该邮件是从 Mom。" 
  
**表 2。规则定义**

|**规则部件**|**值**|
|:-----|:-----|
|条件  <br/> |发送到 Internet Cat 视频爱好者通讯组列表  <br/> |
|操作  <br/> |将邮件移动到猫文件夹  <br/> 和停止处理其他规则  <br/> |
|异常  <br/> |从 Mom  <br/> |
   
> [!NOTE]
> 请注意，"停止处理其他规则"中的结果的规则操作之一。 通常最好包括此操作可避免的混淆通过该规则会在任何给定的消息。 但是，可以通过省略此操作，正确排序规则，获得更高级的处理的传入邮件。 在这种情况下，它可能是 Internet cat 视频邮件不妨碍高级处理得多需要安全匹配。 
  
创建此规则，不久新消息传入。 同事希望向通讯组列表发送邮件。 如果我们心理执行规则引擎的工作，邮件符合 （它发送到 Internet Cat 视频爱好者） 的所有条件，并且它都符合 none （不是从 Mom） 的例外，因此该规则适用和邮件获取移至猫文件夹。
  
下图显示了如何对传入邮件应用规则。
  
**图 2。规则处理传入邮件**

![此说明显示同事发送到通讯组列表的新消息。此消息满足规则中定义的所有条件，且无任何异常，并且将移动到“Cats”文件夹。](media/Ex15_Rules_RuleEvaluationSample.png)
  
## <a name="blocking-senders"></a>阻止发件人
<a name="bk_Blocking"> </a>

尽管您可以创建移动的所有邮件来自特定发件人到垃圾邮件文件夹的规则，您也可以执行此操作使用垃圾邮件选项中阻止的发件人列表。 因为没有限制用户可以具有多少规则，所以应该使用阻止发件人列表。 可以通过使用[ExchangeService.MarkAsJunk](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.markasjunk%28v=exchg.80%29.aspx) EWS 托管 API 方法或[MarkAsJunk](http://msdn.microsoft.com/library/1f71f04d-56a9-4fee-a4e7-d1034438329e%28Office.15%29.aspx) EWS 操作来[添加或删除被阻止发件人名单的特定的电子邮件地址](how-to-add-and-remove-email-addresses-from-blocked-senders-list-by-using-ews.md)。 请注意，在 EWS 以访问阻止发件人列表的顺序，用户邮箱必须包含电子邮件从要添加或删除的电子邮件地址。 
  
## <a name="in-this-section"></a>本节内容
<a name="bk_InThisSection"> </a>

- [使用 EWS 在 Exchange 管理收件箱规则](how-to-manage-inbox-rules-by-using-ews-in-exchange.md)
    
- [添加并在 Exchange 使用 EWS 从阻止发件人列表中删除电子邮件地址](how-to-add-and-remove-email-addresses-from-blocked-senders-list-by-using-ews.md)
    
## <a name="see-also"></a>另请参阅


- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)
    
- [GetInboxRules 操作](http://msdn.microsoft.com/library/b4b2701a-4a23-4acc-8c75-19f7955ad7ae%28Office.15%29.aspx)
    
- [UpdateInboxRules 操作](http://msdn.microsoft.com/library/f982a237-471e-45c5-a2b5-468cfc53150b%28Office.15%29.aspx)
    
- [MarkAsJunk 操作](http://msdn.microsoft.com/library/1f71f04d-56a9-4fee-a4e7-d1034438329e%28Office.15%29.aspx)
    

