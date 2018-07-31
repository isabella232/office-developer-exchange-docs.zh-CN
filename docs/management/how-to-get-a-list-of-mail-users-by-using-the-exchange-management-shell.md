---
title: 使用 Exchange 命令行管理程序中获取邮件用户的列表
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8b790dc8-5c4f-4acf-bbe7-63523395fbe7
description: 了解如何使用 Exchange 命令行管理程序 cmdlet 创建一个工具，返回的 Exchange 邮箱用户列表。
ms.openlocfilehash: e9493571e98760e5a11674db9a552111c1ec29b2
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353999"
---
# <a name="get-a-list-of-mail-users-by-using-the-exchange-management-shell"></a><span data-ttu-id="3bb9c-103">使用 Exchange 命令行管理程序中获取邮件用户的列表</span><span class="sxs-lookup"><span data-stu-id="3bb9c-103">Get a list of mail users by using the Exchange Management Shell</span></span>

<span data-ttu-id="3bb9c-104">了解如何使用 Exchange 命令行管理程序 cmdlet 创建一个工具，返回的 Exchange 邮箱用户列表。</span><span class="sxs-lookup"><span data-stu-id="3bb9c-104">Learn how to use Exchange Management Shell cmdlets to create a tool that returns a list of Exchange mailbox users.</span></span>
  
<span data-ttu-id="3bb9c-105">**适用于：** Exchange Online |Exchange Server 2013 |Office 365</span><span class="sxs-lookup"><span data-stu-id="3bb9c-105">**Applies to:** Exchange Online | Exchange Server 2013 | Office 365</span></span> 
  
<span data-ttu-id="3bb9c-106">从 Exchange Online 中获取用户的列表，Exchange Online 作为 Office 365 的一部分或的开头使用调用 Exchange 命令行管理程序 cmdlet 的管理的工具的 Exchange 2013 的 Exchange 版本是一个两步过程。</span><span class="sxs-lookup"><span data-stu-id="3bb9c-106">Getting a list of users from Exchange Online, Exchange Online as part of Office 365, or a version of Exchange starting with Exchange 2013 by using a managed tool that calls an Exchange Management Shell cmdlet is a two-step process.</span></span> <span data-ttu-id="3bb9c-107">首先，建立在 Exchange server; 上的远程运行空间然后，运行此 cmdlet 检索远程运行空间中的用户信息。</span><span class="sxs-lookup"><span data-stu-id="3bb9c-107">First, you establish a remote runspace on an Exchange server; then, you run the cmdlet to retrieve the user information in the remote runspace.</span></span> 

<span data-ttu-id="3bb9c-108">若要连接到远程运行空间，您必须使用满足组织的安全要求的身份验证方案与 Exchange server 身份验证。</span><span class="sxs-lookup"><span data-stu-id="3bb9c-108">To connect to the remote runspace, you have to authenticate with the Exchange server by using the authentication scheme that meets the security requirements of your organization.</span></span> 

<span data-ttu-id="3bb9c-109">本文提供了可用于设置远程运行空间和运行 Exchange 命令行管理程序 cmdlet 可从 Exchange 服务器获取用户的列表的代码示例。</span><span class="sxs-lookup"><span data-stu-id="3bb9c-109">This article provides code examples that you can use to set up a remote runspace and run an Exchange Management Shell cmdlet to get a list of users from an Exchange server.</span></span>

<span data-ttu-id="3bb9c-110"><a name="bk_prerequisites"> </a></span><span class="sxs-lookup"><span data-stu-id="3bb9c-110"></span></span>

## <a name="prerequisites-for-getting-a-list-of-mailbox-users"></a><span data-ttu-id="3bb9c-111">获取列表的邮箱用户的先决条件</span><span class="sxs-lookup"><span data-stu-id="3bb9c-111">Prerequisites for getting a list of mailbox users</span></span>

<span data-ttu-id="3bb9c-112">若要执行此任务，您需要对以下命名空间的引用：</span><span class="sxs-lookup"><span data-stu-id="3bb9c-112">To perform this task, you need a reference to the following namespaces:</span></span>
  
