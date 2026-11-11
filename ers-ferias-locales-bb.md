PROYECTO

# Especificación de Requerimientos de Software (ERS)

## Plataforma Integral de Gestión y Visibilización de Ferias Locales en Bahía Blanca

**Analistas de requerimientos**: Murano Manuel, Torres Fernandez Sergio, Martinez Facundo, Lourdes De Andres, Cisneros Nahuel . 
--------------------------
## Indice
   1. Introducción	
   2. Descripción general	
   3. Características del sistema	
   4. Requerimientos de la interfaz externa	
   5. Otros requerimientos no funcionales	
   6. Apéndices	
   7. Anexo
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

## 2. Descripción general
   
a) Perspectiva del producto: Será un sistema web independiente que utilizará APIs* de mapas (Google Maps) para mostrar la información del circuito de ferias de la ciudad en tiempo real.

b) Características del producto: Permite gestionar perfiles de usuarios, ubicar ferias itinerantes y fijas, automatizar la fila de espera para los puestos, cargar actas de inspección y visualizar datos estadísticos.

c) Clases y características del usuario: Abarca desde vecinos sin conocimientos técnicos avanzados hasta inspectores municipales que cargarán datos desde la calle.

d) Ambiente de operación: Navegadores web estándar (Chrome, Edge, Firefox) y visualización adaptada para celulares (Android/iOS).

e) Restricciones de diseño e implementación: Todo el manejo de datos debe cumplir con las Ordenanzas Municipales vigentes en Bahía Blanca y la Ley 25.326 de Protección de Datos Personales.

f) Documentación para el usuario: El sistema incluirá una sección de ayuda en línea y pequeñas guías visuales la primera vez que un feriante ingresa a su panel. 

g) Suposiciones y dependencias: El funcionamiento del sistema en la vía pública asume que tanto los inspectores como los feriantes contarán con acceso a internet móvil. Además, la función del mapa depende de que el servicio externo de Google Maps se encuentre activo y disponible.

h) Mensajería espontánea: El usuario le podrá enviar un mensaje rápido al feriante para compartir información y/ o realizar algún encuentro fuera de la feria para una posible compra.

--------------------------
 
## 3. Características del sistema
Agrupamos los requerimientos en 5 módulos principales:

● Módulo de Usuarios y Autenticación: Sistema de registro de usuarios según su rol. Los feriantes arman su perfil, suben fotos, definen su rubro y pueden enlazar sus redes sociales (muy útil para los que usan la feria como punto de entrega o vidriera) y su número de teléfono.

● Módulo de Visibilización Ciudadana: Pantalla principal con el mapa de la ciudad y pines que marcan dónde hay ferias abiertas. Permite buscar por tipo de producto y ver la información de cada puesto.

● Módulo de Asignación de Puestos y Fila de Espera: Los feriantes se postulan para ir a una feria. Si no hay lugar, quedan en una lista de espera virtual. Si alguien se da de baja, el sistema le avisa automáticamente al que sigue en la fila. Los organizadores pueden habilitar o rechazar puestos según si cumplen con las reglas.

● Módulo de Fiscalización y Bromatología: Pantalla exclusiva para inspectores que permite leer códigos QR desde la cámara del celular para chequear libretas sanitarias o permisos en el acto.

●  Módulo de Business Intelligence Municipal: Panel con gráficos para que la Municipalidad pueda ver qué zonas tienen más movimiento, qué rubros crecen más y organizar mejor las políticas de apoyo al sector. 

--------------------------

## 4. Requerimientos de la interfaz externa
   
 a) Interfaces de usuario: Diseño enfocado en el uso desde el celular, con letras legibles y buen contraste para que se pueda ver bien al  aire libre bajo el sol.

 b) Interfaces de hardware: Permisos para acceder a la cámara del teléfono (para escanear QRs), el GPS (para centrar el mapa en la  ubicación del usuario) y permisos de notificaciones (para avisos importantes sobre el clima o espectáculos próximos).

 c) Interfaces de software: Conexión con la API de Google Maps para cargar la cartografía de Bahía Blanca.

 d) Interfaces de las comunicaciones: Optimización de carga de imágenes para consumir pocos datos móviles, ya que se usará mucho en plazas y parques.

--------------------------
 
 ## 5. Otros requerimientos no funcionales
    
Desempeño: Tanto el mapa interactivo como el motor de búsqueda deben ofrecer respuestas ágiles, operando en un tiempo menor a 2 segundos.

Seguridad: El sistema garantizará la protección de la información mediante el cifrado de contraseñas y conexiones seguras.

Estabilidad y Consistencia: Se implementarán operaciones atómicas en la gestión de la fila de espera para prevenir y evitar la doble asignación de un mismo puesto ferial.

Usabilidad: La interfaz mantendrá un diseño simple e intuitivo que no requiera tutoriales extensos, incorporando además un buen contraste visual para facilitar su uso al aire libre bajo la luz solar.

Compatibilidad: La solución estará diseñada para funcionar de manera fluida en los principales navegadores web estándar (tales como Chrome, Firefox, Safari y Edge) y contar con soporte adaptado para dispositivos móviles Android e iOS.

Portabilidad y Datos Móviles: Se optimizará la carga de imágenes y recursos para asegurar un bajo consumo de datos móviles, considerando el uso frecuente de la plataforma en plazas y parques públicos.

Disponibilidad: El sistema deberá mantenerse operativo y accesible de forma permanente, priorizando su disponibilidad en los horarios habituales de feria (idealmente 24 horas).

Documentación: Se incorporará soporte de ayuda en línea y una guía visual orientada a facilitar el primer ingreso y registro de los feriantes.

