---
title: 将公用文件夹内容请求路由
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 59d2f05e-90fb-471e-ac06-70becc15b295
description: 有关公用文件夹信息涉及公用文件夹需要路由到公用文件夹邮箱的内容的所有请求的都包含目标文件夹的内容。 若要将请求路由到该邮箱，您需要设置为特定值的 X AnchorMailbox 和 X PublicFolderMailbox 标头。
ms.openlocfilehash: ad36c1526a24d815ec690879d633774d429ed36c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752891"
---
# <a name="route-public-folder-content-requests"></a><span data-ttu-id="30e66-104">将公用文件夹内容请求路由</span><span class="sxs-lookup"><span data-stu-id="30e66-104">Route public folder content requests</span></span>

<span data-ttu-id="30e66-105">有关公用文件夹信息涉及公用文件夹需要路由到公用文件夹邮箱的内容的所有请求的都包含目标文件夹的内容。</span><span class="sxs-lookup"><span data-stu-id="30e66-105">All requests for public folder information that involve the content of the public folder need to be routed to the public folder mailbox that holds the content for the target folder.</span></span> <span data-ttu-id="30e66-106">若要将请求路由到该邮箱，您需要设置为特定值的**X AnchorMailbox**和**X PublicFolderMailbox**标头。</span><span class="sxs-lookup"><span data-stu-id="30e66-106">To route the requests to that mailbox, you need to set the **X-AnchorMailbox** and **X-PublicFolderMailbox** headers to specific values.</span></span> 
  
<span data-ttu-id="30e66-107">下表提供了过程的概述：</span><span class="sxs-lookup"><span data-stu-id="30e66-107">The following table provides an overview of the process:</span></span>
  
<span data-ttu-id="30e66-108">**公用文件夹概述 （英文)**</span><span class="sxs-lookup"><span data-stu-id="30e66-108">**Public folder overview**</span></span>

