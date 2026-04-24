## Capítulo IV: Product Design

### 4.1. Style Guidelines.

En esta sección se sientan las bases visuales y de comunicación comunes para la experiencia de MineTrack. Se define el repositorio de estilos compartido por Landing Page y Web Application, con el fin de mantener una presentación consistente entre pantallas, roles y dispositivos.

### 4.1.1. General Style Guidelines.

### **Colores**

![Colors](Resources/style/colors.jpeg)

Ámbar — #F59E0B: Este color transmite energía, acción y el ambiente industrial propio de la maquinaria pesada. Es ideal para botones principales, acentos, íconos clave y elementos que deben destacar en la interfaz.

Ámbar Suave — #FEF3C7: Este color se utiliza como fondo para banners promocionales, estados seleccionados y elementos que requieren resaltar sin competir con los botones principales.

Slate Oscuro — #0F172A: Este color expresa robustez, seriedad y confiabilidad. Es el color principal de la marca, usado en textos importantes, logo, sidebar de navegación y fondos oscuros.

Slate Medio — #475569: Este color se usa para el cuerpo del texto principal. Aporta buena legibilidad sobre fondos claros sin la rigidez del negro puro.

Slate Claro — #F1F5F9: Este color se utiliza como fondo de tarjetas, paneles y áreas secundarias. Aporta limpieza sin competir con el blanco puro.

Teal — #14B8A6: Este color se reserva exclusivamente para elementos del módulo IoT y telemetría, lo que hace visualmente distinguible ese contexto frente al resto de la plataforma.

Verde Éxito — #10B981: Este color se utiliza para confirmaciones, estados "Disponible", mensajes de éxito y métricas positivas.

Rojo Peligro — #EF4444: Este color se reserva para errores, alertas críticas, estados "Rechazado" y acciones destructivas.

Blanco — #FFFFFF: El color ideal para fondos principales de la aplicación, tarjetas y superficies que requieren máxima legibilidad.

### **Tipografía**

Se seleccionó la tipografía "Manrope" como la principal para los títulos, encabezados y botones de la plataforma. Además, se utiliza la tipografía "Inter" como secundaria para los textos de cuerpo y descripciones largas. Ambas se eligieron por su estilo moderno, legible y técnico, adecuado para un producto orientado a operaciones mineras, donde la claridad en la información es crítica.

Adicionalmente, se utiliza la tipografía monoespaciada "JetBrains Mono" para valores numéricos de telemetría, IDs de máquina, coordenadas GPS y horómetros, asegurando una lectura precisa de datos técnicos.

Manrope:

![Manrope](Resources/style/Manrope_Tamanios.png)

Inter:

![Inter](Resources/style/Inter_Tamanios.png)

JetBrains Mono:

![JetBrains Mono](Resources/style/JetBrainsMono_Tamanios.png)

### **Branding**

El branding de MineTrack se diseñó para transmitir robustez industrial, precisión técnica y confiabilidad. El logo combina un hexágono (que representa una tuerca y una red de conexión) con un pin de ubicación inscrito en su interior, simbolizando la trazabilidad y el monitoreo de la flota. El uso del ámbar sobre el slate oscuro refleja el color característico de la maquinaria pesada minera.

![MineTrack Logo](Resources/MIneTrack.jpg)

### **Espaciado**

El diseño de MineTrack se apoya en un sistema de espaciado basado en múltiplos de 4 píxeles, que asegura ritmo y consistencia en todas las pantallas. Cada sección de la plataforma mantiene un ancho máximo definido que evita la sobrecarga visual y permite que el contenido respire adecuadamente. Los márgenes alrededor de tarjetas, tablas y formularios generan equilibrio visual, mientras que los rellenos internos en botones, inputs y secciones principales permiten destacar las acciones clave. Esta distribución asegura que los elementos más relevantes (estado de máquinas, alertas críticas, CTAs) sobresalgan con claridad sin competir entre sí.

### **Dimensiones para el tono de comunicación y lenguaje aplicado**

En MineTrack, el tono de comunicación refleja seriedad y cercanía profesional, acorde con un segmento que maneja contratos formales, equipos de alto valor y operaciones críticas. La voz de la marca es clara, directa y respetuosa, con el objetivo de que Propietarios, Clientes e Intermediarios se sientan acompañados sin infantilización ni adornos innecesarios.

En cuanto al lenguaje, se prefiere el uso del "tú" para mantener cercanía sin perder profesionalismo, con verbos en infinitivo para botones ("Solicitar alquiler", "Cerrar alquiler") y mensajes de error que explican qué pasó y qué hacer. El tono se posiciona como serio (8/10), intermedio en formalidad (6/10 hacia formal), altamente respetuoso (9/10) y sereno (7/10), evitando celebraciones exageradas y priorizando retroalimentación útil.

### **Elementos de diseño**

El diseño visual de MineTrack se basa en una estética limpia, técnica y moderna. La paleta combina el slate oscuro como base de robustez con acentos en ámbar que resaltan las llamadas a la acción y aportan la identidad industrial del sector minero. La tipografía mantiene jerarquías claras: encabezados de gran tamaño para la Landing Page y títulos de módulo, subtítulos intermedios que organizan el contenido, y cuerpos de texto con buena legibilidad tanto en desktop como en móvil.

En cuanto a las formas, predominan los bordes redondeados moderados (8 px para botones y cards, 12–16 px para modales) que aportan accesibilidad sin restar robustez. Esto se complementa con el uso de iconografía de la librería Lucide Icons (open-source, stroke 1.5 px) y fotografías reales de maquinaria pesada en contextos operativos. La combinación de estos elementos garantiza que el usuario perciba la plataforma como profesional, técnica y confiable, alineada con la naturaleza del negocio minero.

