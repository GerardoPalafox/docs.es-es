---
title: BucketParameters (Estructura)
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: BucketParameters
api_location: mscoree.dll
api_type: COM
f1_keywords: BucketParameters
helpviewer_keywords: BucketParameters structure [.NET Framework hosting]
ms.assetid: 9432487e-f276-45d6-9a13-9a68024dbd46
topic_type: apiref
caps.latest.revision: "8"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 7626ce6b2b6278be7cd9989718c13f7c98e4ace3
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/18/2017
---
# <a name="bucketparameters-structure"></a><span data-ttu-id="3939d-102">BucketParameters (Estructura)</span><span class="sxs-lookup"><span data-stu-id="3939d-102">BucketParameters Structure</span></span>
<span data-ttu-id="3939d-103">Almacena el nombre de tipo de un evento y los parámetros de la excepción actual que está asociado con el evento.</span><span class="sxs-lookup"><span data-stu-id="3939d-103">Stores the type name of an event and the parameters for the current exception that is associated with the event.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3939d-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3939d-104">Syntax</span></span>  
  
```  
typedef struct _BucketParameters {  
    BOOL  fInited;                    
    WCHAR pszEventTypeName[255];      
    WCHAR pszParams[10][255];         
} BucketParameters;  
```  
  
## <a name="members"></a><span data-ttu-id="3939d-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="3939d-105">Members</span></span>  
  
|<span data-ttu-id="3939d-106">Miembro</span><span class="sxs-lookup"><span data-stu-id="3939d-106">Member</span></span>|<span data-ttu-id="3939d-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="3939d-107">Description</span></span>|  
|------------|-----------------|  
|`fInited`|<span data-ttu-id="3939d-108">`true`, si el resto de esta estructura es válido; en caso contrario, `false`.</span><span class="sxs-lookup"><span data-stu-id="3939d-108">`true`, if the rest of this structure is valid; otherwise, `false`.</span></span>|  
|`pszEventTypeName`|<span data-ttu-id="3939d-109">Nombre del tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="3939d-109">Name of the event type.</span></span>|  
|`pszParams`|<span data-ttu-id="3939d-110">Una matriz de cadenas, cada uno de los cuales especifica un parámetro para la excepción actual asociada al evento.</span><span class="sxs-lookup"><span data-stu-id="3939d-110">An array of strings, each of which specifies a parameter for the current exception associated with the event.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="3939d-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3939d-111">Requirements</span></span>  
 <span data-ttu-id="3939d-112">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3939d-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3939d-113">**Encabezado:** MSCorEE.idl</span><span class="sxs-lookup"><span data-stu-id="3939d-113">**Header:** MSCorEE.idl</span></span>  
  
 <span data-ttu-id="3939d-114">**Versiones de .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3939d-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3939d-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="3939d-115">See Also</span></span>  
 [<span data-ttu-id="3939d-116">Estructuras de hospedaje</span><span class="sxs-lookup"><span data-stu-id="3939d-116">Hosting Structures</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-structures.md)