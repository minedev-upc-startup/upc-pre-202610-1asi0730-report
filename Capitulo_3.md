# Capítulo III: Requirements Specification

## 3.1. User Stories

| User Story ID | HU01 | Epic ID | EP01 |
| :--- | :--- | :--- | :--- |
| **Título** | Inicio de sesión seguro |
| **Descripción** | Como usuario de MineTrack, deseo ingresar a la plataforma con mi correo y contraseña para acceder a las funciones según mi rol asignado. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que ingreso credenciales válidas, <br> *When* hago clic en "Ingresar", <br> *Then* el sistema me redirige al dashboard principal. <br><br> **Escenario 2:** <br> *Given* que ingreso una contraseña errónea, <br> *When* intento acceder, <br> *Then* el sistema muestra un mensaje de "Credenciales incorrectas". |

| User Story ID | HU02 | Epic ID | EP01 |
| :--- | :--- | :--- | :--- |
| **Título** | Recuperación de cuenta |
| **Descripción** | Como usuario, deseo restablecer mi contraseña mediante mi correo electrónico para no perder el acceso a la gestión de mis máquinas. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que ingreso mi correo registrado, <br> *When* solicito el cambio, <br> *Then* recibo un enlace temporal para crear una nueva clave. <br><br> **Escenario 2:** <br> *Given* que ingreso un correo inexistente, <br> *When* envío la solicitud, <br> *Then* el sistema indica que el usuario no está registrado. |

| User Story ID | HU03 | Epic ID | EP01 |
| :--- | :--- | :--- | :--- |
| **Título** | Registro de nuevos integrantes del equipo |
| **Descripción** | Como administrador del grupo Brainstorm, deseo registrar a mis compañeros para que colaboren en el desarrollo del proyecto. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que ingreso los datos del nuevo miembro, <br> *When* guardo el registro, <br> *Then* se genera un nuevo usuario en la base de datos. <br><br> **Escenario 2:** <br> *Given* que el código de usuario ya existe, <br> *When* intento registrarlo, <br> *Then* el sistema me avisa que el integrante ya fue añadido. |

| User Story ID | HU04 | Epic ID | EP02 |
| :--- | :--- | :--- | :--- |
| **Título** | Registro de maquinaria nueva |
| **Descripción** | Como distribuidor, deseo subir los datos de una nueva máquina al sistema para ponerla en el catálogo de venta. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que lleno el formulario técnico, <br> *When* guardo los cambios, <br> *Then* la máquina aparece listada en el inventario disponible. <br><br> **Escenario 2:** <br> *Given* que faltan campos obligatorios como el modelo, <br> *When* intento guardar, <br> *Then* el sistema marca el error en rojo y no guarda nada. |

| User Story ID | HU05 | Epic ID | EP02 |
| :--- | :--- | :--- | :--- |
| **Título** | Subida de fotos de equipos |
| **Descripción** | Como distribuidor, deseo añadir imágenes reales de la maquinaria para que los compradores vean el estado físico del activo. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que selecciono archivos JPG o PNG, <br> *When* subo las fotos, <br> *Then* se visualizan correctamente en la galería del equipo. <br><br> **Escenario 2:** <br> *Given* que el archivo pesa más de 5MB, <br> *When* intento subirlo, <br> *Then* el sistema indica que el archivo es demasiado pesado. |

| User Story ID | HU06 | Epic ID | EP02 |
| :--- | :--- | :--- | :--- |
| **Título** | Edición de precios de catálogo |
| **Descripción** | Como distribuidor, deseo actualizar el precio de venta de las máquinas para ajustarme a las variaciones del mercado minero. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que ingreso un nuevo monto numérico, <br> *When* actualizo la ficha técnica, <br> *Then* el precio se refleja inmediatamente en la vista pública. <br><br> **Escenario 2:** <br> *Given* que ingreso un valor negativo o cero, <br> *When* intento guardar, <br> *Then* la app me obliga a poner un precio válido mayor a cero. |

