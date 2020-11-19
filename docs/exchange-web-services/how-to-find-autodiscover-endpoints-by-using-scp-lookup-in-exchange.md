---
title: 使用 Exchange 中的“SCP 查找”来找到自动发现终结点
manager: kelbow
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: b24228a8-5127-4bac-aef0-9c9e8843c9ff
description: 了解如何在 Active Directory 域服务 (AD DS) 中找到自动发现 SCP 对象并用它们来查找要用于 Exchange 自动发现服务的自动发现终结点 URL。
localization_priority: Priority
ms.openlocfilehash: 5468c18b6d614016915c292c2e02c1a4b570ae37
ms.sourcegitcommit: 37d4ecd4f469690ba1de87baad2f2f58c40c96ba
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49348806"
---
# <a name="find-autodiscover-endpoints-by-using-scp-lookup-in-exchange"></a><span data-ttu-id="e9251-103">使用 Exchange 中的“SCP 查找”来找到自动发现终结点</span><span class="sxs-lookup"><span data-stu-id="e9251-103">Find Autodiscover endpoints by using SCP lookup in Exchange</span></span>

<span data-ttu-id="e9251-104">了解如何在 Active Directory 域服务 (AD DS) 中找到自动发现 SCP 对象并用它们来查找要用于 Exchange 自动发现服务的自动发现终结点 URL。</span><span class="sxs-lookup"><span data-stu-id="e9251-104">Find out how to locate Autodiscover SCP objects in Active Directory Domain Services (AD DS) and use them to find Autodiscover endpoint URLs to use with the Exchange Autodiscover service.</span></span>
  
<span data-ttu-id="e9251-105">借助自动发现功能，可轻松检索连接到 Exchange 服务器上的邮箱所需的信息。</span><span class="sxs-lookup"><span data-stu-id="e9251-105">Autodiscover makes it easy to retrieve information that you need to connect to mailboxes on Exchange servers.</span></span> <span data-ttu-id="e9251-106">但若要使用自动发现功能，你需要一种方式来查找适用于你正在检索其设置的用户的自动发现服务。</span><span class="sxs-lookup"><span data-stu-id="e9251-106">However, in order to use Autodiscover, you need a way to find Autodiscover servers that are appropriate for the user you're retrieving settings for.</span></span> <span data-ttu-id="e9251-107">AD DS 中的服务连接点 (SCP) 对象为加入域的客户端提供了一种简单的方法来查找自动发现服务器。</span><span class="sxs-lookup"><span data-stu-id="e9251-107">Service connection point (SCP) objects in AD DS provide an easy way for domain-joined clients to look up Autodiscover servers.</span></span> 
  
## <a name="get-set-up-to-find-autodiscover-endpoints"></a><span data-ttu-id="e9251-108">进行设置来查找自动发现终结点</span><span class="sxs-lookup"><span data-stu-id="e9251-108">Get set up to find Autodiscover endpoints</span></span>
<span data-ttu-id="e9251-109"><a name="bk_PreReqs"> </a></span><span class="sxs-lookup"><span data-stu-id="e9251-109"><a name="bk_PreReqs"> </a></span></span>

<span data-ttu-id="e9251-110">若要在 AD DS 中找到自动发现 SCP 对象，你需要有权访问以下内容：</span><span class="sxs-lookup"><span data-stu-id="e9251-110">To locate Autodiscover SCP objects in AD DS, you need to have access to the following:</span></span>
  
- <span data-ttu-id="e9251-111">运行 Exchange 本地版本（最低版本为 Exchange 2007 SP1）的服务器。</span><span class="sxs-lookup"><span data-stu-id="e9251-111">A server that is running a version of Exchange on-premises starting with Exchange 2007 SP1.</span></span>
    
- <span data-ttu-id="e9251-112">已加入安装 Exchange 服务器的域的客户端计算机。</span><span class="sxs-lookup"><span data-stu-id="e9251-112">A client computer that is joined to the domain that the Exchange server is installed in.</span></span>
    
