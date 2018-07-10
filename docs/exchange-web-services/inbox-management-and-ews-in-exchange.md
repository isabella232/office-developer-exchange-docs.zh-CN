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
# <a name="inbox-management-and-ews-in-exchange"></a><span data-ttu-id="cd671-103">收件箱管理和 Exchange 中的 EWS</span><span class="sxs-lookup"><span data-stu-id="cd671-103">Inbox management and EWS in Exchange</span></span>

<span data-ttu-id="cd671-104">了解如何通过使用收件箱规则和阻止发件人列表可以管理 EWS 托管 API 或 EWS 应用程序中的收件箱。</span><span class="sxs-lookup"><span data-stu-id="cd671-104">Find out how you can manage your Inbox in your EWS Managed API or EWS application by using Inbox rules and the blocked senders list.</span></span>
  
<span data-ttu-id="cd671-105">Exchange 邮箱配备功能来帮助自动组织其传入邮件的用户。</span><span class="sxs-lookup"><span data-stu-id="cd671-105">Exchange mailboxes come equipped with features to help users organize their incoming mail automatically.</span></span> <span data-ttu-id="cd671-106">无需用户干预的服务器上运行的所有这些功能，但它们提供不同的需求。</span><span class="sxs-lookup"><span data-stu-id="cd671-106">These features all operate on the server without user intervention, but they serve different needs.</span></span> <span data-ttu-id="cd671-107">EWS 托管 API 和 EWS 提供访问这些功能，使您的用户可以管理其收件箱。</span><span class="sxs-lookup"><span data-stu-id="cd671-107">The EWS Managed API and EWS provide access to these features, enabling your users to manage their Inboxes.</span></span>
  
<span data-ttu-id="cd671-108">**表 1。收件箱管理功能**</span><span class="sxs-lookup"><span data-stu-id="cd671-108">**Table 1. Inbox management features**</span></span>

|<span data-ttu-id="cd671-109">**如果您希望...**</span><span class="sxs-lookup"><span data-stu-id="cd671-109">**If you want to…**</span></span>|<span data-ttu-id="cd671-110">**使用...**</span><span class="sxs-lookup"><span data-stu-id="cd671-110">**Use…**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cd671-111">执行操作 （如将它们移动到另一个文件夹，或删除这些） 的传入邮件上基于特定条件 （如发件人、 主题或附件）</span><span class="sxs-lookup"><span data-stu-id="cd671-111">Take action on incoming messages (such as moving them to another folder or deleting them) based on specific criteria (such as sender, subject, or attachments)</span></span>  <br/> |<span data-ttu-id="cd671-112">收件箱规则</span><span class="sxs-lookup"><span data-stu-id="cd671-112">Inbox rules</span></span>  <br/> |
|<span data-ttu-id="cd671-113">删除所有传入邮件来自特定发件人</span><span class="sxs-lookup"><span data-stu-id="cd671-113">Delete all incoming mail from a particular sender</span></span>  <br/> |<span data-ttu-id="cd671-114">阻止发件人列表</span><span class="sxs-lookup"><span data-stu-id="cd671-114">Blocked Senders List</span></span>  <br/> |
   
## <a name="inbox-rules"></a><span data-ttu-id="cd671-115">收件箱规则</span><span class="sxs-lookup"><span data-stu-id="cd671-115">Inbox rules</span></span>
<span data-ttu-id="cd671-116"><a name="bk_InboxRules"> </a></span><span class="sxs-lookup"><span data-stu-id="cd671-116"></span></span>

