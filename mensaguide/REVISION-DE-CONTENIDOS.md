# Revisión de contenidos y visualización

Última descarga: [MensaGuide-revision-completa.html](MensaGuide-revision-completa.html), aproximadamente **47,3 MB**. Pulsa **Download raw file** y abre el archivo descargado. Conserva las imágenes ligeras, CIMA, los iconos del menú y el calendario corregido.

Se recorrieron las 1.962 fichas de las ocho categorías. Se compararon 19.333 campos de texto con la SQLite española de la app original 26.41 (345): no hay diferencias. Se compararon también las 12 ediciones publicadas conservadas que comparten esa base; sus textos y tablas de datos permanecen iguales. Esto no equivale a revisar todos los borradores transitorios ni a afirmar paridad completa con la interfaz nativa.

## Omisiones corregidas

| Hallazgo | Alcance | Corrección |
|---|---:|---|
| Calendario vacunal sin representar | 1 ficha | Corrección anterior conservada: tabla original, 55 celdas y 11 notas. |
| Encabezados de columnas de síndromes omitidos | 45 fichas | Se recuperan etiquetas originales como Frecuentes, Menos frecuentes, Bacterias, Virus y otros grupos. Las etiquetas se colocan en su columna correspondiente; no se añaden pautas nuevas. |
| Fórmulas estructurales gráficas excluidas de la conversión inicial | 255 antimicrobianos | Se recuperan los SVG originales, sin modificar sus bytes, en «Fórmula molecular», con visor ampliado. Se mantiene también la fórmula escrita. |

Las restantes referencias de tabla están disponibles: Antisépticos contiene sus 79 celdas, además de las diez tablas derivadas de los campos de antimicrobianos. En síndromes se comprueban las 161 matrices y sus 1.437 celdas de cuerpo, sin pérdidas ni desplazamientos de columna. Los encabezados cuyo valor original es un guion son marcadores sin etiqueta y no generan títulos inventados. Los títulos de vacuna precargados que no tienen texto asociado no se consideran contenido clínico perdido.

Tras la corrección del calendario, el recorrido no detecta otras fichas completamente vacías ni campos de texto presentes en la base pero ausentes de las secciones. Una utilidad con un aviso de función pendiente no se considera una calculadora implementada.

## Utilidades pendientes

Hay 108 utilidades: 88 formularios, 11 tablas, una consulta textual y **ocho calculadoras nativas pendientes**. La documentación histórica de la base 26.40 enumeraba siete; la base 26.41 añadió Candida score. Esta revisión corrige el inventario actual y no simula algoritmos no implementados.

- Administración de β-lactámicos IV (concentración y %T > CIM)
- Bacteriemia en neutropenia febril
- BOSS-3 (bacteriemia en neoplasia hematológica)
- Candida score
- Meropenem (dosis en TRR)
- Meropenem y piperacilina/tazobactam, dosis en TRR
- Piperacilina/tazobactam (dosis en TRR)
- Vancomicina, ajuste de dosis

## Verificación y límites

Las 255 estructuras vectoriales coinciden por hash con los recursos de la SQLite original y se decodifican en Chromium. Se comprueban el visor y su cierre, los encabezados y celdas de las matrices, la conservación de las 621 referencias fotográficas, el calendario, CIMA y los 12 iconos. La navegación con la red desconectada funciona en las pruebas. No se registran errores JavaScript ni solicitudes externas durante la verificación específica.

Se mantienen los datos, las recomendaciones y las fórmulas de cálculo existentes. Estas comprobaciones son de integridad y visualización: no validan clínicamente todos los cálculos ni actualizan recomendaciones. Las anotaciones complejas pueden conservar algunos marcadores de formato del original. La disponibilidad de las páginas de CIMA sigue sin poder comprobarse en línea por el bloqueo de red del entorno.

Evidencia: [informe de revisión](render-audit-report.json), [pruebas de las correcciones](render-fixes-validation.json), [comparación de versiones](version-comparison.json) y [cotejo de recursos originales](original-resource-comparison.json).
