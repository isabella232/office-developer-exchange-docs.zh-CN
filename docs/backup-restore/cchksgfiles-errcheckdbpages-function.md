---
title: CChkSGFiles.ErrCheckDbPages 函数
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ErrCheckDbPages
api_type:
- dllExport
ms.assetid: 5e981a7c-28cd-470c-b7eb-606463e9dd05
description: 上次修改时间：2013 年 2 月 22 日
ms.openlocfilehash: e458e4ad552abfebb7611822a6e756bdd2ac6350
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510405"
---
# <a name="cchksgfileserrcheckdbpages-function"></a>CChkSGFiles.ErrCheckDbPages 函数

**适用于：Exchange Server** 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013 年
  
验证指定数据库中的一系列页面。 
  
```cs
Vitual ERRErrCheckDbPages  
(
    Const ULONGiDb,
    Const VOID  * const pvPageBuffer,
    Const ULONGcbPageBuffer,
    PAGE_INFOrgPageInfo[],
    Const ULONGcPageInfo,
    Const ULONGulFlags = NO_FLAGS
);

```

## <a name="parameters"></a>参数

### <a name="idb"></a>iDb
  
输入参数。 ErrInit 函数 **的 rgwszDb[]** 参数中指定的数据库 **数组的** 索引。 将检查通过此参数编制索引的数据库。 
    
### <a name="pvpagebuffer"></a>pvPageBuffer 
  
输入参数。 指向包含要检查的一个或多个数据库页的缓冲区的指针。 缓冲区的大小必须是数据库页面大小的倍数，由 **ErrCheckDbHeaders** 函数在 **dbPageSize** 参数中返回。 调用应用程序在调用 **ErrCheckDbPages** 之前，必须使用数据库页面内容填充缓冲区。
    
### <a name="cbpagebuffer"></a>cbPageBuffer
  
输入参数。 **pvPageBuffer** 参数的大小（以字节为单位）。 此值必须是数据库页面大小的倍数，由 **ErrCheckDbHeaders** 函数在 **dbPageSize** 参数中返回。 
    
### <a name="rgpageinfo"></a>rgPageInfo[] 
  
输入/输出参数。 **ErrCheckDbPages** 用所检查的每个数据库页的详细结果填充的一组 **PAGE \_ INFO** 结构。 对于 **在 pvPageBuffer** 参数中传递的每个数据库页，数组必须具有一个元素，并且每个 **PAGE \_ INFO** 结构中的 **ulPgno** 字段必须设置为与数据库页对应的逻辑页码。 有关详细信息，请参阅本主题稍后介绍的"备注"。 
    
### <a name="cpageinfo"></a>cPageInfo
  
输入参数。 **rgPageInfo[]** 数组中的条目数。 此值必须等于 **pvPageBuffer** 参数中传递的数据库页数。 
    
### <a name="ulflags"></a>ulFlags 
  
可选输入参数。 保留此值以供将来使用。 此参数中传递的值应为 0， (0) 。
    
## <a name="return-value"></a>返回值

ERR [枚举中的错误](cchksgfiles-err-enumeration.md) 代码。 
  
## <a name="remarks"></a>注解

请注意，您需要在传递给 **ErrInit** 函数的数据库数组中指定数据库。 此外，**必须在 ErrCheckDbPages 之前调用 ErrCheckDbHeaders。** 
  
调用应用程序必须分配一个足够大的内存缓冲区，以容纳要检查的数据库页面。 应用程序负责使用一个或多个此类数据库页的内容填充缓冲区。 
  
调用应用程序必须在调用 **ErrCheckDbPages 之前调用 ErrCheckDbHeaders。**  可以在必要时多次调用此函数，以覆盖要检查的所有数据库文件的所有页面。
  
在 **rgPageInfo[]** 参数中，返回的每个元素都包含有关 **PAGE \_ INFO** 结构中数据库页的信息。 如果 **ErrCheckDbPages** 函数返回错误，应用程序应检查每个 **PAGE \_ INFO** 结构以确定在哪个页面上找到错误。 例如，比较 **checksumActual** 和 **checksumExpected** 值将指示是否在该数据库页上检测到校验和错误。 
  
如果 **ErrCheckDbPages** 检测到数据库内容中出现任何错误，它将创建一Windows错误事件日志条目。 
  
**CChkSGFiles** 对象确定是否实际检查了使用 **ErrInit** 函数注册的所有数据库。 具体而言 **，CChkSGFiles** 使用 **ErrCheckDbPages** 函数确定是否实际验证 **了 ErrCheckDbHeaders** 指示的相同数量的数据库页。 如果未成功检查每个数据库中的正确页数， **则 ErrTerm** 函数将返回错误。 
  
如果在多线程应用程序中使用 CHKSGFILES，可以在应用程序的多线程部分调用 **ErrCheckDbPages** 函数。 请注意，对于检查的每个数据库，通常调用 **ErrCheckDbPages** 多次。 
  
## <a name="requirements"></a>Requirements

Exchange 2013 仅包括 64 位版本的 CHKSGFILES API。
  
运行应用程序的帐户必须具有对要检查的数据库和日志文件的读取权限。
  