- <span data-ttu-id="3bb9c-113">**System.Collections.ObjectModel**</span><span class="sxs-lookup"><span data-stu-id="3bb9c-113">**System.Collections.ObjectModel**</span></span>
- <span data-ttu-id="3bb9c-114">**System.Management.Automation**</span><span class="sxs-lookup"><span data-stu-id="3bb9c-114">**System.Management.Automation**</span></span>
- <span data-ttu-id="3bb9c-115">**System.Management.Automation.Remoting**</span><span class="sxs-lookup"><span data-stu-id="3bb9c-115">**System.Management.Automation.Remoting**</span></span>
- <span data-ttu-id="3bb9c-116">**System.Management.Automation.Runspaces**</span><span class="sxs-lookup"><span data-stu-id="3bb9c-116">**System.Management.Automation.Runspaces**</span></span>
    
> [!NOTE]
>  <span data-ttu-id="3bb9c-117">当您使用 Visual Studio 创建应用程序时，您必须将 System.Management.Automation.dll 程序集的引用添加到项目中。</span><span class="sxs-lookup"><span data-stu-id="3bb9c-117">When you are using Visual Studio to create an application, you must add a reference to the System.Management.Automation.dll assembly to the project.</span></span> <span data-ttu-id="3bb9c-118">可以在以下位置之一找到程序集：</span><span class="sxs-lookup"><span data-stu-id="3bb9c-118">The assembly can be found in one of the following locations:</span></span>
> - <span data-ttu-id="3bb9c-119">对于 Windows XP 和 Windows Vista 操作系统，Windows PowerShell 安装目录 ($PSHOME)。</span><span class="sxs-lookup"><span data-stu-id="3bb9c-119">For Windows XP and Windows Vista operating systems, the Windows PowerShell installation directory ($PSHOME).</span></span>
> - <span data-ttu-id="3bb9c-120">对于 Windows 7 和 Windows 8 操作系统，以下文件夹： Windows\assembly\GAC_MSIL\System.Management.Automation。</span><span class="sxs-lookup"><span data-stu-id="3bb9c-120">For the Windows 7 and Windows 8 operating systems, the following folder: Windows\assembly\GAC_MSIL\System.Management.Automation.</span></span> 
  
<span data-ttu-id="3bb9c-121">不会加载 Exchange 2013 管理管理单元中运行的应用程序自动执行 Exchange 命令行管理程序 cmdlet 的计算机上运行空间到。</span><span class="sxs-lookup"><span data-stu-id="3bb9c-121">Do not load the Exchange 2013 Management snap-in into the runspace on computers that are running applications that automate Exchange Management Shell cmdlets.</span></span> <span data-ttu-id="3bb9c-122">下文中所述，应用程序而是应创建远程运行空间。</span><span class="sxs-lookup"><span data-stu-id="3bb9c-122">The application should instead create a remote runspace, as described later in this article.</span></span>

<span data-ttu-id="3bb9c-123"><a name="bk_gettinglistmailbox"> </a></span><span class="sxs-lookup"><span data-stu-id="3bb9c-123"></span></span>

## <a name="connect-to-a-remote-runspace-on-an-exchange-server"></a><span data-ttu-id="3bb9c-124">连接到 Exchange 服务器上远程运行空间</span><span class="sxs-lookup"><span data-stu-id="3bb9c-124">Connect to a remote runspace on an Exchange server</span></span>

<span data-ttu-id="3bb9c-125">用于连接到远程运行空间用于 Exchange Management Shell cmdlet 会有所不同，该方法根据您使用的身份验证方案。</span><span class="sxs-lookup"><span data-stu-id="3bb9c-125">The method that you use to connect to a remote runspace to use an Exchange Management Shell cmdlet varies based on the authentication scheme that you are using.</span></span> <span data-ttu-id="3bb9c-126">本节提供代码示例演示如何使用下表中列出的身份验证方法时，连接到远程运行空间。</span><span class="sxs-lookup"><span data-stu-id="3bb9c-126">This section provides code examples that show how to connect to a remote runspace when you are using an authentication method listed in the following table.</span></span>
  