<span data-ttu-id="cd671-117">面对事实吧： 不是每个电子邮件创建相等。</span><span class="sxs-lookup"><span data-stu-id="cd671-117">Let's face it: not every email message is created equal.</span></span> <span data-ttu-id="cd671-118">对于从他/她的管理器中获取用户的每封电子邮件，没有从他/她加入年以前，但从未考虑到离开 Internet cat 视频通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="cd671-118">For every email a user gets from his or her manager, there's one from an Internet cat video distribution list he or she joined years ago and never got around to leaving.</span></span> <span data-ttu-id="cd671-119">有趣 Internet cat 视频时，可以轻松地在收件箱中的通讯组列表邮件 sea 丢失的通讯组列表获取可以变得的通信和重要邮件量。</span><span class="sxs-lookup"><span data-stu-id="cd671-119">While Internet cat videos are entertaining, the amount of traffic that distribution list gets can get out of hand, and important messages can easily be lost in the sea of distribution list mail in an Inbox.</span></span> <span data-ttu-id="cd671-120">许多用户到收件箱规则，以帮助减这些邮件中，打开，并使其收件箱多代码好地方。</span><span class="sxs-lookup"><span data-stu-id="cd671-120">Many users turn to Inbox rules to help pare down those messages, and make their Inbox a much nicer place to be.</span></span> <span data-ttu-id="cd671-121">使用 Exchange Web Services (EWS)，您的应用程序可以将承担的规则的功能引入。</span><span class="sxs-lookup"><span data-stu-id="cd671-121">With Exchange Web Services (EWS), your application can bring the power of rules to bear.</span></span>
  
