# Capítulo III: Requirements Specification

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

# 3.1. User Stories

| User Story ID | HU01 | Epic ID | EP00 |
| :--- | :--- | :--- | :--- |
| **Título** | Presentación de la propuesta de valor |
| **Descripción** | Como visitante, deseo visualizar el propósito de la plataforma para comprender cómo MineTrack optimiza la gestión minera. |
| **Criterios de Aceptación** | **Escenario 1: Navegación por la sección informativa.** <br> * **Given** que el visitante se encuentra en la página de inicio, <br> * **When** visualiza el contenido informativo, <br> * **Then** el sistema presenta los beneficios de la centralización y el monitoreo IoT. <br><br> **Escenario 2: Interacción con material visual de apoyo.** <br> * **Given** que el visitante explora la landing page, <br> * **When** accede a la sección de producto, <br> * **Then** el sistema muestra representaciones gráficas del dashboard para ilustrar la solución. |

| User Story ID | HU02 | Epic ID | EP00 |
| :--- | :--- | :--- | :--- |
| **Título** | Captura de prospectos (Call-To-Action) |
| **Descripción** | Como visitante interesado, deseo registrar mis datos de contacto para solicitar información comercial personalizada. |
| **Criterios de Aceptación** | **Escenario 1: Envío exitoso de datos de contacto.** <br> * **Given** que el visitante ingresa información de contacto válida en el formulario, <br> * **When** confirma la acción de envío, <br> * **Then** el sistema almacena el registro y confirma la operación al usuario. <br><br> **Escenario 2: Validación de datos incompletos.** <br> * **Given** que el visitante omite un campo obligatorio, <br> * **When** intenta realizar el envío, <br> * **Then** el sistema restringe la acción y solicita completar la información pendiente. |

| User Story ID | HU03 | Epic ID | EP01 |
| :--- | :--- | :--- | :--- |
| **Título** | Autenticación al sistema |
| **Descripción** | Como usuario de MineTrack, deseo ingresar al sistema con mis credenciales para acceder a las funciones de mi perfil. |
| **Criterios de Aceptación** | **Escenario 1: Inicio de sesión correcto.** <br> * **Given** que el usuario ingresa un correo y contraseña registrados, <br> * **When** solicita el acceso, <br> * **Then** el sistema otorga una sesión activa y redirige al panel principal. <br><br> **Escenario 2: Denegación de acceso.** <br> * **Given** que las credenciales no coinciden con los registros, <br> * **When** solicita el ingreso, <br> * **Then** el sistema informa sobre el error de autenticación y previene el acceso. |

| User Story ID | HU04 | Epic ID | EP01 |
| :--- | :--- | :--- | :--- |
| **Título** | Recuperación de credenciales |
| **Descripción** | Como usuario, deseo restablecer mi contraseña para recuperar el acceso ante la pérdida de mis datos de ingreso. |
| **Criterios de Aceptación** | **Escenario 1: Solicitud con cuenta verificada.** <br> * **Given** que el usuario ingresa su correo electrónico registrado, <br> * **When** confirma la solicitud, <br> * **Then** el sistema envía un enlace de recuperación con vigencia temporal. <br><br> **Escenario 2: Solicitud con cuenta inexistente.** <br> * **Given** que el correo ingresado no está registrado, <br> * **When** confirma la acción, <br> * **Then** el sistema presenta un mensaje genérico de confirmación para proteger la privacidad. |

| User Story ID | HU05 | Epic ID | EP02 |
| :--- | :--- | :--- | :--- |
| **Título** | Registro de activos en catálogo |
| **Descripción** | Como distribuidor, deseo registrar los datos técnicos de maquinaria nueva para incluirla en el inventario de ventas. |
| **Criterios de Aceptación** | **Escenario 1: Registro completo de equipo.** <br> * **Given** que el distribuidor ingresa los datos obligatorios de la ficha técnica, <br> * **When** guarda el registro, <br> * **Then** el sistema almacena la máquina y la visualiza en el inventario disponible. <br><br> **Escenario 2: Error por campos vacíos.** <br> * **Given** que el distribuidor omite campos críticos de identificación, <br> * **When** intenta guardar, <br> * **Then** el sistema bloquea el registro y señala las omisiones. |

| User Story ID | HU06 | Epic ID | EP02 |
| :--- | :--- | :--- | :--- |
| **Título** | Actualización de precios de mercado |
| **Descripción** | Como distribuidor, deseo actualizar el valor comercial de un equipo para ajustarlo a las fluctuaciones del mercado. |
| **Criterios de Aceptación** | **Escenario 1: Actualización válida de monto.** <br> * **Given** que el usuario ingresa un nuevo valor numérico positivo, <br> * **When** confirma la edición, <br> * **Then** el sistema actualiza el valor en el catálogo global. <br><br> **Escenario 2: Validación de valor negativo.** <br> * **Given** que el usuario intenta ingresar un precio menor o igual a cero, <br> * **When** intenta guardar, <br> * **Then** el sistema restringe la actualización y solicita un valor válido. |

| User Story ID | HU07 | Epic ID | EP00 |
| :--- | :--- | :--- | :--- |
| **Título** | Búsqueda por filtros |
| **Descripción** | Como visitante del catálogo, deseo filtrar la maquinaria por categoría para localizar activos de mi interés. |
| **Criterios de Aceptación** | **Escenario 1: Filtrado con coincidencias.** <br> * **Given** que el visitante aplica parámetros de filtrado por categoría, <br> * **When** ejecuta la consulta, <br> * **Then** el sistema recupera y expone únicamente los activos que cumplen la condición. <br><br> **Escenario 2: Consulta sin resultados disponibles.** <br> * **Given** que el visitante aplica parámetros para los cuales no hay stock, <br> * **When** ejecuta la consulta, <br> * **Then** el sistema informa la ausencia de resultados y sugiere restablecer los parámetros. |

| User Story ID | HU08 | Epic ID | EP00 |
| :--- | :--- | :--- | :--- |
| **Título** | Generación de solicitud de compra |
| **Descripción** | Como visitante interesado, deseo enviar una solicitud formal por un equipo para iniciar el proceso de negociación comercial. |
| **Criterios de Aceptación** | **Escenario 1: Creación de prospecto (Lead).** <br> * **Given** que el visitante proporciona información de contacto válida, <br> * **When** confirma el envío de la solicitud, <br> * **Then** el sistema registra el interés y notifica al distribuidor correspondiente. <br><br> **Escenario 2: Restricción sobre equipos no disponibles.** <br> * **Given** que el visitante intenta solicitar un equipo con estado de vendido, <br> * **When** interactúa con la opción de solicitud, <br> * **Then** el sistema deshabilita la acción y notifica la falta de disponibilidad. |

