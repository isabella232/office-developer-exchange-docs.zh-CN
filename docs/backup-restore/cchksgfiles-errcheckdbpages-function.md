---
title: CChkSGFiles.ErrCheckDbPages 函数
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ErrCheckDbPages
api_type:
- dllExport
ms.assetid: 5e981a7c-28cd-470c-b7eb-606463e9dd05
description: 上次修改时间： 2013 年 2 月 22 日
ms.openlocfilehash: f1588b1dbc4bd7e83683fa4432a175405ad17903
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752687"
---
# <a name="cchksgfileserrcheckdbpages-function"></a>CChkSGFiles.ErrCheckDbPages 函数

**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013
  
验证指定的数据库中的页面范围。 
  
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
  
输入的参数。 **ErrInit**函数**rgwszDb []** 参数中指定的数据库的数组中的索引。 此参数所编制索引的数据库将被选中。 
    
### <a name="pvpagebuffer"></a>pvPageBuffer 
  
输入的参数。 指向包含要检查的一个或多个数据库页的缓冲区的指针。 缓冲区的大小必须是数据库页面大小的倍数，如**ErrCheckDbHeaders**函数返回**pcbDbPageSize**参数中。 调用应用程序必须调用**ErrCheckDbPages**之前填充数据库页面内容的缓冲区。
    
### <a name="cbpagebuffer"></a>cbPageBuffer
  
输入的参数。 **PvPageBuffer**参数，以字节为单位的大小。 由**ErrCheckDbHeaders**函数返回**pcbDbPageSize**参数中，此值必须是数据库页面大小的倍数。 
    
### <a name="rgpageinfo"></a>rgPageInfo] 
  
输入/输出参数。 数组**页\_INFO** **ErrCheckDbPages**填入的结构详细进行检查每个数据库页的结果。 该数组必须具有一个元素传递**pvPageBuffer**参数和中每**ulPgno**字段中每个数据库页**页\_INFO**结构必须设置为逻辑页码对应于数据库页。 有关详细信息，请参阅本主题后面的"备注"。 
    
### <a name="cpageinfo"></a>cPageInfo
  
输入的参数。 **RgPageInfo []** 数组中的条目数。 该值必须等于**pvPageBuffer**参数中传递的数据库页面的数量。 
    
### <a name="ulflags"></a>ulFlags 
  
可选的输入的参数。 此值保留以供将来使用。 此参数中传递的值应为 0 （零）。
    
## <a name="return-value"></a>返回值

从[ERR](cchksgfiles-err-enumeration.md)枚举错误代码。 
  
## <a name="remarks"></a>注解

请注意，您需要指定数据库的数据库传递给**ErrInit**函数数组中。 此外，必须在**ErrCheckDbPages**之前调用**ErrCheckDbHeaders** 。
  
调用应用程序必须分配内存缓冲区的足以容纳要检查的数据库页面。 应用程序负责为一个或多个此类数据库页的内容填充缓冲区。 
  
调用应用程序必须调用**ErrCheckDbPages**之前调用**ErrCheckDbHeaders** 。 可以根据需要以覆盖要检查的所有数据库文件中的所有页面多次调用此函数。
  
在**rgPageInfo []** 参数中，返回每个元素包含有关在数据库页的信息**页\_INFO**结构。 如果**ErrCheckDbPages**函数将返回错误，应用程序应检查每个**页\_INFO**结构以确定哪一页上找到错误。 例如，比较**checksumActual**和**checksumExpected**值将指示是否已在该数据库页上检测到的校验和错误。 
  
如果**ErrCheckDbPages**检测到数据库内容中的任何错误，其将创建一个 Windows 错误事件日志条目。 
  
**CChkSGFiles**对象确定是否已实际签**ErrInit**函数注册的所有数据库。 具体而言， **CChkSGFiles**使用**ErrCheckDbPages**函数来确定是否相同数量的数据库页由**ErrCheckDbHeaders**实际已验证。 如果未成功签正确的每个数据库中的页面数，则**ErrTerm**函数将返回错误。 
  
如果您使用 CHKSGFILES 多线程应用程序中，您可以在应用程序的多线程部分调用**ErrCheckDbPages**函数。 请注意**ErrCheckDbPages**通常会调用多次进行检查的每个数据库。 
  
## <a name="requirements"></a>要求

Exchange 2013 只包括 CHKSGFILES API 的 64 位版本。
  
下运行该应用程序的帐户必须具有读取权限要检查的数据库和日志文件。
  