| User Story ID | HU07 | Epic ID | EP02 |
| :--- | :--- | :--- | :--- |
| **Título** | Búsqueda por filtros |
| **Descripción** | Como cliente, deseo filtrar por tipo de máquina (excavadora, tractor, etc.) para encontrar rápido lo que necesito comprar. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que selecciono una categoría, <br> *When* aplico el filtro, <br> *Then* solo veo las máquinas de esa categoría. <br><br> **Escenario 2:** <br> *Given* que no hay stock de lo filtrado, <br> *When* realizo la búsqueda, <br> *Then* veo un mensaje indicando que no hay resultados disponibles. |

| User Story ID | HU08 | Epic ID | EP02 |
| :--- | :--- | :--- | :--- |
| **Título** | Generación de solicitud de compra |
| **Descripción** | Como cliente minero, deseo enviar una solicitud formal por un equipo para iniciar el proceso de negociación. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que hago clic en "Solicitar Cotización", <br> *When* confirmo el envío, <br> *Then* el distribuidor recibe una notificación con mis datos de contacto. <br><br> **Escenario 2:** <br> *Given* que el equipo ya fue vendido, <br> *When* intento solicitarlo, <br> *Then* el botón aparece deshabilitado. |

| User Story ID | HU09 | Epic ID | EP03 |
| :--- | :--- | :--- | :--- |
| **Título** | Dashboard de monitoreo IoT |
| **Descripción** | Como técnico, deseo ver un panel con los datos de los sensores en vivo para supervisar la flota sin estar presente. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que los sensores están conectados, <br> *When* entro al panel técnico, <br> *Then* veo las gráficas de temperatura y presión moviéndose en tiempo real. <br><br> **Escenario 2:** <br> *Given* que la máquina está apagada, <br> *When* reviso el dashboard, <br> *Then* los indicadores muestran valores en cero. |

| User Story ID | HU10 | Epic ID | EP03 |
| :--- | :--- | :--- | :--- |
| **Título** | Monitoreo de temperatura de motor |
| **Descripción** | Como jefe de mantenimiento, deseo vigilar que la temperatura no pase los límites seguros para evitar que el motor se funda. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que la temperatura sube a 95°C, <br> *When* el sensor envía el dato, <br> *Then* el indicador en pantalla cambia a color rojo. <br><br> **Escenario 2:** <br> *Given* que la temperatura es normal, <br> *When* observo el monitor, <br> *Then* el indicador se mantiene en color verde. |

| User Story ID | HU11 | Epic ID | EP03 |
| :--- | :--- | :--- | :--- |
| **Título** | Control de vibración mecánica |
| **Descripción** | Como técnico, deseo medir la vibración de la maquinaria para detectar piezas sueltas o desgaste excesivo de rodajes. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que accedo al historial de vibración, <br> *When* reviso la gráfica, <br> *Then* puedo identificar picos de anomalía en fechas específicas. <br><br> **Escenario 2:** <br> *Given* que no hay datos de sensores, <br> *When* intento ver la gráfica, <br> *Then* el sistema muestra "Sin conexión de sensor". |

| User Story ID | HU12 | Epic ID | EP03 |
| :--- | :--- | :--- | :--- |
| **Título** | Medición de presión hidráulica |
| **Descripción** | Como operador, deseo conocer la presión del sistema hidráulico para asegurar que el brazo de la máquina tenga la fuerza correcta. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que la máquina está trabajando, <br> *When* el valor baja de 2000 PSI, <br> *Then* el sistema genera una alerta visual de baja presión. <br><br> **Escenario 2:** <br> *Given* que la presión es estable, <br> *When* consulto la app, <br> *Then* visualizo el valor exacto en el medidor digital. |

| User Story ID | HU13 | Epic ID | EP04 |
| :--- | :--- | :--- | :--- |
| **Título** | Configuración de alertas críticas |
| **Descripción** | Como administrador técnico, deseo definir los rangos de peligro para cada sensor para que la app me avise solo cuando sea urgente. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que establezco el límite de calor en 100°C, <br> *When* el sistema guarda el cambio, <br> *Then* las alertas se dispararán solo al llegar a ese número. <br><br> **Escenario 2:** <br> *Given* que intento poner un límite absurdo, <br> *When* guardo la configuración, <br> *Then* el sistema pide una validación de seguridad. |

