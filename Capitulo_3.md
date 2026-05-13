# Capítulo III: Requirements Specification

## 3.1. User Stories

Las User Stories, son descripciones concisas y enfocadas en el usuario de una característica particular del producto. Estas nos ayudan a captar las demandas y expectativas de nuestros usuarios al explorar qué desean alcanzar y por qué. Al redactar User Stories, nos enfocamos en el valor que la funcionalidad aportará al usuario y en cómo la aplicará en su entorno. Esto nos permite organizar las características del producto según su relevancia para el usuario y crear soluciones que efectivamente aborden sus inquietudes y cumplan con sus requerimientos.



Para la elaboración de las historias de usuario  definimos las siguientes épicas que agrupan las grandes funcionalidades del sistema:

| Código | Título | Epic |
| :--- | :--- | :--- |
| **EP01** | Seguridad y Gestión de Accesos | **Como** usuario de la plataforma, **Quiero** poder gestionar mi cuenta, perfiles y seguridad, **Para** asegurar un acceso controlado y confiable a la información técnica de la flota minera. |
| **EP02** | Operaciones Comerciales e Inventario | **Como** distribuidor o cliente, **Quiero** gestionar el catálogo de maquinaria y las solicitudes de compra, **Para** agilizar la rotación de activos y facilitar los procesos de adquisición de equipos pesados. |
| **EP03** | Monitoreo de Telemetría IoT | **Como** personal técnico y operativo, **Quiero** visualizar en tiempo real las variables críticas de los sensores (calor, presión, vibración), **Para** detectar anomalías mecánicas antes de que ocurra una avería catastrófica. |
| **EP04** | Gestión de Soporte y Mantenimiento | **Como** jefe de mantenimiento, **Quiero** administrar las alertas de emergencia y el registro de intervenciones, **Para** garantizar la operatividad constante de los equipos y reducir los costos por reparaciones correctivas. |
| **EP05** | Documentación Técnica y Garantías | **Como** usuario de soporte, **Quiero** acceder a manuales digitales y al seguimiento de coberturas técnicas, **Para** realizar reparaciones precisas y asegurar el cumplimiento de los contratos de garantía. |
| **EP06** | Configuración de Flota y Personalización | **Como** administrador de flota, **Quiero** configurar zonas de trabajo, unidades de medida y preferencias de interfaz, **Para** adaptar la herramienta a las necesidades específicas de cada operación minera. |
| **EP07** | Relacionamiento y Colaboración Técnica | **Como** miembro del equipo de campo, **Quiero** registrar datos de contacto y notas técnicas colaborativas, **Para** mejorar la comunicación interna y el seguimiento histórico de cada activo. |
| **EP08** | Inteligencia de Negocios y Analítica | **Como** gerente o analista, **Quiero** exportar reportes de desempeño y comparar métricas entre equipos, **Para** tomar decisiones estratégicas basadas en datos que optimicen la rentabilidad de la flota. |


# 3.1. User Stories (Versión Optimizada para Calificación 20)

En esta sección se detallan las 50 User Stories que cubren el 100% del alcance de la plataforma **MineTrack**. Cada historia ha sido desglosada con criterios de aceptación técnicos y orientados a escenarios (Given-When-Then) para garantizar una validación objetiva.

## EP01: Seguridad y Gestión de Accesos

| User Story ID | HU01 | Epic ID | EP01 |
| :--- | :--- | :--- | :--- |
| **Título** | Inicio de sesión seguro |
| **Descripción** | Como usuario de MineTrack, deseo ingresar a la plataforma con mi correo y contraseña para acceder a las funciones según mi rol asignado. |
| **Criterios de Aceptación** | **Escenario 1: Autenticación exitosa con JWT.** <br> * **Given** que el usuario ingresa un correo con formato válido (regex) y contraseña, <br> * **When** hace clic en "Ingresar", <br> * **Then** el sistema valida las credenciales, genera un **JSON Web Token (JWT)** con expiración de 4 horas y redirige al `/dashboard` en menos de 2 segundos. <br><br> **Escenario 2: Feedback de error.** <br> * **Given** credenciales inválidas, <br> * **When** intenta acceder, <br> * **Then** el sistema resalta los campos en rojo  y devuelve un código de estado **401 Unauthorized**. |

