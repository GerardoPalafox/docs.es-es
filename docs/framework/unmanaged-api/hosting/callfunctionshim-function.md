---
title: CallFunctionShim (Función)
ms.date: 03/30/2017
api_name:
- CallFunctionShim
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- CallFunctionShim
helpviewer_keywords:
- CallfunctionShim function [.NET Framework hosting]
ms.assetid: 37118465-ddf3-41f0-bf27-335b72777e63
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 39223e10b0f75eefb83f3b9a83c5f030318cd715
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/23/2019
ms.locfileid: "54738935"
---
# <a name="callfunctionshim-function"></a>CallFunctionShim (Función)
Realiza una llamada a la función que tiene el nombre especificado y los parámetros de la biblioteca especificada.  
  
 Esta función está en desuso en [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].  
  
## <a name="syntax"></a>Sintaxis  
  
```  
HRESULT CallFunctionShim (  
    [in] LPCWSTR     szDllName,  
    [in] LPCSTR      szFunctionName,  
    [in] LPVOID      lpvArgument1,  
    [in] LPVOID      lpvArgument2,  
    [in] LPCWSTR     szVersion,  
    [in] LPVOID      pvReserved  
);  
```  
  
#### <a name="parameters"></a>Parámetros  
 `szDllName`  
 [in] El nombre de la biblioteca que contiene la función.  
  
 `szFunctionName`  
 [in] El nombre de la función.  
  
 `lpvArgument1`  
 [in] El primer argumento para pasar a la función.  
  
 `lpvArgument2`  
 [in] El segundo argumento para pasar a la función.  
  
 `szVersion`  
 [in] La versión de la biblioteca que contiene la función.  
  
 `pvReserved`  
 [in] Reservado para uso futuro. Pasar cero en este parámetro.  
  
## <a name="requirements"></a>Requisitos  
 **Plataformas:** Consulte [Requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Encabezado**: MSCorEE.h  
  
 **Biblioteca:** MSCorEE.dll  
  
 **Versiones de .NET Framework:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Vea también
- [Funciones de hospedaje de CLR en desuso](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)