| User Story ID | HU14 | Epic ID | EP04 |
| :--- | :--- | :--- | :--- |
| **Título** | Notificaciones Push de emergencia |
| **Descripción** | Como jefe de soporte, deseo recibir alertas en mi celular cuando una máquina se detenga por falla para enviar ayuda rápido. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que ocurre una parada de emergencia, <br> *When* el sistema lo detecta, <br> *Then* me llega una notificación inmediata con el código de la máquina. <br><br> **Escenario 2:** <br> *Given* que tengo las notificaciones desactivadas, <br> *When* ocurre la falla, <br> *Then* la alerta se guarda únicamente en el registro interno de la app. |

| User Story ID | HU15 | Epic ID | EP04 |
| :--- | :--- | :--- | :--- |
| **Título** | Registro de mantenimiento preventivo |
| **Descripción** | Como técnico de campo, deseo anotar qué reparaciones le hice a una máquina para que el historial esté al día. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que termino un cambio de aceite, <br> *When* lleno el formulario de registro, <br> *Then* la fecha de la próxima revisión se actualiza automáticamente. <br><br> **Escenario 2:** <br> *Given* que intento registrar un mantenimiento sin descripción, <br> *When* guardo, <br> *Then* el sistema me pide detallar qué piezas se cambiaron. |

| User Story ID | HU16 | Epic ID | EP05 |
| :--- | :--- | :--- | :--- |
| **Título** | Seguimiento de garantías vendidas |
| **Descripción** | Como distribuidor, deseo ver cuánto tiempo de garantía le queda a cada máquina vendida para avisar al cliente sobre renovaciones. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que busco una máquina por su serie, <br> *When* reviso su ficha, <br> *Then* veo los meses restantes de cobertura técnica. <br><br> **Escenario 2:** <br> *Given* que la garantía ya expiró, <br> *When* cargo los datos, <br> *Then* el sistema muestra una etiqueta roja de "Expirado". |

| User Story ID | HU17 | Epic ID | EP05 |
| :--- | :--- | :--- | :--- |
| **Título** | Certificado de venta en PDF |
| **Descripción** | Como vendedor, deseo descargar un comprobante de la venta en PDF para enviárselo al cliente por correo. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que la venta fue aprobada, <br> *When* presiono "Generar PDF", <br> *Then* se descarga un documento con todos los datos técnicos y legales. <br><br> **Escenario 2:** <br> *Given* que la venta aún está pendiente, <br> *When* busco el botón de descarga, <br> *Then* este aparece bloqueado. |

| User Story ID | HU18 | Epic ID | EP06 |
| :--- | :--- | :--- | :--- |
| **Título** | Asignación de técnicos a zonas |
| **Descripción** | Como gerente, deseo asignar técnicos a zonas mineras específicas para que solo vean las máquinas bajo su responsabilidad. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que elijo un técnico y una zona, <br> *When* vinculo ambos datos, <br> *Then* el dashboard del técnico se filtra automáticamente por esa ubicación. <br><br> **Escenario 2:** <br> *Given* que el técnico ya tiene 10 máquinas asignadas, <br> *When* intento ponerle más, <br> *Then* el sistema me da un aviso de sobrecarga de trabajo. |

| User Story ID | HU19 | Epic ID | EP06 |
| :--- | :--- | :--- | :--- |
| **Título** | Contador de horas de uso (Horómetro) |
| **Descripción** | Como jefe de taller, deseo ver cuántas horas ha trabajado el motor para saber si ya le toca cambio de filtros. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que la máquina está en línea, <br> *When* consulto el horómetro, <br> *Then* veo el tiempo acumulado exacto desde la última revisión. <br><br> **Escenario 2:** <br> *Given* que se intenta manipular el contador, <br> *When* el usuario no es administrador, <br> *Then* el sistema bloquea cualquier edición manual. |