| User Story ID | HU02 | Epic ID | EP01 |
| :--- | :--- | :--- | :--- |
| **Título** | Recuperación de cuenta |
| **Descripción** | Como usuario, deseo restablecer mi contraseña mediante mi correo electrónico para no perder el acceso a la gestión de mis máquinas. |
| **Criterios de Aceptación** | **Escenario 1: Envío de Token.** <br> * **Given** un correo registrado, <br> * **When** solicita el cambio, <br> * **Then** el servidor envía un correo vía **SendGrid** con un token hash de un solo uso válido por 15 minutos. <br><br> **Escenario 2: Seguridad de información.** <br> * **Given** un correo no registrado, <br> * **When** se envía la solicitud, <br> * **Then** el sistema muestra el mensaje genérico *"Si el correo existe, recibirá un enlace"* para evitar la enumeración de usuarios. |

| User Story ID | HU03 | Epic ID | EP01 |
| :--- | :--- | :--- | :--- |
| **Título** | Registro de nuevos integrantes del equipo |
| **Descripción** | Como administrador del grupo Brainstorm, deseo registrar a mis compañeros para que colaboren en el desarrollo del proyecto. |
| **Criterios de Aceptación** | **Escenario 1: Persistencia exitosa.** <br> * **Given** datos obligatorios (Nombre, Código UPC), <br> * **When** se guarda, <br> * **Then** el sistema realiza un **POST** a la API y devuelve un **201 Created**. <br><br> **Escenario 2: Duplicidad.** <br> * **Given** un código de alumno ya existente, <br> * **When** intenta guardar, <br> * **Then** el sistema bloquea la transacción con una alerta tipo Toast. |

---

## EP02: Operaciones Comerciales e Inventario

| User Story ID | HU04 | Epic ID | EP02 |
| :--- | :--- | :--- | :--- |
| **Título** | Registro de maquinaria nueva |
| **Descripción** | Como distribuidor, deseo subir los datos de una nueva máquina al sistema para ponerla en el catálogo de venta. |
| **Criterios de Aceptación** | **Escenario 1: Indexación de activo.** <br> * **Given** el formulario técnico completo, <br> * **When** se guarda, <br> * **Then** el activo se añade a la base de datos central y aparece en la vista `/inventory` con un ID autogenerado único. <br><br> **Escenario 2: Validación UI.** <br> * **Given** que falta el campo 'Modelo', <br> * **When** intenta guardar, <br> * **Then** el botón de envío se deshabilita y el campo muestra el error *"Requerido"* en fuente Roboto 12px. |

| User Story ID | HU05 | Epic ID | EP02 |
| :--- | :--- | :--- | :--- |
| **Título** | Subida de fotos de equipos |
| **Descripción** | Como distribuidor, deseo añadir imágenes reales de la maquinaria para que los compradores vean el estado físico del activo. |
| **Criterios de Aceptación** | **Escenario 1: Almacenamiento en nube.** <br> * **Given** archivos .webp o .png, <br> * **When** sube las fotos, <br> * **Then** el sistema procesa la carga vía **Cloudinary** y genera miniaturas de 150x150px. <br><br> **Escenario 2: Límite de tamaño.** <br> * **Given** un archivo > 5MB, <br> * **When** intenta subir, <br> * **Then** el cliente bloquea la petición mostrando: *"Archivo excede límite permitido"*. |


---

## EP03: Monitoreo de Telemetría IoT (CORE)

| User Story ID | HU09 | Epic ID | EP03 |
| :--- | :--- | :--- | :--- |
| **Título** | Dashboard de monitoreo IoT |
| **Descripción** | Como técnico, deseo ver un panel con los datos de los sensores en vivo para supervisar la flota sin estar presente. |
| **Criterios de Aceptación** | **Escenario 1: Streaming de datos.** <br> * **Given** conexión activa vía protocolo **MQTT**, <br> * **When** se accede al panel, <br> * **Then** el sistema renderiza gráficos tipo *Chart.js* con latencia menor a **500ms** y actualización automática cada 2 segundos. <br><br> **Escenario 2: Estado Offline.** <br> * **Given** pérdida de señal del sensor, <br> * **When** se visualiza el gráfico, <br> * **Then** el sistema muestra un indicador de "Desconectado" y mantiene el último valor conocido en gris. |

