# Incorporación del ZIP de imágenes recuperadas

Descarga [MensaGuide-escritorio-PHIL-actualizado.html](MensaGuide-escritorio-PHIL-actualizado.html) mediante **Download raw file**. El archivo autónomo ocupa aproximadamente 56,9 MB e incluye las fotografías para consultarlas sin conexión.

Se examinaron 391 archivos JPEG y sus metadatos del ZIP `Imagenes_PHIL_Microorganismos_recuperados.zip`. Se añaden 76 fotografías distintas: 30 fichas obtienen imagen por primera vez y las demás incorporaciones amplían fichas existentes. Hay 304 fichas con imágenes y 416 referencias fotográficas en total. Las 340 referencias anteriores conservan sus archivos, descripciones y créditos. Quedan 586 fichas sin fotografía: [listado actualizado](Microorganismos-sin-fotografia.txt).

Las fichas con varias imágenes disponen del selector «Fotografía». Las imágenes de lesiones humanas o animales se etiquetan **Manifestación clínica** y se aclara que no son imágenes del microorganismo. Se incluyen, por ejemplo, cultivos de Cardiobacterium, tejidos con Balantioides y Trypanosoma cruzi, micrografías de Helicobacter y HHV-8, fotografías de artrópodos y manifestaciones de infecciones confirmadas en la leyenda.

No se asignan imágenes por el nombre de carpeta. El ZIP contiene numerosas coincidencias erróneas: amebas hospedadoras en mimivirus; tuberculosis en carpetas de otras micobacterias; S. aureus en otros estafilococos; bacterias en priones; además de retratos, personal de laboratorio, vectores e ilustraciones. Tampoco se atribuye una especie cuando la leyenda solo identifica el género. Algunos archivos ya estaban incorporados y se omiten como duplicados. El registro de cada decisión y las leyendas originales están en [phil-recuperados-creditos.json](phil-recuperados-creditos.json).

Cuando la leyenda permite identificar con claridad el organismo y existe una ficha apropiada, se corrige el destino: Treponema vincentii se incorpora a Treponema otras spp; Elizabethkingia meningoseptica a Elizabethkingia; el nombre histórico Eubacterium lentum a Eggerthella; Ochroconis humicola a Ochroconis, no a Humicola; las imágenes de retina infectada por CMV no se asignan a Phoma.

Los JPEG se incrustan sin recortar, retocar, ampliar ni recomprimir. Se conservan autoría, identificador, enlace PHIL y condiciones de uso aportadas, con comprobaciones de dimensiones y hashes. El acceso en línea a CDC sigue bloqueado en el entorno: la identificación se basa en los metadatos suministrados y la revisión visual, sin afirmar una comprobación independiente en PHIL.

La base clínica y los algoritmos no cambian. [recovered-validation.json](recovered-validation.json) documenta la comprobación de imágenes, conservación de la colección previa, búsqueda, filtro, selector, visor ampliado, navegación sin conexión y ausencia de errores JavaScript. Estas pruebas no constituyen validación clínica.
