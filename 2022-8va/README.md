---
title: Minuta de la 8a. Reunión Anual GArCyAR 2022
author: Héctor Lestani
thanks: Agradecimientos por la ayuda en la organización a: A. Weir, R. Zalazar, Z. Prieto, D. Ferraro, G. Theler}
date: 2022-12-26
...


> En GArCyAR queremos pasar al siguiente paso.
> El Grupo Argentino de Cálculo y Análisis de Reactores quiere aportar mediante la cooperación de sus miembros, apuntando a resolver problemas que tengan un impacto positivo en la industria nuclear argentina; que si un calculista tiene una dificultad pueda encontrar eco y respuestas en esta comunidad; que sigamos respetando las reglas y restricciones de las instituciones a las que pertenecemos pero que, conscientes de que somos pocos, podamos proyectarnos en conjunto. Ya hemos logrado realizar reuniones periódicas mostrando nuestras capacidades y recibiendo aplausos y palmaditas en la espalda, pero podemos más, podemos además ser un foro de cooperación.
> Es en ese espíritu de apertura que esta primera _Minuta de la 8a. Reunión Anual_ recibirá el aporte de sus participantes a través de la cuenta de [_GArCyAR_ en GitHub](https://github.com/GArCyAR).
> Para realizar aportes, correcciones, comentarios, dirigirse a <https://github.com/GArCyAR/reuniones>.^[Agradecimientos por la ayuda en la organización a: A. Weir, R Zalazar, Z. Prieto, D. Ferraro, G. Theler]


El 5 de diciembre llevamos a cabo la 8a. Reunión Anual del Grupo
Argentino de Cálculo y Análisis de Reactores, con el siguiente
[cronograma](https://nube.cnea.gob.ar/index.php/s/a8Jn84TpLYyGj99). En
esta minuta se enumeran las presentaciones realizadas y se ponen a
disposición enlaces para bajar los archivos.

# Presentaciones

## Presentación proyecto McSAFER

Héctor Lestani presentó el proyecto McSAFER. Es un proyecto de
verificación de códigos mediante la comparación de resultados de
transitorios accidentales aplicados a varios diseños de SMR. Se
presentaron resultados muy satisfactorios y también algunas
inconsistencias y discrepancias.

Durante las preguntas Eduardo Villarino sugirió revisar si las
discrepancias en DNBr no tenían que ver con el momento en el cual se
introducen los factores de pico locales, existiendo la posibilidad de
que un DNBr se calcule antes de considerar el factor de pico de celda.

Diego Ferraro compartió un enlace donde se puede averiguar más sobre el
proyecto: <https://cordis.europa.eu/project/id/945063> Y la web oficial
del proyecto es: <https://mcsafer-h2020.eu/>

<https://nube.cnea.gob.ar/index.php/s/ESzESnPpBKj4Gnj>

## INVAP's neutronic Design and Analysis group: on-going efforts

Diego Ferraro presentó diversos esfuerzos que se vienen llevando a cabo
en INVAP para fortalecer, extender y actualizar sus capacidades de
cálculo neutronico. Mencionó como ejemplos de dificultades en la labor
la reciente inclusión de SERPENT entre los códigos sometidos a *export
control* y la dificultad de capturar y retener talentos profesionales en
generaciones con gran mobilidad que reciben ofertas de trabajo modernas.
Mencionó como posible solución al tema SERPENT comprar la licencia para
usos no comerciales y luego la comercial, lo cual implica un gasto de
aproximadamente 2000\ €/año. Dijo "quizás nuestras instituciones se
acostumbraron a que consigamos licencias gratuitas gracias a nuestras
gestiones, y por eso al momento de pagar una licencia nos encontramos
con grandes dificultades".

Germán Theler citó el
[MMS](https://onscale.com/blog/solve-verification-the-method-of-manufactured-solutions)
como enfoque para la resolución de ecs. diferenciales.

<https://nube.cnea.gob.ar/index.php/s/XcnMWXwZQ5SwMdF>

## Progreso y plan de desarrollo en la línea de cálculo de INVAP

Eduardo Villarino describió brevemente la historia de los códigos
neutrónicos en INVAP y la interacción entre proyectos, códigos, usuarios
y métodos. Luego describió las planes y tareas referentes a
actualización y mejora de bibliotecas, códigos neutrónicos y
herramientas.

Discutiendo sobre distintos compiladores, mencionó como ventaja que
distintos compiladores encuentran distintos errores, entonces la
multiplicidad lleva a una mejor depuración de los códigos. Con respecto
a documentación, validación y métodos, dijo que nada que no esté
documentado se puede utilizar en evaluaciones de seguridad nuclear.

<https://nube.cnea.gob.ar/index.php/s/jPEAnEEb3MFFaCd>

## A cloud-first approach for solving core-level neutron transport

Germán Theler describió cómo los problemas que resolvemos están
moldeados y limitados por simplificaciones teóricas, limitaciones de los
modelos y cierta arbitrariedad de los desarrolladores. Discutió la
diferencia entre códigos amigables con el desarrollador y códigos
amigables con el usuario. Y la posibilidad / necesidad de usar FOSS
(Free & Open Source Software). Presentó el concepto de 'cloud-first' y
sus ventajas.

Mostró ejemplos de cálculos neutrónicos "state of the art", con sus
limitaciones, y cómo el buen uso de la herramientas y métodos
disponibles puede mejorar los resultados. Concluyó con su propuesta de
cómo deben desarrollarse los códigos neutrónicos modernos.

Héctor Lestani preguntó si el enfoque open source era aplicable a
herramientas nucleares que, tarde o temprano, terminan siendo sometidas
a export control, como el caso de SERPENT. Germán respondió que si hay
información sensible a cuidar deberían ser los datos nucleares, no las
herramientas de resolución de las ecuaciones.

<https://nube.cnea.gob.ar/index.php/s/fKbSGejfF9FRA7z>

## Desarrollo de Código Nodal para Cálculos de Núcleo

Christian Dacal presentó el desarrollo de un Código Nodal para Cálculos
de Núcleo. Describió por qué un método nodal permite relajar la
necesidad de mallado fino y qué tipos de métodos nodales hay. Que no hay
un código nodal argentino y que resultan de utilidad para PWR. Presentó
resultados consistentes de benchmarks calculados con su desarrollo de
código nodal. Mostró que tanto para el $k_\text{eff}$ como para el error en
la distribución de potencia, los resultados nodales tienen menos
discrepancias con las referencias que los resultados por diferencias
finitas, y además son menos sensibles a cambios del mallado. En todos
los casos el tiempo del solver nodal resulta menor.
Comentó que paralelizar un código que no fue pensado desde un principio,
puede llevar el mismo tiempo paralelizarlo que el propio desarrollo.

Finalizó contando los planes futuros en la línea de desarrollo. El
propietario del código es CNEA y aún no saben si será manejado igual que
PUMA.

<https://nube.cnea.gob.ar/index.php/s/ibTfyfJA3bBXWJE>

## Opciones de generación de geometrías Monte Carlo a partir de planos mecánicos 3D

Gabriel Meyer presentó varias metodologías para generar inputs Monte
Carlo a partir de planos mecánicos 3D, motivado en la creciente
necesidad de integración de distintas herramientas de ingeniería, en
particular el diseño mecánico y el modelado neutrónico (n, p). Comentó
brevemente algunas ventajas y desventajas de cada opción.

Concluyó con recomendaciones para todo el proceso, desde el modelado CAD
hasta el transporte de radiación. Y compartió un video mostrando la
integración del campo de radiación a un modelo de realidad virtual.

[La presentación está disponible en la Nube de
CNEA](https://nube.cnea.gob.ar/index.php/s/pKfrP7LwqMQ9KMA).

## Optimización ciclo combustible CAREM. Evaluación uso ATFs.

Héctor Lestani presentó los avances de una metodología de optimización
de ciclo de combustibles presentada en la reunión anual previa. La
metodología incluye la optimización neutrónica y su evaluación
económica. Mostró cómo la dificultad de mantener factores de pico bajos
al optimizar el ciclo disminuye las alternativas posibles, algo que le
había sido sugerido en la reunión anterior de GArCyAR. Presentó
resultados de aplicación de la metodología para optimizar el núcleo
actual de CAREM\ 25 y también de núcleos alternativos utilizando otros
materiales de vaina, como el FeCrAl, una vaina de ATFs.

Presentó resultados prometedores de combustibles ATF.

<https://nube.cnea.gob.ar/index.php/s/qfNsyer9wHCkcsR>

## Nueva metodología de cálculo de Parámetros Cinéticos

Eduardo Villarino presentó una nueva metodología para el cálculo de
parámetros cinéticos en la cadena de cálculo de INVAP. Describió las
diferencias entre la línea de cálculo actual y la nueva, y cómo
coexistirán durante un tiempo para evitar repetir toda la V&V de CITVAP.
Se describieron detalladamente las modificaciones necesarias a cada
eslabón de la línea de cálculo.

Presentó resultados muy satisfactorios de V&V con respecto a arreglos
críticos y a la línea de cálculo actual. Se mostró también la
sensibilidad a la cantidad de grupos de biblioteca utilizados.

[La presentación está disponible en la Nube de
CNEA](https://nube.cnea.gob.ar/index.php/s/5SWRTxdeyQ2bY8L).

## Tutorial KDSource.

Zoe Prieto presentó un tutorial de KDSource, una implementación de KDE
para aumentar el número de partículas de una fuente. KDE, Kernel Density
Estimation, consiste en generar nuevas partículas a partir de
perturbaciones (de posición, energía, dirección, etc) en torno a las
partículas originales de fuente. Las perturbaciones responden a la
incerteza de las partículas en cada uno de los parámetros perturbados.
Mostró resultados de cómo mejora la estadística en, por ejemplo, haces
de partículas, al usar KDE.

Compartió recursos con documentación y ejemplos, y el enlace de GitHub
para bajar el paquete.

<https://nube.cnea.gob.ar/index.php/s/Ey4adiEY58bt23Y>

## Sesión Matutina

Con la charla anterior se terminó la serie de presentaciones.
Compartimos el enlace a la [grabación de la sesión
matutina: <https://nube.cnea.gob.ar/index.php/s/rHYm8Z9KEo5xcag>.
Desafortunadamente la sesión de la tarde no pudo ser grabada.

# Discusión de temas abiertos

Luego de las presentaciones, dedicamos tiempo a discutir problemáticas
abiertas, que se enumeran a continuación.

## Discusiones GArCyAR

Se propuso y acordó generar canales informáticos tipo foro que permitan
continuar, a lo largo del año, las discusiones que se van generando en
las reuniones anuales. En respuesta a esta propuesta es que en el sitio
de GitHub donde residirá esta minuta, se abrirá una discusión por cada
uno de los temas listados abajo.

## Próxima Reunión Anual

Se manifestó la necesidad de garantizar la reunión 2023 buscando una/s
persona/s que se hagan cargo de la organización.
Ante este pedido, Martín Silva dio un paso al frente y se ofreció como
posible candidato. No lo pudo confirmar aún, pero adelante Martín,
estamos acá para ayudar si decidís organizarla vos.

Sigue abierta la invitación, hasta que tengamos una persona confirmada,
para ofrecerse a esta tarea. Seguimos estando acá para ayudar a quien se
ofrezca.

Para discutir sobre este tema, podemos escribir en [esta *discussion* de
GitHub.](https://github.com/GArCyAR/ReunionesAnuales/discussions/1#discussion-4699808)

## Cálculo de PWR

Se presentó el Cálculo de núcleos de reactores PWR como una materia
incompleta entre nuestras capacidades. La memoria de cálculo necesaria
para problemas PWR en esquema de diferencia finitas resulta prohibitiva.
Estas ideas fueron pensadas antes del desarrollo presentado por
Christian Dacal, que muestra un adelanto notable en la resolución de
este tema. No podemos desconocer que faltaría aún mucho trabajo de
desarrollo y de V&V para que esa herramienta pueda cumplir este rol,
además de que falta el marco institucional en el que eso podría ocurrir.
Se ha discutido brevemente al respecto.

De todos, claramente el desarrollo de Christian Dacal (y el equipo
involucrado) es un gran avance en este sentido.

Durante la discusión se mencionó que un recambio sale del orden de
$10^8~\text{USD}$, y eso debería tenerse en mente al momento de pedir apoyo
institucional para este desarrollo.

Se mencionó también que una incerteza de 5% en márgenes TH implica mucho
dinero, y va en línea del comentario anterior.

Para discutir sobre este tema, podemos escribir en [esta *discussion* de
GitHub.](https://github.com/GArCyAR/ReunionesAnuales/discussions/2#discussion-4699888)

## Datos Nucleares para proyectos

Del mismo modo que con el cálculo de PWR, se identifica a esta tarea
como una materia incompleta en nuestras capacidades.\
A diferencia del cálculo PWR, estas capacidades existieron en nuestro
ecosistema pero se fueron perdiendo con el tiempo (porque las personas
ya no están, como el caso de Francisco Leszynsky, o porque se ha ido a
otras empresas).

Para discutir sobre este tema, podemos escribir en [esta *discussion* de
GitHub.](https://github.com/GArCyAR/ReunionesAnuales/discussions/4#discussion-4699914)

## Recursos Humanos

Se planteó la necesidad de visibilizar las posibilidades laborales para
que los/as egresados/as puedan ver claramente sus alternativas.

Se abre entonces [esta *discussion* de
GitHub.](https://github.com/GArCyAR/ReunionesAnuales/discussions/5#discussion-4700233)

## Datos Experimentales

Se mencionó la existencia de fuertes discrepancias en resultados de
reactividad cuando se involucra quemado de *venenos quemables*. Dada la
aplicación de venenos quemables de Cd en los MTR y de Gd en el diseño
CAREM, se considera importante buscar el origen de las discrepancias
observadas.

Se abre entonces [esta *discussion* de
GitHub.](https://github.com/GArCyAR/ReunionesAnuales/discussions/6#discussion-4700244)

# Conclusión

Llegó el momento ocupar nuestro lugar. GArCyAR no tiene dueño/a ni
presidente. Aquí somos todas/os protagonistas. Vení, ocupá tu lugar,
comentá, opiná, aportá, consultá.
Este espacio es tuyo.