### **Principios de diseño**

Los principios de diseño aplicados en MineTrack buscan asegurar coherencia, claridad y facilidad de uso. El contraste juega un papel clave para resaltar botones de acción, badges de estado y alertas críticas, garantizando que la información crítica siempre esté visible. La repetición de patrones visuales (colores, estilos de cards, tipografías y componentes compartidos) genera consistencia y familiaridad, reduciendo la curva de aprendizaje al navegar entre los tres roles de la plataforma.

La alineación refuerza el orden y la profesionalidad, asegurando que tablas, formularios y paneles mantengan una disposición armónica. Finalmente, la proximidad organiza los elementos de manera lógica: las tarjetas resumen del Dashboard se agrupan en una fila superior, las acciones relacionadas con un alquiler se agrupan en su ficha, y las alertas se agrupan en un panel dedicado. Estos principios en conjunto permiten que la experiencia sea intuitiva, confiable y visualmente coherente, alineada con la misión de MineTrack de ofrecer trazabilidad total y operación sin fricción.

### 4.1.2. Web Style Guidelines.

El diseño web de MineTrack está optimizado para proporcionar una experiencia fluida y coherente en distintos dispositivos y tamaños de pantalla. Se emplean layouts adaptativos, que reacomodan los elementos según el breakpoint (desktop ≥ 1024 px, tablet 768–1023 px, mobile < 768 px), manteniendo la jerarquía visual en cualquier resolución. Los anchos de contenido y las imágenes se ajustan dinámicamente para preservar las proporciones y evitar distorsión.

Los elementos interactivos (botones, enlaces, filas de tabla, tarjetas del catálogo) poseen estados visuales claros — default, hover, active, focus y disabled — que indican al usuario el resultado de cada interacción antes de ejecutarla. Los formularios están diseñados para ser intuitivos y rápidos de completar: labels siempre visibles sobre el input (nunca placeholder como único indicador), validación en tiempo real con mensajes específicos y helper text para campos complejos. Las tablas de datos soportan ordenamiento por columna, filtros persistentes y paginación del lado servidor, mientras que los dashboards combinan tarjetas resumen, charts y tablas compactas para ofrecer información agregada en una sola vista.

### 4.1.3. Mobile Style Guidelines.

El diseño móvil de MineTrack adopta un enfoque _mobile-first_ que prioriza la legibilidad y la facilidad de interacción en pantallas pequeñas. Los componentes base de la guía web se mantienen, con ajustes específicos: todos los elementos tappables (botones, íconos de acción, filas de listas) respetan un tamaño mínimo de 44×44 píxeles conforme al estándar WCAG 2.5.5, y el espaciado entre elementos interactivos es suficiente para evitar toques accidentales.

La navegación en móvil se apoya en tres patrones: un App Bar superior de 56 px con botón hamburguesa que despliega un drawer lateral, una Bottom Navigation de 64 px con los accesos más frecuentes según el rol (Dashboard, Catálogo/Máquinas, Alquileres, Perfil), y un Floating Action Button (FAB) para la acción principal de cada pantalla (por ejemplo, "Nueva solicitud" para Cliente o "Nueva máquina" para Propietario). Las tablas de datos se convierten en cards apiladas verticalmente, cada una mostrando los campos clave de una fila en formato label-valor. Los formularios ocupan el ancho completo, con el teclado contextual apropiado (`type=email`, `inputmode=numeric`, datepicker nativo) para minimizar la fricción.

### 4.2. Information Architecture.

### 4.2.1. Organization Systems.

En el sistema de MineTrack se implementa una organización jerárquica para estructurar la información crítica: el catálogo de máquinas, el ciclo de alquileres, el panel IoT y la gestión de usuarios. Esta jerarquía permite que cada rol (Cliente, Propietario, Intermediario) identifique de forma inmediata los módulos relevantes para su flujo de trabajo, con una Sidebar que agrupa las funcionalidades principales por contexto.

Se aplica además una organización secuencial en procesos que requieren una guía paso a paso, como el registro de una nueva máquina (wizard de 3 pasos: información básica → especificaciones → fotos y tarifa), la solicitud de un alquiler (selección de máquina → fechas → confirmación) y el cierre de un alquiler (revisión de horas → validación → generación de contrato PDF). Estos flujos siguen una progresión lógica que minimiza errores y garantiza que toda la información necesaria sea registrada en el orden correcto.

En cuanto a esquemas de categorización, se emplea una organización cronológica para visualizar datos históricos, como el historial de alquileres cerrados, las lecturas IoT por rango de fechas o el registro de alertas. Además, el contenido se clasifica según el rol: el Intermediario accede al panel operativo completo (dashboard, solicitudes, alquileres, IoT, alertas, facturación, usuarios), el Propietario accede a la gestión de su flota y reporte de ganancias, y el Cliente accede al catálogo público, sus solicitudes y su historial. Esta separación por rol garantiza que cada usuario vea únicamente lo que necesita para su responsabilidad en el negocio.

### 4.2.2. Labeling Systems.

A continuación se presenta el sistema de etiquetado diseñado para la plataforma MineTrack. El sistema busca representar los datos de forma clara, con etiquetas cortas, familiares y alineadas con el lenguaje del sector minero, para minimizar la carga cognitiva y mantener coherencia visual con la guía de estilo.

Se ha priorizado la claridad semántica y la coherencia con el _Ubiquitous Language_ definido en el Capítulo III, respetando los mismos conceptos ("Máquina", "Alquiler", "Solicitud", "Propietario", "Cliente", "Intermediario") en toda la plataforma.