| User Story ID | HU09 | Epic ID | EP03 |
| :--- | :--- | :--- | :--- |
| **Título** | Dashboard de monitoreo IoT |
| **Descripción** | Como técnico, deseo supervisar el estado de los sensores IoT para controlar la salud de la maquinaria sin estar presente. |
| **Criterios de Aceptación** | **Escenario 1: Transmisión continua de telemetría.** <br> * **Given** que los sensores IoT establecen conexión con el servidor, <br> * **When** el técnico accede al módulo de monitoreo, <br> * **Then** el sistema procesa los paquetes de datos y actualiza los indicadores numéricos periódicamente. <br><br> **Escenario 2: Pérdida de comunicación con el dispositivo.** <br> * **Given** que el servidor deja de recibir paquetes de un sensor, <br> * **When** el técnico visualiza el estado del equipo, <br> * **Then** el sistema reporta la desconexión y mantiene el último registro válido como referencia. |

| User Story ID | HU10 | Epic ID | EP03 |
| :--- | :--- | :--- | :--- |
| **Título** | Monitoreo de temperatura de motor |
| **Descripción** | Como jefe de mantenimiento, deseo vigilar la temperatura del motor para prevenir daños por sobrecalentamiento. |
| **Criterios de Aceptación** | **Escenario 1: Detección de sobrecalentamiento.** <br> * **Given** que la temperatura reportada supera el umbral máximo de operación, <br> * **When** el sistema analiza el valor recibido, <br> * **Then** genera una alerta de criticidad visual para informar el estado de riesgo. <br><br> **Escenario 2: Operación en rangos normales.** <br> * **Given** que la temperatura se mantiene dentro de los parámetros seguros, <br> * **When** el sistema analiza el valor, <br> * **Then** presenta el indicador en estado nominal sin generar advertencias. |

| User Story ID | HU11 | Epic ID | EP03 |
| :--- | :--- | :--- | :--- |
| **Título** | Control de vibración mecánica |
| **Descripción** | Como técnico, deseo medir la vibración de la maquinaria para detectar piezas sueltas o desgaste mecánico. |
| **Criterios de Aceptación** | **Escenario 1: Registro de anomalías de movimiento.** <br> * **Given** que el sensor reporta niveles de vibración anómalos, <br> * **When** el técnico revisa la información del componente, <br> * **Then** el sistema destaca los picos de frecuencia que superan la tolerancia estándar. <br><br> **Escenario 2: Diagnóstico sin conectividad de sensor.** <br> * **Given** que el hardware de vibración se encuentra inactivo, <br> * **When** el técnico solicita la medición, <br> * **Then** el sistema advierte sobre la ausencia de lectura de hardware. |

| User Story ID | HU12 | Epic ID | EP03 |
| :--- | :--- | :--- | :--- |
| **Título** | Medición de presión hidráulica |
| **Descripción** | Como operador, deseo verificar la presión del sistema hidráulico para asegurar la fuerza operativa del equipo. |
| **Criterios de Aceptación** | **Escenario 1: Caída de presión operativa.** <br> * **Given** que la presión desciende del límite mínimo establecido, <br> * **When** el sistema recibe la medición actualizada, <br> * **Then** registra una incidencia preventiva e informa sobre la pérdida de fuerza. <br><br> **Escenario 2: Lectura de presión óptima.** <br> * **Given** que el fluido hidráulico mantiene la presión requerida, <br> * **When** el operador consulta el estado, <br> * **Then** el sistema presenta el valor cuantificado sin alertas adicionales. |

| User Story ID | HU13 | Epic ID | EP04 |
| :--- | :--- | :--- | :--- |
| **Título** | Configuración de alertas críticas |
| **Descripción** | Como administrador técnico, deseo definir los rangos de peligro para cada sensor para recibir notificaciones solo ante emergencias. |
| **Criterios de Aceptación** | **Escenario 1: Actualización de parámetros de seguridad.** <br> * **Given** que el administrador ingresa nuevos umbrales numéricos de advertencia, <br> * **When** confirma la configuración, <br> * **Then** el sistema ajusta la lógica de evaluación y aplica los nuevos límites. <br><br> **Escenario 2: Validación de umbrales inconsistentes.** <br> * **Given** que el administrador intenta establecer un límite mínimo mayor al máximo, <br> * **When** confirma la configuración, <br> * **Then** el sistema rechaza la regla e indica la incoherencia lógica. |

| User Story ID | HU14 | Epic ID | EP04 |
| :--- | :--- | :--- | :--- |
| **Título** | Notificaciones Push de emergencia |
| **Descripción** | Como jefe de soporte, deseo recibir alertas inmediatas en mi dispositivo móvil cuando una máquina se detiene por emergencia. |
| **Criterios de Aceptación** | **Escenario 1: Emisión exitosa de alerta móvil.** <br> * **Given** que el servidor procesa un evento de parada de emergencia, <br> * **When** determina la criticidad del evento, <br> * **Then** transmite una notificación directa al dispositivo del jefe de soporte. <br><br> **Escenario 2: Registro en historial ante falla de entrega.** <br> * **Given** que el dispositivo de destino se encuentra fuera de cobertura de red, <br> * **When** el sistema intenta transmitir la notificación, <br> * **Then** almacena la alerta en la base de datos para su consulta posterior. |

| User Story ID | HU15 | Epic ID | EP04 |
| :--- | :--- | :--- | :--- |
| **Título** | Registro de mantenimiento preventivo |
| **Descripción** | Como técnico de campo, deseo registrar las intervenciones técnicas realizadas para mantener el historial del equipo actualizado. |
| **Criterios de Aceptación** | **Escenario 1: Creación de reporte de servicio.** <br> * **Given** que el técnico proporciona la descripción de la intervención realizada, <br> * **When** registra la actividad, <br> * **Then** el sistema anexa el reporte al ciclo de vida del equipo y programa la próxima revisión. <br><br> **Escenario 2: Prevención de reportes en blanco.** <br> * **Given** que el técnico intenta concluir la tarea sin justificar las acciones, <br> * **When** solicita el registro, <br> * **Then** el sistema paraliza la acción y requiere el detalle del servicio técnico. |

