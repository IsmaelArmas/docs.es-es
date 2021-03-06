---
title: Buscar un elemento de UI Automation basándose en una condición de propiedad
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- elements, finding by property conditions
- UI Automation, finding elements by property conditions
ms.assetid: 3acaee5a-6ce8-4c3e-81c8-67e59eb74477
author: Xansky
ms.author: mhopkins
ms.openlocfilehash: 08bf454ef5514af2c7c056ad90db247792a5d61c
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/13/2019
ms.locfileid: "56221113"
---
# <a name="find-a-ui-automation-element-based-on-a-property-condition"></a>Buscar un elemento de UI Automation basándose en una condición de propiedad
> [!NOTE]
>  Esta documentación está dirigida a los desarrolladores de .NET Framework que quieran usar las clases [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] administradas definidas en el espacio de nombres <xref:System.Windows.Automation>. Para obtener información más reciente sobre [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)], consulte [Windows Automation API: Automatización de interfaz de usuario](https://go.microsoft.com/fwlink/?LinkID=156746).  
  
 En este tema contiene código de ejemplo que muestra cómo buscar un elemento dentro de la [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] en forma de árbol en una o varias propiedades específicas.  
  
## <a name="example"></a>Ejemplo  
 En el ejemplo siguiente, un conjunto de condiciones de propiedades se especifican que identifican un elemento determinado (o elementos) de interés en el <xref:System.Windows.Automation.AutomationElement> árbol. A continuación, se realiza una búsqueda para todos los elementos coincidentes con el <xref:System.Windows.Automation.AutomationElement.FindAll%2A> método que incorpora una serie de <xref:System.Windows.Automation.AndCondition> operaciones booleanas para limitar el número de elementos coincidentes.  
  
> [!NOTE]
>  Al realizar búsquedas desde el <xref:System.Windows.Automation.AutomationElement.RootElement%2A>, debería intentar obtener solo los elementos secundarios directos. Una búsqueda de descendientes puede iterar a través de cientos o incluso miles de elementos, lo cual un desbordamiento de pila. Si intenta obtener un elemento concreto en un nivel inferior, debe iniciar la búsqueda desde la ventana de aplicación o desde un contenedor en un nivel inferior.  
  
 [!code-csharp[InvokePatternApp#1100](../../../samples/snippets/csharp/VS_Snippets_Wpf/InvokePatternApp/CSharp/InvokePatternApp.cs#1100)]
 [!code-vb[InvokePatternApp#1100](../../../samples/snippets/visualbasic/VS_Snippets_Wpf/InvokePatternApp/VisualBasic/Client.vb#1100)]  
  
## <a name="see-also"></a>Vea también
- [Ejemplo de elemento de menú ExpandCollapsePattern y InvokePattern](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms771636(v=vs.90))
- [Obtención de elementos de Automatización de la interfaz de usuario](../../../docs/framework/ui-automation/obtaining-ui-automation-elements.md)
- [Uso de la propiedad AutomationID](../../../docs/framework/ui-automation/use-the-automationid-property.md)
