---
title: 验证 EWS 托管 API 的服务器证书
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 1fe0b215-8340-4bc8-a6ce-4f591ca9e353
description: 了解如何创建和引用证书验证回调方法，以便可以对 Exchange 服务器进行 EWS 托管的 API 请求。
localization_priority: Priority
ms.openlocfilehash: 195c51ca71890d6092e4182d23990bb528d37095
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456778"
---
# <a name="validate-a-server-certificate-for-the-ews-managed-api"></a>验证 EWS 托管 API 的服务器证书

了解如何创建和引用证书验证回调方法，以便可以对 Exchange 服务器进行 EWS 托管的 API 请求。
  
默认情况下，从 Exchange 2007 SP1 开始的 Exchange 版本使用自签名的 X509 证书对来自 EWS 的呼叫进行身份验证。 使用 EWS 托管 API 时，需要创建证书验证回调方法;否则，EWS 托管 API 请求将失败。 如果使用自动发现服务，则对 EWS 托管 API 自动发现方法的调用将失败，并出现**AutodiscoverLocalException**错误。 如果使用的是 web 生成的 web 服务代理，您可能还需要创建验证回调方法，具体取决于代理的创建方式。 
  
## <a name="prerequisites-for-creating-a-validation-callback-method"></a>创建验证回调方法的先决条件
<a name="bk_prereq"> </a>

若要设置为验证服务器证书，请确保满足以下条件： 
  
- 您的 Exchange 服务器使用的是自签名证书的 EWS。 如果管理员已安装了跟踪到根证书的有效证书，则无需创建验证回调方法。 
    
- 您正在创建一个包含对以下必需的 .NET Framework 命名空间的引用的托管应用程序： 
    
  - **System.Net**
  - **系统 .Net。安全性**  
  - **X509Certificates 的安全加密**
    
## <a name="example-callback-method-to-validate-a-server-certificate-for-the-ews-managed-api"></a>示例：用于验证 EWS 托管 API 的服务器证书的回调方法
<a name="bk_example"> </a>

下面的代码示例演示如何为 EWS 托管 API 创建 X509 证书验证回调方法。 此方法将验证 X509 证书，并且仅当满足以下任一条件时才返回 true： 
  
- 证书有效并将追溯到有效的根证书。    
- 证书有效，并且由返回它的服务器自行签署。 
    
> [!IMPORTANT]
> 此示例中的证书验证回调方法为 EWS 托管 API 应用程序的开发和测试提供了足够的安全性。 但是，它可能不会为部署的应用程序提供足够的安全性。 应始终确保您使用的证书验证回调方法符合组织的安全要求。 
  
```cs
      private static bool CertificateValidationCallBack(
         object sender,
         System.Security.Cryptography.X509Certificates.X509Certificate certificate,
         System.Security.Cryptography.X509Certificates.X509Chain chain,
         System.Net.Security.SslPolicyErrors sslPolicyErrors)
    {
      // If the certificate is a valid, signed certificate, return true.
      if (sslPolicyErrors == System.Net.Security.SslPolicyErrors.None)
      {
        return true;
      }
      // If there are errors in the certificate chain, look at each error to determine the cause.
      if ((sslPolicyErrors &amp; System.Net.Security.SslPolicyErrors.RemoteCertificateChainErrors) != 0)
      {
        if (chain != null &amp;&amp; chain.ChainStatus != null)
        {
          foreach (System.Security.Cryptography.X509Certificates.X509ChainStatus status in chain.ChainStatus)
          {
            if ((certificate.Subject == certificate.Issuer) &amp;&amp;
               (status.Status == System.Security.Cryptography.X509Certificates.X509ChainStatusFlags.UntrustedRoot))
            {
              // Self-signed certificates with an untrusted root are valid. 
              continue;
            }
            else
            {
              if (status.Status != System.Security.Cryptography.X509Certificates.X509ChainStatusFlags.NoError)
              {
                // If there are any other errors in the certificate chain, the certificate is invalid,
             // so the method returns false.
                return false;
              }
            }
          }
        }
        // When processing reaches this line, the only errors in the certificate chain are 
    // untrusted root errors for self-signed certificates. These certificates are valid
    // for default Exchange server installations, so return true.
        return true;
      }
      else
      {
     // In all other cases, return false.
        return false;
      }
    }

```

您可以使用 .NET **System.Net**命名空间中的**ServicePointManager**类，通过设置**ServerCertificateValidationCallback**属性来挂钩验证回调方法。 您可以使用类似于下面的代码示例的代码来设置**ServerCertificateValidationCallback**属性。 
  
```cs
ServicePointManager.ServerCertificateValidationCallback = CertificateValidationCallBack;

```

## <a name="next-steps"></a>后续步骤
<a name="bk_example"> </a>

为 EWS 托管 API 创建验证回调方法后，可以使用自动发现服务从 Exchange 服务器获取连接点和用户和域设置。 有关详细信息，请参阅以下文章：
  
- [使用自动发现查找连接点](how-to-use-autodiscover-to-find-connection-points.md)
    
- [使用自动发现从 Exchange 获取用户设置](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    
- [获取来自 Exchange 服务器的域设置](how-to-get-domain-settings-from-an-exchange-server.md)
    
## <a name="see-also"></a>另请参阅

- [设置 EWS 应用程序](setting-up-your-ews-application.md)  
- [Start using web services in Exchange](start-using-web-services-in-exchange.md)
    

