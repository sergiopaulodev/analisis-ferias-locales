# Especificación de Requerimientos de Software (ERS)
## Plataforma Integral de Gestión y Visibilización de Ferias Locales en Bahía Blanca
**Institución**: I.S.F.T N° 191 - Bahía Blanca
**Materia**: Prácticas Profesionalizantes 1
**Profesora**: Gisela B. Gorjon
**Analistas de requerimientos**: Murano Manuel, Torres Sergio, Martinez Facundo, Lourdes De Andres, Cisneros Nahuel . 
 
1. Introducción
- Propósito: Documentar los requerimientos funcionales y no funcionales para desarrollar una plataforma web y móvil que permita gestionar y dar visibilidad a las ferias locales de Bahía Blanca.
- Convenciones del documento: El documento se estructura según el estándar ERS visto en la cátedra para el ciclo de vida del software, basándonos en las reglas del sector ferial local.
- Audiencia del proyecto y sugerencias de lectura: El texto está dirigido a los futuros desarrolladores del sistema, analistas, diseñadores de bases de datos.
- Alcance del Proyecto: La plataforma busca organizar la información dispersa sobre las ferias de la ciudad. Conectará a los ciudadanos (a través de un mapa interactivo), a los feriantes (mediante registro y listas de espera) y a los organizadores/Municipio (para tareas de fiscalización y armado de estadísticas).
- Referencias:
+     Informe "Primeras aproximaciones al fenómeno de las ferias en Bahía Blanca" (Cantamutto et al., 2023).
+     Ordenanza 11.947 de la Municipalidad de Bahía Blanca.
+     Material de la Unidad 2 de Prácticas Profesionalizantes 1.
 
 
2. Descripción general
- Perspectiva del producto: Será un sistema web independiente que utilizará APIs* de mapas (Google Maps) para mostrar la información del circuito de ferias de la ciudad en tiempo real.(Una API es un conjunto de reglas y protocolos que permitea que dos programas de software se comuniquen entre si)
- Características del producto: Permite gestionar perfiles de usuarios, ubicar ferias itinerantes y fijas, automatizar la fila de espera para los puestos, cargar actas de inspección y visualizar datos estadísticos.

- Clases y características del usuario: Abarca desde vecinos sin conocimientos técnicos avanzados hasta inspectores municipales que cargarán datos desde la calle.
- Ambiente de operación: Navegadores web estándar (Chrome, Edge, Firefox) y visualización adaptada para celulares (Android/iOS).
- Restricciones de diseño e implementación: Todo el manejo de datos debe cumplir con las Ordenanzas Municipales vigentes en Bahía Blanca y la Ley 25.326 de Protección de Datos Personales.
- Documentación para el usuario: El sistema incluirá una sección de ayuda en línea y pequeñas guías visuales la primera vez que un feriante ingresa a su panel. 
- Suposiciones y dependencias: El funcionamiento del sistema en la vía pública asume que tanto los inspectores como los feriantes contarán con acceso a internet móvil. Además, la función del mapa depende de que el servicio externo de Google Maps se encuentre activo y disponible.
- Mensajería espontánea: El usuario le podrá enviar un mensaje rápido al feriante para compartir información y/ o realizar algun encuentro fuera de la feria para una posible compra.
 
3. Características del sistema
Agrupamos los requerimientos en 5 módulos principales:
+     Módulo de Usuarios y Autenticación: Sistema de registro de usuarios según su rol. Los feriantes arman su perfil, suben fotos, definen su rubro y pueden enlazar sus redes sociales (muy útil para los que usan la feria como punto de entrega o vidriera).
+     Módulo de Visibilización Ciudadana: Pantalla principal con el mapa de la ciudad y pines que marcan dónde hay ferias abiertas. Permite buscar por tipo de producto y ver la información de cada puesto.
+     Módulo de Asignación de Puestos y Fila de Espera: Los feriantes se postulan para ir a una feria. Si no hay lugar, quedan en una lista de espera virtual. Si alguien se da de baja, el sistema le avisa automáticamente al que sigue en la fila. Los organizadores pueden habilitar o rechazar puestos según si cumplen con las reglas.
+     Módulo de Fiscalización y Bromatología: Pantalla exclusiva para inspectores que permite leer códigos QR desde la cámara del celular para chequear libretas sanitarias o permisos en el acto.
+     Módulo de Business Intelligence Municipal: Panel con gráficos para que la Municipalidad pueda ver qué zonas tienen más movimiento, qué rubros crecen más y organizar mejor las políticas de apoyo al sector. 
               IMPORTANTE: En nuestro sistema queremos que se apoye al feriante más comprometido con las participaciones de las ferias, también como a los que cumplan con las normas y vean a las ferias como un negocio sano para las mipymes o nuevos emprendedores. 
4. Requerimientos de la interfaz externa
- Interfaces de usuario: Diseño enfocado en el uso desde el celular, con letras legibles y buen contraste para que se pueda ver bien al aire libre bajo el sol.
- Interfaces de hardware: Permisos para usar la cámara del teléfono (para escanear QRs) y el GPS (para centrar el mapa en la ubicación del usuario).
- Interfaces de software: Conexión con la API de Google Maps para cargar la cartografía de Bahía Blanca.
- Interfaces de las comunicaciones: Optimización de carga de imágenes para consumir pocos datos móviles, ya que se usará mucho en plazas y parques.
 
5. Otros requerimientos no funcionales
- Requerimientos de desempeño: El mapa y el buscador de feriantes deben responder en menos de 2 segundos.
- Requerimientos de seguridad: Las contraseñas de los usuarios deben estar encriptadas en la base de datos y la conexión debe ser segura.
- Requerimientos de estabilidad y consistencia: El sistema de asignación de puestos debe asegurar que nunca se le asigne el mismo lugar a dos feriantes al mismo tiempo por errores de conexión (operaciones atómicas).
- Atributos de calidad: Interfaz simple e intuitiva para que cualquier persona pueda anotarse a una feria sin necesidad de un tutorial extenso.
 
6. Otros requerimientos (Técnicas de Exploración)

 
 
7. Apéndices
*Glosario de Actores*
*Actor*
*Descripción*
*Ciudadano*
El vecino entra al sistema para ver el mapa, buscar qué ferias están abiertas el fin de semana, mirar los horarios y buscar qué stands hay disponibles.
Feriante
El emprendedor o productor que usa la plataforma para ofrecer sus cosas. Puede armar su catálogo, pedir lugar en las ferias, avisar si no va a ir y seguir su turno en la lista de espera.
Organizador Independiente
Puede ser una sociedad de fomento, una cooperativa o un grupo barrial que coordina ferias que no son del Municipio. Usan el sistema para filtrar quién entra, ver los rubros y habilitar espacios.
Inspector Municipal
El empleado de áreas como Bromatología que está en la calle y usa su celular para escanear las credenciales de los puestos y fiscalizar que todo esté en regla.
Analista BI / Administrador
Personal interno de la Municipalidad que mira los gráficos del sistema para entender cómo se está moviendo el sector de las ferias y tomar decisiones.

 




**NOTAS**: 

**integrantes**:
*Manuel Murano*
*Sergio Torres*
*Facundo Martinez*
*Nahuel Cisneros*
