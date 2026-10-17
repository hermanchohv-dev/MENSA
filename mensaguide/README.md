# MensaGuide para navegador — versión web 5

Descarga `MensaGuide.html` mediante **Download raw file** en GitHub y ábrelo en un navegador moderno. Es un archivo autónomo, sin dependencias remotas para las consultas y los cálculos implementados.

## Interfaz

- Título MensaGuide de 100 px en escritorio (antes 25 px), adaptable al ancho del móvil.
- Menú con marco redondeado, textura suave y tarjetas en tonos azules.
- Fichas ordenadas: dosis en adultos, dosis pediátrica, ajuste de dosis en insuficiencia renal, excreción, hemodiálisis, TRRC, ECMO y resto del contenido. Solo se muestran los campos presentes; la bibliografía queda siempre al final.
- «Buscar como»: **Principio activo** por defecto, **Nombre comercial**, **Todo el contenido**, en ese orden.
- Resultados por principio activo: `Ledipasvir (Harvoni)`. Por nombre comercial: `Harvoni (Ledipasvir)`. Las marcas proceden de las presentaciones originales, más el alias Tazocel aportado por el usuario; no constituyen un catálogo exhaustivo por país.

## Alcance y verificación

Incluye 1.962 registros españoles de MensaGuide 26.41 (345), 88 calculadoras y 11 tablas. Siete módulos de cálculo siguen pendientes. No es una versión oficial ni una réplica completa validada clínicamente.

Se comprobó el orden en las 275 fichas de antimicrobianos, la bibliografía al final en las 200 que la contienen, los dos modos de nombres y la ausencia de desbordamiento horizontal en anchos de 320, 390, 760, 1024 y 1440 px. Detalles en [v4-validation.json](v4-validation.json). No se han modificado los cálculos.

Consulta [LEEME.md](LEEME.md) para el uso y [ANALISIS.md](ANALISIS.md) para el alcance completo. [release-validation.json](release-validation.json) conserva las pruebas de cálculo anteriores y las observaciones aportadas desde la app original.

## Encabezado de la ficha — versión web 5

Al abrir un medicamento desde una búsqueda por principio activo, el encabezado muestra `Ledipasvir (Harvoni)`. Si se busca por nombre comercial, muestra `Harvoni (Ledipasvir)`, incluyendo la marca coincidente. El nombre alternativo aparece junto al principal, encima de «Imprimir / PDF», y se conserva en la impresión. En pantallas estrechas puede pasar a la línea siguiente. Las fichas sin marcas documentadas conservan su nombre sin paréntesis vacíos.

Se probaron ambos modos, favoritos, impresión y móvil sin errores JavaScript. Detalles en [v5-validation.json](v5-validation.json). No se modificaron datos clínicos ni cálculos.

## Actualización de datos — 10/10/2026

Se incorporó la base española de la nueva app aportada, versión 26.41 (345). La interfaz conserva «WEB - V5» y muestra a su derecha «Actualizado a 10/10/2026», según la fecha solicitada por el usuario.

La comparación por identidad estable detecta cambios de texto en 9 antimicrobianos, 28 microorganismos, 12 síndromes, 4 profilaxis y 1 vacuna, más una nueva entrada de utilidad Candida score. El nuevo total es 1.962 registros; la nueva entrada reutiliza la calculadora CandidaScore ya implementada y no aumenta el número de algoritmos. Se preservan los identificadores de las fichas existentes para mantener enlaces y favoritos.

Se comprobaron 18.875 campos de texto contra la nueva SQLite, todos los destinos de enlaces internos y la presentación móvil. Las 2.047 comparaciones de funciones nativas siguen pasando como regresiones de 26.40: no constituyen una nueva validación del ejecutable 26.41. Los cálculos web no se han modificado. Véanse [data-update-diff.json](data-update-diff.json) y [data-update-validation.json](data-update-validation.json).

## Propuesta de interfaz para valorar

Disponible por separado en [MensaGuide-interfaz-prueba.html](MensaGuide-interfaz-prueba.html): menú móvil plegable, índice por medicamento, secciones plegables y cabecera compacta al desplazarse. La versión anterior sigue en MensaGuide.html. Consulta [INTERFAZ-PRUEBA.md](INTERFAZ-PRUEBA.md) para los detalles y la verificación.

## Herramientas de escritorio

Nueva entrega independiente: [MensaGuide-escritorio.html](MensaGuide-escritorio.html). Incorpora índice lateral fijo, comparación de dos fármacos, regreso a resultados conservando contexto, perfiles de lectura, búsqueda resaltada dentro de la ficha, historial e impresión selectiva. Detalles de uso y pruebas en [ESCRITORIO.md](ESCRITORIO.md) y [desktop-review-validation.json](desktop-review-validation.json). El contenido clínico y los cálculos permanecen iguales a la entrega anterior.

## Escritorio con fotografías de microorganismos

Nueva descarga: [MensaGuide-escritorio-fotos.html](MensaGuide-escritorio-fotos.html). Conserva todas las herramientas de escritorio e incorpora una colección inicial de 18 imágenes en miniaturas y fichas, con visor ampliable y uso sin conexión. El filtro «Solo con fotografía» permite encontrarlas. Las demás fichas muestran que la imagen no está disponible. Créditos, licencia y cobertura en [FOTOGRAFIAS-MICROORGANISMOS.md](FOTOGRAFIAS-MICROORGANISMOS.md).

## Búsqueda en libros aportados

[Catálogo de imágenes localizadas en el Atlas de parasitología](IMAGENES-LOCALIZADAS-ATLAS.md): 33 fichas adicionales con candidatas, páginas y figuras. Esta entrega localiza imágenes; no incorpora ni publica las fotografías del libro y no cambia los HTML anteriores. Los PDF de Botero y Spicer superan el límite de transferencia de 32 MiB y siguen sin examinarse.

## Color Atlas of Diagnostic Microbiology, partes 1 y 2

Ambos archivos se pudieron abrir. [Catálogo de imágenes localizadas](IMAGENES-LOCALIZADAS-DIAGNOSTICO.md): 68 fichas sin imagen actual con candidatas identificadas por parte, página y figura (29 bacterias, 25 hongos, 6 virus y 8 parásitos). Datos estructurados en [diagnostic-atlas-candidates.json](diagnostic-atlas-candidates.json). Se añade la localización, sin modificar el HTML ni republicar imágenes de los PDF en esta entrega.
