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
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456778"
---
# <a name="validate-a-server-certificate-for-the-ews-managed-api"></a><span data-ttu-id="69c24-103">验证 EWS 托管 API 的服务器证书</span><span class="sxs-lookup"><span data-stu-id="69c24-103">Validate a server certificate for the EWS Managed API</span></span>

<span data-ttu-id="69c24-104">了解如何创建和引用证书验证回调方法，以便可以对 Exchange 服务器进行 EWS 托管的 API 请求。</span><span class="sxs-lookup"><span data-stu-id="69c24-104">Learn how to create and reference a certificate validation callback method so that you can make EWS Managed API requests to an Exchange server.</span></span>
  
<span data-ttu-id="69c24-105">默认情况下，从 Exchange 2007 SP1 开始的 Exchange 版本使用自签名的 X509 证书对来自 EWS 的呼叫进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="69c24-105">By default, versions of Exchange starting with Exchange 2007 SP1 use self-signed X509 certificates to authenticate calls from EWS.</span></span> <span data-ttu-id="69c24-106">使用 EWS 托管 API 时，需要创建证书验证回调方法;否则，EWS 托管 API 请求将失败。</span><span class="sxs-lookup"><span data-stu-id="69c24-106">When you are using the EWS Managed API, you need to create a certificate validation callback method; otherwise, EWS Managed API requests will fail.</span></span> <span data-ttu-id="69c24-107">如果使用自动发现服务，则对 EWS 托管 API 自动发现方法的调用将失败，并出现**AutodiscoverLocalException**错误。</span><span class="sxs-lookup"><span data-stu-id="69c24-107">If you are using the Autodiscover service, the call to the EWS Managed API Autodiscover method will fail with an **AutodiscoverLocalException** error.</span></span> <span data-ttu-id="69c24-108">如果使用的是 web 生成的 web 服务代理，您可能还需要创建验证回调方法，具体取决于代理的创建方式。</span><span class="sxs-lookup"><span data-stu-id="69c24-108">If you are using a web-generated web service proxy, you might also have to create a validation callback method, depending on how the proxy is created.</span></span> 
  
## <a name="prerequisites-for-creating-a-validation-callback-method"></a><span data-ttu-id="69c24-109">创建验证回调方法的先决条件</span><span class="sxs-lookup"><span data-stu-id="69c24-109">Prerequisites for creating a validation callback method</span></span>
<span data-ttu-id="69c24-110"><a name="bk_prereq"> </a></span><span class="sxs-lookup"><span data-stu-id="69c24-110"><a name="bk_prereq"> </a></span></span>

<span data-ttu-id="69c24-111">若要设置为验证服务器证书，请确保满足以下条件：</span><span class="sxs-lookup"><span data-stu-id="69c24-111">To set up to validate a server certificate, ensure that the following are true:</span></span> 
  
- <span data-ttu-id="69c24-112">您的 Exchange 服务器使用的是自签名证书的 EWS。</span><span class="sxs-lookup"><span data-stu-id="69c24-112">Your Exchange server is using a self-signed certificate for EWS.</span></span> <span data-ttu-id="69c24-113">如果管理员已安装了跟踪到根证书的有效证书，则无需创建验证回调方法。</span><span class="sxs-lookup"><span data-stu-id="69c24-113">If the administrator has installed a valid certificate that traces to a root certificate, you do not need to create a validation callback method.</span></span> 
    
- <span data-ttu-id="69c24-114">您正在创建一个包含对以下必需的 .NET Framework 命名空间的引用的托管应用程序：</span><span class="sxs-lookup"><span data-stu-id="69c24-114">You are creating a managed application that includes a reference to the following required .NET Framework namespaces:</span></span> 
    
  - <span data-ttu-id="69c24-115">**System.Net**</span><span class="sxs-lookup"><span data-stu-id="69c24-115">**System.Net**</span></span>
  - <span data-ttu-id="69c24-116">**系统 .Net。安全性**</span><span class="sxs-lookup"><span data-stu-id="69c24-116">**System.Net.Security**</span></span>  
  - <span data-ttu-id="69c24-117">**X509Certificates 的安全加密**</span><span class="sxs-lookup"><span data-stu-id="69c24-117">**System.Security.Cryptography.X509Certificates**</span></span>
    
## <a name="example-callback-method-to-validate-a-server-certificate-for-the-ews-managed-api"></a><span data-ttu-id="69c24-118">示例：用于验证 EWS 托管 API 的服务器证书的回调方法</span><span class="sxs-lookup"><span data-stu-id="69c24-118">Example: Callback method to validate a server certificate for the EWS Managed API</span></span>
<span data-ttu-id="69c24-119"><a name="bk_example"> </a></span><span class="sxs-lookup"><span data-stu-id="69c24-119"><a name="bk_example"> </a></span></span>

