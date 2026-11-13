PROYECTO

# Especificación de Requerimientos de Software (ERS)

## Plataforma Integral de Gestión y Visibilización de Ferias Locales en Bahía Blanca

**Analistas de requerimientos**: Murano Manuel, Torres Fernandez Sergio, Martinez Facundo, Lourdes De Andres, Cisneros Nahuel . 
--------------------------
## Indice
   1. Introducción
   2. Necesidades del negocio 	
   3. Descripción general	
   4. Características del sistema	
   5. Requerimientos de la interfaz externa	
   6. Otros requerimientos no funcionales	
   7. Apéndices	
   8. Anexos
--------------------------
 
## 1. Introducción
   
Propósito: Documentar los requerimientos funcionales y no funcionales necesarios para el desarrollo de una plataforma web y móvil destinada a la gestión y jerarquización de las ferias locales de Bahía Blanca. Como premisa fundamental, el sistema buscará respaldar activamente a los feriantes que mantengan un compromiso constante con las convocatorias, cumplan con las normativas regulatorias y consoliden su actividad como un negocio formal y saludable para el crecimiento de minipymes y emprendedores regionales.  

Convenciones del documento: El documento se estructura según el estándar ERS visto en la cátedra para el ciclo de vida del software, basándonos en las reglas del sector ferial local.

Audiencia del proyecto y sugerencias de lectura: El texto está dirigido a los futuros desarrolladores del sistema, analistas, diseñadores de bases de datos.
 Alcance del Proyecto: La plataforma busca organizar la información dispersa sobre las ferias de la ciudad. Conectará a los ciudadanos (a través de un mapa interactivo), a los feriantes (mediante registro y listas de espera) y a los organizadores/Municipio (para tareas de fiscalización y armado de estadísticas).

### Referencias: 

●  Informe "Primeras aproximaciones al fenómeno de las ferias en Bahía Blanca" (Cantamutto et al., 2023).

●  Ordenanza 11.947 de la Municipalidad de Bahía Blanca.

●  Material de la Unidad 2 de Prácticas Profesionalizantes 1.

--------------------------
## 2. Necesidades del negocio

Situación actual: En la ciudad de Bahía Blanca se identifican 21 ferias de funcionamiento regular (artesanales, de emprendedores, de productores agroecológicos y de economía popular), relevadas en el informe “Primeras aproximaciones al fenómeno de las ferias en Bahía Blanca” (Cantamutto et al., 2023). Dicho relevamiento constató la ausencia de una fuente oficial centralizada que documente su funcionamiento, organización y participantes: solo una minoría de las ferias cuenta con reconocimiento formal por parte de la Municipalidad, mientras que la difusión del resto depende exclusivamente de canales informales (redes sociales de organizadores y feriantes).
Problemas detectados:
Inexistencia de un canal único de consulta pública sobre oferta ferial (ubicación, horarios, rubros disponibles).
Variabilidad en la ubicación de varias ferias, sin mecanismo de actualización accesible para el usuario final.
Ausencia de una herramienta municipal de relevamiento estadístico que permita monitorear el crecimiento del sector, los rubros con mayor actividad y el nivel de regularización de los participantes.
Marco normativo vigente (Ordenanza 11.947/2003) desactualizado respecto de la heterogeneidad actual del sector, con vacíos de control en rubros sensibles (producción alimentaria artesanal: conservas, chacinados).

Alcance del sistema: El sistema deberá dar soporte a los tres actores identificados:

1-Ciudadanía: centralización de la oferta ferial en un mapa interactivo, con información de horarios, ubicación, rubros y contacto de feriantes.

2-Feriantes y organizadores independientes: visibilización de puestos y formalización de los requisitos de participación.

3-Municipio: disponibilidad de una herramienta de Business Intelligence para el monitoreo del sector, la identificación del nivel de regularización y la detección de necesidades de asistencia o capacitación (en coordinación con el área de Bromatología).

Fuera de alcance: gestión de ferias de carácter esporádico o de escala no representativa, y automatización de trámites de habilitación municipal (continúan gestionando por los canales administrativos vigentes).

Factores críticos de éxito (sin ellos el sistema no cumple su propósito):

-Que el mapa de ferias muestre información real y actualizada (ubicación, horario, vigencia).
-Que la asignación de puestos y la fila de espera nunca dupliquen un mismo lugar entre dos feriantes.
-Que la fiscalización sanitaria pueda verificarse en el momento, en terreno, desde el celular del inspector.
-Que el sistema cumpla la normativa de protección de datos personales (Ley 25.326) y las ordenanzas municipales vigentes.

