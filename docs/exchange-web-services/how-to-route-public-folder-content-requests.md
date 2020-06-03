---
title: 路由公用文件夹内容请求
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 59d2f05e-90fb-471e-ac06-70becc15b295
description: 需要将涉及公用文件夹内容的所有公用文件夹信息请求路由到包含目标文件夹内容的公用文件夹邮箱。 若要将请求路由到该邮箱，您需要将 X-anchormailbox 和 PublicFolderMailbox 标头设置为特定值。
ms.openlocfilehash: 523b9c8efc65253f7970fffeb5800e451784522d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527733"
---
# <a name="route-public-folder-content-requests"></a><span data-ttu-id="cef22-104">路由公用文件夹内容请求</span><span class="sxs-lookup"><span data-stu-id="cef22-104">Route public folder content requests</span></span>

<span data-ttu-id="cef22-105">需要将涉及公用文件夹内容的所有公用文件夹信息请求路由到包含目标文件夹内容的公用文件夹邮箱。</span><span class="sxs-lookup"><span data-stu-id="cef22-105">All requests for public folder information that involve the content of the public folder need to be routed to the public folder mailbox that holds the content for the target folder.</span></span> <span data-ttu-id="cef22-106">若要将请求路由到该邮箱，您需要将**x-anchormailbox**和**PublicFolderMailbox**标头设置为特定值。</span><span class="sxs-lookup"><span data-stu-id="cef22-106">To route the requests to that mailbox, you need to set the **X-AnchorMailbox** and **X-PublicFolderMailbox** headers to specific values.</span></span> 
  
<span data-ttu-id="cef22-107">下表提供了该过程的概述：</span><span class="sxs-lookup"><span data-stu-id="cef22-107">The following table provides an overview of the process:</span></span>
  
<span data-ttu-id="cef22-108">**公用文件夹概述**</span><span class="sxs-lookup"><span data-stu-id="cef22-108">**Public folder overview**</span></span>

|<span data-ttu-id="cef22-109">标头</span><span class="sxs-lookup"><span data-stu-id="cef22-109">Header</span></span>|<span data-ttu-id="cef22-110">我需要什么？</span><span class="sxs-lookup"><span data-stu-id="cef22-110">What do I need?</span></span>|<span data-ttu-id="cef22-111">如何获取？</span><span class="sxs-lookup"><span data-stu-id="cef22-111">How do I get it?</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cef22-112">**X-X-anchormailbox**</span><span class="sxs-lookup"><span data-stu-id="cef22-112">**X-AnchorMailbox**</span></span> <br/> |<span data-ttu-id="cef22-113">1. 公用文件夹层次结构邮箱[的 x-x-anchormailbox 和 x PublicFolderInformation 值](how-to-route-public-folder-hierarchy-requests.md)。</span><span class="sxs-lookup"><span data-stu-id="cef22-113">1. [The X-AnchorMailbox and X-PublicFolderInformation values ](how-to-route-public-folder-hierarchy-requests.md) for the public folder hierarchy mailbox.</span></span><br/><br/><span data-ttu-id="cef22-114">2. 包含邮箱内容的公用文件夹邮箱的 GUID，该邮箱内容将发送到自动发现服务。</span><span class="sxs-lookup"><span data-stu-id="cef22-114">2. The GUID of the public folder mailbox that contains the mailbox content, which is sent to the Autodiscover service.</span></span><br/><br/>  <span data-ttu-id="cef22-115">Autodisover 响应中的**AutoDiscoverSMTPAddress**将成为**X x-anchormailbox**标头的值。</span><span class="sxs-lookup"><span data-stu-id="cef22-115">The **AutoDiscoverSMTPAddress** in the Autodisover response becomes the value of the **X-AnchorMailbox** header.</span></span>  <br/> <span data-ttu-id="cef22-116">![TODO](media/Ex15_PF_PFContent.png)</span><span class="sxs-lookup"><span data-stu-id="cef22-116">![TODO](media/Ex15_PF_PFContent.png)</span></span>| <span data-ttu-id="cef22-117">1. 使用本文中的代码示例，这将[实现 EWS 托管 API](#bk_determineguidewsma)。</span><span class="sxs-lookup"><span data-stu-id="cef22-117">1. Use the code example in this article, which [implements the EWS Managed API](#bk_determineguidewsma).</span></span> <span data-ttu-id="cef22-118">或[使用 EWS](#bk_determineguidews)并转换结果以获取 GUID。</span><span class="sxs-lookup"><span data-stu-id="cef22-118">Or [use EWS](#bk_determineguidews) and convert your results to obtain a GUID.</span></span><br/><br/><span data-ttu-id="cef22-119">2. 使用 GUID 加上域名[进行自动发现请求](#bk_makeautodrequest)。</span><span class="sxs-lookup"><span data-stu-id="cef22-119">2. [Make an Autodiscover request](#bk_makeautodrequest) by using the GUID plus the domain name.</span></span><br/><br/><span data-ttu-id="cef22-120">3. 使用自动发现响应中返回的**AutoDiscoverSMTPAddress**元素的值来[填充标头的值](#bk_setheadervalues)。</span><span class="sxs-lookup"><span data-stu-id="cef22-120">3. Use the value of the **AutoDiscoverSMTPAddress** element returned in the Autodiscover response to [populate the value of the headers](#bk_setheadervalues).</span></span>  <br/> |
|<span data-ttu-id="cef22-121">**X-PublicFolderMailbox**</span><span class="sxs-lookup"><span data-stu-id="cef22-121">**X-PublicFolderMailbox**</span></span> <br/> |<span data-ttu-id="cef22-122">您的工作已完成，则 PublicFolderMailbox 值与 X-X-anchormailbox 值相同！</span><span class="sxs-lookup"><span data-stu-id="cef22-122">Your work is done, the X-PublicFolderMailbox value is the same as the X-AnchorMailbox value!</span></span>  <br/> |<span data-ttu-id="cef22-123">你已拥有！</span><span class="sxs-lookup"><span data-stu-id="cef22-123">You already have it!</span></span>  <br/> |
   