| User Story ID | HU20 | Epic ID | EP06 |
| :--- | :--- | :--- | :--- |
| **Título** | Ubicación GPS de maquinaria |
| **Descripción** | Como gestor de activos, deseo ver en un mapa dónde están mis máquinas para coordinar los viajes de mantenimiento. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que el GPS está activo, <br> *When* abro el mapa de flota, <br> *Then* veo puntos geolocalizados de cada unidad en tiempo real. <br><br> **Escenario 2:** <br> *Given* que no hay señal satelital, <br> *When* cargo el mapa, <br> *Then* veo la última ubicación conocida de la máquina. |

| User Story ID | HU21 | Epic ID | EP07 |
| :--- | :--- | :--- | :--- |
| **Título** | Registro de clientes mineros |
| **Descripción** | Como distribuidor, deseo guardar la información de contacto de las empresas mineras para agilizar futuras ventas. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que ingreso el RUC y nombre de la empresa, <br> *When* guardo el perfil, <br> *Then* los datos quedan disponibles para cualquier proceso de venta futuro. <br><br> **Escenario 2:** <br> *Given* que el RUC está mal escrito, <br> *When* intento guardar, <br> *Then* el sistema indica que el formato no es válido. |

| User Story ID | HU22 | Epic ID | EP07 |
| :--- | :--- | :--- | :--- |
| **Título** | Comentarios técnicos por equipo |
| **Descripción** | Como mecánico de turno, deseo dejar notas sobre ruidos extraños en una máquina para que el siguiente turno esté prevenido. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que estoy en la ficha de la máquina, <br> *When* escribo un comentario y lo publico, <br> *Then* este aparece con mi nombre y la hora exacta del registro. <br><br> **Escenario 2:** <br> *Given* que intento borrar un comentario de otro técnico, <br> *When* hago clic en borrar, <br> *Then* el sistema me deniega el permiso. |

| User Story ID | HU23 | Epic ID | EP08 |
| :--- | :--- | :--- | :--- |
| **Título** | Exportación de historial de sensores |
| **Descripción** | Como analista de datos, deseo descargar un archivo Excel con las lecturas de los últimos 30 días para hacer informes gerenciales. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que selecciono el rango de fechas, <br> *When* presiono "Exportar a Excel", <br> *Then* se descarga un archivo con todas las mediciones de temperatura y vibración. <br><br> **Escenario 2:** <br> *Given* que no hay datos en ese rango, <br> *When* intento descargar, <br> *Then* el archivo baja vacío con un aviso previo. |

| User Story ID | HU24 | Epic ID | EP08 |
| :--- | :--- | :--- | :--- |
| **Título** | Gráficas comparativas de flota |
| **Descripción** | Como gerente, deseo comparar el desempeño de dos excavadoras iguales para saber cuál está rindiendo mejor. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que elijo dos IDs de máquinas, <br> *When* selecciono "Comparar", <br> *Then* veo dos líneas en una misma gráfica para ver cuál calienta más rápido. <br><br> **Escenario 2:** <br> *Given* que una de las máquinas no tiene sensores, <br> *When* intento comparar, <br> *Then* el sistema me indica que faltan datos técnicos. |

| User Story ID | HU25 | Epic ID | EP01 |
| :--- | :--- | :--- | :--- |
| **Título** | Cerrar sesión correctamente |
| **Descripción** | Como usuario de una computadora compartida en la mina, deseo cerrar mi sesión para que nadie más vea los datos de mi empresa. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que estoy logueado, <br> *When* hago clic en "Cerrar Sesión", <br> *Then* el sistema me expulsa al login y borra el token de acceso. <br><br> **Escenario 2:** <br> *Given* que cierro la ventana sin desloguearme, <br> *When* alguien vuelve a entrar en menos de 5 minutos, <br> *Then* el sistema le pide contraseña nuevamente por seguridad. |