| User Story ID | HU16 | Epic ID | EP05 |
| :--- | :--- | :--- | :--- |
| **Título** | Seguimiento de garantías vendidas |
| **Descripción** | Como distribuidor, deseo verificar el tiempo restante de cobertura de un equipo para gestionar renovaciones de contrato. |
| **Criterios de Aceptación** | **Escenario 1: Verificación de póliza activa.** <br> * **Given** que el equipo posee un contrato en curso, <br> * **When** el distribuidor consulta los datos de cobertura, <br> * **Then** el sistema calcula y expone el periodo restante de validez. <br><br> **Escenario 2: Identificación de contrato caducado.** <br> * **Given** que la fecha actual supera el plazo límite del contrato, <br> * **When** se consultan los datos, <br> * **Then** el sistema clasifica y advierte que el estado de la cobertura es expirado. |

| User Story ID | HU17 | Epic ID | EP05 |
| :--- | :--- | :--- | :--- |
| **Título** | Certificado de venta en PDF |
| **Descripción** | Como vendedor, deseo generar un comprobante de venta en formato documento para remitirlo al cliente. |
| **Criterios de Aceptación** | **Escenario 1: Generación de documento legal.** <br> * **Given** que existe una transacción aprobada en el sistema, <br> * **When** el vendedor solicita la extracción del documento, <br> * **Then** el sistema compila la información y entrega un archivo exportable estructurado. <br><br> **Escenario 2: Intento de generación sin aprobación.** <br> * **Given** que la transacción se mantiene en estado pendiente, <br> * **When** el vendedor busca extraer el comprobante, <br> * **Then** el sistema restringe la descarga hasta la confirmación financiera. |

| User Story ID | HU18 | Epic ID | EP06 |
| :--- | :--- | :--- | :--- |
| **Título** | Asignación de técnicos a zonas |
| **Descripción** | Como gerente, deseo restringir la visibilidad de la flota asignando técnicos a delimitaciones geográficas específicas. |
| **Criterios de Aceptación** | **Escenario 1: Segmentación de acceso por territorio.** <br> * **Given** que el gerente asocia el perfil de un técnico a una delimitación geográfica, <br> * **When** el técnico solicita ver el listado de flota, <br> * **Then** el sistema filtra los datos devolviendo exclusivamente los activos de dicha región. <br><br> **Escenario 2: Advertencia por saturación operativa.** <br> * **Given** que el gerente excede la capacidad máxima de equipos por técnico, <br> * **When** confirma la asignación adicional, <br> * **Then** el sistema advierte sobre la sobrecarga de responsabilidad del operario. |

| User Story ID | HU19 | Epic ID | EP06 |
| :--- | :--- | :--- | :--- |
| **Título** | Contador de horas de uso (Horómetro) |
| **Descripción** | Como jefe de taller, deseo consultar el tiempo acumulado de trabajo del motor para programar cambios de insumos. |
| **Criterios de Aceptación** | **Escenario 1: Consulta de métricas acumulativas.** <br> * **Given** que la maquinaria transmite periódicamente sus ciclos de trabajo, <br> * **When** el jefe de taller verifica los datos del motor, <br> * **Then** el sistema presenta el total exacto del tiempo operado. <br><br> **Escenario 2: Protección contra alteración de datos.** <br> * **Given** que un usuario sin privilegios administrativos intenta modificar el valor, <br> * **When** ejecuta la acción de edición, <br> * **Then** el sistema rechaza la petición por falta de autorización. |

| User Story ID | HU20 | Epic ID | EP06 |
| :--- | :--- | :--- | :--- |
| **Título** | Ubicación GPS de maquinaria |
| **Descripción** | Como gestor de activos, deseo visualizar la ubicación geoespacial de mis máquinas para coordinar los viajes de mantenimiento. |
| **Criterios de Aceptación** | **Escenario 1: Posicionamiento geoespacial exitoso.** <br> * **Given** que el módulo satelital provee coordenadas precisas, <br> * **When** el gestor inicializa el módulo de geolocalización, <br> * **Then** el sistema ubica los activos sobre la representación cartográfica. <br><br> **Escenario 2: Falla de triangulación satelital.** <br> * **Given** que el equipo se encuentra en una zona sin cobertura, <br> * **When** el gestor inicializa la consulta, <br> * **Then** el sistema muestra la última posición conocida y marca el dato como no reciente. |

| User Story ID | HU21 | Epic ID | EP07 |
| :--- | :--- | :--- | :--- |
| **Título** | Registro de clientes mineros |
| **Descripción** | Como distribuidor, deseo almacenar la identidad corporativa de las empresas mineras para agilizar futuras transacciones. |
| **Criterios de Aceptación** | **Escenario 1: Almacenamiento de identidad corporativa.** <br> * **Given** que el distribuidor ingresa datos tributarios e identificación correctos, <br> * **When** ejecuta el guardado de la entidad, <br> * **Then** el sistema persiste la información habilitándola para nuevos contratos. <br><br> **Escenario 2: Validación de formato de identificación.** <br> * **Given** que el distribuidor ingresa un identificador tributario incompleto, <br> * **When** ejecuta el guardado, <br> * **Then** el sistema detecta la anomalía de longitud y exige la corrección. |

| User Story ID | HU22 | Epic ID | EP07 |
| :--- | :--- | :--- | :--- |
| **Título** | Comentarios técnicos por equipo |
| **Descripción** | Como mecánico de turno, deseo aportar observaciones técnicas en la bitácora del equipo para informar a futuros turnos. |
| **Criterios de Aceptación** | **Escenario 1: Trazabilidad de observaciones.** <br> * **Given** que el mecánico aporta información descriptiva sobre el estado físico, <br> * **When** asienta el registro en la bitácora del equipo, <br> * **Then** el sistema añade el apunte identificando al autor y la estampa de tiempo. <br><br> **Escenario 2: Protección de la bitácora.** <br> * **Given** que un mecánico intenta suprimir un apunte de otro colega, <br> * **When** ejecuta la orden de borrado, <br> * **Then** el sistema deniega el permiso garantizando la inmutabilidad del registro. |

| User Story ID | HU23 | Epic ID | EP08 |
| :--- | :--- | :--- | :--- |
| **Título** | Exportación de historial de sensores |
| **Descripción** | Como analista de datos, deseo extraer una matriz de datos históricos de sensores para elaborar informes gerenciales. |
| **Criterios de Aceptación** | **Escenario 1: Extracción de matriz de datos.** <br> * **Given** que el analista define un intervalo de tiempo con registros existentes, <br> * **When** solicita la exportación de información, <br> * **Then** el sistema compila la estructura de datos y entrega un archivo tabular descargable. <br><br> **Escenario 2: Solicitud de intervalos vacíos.** <br> * **Given** que el analista define un periodo de inactividad de la maquinaria, <br> * **When** solicita la exportación, <br> * **Then** el sistema notifica la carencia de lecturas y previene la descarga vacía. |