#### 1. Landing Page:

Inicio: Sección principal de bienvenida. Presenta la propuesta de valor de la plataforma con dos CTAs diferenciadas por segmento (Cliente y Propietario).

Características: Explicación de los seis módulos principales de la plataforma (Catálogo, Proceso de Alquiler, Dashboard, Monitoreo IoT, Gestión de Usuarios y Facturación).

Beneficios: Sección con contenido diferenciado según el segmento del visitante (Cliente o Propietario), resaltando el valor concreto para cada perfil.

Contacto: Formulario de contacto con selector de rol (Cliente / Propietario / Otro) y campo de consulta, para resolver dudas antes del registro.

Footer: Información legal (términos, política de privacidad), selector de idioma (ES / EN) y accesos secundarios.

#### 2. Aplicación Web:

Dashboard: Vista general adaptada al rol. Para el Intermediario muestra tarjetas resumen de la flota, alquileres activos y panel de alertas; para el Propietario muestra su flota, ganancias y alquileres asociados; para el Cliente muestra sus solicitudes activas y gasto reciente.

Catálogo: Listado de máquinas con filtros por tipo, marca y tarifa. Accesible para Cliente e Intermediario.

Mis Máquinas: Sección del Propietario para registrar, editar y gestionar el estado (Disponible / En Mantenimiento) de sus máquinas.

Solicitudes: Bandeja del Intermediario para revisar y aprobar o rechazar las solicitudes de alquiler pendientes.

Alquileres: Listado de alquileres activos y cerrados, con acceso al detalle de cada uno y acciones según rol (registrar horas, cerrar, descargar contrato).

Monitoreo IoT: Panel del Intermediario con mapa en vivo de la ubicación GPS de la flota y lista lateral con el estado de cada máquina.

Alertas: Bandeja de alertas operativas (devoluciones vencidas, mantenimientos próximos, lecturas IoT fuera de rango).

Facturación: Resumen consolidado del Intermediario con totales facturados, cobrados y pendientes, junto con desglose por Propietario.

Ganancias: Reporte del Propietario con totales por rango de fechas y desglose por máquina.

Usuarios: Gestión de los tres roles de la plataforma (Cliente, Propietario, Intermediario) por parte del Intermediario.

Perfil: Gestión de datos personales, contraseña y preferencias de cada usuario autenticado.

### 4.2.3. SEO Tags and Meta Tags.

#### 1. Landing Page

##### Charset

```
<meta charset="utf-8">
```

Define la codificación de caracteres como UTF-8, garantizando que se muestren correctamente acentos, la ñ y símbolos especiales en cualquier idioma.

##### Viewport

```
<meta name="viewport" content="width=device-width, initial-scale=1">
```

Hace que la página sea responsiva, adaptándose automáticamente a diferentes tamaños de pantalla para una visualización óptima y legible.

##### Title

```
<title>MineTrack | Smart rental of mining machinery</title>
```

Define el título de la página que aparece en la pestaña del navegador y en los resultados de búsqueda.

##### Meta Description

```
<meta name="description" content="Digital platform that connects owners and customers of heavy mining equipment. Request machinery, monitor operations in real time with IoT and manage rentals in one place.">
```

Proporciona un resumen breve y atractivo del contenido de la página para los resultados de búsqueda.

##### Meta Keywords

```
<meta name="keywords" content="mining machinery rental, mining, excavator, heavy equipment, IoT monitoring, fleet management, Peru">
```

Especifica palabras clave para el contenido de la página.

##### Meta Author

```
<meta name="author" content="MineTrack Team">
```

Identifica al creador o responsable del contenido.

##### Meta Language

```
<meta name="language" content="en">
```

Declara el idioma principal del contenido de la página.

##### Meta Copyright

```
<meta name="copyright" content="MineTrack 2026">
```

Indica la entidad propietaria de los derechos de autor y el año correspondiente.

##### Open Graph

```
<meta property="og:title" content="MineTrack | Smart rental of mining machinery">
<meta property="og:description" content="Connect owners and customers of heavy mining equipment with IoT monitoring and digital contracts.">
<meta property="og:image" content="https://minetrack.app/og/og-home.png">
<meta property="og:url" content="https://minetrack.app/">
<meta property="og:type" content="website">
```

Controlan cómo se muestra la página cuando se comparte en redes sociales.

#### 2. Web Application

##### Charset

```
<meta charset="utf-8">
```

##### Viewport

```
<meta name="viewport" content="width=device-width, initial-scale=1">
```

##### Title

```
<title>MineTrack | Smart rental of mining machinery</title>
```

##### Meta Description

```
<meta name="description" content="Platform that connects owners and customers of heavy mining equipment with IoT monitoring and digital contracts in one place.">
```

##### Meta Robots

```
<meta name="robots" content="noindex, nofollow">
```

Indica a los motores de búsqueda que no indexen el contenido de la aplicación autenticada, ya que se trata de información privada de cada usuario.

##### Meta Author

```
<meta name="author" content="MineTrack Team">
```

##### Meta Language

```
<meta name="language" content="en">
```

##### Meta Copyright

```
<meta name="copyright" content="MineTrack 2026">
```

### 4.2.4. Searching Systems.

#### 1. Medios de ayuda para la búsqueda de elementos de gestión

Barra de búsqueda global en el top bar de la aplicación, accesible desde cualquier pantalla autenticada. Permite buscar máquinas por nombre o modelo, alquileres por ID o cliente, y usuarios (este último solo para el Intermediario).

Barra de búsqueda específica en cada módulo principal (Catálogo, Alquileres, Alertas, Usuarios) con autocompletado inteligente que muestra sugerencias conforme el usuario escribe.

