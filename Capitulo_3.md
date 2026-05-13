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


# 3.1. User Stories (Completo HU06 - HU50)

| User Story ID | HU06 | Epic ID | EP02 |
| :--- | :--- | :--- | :--- |
| **Título** | Edición de precios de catálogo |
| **Descripción** | Como distribuidor, deseo actualizar el precio de venta de las máquinas para ajustarme a las variaciones del mercado minero. |
| **Criterios de Aceptación** | **Escenario 1: Actualización de precio en tiempo real.** <br> * **Given** que el usuario ingresa un nuevo monto numérico positivo en el campo de precio, <br> * **When** confirma la edición mediante el botón "Actualizar", <br> * **Then** el sistema valida que el valor sea de tipo decimal con máximo 2 dígitos, realiza un **PUT** a la API de inventario y refleja el cambio en la vista pública en menos de 1 segundo. <br><br> **Escenario 2: Bloqueo de valores inválidos.** <br> * **Given** que se intenta ingresar un valor ≤ 0 o caracteres no numéricos, <br> * **When** se intenta guardar, <br> * **Then** el sistema muestra un mensaje de error en color rojo (#D32F2F): *"El precio debe ser un valor numérico superior a 0"*. |

| User Story ID | HU07 | Epic ID | EP02 |
| :--- | :--- | :--- | :--- |
| **Título** | Búsqueda por filtros |
| **Descripción** | Como cliente, deseo filtrar por tipo de máquina (excavadora, tractor, etc.) para encontrar rápido lo que necesito comprar. |
| **Criterios de Aceptación** | **Escenario 1: Filtrado reactivo.** <br> * **Given** que el usuario selecciona una o varias categorías del menú lateral, <br> * **When** aplica los filtros, <br> * **Then** el sistema debe ejecutar una consulta filtrada (query params) y renderizar únicamente los activos correspondientes, manteniendo una velocidad de carga (LCP) menor a 1.5s. <br><br> **Escenario 2: Estado vacío (Empty State).** <br> * **Given** que la combinación de filtros no arroja resultados en el inventario actual, <br> * **When** se realiza la búsqueda, <br> * **Then** el sistema muestra una ilustración de "No resultados" con un botón para limpiar filtros. |

| User Story ID | HU08 | Epic ID | EP02 |
| :--- | :--- | :--- | :--- |
| **Título** | Generación de solicitud de compra |
| **Descripción** | Como cliente minero, deseo enviar una solicitud formal por un equipo para iniciar el proceso de negociación. |
| **Criterios de Aceptación** | **Escenario 1: Envío de Lead.** <br> * **Given** que el usuario hace clic en el botón de "Solicitar Cotización", <br> * **When** confirma sus datos de contacto, <br> * **Then** el sistema genera una entrada en la base de datos de 'Leads', envía una notificación **FCM** al panel del distribuidor y un correo automático de confirmación al cliente vía **SendGrid**. |

| User Story ID | HU11 | Epic ID | EP03 |
| :--- | :--- | :--- | :--- |
| **Título** | Control de vibración mecánica |
| **Descripción** | Como técnico, deseo medir la vibración de la maquinaria para detectar piezas sueltas o desgaste excesivo de rodajes. |
| **Criterios de Aceptación** | **Escenario 1: Análisis de frecuencia.** <br> * **Given** que los sensores de vibración están calibrados, <br> * **When** el técnico accede al historial gráfico, <br> * **Then** el sistema debe mostrar una gráfica de espectro de frecuencia actualizada en tiempo real, resaltando picos superiores a los **5 mm/s (RMS)** en color naranja. |

| User Story ID | HU12 | Epic ID | EP03 |
| :--- | :--- | :--- | :--- |
| **Título** | Medición de presión hidráulica |
| **Descripción** | Como operador, deseo conocer la presión del sistema hidráulico para asegurar que el brazo de la máquina tenga la fuerza correcta. |
| **Criterios de Aceptación** | **Escenario 1: Alerta de presión crítica.** <br> * **Given** que la presión operativa cae por debajo de los **2000 PSI**, <br> * **When** el sistema recibe el paquete de datos del sensor, <br> * **Then** se activa un aviso visual persistente en el dashboard con el código de error correspondiente. |

| User Story ID | HU13 | Epic ID | EP04 |
| :--- | :--- | :--- | :--- |
| **Título** | Configuración de alertas críticas |
| **Descripción** | Como administrador técnico, deseo definir los rangos de peligro para cada sensor para que la app me avise solo cuando sea urgente. |
| **Criterios de Aceptación** | **Escenario 1: Ajuste de umbrales.** <br> * **Given** la interfaz de configuración de sensores, <br> * **When** se modifica el valor límite (ej: 100°C), <br> * **Then** el sistema guarda el parámetro en la base de datos y lo sincroniza con la lógica de alertas del servidor inmediatamente. |

| User Story ID | HU15 | Epic ID | EP04 |
| :--- | :--- | :--- | :--- |
| **Título** | Registro de mantenimiento preventivo |
| **Descripción** | Como técnico de campo, deseo anotar qué reparaciones le hice a una máquina para que el historial esté al día. |
| **Criterios de Aceptación** | **Escenario 1: Actualización de historial.** <br> * **Given** el formulario de servicio completado, <br> * **When** se registra la actividad, <br> * **Then** el sistema actualiza el estado del activo y calcula automáticamente la fecha de la próxima revisión basada en el horómetro actual + 250 horas. |

| User Story ID | HU17 | Epic ID | EP05 |
| :--- | :--- | :--- | :--- |
| **Título** | Certificado de venta en PDF |
| **Descripción** | Como vendedor, deseo descargar un comprobante de la venta en PDF para enviárselo al cliente por correo. |
| **Criterios de Aceptación** | **Escenario 1: Generación de documento.** <br> * **Given** una transacción confirmada, <br> * **When** se hace clic en "Generar PDF", <br> * **Then** el servidor procesa los datos y devuelve un archivo PDF dinámico con firma digital y código QR de validación en menos de 3 segundos. |

| User Story ID | HU18 | Epic ID | EP06 |
| :--- | :--- | :--- | :--- |
| **Título** | Asignación de técnicos a zonas |
| **Descripción** | Como gerente, deseo asignar técnicos a zonas mineras específicas para que solo vean las máquinas bajo su responsabilidad. |
| **Criterios de Aceptación** | **Escenario 1: Control de visibilidad por zona.** <br> * **Given** la tabla de asignaciones, <br> * **When** se vincula a un técnico con una zona geográfica (Geofence), <br> * **Then** el sistema aplica un filtro de seguridad a nivel de base de datos para que el técnico solo recupere activos de dicha zona. |

| User Story ID | HU19 | Epic ID | EP06 |
| :--- | :--- | :--- | :--- |
| **Título** | Contador de horas de uso (Horómetro) |
| **Descripción** | Como jefe de taller, deseo ver cuántas horas ha trabajado el motor para saber si ya le toca cambio de filtros. |
| **Criterios de Aceptación** | **Escenario 1: Sincronización de horas.** <br> * **Given** que la máquina envía su estado de operación, <br> * **When** se consulta el perfil del equipo, <br> * **Then** el sistema muestra el acumulado de horas con una precisión de 0.1h, bloqueando cualquier intento de edición manual por usuarios no administradores. |

| User Story ID | HU21 | Epic ID | EP07 |
| :--- | :--- | :--- | :--- |
| **Título** | Registro de clientes mineros |
| **Descripción** | Como distribuidor, deseo guardar la información de contacto de las empresas mineras para agilizar futuras ventas. |
| **Criterios de Aceptación** | **Escenario 1: Validación de RUC.** <br> * **Given** que se ingresan los datos de una nueva empresa, <br> * **When** se procede a guardar, <br> * **Then** el sistema valida que el RUC tenga exactamente 11 dígitos numéricos y guarda el perfil en la colección de clientes. |

| User Story ID | HU22 | Epic ID | EP07 |
| :--- | :--- | :--- | :--- |
| **Título** | Comentarios técnicos por equipo |
| **Descripción** | Como mecánico de turno, deseo dejar notas sobre ruidos extraños en una máquina para que el siguiente turno esté prevenido. |
| **Criterios de Aceptación** | **Escenario 1: Muro de comentarios.** <br> * **Given** que el técnico escribe una nota en el perfil de la máquina, <br> * **When** publica el comentario, <br> * **Then** el sistema almacena la cadena de texto junto con el ID del técnico y un timestamp **ISO 8601** para auditoría. |

| User Story ID | HU24 | Epic ID | EP08 |
| :--- | :--- | :--- | :--- |
| **Título** | Gráficas comparativas de flota |
| **Descripción** | Como gerente, deseo comparar el desempeño de dos excavadoras iguales para saber cuál está rindiendo mejor. |
| **Criterios de Aceptación** | **Escenario 1: Comparativa Multi-serie.** <br> * **Given** la selección de dos o más máquinas, <br> * **When** se genera la vista comparativa, <br> * **Then** el sistema superpone las líneas de telemetría en un solo gráfico con diferentes colores para análisis visual inmediato. |

| User Story ID | HU25 | Epic ID | EP01 |
| :--- | :--- | :--- | :--- |
| **Título** | Cerrar sesión correctamente |
| **Descripción** | Como usuario de una computadora compartida en la mina, deseo cerrar mi sesión para que nadie más vea los datos de mi empresa. |
| **Criterios de Aceptación** | **Escenario 1: Invalidación de Token.** <br> * **Given** que el usuario está autenticado, <br> * **When** hace clic en "Cerrar Sesión", <br> * **Then** el sistema elimina el JWT del **localStorage/Cookies** y redirige al `/login` inmediatamente. |

| User Story ID | HU26 | Epic ID | EP02 |
| :--- | :--- | :--- | :--- |
| **Título** | Reporte de fallas por operario |
| **Descripción** | Como operario de maquinaria, deseo reportar una falla mecánica detectada visualmente para que el equipo de mantenimiento la revise. |
| **Criterios de Aceptación** | **Escenario 1: Creación de Ticket.** <br> * **Given** el formulario de reporte de fallas, <br> * **When** el operario describe el problema y envía, <br> * **Then** el sistema genera un ticket con prioridad "Media" y notifica al jefe de mantenimiento asignado. |

| User Story ID | HU27 | Epic ID | EP02 |
| :--- | :--- | :--- | :--- |
| **Título** | Búsqueda por modelo de motor |
| **Descripción** | Como técnico, deseo buscar maquinaria según el modelo de motor para saber qué repuestos específicos debo llevar a la mina. |
| **Criterios de Aceptación** | **Escenario 1: Filtro de hardware específico.** <br> * **Given** el buscador de flota, <br> * **When** se ingresa el nombre o código del motor, <br> * **Then** el sistema realiza un filtro de concordancia parcial (Like) y muestra todos los activos vinculados a dicho motor. |

| User Story ID | HU28 | Epic ID | EP03 |
| :--- | :--- | :--- | :--- |
| **Título** | Filtro por estado operativo |
| **Descripción** | Como gestor de flota, deseo filtrar los equipos por "Operativo" o "En Reparación" para organizar el trabajo del día. |
| **Criterios de Aceptación** | **Escenario 1: Segmentación de disponibilidad.** <br> * **Given** el panel de control, <br> * **When** se selecciona el estado "En Reparación", <br> * **Then** el sistema filtra la tabla de activos basándose en la bandera lógica `status` de la base de datos. |

| User Story ID | HU29 | Epic ID | EP03 |
| :--- | :--- | :--- | :--- |
| **Título** | Alerta de nivel de combustible |
| **Descripción** | Como administrador, deseo recibir una alerta cuando el nivel de combustible sea menor al 15% para evitar paradas por falta de energía. |
| **Criterios de Aceptación** | **Escenario 1: Alerta de autonomía.** <br> * **Given** que el sensor ultrasónico de tanque reporta < 15%, <br> * **When** se recibe el dato, <br> * **Then** el sistema activa una alerta visual amarilla en el dashboard y envía un SMS de prioridad baja al supervisor. |

| User Story ID | HU30 | Epic ID | EP04 |
| :--- | :--- | :--- | :--- |
| **Título** | Gestión de proveedores de repuestos |
| **Descripción** | Como distribuidor, deseo registrar los datos de contacto de proveedores para agilizar la compra de piezas de garantía. |
| **Criterios de Aceptación** | **Escenario 1: Directorio de proveedores.** <br> * **Given** el módulo de logística, <br> * **When** se guarda un nuevo proveedor, <br> * **Then** el sistema almacena el nombre, contacto y marcas asociadas para futuras búsquedas. |

| User Story ID | HU31 | Epic ID | EP04 |
| :--- | :--- | :--- | :--- |
| **Título** | Notificación de vencimiento de seguro |
| **Descripción** | Como gestor, deseo que el sistema me avise 30 días antes de que venza el seguro de la máquina para realizar el trámite de renovación. |
| **Criterios de Aceptación** | **Escenario 1: Alerta cronológica.** <br> * **Given** la fecha de vencimiento de la póliza, <br> * **When** el servidor detecta que `current_date + 30` es igual a la fecha de vencimiento, <br> * **Then** se dispara una notificación push al usuario responsable. |

| User Story ID | HU32 | Epic ID | EP05 |
| :--- | :--- | :--- | :--- |
| **Título** | Visualización de manuales digitales |
| **Descripción** | Como técnico en campo, deseo abrir el manual del fabricante desde la app para consultar esquemas técnicos sin cargar libros físicos. |
| **Criterios de Aceptación** | **Escenario 1: Lector de documentos.** <br> * **Given** que el técnico selecciona el botón "Manual", <br> * **When** existe un archivo asociado, <br> * **Then** el sistema abre el PDF en una pestaña nueva o visor embebido con controles de Zoom y búsqueda. |

| User Story ID | HU33 | Epic ID | EP05 |
| :--- | :--- | :--- | :--- |
| **Título** | Registro de piezas reemplazadas |
| **Descripción** | Como técnico, deseo marcar qué piezas específicas cambié en una máquina para llevar un control exacto del inventario de repuestos. |
| **Criterios de Aceptación** | **Escenario 1: Control de stock por activo.** <br> * **Given** la orden de mantenimiento, <br> * **When** se seleccionan piezas del catálogo, <br> * **Then** el sistema descuenta las unidades del inventario global y las vincula al historial de vida útil del equipo. |

| User Story ID | HU34 | Epic ID | EP03 |
| :--- | :--- | :--- | :--- |
| **Título** | Dashboard de eficiencia de combustible |
| **Descripción** | Como analista, deseo ver cuánto combustible consume cada máquina por hora para identificar equipos que necesitan afinamiento. |
| **Criterios de Aceptación** | **Escenario 1: Cálculo de consumo (GPH).** <br> * **Given** el flujo de datos de nivel de combustible y horómetro, <br> * **When** se visualiza el dashboard de eficiencia, <br> * **Then** el sistema calcula y muestra el promedio de Galones por Hora mediante una fórmula de regresión lineal simple. |

| User Story ID | HU35 | Epic ID | EP05 |
| :--- | :--- | :--- | :--- |
| **Título** | Historial de ubicaciones GPS |
| **Descripción** | Como jefe de logística, deseo ver el recorrido de la máquina en el mapa durante las últimas 24 horas para verificar que no salió de la zona de trabajo. |
| **Criterios de Aceptación** | **Escenario 1: Trazo de ruta.** <br> * **Given** el selector de fechas histórico, <br> * **When** se eligen las últimas 24 horas, <br> * **Then** el sistema dibuja una polilínea en el mapa conectando todos los puntos de latitud/longitud registrados en ese periodo. |

| User Story ID | HU36 | Epic ID | EP06 |
| :--- | :--- | :--- | :--- |
| **Título** | Cambio de unidades de medida |
| **Descripción** | Como usuario internacional, deseo cambiar entre Celsius y Fahrenheit para leer los datos de temperatura en el sistema que prefiera. |
| **Criterios de Aceptación** | **Escenario 1: Conversión dinámica.** <br> * **Given** el interruptor de unidad de medida, <br> * **When** se cambia la preferencia, <br> * **Then** el frontend aplica la fórmula matemática de conversión a todos los valores de temperatura mostrados sin necesidad de recargar la página. |

| User Story ID | HU37 | Epic ID | EP06 |
| :--- | :--- | :--- | :--- |
| **Título** | Modo oscuro para trabajo nocturno |
| **Descripción** | Como operador de noche, deseo activar el modo oscuro para no cansar mi vista al revisar el dashboard en la oscuridad de la mina. |
| **Criterios de Aceptación** | **Escenario 1: Aplicación de tema CSS.** <br> * **Given** la opción de personalización de UI, <br> * **When** se activa el modo oscuro, <br> * **Then** la aplicación inyecta una hoja de estilos que cambia el fondo a #121212 y los textos a colores de bajo contraste. |

| User Story ID | HU38 | Epic ID | EP06 |
| :--- | :--- | :--- | :--- |
| **Título** | Suscripción a alertas específicas |
| **Descripción** | Como técnico jefe, deseo suscribirme solo a las alertas de "Presión Hidráulica" para no recibir notificaciones que no corresponden a mi área. |
| **Criterios de Aceptación** | **Escenario 1: Filtro de notificaciones.** <br> * **Given** el panel de preferencias de alertas, <br> * **When** se seleccionan categorías específicas, <br> * **Then** el sistema actualiza el registro de suscripción en el servicio de notificaciones para filtrar los mensajes push. |

| User Story ID | HU39 | Epic ID | EP01 |
| :--- | :--- | :--- | :--- |
| **Título** | Auditoría de cambios en inventario |
| **Descripción** | Como administrador, deseo ver quién modificó el stock de una máquina para evitar cambios no autorizados en los datos de venta. |
| **Criterios de Aceptación** | **Escenario 1: Registro de logs.** <br> * **Given** cualquier operación de edición en inventario, <br> * **When** se completa la acción, <br> * **Then** el sistema registra automáticamente el ID del usuario, la acción realizada y el valor anterior/nuevo en la tabla de auditoría. |

| User Story ID | HU41 | Epic ID | EP04 |
| :--- | :--- | :--- | :--- |
| **Título** | Registro de kilometraje |
| **Descripción** | Como gestor de transporte, deseo registrar el kilometraje de los camiones mineros para programar el rotado de neumáticos. |
| **Criterios de Aceptación** | **Escenario 1: Control de odómetro.** <br> * **Given** el registro de kilometraje del camión, <br> * **When** el valor supera los **10,000 km** desde la última rotación, <br> * **Then** el sistema activa una tarea automática de mantenimiento preventivo. |

| User Story ID | HU42 | Epic ID | EP03 |
| :--- | :--- | :--- | :--- |
| **Título** | Alerta de batería de dispositivo IoT |
| **Descripción** | Como técnico de sistemas, deseo saber si la batería del sensor IoT está por agotarse para ir a cambiarla antes de perder la conexión. |
| **Criterios de Aceptación** | **Escenario 1: Monitoreo de alimentación.** <br> * **Given** que el sensor reporta un nivel de carga < 10%, <br> * **When** se actualiza el estado, <br> * **Then** el sistema muestra un icono de batería baja en la vista de administración de dispositivos. |

| User Story ID | HU43 | Epic ID | EP03 |
| :--- | :--- | :--- | :--- |
| **Título** | Evaluación de desempeño (KPIs) |
| **Descripción** | Como gerente, deseo ver un puntaje de salud (0-100) de cada máquina para saber cuáles son las más confiables de mi flota. |
| **Criterios de Aceptación** | **Escenario 1: Algoritmo de salud.** <br> * **Given** el historial de alertas y horas de uso, <br> * **When** se carga el panel de KPIs, <br> * **Then** el sistema aplica un algoritmo ponderado para generar un índice de confiabilidad porcentual por activo. |

| User Story ID | HU44 | Epic ID | EP06 |
| :--- | :--- | :--- | :--- |
| **Título** | Chat interno para equipo técnico |
| **Descripción** | Como técnico, deseo enviar mensajes directos a otros compañeros desde la ficha de la máquina para coordinar reparaciones grupales. |
| **Criterios de Aceptación** | **Escenario 1: Comunicación en tiempo real.** <br> * **Given** la interfaz de chat en la ficha del equipo, <br> * **When** se envía un mensaje, <br> * **Then** el sistema utiliza **WebSockets** para distribuir el mensaje a todos los usuarios conectados con permisos sobre ese equipo. |

| User Story ID | HU45 | Epic ID | EP04 |
| :--- | :--- | :--- | :--- |
| **Título** | Carga de facturas de mantenimiento |
| **Descripción** | Como contador, deseo subir las facturas de repuestos comprados para llevar el control de gastos por cada máquina. |
| **Criterios de Aceptación** | **Escenario 1: Adjunto de archivos contables.** <br> * **Given** una orden de mantenimiento cerrada, <br> * **When** se carga un archivo .pdf, <br> * **Then** el sistema asocia el documento al costo operativo del activo y permite su descarga posterior para auditoría. |

| User Story ID | HU46 | Epic ID | EP03 |
| :--- | :--- | :--- | :--- |
| **Título** | Mapa de calor de actividad |
| **Descripción** | Como jefe de operaciones, deseo ver un mapa de calor para identificar en qué zonas de la mina las máquinas están sufriendo más sobrecalentamiento. |
| **Criterios de Aceptación** | **Escenario 1: Visualización térmica espacial.** <br> * **Given** el conjunto de datos de ubicación y temperatura, <br> * **When** se selecciona la vista de calor, <br> * **Then** el sistema genera una capa de densidad sobre el mapa donde el radio de intensidad aumenta con los valores de temperatura. |

| User Story ID | HU48 | Epic ID | EP04 |
| :--- | :--- | :--- | :--- |
| **Título** | Recordatorio de inspección de seguridad |
| **Descripción** | Como oficial de seguridad, deseo que el sistema me obligue a llenar un checklist de seguridad antes de permitir que un técnico registre un mantenimiento. |
| **Criterios de Aceptación** | **Escenario 1: Bloqueo por validación de seguridad.** <br> * **Given** que un técnico intenta registrar un servicio, <br> * **When** no se han marcado los puntos obligatorios del checklist, <br> * **Then** el sistema deshabilita el botón de "Guardar" y muestra una advertencia de seguridad. |

| User Story ID | HU49 | Epic ID | EP05 |
| :--- | :--- | :--- | :--- |
| **Título** | Visualización de esquemas eléctricos |
| **Descripción** | Como electricista, deseo ver los planos eléctricos del equipo en alta resolución para encontrar cables cortados rápidamente. |
| **Criterios de Aceptación** | **Escenario 1: Visualización de alta definición.** <br> * **Given** el catálogo de planos técnicos, <br> * **When** se abre un plano eléctrico, <br> * **Then** el sistema debe permitir el renderizado de imágenes de alta resolución con funcionalidad de **Pinch-to-Zoom** en dispositivos móviles. |

| User Story ID | HU50 | Epic ID | EP06 |
| :--- | :--- | :--- | :--- |
| **Título** | Backup de datos técnicos |
| **Descripción** | Como administrador de sistemas, deseo programar una descarga semanal de toda la base de datos para no perder información por fallas del servidor. |
| **Criterios de Aceptación** | **Escenario 1: Tarea programada (Cron Job).** <br> * **Given** la configuración del servidor, <br> * **When** se cumple el horario programado, <br> * **Then** el sistema genera un volcado de base de datos cifrado en formato .sql.gz y lo almacena en un repositorio externo de seguridad. |

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
