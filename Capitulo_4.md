## Capítulo IV: Product Design

### 4.1. Style Guidelines.

En esta sección se sientan las bases visuales y de comunicación comunes para la experiencia de MineTrack. Se define el repositorio de estilos compartido por Landing Page y Web Application, con el fin de mantener una presentación consistente entre pantallas, roles y dispositivos.

### 4.1.1. General Style Guidelines.

### **Colores**

![Colors](Resources/style/Colors.png)

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

![MineTrack Logo](Resources/style/Logo.png)

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
