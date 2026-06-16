*Taller Final — Arquitectura Tecnológica*

**Taller Final**

**Arquitectura de Sistemas de Información**

**y Arquitectura Tecnológica**

Plataforma Turística Integral de Sucre (PTIS)

|**Asignatura**|Arquitectura Empresarial|
| :- | :- |
|**Docente**|Prof. Jhon Jaime Mendez|
|**Integrantes**|<p>Carlos Andrés Carriazo Sierra</p><p>Santiago Visbal Romero</p><p>Leonard Andrés Ortega González</p><p>David Escudero Vidual</p>|
|**Institución**|Corporación Universitaria del Caribe CECAR — Ingeniería de Sistemas|
|**Ciudad**|Sincelejo, Sucre — Colombia|


# **Introducción**
El presente documento desarrolla la Arquitectura Tecnológica de la Plataforma Turística Integral de Sucre (PTIS), continuando el ejercicio de Arquitectura Empresarial iniciado en los Talleres 1, 2 y 3. Su objetivo es definir la infraestructura tecnológica necesaria para soportar las aplicaciones y los procesos de negocio descritos previamente: el modelo operativo (Captación, Interacción, Transacción y Entrega de Valor), los procesos de negocio (onboarding de prestadores, búsqueda y recomendaciones, procesamiento de reservas y pagos, y gestión post-servicio) y las capacidades de negocio críticas y diferenciadoras identificadas, en particular la Personalización Inteligente de Experiencias, el Procesamiento Seguro de Transacciones, la Operación Tecnológica Escalable y la Inteligencia de Datos Turísticos.

El documento se organiza en tres entregables: (1) el Catálogo Tecnológico, que identifica cada componente, su función y la tecnología seleccionada; (2) el Diagrama Tecnológico, que representa la infraestructura general de la solución; y (3) el Diagrama de Despliegue, que detalla cómo se distribuyen las aplicaciones dentro de dicha infraestructura. Finalmente, se presenta la justificación de las decisiones tecnológicas adoptadas y su coherencia con la Arquitectura de Negocio y de Datos definida en los talleres anteriores.
# **1. Catálogo Tecnológico**
A continuación se identifican los componentes tecnológicos necesarios para soportar la solución propuesta, organizados según la capa arquitectónica a la que pertenecen: presentación, aplicación/cómputo, datos, seguridad/red e integraciones externas. Para cada componente se indica su nombre, su función dentro de la plataforma y la tecnología seleccionada.

|**Nombre**|**Función**|**Tecnología seleccionada**|
| :-: | :-: | :-: |
|**A. Capa de Presentación**|||
|**Frontend Web**|Interfaz web responsive donde turistas y prestadores acceden al catálogo de servicios, búsqueda, reservas y panel de gestión.|React.js|
|**Frontend Móvil**|Aplicación nativa para iOS y Android que replica las funcionalidades de la plataforma web, optimizada para uso en movimiento durante el viaje.|React Native|
|**B. Capa de Aplicación / Cómputo**|||
|**Backend / API**|Expone los servicios REST/GraphQL que implementan la lógica de negocio: gestión de usuarios, prestadores, búsqueda, reservas, pagos y reseñas.|Node.js (NestJS)|
|**Motor de Recomendaciones IA**|Analiza el perfil, historial y preferencias del usuario para generar recomendaciones personalizadas de experiencias turísticas.|Python (Scikit-learn / TensorFlow)|
|**Chatbot de Asistencia (NLP)**|Atiende consultas frecuentes del viajero 24/7 (destinos, reservas, itinerarios) y escala a soporte humano los casos complejos.|Modelo de lenguaje con procesamiento de lenguaje natural (NLP)|
|**Servicios Cloud (Cómputo)**|Ejecuta el backend, el motor de IA y el chatbot como contenedores escalables, permitiendo absorber picos de demanda en temporada alta.|Amazon ECS sobre AWS Fargate (contenedores Docker)|
|**C. Capa de Datos**|||
|**Base de Datos Relacional**|Almacena de forma transaccional y consistente los datos de usuarios, prestadores, reservas, pagos y reseñas.|PostgreSQL (Amazon RDS, Multi-AZ)|
|**Caché en Memoria**|Acelera los resultados de búsqueda frecuentes y gestiona el bloqueo temporal de cupos durante el proceso de reserva (15 minutos).|Redis (Amazon ElastiCache)|
|**Almacenamiento de Objetos**|Guarda imágenes de servicios turísticos, documentos de verificación (RNT) y comprobantes de reserva. Sirve como repositorio base para análisis de datos.|Amazon S3|
|**Plataforma de Analítica de Datos**|Consulta y agrega los datos almacenados para generar reportes de inteligencia turística dirigidos a la Gobernación, PROCOLOMBIA y prestadores.|Amazon Athena + Amazon QuickSight|
|**D. Capa de Seguridad y Red**|||
|**Firewall de Aplicaciones Web**|Protege la plataforma contra ataques comunes (inyección SQL, XSS) y mitiga ataques de denegación de servicio (DDoS).|AWS WAF|
|**Balanceador de Carga**|Distribuye el tráfico entrante entre las instancias de los contenedores de aplicación para garantizar disponibilidad.|AWS Application Load Balancer (ALB)|
|**CDN (Red de Distribución de Contenido)**|Distribuye contenido estático (imágenes, archivos del frontend) desde ubicaciones cercanas al usuario, reduciendo la latencia.|Amazon CloudFront|
|**NAT Gateway**|Permite que los servicios alojados en la subred privada se conecten a APIs externas sin exponer su dirección IP interna.|AWS NAT Gateway|
|**E. Integraciones Externas**|||
|**Pasarela de Pagos**|Procesa pagos en línea de forma segura mediante PSE, tarjetas de crédito/débito y billeteras digitales (Nequi, Daviplata).|PayU / Wompi|
|**Servicio de Mapas**|Provee el mapa interactivo georreferenciado con la ubicación de atractivos turísticos, hoteles y restaurantes, y rutas sugeridas entre ellos.|Google Maps Platform|
|**Servicio de Notificaciones**|Envía confirmaciones automáticas de reserva, recordatorios y solicitudes de reseña por correo electrónico y mensaje de texto.|Amazon SES (correo) + Twilio (SMS)|