- <span data-ttu-id="e9251-113">在 Exchange 服务器上有邮箱的用户帐户。</span><span class="sxs-lookup"><span data-stu-id="e9251-113">A user account that has a mailbox on the Exchange server.</span></span> 
    
<span data-ttu-id="e9251-114">此外，在开始之前，你还需要熟悉一些基本概念。</span><span class="sxs-lookup"><span data-stu-id="e9251-114">Also, before you begin, you'll want to be familiar some basic concepts.</span></span> <span data-ttu-id="e9251-115">下面是将帮助到你的一些资源。</span><span class="sxs-lookup"><span data-stu-id="e9251-115">The following are some resources that you'll find helpful.</span></span>
  
<span data-ttu-id="e9251-116">**表 1. 有关从 SCP 对象查找自动发现终结点的相关文章**</span><span class="sxs-lookup"><span data-stu-id="e9251-116">**Table 1. Related articles for finding Autodiscover endpoints from SCP objects**</span></span>

|<span data-ttu-id="e9251-117">**阅读本文**</span><span class="sxs-lookup"><span data-stu-id="e9251-117">**Read this article**</span></span>|<span data-ttu-id="e9251-118">**若要了解…**</span><span class="sxs-lookup"><span data-stu-id="e9251-118">**To learn about…**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e9251-119">Exchange 自动发现</span><span class="sxs-lookup"><span data-stu-id="e9251-119">Autodiscover for Exchange</span></span>](autodiscover-for-exchange.md) <br/> |<span data-ttu-id="e9251-120">自动发现服务的工作方式。</span><span class="sxs-lookup"><span data-stu-id="e9251-120">How the Autodiscover service works.</span></span>  <br/> |
|[<span data-ttu-id="e9251-121">使用服务连接点进行发布</span><span class="sxs-lookup"><span data-stu-id="e9251-121">Publishing with Service Connection Points</span></span>](https://msdn.microsoft.com/library/3544aa64-ecb0-48a1-ae49-05247a983842%28Office.15%29.aspx) <br/> |<span data-ttu-id="e9251-122">SCP 对象如何用于发布服务特定的数据。</span><span class="sxs-lookup"><span data-stu-id="e9251-122">How SCP objects are used to publish service-specific data.</span></span>  <br/> |
   
## <a name="locate-autodiscover-scp-objects-in-ad-ds"></a><span data-ttu-id="e9251-123">在 AD DS 中找到自动发现 SCP 对象</span><span class="sxs-lookup"><span data-stu-id="e9251-123">Locate Autodiscover SCP objects in AD DS</span></span>
<span data-ttu-id="e9251-124"><a name="bk_LocateScpObjects"> </a></span><span class="sxs-lookup"><span data-stu-id="e9251-124"><a name="bk_LocateScpObjects"> </a></span></span>

<span data-ttu-id="e9251-125">要找到在 AD DS 中发布的自动发现终结点，首先是找到自动发现 SCP 对象。</span><span class="sxs-lookup"><span data-stu-id="e9251-125">The first step toward finding Autodiscover endpoints published in AD DS is to locate the Autodiscover SCP objects.</span></span> <span data-ttu-id="e9251-126">Exchange 针对自动发现发布了两种类型的 SCP 对象：</span><span class="sxs-lookup"><span data-stu-id="e9251-126">Exchange publishes two types of SCP objects for Autodiscover:</span></span>
  
- <span data-ttu-id="e9251-127">**SCP 指针** - 其中包含指向特定 LDAP 服务器的信息，此信息应该用于查找用户的域的自动发现 SCP 对象。</span><span class="sxs-lookup"><span data-stu-id="e9251-127">**SCP pointers** — These contain information that points to specific LDAP servers that should be used to locate Autodiscover SCP objects for the user's domain.</span></span> <span data-ttu-id="e9251-128">使用以下 GUID 标记 SCP 指针：67661d7F-8FC4-4fa7-BFAC-E1D7794C1F68。</span><span class="sxs-lookup"><span data-stu-id="e9251-128">SCP pointers are stamped with the following GUID: 67661d7F-8FC4-4fa7-BFAC-E1D7794C1F68.</span></span> 
    
- <span data-ttu-id="e9251-129">**SCP URL** - 其中包含自动发现终结点的 URL。</span><span class="sxs-lookup"><span data-stu-id="e9251-129">**SCP URLs** — These contain URLs for Autodiscover endpoints.</span></span> <span data-ttu-id="e9251-130">使用以下 GUID 标记 SCP URL：77378F46-2C66-4aa9-A6A6-3E7A48B19596。</span><span class="sxs-lookup"><span data-stu-id="e9251-130">SCP URLs are stamped with the following GUID: 77378F46-2C66-4aa9-A6A6-3E7A48B19596.</span></span> 
    
### <a name="to-locate-autodiscover-scp-objects"></a><span data-ttu-id="e9251-131">若要查找自动发现 SCP 对象</span><span class="sxs-lookup"><span data-stu-id="e9251-131">To locate Autodiscover SCP objects</span></span>

1. <span data-ttu-id="e9251-132">读取 AD DS 中根 DSE 条目的 **configurationNamingContext** 属性，获取指向域的配置命名上下文的路径。</span><span class="sxs-lookup"><span data-stu-id="e9251-132">Read the **configurationNamingContext** property of the root DSE entry in AD DS to get the path to the configuration naming context for the domain.</span></span> <span data-ttu-id="e9251-133">可使用 [DirectoryEntry](https://msdn2.microsoft.com/library/z9cddzaa) 类或可访问 AD DS 的任何其他 API 来实现这一点。</span><span class="sxs-lookup"><span data-stu-id="e9251-133">You can do this by using the [DirectoryEntry](https://msdn2.microsoft.com/library/z9cddzaa) class, or any other API that can acces AD DS.</span></span> 
    
2. <span data-ttu-id="e9251-134">在配置命名上下文中搜索 **keywords** 属性中具有 SCP 指针 GUID 或 SCP URL GUID 的 SCP 对象。</span><span class="sxs-lookup"><span data-stu-id="e9251-134">Search for SCP objects in the configuration naming context that have either the SCP pointer GUID or the SCP URL GUID in the **keywords** property.</span></span> 
    
3. <span data-ttu-id="e9251-135">通过检查等于 `"Domain=<domain>"` 的条目的 **keywords** 属性，检查你为范围是用户域的 SCP 指针找到的 SCP 对象。</span><span class="sxs-lookup"><span data-stu-id="e9251-135">Check the SCP objects you found for an SCP pointer that is scoped to the user's domain by checking the **keywords** property for an entry equal to `"Domain=<domain>"`.</span></span> <span data-ttu-id="e9251-136">例如，如果用户的电子邮件地址是 elvin@contoso.com，则你要使用 **keywords** 属性中等于 `"Domain=contoso.com"` 的条目查找 SCP 指针。</span><span class="sxs-lookup"><span data-stu-id="e9251-136">For example, if the user's email address is elvin@contoso.com, you would look for an SCP pointer with an entry in the **keywords** property that is equal to `"Domain=contoso.com"`.</span></span> <span data-ttu-id="e9251-137">如果找到匹配的 SCP 指针，请放弃一组 SCP 对象，并从步骤 1 开始操作，对于根 DSE 条目，使用 **serviceBindingInformation** 属性的值作为要连接到的服务器。</span><span class="sxs-lookup"><span data-stu-id="e9251-137">If a matching SCP pointer is found, discard the set of SCP objects and start over at step 1 using the value of the **serviceBindingInformation** property as the server to connect to for the Root DSE entry.</span></span> 
    
4. <span data-ttu-id="e9251-138">如果找不到任何范围是用户域的 SCP 指针，请检查范围不是任何域的所有 SCP 指针，并将 **serviceBindingInformation** 属性的值保存为“回退”服务器，以防当前服务器不返回任何结果。</span><span class="sxs-lookup"><span data-stu-id="e9251-138">If you don't find any SCP pointers scoped to the user's domain, check for any SCP pointers that aren't scoped to any domain, and save the value of the **serviceBindingInformation** property as a "fallback" server, in case the current server doesn't give you any results.</span></span> 
    
5. <span data-ttu-id="e9251-139">如果找不到任何范围是域的 SCP 指针，则表示你可继续到下一步，也就是基于结果生成一个已排列优先级的自动发现终结点列表。</span><span class="sxs-lookup"><span data-stu-id="e9251-139">If you didn't find any SCP pointers scoped to the domain, you're ready to move on to the next step: generating a prioritized list of Autodiscover endpoints from your results.</span></span>
    
## <a name="generate-a-prioritized-list-of-autodiscover-endpoints"></a><span data-ttu-id="e9251-140">生成已排列优先级的自动发现终结点列表</span><span class="sxs-lookup"><span data-stu-id="e9251-140">Generate a prioritized list of Autodiscover endpoints</span></span>
<span data-ttu-id="e9251-141"><a name="bk_GenerateList"> </a></span><span class="sxs-lookup"><span data-stu-id="e9251-141"><a name="bk_GenerateList"> </a></span></span>

<span data-ttu-id="e9251-142">你可执行以下操作，使用你找到的那组 SCP 对象生成一个已排列优先级的自动发现终结点 URL 的列表：</span><span class="sxs-lookup"><span data-stu-id="e9251-142">You can generate a prioritized list of Autodiscover endpoint URLs, using the set of SCP objects that you located, by doing the following:</span></span>
  
1. <span data-ttu-id="e9251-143">获取客户端计算机的 Active Directory 站点名称。</span><span class="sxs-lookup"><span data-stu-id="e9251-143">Get the Active Directory site name of the client computer.</span></span>
    
2. <span data-ttu-id="e9251-144">在你找到的那组 SCP 对象中检查每个 SCP URL 上的 **keywords** 属性，然后根据以下规则向 URL 分配一个优先级：</span><span class="sxs-lookup"><span data-stu-id="e9251-144">Check the **keywords** property on each SCP URL in the set of SCP objects you found, and assign a priority to the URL based on the following rules:</span></span> 
    
  - <span data-ttu-id="e9251-145">如果 **keywords** 属性包含一个 `"Site=<site name>"` 值，其中 `<site name>` 等于你在上一步中检索到的 Active Directory 站点的名称，请向 URL 分配优先级 1。</span><span class="sxs-lookup"><span data-stu-id="e9251-145">If the **keywords** property contains a value of `"Site=<site name>"`, where `<site name>` equals the name of the Active Directory site you retrieved in the previous step, assign the URL a priority of 1.</span></span> 
    
  - <span data-ttu-id="e9251-146">如果 **keywords** 属性中没有以 `"Site="` 开头的值的条目，那么请向 URL 分配优先级 2。</span><span class="sxs-lookup"><span data-stu-id="e9251-146">If the **keywords** property does not contain an entry with a value that starts with `"Site="`, assign the URL a priority of 2.</span></span> 
    
  - <span data-ttu-id="e9251-147">如果 **keywords** 属性包含一个 `"Site=<site name>` 值，其中 `<site name>` 不等于你在上一步中检索到的 Active Directory 站点的名称，请向 URL 分配优先级 3。</span><span class="sxs-lookup"><span data-stu-id="e9251-147">If the **keywords** property contains a value of `"Site=<site name>`, where `<site name>` does not equal the name of the Active Directory site you retrieved in the previous step, assign the URL a priority of 3.</span></span> 
    
## <a name="code-example-performing-an-scp-lookup"></a><span data-ttu-id="e9251-148">代码示例：执行 SCP 查找</span><span class="sxs-lookup"><span data-stu-id="e9251-148">Code example: Performing an SCP lookup</span></span>
<span data-ttu-id="e9251-149"><a name="bk_CodeExample"> </a></span><span class="sxs-lookup"><span data-stu-id="e9251-149"><a name="bk_CodeExample"> </a></span></span>

<span data-ttu-id="e9251-150">在下面的代码示例中，你将了解如何查找自动发现 SCP 对象和生成已排列优先级的自动发现终结点列表。</span><span class="sxs-lookup"><span data-stu-id="e9251-150">In the following code example, you'll see how to locate Autodiscover SCP objects and generate a prioritized list of Autodiscover endpoints.</span></span>
  
```cs
using System;
using System.Collections.Generic;
using System.DirectoryServices;
using System.DirectoryServices.ActiveDirectory;
namespace ScpLookup
{
    // This sample is for demonstration purposes only. Before you run this sample, make sure 
    // that the code meets the coding requirements of your organization. 
    class Program
    {
        static void Main(string[] args)
        {
            string domain = args[0];
            Console.WriteLine("Performing SCP lookup for {0}.", domain);
            List<string> scpUrls = GetScpUrls(null, domain);
            Console.WriteLine("\nOrdered List of Autodiscover endpoints:");
            foreach (string url in scpUrls)
            {
                Console.WriteLine("  {0}", url);
            }
            Console.WriteLine("SCP lookup done.");
        }
        // GUID for SCP URL keyword.
        private const string ScpUrlGuidString = @"77378F46-2C66-4aa9-A6A6-3E7A48B19596";
        // GUID for SCP pointer keyword.
        private const string ScpPtrGuidString = @"67661d7F-8FC4-4fa7-BFAC-E1D7794C1F68";
        static List<string> GetScpUrls(string ldapServer, string domain)
        {
            // Create a new list to return.
            List<string> scpUrlList = new List<string>();
            string rootDSEPath = null;
            // If ldapServer is null/empty, use LDAP://RootDSE to
            // connect to Active Directory Domain Services (AD DS). Otherwise, use
            // LDAP://SERVERNAME/RootDSE to connect to a specific server.
            if (string.IsNullOrEmpty(ldapServer))
            {
                rootDSEPath = "LDAP://RootDSE";
            }
            else
            {
                rootDSEPath = ldapServer + "/RootDSE";
            }
            SearchResultCollection scpEntries = null;
            try
            {
                // Get the root directory entry.
                DirectoryEntry rootDSE = new DirectoryEntry(rootDSEPath);
                // Get the configuration path.
                string configPath = rootDSE.Properties["configurationNamingContext"].Value as string;
                // Get the configuration entry.
                DirectoryEntry configEntry = new DirectoryEntry("LDAP://" + configPath);
                // Create a search object for the configuration entry.
                DirectorySearcher configSearch = new DirectorySearcher(configEntry);
                // Set the search filter to find SCP URLs and SCP pointers.
                configSearch.Filter = "(&amp;(objectClass=serviceConnectionPoint)" +
                    "(|(keywords=" + ScpPtrGuidString + ")(keywords=" + ScpUrlGuidString + ")))";
                // Specify which properties you want to retrieve.
                configSearch.PropertiesToLoad.Add("keywords");
                configSearch.PropertiesToLoad.Add("serviceBindingInformation");
                scpEntries = configSearch.FindAll();
            }
            catch (Exception ex)
            {
                Console.WriteLine("SCP lookup failed with: ");
                Console.WriteLine(ex.ToString());
            }
            // If no SCP entries were found, then exit.
            if (scpEntries == null || scpEntries.Count <= 0)
            {
                Console.WriteLine("No SCP records found.");
                return null;
            }
            string fallBackLdapPath = null;
            // Check for SCP pointers.
            foreach (SearchResult scpEntry in scpEntries)
            {
                ResultPropertyValueCollection entryKeywords = scpEntry.Properties["keywords"];
                if (CollectionContainsExactValue(entryKeywords, ScpPtrGuidString))
                {
                    string ptrLdapPath = scpEntry.Properties["serviceBindingInformation"][0] as string;
                    // Determine whether this pointer is scoped to the user's domain.
                    if (CollectionContainsExactValue(entryKeywords, "Domain=" + domain))
                    {
                        Console.WriteLine("Found SCP pointer for " + domain + " in " + scpEntry.Path);
                        // Restart SCP lookup with the server assigned for the domain.
                        Console.WriteLine("Restarting SCP lookup in " + ptrLdapPath);
                        return GetScpUrls(ptrLdapPath, domain);
                    }
                    else
                    {
                        // Save the first SCP pointer that is not scoped to a domain as a fallback
                        // in case you do not get any results from this server.
                        if (entryKeywords.Count == 1 && string.IsNullOrEmpty(fallBackLdapPath))
                        {
                            fallBackLdapPath = ptrLdapPath;
                            Console.WriteLine("Saved fallback SCP pointer: " + fallBackLdapPath);
                        }
                    }
                }
            }
            string computerSiteName = null;
            try
            {
                // Get the name of the ActiveDirectorySite the computer
                // belongs to (if it belongs to one).
                ActiveDirectorySite site = ActiveDirectorySite.GetComputerSite();
                computerSiteName = site.Name;
                Console.WriteLine("Local computer in site: " + computerSiteName);
            }
            catch (Exception ex)
            {
                Console.WriteLine("Unable to get computer site name.");
                Console.WriteLine(ex.ToString());
            }
            if (!string.IsNullOrEmpty(computerSiteName))
            {
                // Scan the search results for SCP URLs.
                // SCP URLs fit into three tiers:
                //   Priority 1: The URL is scoped to the computer's Active Directory site.
                //   Priority 2: The URL is not scoped to any Active Directory site.
                //   Priority 3: The URL is scoped to a different Active Directory site.
                // Temporary lists to hold priority 2 and 3 URLs.
                List<string> priorityTwoUrls = new List<string>();
                List<string> priorityThreeUrls = new List<string>();
                foreach (SearchResult scpEntry in scpEntries)
                {
                    ResultPropertyValueCollection entryKeywords = scpEntry.Properties["keywords"];
                    // Check for SCP URLs.
                    if (CollectionContainsExactValue(entryKeywords, ScpUrlGuidString))
                    {
                        string scpUrlPath = scpEntry.Properties["adsPath"][0] as string;
                        Console.WriteLine("SCP URL found at {0}", scpUrlPath);
                        string scpUrl = scpEntry.Properties["serviceBindingInformation"][0] as string;
                        scpUrl = scpUrl.ToLower();
                        // Determine whether this entry is scoped to the computer's site.
                        if (CollectionContainsExactValue(entryKeywords, "Site=" + computerSiteName))
                        {
                            // Priority 1.
                            if (!scpUrlList.Contains(scpUrl.ToLower()))
                            {
                                Console.WriteLine("Adding priority 1 SCP URL: {0}", scpUrl.ToLower());
                                scpUrlList.Add(scpUrl);
                            }
                            else
                            {
                                Console.WriteLine("Priority 1 SCP URL already found: {0}", scpUrl);
                            }
                        }
                        else
                        {
                            // Determine whether this is a priority 2 or 3 URL.
                            if (CollectionContainsPrefixValue(entryKeywords, "Site="))
                            {
                                // Priority 3.
                                if (!priorityThreeUrls.Contains(scpUrl))
                                {
                                    Console.WriteLine("Adding priority 3 SCP URL: {0}", scpUrl);
                                    priorityThreeUrls.Add(scpUrl);
                                }
                                else
                                {
                                    Console.WriteLine("Priority 3 SCP URL already found: {0}", scpUrl);
                                }
                            }
                            else
                            {
                                // Priority 2.
                                if (!priorityTwoUrls.Contains(scpUrl))
                                {
                                    Console.WriteLine("Adding priority 2 SCP URL: {0}", scpUrl);
                                    priorityTwoUrls.Add(scpUrl);
                                }
                                else
                                {
                                    Console.WriteLine("Priority 2 SCP URL already found: {0}", scpUrl);
                                }
                            }
                        }
                    }
                }
                // Now add the priority 2 URLs into the main list.
                foreach (string priorityTwoUrl in priorityTwoUrls)
                {
                    // If the URL is already in the list as a priority 1, 
                    // don't add it again.
                    if (!scpUrlList.Contains(priorityTwoUrl))
                    {
                        scpUrlList.Add(priorityTwoUrl);
                    }
                }
                // Now add the priority 3 URLs into the main list.
                foreach (string priorityThreeUrl in priorityThreeUrls)
                {
                    // If the URL is already in the list as a priority 1
                    // or priority 2, don't add it again.
                    if (!scpUrlList.Contains(priorityThreeUrl))
                    {
                        scpUrlList.Add(priorityThreeUrl);
                    }
                }
                // If after all this, you still have no URLs in your list,
                // try the fallback SCP pointer, if you have one.
                if (scpUrlList.Count == 0 && fallBackLdapPath != null)
                {
                    return GetScpUrls(fallBackLdapPath, domain);
                }
            }
            return scpUrlList;
        }
        private static bool CollectionContainsExactValue(ResultPropertyValueCollection collection, string value)
        {
            foreach (object obj in collection)
            {
                string entry = obj as string;
                if (entry != null)
                {
                    if (string.Compare(value, entry, true) == 0)
                        return true;
                }
            }
            return false;
        }
        private static bool CollectionContainsPrefixValue(ResultPropertyValueCollection collection, string value)
        {
            foreach (object obj in collection)
            {
                string entry = obj as string;
                if (entry != null)
                {
                    if (entry.StartsWith(value))
                        return true;
                }
            }
            return false;
        }
    }
}
```

## <a name="next-steps"></a><span data-ttu-id="e9251-151">后续步骤</span><span class="sxs-lookup"><span data-stu-id="e9251-151">Next steps</span></span>
<span data-ttu-id="e9251-152"><a name="bk_NextSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="e9251-152"><a name="bk_NextSteps"> </a></span></span>

<span data-ttu-id="e9251-153">在自动发现过程中，下一步是将自动发现请求发送至你找到的 URL，首先发给优先级为 1 的 URL，然后是优先级为 2 的URL，最后是优先级为 3 的 URL。</span><span class="sxs-lookup"><span data-stu-id="e9251-153">The next step in the Autodiscover process is to send Autodiscover requests to the URLs that you found, starting with priority 1 URLs, then priority 2 URLs, and finally priority 3 URLs.</span></span> <span data-ttu-id="e9251-154">若要详细了解如何发送自动发现请求和处理响应，请阅读以下文章：</span><span class="sxs-lookup"><span data-stu-id="e9251-154">To learn more about how to send Autodiscover requests and handle responses, read the following articles:</span></span>
  
- [<span data-ttu-id="e9251-155">使用自动发现从 Exchange 获取用户设置</span><span class="sxs-lookup"><span data-stu-id="e9251-155">Get user settings from Exchange by using Autodiscover</span></span>](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    
- [<span data-ttu-id="e9251-156">处理自动发现错误消息</span><span class="sxs-lookup"><span data-stu-id="e9251-156">Handling Autodiscover error messages</span></span>](handling-autodiscover-error-messages.md)
    
## <a name="see-also"></a><span data-ttu-id="e9251-157">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e9251-157">See also</span></span>

- [<span data-ttu-id="e9251-158">Exchange 自动发现</span><span class="sxs-lookup"><span data-stu-id="e9251-158">Autodiscover for Exchange</span></span>](autodiscover-for-exchange.md)   
- [<span data-ttu-id="e9251-159">设置 EWS 应用程序</span><span class="sxs-lookup"><span data-stu-id="e9251-159">Setting up your EWS application</span></span>](setting-up-your-ews-application.md)
    

