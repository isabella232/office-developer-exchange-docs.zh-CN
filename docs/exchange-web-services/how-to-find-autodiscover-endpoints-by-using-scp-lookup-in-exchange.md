---
title: 通过使用 Exchange 中的 SCP 查找来找到自动发现终结点
manager: kelbow
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: b24228a8-5127-4bac-aef0-9c9e8843c9ff
description: 了解如何查找 Active Directory 域服务（AD DS）中的自动发现 SCP 对象，并使用它们查找要与 Exchange 自动发现服务一起使用的自动发现终结点 Url。
localization_priority: Priority
ms.openlocfilehash: c0c0364a7d69364e12db902f1f22d65c4b5a0cc5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455875"
---
# <a name="find-autodiscover-endpoints-by-using-scp-lookup-in-exchange"></a><span data-ttu-id="3d51a-103">通过使用 Exchange 中的 SCP 查找来找到自动发现终结点</span><span class="sxs-lookup"><span data-stu-id="3d51a-103">Find Autodiscover endpoints by using SCP lookup in Exchange</span></span>

<span data-ttu-id="3d51a-104">了解如何查找 Active Directory 域服务（AD DS）中的自动发现 SCP 对象，并使用它们查找要与 Exchange 自动发现服务一起使用的自动发现终结点 Url。</span><span class="sxs-lookup"><span data-stu-id="3d51a-104">Find out how to locate Autodiscover SCP objects in Active Directory Domain Services (AD DS) and use them to find Autodiscover endpoint URLs to use with the Exchange Autodiscover service.</span></span>
  
<span data-ttu-id="3d51a-105">自动发现使您能够轻松地检索连接到 Exchange 服务器上的邮箱所需的信息。</span><span class="sxs-lookup"><span data-stu-id="3d51a-105">Autodiscover makes it easy to retrieve information that you need to connect to mailboxes on Exchange servers.</span></span> <span data-ttu-id="3d51a-106">但是，若要使用自动发现，需要一种方法来查找适用于要检索其设置的用户的自动发现服务器。</span><span class="sxs-lookup"><span data-stu-id="3d51a-106">However, in order to use Autodiscover, you need a way to find Autodiscover servers that are appropriate for the user you're retrieving settings for.</span></span> <span data-ttu-id="3d51a-107">AD DS 中的服务连接点（SCP）对象为加入域的客户端提供了一种用于查找自动发现服务器的简单方法。</span><span class="sxs-lookup"><span data-stu-id="3d51a-107">Service connection point (SCP) objects in AD DS provide an easy way for domain-joined clients to look up Autodiscover servers.</span></span> 
  
## <a name="get-set-up-to-find-autodiscover-endpoints"></a><span data-ttu-id="3d51a-108">设置以查找自动发现终结点</span><span class="sxs-lookup"><span data-stu-id="3d51a-108">Get set up to find Autodiscover endpoints</span></span>
<span data-ttu-id="3d51a-109"><a name="bk_PreReqs"> </a></span><span class="sxs-lookup"><span data-stu-id="3d51a-109"><a name="bk_PreReqs"> </a></span></span>

<span data-ttu-id="3d51a-110">若要在 AD DS 中查找自动发现 SCP 对象，您需要具有以下权限：</span><span class="sxs-lookup"><span data-stu-id="3d51a-110">To locate Autodiscover SCP objects in AD DS, you need to have access to the following:</span></span>
  
- <span data-ttu-id="3d51a-111">运行本地 Exchange 版本（从 Exchange 2007 SP1 开始）的服务器。</span><span class="sxs-lookup"><span data-stu-id="3d51a-111">A server that is running a version of Exchange on-premises starting with Exchange 2007 SP1.</span></span>
    
- <span data-ttu-id="3d51a-112">加入到安装了 Exchange server 的域的客户端计算机。</span><span class="sxs-lookup"><span data-stu-id="3d51a-112">A client computer that is joined to the domain that the Exchange server is installed in.</span></span>
    
- <span data-ttu-id="3d51a-113">在 Exchange 服务器上拥有邮箱的用户帐户。</span><span class="sxs-lookup"><span data-stu-id="3d51a-113">A user account that has a mailbox on the Exchange server.</span></span> 
    
<span data-ttu-id="3d51a-114">此外，在开始之前，您需要熟悉一些基本概念。</span><span class="sxs-lookup"><span data-stu-id="3d51a-114">Also, before you begin, you'll want to be familiar some basic concepts.</span></span> <span data-ttu-id="3d51a-115">下面是一些可帮助您了解的资源。</span><span class="sxs-lookup"><span data-stu-id="3d51a-115">The following are some resources that you'll find helpful.</span></span>
  