<span data-ttu-id="cd671-122">EWS 托管 API 提供用于处理规则[ExchangeService.GetInboxRules](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.getinboxrules%28v=exchg.80%29.aspx)和[ExchangeService.UpdateInboxRules](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.updateinboxrules%28v=exchg.80%29.aspx)方法。</span><span class="sxs-lookup"><span data-stu-id="cd671-122">The EWS Managed API provides the [ExchangeService.GetInboxRules](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.getinboxrules%28v=exchg.80%29.aspx) and [ExchangeService.UpdateInboxRules](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.updateinboxrules%28v=exchg.80%29.aspx) methods for working with rules.</span></span> <span data-ttu-id="cd671-123">EWS 提供用于处理规则[GetInboxRules](http://msdn.microsoft.com/library/b4b2701a-4a23-4acc-8c75-19f7955ad7ae%28Office.15%29.aspx)和[UpdateInboxRules](http://msdn.microsoft.com/library/f982a237-471e-45c5-a2b5-468cfc53150b%28Office.15%29.aspx)操作。</span><span class="sxs-lookup"><span data-stu-id="cd671-123">EWS provides the [GetInboxRules](http://msdn.microsoft.com/library/b4b2701a-4a23-4acc-8c75-19f7955ad7ae%28Office.15%29.aspx) and [UpdateInboxRules](http://msdn.microsoft.com/library/f982a237-471e-45c5-a2b5-468cfc53150b%28Office.15%29.aspx) operations for working with rules.</span></span> <span data-ttu-id="cd671-124">但是，请注意，EWS 托管 API 和 EWS 有以下限制使用收件箱规则时：</span><span class="sxs-lookup"><span data-stu-id="cd671-124">However, note that the EWS Managed API and EWS have the following limitations when working with Inbox rules:</span></span> 
  
- <span data-ttu-id="cd671-125">EWS 无法访问或创建"仅限客户端"规则或运行"此计算机上只"在 Outlook 中设置的规则。</span><span class="sxs-lookup"><span data-stu-id="cd671-125">EWS cannot access or create "client-only" rules or rules that are set in Outlook to run "on this computer only".</span></span>
    
- <span data-ttu-id="cd671-126">若要使用 EWS 更改当前的规则集，您必须删除 Outlook 规则 BLOB，如果存在。</span><span class="sxs-lookup"><span data-stu-id="cd671-126">To change the current set of rules by using EWS, you have to remove the Outlook rules BLOB, if it is present.</span></span> <span data-ttu-id="cd671-127">这意味着，使用 EWS 修改规则删除将通过使用 Outlook 先前已关闭 （禁用） 的任何规则。</span><span class="sxs-lookup"><span data-stu-id="cd671-127">This means that using EWS to modify rules deletes any rules that were previously turned off (disabled) by using Outlook.</span></span> 
    
### <a name="how-do-rules-work"></a><span data-ttu-id="cd671-128">规则如何工作？</span><span class="sxs-lookup"><span data-stu-id="cd671-128">How do rules work?</span></span>
<span data-ttu-id="cd671-129"><a name="bk_HowRulesWork"> </a></span><span class="sxs-lookup"><span data-stu-id="cd671-129"></span></span>

<span data-ttu-id="cd671-130">规则引擎充当网关守卫到用户的邮箱。</span><span class="sxs-lookup"><span data-stu-id="cd671-130">The rules engine acts as a gatekeeper to a user's mailbox.</span></span> <span data-ttu-id="cd671-131">邮件到达用户的邮箱，但在收件箱中将显示以下消息之前，计算该邮件所依据的规则的一个已排序列表。</span><span class="sxs-lookup"><span data-stu-id="cd671-131">As a message arrives in the user's mailbox, but before the message appears in the Inbox, that message is evaluated against an ordered list of rules.</span></span> <span data-ttu-id="cd671-132">请注意，这仅会在到达时间，且只能在收件箱。</span><span class="sxs-lookup"><span data-stu-id="cd671-132">Note that this only occurs at arrival time, and only in the Inbox.</span></span> <span data-ttu-id="cd671-133">这些规则将由三个部分组成：[条件](#bk_Conditions)、[操作](#bk_Actions)和[例外](#bk_Exceptions)。</span><span class="sxs-lookup"><span data-stu-id="cd671-133">These rules are comprised of three parts: [Conditions](#bk_Conditions), [Actions](#bk_Actions), and [Exceptions](#bk_Exceptions).</span></span>
  
<span data-ttu-id="cd671-134">直至到达的规则列表末尾，从开始顶部的规则列表的规则，规则引擎执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="cd671-134">Starting with the rule at the top of the rule list, the rules engine performs the following steps until it reaches the end of the list of rules:</span></span>
  
1. <span data-ttu-id="cd671-135">检查邮件以确定其是否符合规则中指定的所有条件。</span><span class="sxs-lookup"><span data-stu-id="cd671-135">Checks the message to determine whether it meets all the conditions specified in the rule.</span></span>
    
1. <span data-ttu-id="cd671-136">如果符合所有条件，评估继续执行步骤 2。</span><span class="sxs-lookup"><span data-stu-id="cd671-136">If it meets all the conditions, evaluation continues with step 2.</span></span>
    
2. <span data-ttu-id="cd671-137">如果它不满足所有条件，则规则引擎加载规则列表中的下一个规则，并在第 1 步启动。</span><span class="sxs-lookup"><span data-stu-id="cd671-137">If it does not meet all the conditions, the rules engine loads the next rule in the rule list and starts over at step 1.</span></span>
    
2. <span data-ttu-id="cd671-138">检查邮件以确定是否满足任一规则中指定的例外。</span><span class="sxs-lookup"><span data-stu-id="cd671-138">Checks the message to determine whether it meets any of the exceptions specified in the rule.</span></span>
    
1. <span data-ttu-id="cd671-139">如果符合任何异常，规则引擎加载规则列表中的下一个规则，并在第 1 步启动。</span><span class="sxs-lookup"><span data-stu-id="cd671-139">If it meets any of the exceptions, the rules engine loads the next rule in the rule list and starts over at step 1.</span></span>
    
2. <span data-ttu-id="cd671-140">如果不满足任何异常，评估继续执行步骤 3。</span><span class="sxs-lookup"><span data-stu-id="cd671-140">If it does not meet any of the exceptions, evaluation continues with step 3.</span></span>
    
3. <span data-ttu-id="cd671-141">执行邮件在规则中指定的操作。</span><span class="sxs-lookup"><span data-stu-id="cd671-141">Performs the actions specified in the rule on the message.</span></span>
    
1. <span data-ttu-id="cd671-142">如果指定的"停止处理其他规则"操作，则规则引擎执行其他操作在的消息，然后退出而不计算邮件针对任何其他规则。</span><span class="sxs-lookup"><span data-stu-id="cd671-142">If the "stop processing more rules" action is specified, the rules engine performs all the other actions on the message, then exits without evaluating any additional rules against the message.</span></span>
    
2. <span data-ttu-id="cd671-143">如果未指定的"停止处理其他规则"操作，则规则引擎加载规则列表中的下一个规则，并在第 1 步启动。</span><span class="sxs-lookup"><span data-stu-id="cd671-143">If the "stop processing more rules" action is not specified, the rules engine loads the next rule in the rule list and starts over at step 1.</span></span>
    
<span data-ttu-id="cd671-144">下图显示了规则引擎下面的过程。</span><span class="sxs-lookup"><span data-stu-id="cd671-144">The following figure shows the process that the rules engine follows.</span></span>
  
<span data-ttu-id="cd671-145">**图 1： 规则引擎概述**</span><span class="sxs-lookup"><span data-stu-id="cd671-145">**Figure 1: Rules engine overview**</span></span>

![此图说明规则引擎使用的步骤：首先评估规则，然后确定是否满足规则条件，再执行操作或移动到下一个规则，直到完成。](media/Ex15_Rules_EngineOverview.png)
  
### <a name="putting-the-pieces-together---parts-of-a-rule"></a><span data-ttu-id="cd671-147">将部分放置在一起的部件的规则</span><span class="sxs-lookup"><span data-stu-id="cd671-147">Putting the pieces together - parts of a rule</span></span>
<span data-ttu-id="cd671-148"><a name="bk_Pieces"> </a></span><span class="sxs-lookup"><span data-stu-id="cd671-148"></span></span>

<span data-ttu-id="cd671-149">一种方法来可视化规则的部分是假设您向某人将您的传入电子邮件组织需要提供说明。</span><span class="sxs-lookup"><span data-stu-id="cd671-149">One way to visualize the parts of a rule is to imagine that you are giving instructions to someone who is tasked with organizing your incoming email.</span></span> <span data-ttu-id="cd671-150">您可能会向此人说:"时的邮件到达\<插入条件此处\>，执行\<插入操作此处\>，除非消息\<插入例外此处\>。</span><span class="sxs-lookup"><span data-stu-id="cd671-150">You might say to this person: "When a message arrives that \<insert conditions here\>, do \<insert actions here\>, unless the message \<insert exceptions here\>.</span></span> <span data-ttu-id="cd671-151">我们来看更详尽介绍了每个部件。</span><span class="sxs-lookup"><span data-stu-id="cd671-151">Let's take a closer look at each part.</span></span>
  
#### <a name="conditions"></a><span data-ttu-id="cd671-152">条件</span><span class="sxs-lookup"><span data-stu-id="cd671-152">Conditions</span></span>
<span data-ttu-id="cd671-153"><a name="bk_Conditions"> </a></span><span class="sxs-lookup"><span data-stu-id="cd671-153"></span></span>

<span data-ttu-id="cd671-154">[条件](http://msdn.microsoft.com/library/f049a48c-9585-43f7-8549-0b8cb19a5eea%28Office.15%29.aspx)描述应时应用规则。</span><span class="sxs-lookup"><span data-stu-id="cd671-154">[Conditions](http://msdn.microsoft.com/library/f049a48c-9585-43f7-8549-0b8cb19a5eea%28Office.15%29.aspx) describe when a rule should be applied.</span></span> <span data-ttu-id="cd671-155">时可以省略 （导致适用于每个收到邮件的规则） 的规则的条件，最多的很常见规则设置了适用于传入消息的子集的条件。</span><span class="sxs-lookup"><span data-stu-id="cd671-155">While you can omit the conditions of a rule (resulting in a rule that applies to every message received), it is far more common for rules to have conditions that apply to a subset of incoming messages.</span></span> <span data-ttu-id="cd671-156">一些示例是"时从 Sadie 是一条消息"或"当邮件发送到 Cat 视频情人通讯组列表"。</span><span class="sxs-lookup"><span data-stu-id="cd671-156">Some examples are "when a message is from Sadie" or "when a message is sent to the 'Cat Video Lovers' distribution list".</span></span> <span data-ttu-id="cd671-157">规则可以有多个条件。</span><span class="sxs-lookup"><span data-stu-id="cd671-157">Rules can have multiple conditions.</span></span> <span data-ttu-id="cd671-158">如果规则有多个条件，必须按顺序执行指定的操作的规则引擎满足所有条件。</span><span class="sxs-lookup"><span data-stu-id="cd671-158">When rules have more than one condition, all the conditions must be met in order for the rules engine to take the specified action.</span></span> 
  
#### <a name="actions"></a><span data-ttu-id="cd671-159">操作</span><span class="sxs-lookup"><span data-stu-id="cd671-159">Actions</span></span>
<span data-ttu-id="cd671-160"><a name="bk_Actions"> </a></span><span class="sxs-lookup"><span data-stu-id="cd671-160"></span></span>

<span data-ttu-id="cd671-161">[操作](http://msdn.microsoft.com/library/c5aa96b1-2d8b-422f-8c2f-f118572ab23f%28Office.15%29.aspx)描述应用规则时，会发生什么情况。</span><span class="sxs-lookup"><span data-stu-id="cd671-161">[Actions](http://msdn.microsoft.com/library/c5aa96b1-2d8b-422f-8c2f-f118572ab23f%28Office.15%29.aspx) describe what happens when a rule applies.</span></span> <span data-ttu-id="cd671-162">示例是"将邮件移动到猫文件夹"或者"为低重要性标记邮件"。</span><span class="sxs-lookup"><span data-stu-id="cd671-162">Examples are "move the message to the 'Cats' folder" or "mark the message with 'Low' importance".</span></span> <span data-ttu-id="cd671-163">规则可以有多个操作。</span><span class="sxs-lookup"><span data-stu-id="cd671-163">Rules can have multiple actions.</span></span> <span data-ttu-id="cd671-164">指定规则的多个操作时，应用该规则时执行所有操作。</span><span class="sxs-lookup"><span data-stu-id="cd671-164">When you specify multiple actions for a rule, all the actions are performed when the rule is applied.</span></span> 
  
#### <a name="exceptions"></a><span data-ttu-id="cd671-165">异常</span><span class="sxs-lookup"><span data-stu-id="cd671-165">Exceptions</span></span>
<span data-ttu-id="cd671-166"><a name="bk_Exceptions"> </a></span><span class="sxs-lookup"><span data-stu-id="cd671-166"></span></span>

<span data-ttu-id="cd671-167">[异常](http://msdn.microsoft.com/library/7cd63ac2-3441-4ed4-915b-6f90af4b28fc%28Office.15%29.aspx)描述时不应该应用规则，即使满足指定条件中的条件。</span><span class="sxs-lookup"><span data-stu-id="cd671-167">[Exceptions](http://msdn.microsoft.com/library/7cd63ac2-3441-4ed4-915b-6f90af4b28fc%28Office.15%29.aspx) describe when a rule should not apply, even if the criteria specified in the conditions are met.</span></span> <span data-ttu-id="cd671-168">例如，"除如果邮件仅发送给我"或"除如果邮件是从 Mom"。</span><span class="sxs-lookup"><span data-stu-id="cd671-168">Examples are "except if the message is sent only to me" or "except if the message is from Mom".</span></span> <span data-ttu-id="cd671-169">规则可以有多个例外项。</span><span class="sxs-lookup"><span data-stu-id="cd671-169">A rule can have multiple exceptions.</span></span> <span data-ttu-id="cd671-170">规则具有多个例外，以及任何异常满足时不应用该规则。</span><span class="sxs-lookup"><span data-stu-id="cd671-170">When rules have more than one exception, and any of the exceptions are met, the rule is not applied.</span></span> 
  
### <a name="example-herding-those-cats"></a><span data-ttu-id="cd671-171">示例： 收集这些猫</span><span class="sxs-lookup"><span data-stu-id="cd671-171">Example: Herding those cats</span></span>
<span data-ttu-id="cd671-172"><a name="bk_Example"> </a></span><span class="sxs-lookup"><span data-stu-id="cd671-172"></span></span>

<span data-ttu-id="cd671-173">我们来看看您的用户如何使用规则以消除从 Internet cat 视频通讯组列表的流量。</span><span class="sxs-lookup"><span data-stu-id="cd671-173">Let's take a look at how your users can use rules to eliminate the traffic from that Internet cat video distribution list.</span></span> <span data-ttu-id="cd671-174">我们假设以下各项：</span><span class="sxs-lookup"><span data-stu-id="cd671-174">Let's assume the following:</span></span>
  
- <span data-ttu-id="cd671-175">这些邮件发送到一个名为"Internet Cat 视频爱好者"的通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="cd671-175">These messages are sent to a distribution list called "Internet Cat Video Enthusiasts".</span></span>
    
- <span data-ttu-id="cd671-176">您的用户想要最终阅读这些消息，它们只是不希望他们会干扰其收件箱。</span><span class="sxs-lookup"><span data-stu-id="cd671-176">Your users want to read these messages eventually, they just don't want them cluttering their Inbox.</span></span> <span data-ttu-id="cd671-177">它们将而文件它们在名为"猫"的文件夹中。</span><span class="sxs-lookup"><span data-stu-id="cd671-177">They'd rather file them in a folder called "Cats".</span></span>
    
- <span data-ttu-id="cd671-178">您的用户想要读取立即，发送给此通讯组列表的母语消息，因为 Mom 发送有趣的视频。</span><span class="sxs-lookup"><span data-stu-id="cd671-178">Your users want to read messages sent to this distribution list by their mother right away, because Mom sends the funniest videos.</span></span>
    
<span data-ttu-id="cd671-179">这会告诉以下规则引擎:"的邮件时，它是到达发送到 Internet Cat 视频爱好者通讯组列表，将其移到猫文件夹，除非该邮件是从 Mom。"</span><span class="sxs-lookup"><span data-stu-id="cd671-179">This tells the rules engine the following: "When a message arrives that is sent to the 'Internet Cat Video Enthusiasts' distribution list, move it to the 'Cats' folder, unless the message is from Mom."</span></span> 
  
<span data-ttu-id="cd671-180">**表 2。规则定义**</span><span class="sxs-lookup"><span data-stu-id="cd671-180">**Table 2. Rule definition**</span></span>

|<span data-ttu-id="cd671-181">**规则部件**</span><span class="sxs-lookup"><span data-stu-id="cd671-181">**Rule part**</span></span>|<span data-ttu-id="cd671-182">**值**</span><span class="sxs-lookup"><span data-stu-id="cd671-182">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cd671-183">条件</span><span class="sxs-lookup"><span data-stu-id="cd671-183">Conditions</span></span>  <br/> |<span data-ttu-id="cd671-184">发送到 Internet Cat 视频爱好者通讯组列表</span><span class="sxs-lookup"><span data-stu-id="cd671-184">Sent to the 'Internet Cat Video Enthusiasts' distribution list</span></span>  <br/> |
|<span data-ttu-id="cd671-185">操作</span><span class="sxs-lookup"><span data-stu-id="cd671-185">Actions</span></span>  <br/> |<span data-ttu-id="cd671-186">将邮件移动到猫文件夹</span><span class="sxs-lookup"><span data-stu-id="cd671-186">Move the message to the 'Cats' folder</span></span>  <br/> <span data-ttu-id="cd671-187">和停止处理其他规则</span><span class="sxs-lookup"><span data-stu-id="cd671-187">AND stop processing more rules</span></span>  <br/> |
|<span data-ttu-id="cd671-188">异常</span><span class="sxs-lookup"><span data-stu-id="cd671-188">Exceptions</span></span>  <br/> |<span data-ttu-id="cd671-189">从 Mom</span><span class="sxs-lookup"><span data-stu-id="cd671-189">From 'Mom'</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="cd671-190">请注意，"停止处理其他规则"中的结果的规则操作之一。</span><span class="sxs-lookup"><span data-stu-id="cd671-190">Notice that "stop processing more rules" is one of the actions in the resulting rule.</span></span> <span data-ttu-id="cd671-191">通常最好包括此操作可避免的混淆通过该规则会在任何给定的消息。</span><span class="sxs-lookup"><span data-stu-id="cd671-191">In general it's a good idea to include this action to avoid confusion over which rules act on any given message.</span></span> <span data-ttu-id="cd671-192">但是，可以通过省略此操作，正确排序规则，获得更高级的处理的传入邮件。</span><span class="sxs-lookup"><span data-stu-id="cd671-192">However, by omitting this action and properly ordering your rules, you can achieve more advanced processing of your incoming mail.</span></span> <span data-ttu-id="cd671-193">在这种情况下，它可能是 Internet cat 视频邮件不妨碍高级处理得多需要安全匹配。</span><span class="sxs-lookup"><span data-stu-id="cd671-193">In this case, it's probably a safe bet that Internet cat video messages don't require much in the way of advanced processing.</span></span> 
  
<span data-ttu-id="cd671-194">创建此规则，不久新消息传入。</span><span class="sxs-lookup"><span data-stu-id="cd671-194">Shortly after creating this rule, a new message comes in.</span></span> <span data-ttu-id="cd671-195">同事希望向通讯组列表发送邮件。</span><span class="sxs-lookup"><span data-stu-id="cd671-195">A coworker Hope sends a message to the distribution list.</span></span> <span data-ttu-id="cd671-196">如果我们心理执行规则引擎的工作，邮件符合 （它发送到 Internet Cat 视频爱好者） 的所有条件，并且它都符合 none （不是从 Mom） 的例外，因此该规则适用和邮件获取移至猫文件夹。</span><span class="sxs-lookup"><span data-stu-id="cd671-196">If we mentally perform the work of the rules engine, the message meets all the conditions (it is sent to 'Internet Cat Videos Enthusiasts'), and it meets none of the exceptions (it isn't from 'Mom'), so the rule applies and the message gets moved to the 'Cats' folder.</span></span>
  
<span data-ttu-id="cd671-197">下图显示了如何对传入邮件应用规则。</span><span class="sxs-lookup"><span data-stu-id="cd671-197">The following figure shows how the rule is applied to an incoming mail message.</span></span>
  
<span data-ttu-id="cd671-198">**图 2。规则处理传入邮件**</span><span class="sxs-lookup"><span data-stu-id="cd671-198">**Figure 2. Incoming message is processed by a rule**</span></span>

![此说明显示同事发送到通讯组列表的新消息。此消息满足规则中定义的所有条件，且无任何异常，并且将移动到“Cats”文件夹。](media/Ex15_Rules_RuleEvaluationSample.png)
  
## <a name="blocking-senders"></a><span data-ttu-id="cd671-201">阻止发件人</span><span class="sxs-lookup"><span data-stu-id="cd671-201">Blocking senders</span></span>
<span data-ttu-id="cd671-202"><a name="bk_Blocking"> </a></span><span class="sxs-lookup"><span data-stu-id="cd671-202"></span></span>

<span data-ttu-id="cd671-203">尽管您可以创建移动的所有邮件来自特定发件人到垃圾邮件文件夹的规则，您也可以执行此操作使用垃圾邮件选项中阻止的发件人列表。</span><span class="sxs-lookup"><span data-stu-id="cd671-203">Although you can create a rule that will move all mail from a specific sender to the Junk Mail folder, you can also do this by using the Blocked Senders List in your Junk Email options.</span></span> <span data-ttu-id="cd671-204">因为没有限制用户可以具有多少规则，所以应该使用阻止发件人列表。</span><span class="sxs-lookup"><span data-stu-id="cd671-204">Because there is a limit to how many rules a user can have, it makes sense to use the Blocked Senders List.</span></span> <span data-ttu-id="cd671-205">可以通过使用[ExchangeService.MarkAsJunk](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.markasjunk%28v=exchg.80%29.aspx) EWS 托管 API 方法或[MarkAsJunk](http://msdn.microsoft.com/library/1f71f04d-56a9-4fee-a4e7-d1034438329e%28Office.15%29.aspx) EWS 操作来[添加或删除被阻止发件人名单的特定的电子邮件地址](how-to-add-and-remove-email-addresses-from-blocked-senders-list-by-using-ews.md)。</span><span class="sxs-lookup"><span data-stu-id="cd671-205">You can [add or remove specific email addresses from the Blocked Senders List](how-to-add-and-remove-email-addresses-from-blocked-senders-list-by-using-ews.md) by using the [ExchangeService.MarkAsJunk](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.markasjunk%28v=exchg.80%29.aspx) EWS Managed API method or the [MarkAsJunk](http://msdn.microsoft.com/library/1f71f04d-56a9-4fee-a4e7-d1034438329e%28Office.15%29.aspx) EWS operation.</span></span> <span data-ttu-id="cd671-206">请注意，在 EWS 以访问阻止发件人列表的顺序，用户邮箱必须包含电子邮件从要添加或删除的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="cd671-206">Note that in order for EWS to access the Blocked Senders List, the user's mailbox must contain an email message from the email address that you want to add or remove.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="cd671-207">本节内容</span><span class="sxs-lookup"><span data-stu-id="cd671-207">In this section</span></span>
<span data-ttu-id="cd671-208"><a name="bk_InThisSection"> </a></span><span class="sxs-lookup"><span data-stu-id="cd671-208"></span></span>

- [<span data-ttu-id="cd671-209">使用 EWS 在 Exchange 管理收件箱规则</span><span class="sxs-lookup"><span data-stu-id="cd671-209">Manage Inbox rules by using EWS in Exchange</span></span>](how-to-manage-inbox-rules-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="cd671-210">添加并在 Exchange 使用 EWS 从阻止发件人列表中删除电子邮件地址</span><span class="sxs-lookup"><span data-stu-id="cd671-210">Add and remove email addresses from the Blocked Senders List by using EWS in Exchange</span></span>](how-to-add-and-remove-email-addresses-from-blocked-senders-list-by-using-ews.md)
    
## <a name="see-also"></a><span data-ttu-id="cd671-211">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cd671-211">See also</span></span>


- [<span data-ttu-id="cd671-212">开发 Exchange Web 服务客户端</span><span class="sxs-lookup"><span data-stu-id="cd671-212">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    
- [<span data-ttu-id="cd671-213">GetInboxRules 操作</span><span class="sxs-lookup"><span data-stu-id="cd671-213">GetInboxRules operation</span></span>](http://msdn.microsoft.com/library/b4b2701a-4a23-4acc-8c75-19f7955ad7ae%28Office.15%29.aspx)
    
- [<span data-ttu-id="cd671-214">UpdateInboxRules 操作</span><span class="sxs-lookup"><span data-stu-id="cd671-214">UpdateInboxRules operation</span></span>](http://msdn.microsoft.com/library/f982a237-471e-45c5-a2b5-468cfc53150b%28Office.15%29.aspx)
    
- [<span data-ttu-id="cd671-215">MarkAsJunk 操作</span><span class="sxs-lookup"><span data-stu-id="cd671-215">MarkAsJunk operation</span></span>](http://msdn.microsoft.com/library/1f71f04d-56a9-4fee-a4e7-d1034438329e%28Office.15%29.aspx)
    

