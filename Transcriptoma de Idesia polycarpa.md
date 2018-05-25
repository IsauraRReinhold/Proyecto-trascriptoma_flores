
# Transcriptoma de *Idesia polycarpa*


## Resumen


- - -


![Ideasia policarpa](https://i.ebayimg.com/images/g/V-QAAOxy~iJQ-6wZ/s-l1600.jpg) 

**Fig. 1**. Frutos de *Ideasia policarpa*



_ _ _
Las flores son una de las estructuras más complejas en las plantas, se originaron a partir de una serie de radiaciones, que comenzaron hacer aproximadamente 130 millones de años (Kramer 2007). Estas estructuras han generado gran fascinación entre los botánicos, includo Darwin quien en 1879 denómino el origen de las angispermas como un abomibale misterio (Friedman 2009). Está fascinación por comprender el origen y desarollo de la flor ha llevado a la generación e implementación de diversos métodos que permitan generar hipotesis sobre su origen principalmente en el campo de la biologia de la evolucion del desarollo o "evo-devo".

Hoy se sabe que las redes regulatorias de los genes de las eudicotiledoneas que dan origen a la flor se encuentrar altamente conservados, indicando que los mecanismos de desarrollo se establecieron probablemente en un momento temprano de la evolución (Alvarez-Buylla et al. 2010, Barllett).

Uno de los principales trabajos enfocados al desarrollo de la flor fue el que determinó el modelo ABC de genes homeóticos porpuesto por Coen y Meyerowitz (1991) en las especies modelo *Arabidopsis thaliana* y *Anthirrinum majus* que han permitido generar hipótesis sobre el origen y desarrollo de la flor. El modelo propone que el dearrollo de cada verticilo se debe a la expresión de ciertos genes que dan origen a cada organo. Cabe mencionar que todos estos genes con excepción de AP2 son miembros de la familia de genes MADS-box.

Aunque hoy en día el modelo ABCE está muy bien comprendido este solo explica la determinación de verticilos florales, pero la diversificación en las flores se debe a la variación que hay entre tamaños, formas(zigomorfas y actinomorfas), colores, número y arreglo de verticilos (Barlett) y son otros genes los que explican estos cambios.

Está fascinación por comprender el origen y desarollo de la flor ha llevado a la generación e implementación de diversos métodos que permitan generar hipotesis sobre su origen principalmente en el campo de la biologia de la evolucion y del desarollo o "evo-devo". La Secuenciación de Nueva Generación (NGS) y en especial el RNA-seq han permitido comprender y generar algunas hipótesis sobre diversificación de las flores a nivel de trasncriptomas.

Actualemente se han publicado un sinumero de artículos referentes al tema como 

_ _ _


![Mapa Idesia](https://github.com/IsauraRReinhold/Proyecto-trascriptoma_flores/blob/master/map_idesia.png)


**Fig. 2**. Mapa de distribución de *Idesia polycarpa*


_ _ _
### *Idesia polycarpa*


*Ideasia polycarpa* var. *vestitas* es una especie que pertenece a la familia Salicaceae, y fue descrita  en 1866 por Maximowicz (http://www.tropicos.org/). Se distribuye de manera natural en el Este de Asia, principalmente en China, Corea, Japón y Taiwan (https://www.gbif.org/species/6043516), aunque también hay presencia de la especie en Nueva Zelanda, Alemania, Suiza, Georgia y Estados Unidos en jardines botánicos y parques (Fig. 2.).

Idesia polycarpa es una planta arborescente que mide de 8-21 m de alto, con corteza grisacea, hojas coriaceas y margenes aserrados. Las flores son unisexuales, color verde amarillento; el fruto es una baya púrpura-rojo o naranja-rojo cuando está maduro (Fig. 1). Florece entre abril y mayo. los frutos maduran de Octubre a Noviembre. Crece entre 300-4000 msnm y se cultiva principalmente con fines hornamentales (http://www.efloras.org). Sin embargo ha adquirido importancia económica debido a su potencial uso como fuente de aceites para biocombustibles y lubricantes (Mei et al. 2017).

Debido a que esta especie alcanza su madurez a los 4-5 años y solo hasta ese momento se puede definir el sexo de la planta, y ya que solo las flores femeninas producen los frutos de interés económico es necesario buscar estrategias que permitan sexarlas antes de que alcancen su estapa madura y así poder hacer una mejor explotación del recurso.

Por está razón Mei et al. (2017) generaron transcriptomas tanto de flores hembra como de machos en diferentes estadios de desarrollo con la finalidad de determinar la presencia de genes y cambios en patrones de expresión que puedan indicar el sexo de la planta.

Para el desarrollo de este proyecto se utilizó unicamente uno de los seis transcriptomas que están publicados para esta especie en NCBI. También se utilizó la base de datos de distribución del género que fue descargada de GBIF y con ella se generó un mapa utilizando Rstudio (Fig. 2), también se generó una gráfica de barras para representar los paises con mayor porcentaje de reportes de la especie (Fig. 3)

En este trabajo se presentan el preprocesamiento de las secuencias macho estadio medio descargadas desde NCBI y un mapa de distribución generado con la base de datos del GBIF. Se había planteado realizar el ensable y la notación de algunos genes, sin embargo, instalar algunos programas y la capacidad computacional resulto ser más dificil de lo pensado.

![Bar plot Idesia](https://github.com/IsauraRReinhold/Proyecto-trascriptoma_flores/blob/master/barplot_idesia.png)

**Fig. 3**. Presencia de *Idesia polycarpa* (CN=China,JP=Japón,NZ= Nueva Zelanda, TW=taiwan, US=Estados Unidos, DE=Alemania, GE=Gerogia, SE=Suiza) El país que presenta mayor porcentaje de datos para la especie es China, seguido de Japón, Taiwan y Nueva Zelanda.




- - -


_ _ _

### Discusión y Conclusiones


La **descacarga** de las secuencias desde el NCBI fue en un principio complicado y confuso, aunque revisé la página y descargue el programa no lograba realizar la descarga, tuve que repetir varias veces y cambiando los comandos hasta que resolví el problema.


Por otra parte, la instalación de los programas no es algo tribial, estamos acostubrados a descargar y listo, sin embargo durante el desarrollo de este proyecto pude darme cuenta que el lugar dónde descargas un programa es importante, además a veces es necesario descargar varios programas más para lograr correr el de interés. Fue así que tuve varios problemas al descargar e instalar mal los programas, varias veces no funcionaron y tuve que repetir la operación. 


El **manejo de datos**


**Capacidad computacional**. Cuando plantie el proyecto para la materia se me hizo muy sencillo pensar en todo lo que quería hacer y descargar, sin embargo al pasar los días me di cuenta que no tenía la capacidad computacional para resolverlos, el tener acceso al cluster de una supercomputadora es esencial, además de que este tiene que tener un soporte correcto para poder realizar los análisis en tiempo y forma. El cluster del LANCIS permite el acceso para llevar a cabo los proyectos bioinformaticos, pero para tener acceso hay que llevar a cabo diferentes procedimientos burócraticos que no tenía contemplados.



**Bitacora en Haroopad**. Un tema que es de suma importancia y que pude constatar durante el desarrollo del proyecto es el de tener todo detalladamente escrito y reportado, no fue una sino varias las veces que tuve que recurrir a los avances tipo diario redactados, ya que en ellos estaba tanto los problemas como las soluciones ante cierta situación. Por ejemplo, tuve que descargar las secuencias dos veces y gracias a que ya tenía escrito como hacerlo me evité volver a hacer todo de manera engorrosa como la primera vez. 


Los scripts son importantes pero a veces estos no son suficientes por lo tanto es necesario tener un diario que nos permita regresar en nuestros pasos para saber como resolver un problemas


**README**. Escribir un buen README no es fácil, además de que sirve para que otros sepan de que va nuestro trabajo nos sirve a nosotros para saber que hay en las diferentes carpetas que vamos generando, ahora creo indispensable escribir READMEs en cada uno de los proyectos que desarrolle y que se encuentre en las carpetas de datos correspondientes para así saber que hay y que algún día pueda entender que quise hacer y porque están los datos donde estan.


![Flores]
(http://ketenewplymouth.peoplesnetworknz.info/image_files/0000/0001/5664/Idesia_polycarpa_Maxim__ligiri_tree-1.JPG)



Por otro lado la revisión de Blogs, grupos de discusión, repositorios, manuales, fueron de suma relevancia durante el desarrollo del proyecto, ya que con ellos logré resolver diferentes problemas, además de que me sirvió para darme cuenta que en ellos ya están planteadas y resueltas muchas preguntas que tuve para poder llevar a cabo el proyecto, aunque no logré todos lo objetivos planteados a pesar de revisar todas las fuentes, estos recursos me dieron una idea de todo lo que uno puede hacer.


Como vimos durante el curso, la información esta en la red, sólo hay que saber buscarla y utilizarla, a mi se me complico en un principio entender los tutoriales de los progrmas, el lenguaje era ageno a mis conocimientos, por suerte también hay bastan información básica que permite ir accesando poco a poco.


El desarrollo de este trabajo fue muy importante porque me hizo darme cuenta que realizar un proyecto bioinformatico va mucho más allá de obtener el RNA de buena calidad y ensablar secuencias, conlleva mucho esfuerzo y que a veces no consideramos cuando planteamos nuestro proyecto. También me di cuenta que es fácil caer en la frustración y desesperación al no poder llevar a cabo uno de los pasos para continuar el o los análisis, pero siempre hay ayuda en algún sitio para resolver el problema.


Aunque no logré obtener todo lo que hubiera querido para presentar en el proyecto aprendí mucho, es necesario dedicar tiempo a revisar manuales, blogs, artículos para poder aprender el uso de los programas de manera correcta, su instalación y requerimentos computacionales.


Otro de los temas que me pareció más interesante durante el desarrollo del trabajo fue la reproducibilidad, el aprender a escribir todo, a documentar cada paso es sumamente relevante, primero para que nosotros podamos repetir nuestros experimetos pero también para dar certeza de que ellos se realizaron de la manera más correcta y por lo tanto podamos validar nuestros resultados











