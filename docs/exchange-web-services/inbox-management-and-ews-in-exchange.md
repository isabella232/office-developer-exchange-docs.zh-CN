---
title: Inbox management and EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3dfa0fc9-64bb-4d18-bff7-bf6b3bed4a0d
description: 了解如何通过使用收件箱规则和阻止发件人列表来管理 EWS 托管 API 或 EWS 应用程序中的收件箱。
ms.openlocfilehash: 7c88015386dc882f14184765e0046a866e8c0e10
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456311"
---
# <a name="inbox-management-and-ews-in-exchange"></a><span data-ttu-id="cdf8c-103">Inbox management and EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="cdf8c-103">Inbox management and EWS in Exchange</span></span>

<span data-ttu-id="cdf8c-104">了解如何通过使用收件箱规则和阻止发件人列表来管理 EWS 托管 API 或 EWS 应用程序中的收件箱。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-104">Find out how you can manage your Inbox in your EWS Managed API or EWS application by using Inbox rules and the blocked senders list.</span></span>
  
<span data-ttu-id="cdf8c-105">Exchange 邮箱附带功能，可帮助用户自动组织传入邮件。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-105">Exchange mailboxes come equipped with features to help users organize their incoming mail automatically.</span></span> <span data-ttu-id="cdf8c-106">这些功能都在服务器上运行，无需用户干预，但它们满足不同的需求。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-106">These features all operate on the server without user intervention, but they serve different needs.</span></span> <span data-ttu-id="cdf8c-107">EWS 托管 API 和 EWS 提供了对这些功能的访问权限，使用户可以管理其收件箱。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-107">The EWS Managed API and EWS provide access to these features, enabling your users to manage their Inboxes.</span></span>
  
<span data-ttu-id="cdf8c-108">**表1。收件箱管理功能**</span><span class="sxs-lookup"><span data-stu-id="cdf8c-108">**Table 1. Inbox management features**</span></span>

|<span data-ttu-id="cdf8c-109">**如果您想要 .。。**</span><span class="sxs-lookup"><span data-stu-id="cdf8c-109">**If you want to…**</span></span>|<span data-ttu-id="cdf8c-110">**使用 .。。**</span><span class="sxs-lookup"><span data-stu-id="cdf8c-110">**Use…**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cdf8c-111">根据特定条件（如发件人、主题或附件）对传入邮件执行操作（例如将其移动到其他文件夹或将其删除）</span><span class="sxs-lookup"><span data-stu-id="cdf8c-111">Take action on incoming messages (such as moving them to another folder or deleting them) based on specific criteria (such as sender, subject, or attachments)</span></span>  <br/> |<span data-ttu-id="cdf8c-112">收件箱规则</span><span class="sxs-lookup"><span data-stu-id="cdf8c-112">Inbox rules</span></span>  <br/> |
|<span data-ttu-id="cdf8c-113">删除来自特定发件人的所有传入邮件</span><span class="sxs-lookup"><span data-stu-id="cdf8c-113">Delete all incoming mail from a particular sender</span></span>  <br/> |<span data-ttu-id="cdf8c-114">阻止发件人列表</span><span class="sxs-lookup"><span data-stu-id="cdf8c-114">Blocked Senders List</span></span>  <br/> |
   
## <a name="inbox-rules"></a><span data-ttu-id="cdf8c-115">收件箱规则</span><span class="sxs-lookup"><span data-stu-id="cdf8c-115">Inbox rules</span></span>
<span data-ttu-id="cdf8c-116"><a name="bk_InboxRules"> </a></span><span class="sxs-lookup"><span data-stu-id="cdf8c-116"><a name="bk_InboxRules"> </a></span></span>

