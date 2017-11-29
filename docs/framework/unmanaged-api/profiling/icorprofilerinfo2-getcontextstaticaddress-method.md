---
title: "ICorProfilerInfo2::GetContextStaticAddress (Método)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerInfo2.GetContextStaticAddress
api_location: mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerInfo2::GetContextStaticAddress
helpviewer_keywords:
- GetContextStaticAddress method [.NET Framework profiling]
- ICorProfilerInfo2::GetContextStaticAddress method [.NET Framework profiling]
ms.assetid: 2b374116-0972-416a-8cf5-79213129be9a
topic_type: apiref
caps.latest.revision: "23"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 2d206ca90b2d89ead67f419f0f4511d19d8ce110
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="icorprofilerinfo2getcontextstaticaddress-method"></a><span data-ttu-id="70373-102">ICorProfilerInfo2::GetContextStaticAddress (Método)</span><span class="sxs-lookup"><span data-stu-id="70373-102">ICorProfilerInfo2::GetContextStaticAddress Method</span></span>
<span data-ttu-id="70373-103">Obtiene la dirección del campo estático de contexto especificado que está en el ámbito del contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="70373-103">Gets the address for the specified context-static field that is in the scope of the specified context.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="70373-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="70373-104">Syntax</span></span>  
  
```  
HRESULT GetContextStaticAddress(  
    [in] ClassID classId,  
    [in] mdFieldDef fieldToken,  
    [in] ContextID contextId,  
    [out] void **ppAddress);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="70373-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="70373-105">Parameters</span></span>  
 `classId`  
 <span data-ttu-id="70373-106">[in] El identificador de la clase que contiene el campo estático de contexto solicitado.</span><span class="sxs-lookup"><span data-stu-id="70373-106">[in] The ID of the class that contains the requested context-static field.</span></span>  
  
 `fieldToken`  
 <span data-ttu-id="70373-107">[in] El token de metadatos para el campo estático de contexto solicitado.</span><span class="sxs-lookup"><span data-stu-id="70373-107">[in] The metadata token for the requested context-static field.</span></span>  
  
 `contextId`  
 <span data-ttu-id="70373-108">[in] El identificador del contexto que es el ámbito del campo estático de contexto solicitado.</span><span class="sxs-lookup"><span data-stu-id="70373-108">[in] The ID of the context that is the scope for the requested context-static field.</span></span>  
  
 `ppAddress`  
 <span data-ttu-id="70373-109">[out] Un puntero a la dirección del campo estático que está dentro del contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="70373-109">[out] A pointer to the address of the static field that is within the specified context.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="70373-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="70373-110">Remarks</span></span>  
 <span data-ttu-id="70373-111">El `GetContextStaticAddress` método puede devolver uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="70373-111">The `GetContextStaticAddress` method may return one of the following:</span></span>  
  
-   <span data-ttu-id="70373-112">Un HRESULT CORPROF_E_DATAINCOMPLETE si el campo estático especificado no se ha asignado una dirección en el contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="70373-112">A CORPROF_E_DATAINCOMPLETE HRESULT if the given static field has not been assigned an address in the specified context.</span></span>  
  
-   <span data-ttu-id="70373-113">Las direcciones de los objetos que pueden estar en el montón de elementos no utilizados.</span><span class="sxs-lookup"><span data-stu-id="70373-113">The addresses of objects that may be in the garbage collection heap.</span></span> <span data-ttu-id="70373-114">Estas direcciones pueden no ser válidas después de recolección de elementos no utilizados, por lo que después de recolección de elementos no utilizados, los generadores de perfiles no deben suponer que son válidos.</span><span class="sxs-lookup"><span data-stu-id="70373-114">These addresses may become invalid after garbage collection, so after garbage collection, profilers should not assume that they are valid.</span></span>  
  
 <span data-ttu-id="70373-115">Antes de que se complete el constructor de clase de una clase, `GetContextStaticAddress` devolverá CORPROF_E_DATAINCOMPLETE para todos sus campos estáticos, aunque algunos de los campos estáticos pueden estar ya inicializados y objetos de la colección de elementos no utilizados de la raíz.</span><span class="sxs-lookup"><span data-stu-id="70373-115">Before a class’s class constructor is completed, `GetContextStaticAddress` will return CORPROF_E_DATAINCOMPLETE for all its static fields, although some of the static fields may already be initialized and rooting garbage collection objects.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="70373-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70373-116">Requirements</span></span>  
 <span data-ttu-id="70373-117">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="70373-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="70373-118">**Encabezado:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="70373-118">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="70373-119">**Biblioteca:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="70373-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="70373-120">**Versiones de .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="70373-120">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="70373-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="70373-121">See Also</span></span>  
 [<span data-ttu-id="70373-122">ICorProfilerInfo (interfaz)</span><span class="sxs-lookup"><span data-stu-id="70373-122">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)  
 [<span data-ttu-id="70373-123">ICorProfilerInfo2 (interfaz)</span><span class="sxs-lookup"><span data-stu-id="70373-123">ICorProfilerInfo2 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-interface.md)