| User Story ID | HU24 | Epic ID | EP08 |
| :--- | :--- | :--- | :--- |
| **Título** | Gráficas comparativas de flota |
| **Descripción** | Como gerente, deseo contrastar el desempeño de múltiples equipos compatibles para evaluar su rendimiento operativo. |
| **Criterios de Aceptación** | **Escenario 1: Superposición de métricas.** <br> * **Given** que el gerente selecciona múltiples activos compatibles, <br> * **When** invoca la herramienta de evaluación comparativa, <br> * **Then** el sistema procesa ambas fuentes y unifica los resultados en una representación conjunta. <br><br> **Escenario 2: Incompatibilidad de fuentes de datos.** <br> * **Given** que el gerente intenta evaluar una máquina sin integración IoT, <br> * **When** invoca la herramienta, <br> * **Then** el sistema reporta la falta de telemetría e impide la comparativa. |

| User Story ID | HU25 | Epic ID | EP01 |
| :--- | :--- | :--- | :--- |
| **Título** | Cerrar sesión correctamente |
| **Descripción** | Como usuario de terminales compartidos, deseo finalizar voluntariamente mi sesión para proteger la integridad de los datos. |
| **Criterios de Aceptación** | **Escenario 1: Finalización voluntaria de acceso.** <br> * **Given** que el usuario finaliza sus operaciones de gestión, <br> * **When** ejecuta la acción de salida, <br> * **Then** el sistema destruye los permisos de sesión y exige nueva autenticación. <br><br> **Escenario 2: Control de concurrencia.** <br> * **Given** que la sesión pierde validez por inactividad prolongada, <br> * **When** un tercero intenta reanudar operaciones, <br> * **Then** el sistema detecta la expiración e impide el acceso al contenido restringido. |

| User Story ID | HU26 | Epic ID | EP02 |
| :--- | :--- | :--- | :--- |
| **Título** | Reporte de fallas por operario |
| **Descripción** | Como operario de maquinaria, deseo reportar averías mecánicas detectadas visualmente para solicitar su revisión técnica. |
| **Criterios de Aceptación** | **Escenario 1: Generación de ticket de soporte.** <br> * **Given** que el operario fundamenta la avería encontrada en el equipo, <br> * **When** envía la solicitud de revisión, <br> * **Then** el sistema cataloga la incidencia y alerta al personal asignado para su atención. <br><br> **Escenario 2: Rechazo de reportes inconsistentes.** <br> * **Given** que el operario intenta enviar un parte sin especificar el problema, <br> * **When** envía la solicitud, <br> * **Then** el sistema exige la justificación descriptiva antes de catalogar la falla. |

| User Story ID | HU27 | Epic ID | EP02 |
| :--- | :--- | :--- | :--- |
| **Título** | Búsqueda por modelo de motor |
| **Descripción** | Como técnico, deseo localizar maquinaria utilizando la nomenclatura específica de su motor para preparar las piezas de recambio. |
| **Criterios de Aceptación** | **Escenario 1: Identificación de componentes compartidos.** <br> * **Given** que el técnico proporciona la nomenclatura específica del motor, <br> * **When** procesa la consulta en el buscador, <br> * **Then** el sistema recupera todos los equipos que integran dicha pieza de hardware. <br><br> **Escenario 2: Consulta de nomenclatura inválida.** <br> * **Given** que el técnico provee una nomenclatura inexistente en los registros, <br> * **When** procesa la consulta, <br> * **Then** el sistema informa que ningún activo coincide con las especificaciones. |

| User Story ID | HU28 | Epic ID | EP03 |
| :--- | :--- | :--- | :--- |
| **Título** | Filtro por estado operativo |
| **Descripción** | Como gestor de flota, deseo segregar el inventario por estado de operatividad para planificar la carga de trabajo diaria. |
| **Criterios de Aceptación** | **Escenario 1: Segregación de flota inactiva.** <br> * **Given** que el gestor aplica la condición de búsqueda de equipos averiados, <br> * **When** ejecuta la instrucción, <br> * **Then** el sistema discrimina el inventario y expone únicamente las unidades indisponibles. <br><br> **Escenario 2: Notificación de operatividad total.** <br> * **Given** que la totalidad de la flota mantiene estado funcional, <br> * **When** el gestor filtra por unidades averiadas, <br> * **Then** el sistema confirma que no existen reportes de inactividad técnica. |

| User Story ID | HU29 | Epic ID | EP03 |
| :--- | :--- | :--- | :--- |
| **Título** | Alerta de nivel de combustible |
| **Descripción** | Como administrador, deseo recibir advertencias preventivas cuando las reservas de energía desciendan a niveles críticos. |
| **Criterios de Aceptación** | **Escenario 1: Prevención de desabastecimiento.** <br> * **Given** que el sensor volumétrico detecta un descenso a niveles mínimos, <br> * **When** transmite la métrica al sistema central, <br> * **Then** se activa un protocolo de advertencia sobre la autonomía restante del equipo. <br><br> **Escenario 2: Desactivación tras repostaje.** <br> * **Given** que los niveles de energía se restablecen tras el abastecimiento, <br> * **When** el sensor confirma el incremento volumétrico, <br> * **Then** el sistema suprime la advertencia de desabastecimiento. |

| User Story ID | HU30 | Epic ID | EP04 |
| :--- | :--- | :--- | :--- |
| **Título** | Gestión de proveedores de repuestos |
| **Descripción** | Como distribuidor, deseo incorporar información de entidades proveedoras para agilizar la logística de reposición. |
| **Criterios de Aceptación** | **Escenario 1: Inclusión en la red de suministros.** <br> * **Given** que el distribuidor ingresa información fidedigna de una nueva entidad comercial, <br> * **When** efectúa la acción de registro, <br> * **Then** el sistema asimila el contacto y lo enlaza a las marcas correspondientes. <br><br> **Escenario 2: Gestión de duplicidades logísticas.** <br> * **Given** que el distribuidor intenta ingresar una entidad previamente registrada, <br> * **When** efectúa el registro, <br> * **Then** el sistema frena la acción y proporciona acceso al perfil ya existente. |