--------------------------

## 6. Apéndices

### Glosario de Actores

| Actor | Descripción |
| :--- | :--- |
| **Ciudadano** | El vecino entra al sistema para ver el mapa, buscar qué ferias están abiertas el fin de semana, mirar los horarios y buscar qué stands hay disponibles. |
| **Feriante** | El emprendedor o productor que usa la plataforma para ofrecer sus productos. Puede armar su catálogo, pedir lugar en las ferias, avisar si no va a ir y ceder su turno en la lista de espera. |
| **Organizador Independiente** | Puede ser una sociedad de fomento, una cooperativa o un grupo barrial que coordina ferias que no son del Municipio. Usan el sistema para filtrar quién entra, ver los rubros y habilitar espacios. |
| **Inspector Municipal** | El empleado de áreas como Bromatología que está en la calle y usa su celular para escanear las credenciales de los puestos y fiscalizar que todo esté en regla. También verificar que todas las habilitaciones solicitadas estén al día. |
| **Analista BI / Administrador** | Personal interno de la Municipalidad que mira los gráficos del sistema para entender cómo se está moviendo el sector de las ferias y tomar decisiones. |

---

### Matriz de trazabilidad

| Código | Requerimiento Funcional | Caso de Uso Relacionado |
| :--- | :--- | :--- | :--- |
| **(RF1)** | Registrar usuario según su rol (ciudadano, feriante, organizador, inspector, administrador). | CU1: Registrar Usuario |
| **(RF2)** | Iniciar sesión de forma segura, con usuario y contraseña predefinida. | CU2: Iniciar Sesión |
| **(RF3)** | Permitir editar perfil público del feriante (fotos, rubro, redes sociales). | CU3: Editar Perfil de Feriante |
| **(RF4)** | Recuperar contraseña. | CU4: Recuperar Contraseña |
| **(RF5)** | Consultar mapa interactivo con ferias activas en tiempo real. | CU5: Visualizar Mapa de Ferias  
| **(RF6)** | Buscar ferias por tipo de producto o rubro. | CU6: Filtrar Búsqueda de Ferias |
| **(RF7)** | Consultar ficha de feria (horarios, stands, feriantes participantes). | CU7: Consultar Ficha de Feria |
| **(RF-8)** | Enviar mensaje espontáneo a un feriante. | CU8: Enviar Mensaje a Feriante |
| **(RF9)** | Postularse a una feria. | CU9: Postularse a Feria |
| **(RF10)** | Ingresar a lista de espera cuando no hay cupo. | CU10: Ingresar a Lista de Espera |
| **(RF11)** | Notificar automáticamente al siguiente de la lista ante una baja. | CU11: Reasignar Puesto Automáticamente |
| **(RF12)** | Confirmar o cancelar asistencia a una feria. | CU12: Confirmar Asistencia - Cancelar Asistencia |
| **(RF13)** | Habilitar o rechazar puesto (organizador). |CU13: Habilitar Puesto |
| **(RF14)** | Escanear código QR de libreta sanitaria o permiso. | CU14: Escanear Código QR |
| **(RF15)** | Verificar vigencia de carnet de manipulador de alimentos. | CU15: Verificar Carnet Sanitario |
| **(RF16)** | Registrar resultado de inspección. | CU16: Actas de Inspección |
| **(RF17)** | Generar estadísticas de concurrencia por feria. | Módulo de Business Intelligence Municipal | CU17: Reportes de Concurrencia |
| **(RF18)** | Visualizar los rubros con mayor crecimiento | CU18: Análisis de Rubros |
| **(RF19)** | Identificar nivel de regularización de feriantes. | Módulo de Business Intelligence Municipal | CU19: Control de Regularidad |
| **(RF20)** | Exportar reportes para la Municipalidad | CU20: Exportación de Datos |
| **(RF21)** | Gestión y programación de ferias | CU21: Gestionar Ferias |
| **()** | Envío de notificaciones automáticas y alertas | CU22:Enviar Notificaciones del Sistema |
| **()** | Gestión de reclamos, consultas o soporte | CU23: Gestionar Reclamos y Soporte |
--------------------------

## 7. Otros requerimientos (Técnicas de Exploración)

 
 
## 8. Apéndices
*Glosario de Actores
*Actor
*Descripción
*Ciudadano

EL<ins>vecino</ins> 
Es el que va a entrar en el  sistema para ver el mapa, buscar qué ferias están abiertas el fin de semana, mirar los horarios y buscar qué stands hay disponibles.

EL<ins>Feriante</ins>
El emprendedor o productor que usa la plataforma para ofrecer sus cosas. Puede armar su catálogo, pedir lugar en las ferias, avisar si no va a ir y seguir su turno en la lista de espera.

EL<ins>Organizador Independiente</ins>
Puede ser una sociedad de fomento, una cooperativa o un grupo barrial que coordina ferias que no son del Municipio. Usan el sistema para filtrar quién entra, ver los rubros y habilitar espacios.

EL<ins>Inspector Municipal</ins>
El empleado de áreas como Bromatología que está en la calle y usa su celular para escanear las credenciales de los puestos y fiscalizar que todo esté en regla.

EL <ins>Analista BI / Administrador</ins>
Personal interno de la Municipalidad que mira los gráficos del sistema para entender cómo se está moviendo el sector de las ferias y tomar decisiones.

 




**NOTAS**: 

**integrantes**:
*Manuel Murano*
*Sergio Torres Fernandez*
*Facundo Martinez*
*Nahuel Cisneros*
*Lourde De Andres*

