---
title: 使用 Exchange 命令行管理程序获取邮件用户列表
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.assetid: 8b790dc8-5c4f-4acf-bbe7-63523395fbe7
description: 了解如何使用 Exchange 命令行管理程序 cmdlet 来创建可返回 Exchange 邮箱用户列表的工具。
localization_priority: Priority
ms.openlocfilehash: 817d92ef1bb88017f471681b448c052ecaa54e7e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44435707"
---
# <a name="get-a-list-of-mail-users-by-using-the-exchange-management-shell"></a><span data-ttu-id="add63-103">使用 Exchange 命令行管理程序获取邮件用户列表</span><span class="sxs-lookup"><span data-stu-id="add63-103">Get a list of mail users by using the Exchange Management Shell</span></span>

<span data-ttu-id="add63-104">了解如何使用 Exchange 命令行管理程序 cmdlet 来创建可返回 Exchange 邮箱用户列表的工具。</span><span class="sxs-lookup"><span data-stu-id="add63-104">Learn how to use Exchange Management Shell cmdlets to create a tool that returns a list of Exchange mailbox users.</span></span>
  
<span data-ttu-id="add63-105">**适用于：** Exchange Online |Exchange Server 2013 |Office 365</span><span class="sxs-lookup"><span data-stu-id="add63-105">**Applies to:** Exchange Online | Exchange Server 2013 | Office 365</span></span> 
  
<span data-ttu-id="add63-106">通过使用调用 Exchange 命令行管理程序 cmdlet 的托管工具，从 Exchange Online、Exchange Online （Office 365 的一部分）或从 Exchange 2013 开始的 Exchange 版本获取用户列表是一个包含两个步骤的过程。</span><span class="sxs-lookup"><span data-stu-id="add63-106">Getting a list of users from Exchange Online, Exchange Online as part of Office 365, or a version of Exchange starting with Exchange 2013 by using a managed tool that calls an Exchange Management Shell cmdlet is a two-step process.</span></span> <span data-ttu-id="add63-107">首先，在 Exchange 服务器上建立远程运行空间;然后，运行 cmdlet 以检索远程运行空间中的用户信息。</span><span class="sxs-lookup"><span data-stu-id="add63-107">First, you establish a remote runspace on an Exchange server; then, you run the cmdlet to retrieve the user information in the remote runspace.</span></span> 

<span data-ttu-id="add63-108">若要连接到远程运行空间，必须使用符合组织的安全要求的身份验证方案对 Exchange 服务器进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="add63-108">To connect to the remote runspace, you have to authenticate with the Exchange server by using the authentication scheme that meets the security requirements of your organization.</span></span> 

<span data-ttu-id="add63-109">本文提供了可用于设置远程运行空间并运行 Exchange 命令行管理程序 cmdlet 以从 Exchange 服务器获取用户列表的代码示例。</span><span class="sxs-lookup"><span data-stu-id="add63-109">This article provides code examples that you can use to set up a remote runspace and run an Exchange Management Shell cmdlet to get a list of users from an Exchange server.</span></span>

<span data-ttu-id="add63-110"><a name="bk_prerequisites"> </a></span><span class="sxs-lookup"><span data-stu-id="add63-110"><a name="bk_prerequisites"> </a></span></span>

## <a name="prerequisites-for-getting-a-list-of-mailbox-users"></a><span data-ttu-id="add63-111">获取邮箱用户列表的先决条件</span><span class="sxs-lookup"><span data-stu-id="add63-111">Prerequisites for getting a list of mailbox users</span></span>

<span data-ttu-id="add63-112">若要执行此任务，您需要一个对以下命名空间的引用：</span><span class="sxs-lookup"><span data-stu-id="add63-112">To perform this task, you need a reference to the following namespaces:</span></span>
  