| User Story ID | HU26 | Epic ID | EP02 |
| :--- | :--- | :--- | :--- |
| **Título** | Reporte de fallas por operario |
| **Descripción** | Como operario de maquinaria, deseo reportar una falla mecánica detectada visualmente para que el equipo de mantenimiento la revise. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que selecciono la opción "Reportar Falla", <br> *When* describo el problema y envío el formulario, <br> *Then* el sistema genera un ticket de atención inmediata. <br><br> **Escenario 2:** <br> *Given* que no adjunto descripción, <br> *When* intento enviar, <br> *Then* el sistema solicita al menos un comentario breve sobre la falla. |

| User Story ID | HU27 | Epic ID | EP02 |
| :--- | :--- | :--- | :--- |
| **Título** | Búsqueda por modelo de motor |
| **Descripción** | Como técnico, deseo buscar maquinaria según el modelo de motor para saber qué repuestos específicos debo llevar a la mina. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que ingreso el modelo del motor en el buscador, <br> *When* realizo la consulta, <br> *Then* el sistema muestra todas las máquinas que utilizan ese motor. <br><br> **Escenario 2:** <br> *Given* que el motor no existe en la base de datos, <br> *When* busco, <br> *Then* se muestra un mensaje de "Motor no registrado". |

| User Story ID | HU28 | Epic ID | EP03 |
| :--- | :--- | :--- | :--- |
| **Título** | Filtro por estado operativo |
| **Descripción** | Como gestor de flota, deseo filtrar los equipos por "Operativo" o "En Reparación" para organizar el trabajo del día. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que selecciono el estado "En Reparación", <br> *When* aplico el filtro, <br> *Then* solo visualizo los equipos que están fuera de servicio. <br><br> **Escenario 2:** <br> *Given* que todas las máquinas están operativas, <br> *When* filtro por reparación, <br> *Then* la lista aparece vacía con un aviso informativo. |

| User Story ID | HU29 | Epic ID | EP03 |
| :--- | :--- | :--- | :--- |
| **Título** | Alerta de nivel de combustible |
| **Descripción** | Como administrador, deseo recibir una alerta cuando el nivel de combustible sea menor al 15% para evitar paradas por falta de energía. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que el tanque baja del 15%, <br> *When* el sensor envía el dato, <br> *Then* el icono de combustible en el dashboard parpadea en amarillo. <br><br> **Escenario 2:** <br> *Given* que el nivel es crítico (5%), <br> *When* se actualiza el dato, <br> *Then* llega una notificación push de "Nivel crítico de combustible". |

| User Story ID | HU30 | Epic ID | EP04 |
| :--- | :--- | :--- | :--- |
| **Título** | Gestión de proveedores de repuestos |
| **Descripción** | Como distribuidor, deseo registrar los datos de contacto de proveedores para agilizar la compra de piezas de garantía. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que ingreso el nombre y teléfono del proveedor, <br> *When* guardo el contacto, <br> *Then* queda vinculado a la marca de maquinaria correspondiente. <br><br> **Escenario 2:** <br> *Given* que el proveedor ya existe, <br> *When* intento duplicarlo, <br> *Then* el sistema me ofrece editar el contacto existente. |

| User Story ID | HU31 | Epic ID | EP04 |
| :--- | :--- | :--- | :--- |
| **Título** | Notificación de vencimiento de seguro |
| **Descripción** | Como gestor, deseo que el sistema me avise 30 días antes de que venza el seguro de la máquina para realizar el trámite de renovación. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que faltan 30 días para el vencimiento, <br> *When* el sistema revisa las fechas, <br> *Then* genera una alerta en la sección de trámites pendientes. <br><br> **Escenario 2:** <br> *Given* que el seguro ya venció, <br> *When* cargo los datos del equipo, <br> *Then* el estado del documento aparece como "Vencido" en rojo. |

| User Story ID | HU32 | Epic ID | EP05 |
| :--- | :--- | :--- | :--- |
| **Título** | Visualización de manuales digitales |
| **Descripción** | Como técnico en campo, deseo abrir el manual del fabricante desde la app para consultar esquemas técnicos sin cargar libros físicos. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que selecciono una máquina, <br> *When* hago clic en "Manual de Usuario", <br> *Then* se abre un visor de PDF integrado en la plataforma. <br><br> **Escenario 2:** <br> *Given* que no hay manual cargado, <br> *When* intento abrirlo, <br> *Then* el sistema me da la opción de solicitar la subida del documento. |

