---
title: <Uri> (Elemento, Configuración de Uri)
ms.date: 03/30/2017
ms.assetid: c22bab8b-477c-4ae4-8498-65ad409e0847
ms.openlocfilehash: f432be7594b1659dfcae0c6eee706358230f2cbb
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/30/2019
ms.locfileid: "55269255"
---
# <a name="uri-element-uri-settings"></a>\<URI > elemento (configuración de Uri)
Contiene valores que especifican cómo .NET Framework controla las direcciones web expresadas mediante identificadores uniformes de recursos (URI).  
  
## <a name="schema-hierarchy"></a>Jerarquía del esquema  
 [Elemento \<configuration>](../../../../../docs/framework/configure-apps/file-schema/configuration-element.md)  
  
 [\<uri>](../../../../../docs/framework/configure-apps/file-schema/network/uri-element-uri-settings.md)  
  
## <a name="syntax"></a>Sintaxis  
  
```xml  
<uri>  
</uri>  
```  
  
## <a name="attributes-and-elements"></a>Atributos y elementos  
 En las siguientes secciones se describen los atributos, los elementos secundarios y los elementos primarios.  
  
### <a name="attributes"></a>Atributos  
 Ninguno.  
  
### <a name="child-elements"></a>Elementos secundarios  
  
|**Element**|**Descripción**|  
|-----------------|---------------------|  
|[idn](../../../../../docs/framework/configure-apps/file-schema/network/idn-element-uri-settings.md)|Especifica si se aplica el análisis de nombres de dominio internacionalizados (IDN) a los nombres de dominio.|  
|[iriParsing](../../../../../docs/framework/configure-apps/file-schema/network/iriparsing-element-uri-settings.md)|Especifica si el análisis de identificadores de recursos internacionales (IRI) se aplica a <xref:System.Uri> y si debe aplicarse las reglas de análisis de IRI.|  
|[schemeSettings](../../../../../docs/framework/configure-apps/file-schema/network/schemesettings-element-uri-settings.md)|Especifica cómo se analizará un <xref:System.Uri> para esquemas concretos.|  
  
### <a name="parent-elements"></a>Elementos primarios  
  
|**Element**|**Descripción**|  
|-----------------|---------------------|  
|[configuration](../../../../../docs/framework/configure-apps/file-schema/configuration-element.md)|Contiene la configuración para todos los espacios de nombres.|  
  
## <a name="remarks"></a>Comentarios  
 El `uri` elemento contiene los valores para los miembros de la <xref:System.Uri> clase usada por las clases en el <xref:System.Net> espacio de nombres. Configura la configuración de la compatibilidad con IRI e IDN.  
  
## <a name="example"></a>Ejemplo  
  
### <a name="description"></a>Descripción  
 El ejemplo siguiente muestra una configuración utilizada por el <xref:System.Uri> clase para admitir el análisis de IRI y nombres de IDN. El ejemplo también borra todos los valores de esquema y, a continuación, agrega compatibilidad para delimitadores de ruta de acceso codificados con porcentaje para el esquema http.  
  
### <a name="code"></a>Código  
  
```xml  
<configuration>  
  <uri>  
    <idn enabled="All" />  
    <iriParsing enabled="true" />  
    <schemeSettings>  
      <clear/>  
      <add name="http" genericUriParserOptions="DontUnescapePathDotsAndSlashes"/>  
    </schemeSettings>  
  </uri>  
</configuration>  
```  
  
## <a name="see-also"></a>Vea también
- [Esquema de la configuración de red](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
