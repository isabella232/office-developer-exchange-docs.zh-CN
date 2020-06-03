---
title: CChkSGFiles 函数
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
description: 上次修改时间：2013年2月22日
ms.openlocfilehash: 78d2dbee6253096d597b4ec2de3878f40ee1b6d7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526723"
---
# <a name="cchksgfileserrcheckdbpages-function"></a>CChkSGFiles 函数

**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013
  
验证指定数据库中的页面范围。 
  
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

### <a name="idb"></a>.Idb
  
输入参数。 指向**ErrInit**函数的**rgwszDb []** 参数中指定的数据库数组的索引。 将检查通过此参数编制索引的数据库。 
    
### <a name="pvpagebuffer"></a>pvPageBuffer 
  
输入参数。 指向包含要检查的一个或多个数据库页面的缓冲区的指针。 缓冲区的大小必须是数据库页面大小的倍数，与**ErrCheckDbHeaders**函数在**pcbDbPageSize**参数中返回的大小相同。 调用**ErrCheckDbPages**之前，调用应用程序必须填充数据库页面内容的缓冲区。
    
### <a name="cbpagebuffer"></a>cbPageBuffer
  
输入参数。 **PvPageBuffer**参数的大小（以字节为单位）。 此值必须是数据库页面大小的倍数，与**ErrCheckDbHeaders**函数在**pcbDbPageSize**参数中返回的大小相同。 
    
### <a name="rgpageinfo"></a>rgPageInfo[] 
  
输入/输出参数。 **ErrCheckDbPages**使用所检查的每个数据库页面的详细结果填充的**页面 \_ 信息**结构的数组。 对于在**pvPageBuffer**参数中传递的每个数据库页面，该数组必须具有一个元素，并且每个**页面 \_ 信息**结构中的**ulPgno**字段必须设置为与数据库页面相对应的逻辑页面编号。 有关详细信息，请参阅本主题后面的 "备注"。 
    
### <a name="cpageinfo"></a>cPageInfo
  
输入参数。 **RgPageInfo []** 数组中的条目数。 此值必须等于在**pvPageBuffer**参数中传递的数据库页面的数目。 
    
### <a name="ulflags"></a>ulFlags 
  
可选的输入参数。 保留此值以供将来使用。 此参数中传递的值应为0（零）。
    
## <a name="return-value"></a>返回值

[ERR](cchksgfiles-err-enumeration.md)枚举中的错误代码。 
  
## <a name="remarks"></a>备注

请注意，您需要在传递给**ErrInit**函数的数据库数组中指定数据库。 此外，还必须在**ErrCheckDbPages**之前调用**ErrCheckDbHeaders** 。
  
调用应用程序必须分配足够大的内存缓冲区，以容纳要检查的数据库页。 应用程序负责使用一个或多个此类数据库页的内容填充缓冲区。 
  
调用应用程序必须先调用**ErrCheckDbHeaders** ，然后才能调用**ErrCheckDbPages**。 可以根据需要多次调用此函数，以涵盖要检查的所有数据库文件中的所有页面。
  
在**rgPageInfo []** 参数中，返回的每个元素都包含有关**页面 \_ 信息**结构中的数据库页面的信息。 如果**ErrCheckDbPages**函数返回一个错误，则应用程序应检查每个**页面 \_ 信息**结构以确定在哪个页面上发现了错误。 例如，比较**checksumActual**和**checksumExpected**值将指示是否在该数据库页上检测到校验和错误。 
  
如果**ErrCheckDbPages**检测到数据库内容中的任何错误，它将创建一个 Windows 错误事件日志条目。 
  
**CChkSGFiles**对象确定是否实际检查了使用**ErrInit**函数注册的所有数据库。 具体来说， **CChkSGFiles**使用**ErrCheckDbPages**函数来确定是否实际验证**ErrCheckDbHeaders**指示的相同数量的数据库页面。 如果未成功检查每个数据库中的正确数量的页面， **ErrTerm**函数将返回一个错误。 
  
如果要在多线程应用程序中使用 CHKSGFILES，则可以在应用程序的多线程部分调用**ErrCheckDbPages**函数。 请注意，对于所检查的每个数据库， **ErrCheckDbPages**通常被多次调用。 
  
## <a name="requirements"></a>Requirements

Exchange 2013 仅包含64位版本的 CHKSGFILES API。
  
运行应用程序所使用的帐户必须具有对要检查的数据库和日志文件的读取权限。
  