| User Story ID | HU33 | Epic ID | EP05 |
| :--- | :--- | :--- | :--- |
| **Título** | Registro de piezas reemplazadas |
| **Descripción** | Como técnico, deseo marcar qué piezas específicas cambié en una máquina para llevar un control exacto del inventario de repuestos. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que estoy en el reporte de mantenimiento, <br> *When* selecciono "Filtro de aire" y guardo, <br> *Then* se descuenta del stock virtual y queda registrado en el equipo. <br><br> **Escenario 2:** <br> *Given* que la pieza no está en lista, <br> *When* la escribo manualmente, <br> *Then* el sistema la añade como observación especial. |

| User Story ID | HU34 | Epic ID | EP03 |
| :--- | :--- | :--- | :--- |
| **Título** | Dashboard de eficiencia de combustible |
| **Descripción** | Como analista, deseo ver cuánto combustible consume cada máquina por hora para identificar equipos que necesitan afinamiento. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que elijo un rango de tiempo, <br> *When* veo la gráfica de consumo, <br> *Then* el sistema calcula el promedio de litros por hora automáticamente. <br><br> **Escenario 2:** <br> *Given* que los datos son inconsistentes, <br> *When* visualizo la eficiencia, <br> *Then* el sistema marca la gráfica con una advertencia de "Datos fuera de rango". |

| User Story ID | HU35 | Epic ID | EP05 |
| :--- | :--- | :--- | :--- |
| **Título** | Historial de ubicaciones GPS |
| **Descripción** | Como jefe de logística, deseo ver el recorrido de la máquina en el mapa durante las últimas 24 horas para verificar que no salió de la zona de trabajo. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que elijo la opción "Trazar ruta", <br> *When* selecciono el día de ayer, <br> *Then* el mapa muestra una línea con los puntos de movimiento. <br><br> **Escenario 2:** <br> *Given* que la máquina estuvo estática, <br> *When* trazo la ruta, <br> *Then* solo aparece un punto con la leyenda "Sin movimiento detectado". |

| User Story ID | HU36 | Epic ID | EP06 |
| :--- | :--- | :--- | :--- |
| **Título** | Cambio de unidades de medida |
| **Descripción** | Como usuario internacional, deseo cambiar entre Celsius y Fahrenheit para leer los datos de temperatura en el sistema que prefiera. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que cambio la configuración a "Fahrenheit", <br> *When* regreso al dashboard, <br> *Then* todos los valores de temperatura se convierten automáticamente. <br><br> **Escenario 2:** <br> *Given* que cierro la sesión, <br> *When* vuelvo a entrar, <br> *Then* mi preferencia de unidad de medida se mantiene guardada. |

| User Story ID | HU37 | Epic ID | EP06 |
| :--- | :--- | :--- | :--- |
| **Título** | Modo oscuro para trabajo nocturno |
| **Descripción** | Como operador de noche, deseo activar el modo oscuro para no cansar mi vista al revisar el dashboard en la oscuridad de la mina. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que activo el interruptor de "Modo Oscuro", <br> *When* navego por la app, <br> *Then* los fondos cambian a tonos oscuros y los textos a claros. <br><br> **Escenario 2:** <br> *Given* que es de día, <br> *When* la app detecta mucha luz (sensor del móvil), <br> *Then* me sugiere volver al modo claro. |

| User Story ID | HU38 | Epic ID | EP06 |
| :--- | :--- | :--- | :--- |
| **Título** | Suscripción a alertas específicas |
| **Descripción** | Como técnico jefe, deseo suscribirme solo a las alertas de "Presión Hidráulica" para no recibir notificaciones que no corresponden a mi área. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que en mi perfil marco solo "Presión", <br> *When* ocurre una falla de temperatura, <br> *Then* no recibo notificación push, pero sí queda en el registro. <br><br> **Escenario 2:** <br> *Given* que ocurre la falla de presión, <br> *When* el sistema la detecta, <br> *Then* me llega el aviso inmediatamente. |