Puntos fuertes/débiles del sistema actual

Situación actual: <ins>puntos fuertes y débiles</ins>
No existe hoy un sistema de información para las ferias de Bahía Blanca; el "sistema actual" es un conjunto de prácticas manuales e informales. Esta caracterización se basa en el informe "Primeras aproximaciones al fenómeno de las ferias en Bahía Blanca" (Cantamutto et al., 2023), que relevó 21 ferias de funcionamiento regular en la ciudad.

Puntos fuertes:
El sector está consolidado: hay 21 ferias regulares identificadas, varias con larga trayectoria (Feria del Lago desde 2004; Parque Independencia y Encuentro de Pato desde 2008).
El Municipio ya interviene en la organización de al menos 5 ferias y otorga permisos de funcionamiento en espacio público a otras.
Existe un marco normativo de base (Ordenanza 11.947/2003) y un mapa oficial (Bahía Georeferenciada) donde se listan algunas ferias municipales.
Los feriantes ya usan activamente redes sociales (Instagram, Facebook) para difundir fechas y ubicaciones, lo que da una base de datos a digitalizar.
En varios casos hay articulación con organizaciones (INTA, UNS, Cáritas, sociedades de fomento) que podrían integrarse como actores del sistema.

Puntos débiles:
No hay un estudio sistemático ni información oficial centralizada sobre funcionamiento, organización e integrantes de las ferias; ninguna entidad centraliza su dinámica.
La difusión depende del esfuerzo individual de cada feriante u organizador, sin un canal único: esto dificulta que el público sepa qué ferias funcionan hoy y en qué horario, ya que muchas ferias no tienen ubicación ni horario fijo.
La Ordenanza 11.947 (2003) está desactualizada: fue pensada para regular "mercados de pulgas" centrándose en el origen de la mercadería, no en condiciones sanitarias, bromatológicas ni en los derechos de los feriantes.
No hay datos estadísticos sistemáticos sobre crecimiento del sector, rubros con mayor demanda ni nivel de regularización de las ferias.
No existe un mecanismo digital de fiscalización en terreno (bromatología/seguridad alimentaria) ni trazabilidad de permisos y habilitaciones sanitarias.
La difusión oficial por parte de la Municipalidad es escasa y despareja entre ferias (algunas con varias menciones en el sitio oficial, la mayoría sin ninguna).



## 3. Descripción general
   
a) Perspectiva del producto: Será un sistema web independiente que utilizará APIs* de mapas (Google Maps) para mostrar la información del circuito de ferias de la ciudad en tiempo real.

b) Características del producto: Permite gestionar perfiles de usuarios, ubicar ferias itinerantes y fijas, automatizar la fila de espera para los puestos, cargar actas de inspección y visualizar datos estadísticos.

c) Clases y características del usuario: Abarca desde vecinos sin conocimientos técnicos avanzados hasta inspectores municipales que cargarán datos desde la calle.

d) Ambiente de operación: Navegadores web estándar (Chrome, Edge, Firefox) y visualización adaptada para celulares (Android/iOS).

e) Restricciones de diseño e implementación: Todo el manejo de datos debe cumplir con las Ordenanzas Municipales vigentes en Bahía Blanca y la Ley 25.326 de Protección de Datos Personales.

f) Documentación para el usuario: El sistema incluirá una sección de ayuda en línea y pequeñas guías visuales la primera vez que un feriante ingresa a su panel. 

g) Suposiciones y dependencias: El funcionamiento del sistema en la vía pública asume que tanto los inspectores como los feriantes contarán con acceso a internet móvil. Además, la función del mapa depende de que el servicio externo de Google Maps se encuentre activo y disponible.

h) Mensajería espontánea: El usuario le podrá enviar un mensaje rápido al feriante para compartir información y/ o realizar algún encuentro fuera de la feria para una posible compra.

--------------------------
 
## 4. Características del sistema
Agrupamos los requerimientos en 5 módulos principales:

● Módulo de Usuarios y Autenticación: Sistema de registro de usuarios según su rol. Los feriantes arman su perfil, suben fotos, definen su rubro y pueden enlazar sus redes sociales (muy útil para los que usan la feria como punto de entrega o vidriera) y su número de teléfono.

