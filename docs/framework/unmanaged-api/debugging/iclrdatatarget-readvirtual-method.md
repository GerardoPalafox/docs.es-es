---
title: "ICLRDataTarget::ReadVirtual (Método)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICLRDataTarget.ReadVirtual
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICLRDataTarget::ReadVirtual
helpviewer_keywords:
- ReadVirtual method, ICLRDataTarget interface [.NET Framework debugging]
- ICLRDataTarget::ReadVirtual method [.NET Framework debugging]
ms.assetid: da3769eb-1828-4aa1-b9ed-db4842136a43
topic_type: apiref
caps.latest.revision: "11"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: dffe95b1bab3d8dae72cc62f5d45baa85e39e590
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/18/2017
---
# <a name="iclrdatatargetreadvirtual-method"></a><span data-ttu-id="94c09-102">ICLRDataTarget::ReadVirtual (Método)</span><span class="sxs-lookup"><span data-stu-id="94c09-102">ICLRDataTarget::ReadVirtual Method</span></span>
<span data-ttu-id="94c09-103">Lee datos de la dirección de memoria virtual especificada en el búfer especificado.</span><span class="sxs-lookup"><span data-stu-id="94c09-103">Reads data from the specified virtual memory address into the specified buffer.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="94c09-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="94c09-104">Syntax</span></span>  
  
```  
HRESULT ReadVirtual (  
    [in] CLRDATA_ADDRESS    address,  
    [out, size_is(bytesRequested), length_is(*bytesRead)]   
        BYTE                *buffer,  
    [in] ULONG32            bytesRequested,  
    [out] ULONG32           *bytesRead  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="94c09-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="94c09-105">Parameters</span></span>  
 `address`  
 <span data-ttu-id="94c09-106">[in] CLRDATA_ADDRESS que almacena la dirección de memoria virtual.</span><span class="sxs-lookup"><span data-stu-id="94c09-106">[in] A CLRDATA_ADDRESS that stores the virtual memory address.</span></span>  
  
 `buffer`  
 <span data-ttu-id="94c09-107">[out] Un puntero a un búfer que recibe los datos.</span><span class="sxs-lookup"><span data-stu-id="94c09-107">[out] A pointer to a buffer that receives the data.</span></span>  
  
 `bytesRequested`  
 <span data-ttu-id="94c09-108">[in] La longitud del búfer.</span><span class="sxs-lookup"><span data-stu-id="94c09-108">[in] The length of the buffer.</span></span>  
  
 `bytesRead`  
 <span data-ttu-id="94c09-109">[out] Devuelve un puntero al número de bytes.</span><span class="sxs-lookup"><span data-stu-id="94c09-109">[out] A pointer to the number of bytes returned.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="94c09-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94c09-110">Requirements</span></span>  
 <span data-ttu-id="94c09-111">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="94c09-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="94c09-112">**Encabezado:** ClrData.idl, ClrData.h</span><span class="sxs-lookup"><span data-stu-id="94c09-112">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="94c09-113">**Biblioteca:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="94c09-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="94c09-114">**Versiones de .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="94c09-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="94c09-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="94c09-115">See Also</span></span>  
 [<span data-ttu-id="94c09-116">ICLRDataTarget (interfaz)</span><span class="sxs-lookup"><span data-stu-id="94c09-116">ICLRDataTarget Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-interface.md)