| User Story ID | HU39 | Epic ID | EP01 |
| :--- | :--- | :--- | :--- |
| **Título** | Auditoría de cambios en inventario |
| **Descripción** | Como administrador, deseo ver quién modificó el stock de una máquina para evitar cambios no autorizados en los datos de venta. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que consulto el log de actividad, <br> *When* filtro por una máquina, <br> *Then* veo el nombre del usuario y la hora exacta en que cambió el precio o estado. <br><br> **Escenario 2:** <br> *Given* que no hay cambios recientes, <br> *When* reviso el historial, <br> *Then* el sistema muestra "Sin modificaciones registradas". |

| User Story ID | HU40 | Epic ID | EP06 |
| :--- | :--- | :--- | :--- |
| **Título** | Vista simplificada para operarios |
| **Descripción** | Como operario de cabina, deseo una vista con botones grandes y solo datos críticos para verlos rápido mientras manejo. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que activo la "Vista de Cabina", <br> *When* miro la pantalla, <br> *Then* solo aparecen los 3 indicadores más importantes en tamaño grande. <br><br> **Escenario 2:** <br> *Given* que necesito ver detalles, <br> *When* hago clic en un indicador, <br> *Then* el sistema me muestra la gráfica detallada. |

| User Story ID | HU41 | Epic ID | EP04 |
| :--- | :--- | :--- | :--- |
| **Título** | Registro de kilometraje |
| **Descripción** | Como gestor de transporte, deseo registrar el kilometraje de los camiones mineros para programar el rotado de neumáticos. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que actualizo el dato de kilómetros recorridos, <br> *When* el valor llega a 10,000 km, <br> *Then* el sistema sugiere una inspección de llantas. <br><br> **Escenario 2:** <br> *Given* que el dato es menor al anterior, <br> *When* intento guardar, <br> *Then* el sistema me pide confirmar si hubo un error de digitación. |

| User Story ID | HU42 | Epic ID | EP03 |
| :--- | :--- | :--- | :--- |
| **Título** | Alerta de batería de dispositivo IoT |
| **Descripción** | Como técnico de sistemas, deseo saber si la batería del sensor IoT está por agotarse para ir a cambiarla antes de perder la conexión. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que el sensor reporta 10% de energía, <br> *When* entro al panel de configuración, <br> *Then* veo un icono de batería baja al lado del ID del sensor. <br><br> **Escenario 2:** <br> *Given* que el sensor muere, <br> *When* el sistema deja de recibir señal, <br> *Then* se genera una alerta de "Pérdida de enlace IoT". |

| User Story ID | HU43 | Epic ID | EP03 |
| :--- | :--- | :--- | :--- |
| **Título** | Evaluación de desempeño (KPIs) |
| **Descripción** | Como gerente, deseo ver un puntaje de salud (0-100) de cada máquina para saber cuáles son las más confiables de mi flota. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que la máquina no ha tenido fallas en el mes, <br> *When* consulto su perfil, <br> *Then* el sistema le asigna un puntaje de "A" o 95/100. <br><br> **Escenario 2:** <br> *Given* que tiene muchas alertas rojas, <br> *When* reviso el ranking, <br> *Then* aparece en los últimos lugares como equipo de alto riesgo. |

| User Story ID | HU44 | Epic ID | EP06 |
| :--- | :--- | :--- | :--- |
| **Título** | Chat interno para equipo técnico |
| **Descripción** | Como técnico, deseo enviar mensajes directos a otros compañeros desde la ficha de la máquina para coordinar reparaciones grupales. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que escribo en el muro de la máquina, <br> *When* envío el mensaje, <br> *Then* todos los asignados a ese equipo reciben la notificación. <br><br> **Escenario 2:** <br> *Given* que adjunto una foto de una pieza rota, <br> *When* la envío por el chat, <br> *Then* la imagen queda guardada en el historial de ese activo. |