| User Story ID | HU31 | Epic ID | EP04 |
| :--- | :--- | :--- | :--- |
| **Título** | Notificación de vencimiento de seguro |
| **Descripción** | Como gestor, deseo recibir notificaciones cronológicas preventivas antes de la expiración de las pólizas de seguro. |
| **Criterios de Aceptación** | **Escenario 1: Ejecución de tarea programada.** <br> * **Given** que el sistema evalúa diariamente las fechas contractuales, <br> * **When** la brecha de tiempo alcanza el límite de prevención establecido, <br> * **Then** expide una alerta administrativa para iniciar los procesos de renovación. <br><br> **Escenario 2: Verificación de contrato vencido.** <br> * **Given** que la cobertura carece de renovación tras su fecha límite, <br> * **When** el gestor revisa el perfil del activo, <br> * **Then** el sistema destaca de forma crítica el estado irregular de la documentación. |

| User Story ID | HU32 | Epic ID | EP05 |
| :--- | :--- | :--- | :--- |
| **Título** | Visualización de manuales digitales |
| **Descripción** | Como técnico en campo, deseo acceder a la documentación técnica del fabricante para consultar procedimientos de reparación. |
| **Criterios de Aceptación** | **Escenario 1: Acceso a documentación técnica.** <br> * **Given** que la maquinaria posee esquemas vinculados a su ficha, <br> * **When** el técnico requiere apoyo documental, <br> * **Then** el sistema facilita la lectura del archivo a través de un visor integrado. <br><br> **Escenario 2: Notificación de ausencia de guías.** <br> * **Given** que no existen archivos subidos por el proveedor para el modelo actual, <br> * **When** el técnico requiere la información, <br> * **Then** el sistema ofrece un medio para reportar y solicitar la carga de la documentación. |

| User Story ID | HU33 | Epic ID | EP05 |
| :--- | :--- | :--- | :--- |
| **Título** | Registro de piezas reemplazadas |
| **Descripción** | Como técnico, deseo registrar los insumos específicos reemplazados en una máquina para mantener la trazabilidad del inventario. |
| **Criterios de Aceptación** | **Escenario 1: Sustracción de existencias en almacén.** <br> * **Given** que el técnico documenta la utilización de insumos durante una reparación, <br> * **When** finaliza la orden de trabajo, <br> * **Then** el sistema afecta el balance del inventario global y liga las piezas al equipo intervenido. <br><br> **Escenario 2: Manejo de insumos no catalogados.** <br> * **Given** que el técnico emplea materiales externos no previstos en el sistema, <br> * **When** especifica su uso de forma manual, <br> * **Then** el sistema añade la observación sin intentar deducir stock inexistente. |

| User Story ID | HU34 | Epic ID | EP03 |
| :--- | :--- | :--- | :--- |
| **Título** | Dashboard de eficiencia de combustible |
| **Descripción** | Como analista, deseo evaluar la tasa promedio de consumo energético por hora para identificar equipos ineficientes. |
| **Criterios de Aceptación** | **Escenario 1: Procesamiento analítico de consumo.** <br> * **Given** que la plataforma recibe constantemente mediciones volumétricas y tiempos de uso, <br> * **When** el analista solicita el índice de desempeño, <br> * **Then** el sistema ejecuta el cálculo y entrega la tasa promedio de consumo horario. <br><br> **Escenario 2: Omisión por inconsistencia de datos.** <br> * **Given** que la telemetría proporciona lecturas alteradas o carentes de sentido lógico, <br> * **When** el analista solicita el cálculo, <br> * **Then** el sistema suspende la operación e indica que la información base no es confiable. |

| User Story ID | HU35 | Epic ID | EP05 |
| :--- | :--- | :--- | :--- |
| **Título** | Historial de ubicaciones GPS |
| **Descripción** | Como jefe de logística, deseo trazar la ruta de desplazamiento de la maquinaria durante el último ciclo diario. |
| **Criterios de Aceptación** | **Escenario 1: Trazado de ruta de desplazamiento.** <br> * **Given** que el sistema almacena de forma secuencial las coordenadas del activo, <br> * **When** el jefe evalúa el lapso diario, <br> * **Then** el sistema grafica las posiciones cronológicas evidenciando la trayectoria. <br><br> **Escenario 2: Detección de estatismo prolongado.** <br> * **Given** que la maquinaria no presenta variaciones en sus coordenadas durante el ciclo, <br> * **When** el jefe evalúa la ruta, <br> * **Then** el sistema consolida un único punto e informa sobre la ausencia de traslado. |

| User Story ID | HU36 | Epic ID | EP06 |
| :--- | :--- | :--- | :--- |
| **Título** | Cambio de unidades de medida |
| **Descripción** | Como usuario, deseo alternar entre diferentes sistemas métricos para consultar las variables térmicas en mi formato de preferencia. |
| **Criterios de Aceptación** | **Escenario 1: Transformación algorítmica de valores.** <br> * **Given** que el usuario modifica los parámetros de localización, <br> * **When** se aplican las nuevas directrices, <br> * **Then** el sistema recalcula inmediatamente las métricas presentadas sin alterar los datos base. <br><br> **Escenario 2: Persistencia de configuración personalizada.** <br> * **Given** que el usuario finaliza su sesión operativa con ajustes específicos, <br> * **When** inicia un nuevo ciclo de trabajo, <br> * **Then** el sistema respeta y restablece sus preferencias métricas previamente definidas. |

| User Story ID | HU37 | Epic ID | EP06 |
| :--- | :--- | :--- | :--- |
| **Título** | Modo oscuro para trabajo nocturno |
| **Descripción** | Como operador nocturno, deseo aplicar un esquema visual adaptativo para reducir la fatiga visual en entornos de baja luminosidad. |
| **Criterios de Aceptación** | **Escenario 1: Transición de esquema de lectura.** <br> * **Given** que el operador interacciona con los ajustes de ergonomía visual, <br> * **When** activa la modalidad nocturna, <br> * **Then** el sistema ajusta dinámicamente los contrastes y luminosidad de la información. <br><br> **Escenario 2: Ajuste por detección de entorno.** <br> * **Given** que el dispositivo cliente percibe cambios drásticos en la iluminación ambiental, <br> * **When** transcurre un lapso diurno, <br> * **Then** el sistema ofrece retornar a la configuración estándar de lectura clara. |