Historial de búsquedas recientes, accesible al hacer clic en la barra vacía, para volver rápidamente a consultas anteriores.

Mensajes contextuales si no se encuentran resultados, con sugerencia de acción (por ejemplo, "No se encontraron máquinas con esos filtros. [Limpiar filtros]").

Atajo de teclado (Cmd/Ctrl + K) para abrir la búsqueda global desde cualquier pantalla sin usar el mouse.

#### 2. Filtros y opciones

Por tipo de máquina: Excavadora, Cargador Frontal, Volquete, Perforadora, Tractor, Otro.

Por marca de máquina: Caterpillar, Komatsu, Volvo, Hitachi, John Deere, Otra.

Por rango de tarifa: slider doble de valor mínimo y máximo en soles por hora.

Por estado de la máquina: Disponible, Alquilada, En Mantenimiento (visible para Intermediario; el Cliente solo ve Disponibles por defecto).

Por rango de fechas: aplicable en Alquileres, Alertas, Ganancias e Histórico IoT.

Por estado del alquiler: Pendiente, Aprobada, Rechazada, Activa, Cerrada.

Por tipo de alerta: Devolución vencida, Mantenimiento próximo, IoT fuera de rango.

Por rol del usuario: Cliente, Propietario, Intermediario (en la pantalla de gestión de usuarios).

#### 3. Visualización de resultados

Los resultados del Catálogo se muestran en una grilla de tarjetas con imagen principal, tipo, marca, modelo, tarifa y badge de estado. Permite alternar entre vista de grilla y vista de lista.

Los resultados de Alquileres se muestran en una tabla con columnas: ID del alquiler, máquina (thumbnail + nombre), cliente, fecha de inicio, fecha de cierre prevista, horas registradas y acciones disponibles según rol.

Los resultados de Alertas se muestran en una lista vertical con ícono por tipo, título, descripción, timestamp e indicador visual de "no leída".

Los resultados de Usuarios se muestran en una tabla con avatar, nombre, correo, empresa, rol, fecha de registro y acciones de gestión (ver, suspender, eliminar).

En todos los casos, cuando se aplican filtros aparece un chip removible debajo de la barra de búsqueda indicando el filtro activo, junto con un botón "Limpiar filtros" y el contador total de resultados encontrados.

### 4.2.5. Navigation Systems.

El sistema de navegación de MineTrack está diseñado para guiar al usuario de forma fluida tanto en la Landing Page como en la aplicación autenticada, respetando las particularidades de cada contexto.

En la Landing Page, la barra de navegación superior funciona como un índice claro que ofrece acceso rápido a las secciones clave de la página. Los enlaces como "Características", "Beneficios" y "Contacto" están estratégicamente ubicados para seguir una lógica narrativa: primero se presenta la solución con la propuesta de valor del Hero, luego se explican las funcionalidades concretas en Características, después se diferencia el valor por segmento en Beneficios, y finalmente se ofrecen canales de contacto directo. Los botones "Iniciar sesión" y "Registrarse" están resaltados en la esquina derecha para funcionar como los principales llamados a la acción, accesibles en todo momento durante el scroll. El desplazamiento vertical es el mecanismo de navegación primario, con secciones que cuentan una historia lógica desde la curiosidad inicial hasta la conversión en usuario registrado.

En la aplicación autenticada, la navegación global se apoya en una Sidebar vertical izquierda que agrupa los módulos del rol activo (Cliente, Propietario o Intermediario). La Sidebar se mantiene visible en todas las pantallas para que el usuario pueda saltar entre módulos sin perder contexto, con un ítem activo resaltado en ámbar sobre fondo slate oscuro. A nivel local, cada módulo utiliza tabs horizontales para moverse entre subvistas (por ejemplo, en Catálogo: "Todas / Disponibles / Alquiladas / Mantenimiento"; en el detalle de una máquina: "Información / Especificaciones / Historial / IoT"). Los breadcrumbs aparecen en el top bar para toda vista a dos o más niveles de profundidad (por ejemplo, "Catálogo / Caterpillar 336 GC"), permitiendo al usuario ubicarse y navegar hacia atrás rápidamente.

La navegación contextual complementa los sistemas anteriores con enlaces que aparecen según el contenido actual: desde la ficha de una máquina se puede saltar a su historial IoT o al perfil del propietario; desde un alquiler cerrado se accede al contrato PDF y al reporte de facturación asociado. Este sistema en conjunto es intuitivo y efectivo porque no solo le dice al usuario dónde ir, sino que le muestra las conexiones naturales entre los datos del negocio, replicando mentalmente el flujo operativo de un alquiler minero.

### 4.3. Landing Page UI Design.

En esta sección se presenta la propuesta visual del Landing Page de MineTrack, traduciendo las decisiones de la guía de estilo y la arquitectura de información en pantallas concretas. El Landing Page cubre las secciones requeridas por las User Stories US30–US35 del Epic EP07 (Landing Page e Información Pública): Hero con propuesta de valor, Características, Beneficios diferenciados por segmento, Testimonios, Contacto y Footer legal. Se presenta en dos niveles de fidelidad (wireframe y mock-up) y cubre el viewport desktop, sobre el cual se derivan las adaptaciones móviles.

### 4.3.1. Landing Page Wireframe.

Hero:

![Hero Wireframe](Resources/wireframes/landingPage/Hero.png)

Características:

![Features Wireframe](Resources/wireframes/landingPage/Caracteristicas.png)

Beneficios:

![Benefits Wireframe](Resources/wireframes/landingPage/Beneficios.png)

Testimonios:

![Testimonials Wireframe](Resources/wireframes/landingPage/Testimonios.png)

