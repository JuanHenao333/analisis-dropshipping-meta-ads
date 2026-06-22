---
name: analisis-dropshipping-meta-ads
description: Analiza el rendimiento de una cuenta o campaña de Meta Ads de dropshipping y propone la siguiente campaña a montar (presupuesto, estructura, ángulos, decisión de escalar/matar/iterar). Úsala SIEMPRE que el usuario pida revisar, auditar o diagnosticar números de una campaña de dropshipping en Meta/Facebook/Instagram Ads, pregunte "por qué no está funcionando" un producto o anuncio, pida una "auditoría de cuenta", quiera saber si debe "escalar, matar o iterar" una campaña, o pida que le "armes la siguiente campaña" después de mostrar resultados de la actual. También aplica si solo comparte números sueltos (ROAS, CPA, CTR, gasto) de un producto de dropshipping sin pedir explícitamente un "análisis". NO la uses si el usuario solo pide copies sueltos (usa copy-meta-ads) o solo la nomenclatura/estructura de una campaña nueva sin datos de rendimiento que analizar primero (usa campana-meta-ads).
---

# Análisis y propuesta de campañas de dropshipping en Meta Ads

Esta skill hace dos cosas en orden: primero diagnostica qué está pasando con una cuenta o campaña de dropshipping en Meta Ads, y después usa ese diagnóstico para proponer la siguiente jugada — no al revés. Una propuesta de campaña sin diagnóstico previo es una adivinanza; el valor de esta skill está en que la recomendación se apoya en lo que los números y los creativos ya están diciendo.

Dropshipping tiene una dinámica particular frente a otras verticales: márgenes ajustados (lo que hace que el ROAS "promedio de industria" casi nunca sea suficiente), productos de impulso que dependen de un ángulo de venta que funcione, y ciclos de vida de producto cortos donde la fatiga de creativo llega rápido. Ten esto presente en cada paso.

## Paso 1 — Consigue los datos

No asumas que el usuario tiene un archivo listo. Antes de pedir nada, revisa si ya hay un conector de Meta/Facebook Ads disponible en la sesión:

1. Llama a `ToolSearch` con palabras clave como `"ads insights meta facebook campaign"` o `"meta ads account performance"`. Los nombres de herramienta varían según cómo esté conectado el plugin en cada instalación (suelen verse como `mcp__<id>__ads_get_ad_accounts`, `ads_insights_performance_trend`, `get_creative_insights`, etc.) — no asumas un nombre fijo, busca por palabra clave.
2. Si encuentras herramientas de Ads disponibles, pide la cuenta publicitaria y el rango de fechas, y trae tú mismo los datos (gasto, ROAS, CPA, CTR, frequency, hook rate si está disponible, y desglose por creativo/ángulo).
3. Si NO hay ningún conector disponible (lo más común para alguien que descargó esta skill sin tener el conector de JP), pide los datos directamente. Da estas tres opciones y deja que el usuario elija la que le quede más fácil:
   - Pegar las métricas en el chat (gasto, ROAS, CPA, CTR, frequency por anuncio/ángulo).
   - Subir el CSV exportado de Ads Manager.
   - Subir una captura de pantalla del dashboard.

En cualquiera de los dos caminos, antes de diagnosticar pide también el contexto de negocio — sin esto el diagnóstico es genérico e inútil:

- Margen neto del producto (o precio de venta + costo, para calcularlo).
- Fase de la campaña: ¿es testeo de producto/ángulo nuevo, o ya está validada y se está escalando?
- Objetivo del usuario en este momento: ¿quiere saber si debe matar algo, quiere escalar lo que funciona, o quiere refrescar creativo porque algo se cayó?

## Paso 2 — Diagnostica en cuatro ejes

Lee `references/benchmarks-dropshipping.md` antes de calificar cualquier número — tiene las tablas de benchmark y, más importante, cómo ajustarlas al contexto de dropshipping (el ROAS mínimo viable se calcula sobre el margen real del producto, no sobre el promedio de industria).

Cubre los cuatro ejes siguientes. No te quedes solo en el primero — el motivo más común de que una propuesta de campaña falle es que se basó únicamente en métricas y ignoró que el problema real era de ángulo creativo o de estructura de cuenta.

**1. Métricas de rendimiento.** ROAS vs. el mínimo viable según margen, CPA vs. el % del precio de venta que el negocio puede absorber, CTR, frequency, hook rate y hold rate si hay datos de video. Identifica qué métrica está fuera de rango y a qué nivel (cuenta completa, campaña, ad set, o anuncio individual) — el nivel donde aparece el problema determina la solución.

