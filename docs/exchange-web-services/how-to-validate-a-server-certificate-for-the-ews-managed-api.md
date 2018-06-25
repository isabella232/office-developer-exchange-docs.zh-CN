---
title: EWS 托管 api 验证服务器证书
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1fe0b215-8340-4bc8-a6ce-4f591ca9e353
description: 了解如何创建和引用证书验证回调方法，以便您可以向 Exchange 服务器发出 EWS 托管 API 请求。
ms.openlocfilehash: 13d7c51e55308b9e9997697a075c8a9e6b4f10d0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752893"
---
# <a name="validate-a-server-certificate-for-the-ews-managed-api"></a>EWS 托管 api 验证服务器证书

了解如何创建和引用证书验证回调方法，以便您可以向 Exchange 服务器发出 EWS 托管 API 请求。
  
开始 Exchange 2007 sp1 的 Exchange 版本默认情况下，使用自签名的 X509 证书进行身份验证从 EWS 的呼叫。 当您使用 EWS 托管 API 时，您需要创建的证书验证回调方法;否则，EWS 托管 API 请求将失败。 如果使用自动发现服务时，对 EWS 托管 API 自动发现方法的调用将失败， **AutodiscoverLocalException**错误。 如果您使用的 web 生成 web 服务代理，您可能需要创建的验证回调方法，具体取决于如何创建代理。 
  
## <a name="prerequisites-for-creating-a-validation-callback-method"></a>创建验证回调方法的先决条件
<a name="bk_prereq"> </a>

若要设置以验证服务器证书，请确保以下是，则返回 true: 
  
- 您的 Exchange 服务器对 EWS 使用自签名的证书。 如果管理员已安装到根证书的跟踪的有效证书，您不需要创建的验证回调方法。 
    
- 您正在创建的托管的应用程序包括以下所需的.NET Framework 命名空间的引用： 
    
  - **System.Net**
  - **System.Net.Security**  
  - **System.Security.Cryptography.X509Certificates**
    
## <a name="example-callback-method-to-validate-a-server-certificate-for-the-ews-managed-api"></a>示例： 回调方法，以验证服务器证书的 EWS 托管 API
<a name="bk_example"> </a>

下面的代码示例演示如何创建 X509 证书验证回调方法的 EWS 托管 API。 此方法将验证 X509 证书，然后仅返回 true，在满足以下条件之一时： 
  
- 证书有效并且跟踪返回到有效的根证书。    
- 证书有效，并且自签名的服务器所返回它。 
    
> [!IMPORTANT]
> 此示例中的证书验证回调方法提供足够的安全性开发和测试 EWS 托管 API 应用程序。 但是，它可能为部署应用程序提供足够的安全性。 始终应确保您使用的证书验证回调方法满足组织的安全要求。 
  
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

您可以使用.NET **System.Net**命名空间中的**ServicePointManager**类挂钩验证回调方法，通过设置**ServerCertificateValidationCallback**属性。 您可以使用类似于下面的代码示例的代码将**ServerCertificateValidationCallback**属性设置。 
  
```cs
ServicePointManager.ServerCertificateValidationCallback = CertificateValidationCallBack;

```

## <a name="next-steps"></a>后续步骤
<a name="bk_example"> </a>

EWS 托管 API 创建验证回调方法后，您可以使用自动发现服务若要从 Exchange 服务器获取连接点和用户和域设置。 有关详细信息，请参阅以下文章：
  
- [使用 Autodiscover 以查找连接点](how-to-use-autodiscover-to-find-connection-points.md)
    
- [通过使用自动发现 Exchange 中获取用户设置](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    
- [从 Exchange 服务器获取域设置](how-to-get-domain-settings-from-an-exchange-server.md)
    
## <a name="see-also"></a>另请参阅

- [EWS 应用程序设置](setting-up-your-ews-application.md)  
- [Start using web services in Exchange](start-using-web-services-in-exchange.md)
    

