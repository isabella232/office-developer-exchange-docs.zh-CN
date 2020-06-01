---
title: 使用 Exchange 中的 EWS 处理隐藏的文件夹
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7ae7c045-cd90-4c9f-baf5-0464d5058f45
description: 了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS 使文件夹隐藏并查找隐藏文件夹。
ms.openlocfilehash: d4fa44a0399542350668359e8abb88d2a0a9d579
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456372"
---
# <a name="work-with-hidden-folders-by-using-ews-in-exchange"></a><span data-ttu-id="2f576-103">使用 Exchange 中的 EWS 处理隐藏的文件夹</span><span class="sxs-lookup"><span data-stu-id="2f576-103">Work with hidden folders by using EWS in Exchange</span></span>

<span data-ttu-id="2f576-104">了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS 使文件夹隐藏并查找隐藏文件夹。</span><span class="sxs-lookup"><span data-stu-id="2f576-104">Learn how to make a folder hidden and find hidden folders by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="2f576-105">除了一个例外，Exchange 邮箱根目录中的文件夹（非 IPM 子树）对用户是隐藏的。</span><span class="sxs-lookup"><span data-stu-id="2f576-105">With one exception, folders in the root of an Exchange mailbox (the non-IPM subtree) are hidden from the user.</span></span> <span data-ttu-id="2f576-106">相反， **MsgFolderRoot** （IPM 子树）中的所有文件夹对用户都是可见的。</span><span class="sxs-lookup"><span data-stu-id="2f576-106">Conversely, all folders in the **MsgFolderRoot** (the IPM subtree) are visible to the user.</span></span> <span data-ttu-id="2f576-107">那么，如何隐藏**MsgFolderRoot**下的文件夹？</span><span class="sxs-lookup"><span data-stu-id="2f576-107">So how do you hide a folder under the **MsgFolderRoot**?</span></span> <span data-ttu-id="2f576-108">这并不难—它只是一个属性，即[PidTagAttributeHidden](https://msdn.microsoft.com/library/cc433490%28v=exchg.80%29.aspx) （0x10F4000B）扩展属性。</span><span class="sxs-lookup"><span data-stu-id="2f576-108">It's not that tricky — it comes down to just one property, the [PidTagAttributeHidden](https://msdn.microsoft.com/library/cc433490%28v=exchg.80%29.aspx) (0x10F4000B) extended property.</span></span> <span data-ttu-id="2f576-109">当此属性设置为**true**时，Outlook 或另一个使用属性来确定文件夹可见性的客户端将从用户的视图中隐藏该文件夹。</span><span class="sxs-lookup"><span data-stu-id="2f576-109">When this property is set to **true**, Outlook or another client that uses the property to determine folder visibility will hide the folder from the user's view.</span></span> <span data-ttu-id="2f576-110">由于这是一个扩展属性，因此比您的 average folder 属性更复杂，因此本文将引导您完成主要方案。</span><span class="sxs-lookup"><span data-stu-id="2f576-110">Because this is an extended property, it's more complex to use than your average folder property, so this article will walk you through the main scenarios.</span></span>
  
<span data-ttu-id="2f576-111">**表1。用于处理隐藏文件夹的 EWS 托管 API 方法和 EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="2f576-111">**Table 1. EWS Managed API methods and EWS operations for working with hidden folders**</span></span>

|<span data-ttu-id="2f576-112">**任务**</span><span class="sxs-lookup"><span data-stu-id="2f576-112">**Task**</span></span>|<span data-ttu-id="2f576-113">**EWS 托管的 API 方法**</span><span class="sxs-lookup"><span data-stu-id="2f576-113">**EWS Managed API method**</span></span>|<span data-ttu-id="2f576-114">**EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="2f576-114">**EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2f576-115">隐藏文件夹</span><span class="sxs-lookup"><span data-stu-id="2f576-115">Hide a folder</span></span>  <br/> |<span data-ttu-id="2f576-116">先[绑定文件夹](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) [. 更新](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2f576-116">[Folder.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) followed by [Folder.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="2f576-117">[GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx)后接[UpdateFolder](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2f576-117">[GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) followed by [UpdateFolder](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx)</span></span> <br/> |
|<span data-ttu-id="2f576-118">查找隐藏文件夹</span><span class="sxs-lookup"><span data-stu-id="2f576-118">Find hidden folders</span></span>  <br/> |[<span data-ttu-id="2f576-119">FindFolders</span><span class="sxs-lookup"><span data-stu-id="2f576-119">FindFolders</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="2f576-120">FindFolder</span><span class="sxs-lookup"><span data-stu-id="2f576-120">FindFolder</span></span>](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) <br/> |
   
<span data-ttu-id="2f576-121">您是否想知道哪种例外是什么（即，根中的哪个文件夹对用户是可见的）？</span><span class="sxs-lookup"><span data-stu-id="2f576-121">Are you wondering what the one exception is — that is, what folder in the root IS visible to users?</span></span> <span data-ttu-id="2f576-122">它是 Finder 文件夹（也称为**SearchFolders**[WellKnownFolder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx)枚举值，或**SearchFolders**[DistinguishedFolderId](https://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx)元素值），其中包含用户的搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="2f576-122">It's the Finder folder (also known as the **SearchFolders**[WellKnownFolder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) enumeration value, or the **searchfolders**[DistinguishedFolderId](https://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) element value), which contains users' search folders.</span></span> <span data-ttu-id="2f576-123">在 Finder 文件夹中创建的搜索文件夹对 Outlook 用户是可见的。</span><span class="sxs-lookup"><span data-stu-id="2f576-123">Search folders created in the Finder folder are visible to Outlook users.</span></span> <span data-ttu-id="2f576-124">如果您需要创建对用户不可见的搜索文件夹，请将其移动到根文件夹下以将其隐藏。</span><span class="sxs-lookup"><span data-stu-id="2f576-124">If you need to create a search folder that is not visible to users, move it under the root folder to hide it.</span></span> <span data-ttu-id="2f576-125">与其他文件夹不同的是，将**PidTagAttributeHidden**属性设置为**true**将不会隐藏 Finder 文件夹中的搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="2f576-125">Unlike for other folders, setting the **PidTagAttributeHidden** property to **true** will not hide a search folder in the Finder folder.</span></span> 
  
## <a name="hide-a-folder-by-using-the-ews-managed-api"></a><span data-ttu-id="2f576-126">使用 EWS 托管 API 隐藏文件夹</span><span class="sxs-lookup"><span data-stu-id="2f576-126">Hide a folder by using the EWS Managed API</span></span>
<span data-ttu-id="2f576-127"><a name="bk_hideewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="2f576-127"><a name="bk_hideewsma"> </a></span></span>

<span data-ttu-id="2f576-128">通过将[PidTagAttributeHidden](https://msdn.microsoft.com/library/cc433490%28v=exchg.80%29.aspx)扩展属性更改为**true**，可以[将现有文件夹设置](how-to-work-with-folders-by-using-ews-in-exchange.md#bk_createfolderewsma)为隐藏文件夹。</span><span class="sxs-lookup"><span data-stu-id="2f576-128">You can [make an existing folder](how-to-work-with-folders-by-using-ews-in-exchange.md#bk_createfolderewsma) a hidden folder by changing the [PidTagAttributeHidden](https://msdn.microsoft.com/library/cc433490%28v=exchg.80%29.aspx) extended property to **true**.</span></span> <span data-ttu-id="2f576-129">首先，[为属性创建扩展属性定义](properties-and-extended-properties-in-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="2f576-129">First, create an [extended property definition for the property](properties-and-extended-properties-in-ews-in-exchange.md).</span></span> <span data-ttu-id="2f576-130">接下来，使用[Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx)方法获取文件夹，然后将**PidTagAttributeHidden**属性的值更新为 True，并使用[update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx)方法保存所做的更改。</span><span class="sxs-lookup"><span data-stu-id="2f576-130">Next, use the [Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) method to get to the folder, then update the value of the **PidTagAttributeHidden** property to true, and use the [Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) method to save the changes.</span></span> 
  
<span data-ttu-id="2f576-131">本示例假定**服务**是邮箱所有者的有效[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象，该用户已通过 Exchange 服务器的身份验证，并且该**folderId**是一个有效的[Folder.Id](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.id%28v=exchg.80%29.aspx) ，用于标识要隐藏的文件夹。</span><span class="sxs-lookup"><span data-stu-id="2f576-131">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the mailbox owner, that the user has been authenticated to an Exchange server, and that **folderId** is a valid [Folder.Id](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.id%28v=exchg.80%29.aspx) that identifies the folder to hide.</span></span> 
  
```cs
private static void MakeHidden(FolderId folderId, ExchangeService service)
{
    // Create an extended property definition for the PidTagAttributeHidden property.
    ExtendedPropertyDefinition isHiddenProp = new ExtendedPropertyDefinition(0x10f4, MapiPropertyType.Boolean);
    PropertySet propSet = new PropertySet(isHiddenProp);
    // Bind to a folder and retrieve the PidTagAttributeHidden property.
    Folder folder = Folder.Bind(service, folderId, propSet);
    // Set the PidTagAttributeHidden property to true.
    folder.SetExtendedProperty(isHiddenProp, true);
    // Save the changes.
    folder.Update();
}
```

## <a name="hide-a-folder-by-using-ews"></a><span data-ttu-id="2f576-132">使用 EWS 隐藏文件夹</span><span class="sxs-lookup"><span data-stu-id="2f576-132">Hide a folder by using EWS</span></span>
<span data-ttu-id="2f576-133"><a name="bk_hideews"> </a></span><span class="sxs-lookup"><span data-stu-id="2f576-133"><a name="bk_hideews"> </a></span></span>

<span data-ttu-id="2f576-134">通过将[PidTagAttributeHidden](https://msdn.microsoft.com/library/cc433490%28v=exchg.80%29.aspx)扩展属性更改为**true**，可以使用 EWS[将现有文件夹设置](how-to-work-with-folders-by-using-ews-in-exchange.md#bk_createfolderewsma)为隐藏文件夹。</span><span class="sxs-lookup"><span data-stu-id="2f576-134">You can use EWS to [make an existing folder](how-to-work-with-folders-by-using-ews-in-exchange.md#bk_createfolderewsma) a hidden folder by changing the [PidTagAttributeHidden](https://msdn.microsoft.com/library/cc433490%28v=exchg.80%29.aspx) extended property to **true**.</span></span> <span data-ttu-id="2f576-135">首先，使用[GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx)操作获取文件夹，然后通过包含[ExtendedFieldURI](https://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx)元素并将**PropertyTag**值设置为4340，并将**recordtype**值设置为 Boolean，从而检索**PidTagAttributeHidden**属性。</span><span class="sxs-lookup"><span data-stu-id="2f576-135">First, use the [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) operation to get to the folder, then retrieve the **PidTagAttributeHidden** property by including the [ExtendedFieldURI](https://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx) element, and setting the **PropertyTag** value to 4340 and the **PropertyType** value to Boolean.</span></span> 
  
<span data-ttu-id="2f576-136">这也是当您使用**Bind**方法获取文件夹以[使其成为一个隐藏文件夹](#bk_hideewsma)之前，EWS 托管 API 发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="2f576-136">This is also the XML request that the EWS Managed API sends when you use the **Bind** method to get a folder before [making it a hidden folder](#bk_hideewsma).</span></span>
  
<span data-ttu-id="2f576-137">为提高可读性， [FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx)值将缩短。</span><span class="sxs-lookup"><span data-stu-id="2f576-137">The [FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) value is shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:GetFolder>
      <m:FolderShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:ExtendedFieldURI PropertyTag="4340"
                              PropertyType="Boolean" />
        </t:AdditionalProperties>
      </m:FolderShape>
      <m:FolderIds>
        <t:FolderId Id="IQywAAAA==" />
      </m:FolderIds>
    </m:GetFolder>
  </soap:Body>
</soap:Envelope>
```

服务器使用[GetFolderResponse](https://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx)邮件响应**GetFolder**请求，其中包含[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值为**NoError**，表示已成功检索该文件夹。 该响应还包括[ExtendedProperty](https://msdn.microsoft.com/library/f9701409-b620-4afe-b9ee-4c1e95507af7%28Office.15%29.aspx)的[值](https://msdn.microsoft.com/library/196278d4-5e77-4e0a-8af6-8ac065610510%28Office.15%29.aspx)。 <span data-ttu-id="2f576-140">在此示例中，将**值**设置为**false**，这意味着该文件夹当前不被隐藏。</span><span class="sxs-lookup"><span data-stu-id="2f576-140">In this example, the **Value** is set to **false**, which means that the folder is currently not hidden.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="898"
                         MinorBuildNumber="23"
                         Version="V2_10"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="IQywAAAA=="
                          ChangeKey="AQAAABYAAAD32nSTjepyT63rYH17n9THAAAAABED" />
              <t:ExtendedProperty>
                <t:ExtendedFieldURI PropertyTag="0x10f4"
                                    PropertyType="Boolean" />
                <t:Value>false</t:Value>
              </t:ExtendedProperty>
            </t:Folder>
          </m:Folders>
        </m:GetFolderResponseMessage>
      </m:ResponseMessages>
    </m:GetFolderResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="2f576-141">若要将**ExtendedProperty**的值更改为 true，请使用[UpdateFolder](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx)操作。</span><span class="sxs-lookup"><span data-stu-id="2f576-141">To change the value of the **ExtendedProperty** to true, use the [UpdateFolder](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="2f576-142">包含**PidTagAttributeHidden**扩展属性的**ExtendedProperty**、 **ExtendedFieldURI**和**Value**元素，并将**value**元素设置为**true**以隐藏该文件夹。</span><span class="sxs-lookup"><span data-stu-id="2f576-142">Include the **ExtendedProperty**, **ExtendedFieldURI**, and **Value** elements for the **PidTagAttributeHidden** extended property, and set the **Value** element to **true** to hide the folder.</span></span> 
  
<span data-ttu-id="2f576-143">这也是当您使用**update**方法更新文件夹以[使其成为一个隐藏文件夹](#bk_hideewsma)时，EWS 托管 API 发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="2f576-143">This is also the XML request that the EWS Managed API sends when you use the **Update** method to update a folder to [make it a hidden folder](#bk_hideewsma).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:UpdateFolder>
      <m:FolderChanges>
        <t:FolderChange>
          <t:FolderId Id="IQywAAAA=="
                      ChangeKey="AQAAABYAAAD32nSTjepyT63rYH17n9THAAAAABED" />
          <t:Updates>
            <t:SetFolderField>
              <t:ExtendedFieldURI PropertyTag="4340"
                                  PropertyType="Boolean" />
              <t:Folder>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="4340"
                                      PropertyType="Boolean" />
                  <t:Value>true</t:Value>
                </t:ExtendedProperty>
              </t:Folder>
            </t:SetFolderField>
          </t:Updates>
        </t:FolderChange>
      </m:FolderChanges>
    </m:UpdateFolder>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="2f576-144">服务器使用[UpdateFolderResponse](https://msdn.microsoft.com/library/31f47739-dc9c-46ba-9e3f-cce25dc85e6e%28Office.15%29.aspx)邮件响应**UpdateFolder**请求，其中包含[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值为**NoError**，这表示文件夹已成功更新，现在处于隐藏状态。</span><span class="sxs-lookup"><span data-stu-id="2f576-144">The server responds to the **UpdateFolder** request with an [UpdateFolderResponse](https://msdn.microsoft.com/library/31f47739-dc9c-46ba-9e3f-cce25dc85e6e%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the folder was updated successfully, and is now hidden.</span></span>
  
## <a name="find-all-hidden-folders-by-using-the-ews-managed-api"></a><span data-ttu-id="2f576-145">使用 EWS 托管 API 查找所有隐藏的文件夹</span><span class="sxs-lookup"><span data-stu-id="2f576-145">Find all hidden folders by using the EWS Managed API</span></span>
<span data-ttu-id="2f576-146"><a name="bk_findhiddenewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="2f576-146"><a name="bk_findhiddenewsma"> </a></span></span>

<span data-ttu-id="2f576-147">您可以通过为**PidTagAttributeHidden**扩展属性创建[扩展属性定义](properties-and-extended-properties-in-ews-in-exchange.md)，然后使用[FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)方法查找**PidTagAttributeHidden**值设置为**true**的文件夹，从而在父文件夹下查找所有隐藏的文件夹。</span><span class="sxs-lookup"><span data-stu-id="2f576-147">You can find all hidden folders under a parent folder by creating an [extended property definition](properties-and-extended-properties-in-ews-in-exchange.md) for the **PidTagAttributeHidden** extended property, and then using the [FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx) method to find folders with a **PidTagAttributeHidden** value that is set to **true**.</span></span> <span data-ttu-id="2f576-148">本示例使用 MsgFolderRoot （也称为信息存储区或 IPM 子树）作为父文件夹，以在其下搜索。</span><span class="sxs-lookup"><span data-stu-id="2f576-148">This example uses the MsgFolderRoot, also known as the Top of Information Store, or IPM Subtree, as the parent folder to search under.</span></span>
  
<span data-ttu-id="2f576-149">本示例假定**服务**是邮箱所有者的有效[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象，并且该用户已通过 Exchange 服务器的身份验证。</span><span class="sxs-lookup"><span data-stu-id="2f576-149">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the mailbox owner, and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
private static void FindHiddenFolders(ExchangeService service)
{
    // Create an extended property definition for the PidTagAttributeHidden property.
    ExtendedPropertyDefinition isHiddenProp = new ExtendedPropertyDefinition(0x10f4, MapiPropertyType.Boolean);
    // Create a folder view to retrieve up to 100 folders and 
    // retrieve only the PidTagAttributeHidden and the display name.
    FolderView folderView = new FolderView(100);
    folderView.PropertySet = new PropertySet(isHiddenProp, FolderSchema.DisplayName);
    // Indicate a Traversal value of Deep, so that all subfolders are retrieved.
    folderView.Traversal = FolderTraversal.Deep;
    // Find all hidden folders under the MsgFolderRoot.
    // This call results in a FindFolder call to EWS.
    FindFoldersResults findFolder = service.FindFolders(WellKnownFolderName.MsgFolderRoot,
            new SearchFilter.IsEqualTo(isHiddenProp, true), folderView);
    // Display the folder ID and display name of each hidden folder.
    foreach (Folder folder in findFolder)
    {
        Console.WriteLine("FolderId: {0}", folder.Id);
        Console.WriteLine("DisplayName: {0}", folder.DisplayName);
        Console.WriteLine("\r\n");
    }
}
```

## <a name="find-all-hidden-folders-by-using-ews"></a><span data-ttu-id="2f576-150">使用 EWS 查找所有隐藏的文件夹</span><span class="sxs-lookup"><span data-stu-id="2f576-150">Find all hidden folders by using EWS</span></span>
<span data-ttu-id="2f576-151"><a name="bk_findhiddenews"> </a></span><span class="sxs-lookup"><span data-stu-id="2f576-151"><a name="bk_findhiddenews"> </a></span></span>

<span data-ttu-id="2f576-152">您可以通过调用[FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)操作并搜索[PidTagAttributeHidden](https://msdn.microsoft.com/library/cc433490%28v=exchg.80%29.aspx)扩展属性设置为**true**的文件夹，来使用 EWS 查找现有文件夹下的所有隐藏文件夹。</span><span class="sxs-lookup"><span data-stu-id="2f576-152">You can use EWS to find all hidden folders under an existing folder by calling the [FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) operation and searching for folders whose [PidTagAttributeHidden](https://msdn.microsoft.com/library/cc433490%28v=exchg.80%29.aspx) extended property is set to **true**.</span></span> <span data-ttu-id="2f576-153">为此，请包括一个[IsEqualTo](https://msdn.microsoft.com/library/48e7e067-049c-4184-8026-071e6f558e8a%28Office.15%29.aspx)[限制](https://msdn.microsoft.com/library/77f19014-d112-4999-8e83-ecc32a117a73%28Office.15%29.aspx)，该限制将搜索**PidTagAttributeHidden**属性（ **PropertyTag**值为4243，将**recordtype**值为 Boolean）的[ExtendedFieldURI](https://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx)元素，如以下请求中所示。</span><span class="sxs-lookup"><span data-stu-id="2f576-153">To do this, include an [IsEqualTo](https://msdn.microsoft.com/library/48e7e067-049c-4184-8026-071e6f558e8a%28Office.15%29.aspx)[Restriction](https://msdn.microsoft.com/library/77f19014-d112-4999-8e83-ecc32a117a73%28Office.15%29.aspx) that searches for the [ExtendedFieldURI](https://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx) element for the **PidTagAttributeHidden** property ( **PropertyTag** value to 4243 and the **PropertyType** value to Boolean), as shown in the following request.</span></span> <span data-ttu-id="2f576-154">本示例使用 MsgFolderRoot （也称为信息存储区或 IPM 子树）作为父文件夹，以在其下搜索。</span><span class="sxs-lookup"><span data-stu-id="2f576-154">This example uses the MsgFolderRoot, also known as the Top of Information Store, or IPM Subtree, as the parent folder to search under.</span></span> 
  
<span data-ttu-id="2f576-155">这也是在使用**FindFolders**方法[查找所有隐藏文件夹](#bk_findhiddenewsma)时，EWS 托管 API 发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="2f576-155">This is also the XML request that the EWS Managed API sends when you use the **FindFolders** method to [find all hidden folders](#bk_findhiddenewsma).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Central Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:FindFolder Traversal="Deep">
      <m:FolderShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:ExtendedFieldURI PropertyTag="4340"
                              PropertyType="Boolean" />
          <t:FieldURI FieldURI="folder:DisplayName" />
        </t:AdditionalProperties>
      </m:FolderShape>
      <m:IndexedPageFolderView MaxEntriesReturned="100"
                               Offset="0"
                               BasePoint="Beginning" />
      <m:Restriction>
        <t:IsEqualTo>
          <t:ExtendedFieldURI PropertyTag="4340"
                              PropertyType="Boolean" />
          <t:FieldURIOrConstant>
            <t:Constant Value="true" />
          </t:FieldURIOrConstant>
        </t:IsEqualTo>
      </m:Restriction>
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="msgfolderroot" />
      </m:ParentFolderIds>
    </m:FindFolder>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="2f576-156">服务器使用[FindFolderResponse](https://msdn.microsoft.com/library/f5dd813c-9698-4a39-8fca-3a825df365ed%28Office.15%29.aspx)邮件响应**FindFolder**请求，其中包含[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值**NoError**，这表示文件夹搜索成功，以及根邮件文件夹下的所有隐藏文件夹。</span><span class="sxs-lookup"><span data-stu-id="2f576-156">The server responds to the **FindFolder** request with a [FindFolderResponse](https://msdn.microsoft.com/library/f5dd813c-9698-4a39-8fca-3a825df365ed%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the folder search was successful, as well as all the hidden folders under the root message folder.</span></span>
  
<span data-ttu-id="2f576-157">为提高可读性， [FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx)值将缩短。</span><span class="sxs-lookup"><span data-stu-id="2f576-157">The [FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) values are shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="898"
                         MinorBuildNumber="23"
                         Version="V2_10"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="6"
                        TotalItemsInView="6"
                        IncludesLastItemInRange="true">
            <t:Folders>
              <t:ContactsFolder>
                <t:FolderId Id="IBHgAAAA=="
                            ChangeKey="AwAAABYAAAD32nSTjepyT63rYH17n9THAAAAAACz" />
                <t:DisplayName>{06967759-274D-40B2-A3EB-D7F9E73727D7}</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x10f4"
                                      PropertyType="Boolean" />
                  <t:Value>true</t:Value>
                </t:ExtendedProperty>
              </t:ContactsFolder>
              <t:ContactsFolder>
                <t:FolderId Id="IBHwAAAA=="
                            ChangeKey="AwAAABYAAAD32nSTjepyT63rYH17n9THAAAAAAC7" />
                <t:DisplayName>{A9E2BC46-B3A0-4243-B315-60D991004455}</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x10f4"
                                      PropertyType="Boolean" />
                  <t:Value>true</t:Value>
                </t:ExtendedProperty>
              </t:ContactsFolder>
              <t:ContactsFolder>
                <t:FolderId Id="IBIQAAAA=="
                            ChangeKey="AwAAABYAAAD32nSTjepyT63rYH17n9THAAAAAADO" />
                <t:DisplayName>GAL Contacts</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x10f4"
                                      PropertyType="Boolean" />
                  <t:Value>true</t:Value>
                </t:ExtendedProperty>
              </t:ContactsFolder>
              <t:ContactsFolder>
                <t:FolderId Id="IBHQAAAA=="
                            ChangeKey="AwAAABYAAAD32nSTjepyT63rYH17n9THAAAAAACa" />
                <t:DisplayName>Recipient Cache</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x10f4"
                                      PropertyType="Boolean" />
                  <t:Value>true</t:Value>
                </t:ExtendedProperty>
              </t:ContactsFolder>
              <t:Folder>
                <t:FolderId Id="HAAAAA=="
                            ChangeKey="AQAAABYAAAD32nSTjepyT63rYH17n9THAAAAAACS" />
                <t:DisplayName>Conversation Action Settings</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x10f4"
                                      PropertyType="Boolean" />
                  <t:Value>true</t:Value>
                </t:ExtendedProperty>
              </t:Folder>
              <t:Folder>
                <t:FolderId Id="IQywAAAA=="
                            ChangeKey="AQAAABYAAAD32nSTjepyT63rYH17n9THAAAeZIBf" />
                <t:DisplayName>TestFolder</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x10f4"
                                      PropertyType="Boolean" />
                  <t:Value>true</t:Value>
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

## 
<span data-ttu-id="2f576-158"><a name="bk_findhiddenews"> </a></span><span class="sxs-lookup"><span data-stu-id="2f576-158"><a name="bk_findhiddenews"> </a></span></span>

<span data-ttu-id="2f576-159">隐藏或隐藏文件夹后，可能需要获取文件夹层次结构或[同步文件夹层次结构](how-to-synchronize-folders-by-using-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="2f576-159">After you have hidden or unhidden folders, you might want to get the folder hierarchy or [synchronize the folder hierarchy](how-to-synchronize-folders-by-using-ews-in-exchange.md).</span></span> <span data-ttu-id="2f576-160">演示如何通过[使用 Ews 托管 API](how-to-work-with-folders-by-using-ews-in-exchange.md#bk_getfolderhierarchyewsma)或[通过使用 ews 获取文件夹层次结构](how-to-work-with-folders-by-using-ews-in-exchange.md#bk_getfolderhierarchyews)来获取文件夹层次结构的示例还指示层次结构中的哪些文件夹是隐藏的。</span><span class="sxs-lookup"><span data-stu-id="2f576-160">The examples that show you how to [get a folder hierarchy by using the EWS Managed API](how-to-work-with-folders-by-using-ews-in-exchange.md#bk_getfolderhierarchyewsma) or [get a folder hierarchy by using EWS](how-to-work-with-folders-by-using-ews-in-exchange.md#bk_getfolderhierarchyews) also indicate which folders in the hierarchy are hidden.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2f576-161">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2f576-161">See also</span></span>


- [<span data-ttu-id="2f576-162">Exchange 中的 EWS 中的文件夹和项目</span><span class="sxs-lookup"><span data-stu-id="2f576-162">Folders and items in EWS in Exchange</span></span>](folders-and-items-in-ews-in-exchange.md)
    
- [<span data-ttu-id="2f576-163">使用 Exchange 中的 EWS 处理文件夹</span><span class="sxs-lookup"><span data-stu-id="2f576-163">Work with folders by using EWS in Exchange</span></span>](how-to-work-with-folders-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="2f576-164">使用 Exchange 中的 EWS 处理搜索文件夹</span><span class="sxs-lookup"><span data-stu-id="2f576-164">Work with search folders by using EWS in Exchange</span></span>](how-to-work-with-search-folders-by-using-ews-in-exchange.md)
    

