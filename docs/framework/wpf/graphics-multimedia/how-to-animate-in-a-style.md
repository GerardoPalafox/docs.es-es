---
title: Cómo animar en un estilo (WPF)
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], properties [WPF], within styles
- styles [WPF], animating properties within
ms.assetid: 6a791f3d-6b1f-4972-a2f9-35880bcfd954
ms.openlocfilehash: a455bbfb9defbcf83f7e490f60031917a3b41779
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/25/2018
ms.locfileid: "47079404"
---
# <a name="how-to-animate-in-a-style"></a>Cómo animar en un estilo

En este ejemplo se muestra cómo animar propiedades dentro de un estilo. Al animar dentro de un estilo, se puede destinar solo el elemento de marco para el que está definido el estilo directamente. Para establecer el destino de un objeto freezable, debe "punto hacia abajo" de una propiedad del elemento de estilo.

En el ejemplo siguiente, se definen dentro de un estilo y se aplica a varias animaciones una <xref:System.Windows.Controls.Button>. Cuando el usuario mueve el mouse sobre el botón, se desvanece de opaco a parcialmente translúcido y viceversa, repetidamente. Cuando el usuario mueve el mouse fuera del botón, se vuelve completamente opaco. Cuando se hace clic en el botón, cambia su color de fondo de color naranja a blanco y viceversa. Dado que el <xref:System.Windows.Media.SolidColorBrush> se usa para pintar el botón no se puede establecer como destino directamente, se tiene acceso a estableciendo una relación en el botón <xref:System.Windows.Controls.Control.Background%2A> propiedad.

## <a name="example"></a>Ejemplo

[!code-xaml[timingbehaviors_snip#21](../../../../samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/StyleStoryboardsExample.xaml#21)]

Tenga en cuenta que al animar dentro de un estilo, es posible a los objetos de destino que no existen. Por ejemplo, suponga que usa el estilo de un <xref:System.Windows.Media.SolidColorBrush> se invalida establecer la propiedad de fondo de un botón, pero en algún momento el estilo y el fondo del botón se establece con un <xref:System.Windows.Media.LinearGradientBrush>.  Intentar animar el <xref:System.Windows.Media.SolidColorBrush> no arrojará una excepción; la animación simplemente se producirá un error en modo silencioso.

Para obtener más información acerca de guión gráfico como destino la sintaxis, vea el [Storyboards Overview](../../../../docs/framework/wpf/graphics-multimedia/storyboards-overview.md). Para obtener más información acerca de la animación, vea el [información general sobre animaciones](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md). Para obtener más información sobre los estilos, vea el [aplicar estilos y plantillas](../../../../docs/framework/wpf/controls/styling-and-templating.md).