# **2. Diagrama Tecnológico**
El siguiente diagrama representa la infraestructura tecnológica general de PTIS, organizada en capas. Incluye los usuarios (turistas y prestadores), el tránsito por Internet, los componentes de seguridad (CDN y firewall web), el balanceador de carga, la capa de aplicación (contenedores que ejecutan el frontend, el backend, el motor de IA y el chatbot), la capa de datos (base de datos relacional, caché y almacenamiento de objetos) y las integraciones externas (pasarela de pagos, mapas y notificaciones).

<img width="882" height="806" alt="Figura 1 - AE" src="https://github.com/user-attachments/assets/778d1664-f336-4018-a240-be28d40d626b" />


*Figura 1. Diagrama Tecnológico de PTIS*
## **2.1. Descripción del Flujo**
- **Usuarios:** turistas y prestadores acceden a la plataforma desde la web o desde la aplicación móvil.
- **Internet y Seguridad:** las peticiones llegan a través de Internet a Amazon CloudFront (CDN) y AWS WAF, que filtran tráfico malicioso y entregan contenido estático de forma eficiente.
- **Balanceo de carga:** el AWS Application Load Balancer distribuye las peticiones entre las instancias disponibles de cada servicio.
- **Capa de Aplicación:** contenedores ejecutados sobre Amazon ECS/Fargate alojan el frontend, el backend (API), el motor de recomendaciones de IA y el chatbot de asistencia.
- **Capa de Datos:** PostgreSQL (RDS) almacena la información transaccional, Redis (ElastiCache) actúa como caché y S3 almacena objetos e imágenes.
- **Integraciones externas:** el backend se comunica con la pasarela de pagos, el servicio de mapas y los servicios de notificación por correo y SMS.


# **3. Diagrama de Despliegue**
El diagrama de despliegue detalla cómo se distribuyen las aplicaciones dentro de la infraestructura tecnológica de AWS, mostrando los servidores/nodos, los contenedores que alojan cada aplicación, las bases de datos, los servicios externos y las relaciones de comunicación (protocolos) entre ellos.

<img width="930" height="762" alt="Figura 2 - AE" src="https://github.com/user-attachments/assets/9cc9400b-b36d-4dc9-86fe-5a9ff1c74da3" />


