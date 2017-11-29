---
title: "ICLRTask::RudeAbort (Método)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICLRTask.RudeAbort
api_location: mscoree.dll
api_type: COM
f1_keywords: ICLRTask::RudeAbort
helpviewer_keywords:
- RudeAbort method, ICLRTask interface [.NET Framework hosting]
- ICLRTask::RudeAbort method [.NET Framework hosting]
ms.assetid: b5785468-fcd7-4cc3-8a5d-8796337b53fc
topic_type: apiref
caps.latest.revision: "8"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: df1f688ec3f58ae7317a4fed0dd70cffc1647045
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="iclrtaskrudeabort-method"></a><span data-ttu-id="41662-102">ICLRTask::RudeAbort (Método)</span><span class="sxs-lookup"><span data-stu-id="41662-102">ICLRTask::RudeAbort Method</span></span>
<span data-ttu-id="41662-103">Indica a common language runtime (CLR) para cancelar la tarea representada por el actual [ICLRTask (interfaz)](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md) instancia inmediatamente y de forma incondicional.</span><span class="sxs-lookup"><span data-stu-id="41662-103">Instructs the common language runtime (CLR) to abort the task represented by the current [ICLRTask Interface](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md) instance immediately and unconditionally.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="41662-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="41662-104">Syntax</span></span>  
  
```  
HRESULT RudeAbort ();   
```  
  
## <a name="return-value"></a><span data-ttu-id="41662-105">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="41662-105">Return Value</span></span>  
  
|<span data-ttu-id="41662-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="41662-106">HRESULT</span></span>|<span data-ttu-id="41662-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="41662-107">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="41662-108">S_OK</span><span class="sxs-lookup"><span data-stu-id="41662-108">S_OK</span></span>|<span data-ttu-id="41662-109">`RudeAbort`se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="41662-109">`RudeAbort` returned successfully.</span></span>|  
|<span data-ttu-id="41662-110">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="41662-110">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="41662-111">El CLR no se han cargado en un proceso o el CLR está en un estado en el que no se puede ejecutar código administrado o procesar la llamada correctamente.</span><span class="sxs-lookup"><span data-stu-id="41662-111">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="41662-112">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="41662-112">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="41662-113">La llamada agotó el tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="41662-113">The call timed out.</span></span>|  
|<span data-ttu-id="41662-114">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="41662-114">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="41662-115">El llamador no posee el bloqueo.</span><span class="sxs-lookup"><span data-stu-id="41662-115">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="41662-116">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="41662-116">HOST_E_ABANDONED</span></span>|<span data-ttu-id="41662-117">Se canceló un evento mientras un subproceso bloqueado o fibra esperó en él.</span><span class="sxs-lookup"><span data-stu-id="41662-117">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="41662-118">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="41662-118">E_FAIL</span></span>|<span data-ttu-id="41662-119">Se ha producido un error catastrófico desconocido.</span><span class="sxs-lookup"><span data-stu-id="41662-119">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="41662-120">Cuando un método devuelve E_FAIL, CLR ya no es utilizable dentro del proceso.</span><span class="sxs-lookup"><span data-stu-id="41662-120">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="41662-121">Las llamadas posteriores a métodos de hospedaje devuelven HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="41662-121">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="41662-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="41662-122">Remarks</span></span>  
 <span data-ttu-id="41662-123">Un host llama al método `RudeAbort` para anular una tarea inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="41662-123">A host calls `RudeAbort` to abort a task immediately.</span></span> <span data-ttu-id="41662-124">No se garantiza que los finalizadores y rutinas de control de excepciones que se ejecute.</span><span class="sxs-lookup"><span data-stu-id="41662-124">Finalizers and exception handling routines are not guaranteed to be executed.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="41662-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41662-125">Requirements</span></span>  
 <span data-ttu-id="41662-126">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="41662-126">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="41662-127">**Encabezado:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="41662-127">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="41662-128">**Biblioteca:** incluye como recurso en MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="41662-128">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="41662-129">**Versiones de .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="41662-129">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="41662-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="41662-130">See Also</span></span>  
 [<span data-ttu-id="41662-131">ICLRTask (interfaz)</span><span class="sxs-lookup"><span data-stu-id="41662-131">ICLRTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)  
 [<span data-ttu-id="41662-132">ICLRTaskManager (interfaz)</span><span class="sxs-lookup"><span data-stu-id="41662-132">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)  
 [<span data-ttu-id="41662-133">IHostTask (interfaz)</span><span class="sxs-lookup"><span data-stu-id="41662-133">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)  
 [<span data-ttu-id="41662-134">IHostTaskManager (interfaz)</span><span class="sxs-lookup"><span data-stu-id="41662-134">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)