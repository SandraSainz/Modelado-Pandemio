
# MODELADO SOFTWARE DE SISTEMAS DE INFORMACIÓN

## PANDEMIO

### Versión: 3
### Fecha: 16/12/2020


**Índice**   
1. [INTRODUCCIÓN](#id1)  
1.1 [Alcance](#id11)  
1.2 [Objetivos](#id12)  
2. [INFORMACIÓN DEL DOMINIO DEL PROBLEMA](#id2)  
2.1 [Introducción al dominio del problema](#id21)  
2.2 [Glosario de términos](#id22)  
3. [DESCRIPCIÓN DE LA SITUACIÓN ACTUAL](#id3)  
3.1 [Pros y contras de la situación actual](#id31)  
3.1.1 [Fortalezas de la situación actual](#id311)  
3.1.2 [Debilidades de la situación actual](#id312)  
3.2 [Modelo de procesos de negocio actuales](#id32)  
3.2.1 [Descripción de los Actores de Negocio Actuales](#id321)  
3.2.2 [Descripción de los Procesos de Negocio Actuales](#id322)  
3.3 [Entorno tecnológico actual](#id33)  
3.3.1 [Descripción del entorno de Hardware actual](#id331)  
3.3.2 [Descripción del entorno de Software actual](#id332)  
4. [NECESIDADES DE NEGOCIO](#id4)  
4.1 [Objetivos de negocio](#id41)  
4.2 [Modelos de procesos de negocio a implantar](#id42)  
4.2.1 [Descripción de los modelos de negocio a implantar](#id421)  
4.2.2 [Descripción de los procesos de negocio a implantar](#id422)  
5. [DESCRIPCIÓN DE LOS SUBSISTEMAS DEL SISTEMA A DESARROLLAR](#id5)  
6. [CATÁLOGO DE REQUISITOS DEL SISTEMA A DESARROLLAR](#id6)  
6.1 [Requisitos Generales del Sistema](#id61)  
6.2 [Casos de uso del Sistema](#id62)  
6.2.1 [Diagrama de Casos de uso del Sistema](#id621)  
6.2.2 [Especificación de Actores del Sistema](#id622)  
6.2.3 [Especificación de Casos de uso del Sistema](#id623)  
6.3 [Requisitos Funcionales del Sistema](#id63)  
6.3.1 [Requisitos de Información del Sistema](#id631)  
6.3.2 [Requisitos de Reglas de Negocio del Sistema](#id632)  
6.3.3 [Requisitos de Conducta del Sistema](#id633)  
6.4 [Requisitos No Funcionales del Sistema](#id64)  
6.4.1 [Requisitos de Fiabilidad](#id641)  
6.4.2 [Requisitos de Usabilidad](#id642)  
6.4.3 [Requisitos de Eficiencia](#id643)  
6.4.4 [Requisitos de Mantenibilidad](#id644)  
6.4.5 [Requisitos de Portabilidad](#id645)  
6.4.6 [Requisitos de Seguridad](#id646)  
6.4.7 [Otros Requisitos No Funcionales](#id647)  
6.5 [Restricciones Técnicas del Sistema](#id65)  
6.6 [Requisitos de Integración del Sistema](#id66)  
6.7 [Información sobre Trazabilidad](#id67)  
7. [ANEXOS](#id7)  
7.1 [Anexo A: Actas de Reuniones](#id71)  
7.2 [Anexo B: Documentación Relevante](#id72)  
7.3 [Anexo C: Glosario de Términos y Abreviaturas](#id73)  

<br>
<img height= "700" src= "https://github.com/irenepenasperez/pandemio/blob/main/DiagramaDeIshikawa.jpg"/>
<br>

<br>
<img height= "700" src= "https://github.com/irenepenasperez/pandemio/blob/main/DFDnivel0.jpg"/>
<br>  


## 1 INTRODUCCIÓN<a name="id1"></a>
En la situación actual, existe una aplicación llamada Radar Covid. Sin embargo, en dicha aplicación, se han detectado una serie de problemas, identificados por un comité de expertos:
* La instalación y uso de la aplicación no eran obligatorios. Por lo tanto, no la instalaron muchas personas.
* Esta aplicación se basa en Bluetooth, por lo que si éste se encuentra apagado u ocupado, la aplicación será inservible.

Habiendo expuesto el problema, se ha generado una consiguiente necesidad de hacer un nuevo desarrollo de otra aplicación, de características similares, pero corrigiendo los errores arriba expuestos.

> Referencia: Pliego de Prescripciones Técnicas.

### 1.1 Alcance
La duración que se estima para la aplicación es el periodo de tiempo en el cual dure la actual pandemia de la COVID-19.

Los elementos organizativos a los que afecta el desarrollo del nuevo sistema son los siguientes:
* Los ciudadanos
* Las operadoras
* Los fabricantes de teléfonos y de sistemas operativos, proporcionando los datos de geolocalización pertinentes.
* Los políticos (tendrán que hacer los cambios legales oportunos para poder hacer ciertas funcionalidades problemáticas de la aplicación, como el uso de los datos de localización de los dispositivos).
* Las fuerzas del orden (Policía Local, Nacional, Guardia Civil y el Ejército) serán capaces de comprobar, según su ámbito, el cumplimiento de las cuarentenas y las obligaciones impuestas a los ciudadanos.
* Ambulatorios, que recibirán los listados de las personas que deben realizar las pruebas. Además podrán notificar a la autoridad el incumplimiento de las mismas.
* Las autonomías, debido a que los sistemas de información son diferentes en cada una de ellas. Podrían intervenir los Gobiernos Autonómicos o las Consejerías Autonómicas.
* Rastreadores, que son las personas encargadas de localizar a todas aquellas personas que hayan estado en contacto con un positivo en COVID-19.

### 1.2 Objetivos<a name="id12"></a>
El objetivo final de la aplicación cuando se ponga en funcionamiento es poder rastrear y gestionar la información de los ciudadanos de la próxima pandemia.

Objetivos complementarios:
* Comprobar el cumplimiento de las cuarentenas y las obligaciones impuestas a los ciudadanos. Este objetivo será llevado a cabo por parte de las FFCCSE. 
* Recibir listado de las personas que deben hacerse las pruebas, y notificar a las autoridades el incumplimiento. 
* Sacar información y estadísticas actualizadas, que serán muy útiles para el Gobierno y las autonomías para poder llevar a cabo decisiones objetivas.

## 2 INFORMACIÓN DEL DOMINIO DEL PROBLEMA<a name="id2"></a>
Con esta aplicación se busca mejorar la aplicación Radar COVID, ya que se han encontrado algunos problemas arriba mencionados.

### 2.1 Introducción al dominio del problema<a name="id21"></a>
En esta aplicación lo que se busca es a través de los datos recogidos de los pacientes positivos en COVID-19 hacer un rastreo de estos, siempre respetando el anonimato, para asegurarse de que estos cumplen con la cuarentena obligatoria. También se busca garantizar el cumplimiento de realización de las diferentes pruebas.

Cuando un paciente de positivo en Covid-19 se le añadirá a una Base de Datos; mediante el uso del GPS y de la geolocalización se vigilará constantemente que este usuario este cumpliendo con la obligación de hacer cuarentena, y en caso de que no la realize podrán intervenir las fuerzas del orden (policía local, nacional, guardia civil y el ejército).  
Los centros de salud recibirán periodicamente un listado con los pacientes positivos, cuando deben realizarse la siguiente prueba y, en caso de ser la primera prueba los contactos de este que deben realizarse la prueba; tendrán la posibilidad de notificar a las autoridades del incumplimiento. Una vez el paciente sea negativo se borrará y destruirá sus información.  
Si para realizar cualquiera de estos procedimientos se incumpliera la Ley de Protección de Datos, esta ley podrá ser modificada con tal de controlar el correcto cumplimiento de las obligaciones de los casos positivos. Solo pordrán acceder a la información de los pacientes positivos quien deba hacerlo y tenga el derecho a hacerlo; la información siempre será anónima.

### 2.2 Glosario de términos<a name="id22"></a>
* Alerta sanitaria: es una medida dispuesta por el Ministerio de Salud en caso de amenaza de alguna epidemia o de aumento de alguna enfermedad o de emergencias que impliquen grave riesgo para salud o para la vida de los habitantes.
* Ambulatorio: edificio o estructura que alberga el núcleo básico de atención sanitaria. Este núcleo está compuesto por un médico de familia, personal de enfermería, un pediatra y el correspondiente personal administrativo. 
* Anónimo: de autor desconocido.
* Aplicación: es un programa informático diseñado como una herramienta para realizar operaciones o funciones específicas.
* Bluetooth: es una especificación tecnológica para redes inalámbricas que permite la transmisión de voz y datos entre distintos dispositivos mediante una radiofrecuencia segura (2,4 GHz).
* Covid-19: La enfermedad por coronavirus (COVID 19) es una ‎enfermedad infecciosa causada por un ‎coronavirus recientemente descubierto. ‎
* Cuarentena: es un período en el que se procura el aislamiento de personas que podrían haber contraído una enfermedad, pero aún no manifiestan síntomas. También aplica en personas o comunidades sanas a las que se quiere proteger de un posible contagio.
* Dato personal: todo dato informativo capaz de hacer identificada o identificable a una persona física. Es decir, cualquier dato que, por sí mismo o en consonancia a otros datos que pudieran cotejarse, pueda llevar a la identificación de una persona física.  
Tipos de datos:  
  * Dato Público: Es el dato que la ley o la Constitución Política determina como tal, así como todos aquellos que no sean semiprivados o privados.
  * Dato Semiprivado: Es el dato que no tiene naturaleza íntima, reservada, ni pública y cuyo conocimiento o divulgación puede interesar no sólo a su titular sino a cierto sector o grupo de personas.
  * Dato Privado: Es el dato que por su naturaleza íntima o reservada sólo es relevante para el titular de la información.
  * Dato Sensible: Es el dato que afecta la intimidad del titular o cuyo uso indebido puede generar su discriminación.
* Epidemia: Enfermedad que ataca a un gran número de personas o de animales en un mismo lugar y durante un mismo período de tiempo.
* Geolocalización: determina la posición de cualquier objeto, persona o vehículo con un margen de error de unos pocos metros. Existen cuatro sistemas de navegación operativos o sistema de localización por satélite: GPS, GLONASS, GALILEO Y BEIDOU.
* Geoposicionamiento: posición de una persona, punto o empresa en un plano cartográfico.
* GPS: Sistema americano de navegación y localización mediante satélites.
* Legal: Que está establecido por la ley o está conforme con ella.
* Ley de Protección de Datos: Las leyes que regulan la protección de datos se basan en la premisa de que todos los datos personales de los usuarios deben ser protegidos por los legisladores europeos. La Ley de Protección de Datos Personales reconoce y protege el derecho que tienen todas las personas a conocer, actualizar y rectificar las informaciones que se hayan recogido sobre ellas en bases de datos o archivos que sean susceptibles de tratamiento por entidades de naturaleza pública o privada.  
¿A qué datos personales no se aplica?
  * A las bases de datos o archivos mantenidos en un ámbito exclusivamente personal o doméstico.
  * Las que tengan por finalidad la seguridad y defensa nacionalla prevención, detección, monitoreo y control del lavado de activos y el financiamiento del terrorismo.
  * Las que tengan como fin y contengan información de inteligencia y contrainteligencia.
  * Las que contengan información periodística y otros contenidos editoriales
  * Las bases de datos con información financiera, crediticia, comercial y de servicios, y de los censos de población y vivienda.
* Localización geográfica: permite la identificación de un punto de la superficie terrestre simplemente con dos números (que expresan la latitud y la longitud geográfica). 
* Pandemia: Enfermedad epidémica que se extiende a muchos países o que ataca a casi todos los individuos de una localidad o región.
* PCR: siglas en inglés de 'Reacción en Cadena de la Polimerasa', es una prueba de diagnóstico que permite detectar un fragmento del material genético de un patógeno.
* PCR +: implica que hay material genético del virus en la persona en la que se ha realizado, por lo tanto está contagiada.
* Prueba de antígenos: es una prueba de diagnóstico que permite detectar cierta proteina del virus.
* Prueba rápida: detectan, o bien anticuerpos producidos frente al virus utilizando una muestra de sangre, o bien proteínas del virus presentes en las muestras respiratorias de exudado nasofaríngeo.
* Prueba serológica: permite comprobar la presencia de anticuerpos en la sangre.
* Segundo plano (app en segundo plano): la aplicación puede realizar alguna funcion sin necesidad de que el usuario esté interactuando con la aplicación.
* Test de antígenos +: se refiere a que hay proteína del virus en la persona que se ha realizado la prueba, por lo tanto en el momento de realizar la prueba está contagiado.
* Triangulación mediante gps: consiste en averiguar el ángulo de cada una de las tres señales respecto al punto de medición. Conocidos los tres ángulos, se determina fácilmente la propia posición relativa respecto a los tres satélites. Conociendo además las coordenadas o posición de cada uno de ellos por la señal que emiten, se obtiene la posición absoluta o coordenadas reales del punto de medición.  
<img src="https://3.bp.blogspot.com/-pFEneQwAM64/UXP4X2glFFI/AAAAAAAAEAk/Ly4htjqfvII/s1600/GPS.jpeg" title="Triangulacion" width="300">  


## 3 DESCRIPCIÓN DE LA SITUACIÓN ACTUAL<a name="id3"></a>
El usuario descarga la aplicación y al abrirla debe aceptar los términos de uso y activar las notificaciones de exposición al COVID-19. El usuario no debe hacer nada más, solo debe esperar a que la aplicación le avise siestá en riesgo de COVID o en caso de que se haya hecho un PCR y la prueba haya salido positiva, deberá introducir un código numérico facilitado por el centro sanitario.  
La aplicación genera identificadores aleatorios cada vez que dos dispositivos móviles que tengan la aplicación instalada y el Bluetooth activado están más de 15 minutos a menos de 2 metros de distancia. Estos identificadores los guarda durante los siguientes 14 días. Cuando se ha detectado un caso positivo, la aplicación mandará un mensaje de alerta a todas las personas que hayan tenido un contacto estrecho con la persona contagiada indicándoles que han tenido un contacto de riesgo.

### 3.1 Pros y contras de la situación actual<a name="id31"></a>
La aplicación Radar Covid es de gran ayuda y cuenta con la ventaja de que en la actualidad mucha gente tiene un Smartphone. Sin embargo, el aspecto más negativo de esta aplicación es su no obligatoriedad, lo que ha hecho que poca gente la haya descargado y no sea tan efectiva como debería.

#### 3.1.1 Fortalezas de la situación actual<a name="id311"></a>
* En la actualidad, la mayor parte de la población tiene un teléfono móvil, lo que facilita la utilización de esta aplicación.
* La actual Radar Covid permite conocer si estás en riesgo en función de los contactos estrechos que hayas tenido en los últimos 14 días (menos de 2 metros más de 15 minutos).
* Permite que las personas con PCR positiva comuniquen el resultado anónimamente.
* La información personal y la ubicación son anónimas.
* Reutilización de código: En la nueva aplicación a desarrollar se puede reutilizar parte del código de la aplicación actual.

| 3.1.1.01           |  Teléfono móvil                                                                       |  
|--------------|---------------------------------------------------------------------------------------|  
| Versión      | 1.0                                                                                   |  
| Descripción  | Hoy en día su uso está muy extendido                                                  |  
| Comentarios  | Si todas las personas con smartphone usaran esta aplicación, sería de gran utilidad.  | 

| 3.1.1.02           | Contactos estrechos                                              |  
|--------------|------------------------------------------------------------------|  
| Versión      | 1.0                                                              |  
| Descripción  | Permite conocer el riesgo en función de los positivos cercanos.  |  
| Comentarios  |                                                                  | 

| 3.1.1.03           | Comunicar positivo                                                               |  
|--------------|----------------------------------------------------------------------------------|  
| Versión      | 1.0                                                                              |  
| Descripción  |  Una de las funciones de la aplicación es comunicar un positivo en test covid.   |  
| Comentarios  |  Esta función es opcional y por ello no todos los usuarios lo comunican.         | 

| 3.1.1.04           | Anonimato                                                                                 |  
|--------------|-------------------------------------------------------------------------------------------|  
| Versión      | 1.0                                                                                       |  
| Descripción  | La aplicación respeta el anonimato de los usuarios y no conoce su localización gográfica. |  
| Comentarios  |                                                                                           | 

| 3.1.1.05           |  Reutilización de código                                                              |  
|--------------|---------------------------------------------------------------------------------------|  
| Versión      | 1.0                                                                                   |  
| Descripción  | Aprovechamiento de parte del código de la aplicación actual                           |  
| Comentarios  | La acual aplicación tiene un desarrollo que puede implementarse en la nueva.          | 

#### 3.1.2 Debilidades de la situación actual<a name="id312"></a>
* Aunque una gran parte de la población tiene un Smartphone, aún hay personas que no lo tienen (personas mayores, sin recursos, etc.) o teléfonos móviles obsoletos que no permiten la instalación de dicha aplicación.
* Al estar basado en conectividad Bluetooth, puede que haya personas que no lo tengan activado y por tanto se pierda la funcionalidad de la aplicación. 
* La aplicación actualmente no es obligatoria, lo que hace que muchas personas no la instalen.
* Lugares sin cobertura ni conexión a Internet.

| 3.1.2.01           | No disponer de smartphone                                                |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |  
| Descripción  | Las personas sin smartphone no pueden utilizar esta aplicación.          |  
| Comentarios  |                                                                          | 

| 3.1.2.02           |  Bluetooth                                                             |  
|--------------|------------------------------------------------------------------------|  
| Versión      | 1.0                                                                    |  
| Descripción  | La aplicación solo funciona si el sistema Bluetooth está activado.     |  
| Comentarios  |                                                                        | 

| 3.1.2.03           |  No obligatoriedad                                                               |  
|--------------|----------------------------------------------------------------------------------|  
| Versión      | 1.0                                                                              |  
| Descripción  | Con la ley vigente, la aplicación no se puede imponer el uso de la aplicación.   |  
| Comentarios  |                                                                                  | 

| 3.1.2.04           |  Cobertura                                                             |  
|--------------|------------------------------------------------------------------------|  
| Versión      | 1.0                                                                    |  
| Descripción  | En la actualidad aún hay lugares en los que no se dispone de conexión a Internet ni cobertura.  |  
| Comentarios  | En muchas zonas rurales este es un problema, ya que además la mayor parte de la población en estos lugares son personas de riesgo.                       | 

### 3.2 Modelos de procesos de negocio actuales<a name="id32"></a>
Radar Covid es una app móvil, desarrollada para ayudar a controlar la propagación de la COVID-19, a través de la identificación de los posibles contactos estrechos de casos confirmados a través de la tecnología Bluetooth.  
El sistema de notificaciones de exposición de Radar Covid avisa a los usuarios cuando han estado expuestos a otro usuario de la app que ha sido positivo y ha introducido un código facilitado por las autoridades sanitarias de su C.A. Cada dispositivo que tenga la app instalada y el Bluetooth activado, genera de forma continua id aleatorios, que se intercambian con otros dispositivos que también la tengan activa, y se encuentren a menos de 2 metros. Cada teléfono almacenará durante los siguientes 14 días sus propios id generados, y los id de los dispositivos que han estado cerca. Cuando un usuario recibe un diagnóstico positivo, los servicios de salud le facilitarán un código numérico de caso positivo, que la persona deberá introducir en la app. Entonces, los id aleatorios generados por ese dispositivo durante los 5 días previos a este momento se etiquetan como positivos y se lanzan a la nube con consentimiento del usuario. Por su parte, periódicamente, todos los dispositivos descargarán los id positivos de la nube y se hará un cruce de datos. Si los id se encuentran entre los almacenados como contactos y si suponen un tiempo de exposición superior a 15 minutos. La búsqueda de contactos será de hasta 5 días antes del momento de la introducción del código (fecha del diagnóstico de 3 días + búsqueda ampliada de 2 días antes de la fecha de inicio de los síntomas).

#### 3.2.1 Descripción de los Actores de Negocio Actuales<a name="id321"></a>
* Usuario: Los usuarios necesitan tener un dispositivo para poder descargar la aplicación Radar Covid. Cuando la han descargado, tienen que aceptar los términos y la aplicación ya empieza a recoger los códigos de los contactos estrechos por medio del sistema Bluetooth. Si reciben una notificación comunicando un riesgo alto, estos deberán hacer cuarentena. Si el usuario ha sido diagnosticado con COVID-19, se le proporcionará un código que puede introducir voluntariamente en la aplicación.
* Desarrolladores: Crean la aplicación siguiendo los modelos ofrecidos por el Gobierno y el Ministerio de Sanidad. 
* Ministerio de sanidad: Ordena hacer la aplicación para poder llevar un control sobre la pandemia a nivel nacional. Recomienda la descarga y la utilización de Radar Covid y adopta las medidas sanitarias necesarias dependiendo de la situación actual sanitaria, apoyándose en la información de Radar Covid.
* Centro de salud: Los sanitarios se encargarán de hacer los test PCR y de comunicar los resultados. Si una PCR es positiva, el centro de salud dará un código al paciente positivo. 
De acuerdo al Real Decreto-ley 21/2020 de medidas urgentes para hacer frente a la crisis sanitaria ocasionada por el COVID-19, las autoridades sanitarias pueden realizar a todo sospechoso de COVID-19 una prueba PCR.
* Policía: Siguiendo las órdenes del Gobierno, controlará que los ciudadanos cumplen con la normativa vigente y las personas con PCR positiva cumplen la cuarentena. También pueden intervenir si una persona sospechosa de COVID-19 se niega a realizarse la PCR.
* Rastreadores: Profesionales encargados de buscar a todas aquellas personas que hayan estado en contacto con un positivo en COVID-19 para controlar la situación según los protocolos. Su labor es esencial a la hora de contener la propagación del virus.
* Gobierno/consejerías de cada comunidad: En cada comunidad autónoma varían las normativas de esta pandemia. En algunas regiones se pueden ordenar confinamientos domiciliarios para frenar el avance del virus y otras medidas apoyados en las estadísticas resultantes de los datos de la aplicación.

#### 3.2.2 Descripción de Procesos de Negocio Actuales<a name="id322"></a>
* Comprobar el cumplimiento de las cuarentenas y las obligaciones impuestas a los ciudadanos: Si un ciudadano es positivo en COVID-19 o sospechoso, se le puede obligar a cumplir la cuarentena preventiva. Si el individuo se niega, pueden intervenir las Fuerzas y Cuerpos de Seguridad del Estado.  
Si no existiera este proceso de negocio, habría un alto riesgo de expansión del virus por el incumplimiento de las cuarentenas.  

| 3.2.2.01           | Cumplimiento de cuarentenas                                                               |  
|--------------|---------------------------------------------------------------------------------------|  
| Versión      | 1.0                                                                                   |  
| Dependencias |                                                                                       |  
| Descripción  | Se puede obligar a una persona a cumplir cuarentena si es positivo o sospechoso.      |  
| Importancia  |  Alta                                                                             |  
| Actores      | -Policía -Ciudadanos -Rastreadores                                                    |  
| Comentarios  | Al principio de la pandemia, las cuarentenas eran de 14 días, pero su duración se ha reducido a 10. |  

* Recibir listado de las personas que deben hacerse las pruebas, y notificar a las autoridades el incumplimiento: Los sanitarios pueden recibir un listado con las personas que deben realizarse las pruebas PCR. Si estas notifican un incumplimiento, pueden avisar a las autoridades que intervendrán. Es importante que se cumpla este paso, ya que deben realizarse las pruebas oportunas para calcular la incidencia del virus en un territorio determinado y para cuarentenar a los positivos.

| 3.2.2.02           |  Listado de pruebas                                                                        |  
|--------------|----------------------------------------------------------------------------------------|  
| Versión      | 1.0                                                                                    |  
| Dependencias |                                                                                        |  
| Descripción  | Listado de personas que deben hacerse la prueba. Si se oponen, las FFCCSE intervienen. |  
| Importancia  |  Alta                                                                           |  
| Actores      | -Ambulatorios -Ciudadanos -Fuerzas del orden       |  
| Comentarios  |                                                                                        |  

* Rastrear a los positivos y a sus contactos: Esta medida puede ayudar a frenar los contagios y a hacer un estudio sobre la evolución de la enfermedad en las personas.

| 3.2.2.03           | Rastreo                                                                         |  
|--------------|-----------------------------------------------------------------------------------------------|  
| Versión      | 1.0                                                                                           |  
| Dependencias | 3.2.2.02                                                                                            |  
| Descripción  | Con los resultados de las pruebas, los rastreadores pueden rastrear a aquellas personas contagiadas y tener un control sobre los contactos de dichas personas.  |  
| Importancia  |  Alta                                                                                     |  
| Actores      | -Ambulatorios -Rastreadores -Gobierno -Autonomías  |  
| Comentarios  |                                                                                               |

* Sacar información y estadísticas actualizadas, que serán muy útiles para el Gobierno y las autonomías para poder llevar a cabo decisiones objetivas: Este proceso depende del cumplimiento de la realización de las pruebas.  
Con los datos obtenidos tras realizar tests, se podrán sacar conclusiones sobre la situación actual y sobre estos datos, los responsables de la salud podrán tomar decisiones para intentar abordar la expansión de la enfermedad.  
Este paso es de gran importancia, ya que si no tenemos datos, no sabremos qué medidas tomar ni el riesgo en el que nos encontramos.

| 3.2.2.04           | Sacar estadísticas                                                                  |  
|--------------|-----------------------------------------------------------------------------------------------|  
| Versión      | 1.0                                                                                           |  
| Dependencias | 3.2.2.02, 3.2.2.03                                                                                          |  
| Descripción  | Con los resultados de las pruebas, el Gobierno puede tomar medidas ajustadas a la situación.  |  
| Importancia  |  Media                                                                                       |  
| Actores      | -Ambulatorios -Gobierno -Autonomías  |  
| Comentarios  |                                                                                               |


### 3.3 Entorno tecnológico actual<a name="id33"></a>
El entorno tecnológico actual estaría formado por los distintos teléfonos móviles (smartphone), la compatibilidad de los distintos sistemas operativos con la aplicación, las distintas bases de datos donde estará almacenada la información necesaria, donde se almacenará esta información (servidor protegido o nube), las antenas de telefonía móvil y la cobertura, tratando las posibles zonas de sombra.

#### 3.3.1 Descripción del Entorno de Hardware Actual<a name="id331"></a>
* Antena de telefonía móvil: es una estación base, de instalación fija, que se conecta con los teléfonos móviles mediante ondas electromagnéticas de radiofrecuencia, asimismo las antenas se comunican con la central de su propia red.
* Smartphone: teléfono celular con pantalla táctil, que permite al usuario conectarse a internet, gestionar cuentas de correo electrónico e instalar otras aplicaciones y recursos a modo de pequeño computador.

#### 3.3.2 Descripción del Entorno de Software Actual.<a name="id332"></a>
* Aplicación Radar Covid: aplicación que permite mediante el uso de bluetooth y geolocalización informar al usuario sobre si ha estado o no en contacto con una persona positiva en coronavirus.
* Base de datos: programa capaz de almacenar gran cantidad de datos, relacionados y estructurados, que pueden ser consultados rápidamente de acuerdo con las características selectivas que se deseen.
* Cobertura: en telecomunicaciones, el término cobertura se refiere al área geográfica en la que se dispone de un servicio. Son zonas a las que la señal de radio de la estación base llega sin sufrir un excesivo debilitamiento
* Nube (Informática en la nube): es el suministro de servicios informáticos (incluidos servidores, almacenamiento, bases de datos, redes, software, análisis e inteligencia) a través de Internet, cuyo objetivo es ofrecer una innovación más rápida, recursos flexibles y economías de escala. La mayoría se utilizan para almacenar grandes cantidades de información en el servidor y tenerla protegida fuera de nuestro ordenador.
* Sistema operativo: Conjunto de órdenes y programas que controlan los procesos básicos de una computadora y permiten el funcionamiento de otros programas.
* Zona de sombra (cobertura): son las zonas en las que la señal de radio de la estación base llega demasiado débil, bien porque hay obstáculos o simplemente porque están muy lejos.  

## 4 NECESIDADES DE NEGOCIO<a name="id4"></a>
En este apartado, se recoge toda la información sobre los objetivos de negocio de clientes y usuarios, además de los modelos de procesos de negocio a implantar.
> Referencia: 1.2 Objetivos:  
El objetivo final de la aplicación cuando se ponga en funcionamiento es poder rastrear y gestionar la información de los ciudadanos de la próxima pandemia.
Objetivos complementarios:
>* Comprobar el cumplimiento de las cuarentenas y las obligaciones impuestas a los ciudadanos. Este objetivo será llevado a cabo por parte de las FFCCSE. 
>* Recibir listado de las personas que deben hacerse las pruebas, y notificar a las autoridades el incumplimiento. 
>* Sacar información y estadísticas actualizadas, que serán muy útiles para el Gobierno y las autonomías para poder llevar a cabo decisiones objetivas.


### 4.1 Objetivos de Negocio<a name="id41"></a>
| 4.1.01       | Rastrear y gestionar información de los ciudadanos de la próxima pandemia|  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias |4.2.1.01, 4.2.1.02, 4.2.1.03, 4.2.1.04, 4.2.1.05, 4.2.1.06, 4.2.1.07, 4.2.1.08                                                                          |
| Descripción  | Hacer un seguimiento de los ciudadanos y manipular los datos derivados del mismo  para esta y otras pandemias  
| Subobjetivos | 02, 03, 04                                                               | 
| Importancia  | muy alta                                                                 |
| Prioridad    |                                                                          |
| Comentarios  |                                                                          |

| 4.1.02       | Comprobar cumplimiento de las cuarentenas y obligaciones impuestas a los ciudadanos|  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias | 4.1.01, 4.2.1.06                                                                       |
| Descripción  | Las FFCCSE verificarán que se cumplan las cuarentenas y las imposiciones a los ciudadanos. 
| Subobjetivos |                                                                          | 
| Importancia  | muy alta                                                                 |
| Prioridad    |                                                                          |
| Comentarios  |                                                                          |

| 4.1.03       | Gestión de realización de pruebas y cumplimientos|  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias | 4.1.01, 4.2.1.05                                                                       |
| Descripción  | Los ambulatorios tendrán un listado de personas que deberán realizarse las pruebas, y en caso de no presentarse a las mismas,deberán notificar a las FFCCSE el incumplimiento de la realización de la prueba.
| Subobjetivos |Recibir listado de personas y notificar a las autoridades su incumplimiento.                                                                           | 
| Importancia  | muy alta                                                                 |
| Prioridad    |                                                                          |
| Comentarios  |                                                                          |

| 4.1.04       | Sacar información y estadísticas actualizadas|  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias | 4.1.01, 4.2.1.08, 4.2.1.04                                                                       |
| Descripción  | Se obtendrá información y estadísticas derivadas del seguimiento realizado, que más tarde estudiarán el Gobierno y las autonomías para la toma de decisiones objetivas.
| Subobjetivos | Analizar la información y crear estadísticas derivadas.                  | 
| Importancia  | muy alta                                                                 |
| Prioridad    |                                                                          |
| Comentarios  |                                                                          | 

### 4.2 Modelos de Procesos de Negocio a Implantar<a name="id42"></a>

#### 4.2.1 Descripción de los Actores de Negocio a Implantar<a name="id421"></a>
| 4.2.1.01           | Usuario                                |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias |                                                                          |
| Descripción  | Cualquier persona que se descargue la App RadarCOVID          |  
| Comentarios  |                                                                          |

| 4.2.1.02           |      Usuario positivo en COVID-19                            |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias |  4.2.1.01                                               |
| Descripción  | Persona con la app RadarCOVID descargada y con positivo en COVID19       |  
| Comentarios  | En este caso, la ubicación no se usará para saber los posibles contactos positivos, sino para saber los contactos estrechos de este, y para comprobar el cumplimiento de la cuarentena. Además, se le indica un código que debe introducir para notificar su positivo.|

| 4.2.1.03          |      Ministerio de sanidad                           |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias | 4.2.1.07                                                                |
| Descripción  |  Ordena hacer la aplicación para poder llevar un control sobre la pandemia a nivel nacional. Recomienda la descarga y la utilización de Radar Covid y adopta las medidas sanitarias necesarias dependiendo de la situación actual sanitaria, apoyándose en la información de Radar Covid.       |  
| Comentarios  |                                                                          |

| 4.2.1.04           | Centro de salud                            |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias |                                                                          |
| Descripción  |  Los sanitarios se encargarán de hacer los test PCR y de comunicar los resultados. Si una PCR es positiva, el centro de salud dará un código al paciente positivo. De acuerdo al Real Decreto-ley 21/2020 de medidas urgentes para hacer frente a la crisis sanitaria ocasionada por el COVID-19, las autoridades sanitarias pueden realizar a todo sospechoso de COVID-19 una prueba PCR.       |  
| Comentarios  |                                                                          |

| 4.2.1.05 | Fuerzas del estado                            |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias |                                                                          |
| Descripción  | Siguiendo las órdenes del Gobierno, controlará que los ciudadanos cumplen con la normativa vigente y las personas con PCR positiva cumplen la cuarentena. También pueden intervenir si una persona sospechosa de COVID-19 se niega a realizarse la PCR.       |  
| Comentarios  |                                                                          |

| 4.2.1.06           | Rastreadores                            |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias |                                                                          |
| Descripción  | Profesionales encargados de buscar a todas aquellas personas que hayan estado en contacto con un positivo en COVID-19 para controlar la situación según los protocolos. Su labor es esencial a la hora de contener la propagación del virus.       |  
| Comentarios  |                                                                          |

| 4.2.1.07           | Gobierno/Consejerías de cada comunidad                            |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias |                                                                          |
| Descripción  | En cada comunidad autónoma varían las normativas de esta pandemia. En algunas regiones se pueden ordenar confinamientos domiciliarios para frenar el avance del virus y otras medidas apoyados en las estadísticas resultantes de los datos de la aplicación.       |  
| Comentarios  |                                                                          |

| 4.2.1.08     | Fabricantes de teléfonos móviles/operadoras móviles                            |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias |                                                                          |
| Descripción  | Se encargan de facilitar los datos de geolocalización y geoposicionamiento de los usuarios       |  
| Comentarios  |                                                                          |

#### 4.2.2 Descripción de Procesos de Negocio a Implantar<a name="id422"></a>

| 4.2.2.01           |  Descarga de la aplicación                                                       |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias |                                                                          |
| Descripción  | Lo primero que debe hacer el usuario es descargarse la aplicación.          |  
| Importancia  |     Muy alta                                                                     | 
| Actores      |  Persona que descarga la app                                                                    |
| Comentarios  |                                                                          |

| 4.2.2.02          |  Aceptar los términos de uso y activar el Radar COVID                                      |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias |     4.2.2.01                                                                     |
| Descripción  | Para que se pueda utilizar la aplicación se deben aceptar las condiciones y activar el radar.          |  
| Importancia  |      Muy alta                                                                    | 
| Actores      |   Persona que descarga la app                                                                    |
| Comentarios  |                                                                          |


| 4.2.2.03           |  Test positivo                                                       |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias |                                                                          |
| Descripción  | Si la persona da positivo en la enfermedad debe comunicarlo a la aplicación.          |  
| Importancia  |    Muy alta                                                                      | 
| Actores      |  Centro de salud, persona positiva en COVID                            |
| Comentarios  | En la aplicación actual, la decisión de comunicarlo es voluntaria.                                                                    |


| 4.2.2.04           |  Comprobar contactos con COVID                                                    |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias |   4.2.2.01, 4.2.2.02                                                                       |
| Descripción  | La aplicación comprueba periódicamente si el móvil ha estado en contacto de otro cuyo dueño haya dado positivo en la enfermedad.          |  
| Importancia  |          Muy alta                                                                | 
| Actores      |   Desarrolladores, persona positiva en COVID, centro de salud                                   |
| Comentarios  |                                                                          |


| 4.2.2.05           | Comprobar veracidad del código de positivo en COVID                           |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias |   4.2.2.03                                                                       |
| Descripción  | Si la persona ha introducido un código, la aplicación comprueba si el código es correcto.      |  
| Importancia  |   Alta                                                                       | 
| Actores      |  Desarrolladores, persona positiva en COVID                            |
| Comentarios  |                                                                          |


| 4.2.2.06           |  Notificación de riesgo                                                       |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias |   4.2.2.04, 4.2.2.05                                                                      |
| Descripción  | Si la persona ha estado en contacto con un positivo, la aplicación mandará un aviso.          |  
| Importancia  |     Muy alta                                                                     | 
| Actores      |  Desarrolladores, persona positiva en COVID, rastreadores                            |
| Comentarios  |  Esta acción se puede ver reforzada por los rastreadores.                                                          |


| 4.2.2.07           | Cumplimiento de cuarentenas                                                               |  
|--------------|---------------------------------------------------------------------------------------|  
| Versión      | 1.0                                                                                   |  
| Dependencias | 4.2.2.03, 4.2.2.04, 4.2.2.06                                                  |  
| Descripción  | Se puede obligar a una persona a cumplir cuarentena si es positivo o sospechoso.      |  
| Importancia  |   Alta                                                                                    |  
| Actores      | Fuerzas del estado, ciudadanos                                                    |  
| Comentarios  | Al principio de la pandemia, las cuarentenas eran de 14 días, pero su duración se ha reducido a 10.|  


| 4.2.2.08           |  Listado de pruebas                                                                        |  
|--------------|----------------------------------------------------------------------------------------|  
| Versión      | 1.0                                                                                    |  
| Dependencias | 4.2.2.03, 4.2.2.06                                                                        |  
| Descripción  | Listado de personas que deben hacerse la prueba. Si se oponen, las FFCCSE intervienen. |  
| Importancia  |  Alta                                                                                      |  
| Actores      | Centros de salud, fuerzas del orden, ciudadanos       |  
| Comentarios  |                                                                                        |  

| 4.2.2.09          | Rastreo                                                                         |  
|--------------|-----------------------------------------------------------------------------------------------|  
| Versión      | 1.0                                                                                           |  
| Dependencias | 4.2.2.01, 4.2.2.02, 4.2.2.03                                                           |  
| Descripción  | Con los resultados de las pruebas, los rastreadores pueden rastrear a aquellas personas contagiadas y tener un control sobre los contactos de dichas personas.  |  
| Importancia  |  Muy alta                                                                                   |  
| Actores      | Rastreadores  |  
| Comentarios  | Realizar una buena labor de rastreo permite que no se extiendan los contagios.                |


| 4.2.2.10           | Sacar estadísticas                                                                         |  
|--------------|-----------------------------------------------------------------------------------------------|  
| Versión      | 1.0                                                                                           |  
| Dependencias | 4.2.2.03, 4.2.2.07                                                                            |  
| Descripción  | Con los resultados de las pruebas, el Gobierno puede tomar medidas ajustadas a la situación.  |  
| Importancia  |                                                                                               |  
| Actores      | Centros de salud, Ministerio de sanidad, Gobierno/ consejerías de cada comunidad  |  
| Comentarios  | Pueden servir para comparar la gestión entre países y entre autonomías.                |



## 5 DESCRIPCIÓN DE LOS SUBSISTEMAS DEL SISTEMA A DESARROLLAR<a name="id5"></a>
| 5.01         | Subsistema de geolocalización                                            |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias | 4.2.1.02, 4.2.1.08                                                      |
| Descripción  | Rastrear y ver la ubicación de las personas para poder localizar a todas las personas que han estado en contacto con algún COVID-19 positivo.          |  
| Importancia  |Muy alta                                                                  | 
| Prioridad    |Muy alta                                                                  |
| Comentarios  |                                                                          |

| 5.02         | Subsistema sanitario                                                     |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias | 4.2.2.08                                                                 |
| Descripción  | Deben hacer las PCR a las personas con COVID-19 positivo que se encuentren en las listas, y en caso de que éstas no se presenten a la prueba, poner en conocimiento de las autoridades competentes (FFCCSSE) el incumplimiento de la prueba por parte de ese ciudadano.         |  
| Importancia  |Muy alta                                                                  | 
| Prioridad    |Muy alta                                                                  |
| Comentarios  |                                                                          |

| 5.03         | Subsistema de las FFCCSSE                                                |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias | 4.2.2.07                                                                      |
| Descripción  | Deben asegurar el cumplimiento de las cuarentenas impuestas a los ciudadanos, además de asegurar el también cumplimiento de las obligaciones de los mismos.          |  
| Importancia  |Muy alta                                                                  | 
| Prioridad    |Muy alta                                                                  |
| Comentarios  |                                                                          |

| 5.04         | Subsistema de notificación al usuario |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias | 4.2.1.01, 4.2.1.02                                                                      |
| Descripción  | Se debe notificar a los usuarios si han estado en contacto con un caso positivo  |  
| Importancia  |Muy alta                                                                  | 
| Prioridad    |Muy alta                                                                  |
| Comentarios  |                                                                          |

| 5.05         | Subsistema de analisis estadísticos                                                |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias | 4.2.2.03, 4.2.2.10                                                                      |
| Descripción  | Con los resultados de las pruebas, el Gobierno puede tomar medidas ajustadas a la situación.          |  
| Importancia  |Muy alta                                                                  | 
| Prioridad    |Muy alta                                                                  |
| Comentarios  |                                                                          |  

## 6. CATÁLOGO DE REQUISITOS DEL SISTEMA A DESARROLLAR<a name="id6"></a>
Poner estructura de directorios
### 6.1 Requisitos Generales del Sistema<a name="id61"></a>
| 6.1.01       |   Registrar usuarios                                                     |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias | 4.1.01                                                                   |
| Descripción  | El sistema deberá permitir que los usuarios se registren en la aplicación.|  
| Requisitos hijo|6.1.02                                                                  | 
| Importancia    |Muy alta                                                                |
| Prioridad    |Muy alta                                                                  |
| Estado       |Realizado                                                                 |
| Comentarios  |                                                                          | 

| 6.1.02       |   Registrar casos COVID-19 positivos                                     |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias | 4.1.01                                                                   |
| Descripción  | El sistema deberá permitir que los usuarios se registren con el código de COVID-19 positivo en la aplicación.|  
| Requisitos hijo|                                                                        | 
| Importancia    |Muy alta                                                                |
| Prioridad    |Muy alta                                                                  |
| Estado       |Realizado                                                                 |
| Comentarios  |                                                                          | 

| 6.1.03       |   Geolocalizar a los ciudadanos                                          |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias | 4.1.01, 4.1.02                                                           |
| Descripción  | El sistema deberá permitir que los ciudadanos estén geolocalizados.      |  
| Requisitos hijo|                                                                        | 
| Importancia  |Muy alta                                                                  |
| Prioridad    |Muy alta                                                                  |
| Estado       |En desarrollo                                                             |
| Comentarios  |                                                                          | 

| 6.1.04       |   Notificar contacto estrecho con un caso COVID-19 positivo              |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias | 4.1.01                                                                   |
| Descripción  | El sistema deberá permitir que los usuarios que hayan estado en contacto estrecho con un caso de COVID-19 positivo sean informados a través de una notificación.      |  
| Requisitos hijo|                                                                        | 
| Importancia  |Muy alta                                                                  |
| Prioridad    |Muy alta                                                                  |
| Estado       |Realizado                                                                 |
| Comentarios  |                                                                          | 

| 6.1.05       |   Realizar estadísticas derivadas de los datos recogidos.                |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias | 4.1.01, 4.1.04                                                           |
| Descripción  | El sistema deberá permitir obtener estadísticas de los datos que se recogen de cada caso. Estos datos serán posteriormente analizados objetivamente por el Ministerio de Sanidad.      |  
| Requisitos hijo|                                                                        | 
| Importancia  |Muy alta                                                                  |
| Prioridad    |Muy alta                                                                  |
| Estado       |En desarrollo                                                             |
| Comentarios  |                                                                          | 

### 6.2 Casos de uso del Sistema<a name="id62"></a>
#### 6.2.1 Diagrama de Casos de uso del Sistema<a name="id621"></a>
* Subsistema de geolocalización
<img src="https://github.com/irenepenasperez/pandemio/blob/main/geolocalizacion.png" title="CasosUsoGeolocalizacion" width="700">

* Diagrama de casos de uso del subsistema FFCCSSE
<img src="https://github.com/irenepenasperez/pandemio/blob/main/DiagramaCasosUsoFFCCSSE.jpg" title="CasosUsoFFCCSSE" width="700">

* Diagrama de casos de uso del subsistema sanitario
<img src="https://github.com/irenepenasperez/pandemio/blob/main/DiagramaCasosUsoSanitarios.png" title="CasosUsoSanitarios" width="700">

* Diagrama de casos de uso del subsistema notificar al usuario
<img src="https://github.com/irenepenasperez/pandemio/blob/main/notificacion.png" title="CasosUsoNotificarUsuario" width="700">

* Diagrama de casos de uso del subsistema analisis estadísticos
<img src="https://github.com/irenepenasperez/pandemio/blob/main/analisis.png" title="CasosUsoAnalisisEstadistico" width="700">

#### 6.2.2 Especificación de Actores del Sistema<a name="id622"></a>
* Subsistema de geolocalización

| 6.2.2.1           |      Proveedor de información de la geolocalización                            |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias |                                                 |
| Descripción  | Proveedor que almacena la información de geolocalización de los usuarios.       |  
| Comentarios  |  |

* Subsistema FFCCSSE

| 6.2.2.2      |FFCCSSE                                                                   |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias |                                                                          |
| Descripción  |Las fuerzas del orden tiene que velar por el cumplimiento de las cuarentenas impuestas a los ciudadanos, además de las obligaciones de los mismos.                                                               |  
| Comentarios  |                                                                          | 

* Subsistema sanitario

| 6.2.2.3           | Usuario                                |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias |                                                                          |
| Descripción  | Persona que acude al centro sanitario a realizarse una prueba, sea a través de un contacto positivo o por voluntad propia|  
| Comentarios  |                                                                          |

| 6.2.2.4     | Centro de salud/Sanitarios                           |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias |                                                                          |
| Descripción  |  Los sanitarios se encargarán de hacer los test PCR y de comunicar los resultados. Si una PCR es positiva, el centro de salud dará un código al paciente positivo. De acuerdo al Real Decreto-ley 21/2020 de medidas urgentes para hacer frente a la crisis sanitaria ocasionada por el COVID-19, las autoridades sanitarias pueden realizar a todo sospechoso de COVID-19 una prueba PCR.       |  
| Comentarios  |                                                                          |

* Subsistema análisis estadísticos

| 6.2.2.5     | Gobierno/Consejerías de cada comunidad                            |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias |                                                                          |
| Descripción  | Teniendo en cuenta las estadísticas de las pruebas el gobierno puede ordenar confinamientos domiciliarios para frenar el avance del virus y otras medidas apoyados en las estadísticas resultantes de los datos de la aplicación.       |  
| Comentarios  |                                                                          |

#### 6.2.3 Especificación de Casos de uso del Sistema<a name="id623"></a>

* Especificación de Casos de uso del subsistema de geolocalización

| 6.2.3.1      |Proporcionar datos de la ubicación actual                                                    |  
|--------------|--------------------------------------------------------------------------|  
| Versión      |1.0                                                                       |
| Dependencias |6.1.01, 6.1.03                                                                    |
| Precondición |El usuario debe ser positivo en COVID-19                                    |
| Descripción  |Se utilizará la información de la geolocalización del usuario actual para asegurarse de que está cumpliendo la cuarentena|  
| Postcondición|En caso de no cumplirse la cuarentena 6.2.3.3                                    | 
| Importancia  |Muy alta                                                                  |
| Prioridad    |Muy alta                                                                  |
| Estado       |En desarrollo                                                             |
| Comentarios  |                                                                          |

* Especificación de Casos de uso del subsistema de FFCCSSE

| 6.2.3.2      |Control de cuarentenas                                                    |  
|--------------|--------------------------------------------------------------------------|  
| Versión      |1.0                                                                       |
| Dependencias |6.1.01, 6.1.03                                                                     |
| Precondición |Debe haber casos positivos por COVID-19                                    |
| Descripción  |Las fuerzas del orden deben asegurarse de que las personas afectadas de COVID-19 cumplen la cuarentena obligatoria impuesta.                                                                                 |  
| Postcondición|La persona debe estar en su domicilio.                                    | 
| Importancia  |Muy alta                                                                  |
| Prioridad    |Muy alta                                                                  |
| Estado       |Realizado                                                                 |
| Comentarios  |                                                                          |

| 6.2.3.3      |Control de obligaciones                                                   |  
|--------------|--------------------------------------------------------------------------|  
| Versión      |1.0                                                                       |
| Dependencias |6.1.01                                                                    |
| Precondición |Debe haber obligaciones impuestas a los ciudadanos a a tenor de las restricciones que haya en dicho momento                                                                                   |
| Descripción  |Las fuerzas del orden deben asegurarse de que los ciudadanos cumplen las obligaciones que tienen durante la existencia de la pandemia.                                                                                 |  
| Postcondición|Los ciudadanos cumplen las obligaciones                                   | 
| Importancia  |Muy alta                                                                  |
| Prioridad    |Muy alta                                                                  |
| Estado       |Realizado                                                                 |
| Comentarios  |                                                                          |

| 6.2.3.4      |Control de realización de PCR                                             |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias |6.1.01, 6.1.02, 6.1.04, 6.1.05                                                                     |
| Precondición |Debe haber realización de PCR                                             |
| Descripción  |Las fuerzas del orden deben asegurarse de que las personas llamadas a hacerse las PCR cumplen con la obligación de acudir al centro sanitario a realizarse las pruebas                                                 |  
| Postcondición|La persona debe haberse hecho las pruebas pertinentes                     | 
| Importancia  |Muy alta                                                                  |
| Prioridad    |Muy alta                                                                  |
| Estado       |Realizado                                                                 |
| Comentarios  |                                                                          |

| 6.2.3.5      |Realizar intervención                                                     |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias |6.1.01, 6.1.03                                                                     |
| Precondición |Debe haber incumplimiento de cuarentena, obligaciones, o negativa a realizarse la PCR.|
| Descripción  |Las fuerzas del orden deberán intervenir en caso de que una persona no acuda o se niegue a  hacerse las pruebas, o de que los ciudadanos no cumplan las obligaciones, o en último caso de que la persona infectada por COVID-19 no guarde los días de cuarentena establecidos.                                                                             |  
| Postcondición|Las fuerzas del orden habrán realizado la intervención.                   | 
| Importancia  |Muy alta                                                                  |
| Prioridad    |Muy alta                                                                  |
| Estado       |Realizado                                                                 |
| Comentarios  |                                                                          |

* Especificación de Casos de uso del subsistema sanitario

| 6.2.3.6      |Recibir listado personas que deben hacerse PCR                    |  
|--------------|--------------------------------------------------------------------------|  
| Versión      |1.0                                                                       |
| Dependencias | 6.1.02, 6.1.04                                                                    |
| Precondición |Debe haber casos positvos por COVID-19                                    |
| Descripción  |Los centros sanitarios reciben un listado de personas que deben realizarse una PCR|  
| Postcondición|Deben realizar las PCR a los usuarios que se encuentran en la lista                                    | 
| Importancia  |Muy alta                                                                  |
| Prioridad    |Muy alta                                                                  |
| Estado       |Realizado                                                                 |
| Comentarios  |                                                                          |

| 6.2.3.7      |Notificar incumplimiento                    |  
|--------------|--------------------------------------------------------------------------|  
| Versión      |1.0                                                                       |
| Dependencias |6.2.3.5, 6.1.04                                                                   |
| Precondición |Un usuario que se encuentra en la lista de personas que deben realizarse PCR no asiste a realizarse la prueba                                    |
| Descripción  |El centro sanitario debe notificar a las FFCCSSE el incumplimiento del usuario.|  
| Postcondición|Los FFCCSSE tomarán las medidas necesarias.                                    | 
| Importancia  |Muy alta                                                                  |
| Prioridad    |Muy alta                                                                  |
| Estado       |Realizado                                                                 |
| Comentarios  |                                                                          |

| 6.2.3.8      |Realizar prueba                    |  
|--------------|--------------------------------------------------------------------------|  
| Versión      |1.0                                                                       |
| Dependencias |   6.2.3.5, 6.1.02, 6.1.04, 6.1.05                                                                 |
| Precondición |          |
| Descripción  |Se realiza la PCR a los usuarios que se encientran en la lista. También a los usuarios que acuden por su cuenta a realizarse la prueba asumiendo los gastos correspondientes |  
| Postcondición|Los usuarios que se hayan realizado la prueba deberán permanecer aislados hasta la comunicación del resultado, que en caso de ser positivo deberán permancer aislados hasta que se cumpla el plazo establecido          | 
| Importancia  |Muy alta                                                                  |
| Prioridad    |Muy alta                                                                  |
| Estado       |Realizado                                                                 |
| Comentarios  |El plazo de aislamiento establecido dependerá de los políticos y las C.A. |

| 6.2.3.9     |Comunicar resultado                    |  
|--------------|--------------------------------------------------------------------------|  
| Versión      |1.0                                                                       |
| Dependencias |   6.2.3.7, 6.1.02, 6.1.04                                                                 |
| Precondición |   Haber realizado una PCR       |
| Descripción  |El centro sanitario notificará al usuario el resultado de la prueba, y en caso de ser positivo le comunicará también el código asociado. |  
| Postcondición|El resultado habrá sido comunicado al usuario                             | 
| Importancia  |Muy alta                                                                  |
| Prioridad    |Muy alta                                                                  |
| Estado       |Realizado                                                                 |
| Comentarios  |       |

* Subsistema notificar al usuario

| 6.2.3.10     |Registrarse                    |  
|--------------|--------------------------------------------------------------------------|  
| Versión      |1.0                                                                       |
| Dependencias | 6.1.01                                                                  |
| Precondición |   Poseer un smartphone       |
| Descripción  |El usuario descargará la aplicación en su teléfono |  
| Postcondición|  El usuario podrá utilizar la aplicación                                 | 
| Importancia  |Muy alta                                                                  |
| Prioridad    |Muy alta                                                                  |
| Estado       |Realizado                                                                 |
| Comentarios  |       |

| 6.2.3.11     |Notificar positivo                    |  
|--------------|--------------------------------------------------------------------------|  
| Versión      |1.0                                                                       |
| Dependencias |   6.2.3.10, 6.1.02, 6.1.04                                                                 |
| Precondición |   Que el usuario reciba un diagnóstico positivo en la enfermedad.       |
| Descripción  | El usuario introduce en el sistema el código proporcionado por el centro sanitario con el que indica que es un contacto positivo. |  
| Postcondición|Comienza a seguirse el protocolo para localizar los contactos estrechos y asegurar el cumplimiento de la cuarentena.| 
| Importancia  |Muy alta                                                                  |
| Prioridad    |Muy alta                                                                  |
| Estado       |Realizado                                                                 |
| Comentarios  |       |

| 6.2.3.12     |Notificar contacto estrecho                    |  
|--------------|--------------------------------------------------------------------------|  
| Versión      |1.0                                                                       |
| Dependencias |   6.2.3.1, 6.1.02, 6.1.04                                                                |
| Precondición |   Haber un usuario positivo que sea contacto estrecho       |
| Descripción  |La aplicación comunicara al usuario que es un contacto estrecho de un caso positivo |  
| Postcondición|  6.2.3.9                                  | 
| Importancia  |Muy alta                                                                  |
| Prioridad    |Muy alta                                                                  |
| Estado       |Realizado                                                                 |
| Comentarios  |       |

* Subsistema análisis estadísticos

| 6.2.3.13     | Consultar datos                    |  
|--------------|--------------------------------------------------------------------------|  
| Versión      |1.0                                                                       |
| Dependencias | 6.1.05                                                                |
| Precondición | El sistema debe haber generado informes con los datos recogidos       |
| Descripción  | El gobierno puede consultar los datos recogidos por la aplicación. |  
| Postcondición| A partir de estos datos se pueden tomar medidas de actuación.                | 
| Importancia  |Muy alta                                                                  |
| Prioridad    |Muy alta                                                                  |
| Estado       |En desarrollo                                                             |
| Comentarios  |       |

| 6.2.3.14     | Realizar análisis estadísticos                    |  
|--------------|--------------------------------------------------------------------------|  
| Versión      |1.0                                                                       |
| Dependencias | 6.2.3.13, 6.1.05                                                                 |
| Precondición |  Haber consultado las estadíscticas de las pruebas       |
| Descripción  | El gobierno puede realizar análisis estadísticos a partir de los datos y tomar medidas para frenar el avance de la pandemia en caso de que las estadísticas sean preocupantes o rebajar medidas en caso de que sean favorables. |  
| Postcondición|                                  | 
| Importancia  |Muy alta                                                                  |
| Prioridad    |Muy alta                                                                  |
| Estado       |En desarrollo                                                             |
| Comentarios  |       |

### 6.3 Requisitos Funcionales del Sistema<a name=""></a>
#### 6.3.1 Requisitos de Información del Sistema<a name="id631"></a>
| 6.3.1.1         |   Guardar información del usuario                                              |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias | 6.1.01, 6.1.02, 6.1.03, 6.1.04                                                  |
| Descripción  |   El sistema guardará datos del usuario, en concreto guardará la geolocalización y el nombre de usuario, junto con los códigos de positivo en COVID asociados a dicho usuario.        |  
| Datos específicos  |                                                                  | 
| Importancia    |  Alta                                                                |
| Prioridad    |  Alta                                                                |
| Estado    |En desarrollo                                                                  |
| Comentarios  |  El sistema almacenará la información de geolocalización sólo el tiempo necesario para garantizar el cumplimiento de las leyes de protección de datos               |

| 6.3.1.2         |  Códigos generados por la aplicación                                               |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias | 6.1.04                                                                   |
| Descripción  |  El sistema guardará los códigos autogenerados por la aplicación durante un máximo de 14 días.          |  
| Datos específicos  |                                                                  | 
| Importancia    |  Alta                                                                |
| Prioridad    |   Alta                                                          |
| Estado    |Realizado                                                                  |
| Comentarios  | Estos códigos se almacenarán en un servidor del gobierno y se destruirán cuando hayan pasado 14 días desde que han sido generados.           |

#### 6.3.2 Requisitos de Reglas de Negocio del Sistema<a name=""></a>
| 6.3.2.1      |   Información personal                                              |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias | 6.1.03                                                                   |
| Descripción  |  Los datos personales de los usuarios no pueden utilizarse para otros fines que los sanitarios.          |  
| Importancia    | Media                                                                 |
| Prioridad    |  Media                                                                |
| Estado    |Realizado                                                                  |
| Comentarios  |                                                                          |

| 6.3.2.2         |   Introducción de código de diagnóstico                                              |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias | 6.1.01, 6.1.02                                                                  |
| Descripción  |  El sistema permitirá que los usuarios que se han identificado introduzcan un código de diagnóstico positivo en un prueba de la enfermedad.           |  
| Importancia    |   Alta                                                               |
| Prioridad    | Alta                                                                 |
| Estado    |Realizado                                                                  |
| Comentarios  |    El sistema comprobará la validez del código introducido.                                                                      |

| 6.3.2.3         |   Estado de riesgo                                              |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias | 6.1.01, 6.1.02, 6.1.04                                                                 |
| Descripción  |  La aplicación debe emitir un mensaje en caso de que el usuario esté expuesto a riesgo de contagio por haber tenido un contacto estrecho con un contagiado.          |  
| Importancia    |  Muy alta                                                                |
| Prioridad    |   Alta                                                               |
| Estado    | Realizado                                                                 |
| Comentarios  |                                                                         |

| 6.3.2.4         |   Informe de nuevos contagiados                                              |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias |  6.3.2.2, 6.1.02, 6.1.04, 6.1.05                                                                     |
| Descripción  |  El sistema generará diariamente un informe con los nuevos usuarios contagiados para llevar un control.          |  
| Importancia    |   Muy alta                                                               |
| Prioridad    |    Muy alta                                                              |
| Estado    |  En desarrollo                                                                |
| Comentarios  |  Gracias a este informe, las FFCCSE podrán llevar un control del cumplimiento de las cuarentenas.              |

| 6.3.2.5         |   Informe de personas que han estado en contacto con positivos                                             |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias |  6.1.02, 6.3.2.4, 6.1.05                                                                     |
| Descripción  |  El sistema generará diariamente un informe con los nuevos usuarios que están en estado de riesgo debido a un contacto estrecho con una persona contagiada de COVID.          |  
| Importancia    |   Muy alta                                                               |
| Prioridad    |    Muy alta                                                              |
| Estado    | En desarrollo                                                                 |
| Comentarios  |  Este informe permitirá a los sanitarios conocer a qué personas deben realizarles las pruebas.                |

| 6.3.2.6      |La aplicación debe asegurar la protección de datos y la privacidad         |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias | 6.1.01, 6.1.03, 6.1.04                                                                   |
| Descripción  |La aplicación deberá asegurar mediante cifrado la confidencialidad de los datos y de las personas|   
| Importancia    |   Alta                                                               |
| Prioridad    |    Alta                                                              |
| Estado    | En desarrollo                                                                 |
| Comentarios  |                                                                          |

| 6.3.2.7      |La aplicación debe tener métodos de autenticación e identificación         |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias | 6.1.01                                                                      |
| Descripción  |La aplicación deberá autenticar e identificar a las personas              |   
| Importancia    |  Alta                                                                |
| Prioridad    |    Alta                                                              |
| Estado    | En desarrollo                                                                 |
| Comentarios  |                                                                          |

| 6.3.2.8      |La aplicación debe asegurar los accesos al sistema                         |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias | 6.1.01                                                                      |
| Descripción  |La aplicación deberá asegurar que sólo las personas autorizadas tienen acceso al sistema|   
| Importancia    |   Alta                                                               |
| Prioridad    | Alta                                                                |
| Estado    | Realizado                                                                 |
| Comentarios  |                                                                          |

| 6.3.2.9      |El usuario no debe tener acceso a los informes de positivos y sospechosos                         |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias | 6.1.04, 6.1.05                                                                      |
| Descripción  |Los informes generados no deben ser accesibles para los usuarios de la aplicación.|   
| Importancia    |   Alta                                                               |
| Prioridad    |   Media                                                               |
| Estado    | Realizado                                                                 |
| Comentarios  |                                                                          |

#### 6.3.3 Requisitos de Conducta del Sistema<a name="id633"></a>
| 6.3.3.1         |  Solicitud de estado de riesgo                                               |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias |  6.3.2.3, 6.1.01, 6.1.04                                                                     |
| Descripción  |  El usuario podrá solicitar al sistema el estado de riesgo en el que se encuentra. A la hora de generar la respuesta, el sistema tendrá en cuenta los códigos autogenerados por la aplicación en los dispositivos de los contactos estrachos del usuario. |  
| Interfaz de Servicio  |                                                                  | 
| Importancia    |  Alta                                                                |
| Prioridad    |   Alta                                                               |
| Estado    |  Realizado                                                                |
| Comentarios  | Los estados pueden ser: sin riesgo o con riesgo.          |

| 6.3.3.2         |  Aviso de incumplimiento de cuarentena                                               |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias |  6.3.2.4, 6.1.01, 6.1.03                                                                    |
| Descripción  |  El sistema podrá generar un aviso cuando se detecte mediante el sistema de geolocalización que un usuario contagiado incumple la cuarentena.          |  
| Interfaz de Servicio  |                                                                  | 
| Importancia    |  Alta                                                                |
| Prioridad    |        Alta                                                          |
| Estado    | En desarollo                                                                  |
| Comentarios  | A estos informes tendrán acceso las FFCCSE y podrán actuar de acuerdo a las normas.          |

| 6.3.3.3         |  Aviso de incumplimiento de prueba                                               |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias |  6.3.2.3, 6.3.2.5, 6.1.01                                                                     |
| Descripción  |  El sistema podrá generar un aviso cuando se detecte que un usuario con riesgo de contagio incumple la obligación de realizarse la prueba.          |  
| Interfaz de Servicio  |                                                                  | 
| Importancia    |  Alta                                                                |
| Prioridad    |        Alta                                                          |
| Estado    |  En desarrollo                                                                |
| Comentarios  | A estos informes tendrán acceso las FFCCSE y podrán actuar de acuerdo a las normas.          |

### 6.4 Requisitos No Funcionales del Sistema<a name="id64"></a>

#### 6.4.1 Requisitos de Fiabilidad<a name="id641"></a>
Estiman la probabilidad de que el software falle durante un período de tiempo.
| 6.4.1.1      | La aplicación debe tener tolerancia a fallos                             |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias |                                                                          |
| Descripción  |El sistema tendrá la capacidad de seguir funcionando aún en caso de producirse algún fallo en el sistema.|   
| Importancia  |Alta                                                                      |
| Prioridad    | Alta                                                                         |
| Estado       | En desarrollo                                                            |
| Comentarios  |                                                                          |

| 6.4.1.2      | La aplicación debe tener la propiedad de recuperabilidad                 |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias |                                                                          |
| Descripción  |El sistema debe tener la capacidad de restablecer un nivel específico de rendimiento y recuperar la información directamente afectada en caso de fallo.|   
| Importancia  |Alta                                                                      |
| Prioridad    | Alta                                                                         |
| Estado       |En desarrollo                                                             |
| Comentarios  |                                                                          |

| 6.4.1.3      | La aplicación debe tener madurez                                         |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias |                                                                          |
| Descripción  |La aplicación debe seguir el modelo de madurez. Este se conforma de 5 estándares (Nivel 0, el “sentido común”; Nivel 1, el cumplimiento de la legislación obligatoria; Nivel 2, evaluación del proceso de Gestión de Seguridad; Nivel 3, analizar el riesgo y la gestión de su resolución, Nivel 4, adquisición de productos para integrarlos en los Sistemas de Gestión; Nivel 5, integración de los componentes certificados en sistemas compuestos y su certificación.) |
| Importancia  |Alta                                                                      |
| Prioridad    | Media                                                                         |
| Estado       |En desarrollo                                                             |
| Comentarios  |                                                                          |

#### 6.4.2 Requisitos de Usabilidad<a name="id642"></a>
La usabilidad comprende todos aquellos factores que hacen que la aplicación sea fácil de usar.

| 6.4.2.1      | La aplicación debe ser intuitiva                                         |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias | 6.1.01, 6.1.02, 6.1.04                                                                       |
| Descripción  | La aplicación debe ser fácil de manejar, teniendo en cuenta que la población entera la va a usar, y hay determinados sectores que no están famirializados con las nuevas tecnologías.                                   |   
| Importancia  | Alta                                                                     |
| Prioridad    | Alta                                                                     |
| Estado       | En desarrollo                                                            |
| Comentarios  |                                                                          |

| 6.4.2.2      | La aplicación debe tener una interfaz amigable                           |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias | 6.1.01, 6.1.02, 6.1.04                                                                         |
| Descripción  | Ídem que la descripción del apartado anterior                            |   
|Importancia   |Alta                                                                      |
| Prioridad    | Media                                                                    |
| Estado       | En desarrollo                                                            |
| Comentarios  |                                                                          |

| 6.4.2.3      | La aplicación debe tener cierto grado de internacionalización            |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias |                                                                          |
| Descripción  | La aplicación debe estar en varios idiomas para que los usuarios de distintos países sean capaces de usarlas       |   
|Importancia   |Alta                                                                      |
| Prioridad    | Media                                                                         |
| Estado       |En desarrollo                                                             |
| Comentarios  |                                                                          |

| 6.4.2.4      | Fácil de instalar y desinstalar            |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias | 6.1.01, 6.1.02, 6.1.04                                                                         |
| Descripción  | La aplicación debe ser fácil de instalar y desinstalar. Se puede obtener la aplicación desde App Store y desde Play Store.         |   
|Importancia   |Alta                                                                      |
| Prioridad    | Media                                                                         |
| Estado       | En desarrollo                                                            |
| Comentarios  |                                                                          |

| 6.4.2.5      | Tiempo de aprendizaje de uso de la aplicación                            |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias | 6.1.01, 6.1.02, 6.1.04                                                                         |
| Descripción  | El tiempo de aprendizaje de la utilización de la aplicación por parte del usuario no debe ser superior a 10 minutos.   |   
|Importancia   |Baja                                                                      |
| Prioridad    |  Baja                                                                    |
| Estado       |En desarrollo                                                             |
| Comentarios  |                                                                          |

#### 6.4.3 Requisitos de Eficiencia<a name="id643"></a>
La eficiencia determina lo bien que el sistema utiliza la capacidad de cómputo
disponible, espacio de almacenamiento, memoria, ancho de banda...

| 6.4.3.1      |Comportamiento en el tiempo del software                                  |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias |                                                                          |
| Descripción  |Los tiempos de respuesta y procesamiento de la BD deben ser óptimos para el buen funcionamiento de la aplicación|   
| Importancia  |Muy alta                                                                  |
| Prioridad    |  Alta                                                                    |
| Estado       | En desarrollo                                                            |
| Comentarios  |                                                                          |

| 6.4.3.2      |Comportamiento según otros recursos                                       |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias | 6.1.03, 6.1.04                                                                         |
| Descripción  |Se utilizarán los recursos estrictamente necesarios para que la aplicación funcione. Se usarán las geolocalizaciones de las personas y sus datos personales en caso de tener que notificar positivos o de que se ha estado en contacto con un positivo.|   
| Importancia  |Muy alta                                                                  |
| Prioridad    |   Alta                                                                   |
| Estado       |   En desarrollo                                                          |
| Comentarios  |                                                                          |

| 6.4.3.3      |Capacidad del software                                       |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias | 6.1.02, 6.1.04                                                                         |
| Descripción  |La capacidad será aquella que permita que se puedan registrar casos positivos y que funcione debidamente la aplicación|   
| Importancia  |Muy alta                                                                  |
| Prioridad    |  Alta                                                                    |
| Estado       | En desarrollo                                                            |
| Comentarios  |                                                                          |

| 6.4.3.4      |Uso del espacio                                      |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias | 6.1.01, 6.1.03, 6.1.04                                                                        |
| Descripción  |La aplicación no deberá ocupar más de 5MB de espacio. |   
| Importancia  |Media                                                                  |
| Prioridad    |  Media                                                                |
| Estado       | En desarrollo                                                            |
| Comentarios  |                                                                          |

| 6.4.3.5      |Consumo de la aplicación                                       |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias |                                                                          |
| Descripción  |El consumo de batería de la aplicación debe ser menor del 2%. |   
| Importancia  |Media                                                                  |
| Prioridad    |   Media                                                               |
| Estado       | En desarrollo                                                              |
| Comentarios  |                                                                          |

#### 6.4.4 Requisitos de Mantenibilidad<a name="id644"></a>
| 6.4.4.1        | La aplicación debe ser estable                                           |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias |                                                                     |
| Descripción  |  La aplicación no debe tener fallos o si es inevitable, tener un número ínfimo de los mismos.          |   
| Importancia    |    Alta                                                              |
| Prioridad    |    Media                                                              |
| Estado    |    En desarrollo                                                              |
| Comentarios  |                                                                          |

| 6.4.4.2        | La aplicación debe tener facilidad para ser cambiada                     |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias |                                                                       |
| Descripción  |La aplicación debe ser flexible para que no sea muy costoso(monetariamente y temporalmente) realizar cambios|   
| Importancia    |    Media                                                              |
| Prioridad    |    Media                                                              |
| Estado    |    En desarrollo                                                               |
| Comentarios  |                                                                          |

#### 6.4.5 Requisitos de Portabilidad<a name="id645"></a>
La portabilidad cuantifica el esfuerzo necesario para migrar el sistema entre dos
entornos operativos.

| 6.4.5.1      |  La aplicación debe tener capacidad de compatibilidad con hardware y software|  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias |                                                                       |
| Descripción  | La aplicación debe ser compatible en múltiples S.O. para que sea usada por el mayor número de personas posibles|   
| Importancia    |  Alta                                                                |
| Prioridad    | Muy alta                                                                 |
| Estado    |     En desarrollo                                                             |
| Comentarios  |                                                                          |

#### 6.4.6 Requisitos de Seguridad<a name="id646"></a>
La seguridad asegura la protección del sistema frente a ataques maliciosos.

| 6.4.6.1      |La aplicación debe asegurar la protección de datos y la privacidad         |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias | 6.1.02, 6.1.03, 6.1.04                                                                      |
| Descripción  |La aplicación deberá asegurar mediante cifrado la confidencialidad de los datos y de las personas|   
| Importancia    |   Alta                                                               |
| Prioridad    |     Alta                                                             |
| Estado    |    En desarrollo                                                              |
| Comentarios  |                                                                          |

| 6.4.6.2      |La aplicación debe tener métodos de autenticación e identificación         |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias | 6.1.01, 6.1.02, 6.1.04                                                                      |
| Descripción  |La aplicación deberá autenticar e identificar a las personas              |   
| Importancia    |  Alta                                                                |
| Prioridad    |    Alta                                                             |
| Estado    |   En desarrollo                                                               |
| Comentarios  |                                                                          |

| 6.4.6.3      |La aplicación debe asegurar los accesos al sistema                         |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias | 6.1.01, 6.1.02, 6.1.04                                                                      |
| Descripción  |La aplicación deberá asegurar que sólo las personas autorizadas tienen acceso al sistema|   
| Importancia    |   Alta                                                               |
| Prioridad    |    Alta                                                              |
| Estado    |  En desarrollo                                                                |
| Comentarios  |                                                                          |

#### 6.4.7 Otros Requisitos No Funcionales<a name="id647"></a>
| 6.4.7.1         |  Lenguaje de desarrollo de la aplicación                             |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias |                                                                       |
| Descripción  |  La aplicación se desarrollará en lenguaje Java.          |   
| Importancia    |                                                                  |
| Prioridad    |   Alta                                                                   |
| Estado       |En desarrollo                                                             |
| Comentarios  |                                                                          |

### 6.5 Restricciones Técnicas del Sistema<a name="id65"></a>
| 6.5.1        | Tenencia de smartphone                                                   |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias | 6.1.01, 6.1.02, 6.1.03, 6.1.04, 6.1.05                                   |
| Descripción  | No todas las personas del país tienen smartphone, por lo que no podrían instalar la aplicación|  
| Importancia    |  Muy alta                                                                |
| Prioridad    |     Alta                                                             |
| Estado    |  En desarrollo                                                                |
| Comentarios  |                                                                          |

| 6.5.2        | Conectividad a Internet                                                   |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias | 6.1.01, 6.1.02, 6.1.03, 6.1.04, 6.1.05                                   |
| Descripción  | No todas las personas del país tienen acceso a Internet, sobre todo en zonas rurales del interior del país. Hay zonas muertas de cobertura, y la aplicación no podría mandar ni recibir datos, por lo que no funcionaría correctamente.|  
| Importancia    |  Alta                                                                |
| Prioridad    |    Alta                                                              |
| Estado    |  En desarrollo                                                          |
| Comentarios  |                                                                          |

| 6.5.3        | La aplicación debe estar disponible para sistemas Android e iOS                                            |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias | 6.1.01, 6.1.02, 6.1.03, 6.1.04, 6.1.05                                   |
| Descripción  | La aplicación se debe poder descargar para dispositivos con sistema Android y con sistema iOS.|  
| Importancia    |  Alta                                                                |
| Prioridad    |  Alta                                                                |
| Estado    |  En desarrollo                                                                |
| Comentarios  |                                                                          |

| 6.5.4        | Espacio disponible en el dispositivo                                          |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias | 6.1.01, 6.1.02, 6.1.03, 6.1.04, 6.1.05                                   |
| Descripción  | El dispositivo debe tener suficiente espacio en memoria para almacenar la aplicación.|  
| Importancia    |  Alta                                                                |
| Prioridad    |  Alta                                                                |
| Estado    |   En desarrollo                                                               |
| Comentarios  |                                                                          |

### 6.6 Requisitos de Integración del Sistema<a name="id66"></a>
| 6.6.1        | El sistema dispondrá de  servidores (nube)                                                |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias | 6.1.01, 6.1.02, 6.1.03, 6.1.04, 6.1.05                                   |
| Descripción  |Estos servidores almacenarán más tarde información relacionada con la aplicación|  
| Importancia    | Muy alta                                                                 |
| Prioridad    |  Alta                                                                |
| Estado    |  En desarrollo                                                                |
| Comentarios  |                                                                          |

| 6.6.2        |El sistema dispondrá de una base de datos                                     |  
|--------------|--------------------------------------------------------------------------|  
| Versión      | 1.0                                                                      |
| Dependencias |                                                                       |
| Descripción  |La base de datos almacenará todos los datos de la aplicación          |  
| Importancia    |  Muy alta                                                                |
| Prioridad    |    Alta                                                              |
| Estado    |   En desarrollo                                                               |
| Comentarios  |                                                                          |

### 6.7 Información sobre Trazabilidad<a name="id67"></a>

| Casos de uso/ Requisitos generales|6.2.3.1|6.2.3.2|6.2.3.3|6.2.3.4|6.2.3.5|6.2.3.6|6.2.3.7|6.2.3.8|6.2.3.9|6.2.3.10|6.2.3.11|6.2.3.12|6.2.3.13|6.2.3.14|
|-------|---------|---------|-------|--------|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
|  6.1.01     |   X      |    X     |  X     |   X     | X |  |  |  |  | X |  |  |  |  |
|  6.1.02     |         |         |       |    X    |  | X |  | X | X |  | X | X |  |  |
|  6.1.03     |    X     |   X      |       |        | X |  |  |  |  |  |  |  |  |  |
|  6.1.04     |         |         |       |   X     |  | X | X | X | X |  |X  | X |  |  |  
|  6.1.05     |         |         |       |   X     |  |  |  | X |  |  |  |  | X | X |

| Requisitos de información/ Requisitos generales      |  6.3.1.1       |   6.3.1.2      | 
|-------------|---------|---------|
|  6.1.01     |   X      |         |
|  6.1.02     |   X      |         |
|  6.1.03     |   X      |         |
|  6.1.04     |   X      |   X      |
|  6.1.05     |         |         |

| Reglas de negocio/ Requisitos generales      | 6.3.2.1| 6.3.2.2  | 6.3.2.3 | 6.3.2.4 |6.3.2.5| 6.3.2.6  | 6.3.2.7 | 6.3.2.8 |6.3.2.9|
|-------|---------|---------|-------|--------|--------|---------|-------|--------|--------|
|  6.1.01     |         |   X      |    X   |        |        |    X     |   X    |     X   |        |
|  6.1.02     |         |   X      |   X    |    X    |   X     |         |       |        |        |
|  6.1.03     |   X      |         |       |        |        |    X     |       |        |        |
|  6.1.04     |         |         |   X    |   X     |    X    |   X      |       |        |    X    |
|  6.1.05     |         |         |       |   X     |     X   |         |       |        |    X    |

| Requisitos de conducta/ Requisitos generales      |  6.3.3.1       |  6.3.3.2       | 6.3.3.3      |  
|-------|---------|---------|-------|
|  6.1.01     |   X      |    X     |   X    |
|  6.1.02     |         |         |       |
|  6.1.03     |         |   X      |       |
|  6.1.04     |    X     |         |       |
|  6.1.05     |         |         |       |

| Requisitos no funcionales/ Requisitos generales      | 6.1.01        |  6.1.02       | 6.1.03      |  6.1.04      |  6.1.05   |
|-------|---------|---------|-------|--------|---------|
|  6.4.1.1     |         |         |       |        |        |
|  6.4.1.2     |         |         |       |        |        |
|  6.4.1.3     |         |         |       |        |        |
|  6.4.2.1     |    X     |     X    |       |  X      |        |
|  6.4.2.2     |    X     |     X    |       |    X    |        |
|  6.4.2.3     |         |         |       |        |        |
|  6.4.2.4     |    X     |     X    |       |    X    |        | 
|  6.4.2.5     |     X    |    X     |       |    X    |        |
|  6.4.3.1     |         |         |       |        |        |
|  6.4.3.2     |         |         |   X    |   X     |        |
|  6.4.3.3     |         |    X     |       |   X     |        |
|  6.4.3.4     |    X     |    X     |       |   X     |        |
|  6.4.3.5     |         |         |       |        |        |
|  6.4.4.1     |         |         |       |        |        |
|  6.4.4.2     |         |         |       |        |        |
|  6.4.5.1     |         |         |       |        |        |
|  6.4.6.1     |         |    X     |   X    |   X     |        |
|  6.4.6.2     |   X      |    X     |       |    X    |        |
|  6.4.6.3     |   X      |    X     |       |    X    |        |
|  6.4.7.1     |         |         |       |        |        |   

| Restricciones técnicas/ Requisitos generales      |  6.5.1       | 6.5.2        | 6.5.3      |  6.5.4      |   
|-------|---------|---------|-------|-------|
|  6.1.01     |   X      |   X      |   X    |   X    |
|  6.1.02     |   X      |   X      |   X    |    X   |
|  6.1.03     |   X      |   X      |   X    |     X  |
|  6.1.04     |   X      |   X      |   X    |     X  |
|  6.1.05     |         |         |       |       |

| Requisitos de integración/ Requisitos generales      |  6.6.1       |  6.6.2       |  
|-------|---------|---------|
|  6.1.01     |    X     |    X     |
|  6.1.02     |    X     |    X     |
|  6.1.03     |    X     |    X     |
|  6.1.04     |    X     |    X     |
|  6.1.05     |         |         |

## 7. ANEXOS<a name="id7"></a>
### 7.1 Anexo A: Actas de Reuniones<a name="id71"></a>
<a href="https://github.com/irenepenasperez/pandemio/blob/main/ActasDeReunion.md">Enlace a las actas de reuniones</a> 

### 7.2 Anexo B: Documentación Relevante<a name="id72"></a>
<a href="https://www.mscbs.gob.es/profesionales/saludPublica/ccayes/alertasActual/nCov/documentos/Preguntas_y_respuestas_RADAR-COVID.pdf">Enlace a la especificación y características de Radar Covid</a> 
<br>
<a href="https://www.boe.es/buscar/pdf/2018/BOE-A-2018-16673-consolidado.pdf">Enlace a la LOPD</a> 
<br>
<a href="http://www.juntadeandalucia.es/servicios/madeja/contenido/recurso/408">Tipos de requisitos no funcionales</a> 
<br>
<a href="http://www.juntadeandalucia.es/servicios/madeja/contenido/recurso/407 ">Enlace a algunas plantillas usadas</a> 

### 7.3 Anexo C: Glosario de Términos y Abreviaturas<a name="id73"></a>
* App: Aplicación
* C.A: Comunidad Autónoma
* COVID-19: coronavirus
* FFCCSSE: Fuerzas y Cuerpos de Seguridad del Estado
* GPS: Global Positioning System
* ID: identification
* LOPD: Ley Orgánica de Protección de Datos
* PCR: Polymerase Chain Reaction
* Radar: radio detectin and ranging
