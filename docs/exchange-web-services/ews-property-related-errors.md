---
title: EWS 与属性相关的错误
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1c4c5969-7bdd-4021-be0e-cae99e86cf2c
description: 了解如何处理属性相关 EWS 应用程序中的错误。
ms.openlocfilehash: f214ab40c3717178c6957a9da93bdf89999fc1d3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19752718"
---
# <a name="ews-property-related-errors"></a>EWS 与属性相关的错误

本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 了解如何处理属性相关 EWS 应用程序中的错误。
  
大多数 EWS 客户端应用程序使用属性，这意味着需要处理与属性相关的错误。您可以处理这些错误在运行时，或者开发 EWS 应用程序时。
  
**表 1: 与属性相关的错误和如何处理它们**

|**错误**|**由尝试...**|**处理它的...**|
|:-----|:-----|:-----|
|ErrorDataSizeLimitExceeded  <br/> |超过最大大小属性的值与属性设置或属性不支持流中，例如，文件夹属性。  <br/> |限制的数据大小的属性上设置。  <br/> |
|ErrorFolderPropertRequestFailed  <br/> |获取无法检索属性。  <br/> |指示不能检索该属性。  <br/> |
|ErrorInvalidExtendedProperty  <br/> |无效的扩展属性统一资源标识符 (URI) 中设置了无效的扩展的属性值或结果组合。  <br/> |正在检查扩展的属性的值。  <br/> |
|ErrorInvalidExtendedPropertyValue  <br/> |设置扩展的属性的值与指定的类型不匹配  <br/> |更新代码以检查有匹配的类型。  <br/> |
|ErrorInvalidFolderId  <br/> |设置为无效的表单的文件夹标识符的结构。  <br/> |仅使用标识符按 EWS 中返回。  <br/> |
|ErrorInvalidId  <br/> |设置标识符的结构和/或变为无效的表单密钥。  <br/> |仅使用标识符按 EWS 中返回。  <br/> |
|ErrorInvalidIdEmpty  <br/> |设置一个空的标识符。  <br/> |设置有效的项或文件夹标识符。  <br/> |
|ErrorInvalidIdMalformed  <br/> |设置标识符的结构和/或变为无效的表单密钥。  <br/> |仅使用标识符按 EWS 中返回。  <br/> |
|ErrorInvalidPropertyAppend  <br/> |将附加属性不支持追加。  <br/> |更新您的代码以便它只能尝试将追加值对收件人集合属性 (收件人、 抄送、 密件抄送)，与会者集合属性 (必填，可选的资源)，Body 属性和回复属性。  <br/> |
|ErrorInvalidPropertyDelete  <br/> |删除属性不支持删除。  <br/> |正在更新您的代码尝试删除该属性。例如，不能删除该文件夹和项的标识符。  <br/> |
|ErrorInvalidPropertyForExists  <br/> |在基于标志的属性上设置 existential 基于的搜索限制。  <br/> |更新代码以 existential 基于的搜索限制在使用基于标记的属性。基于标记的属性是 IsDraft、 IsSubmitted、 IsUnmodified、 IsResend 和 IsFromMe。  <br/> |
|ErrorInvalidPropertyForOperation  <br/> |作用于项目或文件夹，该操作不支持的属性。  <br/> |更新代码以访问属性的操作导致错误。  <br/> |
|ErrorInvalidPropertyRequest  <br/> |指定的项目类型不支持该请求中的属性。  <br/> |正在更新您的代码尝试访问的属性和操作。  <br/> |
|ErrorInvalidPropertySet  <br/> |设置只读属性。  <br/> |正在更新您的代码尝试设置该属性。  <br/> |
|ErrorInvalidValueForProperty  <br/> |搜索限制不匹配的属性类型比较值中的属性值进行比较。  <br/> |更新代码以检查属性类型不匹配。  <br/> |
|ErrorItemSavePropertyError  <br/> |无效的属性值保存项或文件夹。  <br/> |在提交请求之前检查属性值和类型。  <br/> |
|ErrorNoFolderClassOverride  <br/> |对新文件夹不是基文件夹类型设置文件夹类。  <br/> |使用一般文件夹类型设置文件夹类。  <br/> |
|ErrorNoPropertyTagForCustomProperties  <br/> |根据属性标记引用的自定义扩展的属性。  <br/> |更新代码以引用自定义扩展属性的属性集标识符和属性名称或属性的调度标识符。  <br/> |
|ErrorObjectTypeChanged  <br/> |设置或更新的架构类型不匹配的项的项类。  <br/> |更新您的代码，以使项目类匹配项的架构类型。  <br/> |
|ErrorPropertyUpdate  <br/> |更新属性具有无效的属性值。  <br/> |在[UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)请求中提交它之前检查该属性值。  <br/> |
|ErrorRequiredPropertyMissing  <br/> |发送 CreateAttachment 请求中缺少必需的属性。  <br/> |更新代码以将缺少的属性设置为指定的响应中返回的属性路径。  <br/> |
|ErrorUnsupportedMapiPropertyType  <br/> |使用扩展的属性类型的类型对象、 对象数组、 错误或 null。  <br/> |更新代码以使用受限制的扩展的属性类型。  <br/> |
|ErrorUnsupportedPathForQuery  <br/> |搜索限制中使用了不支持的属性的路径。  <br/> |更改搜索限制，以排除不受支持的属性路径。  <br/> |
|ErrorUnsupportedPathForSortGroup  <br/> |排序或分组搜索请求中使用了不支持的属性的路径。  <br/> |更改搜索限制，以排除不受支持的属性路径。  <br/> |
|ErrorUnsupportedTypeForConversion  <br/> |请求的属性类型不能转换为 EWS 响应中返回的 XML。  <br/> |更新代码以请求不受支持的属性。  <br/> |
|ErrorUpdatePropertyMismatch  <br/> |更新的项或文件夹的更改说明与指定为要更新的属性不匹配。  <br/> |更改您的代码以更改说明匹配的项或文件夹的类型，正在被更新的。  <br/> |
   
## <a name="see-also"></a>另请参阅


- [属性和交换中的 EWS 中的扩展的属性](properties-and-extended-properties-in-ews-in-exchange.md)
    
- [Start using web services in Exchange](start-using-web-services-in-exchange.md)
    
- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)
    