Contacto:

![Contact Wireframe](Resources/wireframes/landingPage/Contacto.png)

Footer:

![Footer Wireframe](Resources/wireframes/landingPage/Footer.png)

### 4.3.2. Landing Page Mock-up.

Hero:

![Hero Mockup](Resources/mockups/landingPage/Hero.png)

Características:

![Features Mockup](Resources/mockups/landingPage/Caracteristicas.png)

Beneficios:

![Benefits Mockup](Resources/mockups/landingPage/Beneficios.png)

Testimonios:

![Testimonials Mockup](Resources/mockups/landingPage/Testimonios.png)

Contacto:

![Contact Mockup](Resources/mockups/landingPage/Contacto.png)

Footer:

![Footer Mockup](Resources/mockups/landingPage/Footer.png)

### 4.4. Web Applications UX/UI Design.

En esta sección se presenta la propuesta visual y de interacción para las pantallas autenticadas de MineTrack, que cubren los tres roles de la plataforma (Cliente, Propietario e Intermediario) y las User Stories funcionales prioritarias del producto (US01–US20, US23, US27). Se presentan los wireframes (baja fidelidad), los wireflow diagrams de las tareas principales, los mock-ups (alta fidelidad) y los user flow diagrams que documentan los flujos end-to-end del producto.

### 4.4.1. Web Applications Wireframes.

Inicio de sesión:

![Login Wireframe](Resources/wireframes/WebApplication/Login.png)

Creación de cuenta:

![Register Wireframe](Resources/wireframes/WebApplication/Register.png)

Catálogo de máquinas:

![Catalog Wireframe](Resources/wireframes/WebApplication/Catalog.png)

Detalle de máquina:

![Machine Detail Wireframe](Resources/wireframes/WebApplication/Machine_Detail.png)

Solicitud de alquiler:

![Request Rental Wireframe](Resources/wireframes/WebApplication/Request_Rental.png)

Mis solicitudes (Cliente):

![My Requests Wireframe](Resources/wireframes/WebApplication/My_Requests.png)

Mis alquileres (Cliente):

![My Rentals Wireframe](Resources/wireframes/WebApplication/My_Rentals.png)

Detalle del alquiler:

![Rental Detail Wireframe](Resources/wireframes/WebApplication/Rental_Detail.png)

Dashboard del Propietario:

![Owner Dashboard Wireframe](Resources/wireframes/WebApplication/Owner_Dashboard.png)

Mis máquinas (Propietario):

![My Machines Wireframe](Resources/wireframes/WebApplication/My_Machines.png)

Registro de nueva máquina (Propietario):

![Register Machine Wireframe](Resources/wireframes/WebApplication/Register_Machine.png)

Dashboard del Intermediario:

![Broker Dashboard Wireframe](Resources/wireframes/WebApplication/Broker_Dashboard.png)

Bandeja de solicitudes (Intermediario):

![Requests Inbox Wireframe](Resources/wireframes/WebApplication/Requests_Inbox.png)

Monitoreo IoT:

![IoT Monitoring Wireframe](Resources/wireframes/WebApplication/IoT_Monitoring.png)

Ficha IoT de máquina (Intermediario):

![IoT Machine Detail Wireframe](Resources/wireframes/WebApplication/IoT_Machine_Detail.png)

### 4.4.2. Web Applications Wireflow Diagrams.

#### Task Flow 1: Solicitud de alquiler por parte del Cliente

Objetivo del usuario: Encontrar una máquina que cumpla con los requerimientos operativos y enviar una solicitud formal de alquiler para un rango de fechas determinado.

**Pasos del Task Flow:**

Acceder a la vista "Catálogo" desde la Sidebar.

Aplicar filtros por tipo, marca y rango de tarifa para reducir las opciones.

Seleccionar una máquina del resultado para ver su detalle completo.

Revisar especificaciones técnicas, fotos y tarifa por hora.

Presionar el botón "Solicitar alquiler".

Completar el rango de fechas en el formulario.

Agregar la ubicación de la obra y detalles opcionales del uso.

Confirmar el envío de la solicitud.

El sistema valida disponibilidad y envía la solicitud al Intermediario.

El Cliente es redirigido a "Mis Solicitudes" con la nueva en estado "Pendiente".

![Task Flow 1 - Cliente solicita máquina](Resources/wireframes/wireflows/flow1.jpg)

**User Goals:**

User goal 1: Como Cliente, quiero encontrar y solicitar una máquina disponible para un rango de fechas específico.

**User Stories:**

US01: Visualización del catálogo público de máquinas
US02: Filtrado y búsqueda de máquinas
US03: Consulta de detalle de una máquina
US06: Solicitud de alquiler de una máquina

#### Task Flow 2: Registro de una nueva máquina por parte del Propietario

Objetivo del usuario: Publicar una máquina en el catálogo con toda la información, fotos y tarifa necesarias para que esté disponible a los Clientes.

**Pasos del Task Flow:**

Acceder a la vista "Mis Máquinas" desde la Sidebar.

Presionar el botón "+ Nueva máquina".

Completar el paso 1 del wizard con información básica (nombre, tipo, marca, modelo, año, ubicación).

Avanzar al paso 2 y completar especificaciones técnicas (potencia, peso, capacidad, tipo de combustible, horas acumuladas iniciales).

Avanzar al paso 3, subir al menos una foto y definir la tarifa por hora.

Agregar una descripción pública de la máquina.

Confirmar el registro.

El sistema crea la máquina con estado inicial "Disponible" y la publica en el catálogo.

El Propietario es redirigido a "Mis Máquinas" donde la nueva máquina es visible.

