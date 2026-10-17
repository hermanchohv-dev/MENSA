# MensaGuide para navegador — versión web 4

Descarga `MensaGuide.html` mediante **Download raw file** en GitHub y ábrelo en un navegador moderno. Es un archivo autónomo, sin dependencias remotas para las consultas y los cálculos implementados.

## Interfaz

- Título MensaGuide de 100 px en escritorio (antes 25 px), adaptable al ancho del móvil.
- Menú con marco redondeado, textura suave y tarjetas en tonos azules.
- Fichas ordenadas: dosis en adultos, dosis pediátrica, ajuste de dosis en insuficiencia renal, excreción, hemodiálisis, TRRC, ECMO y resto del contenido. Solo se muestran los campos presentes; la bibliografía queda siempre al final.
- «Buscar como»: **Principio activo** por defecto, **Nombre comercial**, **Todo el contenido**, en ese orden.
- Resultados por principio activo: `Ledipasvir (Harvoni)`. Por nombre comercial: `Harvoni (Ledipasvir)`. Las marcas proceden de las presentaciones originales, más el alias Tazocel aportado por el usuario; no constituyen un catálogo exhaustivo por país.

## Alcance y verificación

Incluye 1.961 registros españoles de MensaGuide 26.40 (344), 88 calculadoras y 11 tablas. Siete módulos de cálculo siguen pendientes. No es una versión oficial ni una réplica completa validada clínicamente.

Se comprobó el orden en las 275 fichas de antimicrobianos, la bibliografía al final en las 200 que la contienen, los dos modos de nombres y la ausencia de desbordamiento horizontal en anchos de 320, 390, 760, 1024 y 1440 px. Detalles en [v4-validation.json](v4-validation.json). No se han modificado los cálculos.

Consulta [LEEME.md](LEEME.md) para el uso y [ANALISIS.md](ANALISIS.md) para el alcance completo. [release-validation.json](release-validation.json) conserva las pruebas de cálculo anteriores y las observaciones aportadas desde la app original.
