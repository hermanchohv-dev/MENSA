# MensaGuide — adaptación HTML, segunda entrega

Abre MensaGuide.html en un navegador moderno. El archivo contiene los datos, estilos y código; las consultas y cálculos implementados no requieren conexión. Los enlaces bibliográficos externos sí necesitan Internet. Si tu equipo bloquea archivos HTML locales, sirve esta carpeta con `python3 -m http.server 8000` y abre MensaGuide.html desde ese servidor en el mismo equipo.

Incluye 1.961 registros españoles de MensaGuide 26.40 (344), 88 calculadoras, 11 tablas y una utilidad de consulta textual. La interfaz permite buscar, consultar fichas relacionadas, guardar favoritos e imprimir/PDF. Es una adaptación independiente de la app aportada; no es una versión oficial ni recibe actualizaciones de contenidos.

## Validación y resultados del Mac

En «Verificación» puedes repetir las comparaciones incluidas y descargar una plantilla con diez casos sintéticos. Ejecuta esos casos en la app original, rellena solamente `expected` con su resultado numérico y revisa versión, unidades y método; importa el JSON de nuevo en el HTML para comparar. También se incluye casos-original.json. No contiene datos de pacientes.

Han pasado 2.047 comparaciones con funciones nativas aisladas mediante emulación y 78 casos matemáticos independientes. Esto no equivale a ejecutar la app completa ni constituye validación clínica. Se ha recibido un caso completo de dosis de meropenem en TRRC, concordante con la clave nativa recuperada; quedan pendientes los casos numéricos de la plantilla y el resto de combinaciones de TRR. Algunas herramientas implementadas no reproducen todas las variantes o interpretaciones del original.

## Pendientes

Siete módulos siguen sin cálculo activo: administración de betalactámicos IV, bacteriemia en neutropenia febril, BOSS, las tres utilidades de dosis en TRR y ajuste de vancomicina. No se sustituyen por algoritmos supuestos. En TRR falta confirmar las opciones de flujo y sus unidades, además de resultados originales; las recomendaciones de las fichas no identifican esas opciones.

Consulta ANALISIS.md y release-validation.json para el alcance y las limitaciones. No se ha podido probar aquí la apertura por doble clic: el navegador administrado bloquea file://. Las pruebas usaron HTTP local, sin solicitudes externas ni errores JavaScript en los recorridos comprobados.

## Búsqueda y bibliografía — versión web 3

En Antimicrobianos, selecciona «Nombre comercial» en «Buscar por» y escribe la marca. Selecciona «Principio activo» para limitar la consulta al nombre del medicamento, o «Todo el contenido» para buscar en la ficha completa. Los resultados muestran presentaciones comerciales. Se conservan los nombres disponibles en la versión de la base aportada; se añadió Tazocel como alias facilitado por el usuario, sin cambiar el texto clínico original. La bibliografía se sitúa al final de cada ficha.

## Interfaz — versión web 4

El selector se llama «Buscar como» y presenta Principio activo (predeterminado), Nombre comercial y Todo el contenido. Los resultados muestran el nombre alternativo entre paréntesis: principio activo (marcas), o marca buscada (principio activo). Los nombres se extraen de las presentaciones originales y del alias Tazocel aportado por el usuario.

El título se amplía de 25 a 100 px en escritorio y se ajusta en móvil. El menú tiene un marco redondeado con textura azul. Cada ficha prioriza dosis en adultos, dosis pediátrica, ajuste renal, excreción, hemodiálisis, TRRC y ECMO, después el resto del contenido disponible y finalmente bibliografía. No se inventan secciones ausentes.