![Task Flow 2 - Propietario registra máquina](Resources/wireframes/wireflows/flow2.jpg)

**User Goals:**

User goal 2: Como Propietario, quiero publicar mi máquina en el catálogo con toda su información para que los Clientes puedan solicitarla.

**User Stories:**

US04: Registro de una máquina nueva
US05: Edición de datos y estado de una máquina

#### Task Flow 3: Aprobación de solicitud por parte del Intermediario

Objetivo del usuario: Procesar una solicitud de alquiler pendiente, revisando su detalle y aprobándola o rechazándola según corresponda para activar el alquiler.

**Pasos del Task Flow:**

Acceder al Dashboard operativo del Intermediario desde el Login.

Identificar solicitudes pendientes en el panel de alertas del Dashboard o navegar directamente a la sección "Solicitudes" desde la Sidebar.

Revisar la bandeja de solicitudes pendientes, donde se muestran los datos clave de cada petición: cliente, máquina solicitada, rango de fechas y tiempo transcurrido desde la solicitud.

Expandir una solicitud para visualizar su detalle completo, incluyendo información del cliente, propósito del alquiler y observaciones adicionales.

Evaluar la viabilidad del alquiler considerando la disponibilidad de la máquina en el rango de fechas propuesto.

Presionar "Aprobar" para activar el alquiler, o "Rechazar" e ingresar el motivo si la solicitud no procede.

El sistema actualiza el estado de la solicitud y notifica al Cliente del resultado.

En caso de aprobación, la máquina cambia automáticamente a estado "Alquilada" y queda lista para ser monitoreada posteriormente desde la sección de Alquileres del Intermediario.

![Task Flow 3 - Intermediario aprueba solicitud](Resources/wireframes/wireflows/flow3.jpg)

**User Goals:**

User goal 3: Como Intermediario, quiero evaluar y procesar las solicitudes de alquiler pendientes de forma eficiente para mantener el flujo operativo de la plataforma.

**User Stories:**

US08: Aprobación o rechazo de solicitudes de alquiler
US13: Visualización de tarjetas resumen del panel operativo
US14: Monitoreo de alquileres activos en tiempo real
US15: Panel de alertas operativas

#### Task Flow 4: Monitoreo IoT y reacción a alertas por parte del Intermediario

Objetivo del usuario: Supervisar el estado físico de la flota en tiempo real y reaccionar de forma temprana ante lecturas anómalas de los dispositivos IoT.

**Pasos del Task Flow:**

Acceder al Dashboard operativo y visualizar el panel de alertas.

Identificar una alerta crítica (por ejemplo, temperatura fuera de rango).

Hacer clic en la alerta para navegar al detalle.

Revisar los indicadores de la máquina (temperatura, vibración, horas de motor).

Consultar el histórico IoT del último período para entender el contexto.

Abrir el panel de Monitoreo IoT para ver la ubicación GPS actual de la máquina.

Decidir la acción correctiva (contactar al Propietario o programar mantenimiento).

![Task Flow 4 - Monitoreo IoT y alertas](Resources/wireframes/wireflows/flow4.jpg)

**User Goals:**

User goal 4: Como Intermediario, quiero supervisar el estado físico de la flota en tiempo real y reaccionar ante eventos anormales.

**User Stories:**

US17: Ubicación GPS de la flota en mapa
US18: Horas de motor acumuladas por máquina
US19: Indicadores de temperatura y vibración
US20: Alertas automáticas por eventos anormales

### 4.4.3. Web Applications Mock-ups.

Inicio de sesión:

![Login Mockup](Resources/mockups/WebApplication/Login.png)

Creación de cuenta:

![Register Mockup](Resources/mockups/WebApplication/Register.png)

Catálogo de máquinas:

![Catalog Mockup](Resources/mockups/WebApplication/Catalog.png)

Detalle de máquina:

![Machine Detail Mockup](Resources/mockups/WebApplication/Machine_Detail.png)

Solicitud de alquiler:

![Request Rental Mockup](Resources/mockups/WebApplication/Request_Rental.png)

Mis solicitudes (Cliente):

![My Requests Mockup](Resources/mockups/WebApplication/My_Requests.png)

Mis alquileres (Cliente):

![My Rentals Mockup](Resources/mockups/WebApplication/My_Rentals.png)

Detalle del alquiler:

![Rental Detail Mockup](Resources/mockups/WebApplication/Rental_Detail.png)

Dashboard del Propietario:

![Owner Dashboard Mockup](Resources/mockups/WebApplication/Owner_Dashboard.png)

Mis máquinas (Propietario):

![My Machines Mockup](Resources/mockups/WebApplication/My_Machines.png)

Registro de nueva máquina (Propietario):

![Register Machine Mockup](Resources/mockups/WebApplication/Register_Machine.png)

Dashboard del Intermediario:

![Broker Dashboard Mockup](Resources/mockups/WebApplication/Broker_Dashboard.png)

Bandeja de solicitudes (Intermediario):

![Requests Inbox Mockup](Resources/mockups/WebApplication/Requests_Inbox.png)

Monitoreo IoT:

![IoT Monitoring Mockup](Resources/mockups/WebApplication/IoT_Monitoring.png)

Ficha IoT de máquina (Intermediario):

![IoT Machine Detail Mockup](Resources/mockups/WebApplication/IoT_Machine_Detail.png)

### 4.4.4. Web Applications User Flow Diagrams.

User Flow 1:

Relacionado con el User Goal 1: Como Cliente, quiero encontrar y solicitar una máquina disponible para un rango de fechas específico.