● Módulo de Visibilización Ciudadana: Pantalla principal con el mapa de la ciudad y pines que marcan dónde hay ferias abiertas. Permite buscar por tipo de producto y ver la información de cada puesto.

● Módulo de Asignación de Puestos y Fila de Espera: Los feriantes se postulan para ir a una feria. Si no hay lugar, quedan en una lista de espera virtual. Si alguien se da de baja, el sistema le avisa automáticamente al que sigue en la fila. Los organizadores pueden habilitar o rechazar puestos según si cumplen con las reglas.

● Módulo de Fiscalización y Bromatología: Pantalla exclusiva para inspectores que permite leer códigos QR desde la cámara del celular para chequear libretas sanitarias o permisos en el acto.

●  Módulo de Business Intelligence Municipal: Panel con gráficos para que la Municipalidad pueda ver qué zonas tienen más movimiento, qué rubros crecen más y organizar mejor las políticas de apoyo al sector. 

--------------------------

## 5. Requerimientos de la interfaz externa
   
 a) Interfaces de usuario: Diseño enfocado en el uso desde el celular, con letras legibles y buen contraste para que se pueda ver bien al  aire libre bajo el sol.

 b) Interfaces de hardware: Permisos para acceder a la cámara del teléfono (para escanear QRs), el GPS (para centrar el mapa en la  ubicación del usuario) y permisos de notificaciones (para avisos importantes sobre el clima o espectáculos próximos).

 c) Interfaces de software: Conexión con la API de Google Maps para cargar la cartografía de Bahía Blanca.

 d) Interfaces de las comunicaciones: Optimización de carga de imágenes para consumir pocos datos móviles, ya que se usará mucho en plazas y parques.

--------------------------
 
 ## 6. Otros requerimientos no funcionales
    
| Categoría | Descripción |
|-----------|-------------|
| **Desempeño** | El mapa interactivo y el motor de búsqueda deben ofrecer respuestas ágiles, en un tiempo menor a 2 segundos. |
| **Seguridad** | Protección de la información mediante cifrado de contraseñas y conexiones seguras. |
| **Estabilidad y Consistencia** | Operaciones atómicas en la gestión de la fila de espera para evitar la doble asignación de un mismo puesto ferial. |
| **Usabilidad** | Interfaz simple e intuitiva que no requiera tutoriales extensos, con buen contraste visual para su uso al aire libre bajo la luz solar. |
| **Compatibilidad** | Funcionamiento fluido en los principales navegadores (Chrome, Firefox, Safari y Edge) y soporte adaptado para dispositivos móviles Android e iOS. |
| **Portabilidad y Datos Móviles** | Optimización de la carga de imágenes y recursos para un bajo consumo de datos móviles, considerando el uso frecuente en plazas y parques públicos. |
| **Disponibilidad** | Sistema operativo y accesible de forma permanente, priorizando los horarios habituales de feria (idealmente 24 horas). |
| **Documentación** | Ayuda en línea y guía visual para facilitar el primer ingreso y registro de los feriantes. |

--------------------------

## 7. Apéndices

### Glosario de Actores

| Actor | Descripción |
| :--- | :--- |
| **Ciudadano** | El vecino entra al sistema para ver el mapa, buscar qué ferias están abiertas el fin de semana, mirar los horarios y buscar qué stands hay disponibles. |
| **Feriante** | El emprendedor o productor que usa la plataforma para ofrecer sus productos. Puede armar su catálogo, pedir lugar en las ferias, avisar si no va a ir y ceder su turno en la lista de espera. |
| **Organizador Independiente** | Puede ser una sociedad de fomento, una cooperativa o un grupo barrial que coordina ferias que no son del Municipio. Usan el sistema para filtrar quién entra, ver los rubros y habilitar espacios. |
| **Inspector Municipal** | El empleado de áreas como Bromatología que está en la calle y usa su celular para escanear las credenciales de los puestos y fiscalizar que todo esté en regla. También verificar que todas las habilitaciones solicitadas estén al día. |
| **Analista BI / Administrador** | Personal interno de la Municipalidad que mira los gráficos del sistema para entender cómo se está moviendo el sector de las ferias y tomar decisiones. |

---

## Matriz de trazabilidad