|<span data-ttu-id="3bb9c-127">**身份验证方法**</span><span class="sxs-lookup"><span data-stu-id="3bb9c-127">**Authentication method**</span></span>|<span data-ttu-id="3bb9c-128">**适用于**</span><span class="sxs-lookup"><span data-stu-id="3bb9c-128">**Applies to**</span></span>|<span data-ttu-id="3bb9c-129">**URI**</span><span class="sxs-lookup"><span data-stu-id="3bb9c-129">**URI**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3bb9c-130">使用基本身份验证连接到 Exchange Online 上远程运行空间</span><span class="sxs-lookup"><span data-stu-id="3bb9c-130">Connect to a remote runspace on Exchange Online by using basic authentication</span></span>](#bk_basic) <br/> |<span data-ttu-id="3bb9c-131">Exchange Online 服务器</span><span class="sxs-lookup"><span data-stu-id="3bb9c-131">Exchange Online servers</span></span>  <br/> |`https://outlook.office365.com/PowerShell-LiveID`<br/><br/>`https://<server>/PowerShell-LiveID`  <br/> |
|[<span data-ttu-id="3bb9c-132">使用证书身份验证连接到远程运行空间</span><span class="sxs-lookup"><span data-stu-id="3bb9c-132">Connect to a remote runspace by using certificate authentication</span></span>](#bk_cert) <br/> |<span data-ttu-id="3bb9c-133">Exchange Online 和 Exchange 内部部署服务器</span><span class="sxs-lookup"><span data-stu-id="3bb9c-133">Exchange Online and Exchange on-premises servers</span></span>  <br/> |`https://outlook.office365.com/PowerShell`<br/><br/>`https://<server>/PowerShell`<br/><br/>`http://<server>/PowerShell`  <br/> |
|[<span data-ttu-id="3bb9c-134">使用 Kerberos 身份验证连接到 Exchange 服务器上远程运行空间</span><span class="sxs-lookup"><span data-stu-id="3bb9c-134">Connect to a remote runspace on an Exchange server by using Kerberos authentication</span></span>](#bk_Kerberos) <br/> |<span data-ttu-id="3bb9c-135">Exchange Online 和 Exchange 内部部署服务器</span><span class="sxs-lookup"><span data-stu-id="3bb9c-135">Exchange Online and Exchange on-premises servers</span></span>  <br/> |`https://<server>/PowerShell`<br/><br/>`http://<server>/PowerShell`  <br/> |

<span data-ttu-id="3bb9c-136"><a name="bk_basic"> </a></span><span class="sxs-lookup"><span data-stu-id="3bb9c-136"></span></span>

### <a name="connect-to-a-remote-runspace-on-exchange-online-by-using-basic-authentication"></a><span data-ttu-id="3bb9c-137">使用基本身份验证连接到 Exchange Online 上远程运行空间</span><span class="sxs-lookup"><span data-stu-id="3bb9c-137">Connect to a remote runspace on Exchange Online by using basic authentication</span></span>

<span data-ttu-id="3bb9c-138">下面的代码示例定义**GetUsersUsingBasicAuth**方法，该 Exchange Online 的远程服务器上的 Exchange 命令行管理程序运行空间创建使用基本身份验证方法。</span><span class="sxs-lookup"><span data-stu-id="3bb9c-138">The following code example defines the **GetUsersUsingBasicAuth** method, which creates an Exchange Management Shell runspace on a remote Exchange Online server by using basic authentication.</span></span> <span data-ttu-id="3bb9c-139">该方法然后调用**GetUserInformation**方法中，在[获取从远程运行空间的邮箱用户的列表](#bk_remote)，请部分定义返回远程服务器上的用户列表。</span><span class="sxs-lookup"><span data-stu-id="3bb9c-139">The method then calls the **GetUserInformation** method, as defined in the section [Get a list of mailbox users from a remote runspace](#bk_remote), to return a list of users on the remote server.</span></span>
  
<span data-ttu-id="3bb9c-140">此方法需要以下参数：</span><span class="sxs-lookup"><span data-stu-id="3bb9c-140">This method requires the following parameters:</span></span>
  
-  <span data-ttu-id="3bb9c-141">**liveIDConnectionUri**&ndash;一个字符串，包含 Exchange Online 将验证应用程序的服务器的 URI。</span><span class="sxs-lookup"><span data-stu-id="3bb9c-141">**liveIDConnectionUri** &ndash; A string that contains the URI of the Exchange Online server that will authenticate the application.</span></span> <span data-ttu-id="3bb9c-142">Exchange Online 运行 Office 365 中，如果 URI 是`https://outlook.office365.com/PowerShell-LiveID`;否则，URI 是`https://<servername>/PowerShell-LiveID`。</span><span class="sxs-lookup"><span data-stu-id="3bb9c-142">If Exchange Online is running in Office 365, the URI is `https://outlook.office365.com/PowerShell-LiveID`; otherwise, the URI is `https://<servername>/PowerShell-LiveID`.</span></span> 
    
-  <span data-ttu-id="3bb9c-143">**schemaUri**&ndash;一个字符串，包含定义的 Exchange 命令行管理程序架构的架构文档的 URI。</span><span class="sxs-lookup"><span data-stu-id="3bb9c-143">**schemaUri** &ndash; A string that contains the URI of the schema document that defines the Exchange Management Shell schema.</span></span> <span data-ttu-id="3bb9c-144">Uri 的架构`http://schemas.microsoft.com/powershell/Microsoft.Exchange`。</span><span class="sxs-lookup"><span data-stu-id="3bb9c-144">The schema URI is `http://schemas.microsoft.com/powershell/Microsoft.Exchange`.</span></span> 
    
-  <span data-ttu-id="3bb9c-145">**凭据**&ndash; [PSCredential](http://msdn.microsoft.com/en-us/library/system.management.automation.pscredential%28VS.85%29.aspx)对象，其中包含正在运行应用程序的用户的凭据。</span><span class="sxs-lookup"><span data-stu-id="3bb9c-145">**credentials** &ndash; A [PSCredential](http://msdn.microsoft.com/en-us/library/system.management.automation.pscredential%28VS.85%29.aspx) object that contains the credentials of the user who is running the application.</span></span> 
    
-  <span data-ttu-id="3bb9c-146">**计数**&ndash;的 Exchange 邮箱用户返回数量。</span><span class="sxs-lookup"><span data-stu-id="3bb9c-146">**count** &ndash; The number of Exchange mailbox users to return.</span></span> 
    
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

<span data-ttu-id="3bb9c-147"><a name="bk_cert"> </a></span><span class="sxs-lookup"><span data-stu-id="3bb9c-147"></span></span>

### <a name="connect-to-a-remote-runspace-by-using-certificate-authentication"></a><span data-ttu-id="3bb9c-148">使用证书身份验证连接到远程运行空间</span><span class="sxs-lookup"><span data-stu-id="3bb9c-148">Connect to a remote runspace by using certificate authentication</span></span>

<span data-ttu-id="3bb9c-149">下面的代码示例定义**GetUsersUsingCertificate**方法，通过使用证书创建远程服务器的 Exchange 命令行管理程序运行空间。</span><span class="sxs-lookup"><span data-stu-id="3bb9c-149">The following code example defines the **GetUsersUsingCertificate** method, which creates an Exchange Management Shell runspace on a remote server by using a certificate.</span></span> <span data-ttu-id="3bb9c-150">该方法然后调用**GetUserInformation**方法中，在[获取从远程运行空间的邮箱用户的列表](#bk_remote)，请部分定义返回远程服务器上的用户列表。</span><span class="sxs-lookup"><span data-stu-id="3bb9c-150">The method then calls the **GetUserInformation** method, as defined in the section [Get a list of mailbox users from a remote runspace](#bk_remote), to return a list of users on the remote server.</span></span>
  
<span data-ttu-id="3bb9c-151">此方法需要以下参数：</span><span class="sxs-lookup"><span data-stu-id="3bb9c-151">This method requires the following parameters:</span></span>
  
-  <span data-ttu-id="3bb9c-152">**指纹**&ndash;一个字符串，包含用于验证应用程序证书的指纹。</span><span class="sxs-lookup"><span data-stu-id="3bb9c-152">**thumbprint** &ndash; A string that contains the thumbprint of the certificate that is used to authenticate the application.</span></span> 
    
-  <span data-ttu-id="3bb9c-153">**certConnectionUri**&ndash;一个字符串，包含将身份验证证书的服务器的 URI。</span><span class="sxs-lookup"><span data-stu-id="3bb9c-153">**certConnectionUri** &ndash; A string that contains the URI of the server that will authenticate the certificate.</span></span> <span data-ttu-id="3bb9c-154">URI 将其中一种下表中列出。</span><span class="sxs-lookup"><span data-stu-id="3bb9c-154">The URI will be one of those listed in the following table.</span></span> 
    
    <span data-ttu-id="3bb9c-155">**表 1。certConnectionUri Uri**</span><span class="sxs-lookup"><span data-stu-id="3bb9c-155">**Table 1. certConnectionUri URIs**</span></span>

    |<span data-ttu-id="3bb9c-156">**Server**</span><span class="sxs-lookup"><span data-stu-id="3bb9c-156">**Server**</span></span>|<span data-ttu-id="3bb9c-157">**URI**</span><span class="sxs-lookup"><span data-stu-id="3bb9c-157">**URI**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="3bb9c-158">无需使用 SSL 的 Exchange 服务器</span><span class="sxs-lookup"><span data-stu-id="3bb9c-158">Exchange server without using SSL</span></span>  <br/> |`http://<servername>/PowerShell`  <br/> |
    |<span data-ttu-id="3bb9c-159">使用 SSL 的 Exchange 服务器</span><span class="sxs-lookup"><span data-stu-id="3bb9c-159">Exchange server using SSL</span></span>  <br/> |`https://<servername>/PowerShell`  <br/> |
    |<span data-ttu-id="3bb9c-160">Exchange Online 作为 Office 365 的一部分</span><span class="sxs-lookup"><span data-stu-id="3bb9c-160">Exchange Online as part of Office 365</span></span>  <br/> |`https://outlook.office365.com/PowerShell`  <br/> |
   
- <span data-ttu-id="3bb9c-161">**schemaUri**&ndash;一个字符串，包含定义的 Exchange 命令行管理程序架构的架构文档的 URI。</span><span class="sxs-lookup"><span data-stu-id="3bb9c-161">**schemaUri** &ndash; A string that contains the URI of the schema document that defines the Exchange Management Shell schema.</span></span> <span data-ttu-id="3bb9c-162">Uri 的架构http://schemas.microsoft.com/powershell/Microsoft.Exchange。</span><span class="sxs-lookup"><span data-stu-id="3bb9c-162">The schema URI is http://schemas.microsoft.com/powershell/Microsoft.Exchange.</span></span> 
    
- <span data-ttu-id="3bb9c-163">**计数**&ndash;的 Exchange 邮箱用户返回数量。</span><span class="sxs-lookup"><span data-stu-id="3bb9c-163">**count** &ndash; The number of Exchange mailbox users to return.</span></span> 
    
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

<span data-ttu-id="3bb9c-164"><a name="bk_Kerberos"> </a></span><span class="sxs-lookup"><span data-stu-id="3bb9c-164"></span></span>

### <a name="connect-to-a-remote-runspace-on-an-exchange-server-by-using-kerberos-authentication"></a><span data-ttu-id="3bb9c-165">使用 Kerberos 身份验证连接到 Exchange 服务器上远程运行空间</span><span class="sxs-lookup"><span data-stu-id="3bb9c-165">Connect to a remote runspace on an Exchange server by using Kerberos authentication</span></span>

<span data-ttu-id="3bb9c-166">下面的代码示例定义**GetUsersUsingKerberos**方法，该远程服务器上的 Exchange 命令行管理程序运行空间创建使用 Kerberos 身份验证方法。</span><span class="sxs-lookup"><span data-stu-id="3bb9c-166">The following code example defines the **GetUsersUsingKerberos** method, which creates an Exchange Management Shell runspace on a remote server by using Kerberos authentication.</span></span> <span data-ttu-id="3bb9c-167">该方法然后调用**GetUserInformation**方法中，在[获取从远程运行空间的邮箱用户的列表](#bk_remote)，请部分定义返回远程服务器上的用户列表。</span><span class="sxs-lookup"><span data-stu-id="3bb9c-167">The method then calls the **GetUserInformation** method, as defined in the section [Get a list of mailbox users from a remote runspace](#bk_remote), to return a list of users on the remote server.</span></span>
  
<span data-ttu-id="3bb9c-168">此方法需要以下参数：</span><span class="sxs-lookup"><span data-stu-id="3bb9c-168">This method requires the following parameters:</span></span>
  
- <span data-ttu-id="3bb9c-169">**kerberosUri**&ndash;一个字符串，包含将验证应用程序的 Kerberos 服务器的 URI。</span><span class="sxs-lookup"><span data-stu-id="3bb9c-169">**kerberosUri** &ndash; A string that contains the URI of the Kerberos server that will authenticate the application.</span></span> <span data-ttu-id="3bb9c-170">URI 将其中一种下表中列出。</span><span class="sxs-lookup"><span data-stu-id="3bb9c-170">The URI will be one of those listed in the following table.</span></span> 
    
    <span data-ttu-id="3bb9c-171">**表 2。kerberosUri Uri**</span><span class="sxs-lookup"><span data-stu-id="3bb9c-171">**Table 2. kerberosUri URIs**</span></span>

    |<span data-ttu-id="3bb9c-172">**Server**</span><span class="sxs-lookup"><span data-stu-id="3bb9c-172">**Server**</span></span>|<span data-ttu-id="3bb9c-173">**URI**</span><span class="sxs-lookup"><span data-stu-id="3bb9c-173">**URI**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="3bb9c-174">无需使用 SSL 的 Exchange 服务器</span><span class="sxs-lookup"><span data-stu-id="3bb9c-174">Exchange server without using SSL</span></span>  <br/> |`http://<servername>/PowerShell`  <br/> |
    |<span data-ttu-id="3bb9c-175">使用 SSL 的 Exchange 服务器</span><span class="sxs-lookup"><span data-stu-id="3bb9c-175">Exchange server using SSL</span></span>  <br/> |`https://<servername>/PowerShell`  <br/> |
   
- <span data-ttu-id="3bb9c-176">**schemaUri**&ndash;一个字符串，包含定义的 Exchange 命令行管理程序架构的架构文档的 URI。</span><span class="sxs-lookup"><span data-stu-id="3bb9c-176">**schemaUri** &ndash; A string that contains the URI of the schema document that defines the Exchange Management Shell schema.</span></span> <span data-ttu-id="3bb9c-177">Uri 的架构http://schemas.microsoft.com/powershell/Microsoft.Exchange。</span><span class="sxs-lookup"><span data-stu-id="3bb9c-177">The schema URI is http://schemas.microsoft.com/powershell/Microsoft.Exchange.</span></span> 
    
- <span data-ttu-id="3bb9c-178">**凭据**&ndash; [PSCredential](http://msdn.microsoft.com/en-us/library/system.management.automation.pscredential%28VS.85%29.aspx)对象，其中包含正在运行应用程序的用户的凭据。</span><span class="sxs-lookup"><span data-stu-id="3bb9c-178">**credentials** &ndash; A [PSCredential](http://msdn.microsoft.com/en-us/library/system.management.automation.pscredential%28VS.85%29.aspx) object that contains the credentials of the user who is running the application.</span></span> 
    
- <span data-ttu-id="3bb9c-179">**计数**&ndash;的 Exchange 邮箱用户返回数量。</span><span class="sxs-lookup"><span data-stu-id="3bb9c-179">**count** &ndash; The number of Exchange mailbox users to return.</span></span> 
    
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

<span data-ttu-id="3bb9c-180"><a name="bk_remote"> </a></span><span class="sxs-lookup"><span data-stu-id="3bb9c-180"></span></span>

## <a name="get-a-list-of-mailbox-users-from-a-remote-runspace"></a><span data-ttu-id="3bb9c-181">从远程运行空间获取邮箱用户的列表</span><span class="sxs-lookup"><span data-stu-id="3bb9c-181">Get a list of mailbox users from a remote runspace</span></span>

<span data-ttu-id="3bb9c-182">下面的代码示例定义**GetUserInformation**方法，它返回[PSObject](http://msdn.microsoft.com/en-us/library/system.management.automation.pscredential%28VS.85%29.aspx)实例表示 Exchange 邮箱用户的集合。</span><span class="sxs-lookup"><span data-stu-id="3bb9c-182">The following code example defines the **GetUserInformation** method, which returns a collection of [PSObject](http://msdn.microsoft.com/en-us/library/system.management.automation.pscredential%28VS.85%29.aspx) instances that represent Exchange mailbox users.</span></span> <span data-ttu-id="3bb9c-183">调用此方法由**GetUsersUsingBasicAuth**、 **GetUsersUsingCertificate**和**GetUsersUsingKerberos**方法可从远程服务器返回的用户的列表。</span><span class="sxs-lookup"><span data-stu-id="3bb9c-183">This method is called by the **GetUsersUsingBasicAuth**, **GetUsersUsingCertificate**, and **GetUsersUsingKerberos** methods to return the list of users from the remote server.</span></span> 
  
<span data-ttu-id="3bb9c-184">此方法需要以下参数：</span><span class="sxs-lookup"><span data-stu-id="3bb9c-184">This method requires the following parameters:</span></span>
  
- <span data-ttu-id="3bb9c-185">**计数**&ndash;的 Exchange 邮箱用户返回数量。</span><span class="sxs-lookup"><span data-stu-id="3bb9c-185">**count** &ndash; The number of Exchange mailbox users to return.</span></span> 
    
- <span data-ttu-id="3bb9c-186">**运行空间**&ndash;的远程 Exchange 服务器建立远程运行空间。</span><span class="sxs-lookup"><span data-stu-id="3bb9c-186">**runspace** &ndash; The remote runspace that is established for the remote Exchange server.</span></span> 
    
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

<span data-ttu-id="3bb9c-187">**GetUserInformation**方法将返回邮箱用户不能超过_计数_。</span><span class="sxs-lookup"><span data-stu-id="3bb9c-187">The **GetUserInformation** method will return no more than  _count_ mailbox users.</span></span> <span data-ttu-id="3bb9c-188">若要简化此示例的代码，该方法不筛选或否则限制返回的邮箱用户。</span><span class="sxs-lookup"><span data-stu-id="3bb9c-188">To simplify the code for this example, the method does not filter or otherwise limit the mailbox users that are returned.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3bb9c-189">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3bb9c-189">See also</span></span>

- [<span data-ttu-id="3bb9c-190">创建 Exchange 命令行管理程序工具</span><span class="sxs-lookup"><span data-stu-id="3bb9c-190">Create Exchange Management Shell tools</span></span>](create-exchange-management-shell-tools.md)   
- [<span data-ttu-id="3bb9c-191">使用 Exchange 命令行管理程序 cmdlet 响应</span><span class="sxs-lookup"><span data-stu-id="3bb9c-191">Use the Exchange Management Shell cmdlet response</span></span>](how-to-use-the-exchange-management-shell-cmdlet-response.md)
    