- <span data-ttu-id="add63-113">**ObjectModel**</span><span class="sxs-lookup"><span data-stu-id="add63-113">**System.Collections.ObjectModel**</span></span>
- <span data-ttu-id="add63-114">**系统管理。自动化**</span><span class="sxs-lookup"><span data-stu-id="add63-114">**System.Management.Automation**</span></span>
- <span data-ttu-id="add63-115">**系统管理. Remoting**</span><span class="sxs-lookup"><span data-stu-id="add63-115">**System.Management.Automation.Remoting**</span></span>
- <span data-ttu-id="add63-116">**系统管理. 自动化**</span><span class="sxs-lookup"><span data-stu-id="add63-116">**System.Management.Automation.Runspaces**</span></span>
    
> [!NOTE]
>  <span data-ttu-id="add63-117">使用 Visual Studio 创建应用程序时，必须在项目中添加对 system.string 程序集的引用。</span><span class="sxs-lookup"><span data-stu-id="add63-117">When you are using Visual Studio to create an application, you must add a reference to the System.Management.Automation.dll assembly to the project.</span></span> <span data-ttu-id="add63-118">可以在以下位置之一找到程序集：</span><span class="sxs-lookup"><span data-stu-id="add63-118">The assembly can be found in one of the following locations:</span></span>
> - <span data-ttu-id="add63-119">对于 Windows XP 和 Windows Vista 操作系统，Windows PowerShell 安装目录（$PSHOME）。</span><span class="sxs-lookup"><span data-stu-id="add63-119">For Windows XP and Windows Vista operating systems, the Windows PowerShell installation directory ($PSHOME).</span></span>
> - <span data-ttu-id="add63-120">对于 Windows 7 和 Windows 8 操作系统，以下文件夹： Windows\assembly\ GAC_MSIL \System.Management.Automation。</span><span class="sxs-lookup"><span data-stu-id="add63-120">For the Windows 7 and Windows 8 operating systems, the following folder: Windows\assembly\GAC_MSIL\System.Management.Automation.</span></span> 
  
<span data-ttu-id="add63-121">请勿将 Exchange 2013 管理管理单元加载到运行自动执行 Exchange 命令行管理程序 cmdlet 的应用程序的计算机上的运行空间中。</span><span class="sxs-lookup"><span data-stu-id="add63-121">Do not load the Exchange 2013 Management snap-in into the runspace on computers that are running applications that automate Exchange Management Shell cmdlets.</span></span> <span data-ttu-id="add63-122">应用程序应改为创建一个远程运行空间，如本文后面所述。</span><span class="sxs-lookup"><span data-stu-id="add63-122">The application should instead create a remote runspace, as described later in this article.</span></span>

<span data-ttu-id="add63-123"><a name="bk_gettinglistmailbox"> </a></span><span class="sxs-lookup"><span data-stu-id="add63-123"><a name="bk_gettinglistmailbox"> </a></span></span>

## <a name="connect-to-a-remote-runspace-on-an-exchange-server"></a><span data-ttu-id="add63-124">连接到 Exchange 服务器上的远程运行空间</span><span class="sxs-lookup"><span data-stu-id="add63-124">Connect to a remote runspace on an Exchange server</span></span>

<span data-ttu-id="add63-125">您用来连接到远程运行空间以使用 Exchange 命令行管理程序 cmdlet 的方法因所使用的身份验证方案而异。</span><span class="sxs-lookup"><span data-stu-id="add63-125">The method that you use to connect to a remote runspace to use an Exchange Management Shell cmdlet varies based on the authentication scheme that you are using.</span></span> <span data-ttu-id="add63-126">本节提供的代码示例演示如何在使用下表中列出的身份验证方法时连接到远程运行空间。</span><span class="sxs-lookup"><span data-stu-id="add63-126">This section provides code examples that show how to connect to a remote runspace when you are using an authentication method listed in the following table.</span></span>
  