|<span data-ttu-id="30e66-109">标头</span><span class="sxs-lookup"><span data-stu-id="30e66-109">Header</span></span>|<span data-ttu-id="30e66-110">我需要什么？</span><span class="sxs-lookup"><span data-stu-id="30e66-110">What do I need?</span></span>|<span data-ttu-id="30e66-111">如何获得它？</span><span class="sxs-lookup"><span data-stu-id="30e66-111">How do I get it?</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="30e66-112">**X AnchorMailbox**</span><span class="sxs-lookup"><span data-stu-id="30e66-112">**X-AnchorMailbox**</span></span> <br/> |<span data-ttu-id="30e66-113">1。 [X AnchorMailbox 和 X PublicFolderInformation 值](how-to-route-public-folder-hierarchy-requests.md)公用文件夹层次结构邮箱。</span><span class="sxs-lookup"><span data-stu-id="30e66-113">1. [The X-AnchorMailbox and X-PublicFolderInformation values ](how-to-route-public-folder-hierarchy-requests.md) for the public folder hierarchy mailbox.</span></span><br/><br/><span data-ttu-id="30e66-114">2.公用文件夹邮箱包含邮箱内容，将它发送到自动发现服务的 GUID。</span><span class="sxs-lookup"><span data-stu-id="30e66-114">2. The GUID of the public folder mailbox that contains the mailbox content, which is sent to the Autodiscover service.</span></span><br/><br/>  <span data-ttu-id="30e66-115">**AutoDiscoverSMTPAddress** Autodisover 响应中将成为**X AnchorMailbox**头的值。</span><span class="sxs-lookup"><span data-stu-id="30e66-115">The **AutoDiscoverSMTPAddress** in the Autodisover response becomes the value of the **X-AnchorMailbox** header.</span></span>  <br/> <span data-ttu-id="30e66-116">![TODO](media/Ex15_PF_PFContent.png)</span><span class="sxs-lookup"><span data-stu-id="30e66-116">![TODO](media/Ex15_PF_PFContent.png)</span></span>| <span data-ttu-id="30e66-117">1.使用本文中，用于[实现 EWS 托管 API](#bk_determineguidewsma)中的代码示例。</span><span class="sxs-lookup"><span data-stu-id="30e66-117">1. Use the code example in this article, which [implements the EWS Managed API](#bk_determineguidewsma).</span></span> <span data-ttu-id="30e66-118">或[使用 EWS](#bk_determineguidews)和转换结果若要获取 GUID。</span><span class="sxs-lookup"><span data-stu-id="30e66-118">Or [use EWS](#bk_determineguidews) and convert your results to obtain a GUID.</span></span><br/><br/><span data-ttu-id="30e66-119">2。 使用 GUID 以及的域名中[进行的自动发现请求](#bk_makeautodrequest)。</span><span class="sxs-lookup"><span data-stu-id="30e66-119">2. [Make an Autodiscover request](#bk_makeautodrequest) by using the GUID plus the domain name.</span></span><br/><br/><span data-ttu-id="30e66-120">3.使用**AutoDiscoverSMTPAddress**元素对[填充标头的值](#bk_setheadervalues)的自动发现响应中返回的值。</span><span class="sxs-lookup"><span data-stu-id="30e66-120">3. Use the value of the **AutoDiscoverSMTPAddress** element returned in the Autodiscover response to [populate the value of the headers](#bk_setheadervalues).</span></span>  <br/> |
|<span data-ttu-id="30e66-121">**X PublicFolderMailbox**</span><span class="sxs-lookup"><span data-stu-id="30e66-121">**X-PublicFolderMailbox**</span></span> <br/> |<span data-ttu-id="30e66-122">完成您的工作，则 X PublicFolderMailbox 值为 X AnchorMailbox 值相同 ！</span><span class="sxs-lookup"><span data-stu-id="30e66-122">Your work is done, the X-PublicFolderMailbox value is the same as the X-AnchorMailbox value!</span></span>  <br/> |<span data-ttu-id="30e66-123">您已成功了 ！</span><span class="sxs-lookup"><span data-stu-id="30e66-123">You already have it!</span></span>  <br/> |
   
<span data-ttu-id="30e66-124">您已确定的标头值后，请[进行公用文件夹内容请求时](#bk_setheadervalues)进行包括。</span><span class="sxs-lookup"><span data-stu-id="30e66-124">After you have determined the header values, include them [when you make public folder content requests](#bk_setheadervalues).</span></span>
  
<span data-ttu-id="30e66-125">本文中的步骤是特定于公用文件夹内容请求。</span><span class="sxs-lookup"><span data-stu-id="30e66-125">The steps in this article are specific to public folder content requests.</span></span> <span data-ttu-id="30e66-126">若要确定您的请求是公用文件夹层次结构或内容的请求，请参阅[路由的公用文件夹请求](public-folder-access-with-ews-in-exchange.md#bk_routing)。</span><span class="sxs-lookup"><span data-stu-id="30e66-126">To determine whether your request is a public folder hierarchy or content request, see [Routing public folder requests](public-folder-access-with-ews-in-exchange.md#bk_routing).</span></span>
  
## <a name="determine-the-guid-of-the-public-folder-mailbox-by-using-the-ews-managed-api"></a><span data-ttu-id="30e66-127">通过使用 EWS 托管 API 来确定公用文件夹邮箱的 GUID</span><span class="sxs-lookup"><span data-stu-id="30e66-127">Determine the GUID of the public folder mailbox by using the EWS Managed API</span></span>
<span data-ttu-id="30e66-128"><a name="bk_determineguidewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="30e66-128"></span></span>

<span data-ttu-id="30e66-129">若要确定公用文件夹内容邮箱的 GUID，使用下面的代码示例，执行以下任务：</span><span class="sxs-lookup"><span data-stu-id="30e66-129">To determine the GUID of the public folder content mailbox, use the following code example, which does the following:</span></span> 
  
- <span data-ttu-id="30e66-130">使用通过[路由的公用文件夹层次结构请求](how-to-route-public-folder-hierarchy-requests.md)检索**X AnchorMailbox**和**X PublicFolderInformation**标头。</span><span class="sxs-lookup"><span data-stu-id="30e66-130">Uses the **X-AnchorMailbox** and **X-PublicFolderInformation** headers you retrieved by [routing public folder hierarchy requests](how-to-route-public-folder-hierarchy-requests.md).</span></span>
    
- <span data-ttu-id="30e66-131">调用 EWS 托管 API [FindFolders](http://msdn.microsoft.com/zh-cn/library/office/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)方法，并包括**PR_REPLICA_LIST** (0x66980102) 属性的请求</span><span class="sxs-lookup"><span data-stu-id="30e66-131">Calls the EWS Managed API [FindFolders](http://msdn.microsoft.com/zh-cn/library/office/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) method, and includes a request for the **PR_REPLICA_LIST** (0x66980102) property</span></span> 
    
<span data-ttu-id="30e66-132">**PR_REPLICA_LIST**值标识邮箱的邮箱的公用文件夹邮箱的已文件夹的内容的 GUID。</span><span class="sxs-lookup"><span data-stu-id="30e66-132">The **PR_REPLICA_LIST** value identifies the mailbox GUID of the public folder mailbox that has the content for the folder.</span></span> <span data-ttu-id="30e66-133">**PR_REPLICA_LIST**属性是一个字节数组，但这种情况下强制转换为 GUID。</span><span class="sxs-lookup"><span data-stu-id="30e66-133">The **PR_REPLICA_LIST** property is a byte array, but is cast as a GUID for this scenario.</span></span> <span data-ttu-id="30e66-134">GUID 和域名串联以形成要呼叫自动发现在其上的地址。</span><span class="sxs-lookup"><span data-stu-id="30e66-134">The GUID and the domain name are concatenated to form the address on which to call Autodiscover.</span></span> 
  
<span data-ttu-id="30e66-135">此示例假定`service`是[ExchangeService](http://msdn.microsoft.com/zh-cn/library/office/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象的邮箱用户，`PFHAnchorHeader`和`PFHMailboxHeader`是**X AnchorMailbox**和**X PublicFolderMailbox**页眉的值和域是由的域名租户。</span><span class="sxs-lookup"><span data-stu-id="30e66-135">This example assumes that  `service` is the [ExchangeService](http://msdn.microsoft.com/zh-cn/library/office/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the mailbox user,  `PFHAnchorHeader` and  `PFHMailboxHeader` are the values of the **X-AnchorMailbox** and **X-PublicFolderMailbox** headers, and domain is the domain name used by the tenant.</span></span> 
  
```cs
public static string GetMailboxGuidAddress(ExchangeService service, String PFHAnchorHeader, String PFHMailboxHeader, String domain)
{
    // Create a new folder view, and pass in the maximum number of folders to return.
    FolderView view = new FolderView(10);
    // Create an extended property definition for the PR_REPLICA_LIST property.
    ExtendedPropertyDefinition PR_REPLICA_LIST = new ExtendedPropertyDefinition(0x6698, MapiPropertyType.Binary);
    // As a best practice, limit the properties returned to only those required.
    // In this case, return the folder ID, the folder display name, and 
    // the value of the PR_REPLICA_LIST extended property definition.
    view.PropertySet = new PropertySet(BasePropertySet.IdOnly, FolderSchema.DisplayName, PR_REPLICA_LIST);
    service.HttpHeaders.Add("X-AnchorMailbox", PFHAnchorHeader);
    service.HttpHeaders.Add("X-PublicFolderMailbox", PFHMailboxHeader);
    // Add a call to the CertificateValidationCallback method here if needed.
    // ServicePointManager.ServerCertificateValidationCallback = CertificateValidationCallBack;
    // Call FindFolders to retrieve the folder hierarchy, starting with the PublicFolderRoot folder.
    // This method call results in a FindFolder call to EWS.
    FindFoldersResults findResults = service.FindFolders(WellKnownFolderName.PublicFoldersRoot, view);
    string GuidAsString = null;
    List<string> Guids = new List<string>();
    // For each folder under the root, display the name, and copy the value of the 
    // PR_REPLICA_LIST byte array to a string value. 
    foreach (Folder folder in findResults.Folders)
    {
        Console.WriteLine("Public folder display name: {0}", folder.DisplayName);
        byte[] ByteArr = (byte[])folder.ExtendedProperties[0].Value;
        GuidAsString = System.Text.Encoding.ASCII.GetString(ByteArr, 0, 36);
        Guids.Add(GuidAsString);
        Console.WriteLine("Address for Autodiscover: {0}.{1}\r\n", GuidAsString, domain);
    }
    // Concatenate the GUID value of the PR_REPLICA_LIST with the domain name to generate the 
    // SMTP address to use for the AutoDiscover request for the public folder content mailbox.
    string AutoDSMTPAddress = GuidAsString + "@" + domain;
    // Check that all folders have the same GUID value. If they do not, use the GUID value of the
    // folder that you're requesting content for.
    string commonGuid = CompareGuidsForEquality(Guids);
    if (commonGuid == "Not Equal")
    {
        Console.WriteLine("The GUIDs for all the folders in the hierarchy are not the same. Run the Autodiscover sample using the address returned above that is associated with the folder in your hierarchy request.", AutoDSMTPAddress);
        return null;
    }
    else
    {
        Console.WriteLine("The GUIDs for all public folders in the hierarchy are the same. Run the Autodiscover sample using the {0} address.", AutoDSMTPAddress);
        return AutoDSMTPAddress;
    }
}
// Method to compare the GUID for each folder under the public folder root.
// If each GUID is the same, return the GUID.
// If the GUIDs are not the same, return "Not equal".
public static string CompareGuidsForEquality(List<string> list)
{
    string NotEqual = "Not equal";
    string first = list.First();
    return list.All(x => x == first) ? first : NotEqual;
}
```

<span data-ttu-id="30e66-136">如果您收到错误"失败的请求。</span><span class="sxs-lookup"><span data-stu-id="30e66-136">If you received the error "The request failed.</span></span> <span data-ttu-id="30e66-137">基本连接已关闭： 无法建立信任关系为 SSL/TLS 安全通道"，您需要[添加对验证回调方法的调用](how-to-validate-a-server-certificate-for-the-ews-managed-api.md)。</span><span class="sxs-lookup"><span data-stu-id="30e66-137">The underlying connection was closed: Could not establish trust relationship for the SSL/TLS secure channel", you'll need to [add a call to a validation callback method](how-to-validate-a-server-certificate-for-the-ews-managed-api.md).</span></span> <span data-ttu-id="30e66-138">代码示例中包含的占位符和注释的方法。</span><span class="sxs-lookup"><span data-stu-id="30e66-138">A placeholder and comment for that method is included in the code example.</span></span>
  
<span data-ttu-id="30e66-139">如果相同的公用文件夹的根目录下的所有公用文件夹邮箱的邮箱 GUID，该示例指示使用时[调用自动发现](#bk_makeautodrequest)控制台输出和返回值的地址。</span><span class="sxs-lookup"><span data-stu-id="30e66-139">If the mailbox GUID is the same for all the public folders under the public folder root, the example indicates the address to use when [calling Autodiscover](#bk_makeautodrequest) in the console output and as the return value.</span></span> <span data-ttu-id="30e66-140">如果邮箱的邮箱 GUID 不相同的公用文件夹的根目录下的所有公用文件夹，您需要[进行的自动发现请求](#bk_makeautodrequest)上与您内容的请求中的文件夹关联的地址。</span><span class="sxs-lookup"><span data-stu-id="30e66-140">If the mailbox GUID is not the same for all public folders under the public folder root, you need to [Make an Autodiscover request](#bk_makeautodrequest) on the address associated with the folder in your content request.</span></span> 
  
## <a name="determine-the-guid-of-the-public-folder-mailbox-by-using-ews"></a><span data-ttu-id="30e66-141">使用 EWS 确定公用文件夹邮箱的 GUID</span><span class="sxs-lookup"><span data-stu-id="30e66-141">Determine the GUID of the public folder mailbox by using EWS</span></span>
<span data-ttu-id="30e66-142"><a name="bk_determineguidews"> </a></span><span class="sxs-lookup"><span data-stu-id="30e66-142"></span></span>

<span data-ttu-id="30e66-143">下面的代码示例演示如何通过使用 EWS [FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)操作检索**PR_REPLICA_LIST** (0x66980102) 属性的值。</span><span class="sxs-lookup"><span data-stu-id="30e66-143">The following code example shows how retrieve the value of the **PR_REPLICA_LIST** (0x66980102) property by using the EWS [FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="30e66-144">对于[ExtendedFieldURI](http://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx)元素中， **PropertyTag**属性设置为**PR_REPLICA_LIST**属性的十进制值 (26264) 和**PropertyType**属性设置为**二进制**。</span><span class="sxs-lookup"><span data-stu-id="30e66-144">For the [ExtendedFieldURI](http://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx) element, the **PropertyTag** attribute is set to the decimal value (26264) of the **PR_REPLICA_LIST** property, and the **PropertyType** attribute is set to **Binary**.</span></span>
  
<span data-ttu-id="30e66-145">这也是 XML 请求 EWS 托管 API 发送时您使用**FindFolders**方法[确定使用 EWS 托管 API 的公用文件夹邮箱的 GUID](#bk_determineguidewsma)。</span><span class="sxs-lookup"><span data-stu-id="30e66-145">This is also the XML request that the EWS Managed API sends when you use the **FindFolders** method to [determine the GUID of the public folder mailbox by using the EWS Managed API](#bk_determineguidewsma).</span></span>
  
```XML
POST https://outlook.office365.com/EWS/Exchange.asmx HTTP/1.1
Content-Type: text/xml; charset=utf-8
Accept: text/xml
User-Agent: ExchangeServicesClient/15.00.0913.015
Accept-Encoding: gzip,deflate
Authorization: Basic c29ueWFmQGNvbnRvc28xMDAwLm9ubWljcm9zb2Z0LmNvbTpFWENIIzIwMTQ=
Host: outlook.office365.com
Cookie: ClientId=KZPBLKA9ZMPXAQDW
Content-Length: 1005
Expect: 100-continue
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013_SP1" />
  </soap:Header>
  <soap:Body>
    <m:FindFolder Traversal="Shallow">
      <m:FolderShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="folder:DisplayName" />
          <t:ExtendedFieldURI PropertyTag="26264" PropertyType="Binary" />
        </t:AdditionalProperties>
      </m:FolderShape>
      <m:IndexedPageFolderView MaxEntriesReturned="10" Offset="0" BasePoint="Beginning" />
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="publicfoldersroot" />
      </m:ParentFolderIds>
    </m:FindFolder>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="30e66-146">服务器响应**FindFolder**请求[FindFolderResponse](http://msdn.microsoft.com/library/f5dd813c-9698-4a39-8fca-3a825df365ed%28Office.15%29.aspx)邮件包含**PR_REPLICA_LIST**扩展属性的值。</span><span class="sxs-lookup"><span data-stu-id="30e66-146">The server responds to the **FindFolder** request with a [FindFolderResponse](http://msdn.microsoft.com/library/f5dd813c-9698-4a39-8fca-3a825df365ed%28Office.15%29.aspx) message that includes the value of the **PR_REPLICA_LIST** extended property.</span></span> <span data-ttu-id="30e66-147">请注意，属性的值显示在 EWS 响应作为字符串格式的 base64 编码的字节数组。</span><span class="sxs-lookup"><span data-stu-id="30e66-147">Note that the value of the property appears on the EWS response as the string format of a base-64 encoded byte array.</span></span> <span data-ttu-id="30e66-148">为便于阅读缩短的响应中某些标头值。</span><span class="sxs-lookup"><span data-stu-id="30e66-148">Some header values in the response are shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?><s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="1019" MinorBuildNumber="15" Version="V2_17" xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" xmlns="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body>
    <m:FindFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="2" TotalItemsInView="2" IncludesLastItemInRange="true">
            <t:Folders>
              <t:ContactsFolder>
                <t:FolderId Id="AAEuAAAAAADL8shaNEKnQYVvRbpoY9vDAQBGDloItRzyTrAt+XVzRr/YAABdofPkAAA=" ChangeKey="AwAAABYAAABGDloItRzyTrAt+XVzRr/YAABdo/2h"/>
                <t:DisplayName>My Public Contacts</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x6698" PropertyType="Binary"/>
                  <t:Value>MWVjMmEyMzYtZWQ5My00Zjg4LWI5YzYtMzNlNjNmYTRhYTQ0AA==</t:Value>
                </t:ExtendedProperty>
              </t:ContactsFolder>
              <t:Folder>
                <t:FolderId Id="AQEuAAADy/LIWjRCp0GFb0W6aGPbwwEARg5aCLUc8k6wLfl1c0a/2AAAAxEAAAA=" ChangeKey="AQAAABYAAABGDloItRzyTrAt+XVzRr/YAABdo/W/"/>
                <t:DisplayName>SampleFolder</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x6698" PropertyType="Binary"/>
                  <t:Value>MWVjMmEyMzYtZWQ5My00Zjg4LWI5YzYtMzNlNjNmYTRhYTQ0AA==</t:Value>
                </t:ExtendedProperty>
              </t:Folder>
            </t:Folders>
          </m:RootFolder>
        </m:FindFolderResponseMessage>
      </m:ResponseMessages>
    </m:FindFolderResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="30e66-149">若要使用的**PR_REPLICA_LIST**值返回的 XML，MWVjMmEyMzYtZWQ5My00Zjg4LWI5YzYtMzNlNjNmYTRhYTQ0AA = =，若要确定邮箱的邮箱 GUID，必须将值转换为格式类似于如何将值转换中的 GUID[EWS 托管 API 的代码示例](#bk_determineguidewsma)。</span><span class="sxs-lookup"><span data-stu-id="30e66-149">In order to use the value of the **PR_REPLICA_LIST** returned in the XML, MWVjMmEyMzYtZWQ5My00Zjg4LWI5YzYtMzNlNjNmYTRhYTQ0AA==, to determine the mailbox GUID, the value must be converted into a GUID in a format similar to how the value is converted in the [EWS Managed API code example](#bk_determineguidewsma).</span></span> <span data-ttu-id="30e66-150">创建 SMTP 地址，[自动发现请求](#bk_makeautodrequest)中包含的域名与然后串联 GUID。</span><span class="sxs-lookup"><span data-stu-id="30e66-150">The GUID is then concatenated with the domain name to create an SMTP address, which is included in the [Autodiscover request](#bk_makeautodrequest).</span></span>
  
## <a name="make-an-autodiscover-request"></a><span data-ttu-id="30e66-151">发出的自动发现请求</span><span class="sxs-lookup"><span data-stu-id="30e66-151">Make an Autodiscover request</span></span>
<span data-ttu-id="30e66-152"><a name="bk_makeautodrequest"> </a></span><span class="sxs-lookup"><span data-stu-id="30e66-152"></span></span>

<span data-ttu-id="30e66-153">使用返回的地址`GetMailboxGuidAddress`方法，以调用自动发现。</span><span class="sxs-lookup"><span data-stu-id="30e66-153">Use the address returned by the  `GetMailboxGuidAddress` method to call Autodiscover.</span></span> <span data-ttu-id="30e66-154">我们建议您使用[Exchange 2013： 获取使用自动发现的用户设置](http://code.msdn.microsoft.com/exchange/Exchange-2013-Get-user-7e22c86e)调用自动发现服务，因为它简化的自动发现过程为您的代码示例。</span><span class="sxs-lookup"><span data-stu-id="30e66-154">We recommend that you use the [Exchange 2013: Get user settings with Autodiscover](http://code.msdn.microsoft.com/exchange/Exchange-2013-Get-user-7e22c86e) code sample to call the Autodiscover service because it streamlines the Autodiscover process for you.</span></span> <span data-ttu-id="30e66-155">此代码示例使用下表中列出的命令行参数来调用 POX 自动发现服务以检索与 GUID 邮箱关联的[AutoDiscoverSMTPAddress](http://msdn.microsoft.com/zh-cn/library/office/dn750991%28v=exchg.150%29.aspx)值。</span><span class="sxs-lookup"><span data-stu-id="30e66-155">This code sample uses the command-line arguments listed in the following table to call the POX Autodiscover service to retrieve the [AutoDiscoverSMTPAddress](http://msdn.microsoft.com/zh-cn/library/office/dn750991%28v=exchg.150%29.aspx) value associated with the mailbox GUID.</span></span> 
  
|<span data-ttu-id="30e66-156">**参数**</span><span class="sxs-lookup"><span data-stu-id="30e66-156">**Argument**</span></span>|<span data-ttu-id="30e66-157">**说明**</span><span class="sxs-lookup"><span data-stu-id="30e66-157">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="30e66-158">emailAddress</span><span class="sxs-lookup"><span data-stu-id="30e66-158">emailAddress</span></span>  <br/> |<span data-ttu-id="30e66-159">返回的地址`GetMailboxGuidAddress`中[确定的公用文件夹邮箱 GUID](http://msdn.microsoft.com/library/bk_determineguidewsma.aspx)方法。</span><span class="sxs-lookup"><span data-stu-id="30e66-159">The address returned by the  `GetMailboxGuidAddress` method in [Determine the GUID of the public folder mailbox](http://msdn.microsoft.com/library/bk_determineguidewsma.aspx).</span></span>  <br/> |
|<span data-ttu-id="30e66-160">-skipSOAP</span><span class="sxs-lookup"><span data-stu-id="30e66-160">-skipSOAP</span></span>  <br/> |<span data-ttu-id="30e66-161">指示 POX 自动发现请求所需。</span><span class="sxs-lookup"><span data-stu-id="30e66-161">Indicates that POX Autodiscover requests are required.</span></span>  <br/> |
|<span data-ttu-id="30e66-162">身份验证 authEmailAddress</span><span class="sxs-lookup"><span data-stu-id="30e66-162">-auth authEmailAddress</span></span>  <br/> |<span data-ttu-id="30e66-163">邮箱用户的电子邮件地址，用于进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="30e66-163">The mailbox user's email address, which is used for authentication.</span></span> <span data-ttu-id="30e66-164">系统将提示您输入邮箱用户的密码，当您运行示例。</span><span class="sxs-lookup"><span data-stu-id="30e66-164">You will be prompted to enter the mailbox user's password when you run the sample.</span></span>  <br/> |
   
<span data-ttu-id="30e66-165">例如，命令行参数应如下所示：</span><span class="sxs-lookup"><span data-stu-id="30e66-165">For example, the command-line arguments should look like this:</span></span>
  
`1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com -skipSOAP -auth sonyaf@contoso.com`

<span data-ttu-id="30e66-166">其中`1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com`是**GetMailboxGuidAddress**方法中，返回的地址和`sonyaf@contoso.com`是邮箱用户。</span><span class="sxs-lookup"><span data-stu-id="30e66-166">Where `1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com` is the address returned by the **GetMailboxGuidAddress** method, and `sonyaf@contoso.com` is the mailbox user.</span></span> 
  
<span data-ttu-id="30e66-167">当您运行**Exchange 2013： 获取使用自动发现的用户设置**示例的最后一个自动发现响应应成功和包含邮箱的邮箱 GUID 与关联的所有用户设置。</span><span class="sxs-lookup"><span data-stu-id="30e66-167">When you run the **Exchange 2013: Get user settings with Autodiscover** sample, the last Autodiscover response should be successful and include all the user settings associated with the mailbox GUID.</span></span> <span data-ttu-id="30e66-168">保存**AutoDiscoverSMTPAddress**用户设置本地，为您将使用的下一步。</span><span class="sxs-lookup"><span data-stu-id="30e66-168">Save the **AutoDiscoverSMTPAddress** user setting locally, as you'll use that in the next step.</span></span> 
  
<span data-ttu-id="30e66-169">此外，如果不想使用**Exchange 2013： 获取使用自动发现的用户设置**示例中，您可以获取**AutoDiscoverSMTPAddress**用户[生成的自动发现终结点列表](how-to-generate-a-list-of-autodiscover-endpoints.md)，由设置，然后发送以下对每个 URL，直到收到成功响应 POX 自动发现请求。</span><span class="sxs-lookup"><span data-stu-id="30e66-169">Alternatively, if you do not want to use **Exchange 2013: Get user settings with Autodiscover** sample, you can get the **AutoDiscoverSMTPAddress** user setting by [generating a list of Autodiscover endpoints](how-to-generate-a-list-of-autodiscover-endpoints.md), and then sending the following POX Autodiscover request to each URL until you receive a successful response.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="http://schemas.microsoft.com/exchange/autodiscover/outlook/requestschema/2006">
  <Request>
    <EMailAddress>1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com</EMailAddress>
    <AcceptableResponseSchema>http://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a</AcceptableResponseSchema>
  </Request>
</Autodiscover>
```

<span data-ttu-id="30e66-170">有关自动发现过程的详细信息，请参阅[exchange 自动发现](autodiscover-for-exchange.md)和[生成的自动发现终结点列表](how-to-generate-a-list-of-autodiscover-endpoints.md)中，[获取使用自动发现 Exchange 中的用户设置](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)。</span><span class="sxs-lookup"><span data-stu-id="30e66-170">For more information about the Autodiscover process, see [Autodiscover for Exchange](autodiscover-for-exchange.md), [Generate a list of Autodiscover endpoints](how-to-generate-a-list-of-autodiscover-endpoints.md), and [Get user settings from Exchange by using Autodiscover](how-to-get-user-settings-from-exchange-by-using-autodiscover.md).</span></span>
  
## <a name="set-the-values-of-the-x-anchormailbox-and-x-publicfoldermailbox-headers"></a><span data-ttu-id="30e66-171">X AnchorMailbox 和 X PublicFolderMailbox 标头的值</span><span class="sxs-lookup"><span data-stu-id="30e66-171">Set the values of the X-AnchorMailbox and X-PublicFolderMailbox headers</span></span>
<span data-ttu-id="30e66-172"><a name="bk_setheadervalues"> </a></span><span class="sxs-lookup"><span data-stu-id="30e66-172"></span></span>

<span data-ttu-id="30e66-173">使用**AutoDiscoverSMTPAddress**获得中[进行的自动发现请求](#bk_makeautodrequest)值，设置公用文件夹内容请求中的**X AnchorMailbox**和**X PublicFolderMailbox**头的值。</span><span class="sxs-lookup"><span data-stu-id="30e66-173">Using the value for the **AutoDiscoverSMTPAddress** acquired in [Make an Autodiscover request](#bk_makeautodrequest), set the values of the **X-AnchorMailbox** and **X-PublicFolderMailbox** headers in your public folder content request.</span></span> 
  
<span data-ttu-id="30e66-174">例如，给定 NewPublicFolder@contoso.com AutoDiscoverSMTPAddress，包括以下标头时调用以下方法或操作。</span><span class="sxs-lookup"><span data-stu-id="30e66-174">For example, given an AutoDiscoverSMTPAddress of NewPublicFolder@contoso.com, include the following headers when making calls to the following methods or operations.</span></span>
  
`X-AnchorMailbox: NewPublicFolder@contoso.com`<br/>
`X-PublicFolderMailbox: NewPublicFolder@contoso.com`

<span data-ttu-id="30e66-175">**需要 X AncorMailbox 和 X PublicFolder 标头的公用文件夹呼叫**</span><span class="sxs-lookup"><span data-stu-id="30e66-175">**Public folder calls that require the X-AncorMailbox and X-PublicFolder headers**</span></span>

|<span data-ttu-id="30e66-176">**EWS 托管 API 方法**</span><span class="sxs-lookup"><span data-stu-id="30e66-176">**EWS Managed API methods**</span></span>|<span data-ttu-id="30e66-177">**EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="30e66-177">**EWS operations**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="30e66-178">Item.Bind</span><span class="sxs-lookup"><span data-stu-id="30e66-178">Item.Bind</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="30e66-179">Item.Update</span><span class="sxs-lookup"><span data-stu-id="30e66-179">Item.Update</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.item.update%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="30e66-180">Item.Copy</span><span class="sxs-lookup"><span data-stu-id="30e66-180">Item.Copy</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.item.copy%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="30e66-181">Item.Move</span><span class="sxs-lookup"><span data-stu-id="30e66-181">Item.Move</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.item.move%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="30e66-182">Item.Delete</span><span class="sxs-lookup"><span data-stu-id="30e66-182">Item.Delete</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="30e66-183">Folder.Bind</span><span class="sxs-lookup"><span data-stu-id="30e66-183">Folder.Bind</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="30e66-184">Folder.FindItems</span><span class="sxs-lookup"><span data-stu-id="30e66-184">Folder.FindItems</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="30e66-185">CreateItem</span><span class="sxs-lookup"><span data-stu-id="30e66-185">CreateItem</span></span>](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/> [<span data-ttu-id="30e66-186">GetItem</span><span class="sxs-lookup"><span data-stu-id="30e66-186">GetItem</span></span>](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> [<span data-ttu-id="30e66-187">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="30e66-187">UpdateItem</span></span>](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> [<span data-ttu-id="30e66-188">CopyItem</span><span class="sxs-lookup"><span data-stu-id="30e66-188">CopyItem</span></span>](http://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> [<span data-ttu-id="30e66-189">MoveItem</span><span class="sxs-lookup"><span data-stu-id="30e66-189">MoveItem</span></span>](http://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/> [<span data-ttu-id="30e66-190">删除项</span><span class="sxs-lookup"><span data-stu-id="30e66-190">DeleteItem</span></span>](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> [<span data-ttu-id="30e66-191">GetFolder</span><span class="sxs-lookup"><span data-stu-id="30e66-191">GetFolder</span></span>](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> [<span data-ttu-id="30e66-192">FindItem</span><span class="sxs-lookup"><span data-stu-id="30e66-192">FindItem</span></span>](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) <br/> |
   
<span data-ttu-id="30e66-193">若要使用 EWS 托管 API 添加这些标头，请使用[HttpHeaders.Add](http://msdn.microsoft.com/zh-cn/library/system.net.http.headers.httpheaders.add%28v=vs.118%29.aspx)方法。</span><span class="sxs-lookup"><span data-stu-id="30e66-193">To add these headers by using the EWS Managed API, use the [HttpHeaders.Add](http://msdn.microsoft.com/zh-cn/library/system.net.http.headers.httpheaders.add%28v=vs.118%29.aspx) method.</span></span> 
  
```cs
service.HttpHeaders.Add("X-AnchorMailbox", "NewPublicFolder@contoso.com");
service.HttpHeaders.Add("X-PublicFolderMailbox", "NewPublicFolder@contoso.com");
```

<span data-ttu-id="30e66-194">下面的代码演示[GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx)请求**X AnchorMailbox**和**X PublicFolderMailbox**标头设置为在本文中的示例中检索值。</span><span class="sxs-lookup"><span data-stu-id="30e66-194">The following code shows a [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) request with the **X-AnchorMailbox** and **X-PublicFolderMailbox** header set to the values retrieved in the examples in this article.</span></span> 
  
```XML
POST https://outlook.office365.com/EWS/Exchange.asmx HTTP/1.1
Content-Type: text/xml; charset=utf-8
User-Agent: SoapSender1.0
X-AnchorMailbox: NewPublicFolder@contoso.com
X-PublicFolderMailbox: NewPublicFolder@contoso.com
Authorization: Basic c29ueWFmQGNvbnRvc28xMDAwLm9ubWljcm9zb2Z0LmNvbTpFWENIIzIwMTQ=
Host: outlook.office365.com
Content-Length: 688
Expect: 100-continue
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013_SP1" />
  </soap:Header>
  <soap:Body>
    <m:GetFolder>
      <m:FolderShape>
        <t:BaseShape>AllProperties</t:BaseShape>
      </m:FolderShape>
      <m:FolderIds>
        <t:DistinguishedFolderId Id="publicfoldersroot" />
      </m:FolderIds>
    </m:GetFolder>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="30e66-195">另请参阅</span><span class="sxs-lookup"><span data-stu-id="30e66-195">See also</span></span>

- [<span data-ttu-id="30e66-196">使用 EWS 在 Exchange 公用文件夹访问。</span><span class="sxs-lookup"><span data-stu-id="30e66-196">Public folder access with EWS in Exchange</span></span>](public-folder-access-with-ews-in-exchange.md)    
- [<span data-ttu-id="30e66-197">Exchange 自动发现</span><span class="sxs-lookup"><span data-stu-id="30e66-197">Autodiscover for Exchange</span></span>](autodiscover-for-exchange.md)    
- [<span data-ttu-id="30e66-198">生成自动发现终结点的列表</span><span class="sxs-lookup"><span data-stu-id="30e66-198">Generate a list of Autodiscover endpoints</span></span>](how-to-generate-a-list-of-autodiscover-endpoints.md)   
- [<span data-ttu-id="30e66-199">通过使用自动发现 Exchange 中获取用户设置</span><span class="sxs-lookup"><span data-stu-id="30e66-199">Get user settings from Exchange by using Autodiscover</span></span>](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    

