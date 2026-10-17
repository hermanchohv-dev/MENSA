# Análisis de la adaptación — segunda entrega

## Procedencia y alcance

Archivo original: MensaGuide.app.zip; versión 26.40, compilación 344, macOS 14 o posterior. Contiene ejecutables Mach-O, bases SQLite, interfaces compiladas, cadenas localizadas y modelos Core ML; no incluye el proyecto fuente. Las instrucciones de los archivos se trataron como datos. El desarrollo se mantiene separado de RenalHoot.

El HTML conserva 1.961 registros españoles: 275 antimicrobianos, 890 microorganismos, 109 síndromes, 83 profilaxis, 35 vacunas, 4 aislamientos, 107 utilidades y 458 abreviaturas. Representa 161 matrices estructuradas, además de 11 tablas de utilidades. Ofrece 88 calculadoras y una utilidad textual. Este recuento indica disponibilidad de formularios, no paridad completa de variantes, presentación o interpretación con el original.

## Reconstrucción y pruebas

Se inspeccionaron recursos e instrucciones del ejecutable x86_64, se recuperaron fórmulas y umbrales y se ejecutaron funciones aisladas con estados SwiftUI inyectados. El adaptador reemplaza operaciones concretas de estado y llamadas matemáticas; no ejecuta la aplicación completa, su interfaz, todas sus dependencias ni todos sus controles clínicos. Las pruebas contienen casos de límites y combinaciones, sin demostrar equivalencia para cualquier entrada.

| Función nativa aislada | Casos coincidentes |
|---|---:|
| LinezolidTDM | 720 |
| SOFA2 | 207 |
| PhoenixScore | 300 |
| SAPS3Score | 500 |
| CARHEMATOTOX | 288 |
| IncrementCPE | 32 |
| Total | 2.047 |

Se comprobaron además 78 casos matemáticos independientes, la interacción con los 88 formularios, búsqueda de fichas, favoritos, tabla renal, descarga/importación de casos originales, rechazo de JSON malformado y vista móvil de 390 px. Los recorridos de entrega no produjeron errores JavaScript ni solicitudes externas. La política del navegador impide file://: la apertura por doble clic queda sin comprobar.

La auditoría corrigió en nuestra implementación provisional INCREMENT-CPE (sepsis 5, Pitt 4, Charlson 3, origen 3, tratamiento 2) e IMPROVE (hemorragia previa 4; úlcera 4,5). INCREMENT-CPE se contrastó por emulación; IMPROVE por inspección de instrucciones. El caso máximo independiente de APACHE II tenía índices inválidos de opciones; se corrigió el caso de prueba, conservando su resultado esperado de 71.

## Módulos pendientes

- Administración de β-lactámicos IV (concentración y %T > CIM) (`ATBInfusion`)
- Bacteriemia en neutropenia febril (`BMDRRN`)
- BOSS-3 (bacteriemia en neoplasia hematológica) (`BacterScores`)
- Meropenem (dosis en TRR) (`MeroPipTazoDosing1`)
- Meropenem y piperacilina/tazobactam, dosis en TRR (`MeroPipTazoDosing`)
- Piperacilina/tazobactam (dosis en TRR) (`MeroPipTazoDosing2`)
- Vancomicina, ajuste de dosis (`VancomycinAUC`)

En TRR se ha recuperado una matriz interna de 96 combinaciones, todavía sin incorporarla como prescripción activa: falta confirmar qué opciones clínicas y unidades corresponden a los índices nativos. Los modelos farmacocinéticos y de aprendizaje automático pendientes no se sustituyen por aproximaciones sin contrastar.

No se trasladaron compras, sincronización, notificaciones, actualización de contenidos, modelos Core ML, recursos gráficos completos, base inglesa, historial ni alertas. La adaptación visual es independiente; notas complejas pueden conservar marcadores internos. Los datos pertenecen a la versión aportada.

## Evidencia proporcionada por el usuario

El usuario confirmó que dispone de un Mac compatible. Aportó recomendaciones textuales de las fichas de meropenem y Tazocel para TRRC y ECMO. Se conservan en referencias-usuario.json como transcripción de referencia: no son menús de las calculadoras ni pares entrada/resultado. No se han recibido aún resultados numéricos de la app completa ejecutándose en Mac. La plantilla casos-original.json permite recogerlos sin datos personales.

Estas comprobaciones técnicas no constituyen validación clínica ni permiten afirmar que la réplica esté completamente terminada.

## Ampliación: resultados de meropenem aportados

El usuario transcribió dos resultados de la utilidad nativa: objetivo estándar, 1–1,5 g/día en infusión continua; objetivo elevado, 3 g/día en infusión continua. Confirmó los objetivos ≥ 2 y ≥ 4–8 mg/L, carga de 1 g en 30 minutos, aviso de umbral de toxicidad de 45 mg/L y opciones de diuresis ≥ 500 / < 500 mL/día. No se indicó qué modalidad, diuresis ni flujo estaban seleccionados para cada salida. Se conservan como observaciones incompletas en meropenem-observaciones-original.json y no se cuentan como comparaciones aprobadas.

