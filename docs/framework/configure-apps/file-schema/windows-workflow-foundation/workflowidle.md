---
title: <workflowIdle>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: b2ef703c-3e01-4213-9d2e-c14c7dba94d2
ms.openlocfilehash: af8a2568eb13bb3007065c4b4a3564aae27de7ac
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/30/2019
ms.locfileid: "55280935"
---
# <a name="workflowidle"></a>\<workflowIdle>
Un comportamiento del servicio que controla cuando las instancias de flujo de trabajo inactivas se descargan y conservan.  
  
\<system.ServiceModel>  
\<comportamientos >  
\<serviceBehaviors>  
\<comportamiento >  
\<workflowIdle>  
  
## <a name="syntax"></a>Sintaxis  
  
```xml  
<behaviors>
  <serviceBehaviors>
    <behavior name="String">
      <workflowIdle timeToPersist="TimeSpan" 
                    timeToUnload="TimeSpan" />
    </behavior>
  </serviceBehaviors>
</behaviors>  
```  
  
## <a name="attributes-and-elements"></a>Atributos y elementos  
 En las siguientes secciones se describen los atributos, los elementos secundarios y los elementos primarios.  
  
### <a name="attributes"></a>Atributos  
  
|Atributo|Descripción|  
|---------------|-----------------|  
|timeToPersist|Un valor Timespan que especifica la duración entre el momento en el flujo de trabajo se vuelve inactivo y se conserva. El valor predeterminado es TimeSpan.MaxValue.<br /><br /> La duración comienza a transcurrir cuando la instancia de flujo de trabajo se vuelve inactiva. Este atributo es útil si desea conservar una instancia de flujo de trabajo de forma más agresiva mientras se mantiene la instancia en memoria mientras sea posible. Este atributo solo es válido si su valor es menor que el **timeToUnload** atributo. Si es mayor, se omite. Si este atributo transcurre antes de que el valor especificado por el **timeToUnload** atributo, la conservación debe completarse antes de que se descarga el flujo de trabajo. Esto implica que se puede retrasar la operación de descarga hasta que se conserve el flujo de trabajo. El nivel de conservación es responsable de administrar todos los reintentos de errores transitorios y solo produce excepciones con errores no recuperables. Por consiguiente, cualquier excepción producida durante la conservación se trata como grave y se anula la instancia de flujo de trabajo.|  
|timeToUnload|Un valor Timespan que especifica el tiempo que transcurre entre el momento en que el flujo de trabajo se vuelve inactivo y descarga. El valor predeterminado es 1 minuto.<br /><br /> Descargar un flujo de trabajo implica que también se conserva. Si este atributo se establece en cero se conservan y se descargan inmediatamente después de la instancia de flujo de trabajo el flujo de trabajo se vuelve inactiva. Establecer este atributo en TimeSpan.MaxValue eficazmente, deshabilita la operación de descarga. Las instancias de flujo de trabajo inactivas nunca se descargan.|  
  
### <a name="child-elements"></a>Elementos secundarios  
 Ninguno.  
  
### <a name="parent-elements"></a>Elementos primarios  
  
|Elemento|Descripción|  
|-------------|-----------------|  
|[\<comportamiento > de \<serviceBehaviors >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/behavior-of-servicebehaviors-of-workflow.md)|Especifica un elemento de comportamiento.|  
  
## <a name="see-also"></a>Vea también
- <xref:System.ServiceModel.Activities.Description.WorkflowIdleBehavior>
- <xref:System.ServiceModel.Activities.Configuration.WorkflowIdleElement>
