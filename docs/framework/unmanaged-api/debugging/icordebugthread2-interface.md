---
title: ICorDebugThread2 (Interfaz1)
ms.date: 03/30/2017
api_name:
- ICorDebugThread2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread2
helpviewer_keywords:
- ICorDebugThread2 interface [.NET Framework debugging]
ms.assetid: 678f89f9-cce7-46d1-af87-5e989abaa93c
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3826bfd16d3cf7534a6e920c516987908547b419
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/23/2019
ms.locfileid: "54716157"
---
# <a name="icordebugthread2-interface1"></a>ICorDebugThread2 (Interfaz1)
Actúa como una extensión lógica ICorDebugThread (interfaz).  
  
## <a name="methods"></a>Métodos  
  
|Método|Descripción|  
|------------|-----------------|  
|[GetActiveFunctions (método)](../../../../docs/framework/unmanaged-api/debugging/icordebugthread2-getactivefunctions-method.md)|Obtiene una matriz de instancias COR_ACTIVE_FUNCTION que contienen datos sobre las funciones activas en los marcos de un subproceso.|  
|[GetConnectionID (método)](../../../../docs/framework/unmanaged-api/debugging/icordebugthread2-getconnectionid-method.md)|Obtiene un identificador de conexión para este `ICorDebugThread2`.|  
|[GetTaskID (método)](../../../../docs/framework/unmanaged-api/debugging/icordebugthread2-gettaskid-method.md)|Obtiene un identificador de tarea para este `ICorDebugThread2`.|  
|[GetVolatileOSThreadID (método)](../../../../docs/framework/unmanaged-api/debugging/icordebugthread2-getvolatileosthreadid-method.md)|Obtiene el identificador del subproceso del sistema operativo para este `ICorDebugThread2`.|  
|[InterceptCurrentException (método)](../../../../docs/framework/unmanaged-api/debugging/icordebugthread2-interceptcurrentexception-method.md)|Permite a un depurador interceptar la excepción actual en un subproceso.|  
  
## <a name="remarks"></a>Comentarios  
  
> [!NOTE]
>  Esta interfaz no admite que se la llame de forma remota, ya sea entre procesos o entre equipos.  
  
## <a name="requirements"></a>Requisitos  
 **Plataformas:** Consulte [Requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Encabezado**: CorDebug.idl, CorDebug.h  
  
 **Biblioteca:** CorGuids.lib  
  
 **Versiones de .NET Framework:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Vea también
- [Interfaces de depuración](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