<span data-ttu-id="cef22-124">在确定了标头值之后，请[在创建公用文件夹内容请求时](#bk_setheadervalues)将其包括在内。</span><span class="sxs-lookup"><span data-stu-id="cef22-124">After you have determined the header values, include them [when you make public folder content requests](#bk_setheadervalues).</span></span>
  
<span data-ttu-id="cef22-125">本文中的步骤特定于公用文件夹内容请求。</span><span class="sxs-lookup"><span data-stu-id="cef22-125">The steps in this article are specific to public folder content requests.</span></span> <span data-ttu-id="cef22-126">若要确定您的请求是否为公用文件夹层次结构或内容请求，请参阅[路由公用文件夹请求](public-folder-access-with-ews-in-exchange.md#bk_routing)。</span><span class="sxs-lookup"><span data-stu-id="cef22-126">To determine whether your request is a public folder hierarchy or content request, see [Routing public folder requests](public-folder-access-with-ews-in-exchange.md#bk_routing).</span></span>

<span data-ttu-id="cef22-127"><a name="bk_determineguidewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="cef22-127"><a name="bk_determineguidewsma"> </a></span></span>

## <a name="determine-the-guid-of-the-public-folder-mailbox-by-using-the-ews-managed-api"></a><span data-ttu-id="cef22-128">使用 EWS 托管 API 确定公用文件夹邮箱的 GUID</span><span class="sxs-lookup"><span data-stu-id="cef22-128">Determine the GUID of the public folder mailbox by using the EWS Managed API</span></span>


<span data-ttu-id="cef22-129">若要确定公用文件夹内容邮箱的 GUID，请使用下面的代码示例，它执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="cef22-129">To determine the GUID of the public folder content mailbox, use the following code example, which does the following:</span></span> 
  
- <span data-ttu-id="cef22-130">使用通过[路由公用文件夹层次结构请求](how-to-route-public-folder-hierarchy-requests.md)检索到的**X-anchormailbox**和**x PublicFolderInformation**的标题。</span><span class="sxs-lookup"><span data-stu-id="cef22-130">Uses the **X-AnchorMailbox** and **X-PublicFolderInformation** headers you retrieved by [routing public folder hierarchy requests](how-to-route-public-folder-hierarchy-requests.md).</span></span>
    
- <span data-ttu-id="cef22-131">调用 EWS 托管 API [FindFolders](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)方法，并包含**PR_REPLICA_LIST** （0x66980102）属性的请求</span><span class="sxs-lookup"><span data-stu-id="cef22-131">Calls the EWS Managed API [FindFolders](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) method, and includes a request for the **PR_REPLICA_LIST** (0x66980102) property</span></span> 
    
<span data-ttu-id="cef22-132">**PR_REPLICA_LIST**值标识包含该文件夹内容的公用文件夹邮箱的邮箱 GUID。</span><span class="sxs-lookup"><span data-stu-id="cef22-132">The **PR_REPLICA_LIST** value identifies the mailbox GUID of the public folder mailbox that has the content for the folder.</span></span> <span data-ttu-id="cef22-133">**PR_REPLICA_LIST**属性是一个字节数组，但它将强制转换为此方案的 GUID。</span><span class="sxs-lookup"><span data-stu-id="cef22-133">The **PR_REPLICA_LIST** property is a byte array, but is cast as a GUID for this scenario.</span></span> <span data-ttu-id="cef22-134">GUID 和域名串联在一起，以形成要调用自动发现的地址。</span><span class="sxs-lookup"><span data-stu-id="cef22-134">The GUID and the domain name are concatenated to form the address on which to call Autodiscover.</span></span> 
  
<span data-ttu-id="cef22-135">此示例假定 `service` 为邮箱用户的[ExchangeService](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象， `PFHAnchorHeader` 并且是 `PFHMailboxHeader` **x-x-anchormailbox**和**x PublicFolderMailbox**标头的值，而 domain 是租户使用的域名。</span><span class="sxs-lookup"><span data-stu-id="cef22-135">This example assumes that  `service` is the [ExchangeService](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the mailbox user,  `PFHAnchorHeader` and  `PFHMailboxHeader` are the values of the **X-AnchorMailbox** and **X-PublicFolderMailbox** headers, and domain is the domain name used by the tenant.</span></span> 
  
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

<span data-ttu-id="cef22-136">如果收到错误 "请求失败。</span><span class="sxs-lookup"><span data-stu-id="cef22-136">If you received the error "The request failed.</span></span> <span data-ttu-id="cef22-137">基础连接已关闭：无法为 SSL/TLS 安全通道建立信任关系，将需要[添加对验证回调方法的调用](how-to-validate-a-server-certificate-for-the-ews-managed-api.md)。</span><span class="sxs-lookup"><span data-stu-id="cef22-137">The underlying connection was closed: Could not establish trust relationship for the SSL/TLS secure channel", you'll need to [add a call to a validation callback method](how-to-validate-a-server-certificate-for-the-ews-managed-api.md).</span></span> <span data-ttu-id="cef22-138">该方法的占位符和注释包含在代码示例中。</span><span class="sxs-lookup"><span data-stu-id="cef22-138">A placeholder and comment for that method is included in the code example.</span></span>
  
<span data-ttu-id="cef22-139">如果公用文件夹根目录下的所有公用文件夹的邮箱 GUID 都相同，则此示例指示在控制台输出中[调用自动发现](#bk_makeautodrequest)时要使用的地址，并将其作为返回值。</span><span class="sxs-lookup"><span data-stu-id="cef22-139">If the mailbox GUID is the same for all the public folders under the public folder root, the example indicates the address to use when [calling Autodiscover](#bk_makeautodrequest) in the console output and as the return value.</span></span> <span data-ttu-id="cef22-140">如果公用文件夹根目录下的所有公用文件夹的邮箱 GUID 不相同，则需要对与内容请求中的文件夹相关联的地址[进行自动发现请求](#bk_makeautodrequest)。</span><span class="sxs-lookup"><span data-stu-id="cef22-140">If the mailbox GUID is not the same for all public folders under the public folder root, you need to [Make an Autodiscover request](#bk_makeautodrequest) on the address associated with the folder in your content request.</span></span> 

<span data-ttu-id="cef22-141"><a name="bk_determineguidews"> </a></span><span class="sxs-lookup"><span data-stu-id="cef22-141"><a name="bk_determineguidews"> </a></span></span>

## <a name="determine-the-guid-of-the-public-folder-mailbox-by-using-ews"></a><span data-ttu-id="cef22-142">使用 EWS 确定公用文件夹邮箱的 GUID</span><span class="sxs-lookup"><span data-stu-id="cef22-142">Determine the GUID of the public folder mailbox by using EWS</span></span>

<span data-ttu-id="cef22-143">下面的代码示例演示如何使用 EWS [FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)操作检索**PR_REPLICA_LIST** （0x66980102）属性的值。</span><span class="sxs-lookup"><span data-stu-id="cef22-143">The following code example shows how retrieve the value of the **PR_REPLICA_LIST** (0x66980102) property by using the EWS [FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="cef22-144">对于[ExtendedFieldURI](https://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx)元素，将**PropertyTag**属性设置为**PR_REPLICA_LIST**属性的十进制值（26264），并将**recordtype**属性设置为**Binary**。</span><span class="sxs-lookup"><span data-stu-id="cef22-144">For the [ExtendedFieldURI](https://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx) element, the **PropertyTag** attribute is set to the decimal value (26264) of the **PR_REPLICA_LIST** property, and the **PropertyType** attribute is set to **Binary**.</span></span>
  
<span data-ttu-id="cef22-145">这也是在使用**FindFolders**方法以[使用 EWS 托管 api 确定公用文件夹邮箱的 GUID](#bk_determineguidewsma)时，EWS 托管 api 发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="cef22-145">This is also the XML request that the EWS Managed API sends when you use the **FindFolders** method to [determine the GUID of the public folder mailbox by using the EWS Managed API](#bk_determineguidewsma).</span></span>
  
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
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="cef22-146">服务器使用[FindFolderResponse](https://msdn.microsoft.com/library/f5dd813c-9698-4a39-8fca-3a825df365ed%28Office.15%29.aspx)邮件响应**FindFolder**请求，其中包含**PR_REPLICA_LIST**扩展属性的值。</span><span class="sxs-lookup"><span data-stu-id="cef22-146">The server responds to the **FindFolder** request with a [FindFolderResponse](https://msdn.microsoft.com/library/f5dd813c-9698-4a39-8fca-3a825df365ed%28Office.15%29.aspx) message that includes the value of the **PR_REPLICA_LIST** extended property.</span></span> <span data-ttu-id="cef22-147">请注意，该属性的值在 EWS 响应中显示为以64编码的字节数组的字符串格式。</span><span class="sxs-lookup"><span data-stu-id="cef22-147">Note that the value of the property appears on the EWS response as the string format of a base-64 encoded byte array.</span></span> <span data-ttu-id="cef22-148">为了提高可读性，响应中的某些标头值会缩短。</span><span class="sxs-lookup"><span data-stu-id="cef22-148">Some header values in the response are shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?><s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="1019" MinorBuildNumber="15" Version="V2_17" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body>
    <m:FindFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="cef22-149">若要使用 XML 中返回的**PR_REPLICA_LIST**的值 MWVjMmEyMzYtZWQ5My00Zjg4LWI5YzYtMzNlNjNmYTRhYTQ0AA = =，以确定邮箱 GUID，则必须将该值转换为 GUID，格式类似于在[EWS 托管 API 代码示例](#bk_determineguidewsma)中如何转换值。</span><span class="sxs-lookup"><span data-stu-id="cef22-149">In order to use the value of the **PR_REPLICA_LIST** returned in the XML, MWVjMmEyMzYtZWQ5My00Zjg4LWI5YzYtMzNlNjNmYTRhYTQ0AA==, to determine the mailbox GUID, the value must be converted into a GUID in a format similar to how the value is converted in the [EWS Managed API code example](#bk_determineguidewsma).</span></span> <span data-ttu-id="cef22-150">然后，将 GUID 与域名串联在一起，以创建一个 SMTP 地址，该地址包含在[自动发现请求](#bk_makeautodrequest)中。</span><span class="sxs-lookup"><span data-stu-id="cef22-150">The GUID is then concatenated with the domain name to create an SMTP address, which is included in the [Autodiscover request](#bk_makeautodrequest).</span></span>
  
## <a name="make-an-autodiscover-request"></a><span data-ttu-id="cef22-151">发出自动发现请求</span><span class="sxs-lookup"><span data-stu-id="cef22-151">Make an Autodiscover request</span></span>
<span data-ttu-id="cef22-152"><a name="bk_makeautodrequest"> </a></span><span class="sxs-lookup"><span data-stu-id="cef22-152"><a name="bk_makeautodrequest"> </a></span></span>

<span data-ttu-id="cef22-153">使用方法返回的地址 `GetMailboxGuidAddress` 调用自动发现。</span><span class="sxs-lookup"><span data-stu-id="cef22-153">Use the address returned by the  `GetMailboxGuidAddress` method to call Autodiscover.</span></span> <span data-ttu-id="cef22-154">建议使用[Exchange 2013： Get user settings With 自动发现](https://code.msdn.microsoft.com/exchange/Exchange-2013-Get-user-7e22c86e)代码示例，以调用自动发现服务，因为它可简化自动发现过程。</span><span class="sxs-lookup"><span data-stu-id="cef22-154">We recommend that you use the [Exchange 2013: Get user settings with Autodiscover](https://code.msdn.microsoft.com/exchange/Exchange-2013-Get-user-7e22c86e) code sample to call the Autodiscover service because it streamlines the Autodiscover process for you.</span></span> <span data-ttu-id="cef22-155">此代码示例使用下表中列出的命令行参数调用 POX 自动发现服务，以检索与邮箱 GUID 关联的[AutoDiscoverSMTPAddress](https://msdn.microsoft.com/library/office/dn750991%28v=exchg.150%29.aspx)值。</span><span class="sxs-lookup"><span data-stu-id="cef22-155">This code sample uses the command-line arguments listed in the following table to call the POX Autodiscover service to retrieve the [AutoDiscoverSMTPAddress](https://msdn.microsoft.com/library/office/dn750991%28v=exchg.150%29.aspx) value associated with the mailbox GUID.</span></span> 

  
|<span data-ttu-id="cef22-156">**参数**</span><span class="sxs-lookup"><span data-stu-id="cef22-156">**Argument**</span></span>|<span data-ttu-id="cef22-157">**说明**</span><span class="sxs-lookup"><span data-stu-id="cef22-157">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cef22-158">emailAddress</span><span class="sxs-lookup"><span data-stu-id="cef22-158">emailAddress</span></span>  <br/> |<span data-ttu-id="cef22-159">`GetMailboxGuidAddress`方法在[确定公用文件夹邮箱的 GUID](#bk_determineguidewsma)时返回的地址。</span><span class="sxs-lookup"><span data-stu-id="cef22-159">The address returned by the  `GetMailboxGuidAddress` method in [Determine the GUID of the public folder mailbox](#bk_determineguidewsma).</span></span>  <br/> |
|<span data-ttu-id="cef22-160">-skipSOAP</span><span class="sxs-lookup"><span data-stu-id="cef22-160">-skipSOAP</span></span>  <br/> |<span data-ttu-id="cef22-161">指示 POX 自动发现请求是必需的。</span><span class="sxs-lookup"><span data-stu-id="cef22-161">Indicates that POX Autodiscover requests are required.</span></span>  <br/> |
|<span data-ttu-id="cef22-162">-auth authEmailAddress</span><span class="sxs-lookup"><span data-stu-id="cef22-162">-auth authEmailAddress</span></span>  <br/> |<span data-ttu-id="cef22-163">邮箱用户的电子邮件地址，用于进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="cef22-163">The mailbox user's email address, which is used for authentication.</span></span> <span data-ttu-id="cef22-164">在运行此示例时，系统将提示您输入邮箱用户的密码。</span><span class="sxs-lookup"><span data-stu-id="cef22-164">You will be prompted to enter the mailbox user's password when you run the sample.</span></span>  <br/> |
   
<span data-ttu-id="cef22-165">例如，命令行参数应如下所示：</span><span class="sxs-lookup"><span data-stu-id="cef22-165">For example, the command-line arguments should look like this:</span></span>
  
`1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com -skipSOAP -auth sonyaf@contoso.com`

<span data-ttu-id="cef22-166">其中， `1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com` 是**GetMailboxGuidAddress**方法返回的地址， `sonyaf@contoso.com` 是邮箱用户。</span><span class="sxs-lookup"><span data-stu-id="cef22-166">Where `1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com` is the address returned by the **GetMailboxGuidAddress** method, and `sonyaf@contoso.com` is the mailbox user.</span></span> 
  
<span data-ttu-id="cef22-167">当您运行**Exchange 2013：使用自动发现示例获取用户设置**时，最后一个自动发现响应应成功，并包含与邮箱 GUID 关联的所有用户设置。</span><span class="sxs-lookup"><span data-stu-id="cef22-167">When you run the **Exchange 2013: Get user settings with Autodiscover** sample, the last Autodiscover response should be successful and include all the user settings associated with the mailbox GUID.</span></span> <span data-ttu-id="cef22-168">在本地保存**AutoDiscoverSMTPAddress**用户设置，在下一步中将使用该设置。</span><span class="sxs-lookup"><span data-stu-id="cef22-168">Save the **AutoDiscoverSMTPAddress** user setting locally, as you'll use that in the next step.</span></span> 
  
<span data-ttu-id="cef22-169">或者，如果您不想使用**Exchange 2013：使用自动发现示例获取用户设置**，则可以通过[生成自动发现终结点列表](how-to-generate-a-list-of-autodiscover-endpoints.md)来获取**AutoDiscoverSMTPAddress**用户设置，然后向每个 URL 发送以下 POX 自动发现请求，直到您收到成功的响应。</span><span class="sxs-lookup"><span data-stu-id="cef22-169">Alternatively, if you do not want to use **Exchange 2013: Get user settings with Autodiscover** sample, you can get the **AutoDiscoverSMTPAddress** user setting by [generating a list of Autodiscover endpoints](how-to-generate-a-list-of-autodiscover-endpoints.md), and then sending the following POX Autodiscover request to each URL until you receive a successful response.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="https://schemas.microsoft.com/exchange/autodiscover/outlook/requestschema/2006">
  <Request>
    <EMailAddress>1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com</EMailAddress>
    <AcceptableResponseSchema>https://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a</AcceptableResponseSchema>
  </Request>
</Autodiscover>
```

<span data-ttu-id="cef22-170">有关自动发现过程的详细信息，请参阅[exchange 的自动发现](autodiscover-for-exchange.md)，[生成自动发现终结点列表](how-to-generate-a-list-of-autodiscover-endpoints.md)，并[使用自动发现获取 Exchange 中的用户设置](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)。</span><span class="sxs-lookup"><span data-stu-id="cef22-170">For more information about the Autodiscover process, see [Autodiscover for Exchange](autodiscover-for-exchange.md), [Generate a list of Autodiscover endpoints](how-to-generate-a-list-of-autodiscover-endpoints.md), and [Get user settings from Exchange by using Autodiscover](how-to-get-user-settings-from-exchange-by-using-autodiscover.md).</span></span>
  
## <a name="set-the-values-of-the-x-anchormailbox-and-x-publicfoldermailbox-headers"></a><span data-ttu-id="cef22-171">设置 X-anchormailbox 和 PublicFolderMailbox 标头的值</span><span class="sxs-lookup"><span data-stu-id="cef22-171">Set the values of the X-AnchorMailbox and X-PublicFolderMailbox headers</span></span>
<span data-ttu-id="cef22-172"><a name="bk_setheadervalues"> </a></span><span class="sxs-lookup"><span data-stu-id="cef22-172"><a name="bk_setheadervalues"> </a></span></span>

<span data-ttu-id="cef22-173">使用 AutoDiscoverSMTPAddress 中获取的**AutoDiscoverSMTPAddress**的值，在公用文件夹内容[请求中设置](#bk_makeautodrequest) **x-anchormailbox**和**x PublicFolderMailbox**标头的值。</span><span class="sxs-lookup"><span data-stu-id="cef22-173">Using the value for the **AutoDiscoverSMTPAddress** acquired in [Make an Autodiscover request](#bk_makeautodrequest), set the values of the **X-AnchorMailbox** and **X-PublicFolderMailbox** headers in your public folder content request.</span></span> 
  
<span data-ttu-id="cef22-174">例如，给定 AutoDiscoverSMTPAddress 的 NewPublicFolder@contoso.com，在调用以下方法或操作时，请包含以下标头。</span><span class="sxs-lookup"><span data-stu-id="cef22-174">For example, given an AutoDiscoverSMTPAddress of NewPublicFolder@contoso.com, include the following headers when making calls to the following methods or operations.</span></span>
  
`X-AnchorMailbox: NewPublicFolder@contoso.com`<br/>
`X-PublicFolderMailbox: NewPublicFolder@contoso.com`

<span data-ttu-id="cef22-175">**需要 AncorMailbox 和 Set-publicfolder 头的公用文件夹调用**</span><span class="sxs-lookup"><span data-stu-id="cef22-175">**Public folder calls that require the X-AncorMailbox and X-PublicFolder headers**</span></span>

|<span data-ttu-id="cef22-176">**EWS 托管 API 方法**</span><span class="sxs-lookup"><span data-stu-id="cef22-176">**EWS Managed API methods**</span></span>|<span data-ttu-id="cef22-177">**EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="cef22-177">**EWS operations**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cef22-178">Item.Bind</span><span class="sxs-lookup"><span data-stu-id="cef22-178">Item.Bind</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="cef22-179">Item.Update</span><span class="sxs-lookup"><span data-stu-id="cef22-179">Item.Update</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.update%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="cef22-180">项。复制</span><span class="sxs-lookup"><span data-stu-id="cef22-180">Item.Copy</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.copy%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="cef22-181">Item。 Move</span><span class="sxs-lookup"><span data-stu-id="cef22-181">Item.Move</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.move%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="cef22-182">Item.Delete</span><span class="sxs-lookup"><span data-stu-id="cef22-182">Item.Delete</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="cef22-183">文件夹。绑定</span><span class="sxs-lookup"><span data-stu-id="cef22-183">Folder.Bind</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="cef22-184">FindItems</span><span class="sxs-lookup"><span data-stu-id="cef22-184">Folder.FindItems</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="cef22-185">CreateItem</span><span class="sxs-lookup"><span data-stu-id="cef22-185">CreateItem</span></span>](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/> [<span data-ttu-id="cef22-186">GetItem</span><span class="sxs-lookup"><span data-stu-id="cef22-186">GetItem</span></span>](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> [<span data-ttu-id="cef22-187">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="cef22-187">UpdateItem</span></span>](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> [<span data-ttu-id="cef22-188">CopyItem</span><span class="sxs-lookup"><span data-stu-id="cef22-188">CopyItem</span></span>](https://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> [<span data-ttu-id="cef22-189">MoveItem</span><span class="sxs-lookup"><span data-stu-id="cef22-189">MoveItem</span></span>](https://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/> [<span data-ttu-id="cef22-190">DeleteItem</span><span class="sxs-lookup"><span data-stu-id="cef22-190">DeleteItem</span></span>](../web-service-reference/deleteitem-operation.md) <br/> [<span data-ttu-id="cef22-191">GetFolder</span><span class="sxs-lookup"><span data-stu-id="cef22-191">GetFolder</span></span>](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> [<span data-ttu-id="cef22-192">FindItem</span><span class="sxs-lookup"><span data-stu-id="cef22-192">FindItem</span></span>](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) <br/> |
   
<span data-ttu-id="cef22-193">若要使用 EWS 托管 API 添加这些邮件头，请使用[HttpHeaders](https://msdn.microsoft.com/library/system.net.http.headers.httpheaders.add%28v=vs.118%29.aspx)方法。</span><span class="sxs-lookup"><span data-stu-id="cef22-193">To add these headers by using the EWS Managed API, use the [HttpHeaders.Add](https://msdn.microsoft.com/library/system.net.http.headers.httpheaders.add%28v=vs.118%29.aspx) method.</span></span> 
  
```cs
service.HttpHeaders.Add("X-AnchorMailbox", "NewPublicFolder@contoso.com");
service.HttpHeaders.Add("X-PublicFolderMailbox", "NewPublicFolder@contoso.com");
```

<span data-ttu-id="cef22-194">以下代码显示了[GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx)请求，其中**x-X-anchormailbox**和**x PublicFolderMailbox**标头设置为在本文的示例中检索到的值。</span><span class="sxs-lookup"><span data-stu-id="cef22-194">The following code shows a [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) request with the **X-AnchorMailbox** and **X-PublicFolderMailbox** header set to the values retrieved in the examples in this article.</span></span> 
  
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
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

## <a name="see-also"></a><span data-ttu-id="cef22-195">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cef22-195">See also</span></span>

- [<span data-ttu-id="cef22-196">使用 EWS 在 Exchange 公用文件夹访问。</span><span class="sxs-lookup"><span data-stu-id="cef22-196">Public folder access with EWS in Exchange</span></span>](public-folder-access-with-ews-in-exchange.md)    
- [<span data-ttu-id="cef22-197">Exchange 自动发现</span><span class="sxs-lookup"><span data-stu-id="cef22-197">Autodiscover for Exchange</span></span>](autodiscover-for-exchange.md)    
- [<span data-ttu-id="cef22-198">生成自动发现终结点列表</span><span class="sxs-lookup"><span data-stu-id="cef22-198">Generate a list of Autodiscover endpoints</span></span>](how-to-generate-a-list-of-autodiscover-endpoints.md)   
- [<span data-ttu-id="cef22-199">使用自动发现从 Exchange 获取用户设置</span><span class="sxs-lookup"><span data-stu-id="cef22-199">Get user settings from Exchange by using Autodiscover</span></span>](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
  