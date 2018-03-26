1. ¿Cuáles son las principales variantes del método de laboratorio para generar mis datos y cuándo es más útil cada una?

2. ¿Qué limitantes y posibles fuentes de error puede presentar este método (en el laboratorio o la bioinformática)? ¿Qué puede hacerse para amortiguarlos?

3. ¿El muestreo requiere algún diseño específico? Por ejemplo, si se quiere secuenciar un genoma de novo ¿qué individuo sería ideal? Si trabajo con trascriptomas, ¿cómo afecta el tejido, la edad, las condiciones, etc. mi muestreo?

4. Menciona al menos dos softwares principales que se utilicen para realizar la parte medular de los análisis bioinformáticos de este tipo de análisis (e.g. si es ensamblado de novo con qué se ensambla, no con qué se hace el pre-procesamiento) y cuáles son los pros y contras de cada uno

Transcriptoma: conjunto de transcritos en una célula en una muestra biológica para un estadío específico de desarrollo o una condición biológica.


Las variantes del método de laboratorio está en función, principalmente, del organismo con el que se esté trabajando y la pregunta de investigación a responder.

## ¿qué preguntas pueden responderse con el uso de transcriptomas?

- Médicas
- Evolutivas (Eco-evo-devo)
- Industria
-
- Genes candidatos
- codificación de proteínas
- perfiles de expresión génica
- detección de RNA no codificante
- descubrimiento de arreglos del transcripto
- variación de nucleótidos
- elementos transponibles (al comparar con adn nuclear)
- patrones de expresión génica - función de órganos homólogos, bases moleculares de la inovación morfológica, convergencias
- diversificación
- alteraciones epigenéticas



## Muestreo
##### grupo estudiado
##### y tejido usado -- congelar inmediatamente
##### errores comunes elección de tejido en los que no se encuentren las expresiones, hora, fases de desarrollo

## Método de extracción
##### molida -- no fragmentar tanto cuando estamos buscando genomas completos o estamos haciendo el ensamble de novo.
##### limpieza debido a que trabajamos con RNA, qué productos usar?
##### congelación hielo seco o nitrógeno -- porque al aumentar la temperatura las RNAsas se activan
##### medir cantidad de RNA -- qubit @[link manual] (https://tools.thermofisher.com/content/sfs/manuals/qubit_3_fluorometer_man.pdf)
##### plantas
puedes usar Kit o método trizol
##### errores comunes contaminación, degradación, poca cantidad de RNA y muestras sucias
solo el 1-2% es RNAm que es el de interés

## Realización de librerías
###Amplificación
#### cDNA
Para hacer la librería dos métodos principalmente colas de poliA o ribodepletion el primero resultó más eficiente al mostrar la expresión de los genes y al hacer el alineamiento.Se pusieron a prueba en ![link artículo](http://www.rna-seqblog.com/poly-a-selection-or-ribo-depletion/)
![link imagen ejemplo] (http://media.springernature.com/full/springer-static/image/art%3A10.1186%2Fs12864-017-4039-1/MediaObjects/12864_2017_4039_Fig1_HTML.gif)
Para ver las variaciones técnicas consultar ![link artículo](https://bmcgenomics.biomedcentral.com/articles/10.1186/s12864-017-4039-1)
quitar el RNA ribosomal con ¿ se hace en la extracción o aquí? 
ribodepetion resulta una buena opción para RNA degradado
poliA tiene mejor desempeño que el RD para detectar expresión diferencial de genes

## Secuenciación
Secuenciación simple o extremos pareados (especial para de novo). Es importante que tengamos 3 réplicas.
Plataformas empleadas y características Illumina o SOLid
Se prefiere el uso de dos más enzimas para obtener fragmentos de diferentes tamaños y poder obtener mayor cobertura
Un factor importante es la profundidad de la secuenciación o el tamaño de la librería (veces de lecturas por muestra, 5-100 millones de lecturas por secuencia son suficientes)

## Manejo de datos
Remover las secuencias de los adaptadores y los low-complexity reads derivados de la PCR
Los errores en la secuenciación pueden ser removidos a través de un análisis de cualidad cons FASTQC o un k-mer frequency
Analizar calidad a través del contenido de CG
#### Programas utilizados 
![link imagen]