En esta etapa el Cliente accede al catálogo, aplica filtros, explora el detalle de una máquina y envía una solicitud de alquiler. El sistema valida la disponibilidad de fechas y, si no hay conflicto, registra la solicitud en estado "Pendiente" para la revisión del Intermediario. En caso de conflicto, se muestra un mensaje de error y se sugieren fechas alternativas.

![User Flow 1 - Solicitud de alquiler](Resources/mockups/userflows/flow1.png)

User Flow 2:

Relacionado con el User Goal 2: Como Propietario, quiero publicar mi máquina en el catálogo con toda su información para que los Clientes puedan solicitarla.

En esta etapa el Propietario completa el wizard de tres pasos para registrar una máquina: información básica, especificaciones técnicas, y fotos junto con tarifa. El sistema valida los campos obligatorios en cada paso y, al confirmar, crea la máquina en estado "Disponible" y la publica inmediatamente en el catálogo.

![User Flow 2 - Registro de máquina](Resources/mockups/userflows/flow2.png)

User Flow 3:

Relacionado con el User Goal 3: Como Intermediario, quiero evaluar y procesar las solicitudes de alquiler pendientes de forma eficiente para mantener el flujo operativo de la plataforma.

En esta etapa el Intermediario accede al Dashboard operativo, identifica las solicitudes pendientes mediante el panel de alertas o navegando directamente a la sección de Solicitudes, y revisa el detalle de cada una para aprobarla o rechazarla. Al aprobar, el sistema cambia el estado de la solicitud a "Aprobada" y la máquina asociada pasa a estado "Alquilada", activando el ciclo del alquiler. En caso de rechazo, el Intermediario debe ingresar un motivo que se notifica automáticamente al Cliente. Este flujo permite mantener el control operativo de la plataforma asegurando que cada solicitud sea evaluada y procesada en tiempo oportuno.

![User Flow 3 - Aprobación de solicitud](Resources/mockups/userflows/flow3.png)

User Flow 4:

Relacionado con el User Goal 4: Como Intermediario, quiero supervisar el estado físico de la flota en tiempo real y reaccionar ante eventos anormales.

En esta etapa el Intermediario detecta una alerta automática generada por una lectura IoT fuera de rango, revisa el detalle de la máquina afectada, consulta su histórico y decide la acción correctiva apropiada (contactar al Propietario o programar mantenimiento).

![User Flow 4 - Monitoreo IoT y respuesta a alertas](Resources/mockups/userflows/flow4.png)

### 4.5. Web Applications Prototyping.

En esta sección se presenta el prototipo navegable de alta fidelidad construido en Figma, que convierte los mock-ups estáticos en una experiencia interactiva que permite validar los flujos diseñados antes de iniciar el desarrollo frontend.

El prototipo cubre los cuatro flujos críticos definidos en la sección 4.4.2 (Task Flows):

1. **Solicitud de alquiler por parte del Cliente** — recorrido desde el Login hasta el envío exitoso de una solicitud en la vista de Mis Solicitudes.
2. **Registro de una nueva máquina por parte del Propietario** — recorrido desde el Dashboard del Propietario hasta la publicación de una máquina en el catálogo.
3. **Aprobación y cierre de alquiler por parte del Intermediario** — recorrido desde el Dashboard operativo pasando por la bandeja de solicitudes hasta el detalle del alquiler.
4. **Monitoreo IoT y reacción a alertas por parte del Intermediario** — recorrido desde el panel de Monitoreo IoT hasta la ficha IoT de una máquina específica.

Cada flujo conecta las pantallas relevantes (mock-ups de la sección 4.4.3) mediante transiciones configuradas en Figma: _Smart Animate_ para cambios dentro de una misma pantalla (tabs, modales, selección de opciones) y _Dissolve_ para cambios de pantalla completa. Las acciones críticas como el envío de una solicitud o la aprobación de un alquiler incluyen un delay corto para simular la latencia de una llamada real al backend.

El prototipo se organiza en el archivo Figma en tres zonas principales: una página con los mock-ups del Landing Page, una con los mock-ups de la Web Application para los tres roles, y una con los Prototype Flows donde se definen los Starting Points de cada recorrido. Cada flujo cuenta con un Starting Point nombrado que produce una URL compartible en modo Presentation View para recopilar feedback de stakeholders sin requerir cuenta Figma.

Los enlaces de los cuatro prototipos navegables y el video walkthrough se documentan a continuación:

Enlace del prototipo Figma: https://www.figma.com/proto/Ly5rB0Aa4PFKAnZ9bbKiGO/MineTrack---Design?node-id=23-29217&p=f&t=EikasJ2GamVE3M3j-1&scaling=min-zoom&content-scaling=fixed&page-id=23%3A27100&starting-point-node-id=23%3A29217

### 4.6.1 Design-Level EventStorming

Se realizó una sesión de Design-Level EventStorming para identificar los principales eventos, actores y reglas de negocio del sistema MineTrack, considerando la interacción entre usuarios y sensores IoT.

#### Evidencia del Event Storming

![EventStorming](Resources/eventstorming-mineTrack.png)

### 4.6.2 Software Architecture Context Diagram

En esta sección se presenta el diagrama de contexto del sistema MineTrack, el cual ilustra la interacción del sistema con actores y sistemas externos. El sistema se representa en el centro, rodeado por los usuarios y servicios con los que interactúa.

MineTrack interactúa con tres actores principales:

User (Usuario): Son los usuarios finales que monitorean el estado de la maquinaria, visualizan información y reciben alertas y reportes.

Maintenance Company (Empresa de Mantenimiento): Encargada de programar y gestionar el mantenimiento, revisar historiales y monitorear las condiciones de la maquinaria.

Administrator (Administrador): Responsable de gestionar la configuración del sistema, usuarios y permisos de la plataforma.

