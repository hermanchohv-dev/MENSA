# MensaGuide — herramientas para escritorio

Descarga [MensaGuide-escritorio.html](MensaGuide-escritorio.html) con **Download raw file** y ábrelo en un navegador moderno. Es autónomo y conserva los datos 26.41 (345), fecha de encabezado 10/10/2026. Las entregas anteriores siguen disponibles para comparar.

## Funciones

1. **Índice lateral fijo por medicamento.** A partir de 1100 px de ancho permanece visible al desplazarse y resalta la sección en lectura. Los enlaces despliegan la sección elegida.
2. **Comparación de dos medicamentos.** Entra desde «Comparar fármacos» o «Comparar con otro fármaco» en una ficha. Admite principios activos y marcas exactas; si una marca identifica varias fichas solicita el principio activo. Las columnas reproducen textos originales, con dosis, ajuste renal, excreción, diálisis e información restante alineadas. La bibliografía queda al final. «No consta» indica un campo ausente; no se combinan recomendaciones ni se calculan equivalencias. Puede imprimirse la comparación.
3. **Volver a resultados.** Conserva término, tipo de búsqueda, número de resultados desplegados y posición de desplazamiento durante la navegación de la sesión. No persiste ese contexto al recargar el HTML.
4. **Perfiles de lectura.** Vista inicial abre dosis adulta, pediátrica y ajuste renal. Ficha completa abre todo. Posología abre los campos de dosis. Función renal y TRR abre ajuste renal, excreción, hemodiálisis, TRRC, ECMO, diálisis peritoneal y los parámetros farmacocinéticos disponibles. Los demás apartados permanecen accesibles, plegados.
5. **Búsqueda dentro de la ficha.** Resalta palabras o frases sin distinguir mayúsculas o acentos. «Anterior», «Siguiente» y Enter recorren los resultados; Mayús+Enter retrocede. Abre las secciones cerradas que contienen la coincidencia. Busca en los textos de sección; no une una frase repartida entre nodos de formato distintos y limita el resaltado a las primeras 1000 coincidencias.
6. **Historial local.** Guarda los diez últimos medicamentos, sin duplicados, en ese navegador cuando permite almacenamiento local. Incluye «Borrar historial». Está separado de favoritos.
7. **Impresión selectiva.** «Imprimir / PDF» permite marcar secciones. Todas se seleccionan inicialmente. Incluye identificación del medicamento, versión y fecha de los datos. La bibliografía se incluye si se selecciona. Restaura el estado plegado tras imprimir o cancelar. La impresión directa del navegador imprime toda la ficha; utiliza el botón para elegir secciones.

## Comprobaciones

La base DB es idéntica a la anterior. Se compararon el texto renderizado y el orden de las secciones de los 275 antimicrobianos. Los textos de ambas columnas de comparación también coinciden con sus fuentes. No se cambiaron cálculos ni contenido clínico. Persisten los siete módulos de cálculo pendientes y los límites de validación anteriores.

Se comprobaron regreso a resultados con posición, perfiles, resaltado y navegación de coincidencias, índice activo, historial persistente y borrado, selección de impresión y restauración, marcas ambiguas y comparación de medicamentos diferentes. Se generó un PDF real con una única sección y se comprobó que contiene el medicamento y la fecha, sin incluir la sección pediátrica no seleccionada.

Pruebas en Chromium a 1280, 1440 y 1920 px sin desbordamiento horizontal ni errores JavaScript. Informe: [desktop-review-validation.json](desktop-review-validation.json). Esta entrega se centra en escritorio; no añade desarrollo específico para teléfono.
