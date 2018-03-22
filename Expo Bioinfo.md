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
*hola*

Extremos simples o extremos pareados