| User Story ID | HU45 | Epic ID | EP04 |
| :--- | :--- | :--- | :--- |
| **Título** | Carga de facturas de mantenimiento |
| **Descripción** | Como contador, deseo subir las facturas de repuestos comprados para llevar el control de gastos por cada máquina. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que subo un archivo PDF de factura, <br> *When* le asigno un monto y categoría, <br> *Then* se suma automáticamente al costo operativo total del equipo. <br><br> **Escenario 2:** <br> *Given* que el monto es muy alto, <br> *When* guardo, <br> *Then* el sistema pide una segunda confirmación para evitar errores. |

| User Story ID | HU46 | Epic ID | EP03 |
| :--- | :--- | :--- | :--- |
| **Título** | Mapa de calor de actividad |
| **Descripción** | Como jefe de operaciones, deseo ver un mapa de calor para identificar en qué zonas de la mina las máquinas están sufriendo más sobrecalentamiento. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que selecciono "Mapa de Calor de Temperatura", <br> *When* cargo la vista, <br> *Then* las zonas con máquinas calientes aparecen en color rojo intenso. <br><br> **Escenario 2:** <br> *Given* que todas operan normal, <br> *When* veo el mapa, <br> *Then* toda la zona se muestra en color azul o verde suave. |

| User Story ID | HU47 | Epic ID | EP01 |
| :--- | :--- | :--- | :--- |
| **Título** | Gestión de perfiles de empresa |
| **Descripción** | Como administrador, deseo editar los datos de mi empresa (logo, dirección, RUC) para que aparezcan correctamente en los reportes PDF. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que subo el nuevo logo de la empresa, <br> *When* guardo la configuración, <br> *Then* todos los documentos generados a partir de ahora tendrán el nuevo logo. <br><br> **Escenario 2:** <br> *Given* que el RUC no tiene 11 dígitos, <br> *When* intento guardar, <br> *Then* el sistema rebota el cambio por formato incorrecto. |

| User Story ID | HU48 | Epic ID | EP04 |
| :--- | :--- | :--- | :--- |
| **Título** | Recordatorio de inspección de seguridad |
| **Descripción** | Como oficial de seguridad, deseo que el sistema me obligue a llenar un checklist de seguridad antes de permitir que un técnico registre un mantenimiento. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que el técnico abre una orden de trabajo, <br> *When* intenta finalizarla, <br> *Then* el sistema le exige marcar que usó casco y guantes antes de cerrar. <br><br> **Escenario 2:** <br> *Given* que no marca los puntos de seguridad, <br> *When* presiona guardar, <br> *Then* el botón de "Finalizar" se mantiene bloqueado. |

| User Story ID | HU49 | Epic ID | EP05 |
| :--- | :--- | :--- | :--- |
| **Título** | Visualización de esquemas eléctricos |
| **Descripción** | Como electricista, deseo ver los planos eléctricos del equipo en alta resolución para encontrar cables cortados rápidamente. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que abro el plano eléctrico, <br> *When* hago zoom en la pantalla, <br> *Then* la imagen no pierde calidad y permite leer los códigos de los cables. <br><br> **Escenario 2:** <br> *Given* que el archivo no carga, <br> *When* refresco la página, <br> *Then* el sistema reintenta la descarga desde el servidor de respaldo. |

| User Story ID | HU50 | Epic ID | EP06 |
| :--- | :--- | :--- | :--- |
| **Título** | Backup de datos técnicos |
| **Descripción** | Como administrador de sistemas, deseo programar una descarga semanal de toda la base de datos para no perder información por fallas del servidor. |
| **Criterios de Aceptación** | **Escenario 1:** <br> *Given* que llega el domingo a las 12 AM, <br> *When* el sistema ejecuta la tarea, <br> *Then* se genera un archivo .sql comprimido en el almacenamiento de la nube. <br><br> **Escenario 2:** <br> *Given* que el backup falla por espacio, <br> *When* termina el proceso, <br> *Then* me llega un correo de alerta inmediata indicando "Error de Backup". |

## 3.2. Impact Mapping

<img width="2167" height="1330" alt="Mapa de impacto" src="https://github.com/user-attachments/assets/de34843f-3b4e-49e4-9241-d44da61a2984" />

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