| User Story ID | HU38 | Epic ID | EP06 |
| :--- | :--- | :--- | :--- |
| **Título** | Suscripción a alertas específicas |
| **Descripción** | Como técnico jefe, deseo suscribirme selectivamente a categorías de alertas específicas para focalizar mi atención operativa. |
| **Criterios de Aceptación** | **Escenario 1: Segmentación de flujo de avisos.** <br> * **Given** que el técnico selecciona exclusiones dentro de las categorías de monitoreo, <br> * **When** se materializa un evento ajeno a sus preferencias, <br> * **Then** el sistema bloquea el envío hacia su perfil y mantiene el registro general. <br><br> **Escenario 2: Despliegue de eventos prioritarios.** <br> * **Given** que ocurre un suceso categorizado dentro de las selecciones del técnico, <br> * **When** se materializa el evento, <br> * **Then** el sistema emite inmediatamente la comunicación hacia el perfil suscrito. |

| User Story ID | HU39 | Epic ID | EP01 |
| :--- | :--- | :--- | :--- |
| **Título** | Auditoría de cambios en inventario |
| **Descripción** | Como administrador, deseo consultar el registro inmutable de alteraciones en el inventario para auditar los cambios comerciales. |
| **Criterios de Aceptación** | **Escenario 1: Registro histórico de manipulaciones.** <br> * **Given** que un miembro del personal altera las características o estados de un equipo, <br> * **When** el sistema confirma la orden, <br> * **Then** genera una traza de auditoría adjuntando identidad, acción y referencias temporales. <br><br> **Escenario 2: Revisión de expedientes sin modificaciones.** <br> * **Given** que un activo se mantiene inalterado desde su concepción, <br> * **When** el administrador consulta su expediente de cambios, <br> * **Then** el sistema atestigua la ausencia de manipulaciones documentadas. |

| User Story ID | HU40 | Epic ID | EP06 |
| :--- | :--- | :--- | :--- |
| **Título** | Vista simplificada para operarios |
| **Descripción** | Como operario de cabina, deseo una interfaz de visualización simplificada para enfocarme en los indicadores críticos durante la operación. |
| **Criterios de Aceptación** | **Escenario 1: Despliegue de modo focalizado.** <br> * **Given** que el usuario requiere concentrarse en datos primarios, <br> * **When** solicita la reducción de complejidad informativa, <br> * **Then** el sistema suprime los datos periféricos y prioriza la legibilidad de la telemetría base. <br><br> **Escenario 2: Retorno a panel exhaustivo.** <br> * **Given** que el usuario precisa acceder a métricas detalladas, <br> * **When** desactiva la modalidad focalizada, <br> * **Then** el sistema restituye la totalidad de los componentes de análisis. |

| User Story ID | HU41 | Epic ID | EP04 |
| :--- | :--- | :--- | :--- |
| **Título** | Registro de kilometraje |
| **Descripción** | Como gestor de transporte, deseo registrar el recorrido acumulado de los camiones para automatizar las alertas de mantenimiento. |
| **Criterios de Aceptación** | **Escenario 1: Activación de ciclo de desgaste.** <br> * **Given** que el gestor ingresa la actualización de recorrido acumulado, <br> * **When** la suma atraviesa la cuota límite establecida para los neumáticos, <br> * **Then** el sistema programa un requerimiento técnico automático. <br><br> **Escenario 2: Evaluación de consistencia numérica.** <br> * **Given** que se ingresa un valor de odómetro inferior al registro previo, <br> * **When** se intenta validar el dato, <br> * **Then** el sistema intercepta el error lógico y demanda confirmación humana. |

| User Story ID | HU42 | Epic ID | EP03 |
| :--- | :--- | :--- | :--- |
| **Título** | Alerta de batería de dispositivo IoT |
| **Descripción** | Como técnico de sistemas, deseo monitorear las reservas de energía del hardware remoto para prevenir la pérdida de conectividad. |
| **Criterios de Aceptación** | **Escenario 1: Monitoreo de alimentación energética.** <br> * **Given** que el hardware remoto cuantifica un desgaste severo de sus reservas, <br> * **When** transfiere la señal de estado, <br> * **Then** el sistema notifica el riesgo inminente de apagón funcional del nodo. <br><br> **Escenario 2: Cese de contingencia energética.** <br> * **Given** que el equipo técnico efectúa el recambio de la unidad de poder, <br> * **When** el hardware transfiere la recuperación de su capacidad, <br> * **Then** el sistema revoca el estado de riesgo. |

| User Story ID | HU43 | Epic ID | EP03 |
| :--- | :--- | :--- | :--- |
| **Título** | Evaluación de desempeño (KPIs) |
| **Descripción** | Como gerente, deseo consultar un índice de salud algorítmico para cada máquina con el fin de identificar las unidades más confiables. |
| **Criterios de Aceptación** | **Escenario 1: Procesamiento de índice de confiabilidad.** <br> * **Given** que el sistema dispone de un histórico rico en comportamientos del activo, <br> * **When** el gerente requiere la síntesis de rendimiento, <br> * **Then** el sistema ejecuta fórmulas matemáticas para arrojar un veredicto de salud. <br><br> **Escenario 2: Calificación punitiva por siniestros.** <br> * **Given** que la unidad registra múltiples caídas de servicio recientes, <br> * **When** se efectúa el cálculo, <br> * **Then** el sistema castiga el puntaje clasificando el activo como riesgo inminente. |

| User Story ID | HU44 | Epic ID | EP06 |
| :--- | :--- | :--- | :--- |
| **Título** | Comunicación interna para equipo técnico |
| **Descripción** | Como técnico, deseo emitir comunicaciones directas desde la ficha del equipo para coordinar intervenciones con otros operarios. |
| **Criterios de Aceptación** | **Escenario 1: Distribución simultánea de mensajes.** <br> * **Given** que el técnico emite un dictamen en el espacio colaborativo, <br> * **When** confirma su difusión, <br> * **Then** el sistema enruta la comunicación hacia los receptores correspondientes sin demora. <br><br> **Escenario 2: Trazabilidad de soporte audiovisual.** <br> * **Given** que el técnico incorpora material fotográfico para justificar una reparación, <br> * **When** transmite la información, <br> * **Then** el sistema preserva el recurso vinculándolo permanentemente a la incidencia tratada. |

| User Story ID | HU45 | Epic ID | EP04 |
| :--- | :--- | :--- | :--- |
| **Título** | Consolidación de facturas de mantenimiento |
| **Descripción** | Como contador, deseo adjuntar comprobantes certificados de gastos para consolidar el pasivo financiero de cada máquina. |
| **Criterios de Aceptación** | **Escenario 1: Asociación de costos al expediente.** <br> * **Given** que el contador aporta un comprobante de egresos certificado, <br> * **When** lo vincula a una orden de soporte finalizada, <br> * **Then** el sistema anexa el pasivo a las métricas financieras del activo implicado. <br><br> **Escenario 2: Protección contra montos atípicos.** <br> * **Given** que el importe declarado sobrepasa los estándares habituales de operación, <br> * **When** se intenta formalizar el gasto, <br> * **Then** el sistema requiere una autenticación jerárquica para permitir la anomalía. |