<span data-ttu-id="cdf8c-117">让我们面对 it：并不是每封电子邮件的创建都相等。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-117">Let's face it: not every email message is created equal.</span></span> <span data-ttu-id="cdf8c-118">对于用户从其经理那里获得的每封电子邮件，从 Internet cat 视频通讯组列表中有一个，他或她以前加入了几年，而从未收到离开。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-118">For every email a user gets from his or her manager, there's one from an Internet cat video distribution list he or she joined years ago and never got around to leaving.</span></span> <span data-ttu-id="cdf8c-119">尽管 Internet cat 视频非常有趣，但通讯组列表获取的流量可能已过期，并且在收件箱中通讯组列表邮件的海洋中可以很容易地丢失重要邮件。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-119">While Internet cat videos are entertaining, the amount of traffic that distribution list gets can get out of hand, and important messages can easily be lost in the sea of distribution list mail in an Inbox.</span></span> <span data-ttu-id="cdf8c-120">许多用户会转到收件箱规则，帮助 pare 这些邮件，并使其收件箱地利用的位置变得很多。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-120">Many users turn to Inbox rules to help pare down those messages, and make their Inbox a much nicer place to be.</span></span> <span data-ttu-id="cdf8c-121">通过 Exchange Web 服务（EWS），应用程序可以让规则的强大功能得以承受。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-121">With Exchange Web Services (EWS), your application can bring the power of rules to bear.</span></span>
  
