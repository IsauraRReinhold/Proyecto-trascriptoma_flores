# Avance 3

### Isaura Rosas-Reinhold
## organización del proyecto

Cuando empecé a generar los datos observé que la manera en que yo estaba organizandolos no era la más 

óptima entonces revisé el libro *Bioinformatics Data Skills* de Vince Buffalo, capítulo 2 y capítulo 12.

Hice un script para organizar toda mi información como recomienda Vince Buffalo

## README

Para escribir el README consulté varias fuentes pues aún no me quedaba muy claro que debe contener, algunos solo tienen una linea y otros son más largos, así que revisé lo siguiente:

En este repositorio hay bibliografía muy interesante sobre READMEs https://github.com/matiassingers/awesome-readme 

Otro repo interesante sobre README https://github.com/noffle/art-of-readme

Este es más corto pero igual bueno https://robots.thoughtbot.com/how-to-write-a-great-readme


## Trimmomatic

logré correr trimmomatic, el problema era la versión de java y la versión de trimmomatic que estaba llamando no era la que yo tenía instalada.

instalé trimmomatic-0.36 en mi computadora y descargué java

Probé los comandos y nuevamente me aparecieron varios errores así que consulté https://www.biostars.org/p/271600/
y econtré varias soluciones.

Al final logré correr el análisis

correr trimmomatic desde la línea de comandos con los siguientes comandos

```java -jar trimmomatic-0.36.jar PE -phred33 -trimlog trimlog.txt -quiet -validatePairs -basein SRR6958534_1.fastq umachos1 pmachos1 umachos2 pmachos2 SLIDINGWINDOW:4:28 HEADCROP:10 MINLEN:10```



## Trinity

Revisé el github de trinity

https://github.com/IsauraRReinhold/trinityrnaseq

**Artículos revisados**

*De novo* transcript sequence reconstruction from RNA-Seq:
reference generation and analysis with Trinity (Haas et al. 2013).

Full-length transcriptome assembly from RNA-Seq data
without a reference genome (Grabherr et al. 2011).

Next-generation transcriptome assembly (Martin y Wang, 2011)

Revisé videos en la paǵina https://www.broadinstitute.org/broade/trinity-screencast

En uno de los videos Haas menciona que se puede accesar a la supercomputadora de https://diagcomputing.org/category/software/ 

Ingresé a la página y no logré encontrar dónde registrarme para poder hacer uso y hacer el ensamble, se supone que cualquiera puede tener acceso.

## Acceso al cluster del Instituto de Biología

Realicé el trámite para poder accesar al servidor del instituto de biología


## Ensamble de novo

comandos para realizar el ensamble *de novo*

``` Trinity --seqType fq --left pmachos_1.fq --right pmachos_2.fq --CPU 6 --max_memory 20G ```



