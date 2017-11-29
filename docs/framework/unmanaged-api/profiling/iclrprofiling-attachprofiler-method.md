---
title: "ICLRProfiling::AttachProfiler (Método)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IClrProfiling.AttachProfiler Method
api_location: Mscorwks.dll
api_type: COM
f1_keywords: IClrProfiling::AttachProfiler
helpviewer_keywords:
- AttachProfiler method [.NET Framework profiling]
- IClrProfiling::AttachProfiler method [.NET Framework profiling]
ms.assetid: 535a6839-c443-405b-a6f4-e2af90725d5b
topic_type: apiref
caps.latest.revision: "15"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 1a0f1e41f7d59074f997a5812da61fdbcd692770
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="iclrprofilingattachprofiler-method"></a><span data-ttu-id="ae12d-102">ICLRProfiling::AttachProfiler (Método)</span><span class="sxs-lookup"><span data-stu-id="ae12d-102">ICLRProfiling::AttachProfiler Method</span></span>
<span data-ttu-id="ae12d-103">Asocia el generador de perfiles especificado al proceso especificado.</span><span class="sxs-lookup"><span data-stu-id="ae12d-103">Attaches the specified profiler to the specified process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ae12d-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ae12d-104">Syntax</span></span>  
  
```  
HRESULT AttachProfiler(  
  [in] DWORD dwProfileeProcessID,  
  [in] DWORD dwMillisecondsMax,                     // optional  
  [in] const CLSID * pClsidProfiler,  
  [in] LPCWSTR wszProfilerPath,                     // optional  
  [in] size_is(cbClientData)] void * pvClientData,  // optional  
  [in] UINT cbClientData);                          // optional  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ae12d-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ae12d-105">Parameters</span></span>  
 `dwProfileeProcessID`  
 <span data-ttu-id="ae12d-106">[in] Identificador del proceso al que se debe asociar el generador de perfiles.</span><span class="sxs-lookup"><span data-stu-id="ae12d-106">[in] The process ID of the process to which the profiler should be attached.</span></span> <span data-ttu-id="ae12d-107">En un equipo de 64 bits, el valor de bits del proceso cuyo perfil se ha generado debe coincidir con el valor de bits del proceso desencadenador que llama a `AttachProfiler`.</span><span class="sxs-lookup"><span data-stu-id="ae12d-107">On a 64-bit machine, the profiled process's bitness must match the bitness of the trigger process that is calling `AttachProfiler`.</span></span> <span data-ttu-id="ae12d-108">Si la cuenta de usuario con la que llama a `AttachProfiler` tiene privilegios administrativos, el proceso de destino puede ser cualquier proceso del sistema.</span><span class="sxs-lookup"><span data-stu-id="ae12d-108">If the user account under which `AttachProfiler` is called has administrative privileges, the target process may be any process on the system.</span></span> <span data-ttu-id="ae12d-109">De lo contrario, el proceso de destino debe pertenecer a la misma cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="ae12d-109">Otherwise, the target process must be owned by the same user account.</span></span>  
  
 `dwMillisecondsMax`  
 <span data-ttu-id="ae12d-110">[in] Tiempo, en milisegundos, que `AttachProfiler` tarda en completarse.</span><span class="sxs-lookup"><span data-stu-id="ae12d-110">[in] The time duration, in milliseconds, for `AttachProfiler` to complete.</span></span> <span data-ttu-id="ae12d-111">El proceso de desencadenador debe pasar un tiempo de espera que se sabe que es suficiente para que el generador de perfiles determinado complete su inicialización.</span><span class="sxs-lookup"><span data-stu-id="ae12d-111">The trigger process should pass a timeout that is known to be sufficient for the particular profiler to complete its initialization.</span></span>  
  
 `pClsidProfiler`  
 <span data-ttu-id="ae12d-112">[in] Puntero al CLSID del generador de perfiles que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="ae12d-112">[in] A pointer to the CLSID of the profiler to be loaded.</span></span> <span data-ttu-id="ae12d-113">El proceso desencadenador puede reutilizar esta memoria después de que `AttachProfiler` vuelva.</span><span class="sxs-lookup"><span data-stu-id="ae12d-113">The trigger process can reuse this memory after `AttachProfiler` returns.</span></span>  
  
 `wszProfilerPath`  
 <span data-ttu-id="ae12d-114">[in] Ruta de acceso completa al archivo DLL del generador de perfiles que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="ae12d-114">[in] The full path to the profiler’s DLL file to be loaded.</span></span> <span data-ttu-id="ae12d-115">Esta cadena debe contener un máximo de 260 caracteres, incluido el terminador NULL.</span><span class="sxs-lookup"><span data-stu-id="ae12d-115">This string should contain no more than 260 characters, including the null terminator.</span></span> <span data-ttu-id="ae12d-116">Si `wszProfilerPath` es NULL o una cadena vacía, Common Language Runtime (CLR) intentará encontrar la ubicación del archivo DLL del generador de perfiles; para ello, buscará en el Registro el CLSID al que `pClsidProfiler` apunta.</span><span class="sxs-lookup"><span data-stu-id="ae12d-116">If `wszProfilerPath` is null or an empty string, the common language runtime (CLR) will try to find the location of the profiler’s DLL file by looking in the registry for the CLSID that `pClsidProfiler` points to.</span></span>  
  
 `pvClientData`  
 <span data-ttu-id="ae12d-117">[in] Un puntero a datos que se va a pasar al generador de perfiles mediante el [ICorProfilerCallback3:: InitializeForAttach](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback3-initializeforattach-method.md) método.</span><span class="sxs-lookup"><span data-stu-id="ae12d-117">[in] A pointer to data to be passed to the profiler by the [ICorProfilerCallback3::InitializeForAttach](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback3-initializeforattach-method.md) method.</span></span> <span data-ttu-id="ae12d-118">El proceso desencadenador puede reutilizar esta memoria después de que `AttachProfiler` vuelva.</span><span class="sxs-lookup"><span data-stu-id="ae12d-118">The trigger process can reuse this memory after `AttachProfiler` returns.</span></span> <span data-ttu-id="ae12d-119">Si `pvClientData` es NULL, `cbClientData` debe ser 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="ae12d-119">If `pvClientData` is null, `cbClientData` must be 0 (zero).</span></span>  
  
 `cbClientData`  
 <span data-ttu-id="ae12d-120">[in] Tamaño, en bytes, de los datos a los que señala `pvClientData`.</span><span class="sxs-lookup"><span data-stu-id="ae12d-120">[in] The size, in bytes, of the data that `pvClientData` points to.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ae12d-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ae12d-121">Return Value</span></span>  
 <span data-ttu-id="ae12d-122">Este método devuelve los HRESULT siguientes.</span><span class="sxs-lookup"><span data-stu-id="ae12d-122">This method returns the following HRESULTs.</span></span>  
  
|<span data-ttu-id="ae12d-123">HRESULT</span><span class="sxs-lookup"><span data-stu-id="ae12d-123">HRESULT</span></span>|<span data-ttu-id="ae12d-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="ae12d-124">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="ae12d-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae12d-125">S_OK</span></span>|<span data-ttu-id="ae12d-126">El generador de perfiles especificado se ha asociado correctamente al proceso de destino.</span><span class="sxs-lookup"><span data-stu-id="ae12d-126">The specified profiler has successfully attached to the target process.</span></span>|  
|<span data-ttu-id="ae12d-127">CORPROF_E_PROFILER_ALREADY_ACTIVE</span><span class="sxs-lookup"><span data-stu-id="ae12d-127">CORPROF_E_PROFILER_ALREADY_ACTIVE</span></span>|<span data-ttu-id="ae12d-128">Ya hay un generador de perfiles activo o asociado al proceso de destino.</span><span class="sxs-lookup"><span data-stu-id="ae12d-128">There is already a profiler active or attaching to the target process.</span></span>|  
|<span data-ttu-id="ae12d-129">CORPROF_E_PROFILER_NOT_ATTACHABLE</span><span class="sxs-lookup"><span data-stu-id="ae12d-129">CORPROF_E_PROFILER_NOT_ATTACHABLE</span></span>|<span data-ttu-id="ae12d-130">El generador de perfiles especificado no admite la asociación.</span><span class="sxs-lookup"><span data-stu-id="ae12d-130">The specified profiler does not support attachment.</span></span> <span data-ttu-id="ae12d-131">El proceso desencadenador puede intentar asociar un generador de perfiles diferente.</span><span class="sxs-lookup"><span data-stu-id="ae12d-131">The trigger process may attempt to attach a different profiler.</span></span>|  
|<span data-ttu-id="ae12d-132">CORPROF_E_PROFILEE_INCOMPATIBLE_WITH_TRIGGER</span><span class="sxs-lookup"><span data-stu-id="ae12d-132">CORPROF_E_PROFILEE_INCOMPATIBLE_WITH_TRIGGER</span></span>|<span data-ttu-id="ae12d-133">No puede solicitar la asociación de un generador de perfiles porque la versión del proceso de destino es incompatible con el proceso actual que está llamando a `AttachProfiler`.</span><span class="sxs-lookup"><span data-stu-id="ae12d-133">Unable to request a profiler attachment, because the version of the target process is incompatible with the current process that is calling `AttachProfiler`.</span></span>|  
|<span data-ttu-id="ae12d-134">HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)</span><span class="sxs-lookup"><span data-stu-id="ae12d-134">HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)</span></span>|<span data-ttu-id="ae12d-135">El usuario del proceso desencadenador no tiene acceso al proceso de destino.</span><span class="sxs-lookup"><span data-stu-id="ae12d-135">The user of the trigger process does not have access to the target process.</span></span>|  
|<span data-ttu-id="ae12d-136">HRESULT_FROM_WIN32(ERROR_PRIVILEGE_NOT_HELD)</span><span class="sxs-lookup"><span data-stu-id="ae12d-136">HRESULT_FROM_WIN32(ERROR_PRIVILEGE_NOT_HELD)</span></span>|<span data-ttu-id="ae12d-137">El usuario del proceso desencadenador no tiene los privilegios necesarios para asociar un generador de perfiles al proceso de destino especificado.</span><span class="sxs-lookup"><span data-stu-id="ae12d-137">The user of the trigger process does not have the privileges necessary to attach a profiler to the given target process.</span></span> <span data-ttu-id="ae12d-138">El registro de eventos de aplicación puede contener más información.</span><span class="sxs-lookup"><span data-stu-id="ae12d-138">The application event log may contain more information.</span></span>|  
|<span data-ttu-id="ae12d-139">CORPROF_E_IPC_FAILED</span><span class="sxs-lookup"><span data-stu-id="ae12d-139">CORPROF_E_IPC_FAILED</span></span>|<span data-ttu-id="ae12d-140">Se produjo un error de comunicación con el proceso de destino.</span><span class="sxs-lookup"><span data-stu-id="ae12d-140">A failure occurred when communicating with the target process.</span></span> <span data-ttu-id="ae12d-141">Esto suele ocurrir si el proceso de destino se estaba cerrando.</span><span class="sxs-lookup"><span data-stu-id="ae12d-141">This commonly happens if the target process was shutting down.</span></span>|  
|<span data-ttu-id="ae12d-142">HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)</span><span class="sxs-lookup"><span data-stu-id="ae12d-142">HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)</span></span>|<span data-ttu-id="ae12d-143">El proceso de destino no existe o no está ejecutando ningún CLR que admita la asociación.</span><span class="sxs-lookup"><span data-stu-id="ae12d-143">The target process does not exist or is not running a CLR that supports attachment.</span></span> <span data-ttu-id="ae12d-144">Esto puede indicar que el CLR se descargó desde la llamada al método de enumeración en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="ae12d-144">This may indicate that the CLR was unloaded since the call to the runtime enumeration method.</span></span>|  
|<span data-ttu-id="ae12d-145">HRESULT_FROM_WIN32(ERROR_TIMEOUT)</span><span class="sxs-lookup"><span data-stu-id="ae12d-145">HRESULT_FROM_WIN32(ERROR_TIMEOUT)</span></span>|<span data-ttu-id="ae12d-146">El tiempo de espera se agotó sin que el generador de perfiles comenzara a cargarse.</span><span class="sxs-lookup"><span data-stu-id="ae12d-146">The timeout expired without beginning to load the profiler.</span></span> <span data-ttu-id="ae12d-147">Puede volver a intentar la operación de asociación.</span><span class="sxs-lookup"><span data-stu-id="ae12d-147">You can retry the attach operation.</span></span> <span data-ttu-id="ae12d-148">El tiempo de espera se agota cuando un finalizador del proceso de destino se ejecuta durante más tiempo que el valor del tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="ae12d-148">Timeouts occur when a finalizer in the target process runs for a longer time than the timeout value.</span></span>|  
|<span data-ttu-id="ae12d-149">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ae12d-149">E_INVALIDARG</span></span>|<span data-ttu-id="ae12d-150">Uno o más parámetros tienen valores no válidos.</span><span class="sxs-lookup"><span data-stu-id="ae12d-150">One or more parameters have invalid values.</span></span>|  
|<span data-ttu-id="ae12d-151">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ae12d-151">E_FAIL</span></span>|<span data-ttu-id="ae12d-152">Se ha producido algún otro error no especificado.</span><span class="sxs-lookup"><span data-stu-id="ae12d-152">Some other, unspecified failure occurred.</span></span>|  
|<span data-ttu-id="ae12d-153">Otros códigos de error</span><span class="sxs-lookup"><span data-stu-id="ae12d-153">Other error codes</span></span>|<span data-ttu-id="ae12d-154">Si el generador de perfiles [ICorProfilerCallback3:: InitializeForAttach](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback3-initializeforattach-method.md) método devuelve un HRESULT que indica un error, `AttachProfiler` devuelve ese mismo HRESULT.</span><span class="sxs-lookup"><span data-stu-id="ae12d-154">If the profiler’s [ICorProfilerCallback3::InitializeForAttach](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback3-initializeforattach-method.md) method returns an HRESULT that indicates failure, `AttachProfiler` returns that same HRESULT.</span></span> <span data-ttu-id="ae12d-155">En este caso, E_NOTIMPL se convierte en CORPROF_E_PROFILER_NOT_ATTACHABLE.</span><span class="sxs-lookup"><span data-stu-id="ae12d-155">In this case, E_NOTIMPL is converted to CORPROF_E_PROFILER_NOT_ATTACHABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ae12d-156">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ae12d-156">Remarks</span></span>  
  
## <a name="memory-management"></a><span data-ttu-id="ae12d-157">Administración de memoria</span><span class="sxs-lookup"><span data-stu-id="ae12d-157">Memory Management</span></span>  
 <span data-ttu-id="ae12d-158">En consonancia con las convenciones de COM, el llamador de `AttachProfiler` (por ejemplo, el código desencadenador creado por el desarrollador del generador de perfiles) es responsable de la asignación y desasignación de la memoria para los datos a los que el parámetro `pvClientData` apunta.</span><span class="sxs-lookup"><span data-stu-id="ae12d-158">In keeping with COM conventions, the caller of `AttachProfiler` (for example, the trigger code authored by the profiler developer) is responsible for allocating and de-allocating the memory for the data that the `pvClientData` parameter points to.</span></span> <span data-ttu-id="ae12d-159">Cuando el CLR ejecuta la llamada a `AttachProfiler`, realiza una copia de la memoria a la que `pvClientData` apunta y la transmite al proceso de destino.</span><span class="sxs-lookup"><span data-stu-id="ae12d-159">When the CLR executes the `AttachProfiler` call, it makes a copy of the memory that `pvClientData` points to and transmits it to the target process.</span></span> <span data-ttu-id="ae12d-160">Cuando el CLR dentro del proceso de destino recibe su propia copia del bloque `pvClientData`, pasa el bloque al generador de perfiles con el método `InitializeForAttach` y, después, desasigna su copia del bloque `pvClientData` del proceso de destino.</span><span class="sxs-lookup"><span data-stu-id="ae12d-160">When the CLR inside the target process receives its own copy of the `pvClientData` block, it passes the block to the profiler through the `InitializeForAttach` method, and then deallocates its copy of the `pvClientData` block from the target process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ae12d-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae12d-161">Requirements</span></span>  
 <span data-ttu-id="ae12d-162">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ae12d-162">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ae12d-163">**Encabezado:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="ae12d-163">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="ae12d-164">**Biblioteca:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ae12d-164">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ae12d-165">**Versiones de .NET framework:**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ae12d-165">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ae12d-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="ae12d-166">See Also</span></span>  
 [<span data-ttu-id="ae12d-167">ICorProfilerCallback (interfaz)</span><span class="sxs-lookup"><span data-stu-id="ae12d-167">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)  
 [<span data-ttu-id="ae12d-168">ICorProfilerInfo3 (interfaz)</span><span class="sxs-lookup"><span data-stu-id="ae12d-168">ICorProfilerInfo3 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-interface.md)  
 [<span data-ttu-id="ae12d-169">Interfaces de generación de perfiles</span><span class="sxs-lookup"><span data-stu-id="ae12d-169">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)  
 [<span data-ttu-id="ae12d-170">Generación de perfiles</span><span class="sxs-lookup"><span data-stu-id="ae12d-170">Profiling</span></span>](../../../../docs/framework/unmanaged-api/profiling/index.md)