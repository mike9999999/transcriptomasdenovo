Isaura Rosas Reinhold
Melania Vega


##Transcriptomas

##Ensamblado *de novo*

1. ¿Cuáles son las principales variantes del método de laboratorio para generar mis datos y cuándo es más util cada una?
2. ¿Qué limitantes y posibles fuentes de error puede presentar este método (en el laboratorio o la bioinformática)? ¿Qué puede hacerse para amortiguarlos?
3. ¿El muestreo requiere algún diseño específico? Por ejemplo, si se quiere secuenciar un genoma de novo ¿qué individuo sería ideal? Si trabajo con trascriptomas, ¿cómo afecta el tejido, la edad, las condiciones, etc. mi muestreo?
4. Menciona al menos dos softwares principales que se utilicen para realizar la parte medular de los análisis bioinformáticos de este tipo de análisis (e.g. si es ensamblado de novo con qué se ensambla, no con qué se hace el pre-procesamiento) y cuáles son los pros y contras de cada uno.


##Qué preguntas podemos responder con el uso de transcriptomas
###Principales variantes del método de laboratorio
####Muestreo
######Grupo de estudio y tejido

Los experimentos y las estrategias de análsis dependen del organismo a estudiar y las metas de la investigació

Cada escenario experimental del RNA-seq potencialmente puede tener diferentes metodos optimos para la cuantificación de la transcripción, normalización y análisis de expresión diferencial. Además diferentes controles de calidad deben aplicarse en los diferentes estado del análisis para asegurar tanto reproduciblidad como confiablidad de los resultados.

==Un prerrequisito crucial para tener un estudio exitoso con RNA-seq es que los datos generados tengan el potencial de responder la pregunta de interés==.

####Diseño experimental

Es necesario contar con un buen diseño experimental, lo que nos llevará a un buena elección del tipo de biblioteca, profundidad de secuenciación y número de replicas para el sistema biologico que esta en estudio, y segundo con una buena planeación y adecuada ejecucuón de la secuenciación, aseguramos que los datos no estaŕan contaminados.

Un paso crucial en el diseño experimental es el protocolo de extracción usado para remover las grandes cantidades de RNA ribosomal (rRNA) que constituye el 90% del total del RNA en la célula, dejando unicamente el 1-2 % de RNA mensajero que es el de interés normalmente.

Para EUryotas**
esto involucra la elección del enriquecimiento usando poli(A) o deplete RNA. El primero por lo general requiere de grandes cantidades de RNAm con una minímia degradación. Comunmentes las muestras biologicas relevantes no se puede obtener grandes cantidades de RNAm y tampoco de buena calidad para producir librerias poli (A) y entonces se prefiere ribosomal depletion.

En el caso de las **bacterias** dónde el RNAm no esta poliadenilado la unica alternativa viable es la ribosomal depletion.

#####Número de replicas

tres factores determinan el número de replicas requeridas en un experimento de RNA-seq
a) variabilidad en las mediciones, las cuales son influenciadas por el ruido tecnico y la variación biológica. mientras la reproducibilidad en RNA-seq es usualmente alta a nivel de secuenciación, otros pasos tales como la extracción y preparacion de bibliotecas son ruidosas y pueden introducir sesgoen los datos que pueden ser minimizados adoptando  buenos procedimientos experimentales.
b)La variabilidad biológica es particular en cada sistema experimental y dificl de controlas, sin embargo replicas biológicas son necesarias si se quieren hacer inferencias a nivel de población, con tres réplicas como minimo por cada análisis. Para un adecuado análisis estadistico , estimar la varianza entre grupos y niveles de expresión genetica son necesarios.
c)
**hola**

Extremos simples o extremos pareados




####################################################    MIKE   ########################################################################
#################################################### RESUMEN   ########################################################################
##INTRODUCCIÓN

El ensablado de novo para genomas y transcriptomas consiste en la conformación de secuencias coherentes a partir de los
datos del secuenciador cuando no existe un genoma de referencia con el cual comparar los datos de la secuenciación. 