| Código | Requerimiento Funcional | Caso de Uso Relacionado. |
| :--- | :--- | :--- |
| **(RF1)** | Registrar usuario según su rol (ciudadano, feriante, organizador, inspector, administrador). |CU1: Registrar Usuario |
| **(RF2)** | Iniciar sesión de forma segura, con usuario y contraseña predefinida. || CU2: Iniciar Sesión |
| **(RF3)** | Permitir editar perfil público del feriante (fotos, rubro, redes sociales). || CU3: Editar Perfil de Feriante |
| **(RF4)** | Recuperar contraseña. | CU4: Recuperar Contraseña |
| **(RF5)** | Consultar mapa interactivo con ferias activas en tiempo real. | CU5: Visualizar Mapa de Ferias  
| **(RF6)** | Buscar ferias por tipo de producto o rubro. | CU6: Filtrar Búsqueda de Ferias |
| **(RF7)** | Consultar ficha de feria (horarios, stands, feriantes participantes). | CU7: Consultar Ficha de Feria |
| **(RF8)** | Enviar mensaje espontáneo a un feriante. | CU8: Enviar Mensaje a Feriante |
| **(RF9)** | Postularse a una feria. | CU9: Postularse a Feria |
| **(RF10)** | Ingresar a lista de espera cuando no hay cupo. | CU10: Ingresar a Lista de Espera |
| **(RF11)** | Notificar automáticamente al siguiente de la lista ante una baja. | CU11: Reasignar Puesto Automáticamente |
| **(RF12)** | Confirmar o cancelar asistencia a una feria. | CU12: Confirmar Asistencia - Cancelar Asistencia |
| **(RF13)** | Habilitar o rechazar puesto (organizador). |CU13: Habilitar Puesto |
| **(RF14)** | Escanear código QR de libreta sanitaria o permiso. | CU14: Escanear Código QR |
| **(RF15)** | Verificar vigencia de carnet de manipulador de alimentos. | CU15: Verificar Carnet Sanitario |
| **(RF16)** | Registrar resultado de inspección. | CU16: Actas de Inspección |
| **(RF17)** | Generar estadísticas de concurrencia por feria. | CU17: Reportes de Concurrencia |
| **(RF18)** | Visualizar los rubros con mayor crecimiento. | CU18: Análisis de Rubros |
| **(RF19)** | Identificar nivel de regularización de feriantes. | CU19: Control de Regularidad |
| **(RF20)** | Exportar reportes para la Municipalidad. | CU20: Exportación de Datos |
| **(RF21)** | Gestión y programación de ferias | CU21: Gestionar Ferias |
| **(RF22)** | Envío de notificaciones automáticas y alertas. | CU22:Enviar Notificaciones del Sistema |
| **(RF23)** | Gestión de reclamos, consultas o soporte. | CU23: Gestionar Reclamos y Soporte |
--------------------------

## 8. Anexo
Documentacion de casos de uso

Entrevista con los usuarios (documentada)

ENTREVISTA CON FERIANTES: 

HABLAMOS CON ARTESANOS QUE SUELEN ESTAR EN LA PLAZA RIVADAVIA. 
ELLOS NOS CONTARON QUE LOS FERIANTES NO PUEDEN ACCEDER A LA PLAZA SIN AUTORIZACIÓN POR LA COMISIÓN DE FERIANTES. 
ELLOS A PESAR DE SER EXPERTOS EN EL ÁMBITO ARTESANOS, TUVIERON QUE GANARSE SU LUGAR, HABIENDO TANTO ESPACIO DISPONIBLE. 
CONOCÍAN UNA APP QUE SE USA EN GRANDES CIUDADES COMO BUENOS AIRES, DONDE APARECEN LOS PUNTOS DE FERIAS Y QUIEN SE VA A PRESENTAR A OFRECER SUS PRODUCTOS. 


¿CÓMO GESTIONAN EL STOCK? 

-El stock se genera durante las semanas previas a la feria, no es solo trabajo el fin de semana sino que también se trabaja produciendo.

¿CÓMO ACEPTAN LOS PAGOS?

-Aceptamos pago por efectivo o transferencias

¿QUÉ ES LO QUE MÁS SE LES COMPLICA AL ORGANIZARSE PARA LA FERIA? 

-No existen complicaciones, ya que en Bahía la asistencia siempre es buena, entonces solo queda producir y tener el medio disponible para venir y traer la mercancía. Es complicado mantener el stock o poder satisfacer a todos nuestros clientes,así que  también manejamos ventas por instagram, aceptamos pedidos por encargo y  nuevos desafíos. 

¿QUÉ LES PARECE UNA APP COMO LA QUE HABLAMOS?