<span data-ttu-id="69c24-120">下面的代码示例演示如何为 EWS 托管 API 创建 X509 证书验证回调方法。</span><span class="sxs-lookup"><span data-stu-id="69c24-120">The following code example shows how to create an X509 certificate validation callback method for the EWS Managed API.</span></span> <span data-ttu-id="69c24-121">此方法将验证 X509 证书，并且仅当满足以下任一条件时才返回 true：</span><span class="sxs-lookup"><span data-stu-id="69c24-121">This method will validate an X509 certificate and only return true when either of the following criteria are met:</span></span> 
  
- <span data-ttu-id="69c24-122">证书有效并将追溯到有效的根证书。</span><span class="sxs-lookup"><span data-stu-id="69c24-122">The certificate is valid and traces back to a valid root certificate.</span></span>    
- <span data-ttu-id="69c24-123">证书有效，并且由返回它的服务器自行签署。</span><span class="sxs-lookup"><span data-stu-id="69c24-123">The certificate is valid and is self-signed by the server that returned it.</span></span> 
    
> [!IMPORTANT]
> <span data-ttu-id="69c24-124">此示例中的证书验证回调方法为 EWS 托管 API 应用程序的开发和测试提供了足够的安全性。</span><span class="sxs-lookup"><span data-stu-id="69c24-124">The certificate validation callback method in this example provides sufficient security for development and testing of EWS Managed API applications.</span></span> <span data-ttu-id="69c24-125">但是，它可能不会为部署的应用程序提供足够的安全性。</span><span class="sxs-lookup"><span data-stu-id="69c24-125">However, it might not provide sufficient security for your deployed application.</span></span> <span data-ttu-id="69c24-126">应始终确保您使用的证书验证回调方法符合组织的安全要求。</span><span class="sxs-lookup"><span data-stu-id="69c24-126">You should always make sure that the certificate validation callback method that you use meets the security requirements of your organization.</span></span> 
  
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

<span data-ttu-id="69c24-127">您可以使用 .NET **System.Net**命名空间中的**ServicePointManager**类，通过设置**ServerCertificateValidationCallback**属性来挂钩验证回调方法。</span><span class="sxs-lookup"><span data-stu-id="69c24-127">You use the **ServicePointManager** class in the .NET **System.Net** namespace to hook up a validation callback method by setting the **ServerCertificateValidationCallback** property.</span></span> <span data-ttu-id="69c24-128">您可以使用类似于下面的代码示例的代码来设置**ServerCertificateValidationCallback**属性。</span><span class="sxs-lookup"><span data-stu-id="69c24-128">You can use code similar to the following code example to set the **ServerCertificateValidationCallback** property.</span></span> 
  
```cs
ServicePointManager.ServerCertificateValidationCallback = CertificateValidationCallBack;

```

## <a name="next-steps"></a><span data-ttu-id="69c24-129">后续步骤</span><span class="sxs-lookup"><span data-stu-id="69c24-129">Next steps</span></span>
<span data-ttu-id="69c24-130"><a name="bk_example"> </a></span><span class="sxs-lookup"><span data-stu-id="69c24-130"><a name="bk_example"> </a></span></span>

<span data-ttu-id="69c24-131">为 EWS 托管 API 创建验证回调方法后，可以使用自动发现服务从 Exchange 服务器获取连接点和用户和域设置。</span><span class="sxs-lookup"><span data-stu-id="69c24-131">After you have created the validation callback method for the EWS Managed API, you can use the Autodiscover service to get connection points and user and domain settings from an Exchange server.</span></span> <span data-ttu-id="69c24-132">有关详细信息，请参阅以下文章：</span><span class="sxs-lookup"><span data-stu-id="69c24-132">For more information, see the following articles:</span></span>
  
- [<span data-ttu-id="69c24-133">使用自动发现查找连接点</span><span class="sxs-lookup"><span data-stu-id="69c24-133">Use Autodiscover to find connection points</span></span>](how-to-use-autodiscover-to-find-connection-points.md)
    
- [<span data-ttu-id="69c24-134">使用自动发现从 Exchange 获取用户设置</span><span class="sxs-lookup"><span data-stu-id="69c24-134">Get user settings from Exchange by using Autodiscover</span></span>](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    
- [<span data-ttu-id="69c24-135">获取来自 Exchange 服务器的域设置</span><span class="sxs-lookup"><span data-stu-id="69c24-135">Get domain settings from an Exchange server</span></span>](how-to-get-domain-settings-from-an-exchange-server.md)
    
## <a name="see-also"></a><span data-ttu-id="69c24-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="69c24-136">See also</span></span>

- [<span data-ttu-id="69c24-137">设置 EWS 应用程序</span><span class="sxs-lookup"><span data-stu-id="69c24-137">Setting up your EWS application</span></span>](setting-up-your-ews-application.md)  
- [<span data-ttu-id="69c24-138">Start using web services in Exchange</span><span class="sxs-lookup"><span data-stu-id="69c24-138">Start using web services in Exchange</span></span>](start-using-web-services-in-exchange.md)
    