En particular la secuenciación de genóma se centra en un estudio amplio del DNA en un organismo para conocer mutaciones, SNP´s, allelos, 
secuencias repetidas en tandem, genes, elementos nucleares, secuencias codificantes y no codificantes. Mientras que, el estudio de secuenciación de novo de transcriptooma 
se centra en el estudio dinámico de la expresión genómica cuantificable y también en el análisis de variantes, splicing y de algunas secuencias no codificantes.

Se debe tomar en cuenta El objetivo claro del estudio.
Tipo de medición (RNA-DNA).
Tipo de tecnología.
Tipo de factor o muestra.
Características de la muestra.


##ENSAMBLADO 

Ensamblado de novo de genóma

Consiste en a) Designación del experimento y sobrelapamiento de reads y conformación-ensamblado de contings. b) generación de scafoldings. c) Rellenado de huecos entre scafolds. d) Generación de 
borradores parciales del genóma en cuestión.

Ensamblado de novo de transcriptoma

Este proceso consiste en  a) Designación experimental, generación de bibliotecas y secuenciación. b) análisis de control de calidad y filtrado de reads. c) Ensamblado de
novo mediante software como: velver, Oases, SPAdes, Trinity o BinPacker. Estos software generalmente utiliza para generar el ensablado los algoritmos o métodos:

OLC: Overlap-Layout-Consensus assembly
DBG: De Bruijn graph assembly

Para el ensamblado de transcriptoma de novo sin genoma de referencia existe una diversidad amplia en software:

Velvet/Oases (2008): Ambos software generan ensablado de novo de transcriptoma a partir de pair-end cortos. También, generan analisis de scplicing, sin embargo para realizar analisis adicionales, requieren de actualizaciones.

SPAdes (2012): este software genera ensamblado de novo en una amplia variedad de especies y tamaños de transcriptomas, además puede generar análisis de expresión.

Triniti: este softeare fué liberado en 2013 y los análisis de ensamblado son realizados mediante la utilización de 3 paquetes que se ejecutan de manera independiente. Ichworm, admite los reads del experimento de secuenciación en transcritos. Chrysalis, ensambla los transcritos y genera gráficas Buijin, mientras que Butterfly analiza los gráficos y genera transcritos completos.
Además triniti brinda  métricas de calidad de ensamblado y ensayos. En particular para transcritptoma exmina con la metrica de “exN50” (top de transcritos que representan el 50% del transcriptoma).

BinPacker ( 2016): este software contruye transcritos, incorpora información de la covertura y genera análisis de splicing. En específico este sistema profundiza en los análisis de splicing y su ensamblado.

Nota: Todos lo software anteriores utilizan entre sus herramientas, el algoritmo Bruijn Graph, que consiste en el traslape de reads para contruir transcritos o cadenas.



Ejemplo de triniti.

TRINITY
http://evomics.org/learning/genomics/trinity/
https://github.com/Jaiswal-lab/Transcriptome_Assembly_Scripts.git

Trinity --seqType fq --left <left_reads> --right <right_reads> --output test-trinity-cotton 
## where --seqType is read type "fq" fastq or "fa" fasta
## where --left is name and location of left reads
## where --right is name and location of right reads
## where --output is the name and location output

Ejemplo: Basic Trinity usage is as follows:

Trinity.pl --seqType (fq for fastq or fa for fast) --left ~/path/to/reads_1.fq --right ~/path/to/reads_2.fq (or --single for single reads) --CPU 4 --bflyHeapSpace 10G --output ~/path/to/output_dir

NOTE: It is recommended to use fully specified paths for sequence files with Trinity.



##EVALUACIÓN DE ENSAMBLADO

El análisis posterior es la evaluación del ensablado donde se analizan métricas como N50 o exN50.

softwares:

BLAST

rnaQUAST

Transrate

CD-HIT-EST


##PERSPECTIVAS

Disminición en la tasa de errores (Pacbio).

Dsitinguir contaminación.

disminución de costo para un mayor estudio de organismos específicos.