-La app nos parece una excelente idea, nos serviría mucho ya que podríamos subir fotos de nuestros trabajos, podríamos interactuar con las personas,  poner nuestras redes sociales y número de contacto o whatsapp. Además creemos que son nuevas oportunidades y motivación para que los feriantes de la ciudad vengan y se animen a hacer crecer a la comunidad.Del lado del cliente esta bueno por si les gusto alguno de nuestros trabajos y no pudieron realizar la compra en la feria, nos puedan volver a encontrar en alguna nueva feria. 


¿QUE LOS MOTIVA A SER FERIANTES?-

Lo hacemos porque es lo que nos gusta y nos permite tener la vida que tenemos (viajan recorriendo países en combi).
 




 
 
## Lista de conceptos

TECNOLOGÍA Y PLATAFORMA

**API**: conjunto de reglas y protocolos que permite que dos programas se comuniquen e intercambien datos sin conocer el funcionamiento interno del otro (ej.: la API de Google Maps).
Plataforma web y móvil / visualización adaptada: sistema accesible desde navegador, cuya interfaz se ajusta al tamaño de pantalla de celulares Android e iOS.
Tiempo real: actualización de la información en el momento en que cambia, sin recargas manuales ni cargas diferidas.

**GPS**: sistema de geolocalización del dispositivo, usado para centrar el mapa en la posición del usuario.
Notificaciones: avisos automáticos enviados al dispositivo (clima, espectáculos, bajas en la fila de espera).

**Código QR**: código bidimensional que guarda información (un enlace o identificador) y se lee con la cámara del celular; en el sistema valida libretas sanitarias y permisos.

FUNCIONALIDAD DEL SISTEMA

**Mapa interactivo**: vista cartográfica de la ciudad donde el usuario se desplaza, amplía y consulta información de cada feria.

**Pin**: marcador sobre el mapa que indica la ubicación de una feria abierta.

**Fila de espera (lista de espera virtual)**: cola ordenada de feriantes que se postularon a una feria sin cupo; se actualiza automáticamente y avisa al siguiente cuando se libera un puesto.

**Postulación**: solicitud de un feriante para ocupar un puesto en una feria.

**Mensajería espontánea**: mensaje rápido de un ciudadano a un feriante, sin conversación previa.

**Perfil / rol**: conjunto de datos y permisos asociados a cada tipo de usuario.

**Autenticación**: proceso de verificar la identidad de un usuario (usuario y contraseña) antes de darle acceso.

**Módulo**: agrupación de funciones del sistema relacionadas entre sí.

 SEGURIDAD Y CALIDAD 
 
**Cifrado de Contraseñas**: transformación de las contraseñas en datos ilegibles para que puedan leerse aunque se acceda a la de datos. 

**HTTPS**: protocolo de comunicación que cifra los datos entre el dispositivo y el servidor.

**Operación atómica**: operación que se ejecuta completa o no se ejecuta, y que evita que dos feriantes reciban el mismo puesto.

**Doble asignación**: error en el que un mismo puesto queda asignado a dos feriantes.

**Ley 25.326**: ley nacional de Protección de Datos Personales.

DOMINIO FERIAL Y ADMINISTRATIVO

**Feria fija / itinerante**: la fija tiene ubicación estable; la itinerante cambia de lugar o fecha

**Rubro**: categoría de producto o actividad del puesto (artesanías, alimentos, etc.).

**Fiscalización**: control del cumplimiento de normas en los puestos.

**Bromatología**: área que controla la calidad e higiene de los alimentos.

**Libreta sanitaria / carnet de manipulador de alimentos**: credenciales que habilitan a manipular alimentos.

**Acta de inspección**: registro formal del resultado de una inspección.

**Habilitación / regularización**: cumplimiento de los requisitos para operar legalmente.

**Mipymes**: micro, pequeñas y medianas empresas.

**Ordenanza 11.947**: norma municipal (2003) que regula las ferias en Bahía Blanca.

INGENIERIA DE REQUERIMIENTOS 

**Requerimiento funcional / no funcional**: el primero describe qué hace el sistema; el segundo, qué tan bien lo hace (desempeño, seguridad, usabilidad).

**Caso de uso**: descripción de una interacción entre un actor y el sistema para lograr un objetivo.

**Trazabilidad**: vínculo que permite seguir cada requerimiento hasta su módulo y su caso de uso.

 
**NOTAS**: 

**integrantes**:
*Manuel Murano*
*Sergio Torres Fernandez*
*Facundo Martinez*
*Nahuel Cisneros*
*Lourde De Andres*