| User Story ID | HU46 | Epic ID | EP03 |
| :--- | :--- | :--- | :--- |
| **Título** | Mapeo de densidad de sobrecalentamiento |
| **Descripción** | Como jefe de operaciones, deseo identificar las zonas geográficas donde las máquinas sufren mayor estrés térmico. |
| **Criterios de Aceptación** | **Escenario 1: Renderizado espacial de anomalías.** <br> * **Given** que el sistema recopila variables de posición y exceso de temperatura, <br> * **When** el jefe solicita la evaluación territorial, <br> * **Then** el sistema proyecta áreas de concentración evidenciando las zonas de conflicto. <br><br> **Escenario 2: Despliegue en condiciones estables.** <br> * **Given** que ninguna maquinaria infringe sus rangos térmicos seguros, <br> * **When** se solicita la evaluación territorial, <br> * **Then** el sistema certifica la ausencia de zonas críticas en el sector minero. |

| User Story ID | HU47 | Epic ID | EP01 |
| :--- | :--- | :--- | :--- |
| **Título** | Sincronización de perfiles empresariales |
| **Descripción** | Como administrador, deseo sincronizar la identidad visual de mi organización para unificar el formato de los documentos emitidos. |
| **Criterios de Aceptación** | **Escenario 1: Actualización de identidad visual.** <br> * **Given** que el administrador provee recursos gráficos corporativos actualizados, <br> * **When** se aprueba la modificación, <br> * **Then** el sistema propaga la nueva imagen a las matrices de exportación documental. <br><br> **Escenario 2: Rechazo de parámetros tributarios ilegales.** <br> * **Given** que se intenta establecer un identificador empresarial de formato inválido, <br> * **When** se procesa la modificación, <br> * **Then** el sistema aborta el cambio protegiendo la legalidad de los reportes. |

| User Story ID | HU48 | Epic ID | EP04 |
| :--- | :--- | :--- | :--- |
| **Título** | Validación de protocolos de seguridad |
| **Descripción** | Como oficial de seguridad, deseo forzar la confirmación de medidas de protección antes de permitir el cierre de una intervención técnica. |
| **Criterios de Aceptación** | **Escenario 1: Bloqueo de avance por negligencia.** <br> * **Given** que el operario técnico evade declarar el uso de protecciones obligatorias, <br> * **When** busca concluir la certificación del soporte, <br> * **Then** el sistema trunca el cierre y exige la confirmación de los protocolos. <br><br> **Escenario 2: Habilitación por cumplimiento de norma.** <br> * **Given** que se constata la totalidad de las medidas de riesgo establecidas, <br> * **When** el operario busca concluir el soporte, <br> * **Then** el sistema valida la responsabilidad y permite archivar la gestión. |

| User Story ID | HU49 | Epic ID | EP09 |
| :--- | :--- | :--- | :--- |
| **Título** | Suministro de esquemas eléctricos |
| **Descripción** | Como Developer, deseo implementar un endpoint GET para servir los recursos de planimetría en alta resolución a los clientes móviles. |
| **Criterios de Aceptación** | **Escenario 1: Entrega de recurso válido.** <br> * **Given** que la petición solicita un identificador de recurso existente, <br> * **When** la interfaz de programación atiende la solicitud, <br> * **Then** despacha el archivo estructurado confirmando la operación mediante un estado de éxito. <br><br> **Escenario 2: Petición de recursos inexistentes.** <br> * **Given** que la petición exige un esquema técnico no catalogado, <br> * **When** la interfaz atiende la solicitud, <br> * **Then** reporta la indisponibilidad del activo mediante un estado de error de hallazgo. |

| User Story ID | HU50 | Epic ID | EP09 |
| :--- | :--- | :--- | :--- |
| **Título** | Automatización de resguardos de datos |
| **Descripción** | Como Developer, deseo configurar un procedimiento programado para extraer y asegurar el resguardo de la base de datos principal. |
| **Criterios de Aceptación** | **Escenario 1: Ejecución del respaldo periódico.** <br> * **Given** que se alcanza el intervalo cronológico predefinido en las políticas de seguridad, <br> * **When** el motor de tareas inicia la rutina, <br> * **Then** el sistema empaqueta la información y la traslada a un repositorio de alta disponibilidad. <br><br> **Escenario 2: Notificación ante fallo de almacenamiento.** <br> * **Given** que el proceso encuentra un impedimento en la asignación de espacio, <br> * **When** intenta concluir la tarea, <br> * **Then** detiene la ejecución y escala una alerta de nivel crítico hacia el equipo de infraestructura. |

## 3.2. Impact Mapping

<img width="1240" height="2079" alt="Impact map 1" src="https://github.com/user-attachments/assets/294b74ff-49ef-455b-a684-7191b382f870" />


## 3.3. Product Backlog

A continuación se presenta el Product Backlog priorizado del proyecto MineTrack. 