<span data-ttu-id="cdf8c-122">EWS 托管 API 提供用于处理规则的[GetInboxRules](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getinboxrules%28v=exchg.80%29.aspx)和[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.updateinboxrules%28v=exchg.80%29.aspx)方法。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-122">The EWS Managed API provides the [ExchangeService.GetInboxRules](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getinboxrules%28v=exchg.80%29.aspx) and [ExchangeService.UpdateInboxRules](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.updateinboxrules%28v=exchg.80%29.aspx) methods for working with rules.</span></span> <span data-ttu-id="cdf8c-123">EWS 提供用于处理规则的[GetInboxRules](https://msdn.microsoft.com/library/b4b2701a-4a23-4acc-8c75-19f7955ad7ae%28Office.15%29.aspx)和[UpdateInboxRules](https://msdn.microsoft.com/library/f982a237-471e-45c5-a2b5-468cfc53150b%28Office.15%29.aspx)操作。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-123">EWS provides the [GetInboxRules](https://msdn.microsoft.com/library/b4b2701a-4a23-4acc-8c75-19f7955ad7ae%28Office.15%29.aspx) and [UpdateInboxRules](https://msdn.microsoft.com/library/f982a237-471e-45c5-a2b5-468cfc53150b%28Office.15%29.aspx) operations for working with rules.</span></span> <span data-ttu-id="cdf8c-124">但是，请注意，在使用收件箱规则时，EWS 托管 API 和 EWS 具有以下限制：</span><span class="sxs-lookup"><span data-stu-id="cdf8c-124">However, note that the EWS Managed API and EWS have the following limitations when working with Inbox rules:</span></span> 
  
- <span data-ttu-id="cdf8c-125">EWS 无法访问或创建 "仅客户端" 规则或在 Outlook 中设置为 "仅在此计算机上运行" 的规则。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-125">EWS cannot access or create "client-only" rules or rules that are set in Outlook to run "on this computer only".</span></span>
    
- <span data-ttu-id="cdf8c-126">若要使用 EWS 更改当前的一组规则，必须删除 Outlook 规则 BLOB （如果存在）。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-126">To change the current set of rules by using EWS, you have to remove the Outlook rules BLOB, if it is present.</span></span> <span data-ttu-id="cdf8c-127">这意味着，使用 EWS 修改规则将删除以前使用 Outlook 关闭（禁用）的任何规则。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-127">This means that using EWS to modify rules deletes any rules that were previously turned off (disabled) by using Outlook.</span></span> 
    
### <a name="how-do-rules-work"></a><span data-ttu-id="cdf8c-128">规则的工作原理</span><span class="sxs-lookup"><span data-stu-id="cdf8c-128">How do rules work?</span></span>
<span data-ttu-id="cdf8c-129"><a name="bk_HowRulesWork"> </a></span><span class="sxs-lookup"><span data-stu-id="cdf8c-129"><a name="bk_HowRulesWork"> </a></span></span>

<span data-ttu-id="cdf8c-130">规则引擎充当用户邮箱的网关守卫。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-130">The rules engine acts as a gatekeeper to a user's mailbox.</span></span> <span data-ttu-id="cdf8c-131">当邮件到达用户的邮箱，但在收件箱中显示该邮件之前，将根据规则的排序列表对该邮件进行评估。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-131">As a message arrives in the user's mailbox, but before the message appears in the Inbox, that message is evaluated against an ordered list of rules.</span></span> <span data-ttu-id="cdf8c-132">请注意，这仅发生在到达时，并且仅发生在收件箱中。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-132">Note that this only occurs at arrival time, and only in the Inbox.</span></span> <span data-ttu-id="cdf8c-133">这些规则由三部分组成：[条件](#bk_Conditions)、[操作](#bk_Actions)和[例外](#bk_Exceptions)。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-133">These rules are comprised of three parts: [Conditions](#bk_Conditions), [Actions](#bk_Actions), and [Exceptions](#bk_Exceptions).</span></span>
  
<span data-ttu-id="cdf8c-134">从规则列表顶部的规则开始，规则引擎将执行以下步骤，直至到达规则列表的末尾：</span><span class="sxs-lookup"><span data-stu-id="cdf8c-134">Starting with the rule at the top of the rule list, the rules engine performs the following steps until it reaches the end of the list of rules:</span></span>
  
1. <span data-ttu-id="cdf8c-135">检查邮件以确定它是否符合规则中指定的所有条件。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-135">Checks the message to determine whether it meets all the conditions specified in the rule.</span></span>
    
1. <span data-ttu-id="cdf8c-136">如果它满足所有条件，请继续执行步骤2评估。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-136">If it meets all the conditions, evaluation continues with step 2.</span></span>
    
2. <span data-ttu-id="cdf8c-137">如果它不符合所有条件，规则引擎将加载规则列表中的下一个规则，然后在步骤1中启动。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-137">If it does not meet all the conditions, the rules engine loads the next rule in the rule list and starts over at step 1.</span></span>
    
2. <span data-ttu-id="cdf8c-138">检查邮件以确定它是否符合规则中指定的任何例外。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-138">Checks the message to determine whether it meets any of the exceptions specified in the rule.</span></span>
    
1. <span data-ttu-id="cdf8c-139">如果它满足任何例外，规则引擎将加载规则列表中的下一个规则，然后在步骤1中启动。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-139">If it meets any of the exceptions, the rules engine loads the next rule in the rule list and starts over at step 1.</span></span>
    
2. <span data-ttu-id="cdf8c-140">如果它不符合任何例外，请继续执行步骤3评估。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-140">If it does not meet any of the exceptions, evaluation continues with step 3.</span></span>
    
3. <span data-ttu-id="cdf8c-141">对邮件执行规则中指定的操作。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-141">Performs the actions specified in the rule on the message.</span></span>
    
1. <span data-ttu-id="cdf8c-142">如果指定了 "停止处理更多规则" 操作，规则引擎将对邮件执行所有其他操作，然后退出而不评估邮件的任何其他规则。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-142">If the "stop processing more rules" action is specified, the rules engine performs all the other actions on the message, then exits without evaluating any additional rules against the message.</span></span>
    
2. <span data-ttu-id="cdf8c-143">如果未指定 "停止处理更多规则" 操作，规则引擎将加载规则列表中的下一个规则，然后在步骤1中启动。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-143">If the "stop processing more rules" action is not specified, the rules engine loads the next rule in the rule list and starts over at step 1.</span></span>
    
<span data-ttu-id="cdf8c-144">下图显示规则引擎遵循的过程。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-144">The following figure shows the process that the rules engine follows.</span></span>
  
<span data-ttu-id="cdf8c-145">**图1：规则引擎概述**</span><span class="sxs-lookup"><span data-stu-id="cdf8c-145">**Figure 1: Rules engine overview**</span></span>

![此图说明规则引擎使用的步骤：首先评估规则，然后确定是否满足规则条件，再执行操作或移动到下一个规则，直到完成。](media/Ex15_Rules_EngineOverview.png)
  
### <a name="putting-the-pieces-together---parts-of-a-rule"></a><span data-ttu-id="cdf8c-147">将组成部分放在一起-规则的各个部分</span><span class="sxs-lookup"><span data-stu-id="cdf8c-147">Putting the pieces together - parts of a rule</span></span>
<span data-ttu-id="cdf8c-148"><a name="bk_Pieces"> </a></span><span class="sxs-lookup"><span data-stu-id="cdf8c-148"><a name="bk_Pieces"> </a></span></span>

<span data-ttu-id="cdf8c-149">可视化规则的各个部分的一种方法是假设您向负责组织传入电子邮件的人员提供说明。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-149">One way to visualize the parts of a rule is to imagine that you are giving instructions to someone who is tasked with organizing your incoming email.</span></span> <span data-ttu-id="cdf8c-150">您可以向此人说： "当邮件到达时" \<insert conditions here\> ，则 \<insert actions here\> 除非邮件 \<insert exceptions here\> 。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-150">You might say to this person: "When a message arrives that \<insert conditions here\>, do \<insert actions here\>, unless the message \<insert exceptions here\>.</span></span> <span data-ttu-id="cdf8c-151">让我们进一步了解每个部分。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-151">Let's take a closer look at each part.</span></span>
  
#### <a name="conditions"></a><span data-ttu-id="cdf8c-152">条件</span><span class="sxs-lookup"><span data-stu-id="cdf8c-152">Conditions</span></span>
<span data-ttu-id="cdf8c-153"><a name="bk_Conditions"> </a></span><span class="sxs-lookup"><span data-stu-id="cdf8c-153"><a name="bk_Conditions"> </a></span></span>

<span data-ttu-id="cdf8c-154">[条件](https://msdn.microsoft.com/library/f049a48c-9585-43f7-8549-0b8cb19a5eea%28Office.15%29.aspx)描述应何时应用规则。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-154">[Conditions](https://msdn.microsoft.com/library/f049a48c-9585-43f7-8549-0b8cb19a5eea%28Office.15%29.aspx) describe when a rule should be applied.</span></span> <span data-ttu-id="cdf8c-155">虽然您可以省略规则的条件（结果是应用于每个收到的邮件的规则），但对于规则而言，有一些条件适用于传入邮件的子集更常见。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-155">While you can omit the conditions of a rule (resulting in a rule that applies to every message received), it is far more common for rules to have conditions that apply to a subset of incoming messages.</span></span> <span data-ttu-id="cdf8c-156">一些示例包括 "当邮件来自 Sadie" 或 "当邮件发送到 ' Cat Video Lovers 更改 ' 通讯组列表 ' 时"。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-156">Some examples are "when a message is from Sadie" or "when a message is sent to the 'Cat Video Lovers' distribution list".</span></span> <span data-ttu-id="cdf8c-157">规则可以有多个条件。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-157">Rules can have multiple conditions.</span></span> <span data-ttu-id="cdf8c-158">当规则具有多个条件时，必须满足所有条件，规则引擎才能执行指定的操作。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-158">When rules have more than one condition, all the conditions must be met in order for the rules engine to take the specified action.</span></span> 
  
#### <a name="actions"></a><span data-ttu-id="cdf8c-159">操作</span><span class="sxs-lookup"><span data-stu-id="cdf8c-159">Actions</span></span>
<span data-ttu-id="cdf8c-160"><a name="bk_Actions"> </a></span><span class="sxs-lookup"><span data-stu-id="cdf8c-160"><a name="bk_Actions"> </a></span></span>

<span data-ttu-id="cdf8c-161">[操作](https://msdn.microsoft.com/library/c5aa96b1-2d8b-422f-8c2f-f118572ab23f%28Office.15%29.aspx)描述应用规则时所发生的情况。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-161">[Actions](https://msdn.microsoft.com/library/c5aa96b1-2d8b-422f-8c2f-f118572ab23f%28Office.15%29.aspx) describe what happens when a rule applies.</span></span> <span data-ttu-id="cdf8c-162">例如 "将邮件移动到 ' 猫 ' 文件夹" 或 "使用 ' 重要性 ' 较低的邮件标记"。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-162">Examples are "move the message to the 'Cats' folder" or "mark the message with 'Low' importance".</span></span> <span data-ttu-id="cdf8c-163">规则可以有多个操作。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-163">Rules can have multiple actions.</span></span> <span data-ttu-id="cdf8c-164">当您为某个规则指定多个操作时，将在应用该规则时执行所有操作。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-164">When you specify multiple actions for a rule, all the actions are performed when the rule is applied.</span></span> 
  
#### <a name="exceptions"></a><span data-ttu-id="cdf8c-165">异常</span><span class="sxs-lookup"><span data-stu-id="cdf8c-165">Exceptions</span></span>
<span data-ttu-id="cdf8c-166"><a name="bk_Exceptions"> </a></span><span class="sxs-lookup"><span data-stu-id="cdf8c-166"><a name="bk_Exceptions"> </a></span></span>

<span data-ttu-id="cdf8c-167">[异常](https://msdn.microsoft.com/library/7cd63ac2-3441-4ed4-915b-6f90af4b28fc%28Office.15%29.aspx)描述规则不应应用的时间，即使满足条件中指定的条件也是如此。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-167">[Exceptions](https://msdn.microsoft.com/library/7cd63ac2-3441-4ed4-915b-6f90af4b28fc%28Office.15%29.aspx) describe when a rule should not apply, even if the criteria specified in the conditions are met.</span></span> <span data-ttu-id="cdf8c-168">例如，"仅将邮件发送给我" 或 "邮件来自 Mom" 时除外。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-168">Examples are "except if the message is sent only to me" or "except if the message is from Mom".</span></span> <span data-ttu-id="cdf8c-169">一个规则可以有多个例外。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-169">A rule can have multiple exceptions.</span></span> <span data-ttu-id="cdf8c-170">如果规则具有多个异常，并且满足了任何异常，则不会应用该规则。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-170">When rules have more than one exception, and any of the exceptions are met, the rule is not applied.</span></span> 
  
### <a name="example-herding-those-cats"></a><span data-ttu-id="cdf8c-171">示例： Herding 这些猫</span><span class="sxs-lookup"><span data-stu-id="cdf8c-171">Example: Herding those cats</span></span>
<span data-ttu-id="cdf8c-172"><a name="bk_Example"> </a></span><span class="sxs-lookup"><span data-stu-id="cdf8c-172"><a name="bk_Example"> </a></span></span>

<span data-ttu-id="cdf8c-173">我们来看看您的用户如何使用规则来消除来自该 Internet cat 视频通讯组列表的流量。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-173">Let's take a look at how your users can use rules to eliminate the traffic from that Internet cat video distribution list.</span></span> <span data-ttu-id="cdf8c-174">让我们假定以下内容：</span><span class="sxs-lookup"><span data-stu-id="cdf8c-174">Let's assume the following:</span></span>
  
- <span data-ttu-id="cdf8c-175">这些邮件将被发送到名为 "Internet Cat Video 爱好者" 的通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-175">These messages are sent to a distribution list called "Internet Cat Video Enthusiasts".</span></span>
    
- <span data-ttu-id="cdf8c-176">您的用户希望最终阅读这些邮件，它们只是不希望他们打乱其收件箱。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-176">Your users want to read these messages eventually, they just don't want them cluttering their Inbox.</span></span> <span data-ttu-id="cdf8c-177">而是将其文件放在名为 "猫" 的文件夹中。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-177">They'd rather file them in a folder called "Cats".</span></span>
    
- <span data-ttu-id="cdf8c-178">您的用户希望立即阅读通过其母亲发送到此通讯组列表的邮件，因为 Mom 发送 funniest 视频。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-178">Your users want to read messages sent to this distribution list by their mother right away, because Mom sends the funniest videos.</span></span>
    
<span data-ttu-id="cdf8c-179">这将告知规则引擎以下内容： "当邮件到达时发送到 ' Internet Cat 视频爱好者 ' 通讯组 ' 列表时，请将其移至" 猫 "文件夹，除非邮件来自 Mom。"</span><span class="sxs-lookup"><span data-stu-id="cdf8c-179">This tells the rules engine the following: "When a message arrives that is sent to the 'Internet Cat Video Enthusiasts' distribution list, move it to the 'Cats' folder, unless the message is from Mom."</span></span> 
  
<span data-ttu-id="cdf8c-180">**表2。规则定义**</span><span class="sxs-lookup"><span data-stu-id="cdf8c-180">**Table 2. Rule definition**</span></span>

|<span data-ttu-id="cdf8c-181">**规则部件**</span><span class="sxs-lookup"><span data-stu-id="cdf8c-181">**Rule part**</span></span>|<span data-ttu-id="cdf8c-182">**值**</span><span class="sxs-lookup"><span data-stu-id="cdf8c-182">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cdf8c-183">条件</span><span class="sxs-lookup"><span data-stu-id="cdf8c-183">Conditions</span></span>  <br/> |<span data-ttu-id="cdf8c-184">发送到 "Internet Cat 视频爱好者" 通讯组列表</span><span class="sxs-lookup"><span data-stu-id="cdf8c-184">Sent to the 'Internet Cat Video Enthusiasts' distribution list</span></span>  <br/> |
|<span data-ttu-id="cdf8c-185">操作</span><span class="sxs-lookup"><span data-stu-id="cdf8c-185">Actions</span></span>  <br/> |<span data-ttu-id="cdf8c-186">将邮件移动到 "猫" 文件夹</span><span class="sxs-lookup"><span data-stu-id="cdf8c-186">Move the message to the 'Cats' folder</span></span>  <br/> <span data-ttu-id="cdf8c-187">并停止处理更多规则</span><span class="sxs-lookup"><span data-stu-id="cdf8c-187">AND stop processing more rules</span></span>  <br/> |
|<span data-ttu-id="cdf8c-188">异常</span><span class="sxs-lookup"><span data-stu-id="cdf8c-188">Exceptions</span></span>  <br/> |<span data-ttu-id="cdf8c-189">从 "Mom"</span><span class="sxs-lookup"><span data-stu-id="cdf8c-189">From 'Mom'</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="cdf8c-190">请注意，"停止处理更多规则" 是结果规则中的操作之一。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-190">Notice that "stop processing more rules" is one of the actions in the resulting rule.</span></span> <span data-ttu-id="cdf8c-191">通常，最好将此操作包括在内，以避免因规则对任何给定的邮件起作用而产生困惑。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-191">In general it's a good idea to include this action to avoid confusion over which rules act on any given message.</span></span> <span data-ttu-id="cdf8c-192">但是，通过省略此操作并正确地对规则进行排序，可以实现对传入邮件的更高级处理。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-192">However, by omitting this action and properly ordering your rules, you can achieve more advanced processing of your incoming mail.</span></span> <span data-ttu-id="cdf8c-193">在这种情况下，可能是因为 Internet cat 视频邮件不需要很多高级处理方式。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-193">In this case, it's probably a safe bet that Internet cat video messages don't require much in the way of advanced processing.</span></span> 
  
<span data-ttu-id="cdf8c-194">在创建此规则后不久，将会收到一封新邮件。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-194">Shortly after creating this rule, a new message comes in.</span></span> <span data-ttu-id="cdf8c-195">同事希望向通讯组列表发送一封邮件。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-195">A coworker Hope sends a message to the distribution list.</span></span> <span data-ttu-id="cdf8c-196">如果我们 mentally 执行规则引擎的工作，则邮件将满足所有条件（它将发送到 "Internet Cat 视频爱好者"），并且不会满足任何例外（不是来自 "Mom"），因此规则将应用并将邮件移动到 "猫" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-196">If we mentally perform the work of the rules engine, the message meets all the conditions (it is sent to 'Internet Cat Videos Enthusiasts'), and it meets none of the exceptions (it isn't from 'Mom'), so the rule applies and the message gets moved to the 'Cats' folder.</span></span>
  
<span data-ttu-id="cdf8c-197">下图显示了如何将规则应用于传入邮件。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-197">The following figure shows how the rule is applied to an incoming mail message.</span></span>
  
<span data-ttu-id="cdf8c-198">**图2。传入邮件由规则处理**</span><span class="sxs-lookup"><span data-stu-id="cdf8c-198">**Figure 2. Incoming message is processed by a rule**</span></span>

![此说明显示同事发送到通讯组列表的新消息。此消息满足规则中定义的所有条件，且无任何异常，并且将移动到“Cats”文件夹。](media/Ex15_Rules_RuleEvaluationSample.png)
  
## <a name="blocking-senders"></a><span data-ttu-id="cdf8c-201">阻止发件人</span><span class="sxs-lookup"><span data-stu-id="cdf8c-201">Blocking senders</span></span>
<span data-ttu-id="cdf8c-202"><a name="bk_Blocking"> </a></span><span class="sxs-lookup"><span data-stu-id="cdf8c-202"><a name="bk_Blocking"> </a></span></span>

<span data-ttu-id="cdf8c-203">虽然您可以创建将来自特定发件人的所有邮件移动到 "垃圾邮件" 文件夹的规则，但您也可以通过使用 "垃圾邮件" 选项中的阻止发件人列表来执行此操作。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-203">Although you can create a rule that will move all mail from a specific sender to the Junk Mail folder, you can also do this by using the Blocked Senders List in your Junk Email options.</span></span> <span data-ttu-id="cdf8c-204">由于用户可以拥有的规则数有限制，因此使用阻止的发件人列表很有意义。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-204">Because there is a limit to how many rules a user can have, it makes sense to use the Blocked Senders List.</span></span> <span data-ttu-id="cdf8c-205">您可以使用[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.markasjunk%28v=exchg.80%29.aspx) EWS 托管 API 方法或[MarkAsJunk](https://msdn.microsoft.com/library/1f71f04d-56a9-4fee-a4e7-d1034438329e%28Office.15%29.aspx) Ews 操作在[阻止发件人列表中添加或删除特定的电子邮件地址](how-to-add-and-remove-email-addresses-from-blocked-senders-list-by-using-ews.md)。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-205">You can [add or remove specific email addresses from the Blocked Senders List](how-to-add-and-remove-email-addresses-from-blocked-senders-list-by-using-ews.md) by using the [ExchangeService.MarkAsJunk](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.markasjunk%28v=exchg.80%29.aspx) EWS Managed API method or the [MarkAsJunk](https://msdn.microsoft.com/library/1f71f04d-56a9-4fee-a4e7-d1034438329e%28Office.15%29.aspx) EWS operation.</span></span> <span data-ttu-id="cdf8c-206">请注意，为了使 EWS 能够访问阻止的发件人列表，用户的邮箱必须包含来自您要添加或删除的电子邮件地址的电子邮件。</span><span class="sxs-lookup"><span data-stu-id="cdf8c-206">Note that in order for EWS to access the Blocked Senders List, the user's mailbox must contain an email message from the email address that you want to add or remove.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="cdf8c-207">本节内容</span><span class="sxs-lookup"><span data-stu-id="cdf8c-207">In this section</span></span>
<span data-ttu-id="cdf8c-208"><a name="bk_InThisSection"> </a></span><span class="sxs-lookup"><span data-stu-id="cdf8c-208"><a name="bk_InThisSection"> </a></span></span>

- [<span data-ttu-id="cdf8c-209">使用 Exchange 中的 EWS 管理收件箱规则</span><span class="sxs-lookup"><span data-stu-id="cdf8c-209">Manage Inbox rules by using EWS in Exchange</span></span>](how-to-manage-inbox-rules-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="cdf8c-210">使用 Exchange 中的 EWS 在阻止的发件人列表中添加和删除电子邮件地址</span><span class="sxs-lookup"><span data-stu-id="cdf8c-210">Add and remove email addresses from the Blocked Senders List by using EWS in Exchange</span></span>](how-to-add-and-remove-email-addresses-from-blocked-senders-list-by-using-ews.md)
    
## <a name="see-also"></a><span data-ttu-id="cdf8c-211">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cdf8c-211">See also</span></span>


- [<span data-ttu-id="cdf8c-212">开发 Exchange Web 服务客户端</span><span class="sxs-lookup"><span data-stu-id="cdf8c-212">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    
- [<span data-ttu-id="cdf8c-213">GetInboxRules 操作</span><span class="sxs-lookup"><span data-stu-id="cdf8c-213">GetInboxRules operation</span></span>](https://msdn.microsoft.com/library/b4b2701a-4a23-4acc-8c75-19f7955ad7ae%28Office.15%29.aspx)
    
- [<span data-ttu-id="cdf8c-214">UpdateInboxRules 操作</span><span class="sxs-lookup"><span data-stu-id="cdf8c-214">UpdateInboxRules operation</span></span>](https://msdn.microsoft.com/library/f982a237-471e-45c5-a2b5-468cfc53150b%28Office.15%29.aspx)
    
- [<span data-ttu-id="cdf8c-215">MarkAsJunk 操作</span><span class="sxs-lookup"><span data-stu-id="cdf8c-215">MarkAsJunk operation</span></span>](https://msdn.microsoft.com/library/1f71f04d-56a9-4fee-a4e7-d1034438329e%28Office.15%29.aspx)
    