|<span data-ttu-id="add63-127">**身份验证方法**</span><span class="sxs-lookup"><span data-stu-id="add63-127">**Authentication method**</span></span>|<span data-ttu-id="add63-128">**适用于**</span><span class="sxs-lookup"><span data-stu-id="add63-128">**Applies to**</span></span>|<span data-ttu-id="add63-129">**URI**</span><span class="sxs-lookup"><span data-stu-id="add63-129">**URI**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="add63-130">使用基本身份验证连接到 Exchange Online 上的远程运行空间</span><span class="sxs-lookup"><span data-stu-id="add63-130">Connect to a remote runspace on Exchange Online by using basic authentication</span></span>](#bk_basic) <br/> |<span data-ttu-id="add63-131">Exchange Online 服务器</span><span class="sxs-lookup"><span data-stu-id="add63-131">Exchange Online servers</span></span>  <br/> |`https://outlook.office365.com/PowerShell-LiveID`<br/><br/>`https://<server>/PowerShell-LiveID`  <br/> |
|[<span data-ttu-id="add63-132">使用证书身份验证连接到远程运行空间</span><span class="sxs-lookup"><span data-stu-id="add63-132">Connect to a remote runspace by using certificate authentication</span></span>](#bk_cert) <br/> |<span data-ttu-id="add63-133">Exchange Online 和 Exchange 本地服务器</span><span class="sxs-lookup"><span data-stu-id="add63-133">Exchange Online and Exchange on-premises servers</span></span>  <br/> |`https://outlook.office365.com/PowerShell`<br/><br/>`https://<server>/PowerShell`<br/><br/>`http://<server>/PowerShell`  <br/> |
|[<span data-ttu-id="add63-134">使用 Kerberos 身份验证连接到 Exchange 服务器上的远程运行空间</span><span class="sxs-lookup"><span data-stu-id="add63-134">Connect to a remote runspace on an Exchange server by using Kerberos authentication</span></span>](#bk_Kerberos) <br/> |<span data-ttu-id="add63-135">Exchange Online 和 Exchange 本地服务器</span><span class="sxs-lookup"><span data-stu-id="add63-135">Exchange Online and Exchange on-premises servers</span></span>  <br/> |`https://<server>/PowerShell`<br/><br/>`http://<server>/PowerShell`  <br/> |

<span data-ttu-id="add63-136"><a name="bk_basic"> </a></span><span class="sxs-lookup"><span data-stu-id="add63-136"><a name="bk_basic"> </a></span></span>

### <a name="connect-to-a-remote-runspace-on-exchange-online-by-using-basic-authentication"></a><span data-ttu-id="add63-137">使用基本身份验证连接到 Exchange Online 上的远程运行空间</span><span class="sxs-lookup"><span data-stu-id="add63-137">Connect to a remote runspace on Exchange Online by using basic authentication</span></span>

<span data-ttu-id="add63-138">下面的代码示例定义了**GetUsersUsingBasicAuth**方法，该方法通过使用基本身份验证在远程 Exchange Online 服务器上创建 Exchange 命令行管理程序运行空间。</span><span class="sxs-lookup"><span data-stu-id="add63-138">The following code example defines the **GetUsersUsingBasicAuth** method, which creates an Exchange Management Shell runspace on a remote Exchange Online server by using basic authentication.</span></span> <span data-ttu-id="add63-139">然后，此方法调用**GetUserInformation**方法，如部分中所定义的，[从远程运行空间获取邮箱用户的列表](#bk_remote)，以返回远程服务器上的用户列表。</span><span class="sxs-lookup"><span data-stu-id="add63-139">The method then calls the **GetUserInformation** method, as defined in the section [Get a list of mailbox users from a remote runspace](#bk_remote), to return a list of users on the remote server.</span></span>
  
<span data-ttu-id="add63-140">此方法需要以下参数：</span><span class="sxs-lookup"><span data-stu-id="add63-140">This method requires the following parameters:</span></span>
  
-  <span data-ttu-id="add63-141">**liveIDConnectionUri** &ndash;一个字符串，包含将对应用程序进行身份验证的 Exchange Online 服务器的 URI。</span><span class="sxs-lookup"><span data-stu-id="add63-141">**liveIDConnectionUri** &ndash; A string that contains the URI of the Exchange Online server that will authenticate the application.</span></span> <span data-ttu-id="add63-142">如果 Exchange Online 在 Office 365 中运行，则 URI 为 `https://outlook.office365.com/PowerShell-LiveID` ; 否则为 uri `https://<servername>/PowerShell-LiveID` 。</span><span class="sxs-lookup"><span data-stu-id="add63-142">If Exchange Online is running in Office 365, the URI is `https://outlook.office365.com/PowerShell-LiveID`; otherwise, the URI is `https://<servername>/PowerShell-LiveID`.</span></span> 
    
-  <span data-ttu-id="add63-143">**schemaUri** &ndash;一个字符串，其中包含定义 Exchange 命令行管理程序架构的架构文档的 URI。</span><span class="sxs-lookup"><span data-stu-id="add63-143">**schemaUri** &ndash; A string that contains the URI of the schema document that defines the Exchange Management Shell schema.</span></span> <span data-ttu-id="add63-144">架构 URI 为 `https://schemas.microsoft.com/powershell/Microsoft.Exchange` 。</span><span class="sxs-lookup"><span data-stu-id="add63-144">The schema URI is `https://schemas.microsoft.com/powershell/Microsoft.Exchange`.</span></span> 
    
-  <span data-ttu-id="add63-145">**凭据** &ndash;一个[PSCredential](https://msdn.microsoft.com/library/system.management.automation.pscredential%28VS.85%29.aspx)对象，其中包含运行该应用程序的用户的凭据。</span><span class="sxs-lookup"><span data-stu-id="add63-145">**credentials** &ndash; A [PSCredential](https://msdn.microsoft.com/library/system.management.automation.pscredential%28VS.85%29.aspx) object that contains the credentials of the user who is running the application.</span></span> 
    
-  <span data-ttu-id="add63-146">**计数** &ndash;要返回的 Exchange 邮箱用户数。</span><span class="sxs-lookup"><span data-stu-id="add63-146">**count** &ndash; The number of Exchange mailbox users to return.</span></span> 
    
```cs
public Collection<PSObject> GetUsersUsingBasicAuth(
    string liveIDConnectionUri, string schemaUri, PSCredential credentials, int count)
{
    WSManConnectionInfo connectionInfo = new WSManConnectionInfo(
        new Uri(liveIDConnectionUri),
        schemaUri, credentials);
    connectionInfo.AuthenticationMechanism = AuthenticationMechanism.Basic;
    using (Runspace runspace = RunspaceFactory.CreateRunspace(connectionInfo))
    {
        return GetUserInformation(count, runspace);
    }
}
```


```vb
  Function GetUsersUsingBasicAuth( _
    ByVal LiveIDConnectionUri As String, ByVal ScehmaUri As String, _
    ByVal Credentials As PSCredential, ByVal Count As Integer) As Collection(Of PSObject)
    Dim ConnectionInfo As WSManConnectionInfo = _
        New WSManConnectionInfo(New Uri(LiveIDConnectionUri), ScehmaUri, Credentials)
    ConnectionInfo.AuthenticationMechanism = AuthenticationMechanism.Basic
    Dim RemoteRunspace As Runspace
    RemoteRunspace = RunspaceFactory.CreateRunspace(ConnectionInfo)
    Return GetUserInformation(Count, RemoteRunspace)
  End Function

```

<span data-ttu-id="add63-147"><a name="bk_cert"> </a></span><span class="sxs-lookup"><span data-stu-id="add63-147"><a name="bk_cert"> </a></span></span>

### <a name="connect-to-a-remote-runspace-by-using-certificate-authentication"></a><span data-ttu-id="add63-148">使用证书身份验证连接到远程运行空间</span><span class="sxs-lookup"><span data-stu-id="add63-148">Connect to a remote runspace by using certificate authentication</span></span>

<span data-ttu-id="add63-149">下面的代码示例定义了**GetUsersUsingCertificate**方法，该方法通过使用证书在远程服务器上创建 Exchange 命令行管理程序运行空间。</span><span class="sxs-lookup"><span data-stu-id="add63-149">The following code example defines the **GetUsersUsingCertificate** method, which creates an Exchange Management Shell runspace on a remote server by using a certificate.</span></span> <span data-ttu-id="add63-150">然后，此方法调用**GetUserInformation**方法，如部分中所定义的，[从远程运行空间获取邮箱用户的列表](#bk_remote)，以返回远程服务器上的用户列表。</span><span class="sxs-lookup"><span data-stu-id="add63-150">The method then calls the **GetUserInformation** method, as defined in the section [Get a list of mailbox users from a remote runspace](#bk_remote), to return a list of users on the remote server.</span></span>
  
<span data-ttu-id="add63-151">此方法需要以下参数：</span><span class="sxs-lookup"><span data-stu-id="add63-151">This method requires the following parameters:</span></span>
  
-  <span data-ttu-id="add63-152">**指纹** &ndash;一个字符串，其中包含用于对应用程序进行身份验证的证书的指纹。</span><span class="sxs-lookup"><span data-stu-id="add63-152">**thumbprint** &ndash; A string that contains the thumbprint of the certificate that is used to authenticate the application.</span></span> 
    
-  <span data-ttu-id="add63-153">**certConnectionUri** &ndash;一个字符串，包含将对证书进行身份验证的服务器的 URI。</span><span class="sxs-lookup"><span data-stu-id="add63-153">**certConnectionUri** &ndash; A string that contains the URI of the server that will authenticate the certificate.</span></span> <span data-ttu-id="add63-154">URI 将是下表中列出的 URI 之一。</span><span class="sxs-lookup"><span data-stu-id="add63-154">The URI will be one of those listed in the following table.</span></span> 
    
    <span data-ttu-id="add63-155">**表1。certConnectionUri Uri**</span><span class="sxs-lookup"><span data-stu-id="add63-155">**Table 1. certConnectionUri URIs**</span></span>

    |<span data-ttu-id="add63-156">**Server**</span><span class="sxs-lookup"><span data-stu-id="add63-156">**Server**</span></span>|<span data-ttu-id="add63-157">**URI**</span><span class="sxs-lookup"><span data-stu-id="add63-157">**URI**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="add63-158">不使用 SSL 的 Exchange server</span><span class="sxs-lookup"><span data-stu-id="add63-158">Exchange server without using SSL</span></span>  <br/> |`http://<servername>/PowerShell`  <br/> |
    |<span data-ttu-id="add63-159">使用 SSL 的 Exchange 服务器</span><span class="sxs-lookup"><span data-stu-id="add63-159">Exchange server using SSL</span></span>  <br/> |`https://<servername>/PowerShell`  <br/> |
    |<span data-ttu-id="add63-160">作为 Office 365 的一部分的 Exchange Online</span><span class="sxs-lookup"><span data-stu-id="add63-160">Exchange Online as part of Office 365</span></span>  <br/> |`https://outlook.office365.com/PowerShell`  <br/> |
   
- <span data-ttu-id="add63-161">**schemaUri** &ndash;一个字符串，其中包含定义 Exchange 命令行管理程序架构的架构文档的 URI。</span><span class="sxs-lookup"><span data-stu-id="add63-161">**schemaUri** &ndash; A string that contains the URI of the schema document that defines the Exchange Management Shell schema.</span></span> <span data-ttu-id="add63-162">架构 URI 为 https://schemas.microsoft.com/powershell/Microsoft.Exchange 。</span><span class="sxs-lookup"><span data-stu-id="add63-162">The schema URI is https://schemas.microsoft.com/powershell/Microsoft.Exchange.</span></span> 
    
- <span data-ttu-id="add63-163">**计数** &ndash;要返回的 Exchange 邮箱用户数。</span><span class="sxs-lookup"><span data-stu-id="add63-163">**count** &ndash; The number of Exchange mailbox users to return.</span></span> 
    
```cs
public Collection<PSObject> GetUsersUsingCertificate(
    string thumbprint, string certConnectionUri, string schemaUri, int count)
{
    WSManConnectionInfo connectionInfo = new WSManConnectionInfo(
        new Uri(certConnectionUri),
        schemaUri,
        thumbprint)
    using (Runspace runspace = RunspaceFactory.CreateRunspace(connectionInfo))
    {
        return GetUserInformation(count, runspace);
    }
}
```


```vb
  Function GetUsersUsingCertificate( _
    ByVal Thumbprint As String, ByVal CertConnectionUri As String, _
    ByVal SchemaUri As String, ByVal Count As Integer) As Collection(Of PSObject)
    Dim ConnectionInfo As WSManConnectionInfo
    ConnectionInfo = New WSManConnectionInfo(New Uri(CertConnectionUri), SchemaUri, Thumbprint)
    Dim RemoteRunspace As Runspace
    RemoteRunspace = RunspaceFactory.CreateRunspace(ConnectionInfo)
    Return GetUserInformation(Count, RemoteRunspace)
  End Function

```

<span data-ttu-id="add63-164"><a name="bk_Kerberos"> </a></span><span class="sxs-lookup"><span data-stu-id="add63-164"><a name="bk_Kerberos"> </a></span></span>

### <a name="connect-to-a-remote-runspace-on-an-exchange-server-by-using-kerberos-authentication"></a><span data-ttu-id="add63-165">使用 Kerberos 身份验证连接到 Exchange 服务器上的远程运行空间</span><span class="sxs-lookup"><span data-stu-id="add63-165">Connect to a remote runspace on an Exchange server by using Kerberos authentication</span></span>

<span data-ttu-id="add63-166">下面的代码示例定义了**GetUsersUsingKerberos**方法，该方法通过使用 Kerberos 身份验证在远程服务器上创建 Exchange 命令行管理程序运行空间。</span><span class="sxs-lookup"><span data-stu-id="add63-166">The following code example defines the **GetUsersUsingKerberos** method, which creates an Exchange Management Shell runspace on a remote server by using Kerberos authentication.</span></span> <span data-ttu-id="add63-167">然后，此方法调用**GetUserInformation**方法，如部分中所定义的，[从远程运行空间获取邮箱用户的列表](#bk_remote)，以返回远程服务器上的用户列表。</span><span class="sxs-lookup"><span data-stu-id="add63-167">The method then calls the **GetUserInformation** method, as defined in the section [Get a list of mailbox users from a remote runspace](#bk_remote), to return a list of users on the remote server.</span></span>
  
<span data-ttu-id="add63-168">此方法需要以下参数：</span><span class="sxs-lookup"><span data-stu-id="add63-168">This method requires the following parameters:</span></span>
  
- <span data-ttu-id="add63-169">**kerberosUri** &ndash;一个字符串，包含将对应用程序进行身份验证的 Kerberos 服务器的 URI。</span><span class="sxs-lookup"><span data-stu-id="add63-169">**kerberosUri** &ndash; A string that contains the URI of the Kerberos server that will authenticate the application.</span></span> <span data-ttu-id="add63-170">URI 将是下表中列出的 URI 之一。</span><span class="sxs-lookup"><span data-stu-id="add63-170">The URI will be one of those listed in the following table.</span></span> 
    
    <span data-ttu-id="add63-171">**表2。kerberosUri Uri**</span><span class="sxs-lookup"><span data-stu-id="add63-171">**Table 2. kerberosUri URIs**</span></span>

    |<span data-ttu-id="add63-172">**Server**</span><span class="sxs-lookup"><span data-stu-id="add63-172">**Server**</span></span>|<span data-ttu-id="add63-173">**URI**</span><span class="sxs-lookup"><span data-stu-id="add63-173">**URI**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="add63-174">不使用 SSL 的 Exchange server</span><span class="sxs-lookup"><span data-stu-id="add63-174">Exchange server without using SSL</span></span>  <br/> |`http://<servername>/PowerShell`  <br/> |
    |<span data-ttu-id="add63-175">使用 SSL 的 Exchange 服务器</span><span class="sxs-lookup"><span data-stu-id="add63-175">Exchange server using SSL</span></span>  <br/> |`https://<servername>/PowerShell`  <br/> |
   
- <span data-ttu-id="add63-176">**schemaUri** &ndash;一个字符串，其中包含定义 Exchange 命令行管理程序架构的架构文档的 URI。</span><span class="sxs-lookup"><span data-stu-id="add63-176">**schemaUri** &ndash; A string that contains the URI of the schema document that defines the Exchange Management Shell schema.</span></span> <span data-ttu-id="add63-177">架构 URI 为 https://schemas.microsoft.com/powershell/Microsoft.Exchange 。</span><span class="sxs-lookup"><span data-stu-id="add63-177">The schema URI is https://schemas.microsoft.com/powershell/Microsoft.Exchange.</span></span> 
    
- <span data-ttu-id="add63-178">**凭据** &ndash;一个[PSCredential](https://msdn.microsoft.com/library/system.management.automation.pscredential%28VS.85%29.aspx)对象，其中包含运行该应用程序的用户的凭据。</span><span class="sxs-lookup"><span data-stu-id="add63-178">**credentials** &ndash; A [PSCredential](https://msdn.microsoft.com/library/system.management.automation.pscredential%28VS.85%29.aspx) object that contains the credentials of the user who is running the application.</span></span> 
    
- <span data-ttu-id="add63-179">**计数** &ndash;要返回的 Exchange 邮箱用户数。</span><span class="sxs-lookup"><span data-stu-id="add63-179">**count** &ndash; The number of Exchange mailbox users to return.</span></span> 
    
```cs
public Collection<PSObject> GetUsersUsingKerberos(
    string kerberosUri, string schemaUri, PSCredential credentials, int count)
{
    WSManConnectionInfo connectionInfo = new WSManConnectionInfo(
        new Uri(kerberosUri),
        schemaUri, credentials);
    connectionInfo.AuthenticationMechanism = AuthenticationMechanism.Kerberos;
    using (Runspace runspace = RunspaceFactory.CreateRunspace(connectionInfo))
    {
        return GetUserInformation(count, runspace);
    }
}
```

```vb
  Function GetUsersUsingKerberos( _
    ByVal KerberosUri As String, ByVal ScehmaUri As String, _
    ByVal Credentials As PSCredential, ByVal Count As Integer) As Collection(Of PSObject)
    Dim ConnectionInfo As WSManConnectionInfo = _
        New WSManConnectionInfo(New Uri(KerberosUri), ScehmaUri, Credentials)
    ConnectionInfo.AuthenticationMechanism = AuthenticationMechanism.Kerberos
    Dim RemoteRunspace As Runspace
    RemoteRunspace = RunspaceFactory.CreateRunspace(ConnectionInfo)
    Return GetUserInformation(Count, RemoteRunspace)
  End Function

```

<span data-ttu-id="add63-180"><a name="bk_remote"> </a></span><span class="sxs-lookup"><span data-stu-id="add63-180"><a name="bk_remote"> </a></span></span>

## <a name="get-a-list-of-mailbox-users-from-a-remote-runspace"></a><span data-ttu-id="add63-181">从远程运行空间获取邮箱用户的列表</span><span class="sxs-lookup"><span data-stu-id="add63-181">Get a list of mailbox users from a remote runspace</span></span>

<span data-ttu-id="add63-182">下面的代码示例定义了**GetUserInformation**方法，该方法返回代表 Exchange 邮箱用户的[PSObject](https://msdn.microsoft.com/library/system.management.automation.pscredential%28VS.85%29.aspx)实例的集合。</span><span class="sxs-lookup"><span data-stu-id="add63-182">The following code example defines the **GetUserInformation** method, which returns a collection of [PSObject](https://msdn.microsoft.com/library/system.management.automation.pscredential%28VS.85%29.aspx) instances that represent Exchange mailbox users.</span></span> <span data-ttu-id="add63-183">此方法由**GetUsersUsingBasicAuth**、 **GetUsersUsingCertificate**和**GetUsersUsingKerberos**方法调用，以返回远程服务器上的用户列表。</span><span class="sxs-lookup"><span data-stu-id="add63-183">This method is called by the **GetUsersUsingBasicAuth**, **GetUsersUsingCertificate**, and **GetUsersUsingKerberos** methods to return the list of users from the remote server.</span></span> 
  
<span data-ttu-id="add63-184">此方法需要以下参数：</span><span class="sxs-lookup"><span data-stu-id="add63-184">This method requires the following parameters:</span></span>
  
- <span data-ttu-id="add63-185">**计数** &ndash;要返回的 Exchange 邮箱用户数。</span><span class="sxs-lookup"><span data-stu-id="add63-185">**count** &ndash; The number of Exchange mailbox users to return.</span></span> 
    
- <span data-ttu-id="add63-186">**运行空间** &ndash;为远程 Exchange 服务器建立的远程运行空间。</span><span class="sxs-lookup"><span data-stu-id="add63-186">**runspace** &ndash; The remote runspace that is established for the remote Exchange server.</span></span> 
    
```cs
public Collection<PSObject> GetUserInformation(int count, Runspace runspace)
{
    using (PowerShell powershell = PowerShell.Create())
    {
        powershell.AddCommand("Get-Users");
        powershell.AddParameter("ResultSize", count);
        runspace.Open();
        powershell.Runspace = runspace;
        return powershell.Invoke();
    }
}
```

```vb
Function GetUserInformation(ByVal Count As Integer, ByVal RemoteRunspace As Runspace) As Collection(Of PSObject)
    Dim RemotePowerShell As PowerShell = PowerShell.Create
    RemotePowerShell.AddCommand("Get-Users")
    RemotePowerShell.AddParameter("ResultSize", Count)
    ' Open the remote runspace on the server.
    RemoteRunspace.Open()
    ' Associate the runspace with the Exchange Management Shell.
    RemotePowerShell.Runspace = RemoteRunspace
    ' Invoke the Exchange Management Shell to run the command.
    Return RemotePowerShell.Invoke
End Function

```

<span data-ttu-id="add63-187">**GetUserInformation**方法将返回的邮箱用户数不会超过_count_ 。</span><span class="sxs-lookup"><span data-stu-id="add63-187">The **GetUserInformation** method will return no more than  _count_ mailbox users.</span></span> <span data-ttu-id="add63-188">若要简化此示例的代码，该方法不会筛选或限制返回的邮箱用户。</span><span class="sxs-lookup"><span data-stu-id="add63-188">To simplify the code for this example, the method does not filter or otherwise limit the mailbox users that are returned.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="add63-189">另请参阅</span><span class="sxs-lookup"><span data-stu-id="add63-189">See also</span></span>

- [<span data-ttu-id="add63-190">创建 Exchange 命令行管理程序工具</span><span class="sxs-lookup"><span data-stu-id="add63-190">Create Exchange Management Shell tools</span></span>](create-exchange-management-shell-tools.md)   
- [<span data-ttu-id="add63-191">使用 Exchange 命令行管理程序 cmdlet 响应</span><span class="sxs-lookup"><span data-stu-id="add63-191">Use the Exchange Management Shell cmdlet response</span></span>](how-to-use-the-exchange-management-shell-cmdlet-response.md)
    

