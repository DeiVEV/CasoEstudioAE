# Taller 1 — Plataforma Digital de Turismo Inteligente para el Departamento de Sucre

---

|                            |                                                                         |
| -------------------------- | ----------------------------------------------------------------------- |
| **Asignatura**       | Arquitectura Empresarial                                                |
| **Docente**          | Prof. Jhon Jaime Mendez                                                 |
| **Integrantes**      | Carlos Andrés Carriazo Sierra                                          |
|                            | Santiago Visbal Romero                                                  |
|                            | Leonard Andrés Ortega González                                        |
|                            | David Escudero Vidual                                                   |
| **Institución**     | Corporación Universitaria del Caribe CECAR — Ingeniería de Sistemas |
| **Fecha de entrega** | 23 de marzo de 2026                                                     |
| **Ciudad**           | Sincelejo, Sucre — Colombia                                            |

---

## Tabla de Contenidos

1. [Contexto](#1-contexto)
2. [Análisis del Entorno](#2-análisis-del-entorno)
   - 2.1 [Elementos del Entorno Identificados](#21-elementos-del-entorno-identificados)
   - 2.2 [Análisis PESTEL](#22-análisis-pestel)
3. [Drivers del Turismo Digital](#3-drivers-del-turismo-digital)
4. [Oportunidad de Negocio](#4-oportunidad-de-negocio)
5. [Idea de Negocio](#5-idea-de-negocio)
   - 5.1 [Definición General](#51-definición-general)
   - 5.2 [Business Model Canvas](#52-business-model-canvas)
6. [Creación de la Empresa](#6-creación-de-la-empresa)
   - 6.1 [Identificación Corporativa](#61-identificación-corporativa)
   - 6.2 [Misión, Visión y Valores](#62-misión-visión-y-valores)
7. [Estrategia](#7-estrategia)
   - 7.1 [Estrategia General y Ventaja Competitiva](#71-estrategia-general-y-ventaja-competitiva)
   - 7.2 [Análisis Competitivo](#72-análisis-competitivo)
8. [MVP — Producto Mínimo Viable](#8-mvp--producto-mínimo-viable)
   - 8.1 [Funcionalidades Principales](#81-funcionalidades-principales)
   - 8.2 [Stack Tecnológico Propuesto](#82-stack-tecnológico-propuesto)
9. [Justificación del Uso de Inteligencia Artificial](#9-justificación-del-uso-de-inteligencia-artificial)
10. [Organización](#10-organización)
11. [Documentos de Referencia](#11-documentos-de-referencia)

---

## 1. Contexto

El departamento de Sucre, ubicado en la región Caribe de Colombia, posee una gran diversidad de atractivos turísticos: playas sobre el Mar Caribe, ecosistemas de ciénagas y manglares, una rica identidad cultural afrocolombiana e indígena, gastronomía tradicional y festividades de proyección nacional como el Festival del Frito y el Festival Internacional del Acordeón.

A pesar de este enorme potencial, gran parte de la oferta turística del departamento se encuentra **fragmentada y escasamente digitalizada**. Guías turísticos, empresas de transporte, hoteles y operadores de actividades locales funcionan de manera aislada, sin integración entre sí, lo que dificulta que los turistas encuentren información confiable, planifiquen experiencias completas o realicen reservas de forma sencilla desde un único punto de acceso.

En el contexto global, el turismo ha sido profundamente transformado por la irrupción de plataformas digitales (Booking, Airbnb, TripAdvisor), sistemas de recomendación basados en inteligencia artificial y el análisis de datos para personalizar experiencias. Colombia ha avanzado en la digitalización del sector turístico en ciudades principales, pero departamentos como Sucre aún carecen de una solución tecnológica propia que articule su ecosistema turístico.

> **Oportunidad central:** Ante este contexto surge la posibilidad de desarrollar una plataforma digital de turismo inteligente que integre los diferentes servicios turísticos del departamento, facilite la planificación de experiencias y posicione a Sucre como un destino turístico competitivo a nivel nacional e internacional.

---

## 2. Análisis del Entorno

### 2.1 Elementos del Entorno Identificados

Se identifican los siguientes elementos del entorno que influyen directamente en el desarrollo del turismo en el departamento de Sucre:

| Tipo de Entorno           | Factor                              | Descripción                                                                                                                                                                                                                                                            |
| ------------------------- | ----------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Tecnológico**    | Baja digitalización local          | La mayoría de los operadores turísticos en Sucre no cuentan con presencia digital ni canales de venta online. Esto crea una brecha respecto al comportamiento del turista moderno, que investiga y reserva a través de internet.                                     |
| **Económico**      | Potencial de crecimiento turístico | Según el Plan de Desarrollo Departamental 2020-2023, el turismo es uno de los sectores productivos con mayor potencial. Sin embargo, la inversión pública en infraestructura digital ha sido limitada y los operadores locales tienen capacidad financiera reducida. |
| **Sociocultural**   | Identidad cultural diferenciada     | Sucre posee una identidad cultural única basada en tradiciones afrocolombianas, indígenas zenú, festividades tradicionales y gastronomía típica. Esta diversidad es un activo diferencial frente a destinos masificados, aunque su promoción digital es dispersa. |
| **Político-Legal** | Política Nacional de Turismo       | Colombia cuenta con la Política de Turismo Sostenible y el Plan Sectorial 2022-2026, que incentivan la digitalización del sector. La gobernación de Sucre tiene alianzas con el MinCIT para el desarrollo de destinos competitivos.                                  |
| **Ambiental**       | Riqueza natural y ecoturismo        | La ciénaga de La Caimanera, el Golfo de Morrosquillo, los manglares y la biodiversidad del departamento son atractivos de ecoturismo con creciente demanda global.                                                                                                     |
| **Competitivo**     | Competencia de destinos cercanos    | Departamentos vecinos como Bolívar (Cartagena) y Córdoba concentran la mayor parte del flujo turístico regional, compitiendo directamente con Sucre por la atención de turistas nacionales e internacionales.                                                       |

### 2.2 Análisis PESTEL

El análisis PESTEL permite comprender las fuerzas del macroentorno que condicionan la viabilidad del proyecto:

| Dimensión             | Oportunidades                                                                     | Amenazas / Desafíos                                                                        |
| ---------------------- | --------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| **Político**    | Programas gubernamentales de digitalización PYME y apoyo al turismo regional.    | Cambios en políticas de inversión pública y presupuestos departamentales.                |
| **Económico**   | Crecimiento del sector turístico colombiano post-pandemia (+18% en 2024).        | Inflación que encarece costos operativos y reduce la capacidad de gasto del turista local. |
| **Social**       | Auge del turismo experiencial y demanda de experiencias auténticas.              | Desconfianza de operadores locales hacia la tecnología y resistencia al cambio.            |
| **Tecnológico** | Disponibilidad de APIs de mapas, pagos, IA y cloud computing a bajo costo.        | Baja conectividad a internet en zonas rurales del departamento.                             |
| **Ecológico**   | Tendencia global al ecoturismo y turismo sostenible.                              | Vulnerabilidad de ecosistemas ante el turismo masivo sin regulación adecuada.              |
| **Legal**        | Marco legal favorable para startups tecnológicas en Colombia (Ley 2069 de 2020). | Regulaciones de protección de datos (Ley 1581) que exigen cumplimiento estricto.           |

---

## 3. Drivers del Turismo Digital

Los _drivers_ son las fuerzas impulsoras que generan un cambio en el entorno y crean condiciones favorables para el desarrollo de la plataforma:

| Driver                                                    | Explicación                                                                                                                                                 | Impacto esperado                                                                                                     |
| --------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------- |
| **Digitalización de servicios turísticos**        | La fragmentación actual de guías, transporte y hospedaje genera fricción. Hay una necesidad urgente de integrar estos servicios en un solo canal digital. | Reducción de fricción en la planificación del viaje y aumento en la tasa de conversión de visitantes.            |
| **Crecimiento del turismo experiencial**            | Los viajeros modernos buscan experiencias auténticas y personalizadas. El turismo cultural y de naturaleza crece un 12% anual en Colombia.                  | Mayor demanda de contenidos locales curados, itinerarios personalizados y actividades únicas.                       |
| **Adopción de IA y análisis de datos**            | La IA para personalizar recomendaciones, predecir demanda y optimizar precios se ha convertido en estándar de la industria turística global.               | Mejora de la experiencia del usuario, incremento en la retención y diferenciación frente a plataformas genéricas. |
| **Penetración de smartphones**                     | El 82% de los colombianos tiene acceso a smartphone. Los turistas investigan, reservan y comparten experiencias principalmente desde dispositivos móviles.  | Necesidad de una aplicación móvil nativa o PWA como canal principal de la plataforma.                              |
| **Política pública de competitividad turística** | El Plan Sectorial de Turismo de Sincelejo 2023-2025 identifica la digitalización como eje estratégico para la competitividad del destino.                  | Posibilidad de cofinanciación pública y alianzas institucionales que reducen la barrera de entrada al mercado.     |

---

## 4. Oportunidad de Negocio

| Elemento                        | Descripción                                                                                                                                                                                                                                                                                                                         |
| ------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Oportunidad central**   | Desarrollar la primera plataforma digital integral de turismo para el departamento de Sucre, que conecte turistas con servicios locales (guías, transporte, hospedaje, gastronomía y actividades experienciales), utilizando IA para personalizar la experiencia y facilitando la reserva desde un único punto de acceso digital. |
| **Problema que resuelve** | La oferta turística fragmentada impide que el turista planifique su visita a Sucre con la misma facilidad que lo haría a destinos con plataformas consolidadas como Cartagena o Medellín. Los operadores locales pierden ventas por no tener visibilidad digital.                                                                 |
| **Tamaño del mercado**   | Sucre recibió aproximadamente 890.000 turistas en 2023 (Gobernación de Sucre). El gasto promedio por turista es de $350.000 COP. Mercado potencial estimado:**$311.500 millones COP anuales**.                                                                                                                               |
| **Momento de mercado**    | La recuperación post-pandemia del turismo nacional (+18% en 2024), el auge del turismo experiencial y la ausencia de competidores locales directos crean una ventana de oportunidad para ser primeros en el mercado.                                                                                                                |

---

## 5. Idea de Negocio

### 5.1 Definición General

| Elemento                       | Descripción                                                                                                                                                                                                                                                              |
| ------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Cliente**              | Turistas nacionales e internacionales que visitan o planean visitar Sucre, y operadores turísticos locales (guías, hoteles, restaurantes, transportadores, prestadores de actividades) que buscan mayor visibilidad y canal de ventas digital.                          |
| **Propuesta de valor**   | Una plataforma única que permite planificar, reservar y vivir experiencias turísticas completas en Sucre: catálogo verificado de servicios, recomendaciones personalizadas por IA, itinerarios sugeridos, pago integrado y asistencia en tiempo real durante el viaje. |
| **Forma de ingresos**    | Comisión del 8-12% por reserva (modelo marketplace); suscripción mensual para operadores (visibilidad premium); publicidad geolocalizada; venta de datos de inteligencia turística a entidades públicas.                                                              |
| **Factor diferenciador** | Foco 100% en Sucre con contenido curado y verificado; IA para recomendaciones personalizadas; integración de cultura, gastronomía y naturaleza en experiencias empaquetadas; alianzas institucionales con gobernación y alcaldías.                                    |

### 5.2 Business Model Canvas

**Socios Clave**

- Gobernación de Sucre y Alcaldía de Sincelejo
- Cámara de Comercio de Sincelejo
- Operadores turísticos locales verificados
- Pasarelas de pago (PSE / Wompi)
- Proveedores cloud (AWS)

**Actividades Clave**

- Desarrollo y mantenimiento de la plataforma
- Curación y verificación de contenido turístico
- Onboarding y capacitación de operadores
- Marketing digital y posicionamiento del destino
- Gestión de modelos de IA y análisis de datos

**Recursos Clave**

- Equipo técnico interdisciplinario
- Base de datos de operadores turísticos verificados
- Algoritmos de IA (recomendación + chatbot)
- Alianzas institucionales
- Marca SucreTravel

**Propuesta de Valor**

> Plataforma integral para planificar y reservar experiencias turísticas auténticas en Sucre, personalizadas por inteligencia artificial, desde un único punto de acceso digital confiable.

**Relación con Clientes**

- Aplicación móvil (autoservicio 24/7)
- Chatbot IA para asistencia en tiempo real
- Panel de gestión para operadores
- Sistema de reseñas verificadas

**Canales**

- App móvil (iOS y Android)
- Sitio web responsivo
- Redes sociales y marketing de contenido
- Alianzas con aerolíneas y agencias de viaje nacionales

**Segmentos de Clientes**

- **Turistas:** nacionales e internacionales con interés en turismo experiencial, cultural y de naturaleza
- **Operadores:** PYMES turísticas de Sucre (guías, hoteles, restaurantes, transportadores)

**Estructura de Costos**

- Desarrollo y mantenimiento de software
- Infraestructura cloud (AWS)
- Marketing digital de adquisición
- Equipo de soporte y curación de contenido
- Licencias de APIs y herramientas de IA

**Fuentes de Ingresos**

- Comisiones por reserva: 8-12% por transacción
- Suscripción premium para operadores
- Publicidad geolocalizada para negocios locales
- Datos de inteligencia turística para entidades públicas

---

## 6. Creación de la Empresa

### 6.1 Identificación Corporativa

| Item                           | Descripción                                                                                                                                                                                    |
| ------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Razón Social**        | SucreTravel S.A.S.                                                                                                                                                                              |
| **Tipo de sociedad**     | Sociedad por Acciones Simplificada — Ley 1258 de 2008 (Colombia)                                                                                                                               |
| **Objeto social**        | Desarrollo, operación y comercialización de plataformas digitales para la gestión, promoción y reserva de servicios turísticos en el departamento de Sucre y la región Caribe colombiana. |
| **Representante Legal**  | Carlos Andrés Carriazo Sierra                                                                                                                                                                  |
| **Domicilio**            | Sincelejo, Departamento de Sucre, Colombia                                                                                                                                                      |
| **Correo institucional** | contacto@sucretravel.co                                                                                                                                                                         |
| **Sitio web**            | www.sucretravel.co                                                                                                                                                                              |

### 6.2 Misión, Visión y Valores

**Misión**

> Conectar a los viajeros con lo mejor del turismo en Sucre mediante una plataforma digital inteligente que integra servicios locales, facilita la planificación de experiencias auténticas y contribuye al desarrollo económico sostenible del departamento y sus comunidades.

**Visión**

> Para 2030, ser la plataforma de referencia del turismo digital en la región Caribe colombiana, reconocida por la calidad de sus experiencias, el uso innovador de tecnología y su impacto positivo en las comunidades locales y el medioambiente.

**Valores corporativos**

- **Autenticidad local** — Promovemos la identidad genuina del territorio sucreño.
-  **Innovación tecnológica** — Adoptamos tecnologías de vanguardia para mejorar la experiencia del viajero.
-  **Inclusión económica** — Generamos oportunidades para los pequeños operadores y comunidades locales.
-  **Sostenibilidad ambiental** — Fomentamos un turismo responsable con el patrimonio natural.
-  **Transparencia y confianza** — Operamos con ética, seguridad de datos y reseñas verificadas.

---

## 7. Estrategia

### 7.1 Estrategia General y Ventaja Competitiva

| Item                            | Descripción                                                                                                                                                                                                                                                                                                                         |
| ------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Estrategia**            | Estrategia de**diferenciación enfocada en el nicho regional**: ser la primera plataforma turística integral del departamento de Sucre, estableciendo alianzas con operadores locales y entidades de turismo departamental para construir una base sólida de oferta verificada antes de escalar a otras regiones del Caribe. |
| **Ventaja competitiva**   | Conocimiento profundo del territorio sucreño, alianzas con gobernación y alcaldías, contenido local auténtico y curado, personalización por IA y soporte en tiempo real: aspectos que plataformas globales como Booking o TripAdvisor no ofrecen con foco específico en Sucre.                                                 |
| **Estrategia de entrada** | **Fase 1 (0-6 meses):** Lanzamiento MVP con los 5 municipios de mayor flujo turístico (Sincelejo, Tolú, Coveñas, San Marcos, Morroa). **Fase 2 (6-18 meses):** Expansión al resto del departamento. **Fase 3 (18-36 meses):** Escala regional Caribe.                                                          |
| **Posicionamiento**       | _"El Sucre que no conocías, a un clic de distancia"_ — plataforma que revela la riqueza turística auténtica del departamento con tecnología de punta y experiencias personalizadas.                                                                                                                                           |

### 7.2 Análisis Competitivo

| Criterio                 |    SucreTravel    |  Booking.com  | TripAdvisor | Operadores locales |
| ------------------------ | :---------------: | :------------: | :---------: | :----------------: |
| Foco en Sucre            |       Alto       |      Bajo      |    Bajo    |        Alto        |
| IA y personalización    |        Sí        |    Básico    |   Básico   |         No         |
| Contenido local curado   |       Alto       |      Bajo      |    Medio    |        Alto        |
| Reserva integrada        |        Sí        |      Sí      |     No     |      Parcial      |
| Alianzas institucionales |        Sí        |       No       |     No     |      Parcial      |
| Chatbot asistente        |        Sí        |    Básico    |     No     |         No         |
| Precio para operadores   | Comisión por uso | Alta comisión |  Freemium  |     Sin costo     |

---

## 8. MVP — Producto Mínimo Viable

### 8.1 Funcionalidades Principales

| # | Funcionalidad                                | Descripción                                                                                                                                                            | Prioridad | Sprint |
| - | -------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :-------: | :----: |
| 1 | **Catálogo de servicios turísticos** | Listado de guías, hoteles, restaurantes y actividades en Sucre con descripción, fotos, precios, calificaciones y disponibilidad en tiempo real.                       |   Alta   |   1   |
| 2 | **Motor de búsqueda y filtros**       | Búsqueda por tipo de experiencia, municipio, rango de precios, fechas y calificación, con resultados ordenados por relevancia y distancia.                            |   Alta   |   1   |
| 3 | **Sistema de reservas y pagos online** | Módulo de reserva directa con pasarela de pago integrada (PSE, tarjeta crédito/débito), confirmación automática por correo/SMS y gestión de cancelaciones.        |   Alta   |   2   |
| 4 | **Recomendador personalizado con IA**  | Algoritmo que sugiere experiencias según el perfil del usuario: intereses, historial de búsqueda y presupuesto. Mejora la conversión y la satisfacción del viajero. |   Alta   |   3   |
| 5 | **Panel de gestión para operadores**  | Dashboard donde los prestadores locales gestionan su perfil, actualizan disponibilidad, consultan reservas, responden reseñas y acceden a métricas de desempeño.     |   Media   |   2   |
| 6 | **Chatbot asistente de viaje**         | Asistente conversacional con NLP que responde preguntas frecuentes, ayuda a planificar itinerarios y resuelve dudas en tiempo real 24/7.                                |   Media   |   3   |
| 7 | **Mapa interactivo de atractivos**     | Visualización georreferenciada de todos los atractivos y servicios turísticos del departamento, con rutas sugeridas y navegación integrada.                          |   Media   |   4   |
| 8 | **Sistema de reseñas verificadas**    | Calificaciones y comentarios de turistas que completaron una reserva, con moderación automática por IA para detectar reseñas falsas o malintencionadas.              |   Media   |   4   |

### 8.2 Stack Tecnológico Propuesto

| Capa                            | Tecnología                     | Justificación                                                                                             |
| ------------------------------- | ------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| **Frontend Web**          | React.js + Next.js              | Renderizado del lado del servidor (SSR) para mejor SEO turístico y carga rápida en conexiones lentas.    |
| **App móvil**            | React Native (iOS + Android)    | Código compartido para ambas plataformas, reduciendo costos y tiempos de desarrollo.                      |
| **Backend**               | Node.js + NestJS                | Alta concurrencia para solicitudes simultáneas de reservas y búsquedas en temporada alta.                |
| **Base de datos**         | PostgreSQL + Redis (caché)     | Datos relacionales para reservas y transacciones; caché para búsquedas frecuentes y alta disponibilidad. |
| **IA / ML**               | Python + FastAPI + TensorFlow   | Modelos de recomendación y NLP para el chatbot, desplegados como microservicio independiente.             |
| **Infraestructura cloud** | AWS (EC2, S3, RDS, Lambda)      | Escalabilidad elástica para picos de demanda turística en temporadas altas (Semana Santa, diciembre).    |
| **Pagos**                 | PayU Colombia / Wompi           | Pasarelas con cobertura nacional, soporte PSE y cumplimiento normativo colombiano.                         |
| **DevOps**                | Docker + GitHub Actions (CI/CD) | Despliegue continuo y automatizado, reduciendo tiempos de entrega de nuevas funcionalidades.               |

---

## 9. Justificación del Uso de Inteligencia Artificial

| Uso de IA                                        | Descripción técnica                                                                                                                                                                                                      | Justificación de negocio                                                                                                                                                                    |
| ------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Motor de recomendación personalizada**  | Algoritmo de filtrado colaborativo y basado en contenido (_collaborative + content-based filtering_) que analiza historial de búsqueda, perfil del usuario y patrones de reseñas para sugerir experiencias relevantes. | Incrementa la tasa de conversión (reservas/visitas) y el ticket promedio al exponer al usuario a opciones que de otro modo no descubriría. Estándar probado en Netflix, Spotify y Airbnb. |
| **Chatbot de asistencia al viajero (NLP)** | Modelo de lenguaje natural entrenado con FAQs turísticas de Sucre, capaz de responder consultas, sugerir itinerarios según preferencias del usuario y escalar a agente humano cuando sea necesario.                      | Reduce en 60-70% las consultas de atención al cliente, permite operar 24/7 sin costo de personal adicional y mejora la experiencia previa al viaje.                                         |
| **Análisis de sentimiento de reseñas**   | Modelo NLP de clasificación de texto que analiza reseñas de turistas para detectar patrones positivos/negativos por tipo de servicio, ubicación y temporada del año.                                                   | Proporciona inteligencia accionable a los operadores para mejorar su oferta, y a la plataforma para priorizar y destacar servicios de alta calidad verificada.                               |
| **Predicción de demanda turística**      | Modelo de series de tiempo (LSTM / Prophet) que predice flujos turísticos por destino, temporada y tipo de servicio, integrando variables climáticas y de calendario de eventos locales.                                 | Permite a los operadores ajustar precios dinámicamente (_revenue management_), optimizar inventarios y planificar capacidad con anticipación, maximizando ingresos en temporada alta.    |

---

## 10. Organización

| Rol                                             | Responsabilidades principales                                                                                                                                       | Perfil requerido                                                                                                    |
| ----------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| **CEO / Gerente General**                 | Define la visión estratégica, gestiona alianzas institucionales, representa la empresa ante inversores y entidades públicas. Toma decisiones de alto nivel.      | Liderazgo, visión de negocio, conocimiento del ecosistema turístico regional y habilidades de negociación.       |
| **Gerente de Producto (Product Manager)** | Define el roadmap del producto, prioriza funcionalidades, coordina equipos técnicos y de negocio, y gestiona el backlog con metodologías ágiles.                 | Experiencia en Scrum/Kanban, design thinking y métricas de producto (OKRs, KPIs de conversión).                   |
| **Desarrollador Full Stack**              | Diseña, construye y mantiene todos los módulos de la plataforma: frontend, backend, base de datos e integraciones con APIs externas (pagos, mapas).               | Dominio de React, Node.js, PostgreSQL, REST APIs y prácticas de desarrollo seguro (OWASP).                         |
| **Especialista en IA / Data Science**     | Desarrolla, entrena y mantiene los modelos de recomendación, chatbot NLP y predicción de demanda. Gestiona la infraestructura de datos y pipelines de ML.         | Python, TensorFlow/PyTorch, scikit-learn, manejo de datos no estructurados y MLOps (despliegue de modelos).         |
| **Especialista en Marketing y Alianzas**  | Gestiona la adquisición de usuarios y operadores, desarrolla alianzas institucionales, administra redes sociales y campañas de posicionamiento del destino Sucre. | Marketing digital, SEO/SEM, gestión de comunidades y conocimiento del ecosistema turístico del Caribe colombiano. |

---

## 11. Documentos de Referencia

| Documento                                               | Utilidad en el taller                                                                                                                                | Enlace                                                                                                                                       |
| ------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| Plan de Desarrollo Departamental de Sucre 2020-2023     | Entender la estrategia del departamento, prioridades económicas, inversión pública y visión del territorio. Construcción del contexto del caso. | [Ver documento](https://fundacionexe.org.co/wp-content/uploads/2024/03/Plan-de-Desarrollo-Departamental-de-Sucre-2020-2023-Sucre-diferente.pdf) |
| Plan Sectorial de Turismo Sincelejo / Región 2023-2025 | Describe problemas y oportunidades del turismo, digitalización y promoción del destino. Identificación de elementos del entorno.                  | [Ver documento](https://www.alcaldiadesincelejo.gov.co/MiMunicipio/Prueba/PLAN%20SECTORIAL%20TURISMO%202023-2025.pdf)                           |
| Plan de Desarrollo Turístico del Departamento de Sucre | Define programas para desarrollar el turismo, competitividad del destino y productos turísticos. Identificación de drivers.                        | [Ver documento](https://www.academia.edu/36509724/PLAN_DE_DESARROLLO_TUR%C3%8DSTICO_DEL_DEPARTAMENTO_DE_SUCRE_2012_2015)                        |
| Ruta Competitiva de Turismo Vacacional Sucre            | Define actores del ecosistema turístico y gobernanza. Identificación de stakeholders y estructura del sector.                                      | [Ver documento](https://es.slideshare.net/slideshow/plan-de-accin-ruta-competitiva-turismo-vacacional-sucre/61161944)                           |

---

_Documento elaborado por:_
_Carlos Andrés Carriazo Sierra · Santiago Visbal Romero · Leonard Andrés Ortega González · David Escudero Vidual_
_Sincelejo, Sucre — Marzo 2026_