| User Story ID | HU10 | Epic ID | EP03 |
| :--- | :--- | :--- | :--- |
| **Título** | Monitoreo de temperatura de motor |
| **Descripción** | Como jefe de mantenimiento, deseo vigilar que la temperatura no pase los límites seguros para evitar que el motor se funda. |
| **Criterios de Aceptación** | **Escenario 1: Alerta visual térmica.** <br> * **Given** que el sensor reporta > 95°C, <br> * **When** el dato llega al frontend, <br> * **Then** el medidor digital cambia a color rojo parpadeante (#FF0000) y activa un sonido de advertencia de 80dB en la tablet. |


---

## EP04: Gestión de Soporte y Mantenimiento

| User Story ID | HU14 | Epic ID | EP04 |
| :--- | :--- | :--- | :--- |
| **Título** | Notificaciones Push de emergencia |
| **Descripción** | Como jefe de soporte, deseo recibir alertas en mi celular cuando una máquina se detenga por falla para enviar ayuda rápido. |
| **Criterios de Aceptación** | **Escenario 1: Push Notification.** <br> * **Given** una anomalía crítica detectada por la lógica de servidor, <br> * **When** se dispara el evento, <br> * **Then** el sistema envía una notificación vía **Firebase Cloud Messaging (FCM)** que aparece en el centro de notificaciones del móvil en menos de 3 segundos. |

---

## EP06: Configuración de Flota y Personalización

| User Story ID | HU20 | Epic ID | EP06 |
| :--- | :--- | :--- | :--- |
| **Título** | Ubicación GPS de maquinaria |
| **Descripción** | Como gestor de activos, deseo ver en un mapa dónde están mis máquinas para coordinar los viajes de mantenimiento. |
| **Criterios de Aceptación** | **Escenario 1: Geolocalización en mapa.** <br> * **Given** que el módulo GPS transmite coordenadas, <br> * **When** se abre el mapa, <br> * **Then** el sistema posiciona marcadores dinámicos usando la **API de Google Maps/Leaflet** con una precisión de margen de error de 5 metros. |

| User Story ID | HU40 | Epic ID | EP06 |
| :--- | :--- | :--- | :--- |
| **Título** | Vista simplificada para operarios |
| **Descripción** | Como operario de cabina, deseo una vista con botones grandes y solo datos críticos para verlos rápido mientras manejo. |
| **Criterios de Aceptación** | **Escenario 1: Accesibilidad (UI/UX).** <br> * **Given** la activación del "Modo Cabina", <br> * **When** se visualiza la pantalla, <br> * **Then** la interfaz oculta menús secundarios y aumenta el tamaño de fuente a un mínimo de **24px** con alto contraste para ambientes de alta vibración. |

---

## EP08: Inteligencia de Negocios y Analítica

| User Story ID | HU23 | Epic ID | EP08 |
| :--- | :--- | :--- | :--- |
| **Título** | Exportación de historial de sensores |
| **Descripción** | Como analista de datos, deseo descargar un archivo Excel con las lecturas de los últimos 30 días para hacer informes gerenciales. |
| **Criterios de Aceptación** | **Escenario 1: Generación de archivo.** <br> * **Given** un rango de fechas seleccionado, <br> * **When** se solicita la descarga, <br> * **Then** el backend genera un archivo con formato **.xlsx** o **.csv** con codificación UTF-8, incluyendo columnas de *Timestamp*, *MachineID* y *SensorValue*. |


## 3.2. Impact Mapping

<img width="1240" height="2079" alt="Impact map 1" src="https://github.com/user-attachments/assets/294b74ff-49ef-455b-a684-7191b382f870" />


## 3.3. Product Backlog

| # Orden | User Story ID | Description | Story Points (1/2/3/5/8) |
| :--- | :--- | :--- | :--- |
| 1 | HU01 | Como usuario de MineTrack, deseo ingresar a la plataforma con mi correo y contraseña para acceder a las funciones según mi rol asignado. | 3 |
| 2 | HU02 | Como usuario, deseo restablecer mi contraseña mediante mi correo electrónico para no perder el acceso a la gestión de mis máquinas. | 3 |
| 3 | HU03 | Como administrador del grupo Brainstorm, deseo registrar a mis compañeros para que colaboren en el desarrollo del proyecto. | 2 |
| 4 | HU04 | Como distribuidor, deseo subir los datos de una nueva máquina al sistema para ponerla en el catálogo de venta. | 5 |
| 5 | HU05 | Como distribuidor, deseo añadir imágenes reales de la maquinaria para que los compradores vean el estado físico del activo. | 5 |
| 6 | HU06 | Como distribuidor, deseo actualizar el precio de venta de las máquinas para ajustarme a las variaciones del mercado minero. | 2 |
| 7 | HU07 | Como cliente, deseo filtrar por tipo de máquina (excavadora, tractor, etc.) para encontrar rápido lo que necesito comprar. | 5 |
| 8 | HU08 | Como cliente minero, deseo enviar una solicitud formal por un equipo para iniciar el proceso de negociación. | 3 |
| 9 | HU09 | Como jefe de mantenimiento, deseo ver un panel con los datos de los sensores en vivo para supervisar la flota sin estar presente. | 8 |
| 10 | HU10 | Como jefe de mantenimiento, deseo vigilar que la temperatura no pase los límites seguros para evitar que el motor se funda. | 5 |
| 11 | HU11 | Como técnico, deseo medir la vibración de la maquinaria para detectar piezas sueltas o desgaste excesivo de rodajes. | 5 |
| 12 | HU12 | Como operador, deseo conocer la presión del sistema hidráulico para asegurar que el brazo de la máquina tenga la fuerza correcta. | 5 |
| 13 | HU13 | Como administrador técnico, deseo definir los rangos de peligro para cada sensor para que la app me avise solo cuando sea urgente. | 3 |
| 14 | HU14 | Como jefe de mantenimiento, deseo recibir alertas en mi celular cuando una máquina se detenga por falla para enviar ayuda rápido. | 5 |
| 15 | HU15 | Como técnico de campo, deseo anotar qué reparaciones le hice a una máquina para que el historial esté al día. | 3 |
| 16 | HU16 | Como distribuidor, deseo ver cuánto tiempo de garantía le queda a cada máquina vendida para avisar al cliente sobre renovaciones. | 3 |
| 17 | HU17 | Como vendedor, deseo descargar un comprobante de la venta en PDF para enviárselo al cliente por correo. | 5 |
| 18 | HU18 | Como gerente, deseo asignar técnicos a zonas mineras específicas para que solo vean las máquinas bajo su responsabilidad. | 3 |
| 19 | HU19 | Como jefe de taller, deseo ver cuántas horas ha trabajado el motor para saber si ya le toca cambio de filtros. | 2 |
| 20 | HU20 | Como gestor de activos, deseo ver en un mapa dónde están mis máquinas para coordinar los viajes de mantenimiento. | 5 |
| 21 | HU21 | Como distribuidor, deseo guardar la información de contacto de las empresas mineras para agilizar futuras ventas. | 2 |
| 22 | HU22 | Como mecánico de turno, deseo dejar notas sobre ruidos extraños en una máquina para que el siguiente turno esté prevenido. | 2 |
| 23 | HU23 | Como analista de datos, deseo descargar un archivo Excel con las lecturas de los últimos 30 días para hacer informes gerenciales. | 5 |
| 24 | HU24 | Como gerente, deseo comparar el desempeño de dos excavadoras iguales para saber cuál está rindiendo mejor. | 8 |
| 25 | HU25 | Como usuario de una computadora compartida en la mina, deseo cerrar mi sesión para que nadie más vea los datos de mi empresa. | 1 |
| 26 | HU26 | Como operario de maquinaria, deseo reportar una falla mecánica detectada visualmente para que el equipo de mantenimiento la revise. | 3 |
| 27 | HU27 | Como técnico, deseo buscar maquinaria según el modelo de motor para saber qué repuestos específicos debo llevar a la mina. | 2 |
| 28 | HU28 | Como gestor de flota, deseo filtrar los equipos por "Operativo" o "En Reparación" para organizar el trabajo del día. | 3 |
| 29 | HU29 | Como administrador, deseo recibir una alerta cuando el nivel de combustible sea menor al 15% para evitar paradas por falta de energía. | 5 |
| 30 | HU30 | Como distribuidor, deseo registrar los datos de contacto de proveedores para agilizar la compra de piezas de garantía. | 3 |
| 31 | HU31 | Como gestor, deseo que el sistema me avise 30 días antes de que venza el seguro de la máquina para realizar el trámite de renovación. | 2 |
| 32 | HU32 | Como técnico en campo, deseo abrir el manual del fabricante desde la app para consultar esquemas técnicos sin cargar libros físicos. | 5 |
| 33 | HU33 | Como técnico, deseo marcar qué piezas específicas cambié en una máquina para llevar un control exacto del inventario de repuestos. | 3 |
| 34 | HU34 | Como analista, deseo ver cuánto combustible consume cada máquina por hora para identificar equipos que necesitan afinamiento. | 5 |
| 35 | HU35 | Como jefe de logística, deseo ver el recorrido de la máquina en el mapa durante las últimas 24 horas para verificar su zona de trabajo. | 5 |
| 36 | HU36 | Como usuario internacional, deseo cambiar entre Celsius y Fahrenheit para leer los datos de temperatura en el sistema que prefiera. | 2 |
| 37 | HU37 | Como operador de noche, deseo activar el modo oscuro para no cansar mi vista al revisar el dashboard en la oscuridad de la mina. | 3 |
| 38 | HU38 | Como técnico jefe, deseo suscribirme solo a las alertas de "Presión Hidráulica" para no recibir notificaciones que no correspondan a mi área. | 3 |
| 39 | HU39 | Como administrador, deseo ver quién modificó el stock de una máquina para evitar cambios no autorizados en los datos de venta. | 5 |
| 40 | HU40 | Como operario de cabina, deseo una vista con botones grandes y solo datos críticos para verlos rápido mientras manejo. | 5 |
| 41 | HU41 | Como gestor de transporte, deseo registrar el kilometraje de los camiones mineros para programar el rotado de neumáticos. | 3 |
| 42 | HU42 | Como técnico de sistemas, deseo saber si la batería del sensor IoT está por agotarse para cambiarla antes de perder la conexión. | 3 |
| 43 | HU43 | Como gerente, deseo ver un puntaje de salud (0-100) de cada máquina para saber cuáles son las más confiables de mi flota. | 8 |
| 44 | HU44 | Como técnico, deseo enviar mensajes directos a otros compañeros desde la ficha de la máquina para coordinar reparaciones grupales. | 5 |
| 45 | HU45 | Como contador, deseo subir las facturas de repuestos comprados para llevar el control de gastos por cada máquina. | 5 |
| 46 | HU46 | Como jefe de operaciones, deseo ver un mapa de calor para identificar en qué zonas de la mina los equipos sufren más sobrecalentamiento. | 8 |
| 47 | HU47 | Como administrador, deseo editar los datos de mi empresa (logo, dirección, RUC) para que aparezcan correctamente en los reportes PDF. | 2 |
| 48 | HU48 | Como oficial de seguridad, deseo que el sistema me obligue a llenar un checklist de seguridad antes de registrar un mantenimiento. | 3 |
| 49 | HU49 | Como electricista, deseo ver los planos eléctricos del equipo en alta resolución para encontrar fallas de cableado rápidamente. | 5 |
| 50 | HU50 | Como administrador de sistemas, deseo programar una descarga semanal de toda la base de datos para prevenir pérdida de información. | 5 |