*Figura 2. Diagrama de Despliegue de PTIS*
## **3.1. Componentes y Relaciones de Comunicación**
- **Dispositivos cliente** (navegador web y app móvil) se conectan por HTTPS a Amazon CloudFront, que actúa como punto de entrada de la red.
- **Subred pública de la VPC:** AWS WAF filtra el tráfico antes de llegar al Application Load Balancer (ALB), que reenvía las peticiones (HTTP interno) hacia la subred privada. El NAT Gateway permite la salida controlada hacia servicios externos.
- **Subred privada (Amazon ECS / Fargate):** aloja los contenedores de Frontend, Backend API, Motor de Recomendaciones IA y Chatbot, cada uno desplegado con al menos dos instancias para alta disponibilidad y autoescalado. El Backend API se comunica internamente con el Motor de IA y el Chatbot mediante llamadas API internas.
- **Subred de datos (privada):** el Backend API se conecta a Amazon RDS (PostgreSQL) por el puerto 5432 para operaciones transaccionales, a Amazon ElastiCache (Redis) por el puerto 6379 para caché y bloqueo de cupos, y a Amazon S3 vía HTTPS (a través de un VPC Endpoint) para almacenamiento de objetos.
- **Servicios externos:** desde la subred privada, a través del NAT Gateway, la plataforma consume las APIs de PayU/Wompi (pagos), Google Maps Platform (mapas), Amazon SES (correo) y Twilio (SMS) mediante peticiones HTTPS/REST.


# **4. Explicación de las Decisiones Tecnológicas Adoptadas**
Cada decisión tecnológica adoptada responde a un requerimiento concreto derivado de la Arquitectura de Negocio (Taller 2 y Taller 3) y de la Arquitectura de Datos descrita en el análisis AS-IS/TO-BE del Taller 3. A continuación se justifica cada grupo de decisiones.
## **4.1. Infraestructura Cloud y Contenedores (AWS / ECS Fargate)**
Se mantiene AWS como proveedor de infraestructura cloud, ya identificado en el Taller 2 como uno de los actores tecnológicos del ecosistema. El uso de contenedores Docker orquestados con Amazon ECS sobre AWS Fargate permite escalar horizontalmente cada servicio (frontend, backend, motor de IA, chatbot) de forma independiente. Esta decisión responde directamente a la capacidad crítica de 'Operación Tecnológica Escalable' definida en el Taller 2 y al riesgo de 'Incapacidad para Escalar de Manera Ordenada' señalado en el Taller 3, ya que el turismo en Sucre tiene una marcada estacionalidad (Semana Santa, diciembre, festivales) que exige absorber picos de tráfico sin degradar el servicio ni intervenir manualmente la infraestructura.
## **4.2. Frontend Web y Móvil (React.js / React Native)**
Se seleccionó React.js para el frontend web y React Native para las aplicaciones móviles porque ambos comparten el mismo lenguaje (JavaScript/TypeScript) y gran parte de la lógica de componentes, lo cual reduce la curva de aprendizaje y el esfuerzo de mantenimiento para un equipo pequeño como el descrito en el Taller 1 (un único Desarrollador Full Stack). Esta decisión soporta la capacidad de 'Experiencia de Usuario Digital', ya que ambas plataformas (web y móvil) pueden mantener una interfaz consistente, rápida y accesible, requisito explícito del MVP definido en el Taller 1 (catálogo de servicios, motor de búsqueda y filtros, sistema de reservas y recomendador con IA).
## **4.3. Backend y Lógica de Negocio (Node.js / NestJS)**
Node.js con el framework NestJS se eligió por mantener coherencia de lenguaje (JavaScript/TypeScript) con el frontend, facilitando que el mismo perfil de Desarrollador Full Stack (rol definido en el Taller 1) pueda trabajar en ambas capas. NestJS aporta una estructura modular que facilita implementar de forma ordenada los procesos core definidos en el Taller 2 y el Taller 3: onboarding de prestadores, búsqueda y recomendaciones, procesamiento de reservas y pagos, y gestión de experiencia post-servicio (reseñas). La exposición de servicios vía REST/GraphQL permite que tanto el frontend web como la app móvil consuman la misma API, evitando duplicidad de lógica.
## **4.4. Persistencia y Gestión de Datos (PostgreSQL, Redis, S3, Athena/QuickSight)**
La selección de PostgreSQL como base de datos relacional responde a la naturaleza transaccional de los procesos core: reservas, pagos y liquidaciones requieren consistencia e integridad referencial (propiedades ACID), especialmente en el flujo descrito en el Taller 2 de bloqueo temporal del cupo durante el pago. Se configura en modalidad Multi-AZ para garantizar disponibilidad ante fallas, alineándose con la capacidad 'Operación Tecnológica Escalable'.

Redis (Amazon ElastiCache) se incorpora como caché en memoria para acelerar las búsquedas frecuentes del motor de recomendaciones y para implementar de forma eficiente el bloqueo temporal de cupos de 15 minutos descrito en el proceso de 'Procesamiento de Reservas y Pagos' (Taller 2), evitando sobreventa sin sobrecargar la base de datos relacional.

