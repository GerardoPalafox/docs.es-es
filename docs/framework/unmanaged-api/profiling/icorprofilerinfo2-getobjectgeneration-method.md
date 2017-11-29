---
title: "ICorProfilerInfo2::GetObjectGeneration (Método)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerInfo2.GetObjectGeneration
api_location: mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerInfo2::GetObjectGeneration
helpviewer_keywords:
- GetObjectGeneration method [.NET Framework profiling]
- ICorProfilerInfo2::GetObjectGeneration method [.NET Framework profiling]
ms.assetid: b0d25f76-0bd5-4aa6-96cf-bfec0e1de28b
topic_type: apiref
caps.latest.revision: "12"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: e90139f96638dbb1a183f98e754838ff52424fc9
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="icorprofilerinfo2getobjectgeneration-method"></a><span data-ttu-id="60b77-102">ICorProfilerInfo2::GetObjectGeneration (Método)</span><span class="sxs-lookup"><span data-stu-id="60b77-102">ICorProfilerInfo2::GetObjectGeneration Method</span></span>
<span data-ttu-id="60b77-103">Obtiene el segmento del montón que contiene el objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="60b77-103">Gets the segment of the heap that contains the specified object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="60b77-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="60b77-104">Syntax</span></span>  
  
```  
HRESULT GetObjectGeneration(  
    [in] ObjectID objectId,  
    [out] COR_PRF_GC_GENERATION_RANGE *range);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="60b77-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="60b77-105">Parameters</span></span>  
 `objectId`  
 <span data-ttu-id="60b77-106">[in] El identificador del objeto.</span><span class="sxs-lookup"><span data-stu-id="60b77-106">[in] The ID of the object.</span></span>  
  
 `range`  
 <span data-ttu-id="60b77-107">[out] Un puntero a un [COR_PRF_GC_GENERATION_RANGE](../../../../docs/framework/unmanaged-api/profiling/cor-prf-gc-generation-range-structure.md) estructura que describe un intervalo (es decir, un bloque) de memoria en la generación que se está sometiendo a la recolección de elementos.</span><span class="sxs-lookup"><span data-stu-id="60b77-107">[out] A pointer to a [COR_PRF_GC_GENERATION_RANGE](../../../../docs/framework/unmanaged-api/profiling/cor-prf-gc-generation-range-structure.md) structure, which describes a range (that is, a block) of memory within the generation that is undergoing garbage collection.</span></span> <span data-ttu-id="60b77-108">Este intervalo contiene el objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="60b77-108">This range contains the specified object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="60b77-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="60b77-109">Remarks</span></span>  
 <span data-ttu-id="60b77-110">La `GetObjectGeneration` puede llamar al método desde cualquier devolución de llamada del generador de perfiles, siempre que la recolección de elementos no utilizados no está en curso.</span><span class="sxs-lookup"><span data-stu-id="60b77-110">The `GetObjectGeneration` method may be called from any profiler callback, provided that garbage collection is not in progress.</span></span> <span data-ttu-id="60b77-111">Es decir, pueden llamarse desde cualquier devolución de llamada excepto las que se producen entre [ICorProfilerCallback2:: GarbageCollectionStarted](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-garbagecollectionstarted-method.md) y [ICorProfilerCallback2:: GarbageCollectionFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-garbagecollectionfinished-method.md).</span><span class="sxs-lookup"><span data-stu-id="60b77-111">That is, it may be called from any callback except those that occur between [ICorProfilerCallback2::GarbageCollectionStarted](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-garbagecollectionstarted-method.md) and [ICorProfilerCallback2::GarbageCollectionFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-garbagecollectionfinished-method.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="60b77-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60b77-112">Requirements</span></span>  
 <span data-ttu-id="60b77-113">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="60b77-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="60b77-114">**Encabezado:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="60b77-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="60b77-115">**Biblioteca:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="60b77-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="60b77-116">**Versiones de .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="60b77-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="60b77-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="60b77-117">See Also</span></span>  
 [<span data-ttu-id="60b77-118">ICorProfilerInfo (interfaz)</span><span class="sxs-lookup"><span data-stu-id="60b77-118">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)  
 [<span data-ttu-id="60b77-119">ICorProfilerInfo2 (interfaz)</span><span class="sxs-lookup"><span data-stu-id="60b77-119">ICorProfilerInfo2 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-interface.md)