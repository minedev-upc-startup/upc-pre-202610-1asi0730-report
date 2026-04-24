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
