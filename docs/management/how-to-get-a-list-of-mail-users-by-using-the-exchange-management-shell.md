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
# <a name="get-a-list-of-mail-users-by-using-the-exchange-management-shell"></a>使用 Exchange 命令行管理程序获取邮件用户列表

了解如何使用 Exchange 命令行管理程序 cmdlet 来创建可返回 Exchange 邮箱用户列表的工具。
  
**适用于：** Exchange Online |Exchange Server 2013 |Office 365 
  
通过使用调用 Exchange 命令行管理程序 cmdlet 的托管工具，从 Exchange Online、Exchange Online （Office 365 的一部分）或从 Exchange 2013 开始的 Exchange 版本获取用户列表是一个包含两个步骤的过程。 首先，在 Exchange 服务器上建立远程运行空间;然后，运行 cmdlet 以检索远程运行空间中的用户信息。 

若要连接到远程运行空间，必须使用符合组织的安全要求的身份验证方案对 Exchange 服务器进行身份验证。 

本文提供了可用于设置远程运行空间并运行 Exchange 命令行管理程序 cmdlet 以从 Exchange 服务器获取用户列表的代码示例。

<a name="bk_prerequisites"> </a>

## <a name="prerequisites-for-getting-a-list-of-mailbox-users"></a>获取邮箱用户列表的先决条件

若要执行此任务，您需要一个对以下命名空间的引用：
  
- **ObjectModel**
- **系统管理。自动化**
- **系统管理. Remoting**
- **系统管理. 自动化**
    
> [!NOTE]
>  使用 Visual Studio 创建应用程序时，必须在项目中添加对 system.string 程序集的引用。 可以在以下位置之一找到程序集：
> - 对于 Windows XP 和 Windows Vista 操作系统，Windows PowerShell 安装目录（$PSHOME）。
> - 对于 Windows 7 和 Windows 8 操作系统，以下文件夹： Windows\assembly\ GAC_MSIL \System.Management.Automation。 
  
请勿将 Exchange 2013 管理管理单元加载到运行自动执行 Exchange 命令行管理程序 cmdlet 的应用程序的计算机上的运行空间中。 应用程序应改为创建一个远程运行空间，如本文后面所述。

<a name="bk_gettinglistmailbox"> </a>

## <a name="connect-to-a-remote-runspace-on-an-exchange-server"></a>连接到 Exchange 服务器上的远程运行空间

您用来连接到远程运行空间以使用 Exchange 命令行管理程序 cmdlet 的方法因所使用的身份验证方案而异。 本节提供的代码示例演示如何在使用下表中列出的身份验证方法时连接到远程运行空间。
  
