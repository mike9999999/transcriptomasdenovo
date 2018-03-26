Para el ensamblado de transcriptomas *de novo* existen varios programas entre ellos ABySS, SOAPdenovo, Oases, Trans-ABySS y Trinity. Sin embargo, son los dos últimos con los cuales se han obtenido mejores resultados al realizar los ensamblados. 
**Trans-ABySS**
Es un programa capaz de analizar hasta 7.4 Gb en lecturas de 50 pares de bases *pairedend* en poco tiempo y sin consumir mucha memoria. Fusiona todos los contig producidos por el programa ABySS en un conjunto de fragmentos transcritos no redundantes. Trans-ABySS puede predecir sitios de poliadelinación, identificar fusión genica y calcular la expresión del gen. Produce en promedio más isoformas por gen , el método de reconstrucción por múltiples ensamblajes permite reconstruir varios fragmentos.
Sin embargo, es poco eficiente con datos *single end*, produciendo fragmentos de secuencias de transcrito con colas de poly A desde 35pb. 
http://www.nature.com.pbidi.unam.mx:8080/articles/nmeth.1517.pdf

**Trinity**
ES un ensamblador de tres modulos, larva, crisalida y mariposa. Esta modularidad otorga una mayor flexibilidad para extender los pasos de sus ensamblajes, empalme de parálogos; y enumeración y graficación de transcripciones. Permitiendo incluso remplazar algún módulo por otro más eficiente.
Este software sobre otros es que tiene una mejor complementatización y la contiguedad más grande. Produce poca cantidad de isoformas.
Tiene como desventaja que utiliza mucha memoria y el proceso lo realiza en mucho tiempo. 
http://europepmc.org/backend/ptpmcrender.fcgi?accid=PMC3571712&blobtype=pdf
Ambos programas han identificado estructuras conocidas, nuevas y expresiones alternas en transcritos. Ambos son poco sensibles con secuenciaciones de baja profundidad. Con el aumento en la cobertura de las secuencias estos softwares *de novo* se consideran más eficientes que los ensambladores guiados por un genoma.