Además, MineTrack interactúa con sistemas externos:

IoT Sensors (Sensores IoT): Proveen datos en tiempo real como temperatura, vibración y horas de uso de la maquinaria.

Database System (Sistema de Base de Datos): Almacena la información del sistema, datos de maquinaria y registros de usuarios.

Notification Service (Servicio de Notificaciones): Envía alertas y notificaciones a los usuarios mediante diferentes canales.

El diagrama muestra cómo MineTrack integra estos componentes para ofrecer una solución completa de monitoreo y gestión de maquinaria.
![Context Diagram](Resources/context-diagram.png)

### 4.6.3 Software Architecture Container Diagrams

En esta sección se presenta el diagrama de contenedores del sistema MineTrack, el cual describe la estructura interna del sistema y cómo se distribuyen las responsabilidades entre sus principales componentes.

El sistema MineTrack está compuesto por los siguientes contenedores:

- **Web Application (Angular):** Interfaz de usuario que permite a los usuarios registrarse, visualizar el estado de la maquinaria, consultar reportes y gestionar información del sistema.

- **API REST (Spring Boot):** Componente backend que gestiona la lógica de negocio, procesa las solicitudes provenientes de la aplicación web y coordina la comunicación con los demás componentes del sistema.

- **Database (MySQL):** Sistema de almacenamiento que guarda la información relacionada con la maquinaria, usuarios y registros generados por el sistema.

Además, el sistema interactúa con componentes externos:

- **IoT Sensors:** Proveen datos en tiempo real como temperatura, vibración y horas de uso de la maquinaria, los cuales son enviados al API REST para su procesamiento.

- **Notification Service:** Servicio externo encargado de enviar alertas y notificaciones a los usuarios mediante correo electrónico o SMS.

En cuanto a la comunicación entre los contenedores, la aplicación web se comunica con el API REST mediante protocolos seguros (HTTPS). El API REST se encarga de leer y escribir información en la base de datos, así como de enviar notificaciones a través del servicio externo cuando se detectan eventos relevantes.

![Container Diagram](Resources/container-diagram.png)

### 4.6.4 Software Architecture Components Diagrams

En esta sección se presenta el diagrama de componentes correspondiente al contenedor API REST (Spring Boot).  
El diagrama describe la estructura interna del backend, identificando los principales componentes
(controladores, servicios y repositorios), sus responsabilidades y las interacciones entre ellos,
así como con sistemas externos.

![Component Diagram](Resources/component-diagram-api-rest..png)

4.7 Software Object-Oriented Design

4.7.1 Class Diagrams

#### Context: User Management

En el contexto de gestión de usuarios se modelan las clases encargadas de administrar el acceso y la interacción de los usuarios dentro de la plataforma. 

La clase `User` representa a los usuarios del sistema, incluyendo sus datos personales y operaciones como registro, inicio de sesión y actualización de perfil. La clase `UserSession` permite gestionar las sesiones activas, garantizando el control de acceso mediante tokens y tiempos de expiración.

Asimismo, se incluyen las clases `Role` y `Permission`, las cuales permiten definir distintos niveles de acceso dentro del sistema, asegurando que cada usuario pueda realizar únicamente las acciones autorizadas. La clase `Company` representa las organizaciones que utilizan la plataforma, como distribuidores de maquinaria o empresas de mantenimiento.

Finalmente, los servicios `AuthenticationService` y `AuthorizationService` permiten validar credenciales y controlar permisos, garantizando la seguridad del sistema.

Este contexto es fundamental para asegurar el acceso controlado y seguro a la plataforma.

![User Management Diagram](Resources/user-management.png)

##### Context: Machinery Sales and Management

En este contexto se modelan las clases encargadas de la gestión del catálogo de maquinaria y el proceso de venta dentro de la plataforma.

La clase `Machinery` representa los equipos disponibles, incluyendo sus características principales como modelo, precio y estado. Estas maquinarias se organizan mediante la clase `Catalog` y se clasifican a través de `Category`.

El proceso de compra se gestiona mediante las clases `Order` y `OrderItem`, las cuales permiten registrar pedidos realizados por los clientes. La clase `Customer` representa a los usuarios que adquieren los equipos.

Además, se incluyen las clases `Payment` e `Invoice`, que permiten gestionar los pagos y la generación de comprobantes, completando así el ciclo de venta.

Este contexto permite centralizar la gestión comercial de la maquinaria, facilitando la compra y administración de los equipos.

![Machinery Sales Diagram](Resources/machinery-sales.png)

#### Context: IoT Monitoring and Maintenance

En este contexto se modela la supervisión del estado de la maquinaria mediante la integración con dispositivos IoT.

La clase `Machinery` se relaciona con múltiples `Sensor`, los cuales recopilan datos en tiempo real como temperatura, vibración y condiciones operativas. Estos datos son representados por la clase `SensorData`.

A partir del análisis de estos datos, se generan alertas mediante la clase `Alert`, permitiendo detectar fallas o condiciones críticas. Asimismo, la clase `Maintenance` permite gestionar las actividades de mantenimiento necesarias para cada equipo, mientras que `MaintenancePlan` define la planificación de dichas actividades.

El sistema también incluye componentes como `IoTGateway`, encargado de recibir los datos de los sensores, y `Dashboard`, que permite visualizar la información en tiempo real. Además, `NotificationService` se encarga de enviar alertas a los usuarios, y `RecommendationService` genera sugerencias de mantenimiento basadas en los datos recopilados.

Este contexto permite mejorar la eficiencia operativa, reducir fallas y optimizar el mantenimiento de la maquinaria.

![IoT Monitoring Diagram](Resources/iot-monitoring.png)