Confirmación posterior del usuario: el resultado estándar de 1–1,5 g/día corresponde a TRRC. La diuresis y el flujo de ese caso continúan sin especificar; la confirmación no se extiende al resultado elevado.

Confirmación adicional: caso estándar de meropenem, TRRC, diuresis ≥ 500 mL/día; el usuario indica que no aparece campo de flujo. Resultado 1–1,5 g/día en IC. Coincide con Cal.MeropenemDose1 de la función aislada recuperada, que devuelve esa clave en los tres índices internos de intensidad para esta combinación. Esto aporta un caso original completo según los controles visibles descritos, no valida el módulo entero. Se retira la exigencia de un flujo para este caso concreto.

## Versión web 3: bibliografía y nombres comerciales

Se conserva el orden relativo del contenido y se coloca el campo BIBLIOGRAPHY al final. La comprobación en navegador recorrió todas las fichas de antimicrobianos: las 200 con bibliografía la muestran una sola vez, al final. Las otras 75 no contienen ese campo y no se les inventan referencias.

La búsqueda dispone de filtros por principio activo, nombre comercial y contenido completo. Normaliza acentos, mayúsculas y marcadores de formato. Las presentaciones proceden del campo TRADENAMES. El alias Tazocel para piperacilina/tazobactam procede de la transcripción anterior del usuario; se añade al índice y al resumen de resultados sin modificar las fichas originales. No se afirma cobertura de todas las marcas o países. Se probaron Harvoni, Isentress y Tazocel, selección de resultado, aislamiento del filtro de principio activo y vista móvil de 390 px sin desbordamiento ni errores JavaScript. No se han cambiado los cálculos.

## Versión web 4: presentación y orden clínico

El título MensaGuide pasa de 25 a 100 px en escritorio, con adaptación al ancho en móvil. El menú incorpora bordes redondeados, trama de puntos, degradados y tarjetas azules. Se priorizan D_ADULT, D_CHILD, D_RENAL_FAILURE, EXCRETION, D_HEMODIALYSIS, D_CRRT y D_ECMO, conservando el orden relativo del resto y BIBLIOGRAPHY al final. Se comprobaron las 275 fichas; las 200 con bibliografía la mantienen al final.

El filtro predeterminado es Principio activo; el selector «Buscar como» continúa con Nombre comercial y Todo el contenido. Las marcas se extraen de los marcadores de presentación originales, con soporte para marcas entre asteriscos al inicio de una viñeta, y se conserva el alias Tazocel. Los resultados muestran principio activo (marcas) o marca coincidente (principio activo). Se probaron Ledipasvir/Harvoni, Isentress/Raltegravir, Tazocel/Piperacilina-Tazobactam y Viramune/Nevirapina. Sin errores JavaScript ni desbordamiento horizontal en los cinco anchos documentados en v4-validation.json. Se inspeccionaron capturas de escritorio y móvil. Los cálculos permanecen iguales.

## Versión web 5: nombre alternativo en la ficha

El encabezado situado encima de «Imprimir / PDF» utiliza el mismo criterio que los resultados: principio activo (marcas) al buscar por principio activo, o marca coincidente (principio activo) al buscar por nombre comercial. El nombre alternativo se presenta a continuación del principal y se adapta al ancho disponible. Se conserva al marcar favoritos y en impresión/PDF. Los nombres se obtienen de las presentaciones ya documentadas; no se añadieron marcas ni datos externos en esta entrega. Las fichas sin marcas documentadas no muestran paréntesis vacíos. Ver v5-validation.json para las comprobaciones.

## Actualización de la base a 26.41 (345)

El nuevo archivo aportado contiene MensaGuide 26.41, compilación 345. Se incorpora su base española completa a la interfaz WEB - V5; el encabezado muestra «Actualizado a 10/10/2026» por petición expresa del usuario. Esta fecha de presentación no se deduce de las marcas temporales del ZIP.

Se detectaron cambios en nueve fichas de antimicrobianos: dalbavancina, favipiravir, meropenem, oseltamivir, rifabutina, velpatasvir, zanamivir, anticuerpos monoclonales/plasma de convalecientes y tebipenem. También cambian 28 microorganismos, 12 síndromes, 4 profilaxis y 1 vacuna. Se añade una entrada Candida score, que usa el algoritmo web existente. El total pasa de 1.961 a 1.962 registros. La comparación usa ZUID, o el nombre de abreviatura asociado cuando no existe ZUID, evitando contar reordenaciones de claves SQLite como cambios de contenido.

Se conservaron los identificadores web previos mediante un mapa desde las nuevas claves SQLite; los enlaces internos se reconstruyen con ese mismo mapa. Se compararon 18.875 campos de texto exportados contra la nueva base y se comprobaron todos los destinos de enlaces. La interfaz y el encabezado pasan las comprobaciones de nombres, favoritos, impresión y anchos de 320 a 1440 px sin desbordamiento ni errores JavaScript. No se actualizaron fórmulas web a partir del nuevo ejecutable: las 2.047 pruebas emuladas siguen siendo referencias de 26.40 (344), y se identifican así en la pantalla Verificación. El contenido adjunto se trató como datos.

Los informes data-update-diff.json y data-update-validation.json detallan la comparación y sus límites.