<span data-ttu-id="3d51a-116">**表1。用于从 SCP 对象中查找自动发现终结点的相关文章**</span><span class="sxs-lookup"><span data-stu-id="3d51a-116">**Table 1. Related articles for finding Autodiscover endpoints from SCP objects**</span></span>

|<span data-ttu-id="3d51a-117">**阅读本文**</span><span class="sxs-lookup"><span data-stu-id="3d51a-117">**Read this article**</span></span>|<span data-ttu-id="3d51a-118">**若要了解 .。。**</span><span class="sxs-lookup"><span data-stu-id="3d51a-118">**To learn about…**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3d51a-119">Exchange 自动发现</span><span class="sxs-lookup"><span data-stu-id="3d51a-119">Autodiscover for Exchange</span></span>](autodiscover-for-exchange.md) <br/> |<span data-ttu-id="3d51a-120">自动发现服务的工作方式。</span><span class="sxs-lookup"><span data-stu-id="3d51a-120">How the Autodiscover service works.</span></span>  <br/> |
|[<span data-ttu-id="3d51a-121">使用服务连接点进行发布</span><span class="sxs-lookup"><span data-stu-id="3d51a-121">Publishing with Service Connection Points</span></span>](https://msdn.microsoft.com/library/3544aa64-ecb0-48a1-ae49-05247a983842%28Office.15%29.aspx) <br/> |<span data-ttu-id="3d51a-122">如何使用 SCP 对象发布服务特定的数据。</span><span class="sxs-lookup"><span data-stu-id="3d51a-122">How SCP objects are used to publish service-specific data.</span></span>  <br/> |
   
## <a name="locate-autodiscover-scp-objects-in-ad-ds"></a><span data-ttu-id="3d51a-123">在 AD DS 中查找自动发现 SCP 对象</span><span class="sxs-lookup"><span data-stu-id="3d51a-123">Locate Autodiscover SCP objects in AD DS</span></span>
<span data-ttu-id="3d51a-124"><a name="bk_LocateScpObjects"> </a></span><span class="sxs-lookup"><span data-stu-id="3d51a-124"><a name="bk_LocateScpObjects"> </a></span></span>

<span data-ttu-id="3d51a-125">在 AD DS 中查找已发布的自动发现终结点的第一步是找到自动发现 SCP 对象。</span><span class="sxs-lookup"><span data-stu-id="3d51a-125">The first step toward finding Autodiscover endpoints published in AD DS is to locate the Autodiscover SCP objects.</span></span> <span data-ttu-id="3d51a-126">Exchange 发布了两种类型的 SCP 对象进行自动发现：</span><span class="sxs-lookup"><span data-stu-id="3d51a-126">Exchange publishes two types of SCP objects for Autodiscover:</span></span>
  
- <span data-ttu-id="3d51a-127">**SCP 指针**—这些信息包含指向特定 LDAP 服务器的信息，这些服务器应用于查找用户域的自动发现 SCP 对象。</span><span class="sxs-lookup"><span data-stu-id="3d51a-127">**SCP pointers** — These contain information that points to specific LDAP servers that should be used to locate Autodiscover SCP objects for the user's domain.</span></span> <span data-ttu-id="3d51a-128">使用以下 GUID 对 SCP 指针进行标记：67661d7F-8FC4-4fa7-BFAC-E1D7794C1F68。</span><span class="sxs-lookup"><span data-stu-id="3d51a-128">SCP pointers are stamped with the following GUID: 67661d7F-8FC4-4fa7-BFAC-E1D7794C1F68.</span></span> 
    
- <span data-ttu-id="3d51a-129">**SCP url** ，其中包含自动发现终结点的 url。</span><span class="sxs-lookup"><span data-stu-id="3d51a-129">**SCP URLs** — These contain URLs for Autodiscover endpoints.</span></span> <span data-ttu-id="3d51a-130">将使用以下 GUID 标记 SCP Url：77378F46-2C66-4aa9-A6A6-3E7A48B19596。</span><span class="sxs-lookup"><span data-stu-id="3d51a-130">SCP URLs are stamped with the following GUID: 77378F46-2C66-4aa9-A6A6-3E7A48B19596.</span></span> 
    
### <a name="to-locate-autodiscover-scp-objects"></a><span data-ttu-id="3d51a-131">查找自动发现 SCP 对象</span><span class="sxs-lookup"><span data-stu-id="3d51a-131">To locate Autodiscover SCP objects</span></span>

1. <span data-ttu-id="3d51a-132">阅读 AD DS 中的根 DSE 条目的**configurationNamingContext**属性，以获取域的配置命名上下文的路径。</span><span class="sxs-lookup"><span data-stu-id="3d51a-132">Read the **configurationNamingContext** property of the root DSE entry in AD DS to get the path to the configuration naming context for the domain.</span></span> <span data-ttu-id="3d51a-133">您可以使用[DirectoryEntry](https://msdn2.microsoft.com/library/z9cddzaa)类或任何其他可对 AD DS 进行的 API 来执行此操作。</span><span class="sxs-lookup"><span data-stu-id="3d51a-133">You can do this by using the [DirectoryEntry](https://msdn2.microsoft.com/library/z9cddzaa) class, or any other API that can acces AD DS.</span></span> 
    
2. <span data-ttu-id="3d51a-134">在具有 SCP 指针 GUID 或 "**关键字**" 属性中的 "scp URL" guid 的配置命名上下文中搜索 SCP 对象。</span><span class="sxs-lookup"><span data-stu-id="3d51a-134">Search for SCP objects in the configuration naming context that have either the SCP pointer GUID or the SCP URL GUID in the **keywords** property.</span></span> 
    
3. <span data-ttu-id="3d51a-135">通过检查等于的条目的**关键字**属性，检查您找到的适用于用户域的 scp 指针的 scp 对象 `"Domain=<domain>"` 。</span><span class="sxs-lookup"><span data-stu-id="3d51a-135">Check the SCP objects you found for an SCP pointer that is scoped to the user's domain by checking the **keywords** property for an entry equal to `"Domain=<domain>"`.</span></span> <span data-ttu-id="3d51a-136">例如，如果用户的电子邮件地址为 elvin@contoso.com，则会查找 "**关键字**" 属性中的条目等于的 SCP 指针 `"Domain=contoso.com"` 。</span><span class="sxs-lookup"><span data-stu-id="3d51a-136">For example, if the user's email address is elvin@contoso.com, you would look for an SCP pointer with an entry in the **keywords** property that is equal to `"Domain=contoso.com"`.</span></span> <span data-ttu-id="3d51a-137">如果找到匹配的 SCP 指针，请丢弃 SCP 对象集，并通过在第1步中使用**serviceBindingInformation**属性的值作为要连接到根 DSE 条目的服务器来重新开始。</span><span class="sxs-lookup"><span data-stu-id="3d51a-137">If a matching SCP pointer is found, discard the set of SCP objects and start over at step 1 using the value of the **serviceBindingInformation** property as the server to connect to for the Root DSE entry.</span></span> 
    
4. <span data-ttu-id="3d51a-138">如果找不到作用域为用户域的任何 SCP 指针，请检查是否有作用域的任何不是任何域的 SCP 指针，并将**serviceBindingInformation**属性的值另存为 "回退" 服务器，以防当前服务器不提供任何结果。</span><span class="sxs-lookup"><span data-stu-id="3d51a-138">If you don't find any SCP pointers scoped to the user's domain, check for any SCP pointers that aren't scoped to any domain, and save the value of the **serviceBindingInformation** property as a "fallback" server, in case the current server doesn't give you any results.</span></span> 
    
5. <span data-ttu-id="3d51a-139">如果找不到作用域的任何 SCP 指针，则可以继续执行下一步：从结果中生成自动发现终结点的优先级列表。</span><span class="sxs-lookup"><span data-stu-id="3d51a-139">If you didn't find any SCP pointers scoped to the domain, you're ready to move on to the next step: generating a prioritized list of Autodiscover endpoints from your results.</span></span>
    
## <a name="generate-a-prioritized-list-of-autodiscover-endpoints"></a><span data-ttu-id="3d51a-140">生成自动发现终结点的优先级列表</span><span class="sxs-lookup"><span data-stu-id="3d51a-140">Generate a prioritized list of Autodiscover endpoints</span></span>
<span data-ttu-id="3d51a-141"><a name="bk_GenerateList"> </a></span><span class="sxs-lookup"><span data-stu-id="3d51a-141"><a name="bk_GenerateList"> </a></span></span>

<span data-ttu-id="3d51a-142">您可以通过执行以下操作，使用您找到的 SCP 对象集生成自动发现终结点 Url 的优先级列表：</span><span class="sxs-lookup"><span data-stu-id="3d51a-142">You can generate a prioritized list of Autodiscover endpoint URLs, using the set of SCP objects that you located, by doing the following:</span></span>
  
1. <span data-ttu-id="3d51a-143">获取客户端计算机的 Active Directory 站点名称。</span><span class="sxs-lookup"><span data-stu-id="3d51a-143">Get the Active Directory site name of the client computer.</span></span>
    
2. <span data-ttu-id="3d51a-144">检查找到的一组 SCP 对象中的每个 SCP URL 上的**关键字**属性，并根据以下规则将优先级分配给 url：</span><span class="sxs-lookup"><span data-stu-id="3d51a-144">Check the **keywords** property on each SCP URL in the set of SCP objects you found, and assign a priority to the URL based on the following rules:</span></span> 
    
  - <span data-ttu-id="3d51a-145">如果**关键字**属性包含的值为 `"Site=<site name>"` ，其中 `<site name>` 等于在上一步中检索到的 Active Directory 站点的名称，请为 URL 分配优先级1。</span><span class="sxs-lookup"><span data-stu-id="3d51a-145">If the **keywords** property contains a value of `"Site=<site name>"`, where `<site name>` equals the name of the Active Directory site you retrieved in the previous step, assign the URL a priority of 1.</span></span> 
    
  - <span data-ttu-id="3d51a-146">如果**关键字**属性不包含以值开头的条目 `"Site="` ，请将 URL 的优先级分配为2。</span><span class="sxs-lookup"><span data-stu-id="3d51a-146">If the **keywords** property does not contain an entry with a value that starts with `"Site="`, assign the URL a priority of 2.</span></span> 
    
  - <span data-ttu-id="3d51a-147">如果**关键字**属性包含的值 `"Site=<site name>` `<site name>` 不等于在上一步中检索到的 Active Directory 站点的名称，则为 URL 分配优先级为3。</span><span class="sxs-lookup"><span data-stu-id="3d51a-147">If the **keywords** property contains a value of `"Site=<site name>`, where `<site name>` does not equal the name of the Active Directory site you retrieved in the previous step, assign the URL a priority of 3.</span></span> 
    
## <a name="code-example-performing-an-scp-lookup"></a><span data-ttu-id="3d51a-148">代码示例：执行 SCP 查找</span><span class="sxs-lookup"><span data-stu-id="3d51a-148">Code example: Performing an SCP lookup</span></span>
<span data-ttu-id="3d51a-149"><a name="bk_CodeExample"> </a></span><span class="sxs-lookup"><span data-stu-id="3d51a-149"><a name="bk_CodeExample"> </a></span></span>

<span data-ttu-id="3d51a-150">在下面的代码示例中，您将了解如何查找自动发现 SCP 对象并生成自动发现终结点的按优先级排序的列表。</span><span class="sxs-lookup"><span data-stu-id="3d51a-150">In the following code example, you'll see how to locate Autodiscover SCP objects and generate a prioritized list of Autodiscover endpoints.</span></span>
  
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
                        if (entryKeywords.Count == 1 &amp;&amp; string.IsNullOrEmpty(fallBackLdapPath))
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
                if (scpUrlList.Count == 0 &amp;&amp; fallBackLdapPath != null)
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

## <a name="next-steps"></a><span data-ttu-id="3d51a-151">后续步骤</span><span class="sxs-lookup"><span data-stu-id="3d51a-151">Next steps</span></span>
<span data-ttu-id="3d51a-152"><a name="bk_NextSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="3d51a-152"><a name="bk_NextSteps"> </a></span></span>

<span data-ttu-id="3d51a-153">自动发现过程中的下一步是将自动发现请求发送到找到的 Url，从优先级为1的 Url 开始，然后是优先级2个 url，最后是优先级为3的 Url。</span><span class="sxs-lookup"><span data-stu-id="3d51a-153">The next step in the Autodiscover process is to send Autodiscover requests to the URLs that you found, starting with priority 1 URLs, then priority 2 URLs, and finally priority 3 URLs.</span></span> <span data-ttu-id="3d51a-154">若要了解有关如何发送自动发现请求和处理响应的详细信息，请阅读以下文章：</span><span class="sxs-lookup"><span data-stu-id="3d51a-154">To learn more about how to send Autodiscover requests and handle responses, read the following articles:</span></span>
  
- [<span data-ttu-id="3d51a-155">使用自动发现从 Exchange 获取用户设置</span><span class="sxs-lookup"><span data-stu-id="3d51a-155">Get user settings from Exchange by using Autodiscover</span></span>](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    
- [<span data-ttu-id="3d51a-156">处理自动发现错误消息</span><span class="sxs-lookup"><span data-stu-id="3d51a-156">Handling Autodiscover error messages</span></span>](handling-autodiscover-error-messages.md)
    
## <a name="see-also"></a><span data-ttu-id="3d51a-157">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3d51a-157">See also</span></span>

- [<span data-ttu-id="3d51a-158">Exchange 自动发现</span><span class="sxs-lookup"><span data-stu-id="3d51a-158">Autodiscover for Exchange</span></span>](autodiscover-for-exchange.md)   
- [<span data-ttu-id="3d51a-159">设置 EWS 应用程序</span><span class="sxs-lookup"><span data-stu-id="3d51a-159">Setting up your EWS application</span></span>](setting-up-your-ews-application.md)
    

