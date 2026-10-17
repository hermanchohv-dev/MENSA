# Propuesta de interfaz para valorar

Descarga [MensaGuide-interfaz-prueba.html](MensaGuide-interfaz-prueba.html) con **Download raw file**. Es un archivo autónomo. [MensaGuide.html](MensaGuide.html) conserva la entrega anterior para comparar.

## Cambios

- **Menú móvil plegable:** cerrado al inicio, botón «Menú de secciones», cierre al seleccionar una sección o pulsar Escape. En escritorio, la navegación sigue visible.
- **Índice por medicamento:** «En esta ficha» enlaza a todas las secciones presentes. Abre la sección elegida, sitúa el contenido debajo de la cabecera y conserva la ruta de la ficha. El índice aparece abierto en escritorio y plegado al abrir una ficha en móvil.
- **Secciones plegables:** dosis en adultos, dosis pediátrica y ajuste renal abiertas inicialmente, cuando existen. El resto cerrado. «Abrir todas» y «Cerrar todas» controlan la ficha; los títulos funcionan también con el teclado.
- **Cabecera compacta:** al desplazarse reduce el título y permanece accesible; al volver al inicio recupera su tamaño. Se reserva su espacio original para evitar saltos del contenido.
- **Impresión:** despliega todas las secciones temporalmente y recupera su estado después de imprimir, para que no se omita contenido por estar plegado.

## Comprobaciones

La base incorporada es idéntica a la entrega anterior: MensaGuide 26.41 (345), fecha de encabezado 10/10/2026. Se compararon los textos renderizados y el orden de secciones de los 275 registros de antimicrobianos. No se cambiaron contenidos clínicos, nombres comerciales ni cálculos. Se mantienen las limitaciones funcionales y de validación documentadas previamente.

Se probaron el menú móvil, Escape, selección de sección, índice, navegación por teclado, apertura/cierre, estado de impresión, cabecera y anchos de 320, 390, 760, 1024 y 1440 px. Sin desbordamiento horizontal ni errores JavaScript. Informe: [usability-review-validation.json](usability-review-validation.json).
