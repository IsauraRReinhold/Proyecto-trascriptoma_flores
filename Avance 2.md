# Avance 2

descargar las secuencias de datos crudos del NCBI en una carpeta especifica para el proyecto

Primero fue necesario instalar toolKit usando los siguientes comandos y así poder descargar los datos crudos del NCBI

Consulte estas páginas

https://trace.ncbi.nlm.nih.gov/Traces/sra/sra.cgi?view=software

https://trace.ncbi.nlm.nih.gov/Traces/sra/sra.cgi?view=toolkit_doc&f=std


```wget ftp://ftp-trace.ncbi.nlm.nih.gov/sra/sdk/current/sratoolkit.current-centos_linux64.tar.gz```

Consulté está página porque no lograba correr el comado de fastq-dump para descargar las secuencias de datos crudos 

https://edwards.sdsu.edu/research/fastq-dump/

https://trace.ncbi.nlm.nih.gov/Traces/sra/sra.cgi?view=toolkit_doc&f=fastq-dump

Probé que funcionara el programa con los comados

```./fastq-dump -X 5 -Z accession number```


Después descargué las secuencias con los comandos del NCBI

Probé el comando abajó indicado y no funcionó del todo 


```./fastq-dump  accession number -X 1000 -Z --split-files .1 .2 --split-files.2 -l -outdir  FM.fastq```


por lo tanto utilice el siguiente

```./fastq-dump accession number -X 1000 -Z outdir .fastq```

Codigos de accesión fueron SRR6958534 (Male flowers) y SRR6958535 (female flowers)

corte las secuencias descargadas con los comandos -X 1000 para solo análizar 1000 debido a la capacidad computacional con la que cuento.

# Pre-procesamiento

## FastQC


Descargué FastQC 

Revisé el manual de FastQC

https://www.bioinformatics.babraham.ac.uk/projects/fastqc/INSTALL.txt


Cuando intente cargar el archivo en fastQC no lo logré, entonces tuve que descargar el archivo completo de las secuencias para ver si así funciona fastQC.

el comando para descargar la secuencias completas es

```./fast-dump --split-files accession code -O nombredeldir.fastq```

con este comando si  logré descargar las secuencias pero el ++fastQC++ no funcionó, entoces lo intenté desde docker.

## Docker

http://www.usadellab.org/cms/?page=trimmomatic

http://manpages.org/trimmomaticpe



Descargue la imange de docker de fastQC


``` docker pull bioicontainers/fastqc ```

monté el volumen de una carpeta llamada fasqc en mis documentos

``` docker run -v/home/isa/Documents/Docker/FastQC:/FastQC -it          
biocontainers/fastqc bin/bash ```

para ver si se habia instalado mi volumen

``` ls ``` 

Para entrar al directorio fastqc 

``` cd fastqc ```

Para ver que hay en fastqc

``` ls ``` 

Para entrar al directorio machos donde se encuentran las secuencias

``` cd manchos ``` 
 
 hacer un list

``` ls ```

SRR6958534_1.fastq  SRR6958534_2.fastq

fastqc SRR6958534_1.fastqc

Obtuve un archivo html dónde pude visualizar la calidad de mis secuencias descargadas.

A partir de lo observado decidí correr trimmomatic usando docker.

##Trimmomatic

Baje la imagen de trimmomatic en docker con

https://hub.docker.com/r/comics/trimmomatic/


``` docker pull comics/trimmomatic ```

monté el volumen

``` docker run -v/home/isa/Documents/Docker/FastQC:/trimmomatic 
-it          
comics/trimmomatic:0:36 bash ```




A partir de la calidad observada en FastQC determiné los parametros a utilizar en el programa Trimmomatic para limpiar las secuencias.

los parametros elegidos fueron:

1. SLIDINGWINDOW 4:28
2. MINLEN:10
3. HEADCROP:10

Intenté hacer el análisis pero hasta hoy no lo he logrado

``` PE [-version] [-threads <threads>] [-phred33|-phred64] [-trimlog <trimLogFile>] [-quiet] [-validatePairs] [-basein <inputBase> | <inputFile1> <inputFile2>] [-baseout <outputBase> | <outputFile1P> <outputFile1U> <outputFile2P> <outputFile2U>] <trimmer1>...```

``` java -jar $TRIMMOMATIC PE -phred33 -trimlog trimlog.txt -quiet -validatePairs -basein SRR6958534_1.fastq SRR6958534_2.fastq pmachos1 pmachos2 SLIDINGWINDOW4:28 HEADCROP:10 MINLEN:10```

Pero me indica que algo está mal

Una vez que logré correr el trimmomatic, haré el ensamble de la secuencia en docker e intentaré hacer un BLAST.