**2. Ángulos de producto y creativos.** ¿Qué ángulos de venta se han probado (dolor, beneficio, urgencia/escasez, prueba social, demostración de uso, comparación con alternativa) y cuáles faltan? ¿Hay un solo ángulo concentrando la mayoría del gasto mientras el resto no tiene data suficiente para opinar? Un dropshipping product casi siempre tiene 3-5 ángulos viables sin explorar — señala cuáles.

**3. Estructura de cuenta.** ¿La cuenta usa CBO o ABO, y tiene sentido para la fase en la que está (ABO para testeo de ángulos nuevos, CBO una vez hay 2-3 ángulos validados)? ¿Existe una fase de testeo separada de la de escalado, o todo vive en una sola campaña sin distinción? ¿El presupuesto de testeo es suficiente para salir de la fase de aprendizaje de Meta (orientativamente ~50 conversiones por ad set) antes de tomar decisiones?

**4. Benchmarks.** Compara contra las referencias del archivo de benchmarks, pero SIEMPRE aclarando que el benchmark real para dropshipping depende del margen del producto — nunca presentes el promedio de industria como si fuera la meta sin esa salvedad.

## Paso 3 — Sintetiza un veredicto, no solo una lista de números

Cierra el diagnóstico con una conclusión clara por cada anuncio/ángulo evaluado: **escalar**, **matar**, o **iterar** (mismo ángulo, creativo nuevo). Evita quedarte en "el CTR está bajo" sin decir qué hacer al respecto — el usuario necesita una decisión, no solo un dato.

## Paso 4 — Propón la siguiente campaña

A partir del veredicto, construye la propuesta concreta:

- **Presupuesto:** cuánto a testeo de ángulos nuevos vs. cuánto a escalar lo que ya funciona, y por qué esa proporción dado el momento de la cuenta.
- **Estructura:** ABO o CBO, cuántos ad sets/anuncios, y el criterio de cuándo pasar de uno al otro.
- **Ángulos a probar:** prioriza los ángulos identificados como huecos en el Paso 2, no ángulos genéricos desconectados del diagnóstico.
- **Criterio de decisión:** en cuánto tiempo / con qué gasto se va a evaluar esta nueva tanda antes de decidir si escala, mata o itera — así la próxima revisión ya tiene una vara clara.

## Paso 5 — Completa la propuesta con las otras skills si están disponibles (opcional)

Esta skill se enfoca en el diagnóstico y la estrategia — no genera copy ni nomenclatura por sí misma, eso vive en otras dos skills especializadas. Antes de cerrar la propuesta, revisa si están instaladas:

- Si **`campana-meta-ads`** está disponible, ofrece usarla para generar la nomenclatura de Campaña/Conjunto/Anuncio y los copies de los ángulos priorizados en el Paso 4.
- Si solo está **`copy-meta-ads`** disponible (sin `campana-meta-ads`), ofrécela para los copies de los ángulos nuevos, sin nomenclatura.
- Si ninguna está disponible, no es un problema — simplemente cierra la propuesta con la estrategia (presupuesto, estructura, ángulos, criterio de decisión) tal como quedó en el Paso 4, sin inventar copies tú mismo. Si el usuario pide copy ahí mismo, puedes redactarlo de forma simple, pero deja claro que para un paquete completo con frameworks (AIDA/PAS) y variantes A/B existe `copy-meta-ads`.

Esto importa porque alguien en la comunidad puede instalar solo esta skill sin las otras dos — la skill tiene que seguir siendo completa y útil por sí sola, y las otras dos son un plus cuando están presentes, no una dependencia dura.

## Formato del reporte final

Entrega siempre el reporte en el chat (no como documento, salvo que el usuario lo pida explícitamente) con esta estructura:

```
## Diagnóstico

[Resumen de 2-3 líneas del estado general de la cuenta/campaña]

### Métricas
[Hallazgos clave vs. benchmark ajustado a margen]

### Ángulos y creativo
[Qué está probado, qué falta, dónde hay saturación]

### Estructura de cuenta
[CBO/ABO, fase de testeo vs escalado, presupuesto vs aprendizaje]

### Veredicto por anuncio/ángulo
- [Anuncio/ángulo A]: Escalar / Matar / Iterar — por qué
- [Anuncio/ángulo B]: ...

## Propuesta de siguiente campaña

- Presupuesto: ...
- Estructura: ...
- Ángulos a probar: ...
- Criterio de decisión: ...
```

Ajusta el nivel de detalle al volumen de datos disponible — si el usuario solo pegó tres números sueltos, no fuerces las cuatro secciones completas; dilo explícitamente ("con estos datos solo puedo evaluar X, para Y necesitaría Z") en vez de rellenar con suposiciones.
