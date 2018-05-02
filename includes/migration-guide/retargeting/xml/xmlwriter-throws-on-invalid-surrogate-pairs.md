### <a name="xmlwriter-throws-on-invalid-surrogate-pairs"></a><span data-ttu-id="9aa90-101">XmlWriter inicia una excepción en los pares suplentes no válidos</span><span class="sxs-lookup"><span data-stu-id="9aa90-101">XmlWriter throws on invalid surrogate pairs</span></span>

|   |   |
|---|---|
|<span data-ttu-id="9aa90-102">Detalles</span><span class="sxs-lookup"><span data-stu-id="9aa90-102">Details</span></span>|<span data-ttu-id="9aa90-103">Para las aplicaciones destinadas a .NET Framework 4.5.2 o versiones anteriores, el procedimiento de escribir un par suplente no válido usando el control de reserva de excepción no siempre produce una excepción.</span><span class="sxs-lookup"><span data-stu-id="9aa90-103">For apps that target the .NET Framework 4.5.2 or previous versions, writing an invalid surrogate pair using exception fallback handling does not always throw an exception.</span></span> <span data-ttu-id="9aa90-104">Para las aplicaciones destinadas a .NET Framework 4.6, si se intenta escribir un par suplente no válido se inicia una excepción <xref:System.ArgumentException?displayProperty=name>.</span><span class="sxs-lookup"><span data-stu-id="9aa90-104">For apps that target the .NET Framework 4.6, attempting to write an invalid surrogate pair throws an <xref:System.ArgumentException?displayProperty=name>.</span></span>|
|<span data-ttu-id="9aa90-105">Sugerencia</span><span class="sxs-lookup"><span data-stu-id="9aa90-105">Suggestion</span></span>|<span data-ttu-id="9aa90-106">Si es necesario, esta interrupción se puede evitar seleccionando .NET Framework 4.5.2 o una versión anterior como destino.</span><span class="sxs-lookup"><span data-stu-id="9aa90-106">If necessary, this break can be avoided by targeting the .NET Framework 4.5.2 or earlier.</span></span> <span data-ttu-id="9aa90-107">Como alternativa, se puede realizar el preprocesamiento de los pares suplentes no válidos en código XML válido antes de escribirlos.</span><span class="sxs-lookup"><span data-stu-id="9aa90-107">Alternatively, invalid surrogate pairs can be pre-processed into valid xml prior to writing them.</span></span>|
|<span data-ttu-id="9aa90-108">Ámbito</span><span class="sxs-lookup"><span data-stu-id="9aa90-108">Scope</span></span>|<span data-ttu-id="9aa90-109">Borde</span><span class="sxs-lookup"><span data-stu-id="9aa90-109">Edge</span></span>|
|<span data-ttu-id="9aa90-110">Versión</span><span class="sxs-lookup"><span data-stu-id="9aa90-110">Version</span></span>|<span data-ttu-id="9aa90-111">4.6</span><span class="sxs-lookup"><span data-stu-id="9aa90-111">4.6</span></span>|
|<span data-ttu-id="9aa90-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="9aa90-112">Type</span></span>|<span data-ttu-id="9aa90-113">Redestinación</span><span class="sxs-lookup"><span data-stu-id="9aa90-113">Retargeting</span></span>|
|<span data-ttu-id="9aa90-114">API afectadas</span><span class="sxs-lookup"><span data-stu-id="9aa90-114">Affected APIs</span></span>|<ul><li><xref:System.Xml.XmlWriter.WriteAttributeString(System.String,System.String)?displayProperty=nameWithType></li><li><xref:System.Xml.XmlWriter.WriteAttributeString(System.String,System.String,System.String)?displayProperty=nameWithType></li><li><xref:System.Xml.XmlWriter.WriteAttributeString(System.String,System.String,System.String,System.String)?displayProperty=nameWithType></li><li><xref:System.Xml.XmlWriter.WriteAttributeStringAsync(System.String,System.String,System.String,System.String)?displayProperty=nameWithType></li><li><xref:System.Xml.XmlWriter.WriteCData(System.String)?displayProperty=nameWithType></li><li><xref:System.Xml.XmlWriter.WriteCDataAsync(System.String)?displayProperty=nameWithType></li><li><xref:System.Xml.XmlWriter.WriteChars(System.Char[],System.Int32,System.Int32)?displayProperty=nameWithType></li><li><xref:System.Xml.XmlWriter.WriteCharsAsync(System.Char[],System.Int32,System.Int32)?displayProperty=nameWithType></li><li><xref:System.Xml.XmlWriter.WriteComment(System.String)?displayProperty=nameWithType></li><li><xref:System.Xml.XmlWriter.WriteCommentAsync(System.String)?displayProperty=nameWithType></li><li><xref:System.Xml.XmlWriter.WriteEntityRef(System.String)?displayProperty=nameWithType></li><li><xref:System.Xml.XmlWriter.WriteEntityRefAsync(System.String)?displayProperty=nameWithType></li><li><xref:System.Xml.XmlWriter.WriteRaw(System.Char[],System.Int32,System.Int32)?displayProperty=nameWithType></li><li><xref:System.Xml.XmlWriter.WriteProcessingInstruction(System.String,System.String)?displayProperty=nameWithType></li><li><xref:System.Xml.XmlWriter.WriteProcessingInstructionAsync(System.String,System.String)?displayProperty=nameWithType></li><li><xref:System.Xml.XmlWriter.WriteRaw(System.String)?displayProperty=nameWithType></li><li><xref:System.Xml.XmlWriter.WriteRawAsync(System.Char[],System.Int32,System.Int32)?displayProperty=nameWithType></li><li><xref:System.Xml.XmlWriter.WriteRawAsync(System.String)?displayProperty=nameWithType></li><li><xref:System.Xml.XmlWriter.WriteString(System.String)?displayProperty=nameWithType></li><li><xref:System.Xml.XmlWriter.WriteStringAsync(System.String)?displayProperty=nameWithType></li><li><xref:System.Xml.XmlWriter.WriteSurrogateCharEntity(System.Char,System.Char)?displayProperty=nameWithType></li><li><xref:System.Xml.XmlWriter.WriteSurrogateCharEntityAsync(System.Char,System.Char)?displayProperty=nameWithType></li><li><xref:System.Xml.XmlWriter.WriteValue(System.String)?displayProperty=nameWithType></li></ul>|
