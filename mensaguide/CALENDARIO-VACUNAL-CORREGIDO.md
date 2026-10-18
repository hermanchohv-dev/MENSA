# Corrección del calendario vacunal vacío

Descarga [MensaGuide-calendario-corregido.html](MensaGuide-calendario-corregido.html) con **Download raw file**. Mantiene la versión ligera, los iconos del menú y los enlaces CIMA.

La ficha «-Calendario vacunal» no contiene texto convencional: su campo TITLE11 remite a `#table:child_vac_cal`. El HTML omitía los campos TITLE al generar las secciones y solo interpretaba referencias de tabla en las utilidades; por eso la ficha aparecía vacía aunque la tabla estuviera incluida en el archivo.

Se ha comprobado la base española de la app original aportada: `MensaGuide.app/Contents/Resources/data.sqlite`. Contiene 55 celdas no vacías de esa tabla. Ahora se muestran las 10 filas de vacunas y 15 columnas de edad o embarazo, con 11 notas desplegables. La cabecera y los nombres de vacunas permanecen visibles al desplazar la tabla. El botón «Abrir todas las notas» facilita la consulta, y las notas se abren al imprimir y recuperan después su estado anterior.

Se reproduce el contenido de la app original 26.41 (345), identificado como tal. No se ha sustituido por un calendario externo ni se han actualizado sus pautas clínicas. Las abreviaturas se explican como meses, años y embarazo. Las celdas originales quedan registradas en [calendario-original-celdas.json](calendario-original-celdas.json).

Se verificaron las 55 celdas frente a la SQLite original y su posición en el navegador, las notas, la conservación del contenido de la base y las imágenes, la consulta sin conexión y los enlaces CIMA e iconos del menú. No se observaron errores JavaScript ni desbordamiento de página en la vista de escritorio. Se comprobó la apertura y restauración de notas mediante los eventos de impresión; no se verificó un PDF exportado. Detalles en [calendar-validation.json](calendar-validation.json). Código incorporado en [calendar-fix.js](calendar-fix.js).