|**身份验证方法**|**适用于**|**URI**|
|:-----|:-----|:-----|
|[使用基本身份验证连接到 Exchange Online 上的远程运行空间](#bk_basic) <br/> |Exchange Online 服务器  <br/> |`https://outlook.office365.com/PowerShell-LiveID`<br/><br/>`https://<server>/PowerShell-LiveID`  <br/> |
|[使用证书身份验证连接到远程运行空间](#bk_cert) <br/> |Exchange Online 和 Exchange 本地服务器  <br/> |`https://outlook.office365.com/PowerShell`<br/><br/>`https://<server>/PowerShell`<br/><br/>`http://<server>/PowerShell`  <br/> |
|[使用 Kerberos 身份验证连接到 Exchange 服务器上的远程运行空间](#bk_Kerberos) <br/> |Exchange Online 和 Exchange 本地服务器  <br/> |`https://<server>/PowerShell`<br/><br/>`http://<server>/PowerShell`  <br/> |

<a name="bk_basic"> </a>

### <a name="connect-to-a-remote-runspace-on-exchange-online-by-using-basic-authentication"></a>使用基本身份验证连接到 Exchange Online 上的远程运行空间

下面的代码示例定义了**GetUsersUsingBasicAuth**方法，该方法通过使用基本身份验证在远程 Exchange Online 服务器上创建 Exchange 命令行管理程序运行空间。 然后，此方法调用**GetUserInformation**方法，如部分中所定义的，[从远程运行空间获取邮箱用户的列表](#bk_remote)，以返回远程服务器上的用户列表。
  
此方法需要以下参数：
  
-  **liveIDConnectionUri** &ndash;一个字符串，包含将对应用程序进行身份验证的 Exchange Online 服务器的 URI。 如果 Exchange Online 在 Office 365 中运行，则 URI 为 `https://outlook.office365.com/PowerShell-LiveID` ; 否则为 uri `https://<servername>/PowerShell-LiveID` 。 
    
-  **schemaUri** &ndash;一个字符串，其中包含定义 Exchange 命令行管理程序架构的架构文档的 URI。 架构 URI 为 `https://schemas.microsoft.com/powershell/Microsoft.Exchange` 。 
    
-  **凭据** &ndash;一个[PSCredential](https://msdn.microsoft.com/library/system.management.automation.pscredential%28VS.85%29.aspx)对象，其中包含运行该应用程序的用户的凭据。 
    
-  **计数** &ndash;要返回的 Exchange 邮箱用户数。 
    
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

<a name="bk_cert"> </a>

### <a name="connect-to-a-remote-runspace-by-using-certificate-authentication"></a>使用证书身份验证连接到远程运行空间

下面的代码示例定义了**GetUsersUsingCertificate**方法，该方法通过使用证书在远程服务器上创建 Exchange 命令行管理程序运行空间。 然后，此方法调用**GetUserInformation**方法，如部分中所定义的，[从远程运行空间获取邮箱用户的列表](#bk_remote)，以返回远程服务器上的用户列表。
  
此方法需要以下参数：
  
-  **指纹** &ndash;一个字符串，其中包含用于对应用程序进行身份验证的证书的指纹。 
    
-  **certConnectionUri** &ndash;一个字符串，包含将对证书进行身份验证的服务器的 URI。 URI 将是下表中列出的 URI 之一。 
    
    **表1。certConnectionUri Uri**

    |**Server**|**URI**|
    |:-----|:-----|
    |不使用 SSL 的 Exchange server  <br/> |`http://<servername>/PowerShell`  <br/> |
    |使用 SSL 的 Exchange 服务器  <br/> |`https://<servername>/PowerShell`  <br/> |
    |作为 Office 365 的一部分的 Exchange Online  <br/> |`https://outlook.office365.com/PowerShell`  <br/> |
   
- **schemaUri** &ndash;一个字符串，其中包含定义 Exchange 命令行管理程序架构的架构文档的 URI。 架构 URI 为 https://schemas.microsoft.com/powershell/Microsoft.Exchange 。 
    
- **计数** &ndash;要返回的 Exchange 邮箱用户数。 
    
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

<a name="bk_Kerberos"> </a>

### <a name="connect-to-a-remote-runspace-on-an-exchange-server-by-using-kerberos-authentication"></a>使用 Kerberos 身份验证连接到 Exchange 服务器上的远程运行空间

下面的代码示例定义了**GetUsersUsingKerberos**方法，该方法通过使用 Kerberos 身份验证在远程服务器上创建 Exchange 命令行管理程序运行空间。 然后，此方法调用**GetUserInformation**方法，如部分中所定义的，[从远程运行空间获取邮箱用户的列表](#bk_remote)，以返回远程服务器上的用户列表。
  
此方法需要以下参数：
  
- **kerberosUri** &ndash;一个字符串，包含将对应用程序进行身份验证的 Kerberos 服务器的 URI。 URI 将是下表中列出的 URI 之一。 
    
    **表2。kerberosUri Uri**

    |**Server**|**URI**|
    |:-----|:-----|
    |不使用 SSL 的 Exchange server  <br/> |`http://<servername>/PowerShell`  <br/> |
    |使用 SSL 的 Exchange 服务器  <br/> |`https://<servername>/PowerShell`  <br/> |
   
- **schemaUri** &ndash;一个字符串，其中包含定义 Exchange 命令行管理程序架构的架构文档的 URI。 架构 URI 为 https://schemas.microsoft.com/powershell/Microsoft.Exchange 。 
    
- **凭据** &ndash;一个[PSCredential](https://msdn.microsoft.com/library/system.management.automation.pscredential%28VS.85%29.aspx)对象，其中包含运行该应用程序的用户的凭据。 
    
- **计数** &ndash;要返回的 Exchange 邮箱用户数。 
    
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

<a name="bk_remote"> </a>

## <a name="get-a-list-of-mailbox-users-from-a-remote-runspace"></a>从远程运行空间获取邮箱用户的列表

下面的代码示例定义了**GetUserInformation**方法，该方法返回代表 Exchange 邮箱用户的[PSObject](https://msdn.microsoft.com/library/system.management.automation.pscredential%28VS.85%29.aspx)实例的集合。 此方法由**GetUsersUsingBasicAuth**、 **GetUsersUsingCertificate**和**GetUsersUsingKerberos**方法调用，以返回远程服务器上的用户列表。 
  
此方法需要以下参数：
  
- **计数** &ndash;要返回的 Exchange 邮箱用户数。 
    
- **运行空间** &ndash;为远程 Exchange 服务器建立的远程运行空间。 
    
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

**GetUserInformation**方法将返回的邮箱用户数不会超过_count_ 。 若要简化此示例的代码，该方法不会筛选或限制返回的邮箱用户。 
  
## <a name="see-also"></a>另请参阅

- [创建 Exchange 命令行管理程序工具](create-exchange-management-shell-tools.md)   
- [使用 Exchange 命令行管理程序 cmdlet 响应](how-to-use-the-exchange-management-shell-cmdlet-response.md)
    