Amazon S3 almacena objetos no estructurados (imágenes de servicios turísticos, documentos de verificación del Registro Nacional de Turismo y comprobantes de reserva), cubriendo la necesidad de un 'catálogo actualizado y verificado de servicios turísticos' descrita en el análisis TO-BE del Taller 3.

Finalmente, Amazon Athena y Amazon QuickSight permiten consultar y visualizar los datos acumulados (búsquedas, reservas, reseñas, flujos turísticos) sin necesidad de una infraestructura analítica adicional. Esta decisión es la respuesta tecnológica directa a la capacidad diferenciadora 'Inteligencia de Datos Turísticos' y al servicio de negocio 'Inteligencia de Mercado Turístico' (dirigido a la Gobernación y PROCOLOMBIA) definidos en el Taller 3, y mitiga el riesgo de 'Pérdida de Valor de los Datos como Activo Estratégico' señalado en el análisis crítico del mismo taller: sin esta capa, los datos capturados por la plataforma no se traducirían en los reportes que sustentan el cuarto modelo de ingresos del Business Model Canvas (licenciamiento de datos e inteligencia de mercado).
## **4.5. Seguridad y Red (AWS WAF, ALB, CloudFront, NAT Gateway)**
AWS WAF y el Application Load Balancer protegen y distribuyen el tráfico hacia la capa de aplicación, mientras que Amazon CloudFront acelera la entrega de contenido estático a turistas que pueden acceder desde distintos lugares del país o del extranjero, en línea con el segmento de 'turistas internacionales interesados en el Caribe colombiano' definido en el Taller 3. Estos componentes son la base tecnológica de la capacidad 'Procesamiento Seguro de Transacciones': sin un perímetro de seguridad adecuado, el procesamiento de pagos descrito en el modelo operativo (Taller 2) no podría garantizar la confianza que la estrategia de diferenciación requiere. El NAT Gateway permite que los contenedores en la subred privada consuman APIs externas (pagos, mapas, notificaciones) sin exponer la infraestructura interna a Internet.
## **4.6. Inteligencia Artificial (Motor de Recomendaciones y Chatbot)**
El motor de recomendaciones (Python con Scikit-learn/TensorFlow) y el chatbot de asistencia basado en NLP se desplegaron como contenedores independientes dentro de la misma capa de aplicación, lo que permite escalarlos, actualizarlos y reentrenarlos sin afectar la disponibilidad del backend transaccional. Esta separación de responsabilidades es coherente con el proceso 'Gestión de Búsqueda y Recomendaciones Personalizadas' y con la justificación del uso de IA presentada en el Taller 1: el motor de recomendaciones aumenta la conversión al reducir el esfuerzo de planificación del viajero, y el chatbot reduce la carga de atención al cliente fuera del horario humano, soportando el proceso de 'Atención al Viajero y al Prestador' (Taller 3).
## **4.7. Integraciones Externas (Pasarela de Pagos, Mapas, Notificaciones)**
PayU y Wompi se mantienen como pasarelas de pago porque ya fueron identificadas como actores tecnológicos del ecosistema en el Taller 2 y permiten los métodos de pago locales requeridos (PSE, tarjetas, Nequi, Daviplata), fundamentales para el mercado colombiano. Google Maps Platform habilita el 'mapa interactivo georreferenciado' descrito en la etapa de Interacción del modelo operativo (Taller 2). Amazon SES y Twilio implementan las notificaciones automáticas por correo y SMS que confirman cada reserva, requerimiento explícito del proceso 'Procesamiento de Reservas y Pagos' y del MVP definido en el Taller 1.
## **4.8. Coherencia General con la Arquitectura de Negocio y de Datos**
La arquitectura tecnológica presentada no introduce componentes ajenos a lo definido en los talleres anteriores: AWS, las pasarelas de pago PayU/Wompi y la infraestructura cloud ya habían sido identificados como actores y recursos clave en el Taller 2. Cada componente del catálogo tecnológico puede trazarse a un proceso de negocio, una capacidad o una necesidad de datos definida previamente: la capa de aplicación ejecuta los procesos core (onboarding, búsqueda/recomendación, reservas, post-servicio); la capa de datos materializa la 'Gestión de Datos' descrita en el AS-IS/TO-BE del Taller 3 (datos de demanda, de oferta y de calidad del servicio); y la capa de seguridad y red sostiene la confianza que exige el modelo de marketplace. De esta forma, la infraestructura tecnológica queda alineada con la estrategia de diferenciación enfocada en Sucre y con el objetivo de capturar el 30% de las reservas online en 18 meses.
Página 1