| # Orden | User Story ID | Descripción (Como [Rol], deseo [Funcionalidad], para [Beneficio]) | Story Points |
| :--- | :--- | :--- | :--- |
| 1 | HU01 | Como visitante, deseo visualizar el propósito de la plataforma para comprender cómo MineTrack optimiza la gestión minera. | 3 |
| 2 | HU02 | Como visitante interesado, deseo registrar mis datos de contacto para solicitar información comercial personalizada. | 3 |
| 3 | HU07 | Como visitante del catálogo, deseo filtrar la maquinaria por categoría para localizar activos de mi interés. | 5 |
| 4 | HU08 | Como visitante interesado, deseo enviar una solicitud formal por un equipo para iniciar el proceso de negociación comercial. | 3 |
| 5 | HU09 | Como técnico, deseo supervisar el estado de los sensores IoT para controlar la salud de la maquinaria sin estar presente. | 8 |
| 6 | HU10 | Como jefe de mantenimiento, deseo vigilar la temperatura del motor para prevenir daños por sobrecalentamiento. | 5 |
| 7 | HU12 | Como operador, deseo verificar la presión del sistema hidráulico para asegurar la fuerza operativa del equipo. | 5 |
| 8 | HU14 | Como jefe de soporte, deseo recibir alertas inmediatas en mi dispositivo móvil cuando una máquina se detiene por emergencia. | 5 |
| 9 | HU05 | Como distribuidor, deseo registrar los datos técnicos de maquinaria nueva para incluirla en el inventario de ventas. | 5 |
| 10 | HU03 | Como usuario de MineTrack, deseo ingresar al sistema con mis credenciales para acceder a las funciones de mi perfil. | 3 |
| 11 | HU04 | Como usuario, deseo restablecer mi contraseña para recuperar el acceso ante la pérdida de mis datos de ingreso. | 3 |
| 12 | HU11 | Como técnico, deseo medir la vibración de la maquinaria para detectar piezas sueltas o desgaste mecánico. | 5 |
| 13 | HU13 | Como administrador técnico, deseo definir los rangos de peligro para cada sensor para recibir notificaciones solo ante emergencias. | 3 |
| 14 | HU20 | Como gestor de activos, deseo visualizar la ubicación geoespacial de mis máquinas para coordinar los viajes de mantenimiento. | 5 |
| 15 | HU16 | Como distribuidor, deseo verificar el tiempo restante de cobertura de un equipo para gestionar renovaciones de contrato. | 3 |
| 16 | HU15 | Como técnico de campo, deseo registrar las intervenciones técnicas realizadas para mantener el historial del equipo actualizado. | 3 |
| 17 | HU06 | Como distribuidor, deseo adjuntar representaciones visuales de la maquinaria para evidenciar el estado físico del activo. | 5 |
| 18 | HU17 | Como vendedor, deseo generar un comprobante de venta en formato documento para remitirlo al cliente. | 5 |
| 19 | HU24 | Como gerente, deseo contrastar el desempeño de múltiples equipos compatibles para evaluar su rendimiento operativo. | 8 |
| 20 | HU43 | Como gerente, deseo consultar un índice de salud algorítmico para cada máquina con el fin de identificar las unidades más confiables. | 8 |
| 21 | HU46 | Como jefe de operaciones, deseo identificar las zonas geográficas donde las máquinas sufren mayor estrés térmico. | 8 |
| 22 | HU19 | Como jefe de taller, deseo consultar el tiempo acumulado de trabajo del motor para programar cambios de insumos. | 2 |
| 23 | HU23 | Como analista de datos, deseo extraer una matriz de datos históricos de sensores para elaborar informes gerenciales. | 5 |
| 24 | HU26 | Como operario de maquinaria, deseo reportar averías mecánicas detectadas visualmente para solicitar su revisión técnica. | 3 |
| 25 | HU29 | Como administrador, deseo recibir advertencias preventivas cuando las reservas de energía desciendan a niveles críticos. | 5 |
| 26 | HU32 | Como técnico en campo, deseo acceder a la documentación técnica del fabricante para consultar procedimientos de reparación. | 5 |
| 27 | HU33 | Como técnico, deseo registrar los insumos específicos reemplazados en una máquina para mantener la trazabilidad del inventario. | 3 |
| 28 | HU40 | Como operario de cabina, deseo una interfaz de visualización simplificada para enfocarme en los indicadores críticos durante la operación. | 5 |
| 29 | HU42 | Como técnico de sistemas, deseo monitorear las reservas de energía del hardware remoto para prevenir la pérdida de conectividad. | 3 |
| 30 | HU21 | Como distribuidor, deseo almacenar la identidad corporativa de las empresas mineras para agilizar futuras transacciones. | 2 |
| 31 | HU22 | Como mecánico de turno, deseo aportar observaciones técnicas en la bitácora del equipo para informar a futuros turnos. | 2 |
| 32 | HU27 | Como técnico, deseo localizar maquinaria utilizando la nomenclatura específica de su motor para preparar las piezas de recambio. | 2 |
| 33 | HU28 | Como gestor de flota, deseo segregar el inventario por estado de operatividad para planificar la carga de trabajo diaria. | 3 |
| 34 | HU30 | Como distribuidor, deseo incorporar información de entidades proveedoras para agilizar la logística de reposición. | 3 |
| 35 | HU31 | Como gestor, deseo recibir notificaciones cronológicas preventivas antes de la expiración de las pólizas de seguro. | 2 |
| 36 | HU34 | Como analista, deseo evaluar la tasa promedio de consumo energético por hora para identificar equipos ineficientes. | 5 |
| 37 | HU35 | Como jefe de logística, deseo trazar la ruta de desplazamiento de la maquinaria durante el último ciclo diario. | 5 |
| 38 | HU38 | Como técnico jefe, deseo suscribirme selectivamente a categorías de alertas específicas para focalizar mi atención operativa. | 3 |
| 39 | HU39 | Como administrador, deseo consultar el registro inmutable de alteraciones en el inventario para auditar los cambios comerciales. | 5 |
| 40 | HU41 | Como gestor de transporte, deseo registrar el recorrido acumulado de los camiones para automatizar las alertas de mantenimiento. | 3 |
| 41 | HU44 | Como técnico, deseo emitir comunicaciones directas desde la ficha del equipo para coordinar intervenciones con otros operarios. | 5 |
| 42 | HU45 | Como contador, deseo adjuntar comprobantes certificados de gastos para consolidar el pasivo financiero de cada máquina. | 5 |
| 43 | HU48 | Como oficial de seguridad, deseo forzar la confirmación de medidas de protección antes de permitir el cierre de una intervención técnica. | 3 |
| 44 | HU18 | Como gerente, deseo restringir la visibilidad de la flota asignando técnicos a delimitaciones geográficas específicas. | 3 |
| 45 | HU25 | Como usuario de terminales compartidos, deseo finalizar voluntariamente mi sesión para proteger la integridad de los datos. | 1 |
| 46 | HU36 | Como usuario, deseo alternar entre diferentes sistemas métricos para consultar las variables térmicas en mi formato de preferencia. | 2 |
| 47 | HU37 | Como operador nocturno, deseo aplicar un esquema visual adaptativo para reducir la fatiga visual en entornos de baja luminosidad. | 3 |
| 48 | HU47 | Como administrador, deseo sincronizar la identidad visual de mi organización para unificar el formato de los documentos emitidos. | 2 |
| 49 | HU49 | Como Developer, deseo implementar un endpoint GET para servir los recursos de planimetría en alta resolución a los clientes móviles. | 5 |
| 50 | HU50 | Como Developer, deseo configurar un procedimiento programado para extraer y asegurar el resguardo de la base de datos principal. | 5 |
