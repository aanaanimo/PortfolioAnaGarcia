# Portfolio Web Expandible — Ana García

## ¿Qué es este proyecto?

Este proyecto es una **plantilla de portfolio web personal**, pensada como una base que se pueda **reutilizar y ampliar con el tiempo**. Aunque ahora mismo está enfocada en mí (mi nombre, mi perfil y mis proyectos), la idea no es que sea un portfolio cerrado, sino una **estructura base** que se pueda adaptar fácilmente a otros perfiles creativos.

El contenido que aparece en la web es en gran parte **semi-inventado**, y está ahí a modo de ejemplo. La intención es que cualquier persona que vea el proyecto entienda qué tipo de información puede incluir, cómo se organizan los proyectos y qué posibilidades tiene la plantilla si se sigue desarrollando.

Actualmente hay **tres proyectos**, representados mediante **tarjetas**, que luego se amplían a una vista más detallada. Esta estructura no está limitada a tres: se pueden añadir más tarjetas y más proyectos sin cambiar la lógica general del código, simplemente duplicando componentes.

---

## Intención del diseño

Desde el principio quise que no fuera el típico portfolio neutro. Me interesaba crear algo con una **estética muy marcada**, que rompiera un poco con lo puramente digital.

Por eso:

- El **color verde lima** es el eje visual del proyecto.
- El fondo con cuadrícula recuerda a un entorno técnico, pero tratado de forma más gráfica.
- La tipografía manuscrita se usa en títulos concretos para **humanizar el diseño** y romper con lo excesivamente limpio o corporativo.

La idea es que visualmente tenga personalidad, pero sin dejar de ser funcional y claro.

---

## HTML semántico y estructura de la web

El proyecto está construido con **HTML5 semántico**, no solo para que “funcione”, sino para que tenga sentido a nivel estructural.

Uso etiquetas como:

- `<header>` para la cabecera
- `<nav>` para la navegación
- `<main>` para el contenido principal
- `<section>` para dividir bloques de contenido
- `<article>` para cada proyecto
- `<footer>` para el cierre de la web

Esto es importante porque el HTML no solo sirve para mostrar cosas en pantalla, sino también para **explicar qué es cada cosa**. Gracias a esto, la web es más fácil de leer para navegadores, buscadores y lectores de pantalla, y también más fácil de mantener y ampliar en el futuro.

Este enfoque está muy relacionado con la **Web Semántica**, ya que la estructura del código aporta información sobre el contenido, no solo sobre su apariencia.

---

## Enfoque Mobile First

El diseño del proyecto sigue una estrategia **Mobile First**. Esto significa que el primer diseño que se plantea es el de móvil, y a partir de ahí se va adaptando a pantallas más grandes.

En móvil:

- Todo el contenido va en una sola columna.
- Las tarjetas se apilan verticalmente.
- Los tamaños de texto y los espacios están pensados para pantallas pequeñas.

Una vez que eso funciona bien, se añaden mejoras para tablet y escritorio. Este enfoque me ha ayudado a no complicarme desde el principio y a asegurar que la web es usable en cualquier dispositivo.

---

## Diseño responsive y Media Queries

Para que la web sea responsive he utilizado varias técnicas combinadas.

### Viewport

En el HTML se define el viewport, lo que permite que la web se adapte correctamente al tamaño del dispositivo desde el inicio.

### Media Queries

Las **Media Queries** son clave en el proyecto. Gracias a ellas, el diseño cambia según el ancho de pantalla:

- Se reorganizan las tarjetas
- Cambia la distribución del grid
- Se ajustan márgenes y espacios

No hay un único layout fijo, sino que el diseño responde al contexto del dispositivo.

### Clamp()

Uso `clamp()` para definir tamaños de texto flexibles. Esto me permite asegurar que el texto no se quede ni demasiado pequeño ni demasiado grande, adaptándose al tamaño de la pantalla de forma fluida.

### Grid y Flexbox

- **CSS Grid** lo utilizo para estructurar el layout general, trabajando con filas y columnas.
- **Flexbox** lo uso dentro de componentes concretos, como tarjetas o bloques de contenido, para alinear y distribuir elementos.

Ambos sistemas me permiten crear un diseño ordenado y adaptable sin depender de valores fijos.

---

## Tipo de web

Este proyecto es una **Web 1.0**, ya que no tiene backend ni base de datos. Es una web unidireccional: el contenido va del servidor al usuario, sin interacción avanzada como comentarios, usuarios o formularios conectados a un servidor.

Todo el trabajo se centra en **frontend**, que es justo el objetivo del proyecto.

---

## Lenguajes y tecnologías utilizadas

- **HTML5** para la estructura
- **CSS3** para estilos, layout y responsive
- **JavaScript** para interacciones
- **Markdown** para la documentación (README)

---

## Protocolo, URL, URI y servidor

La web se sirve mediante **HTTPS**, lo que significa que la comunicación entre el navegador y el servidor está cifrada. El puerto utilizado es el **443**, que es el estándar para HTTPS.

- La **URL** es la dirección completa de la web.
- La **URI** identifica recursos concretos dentro de la página, como los identificadores que aparecen después del `#`.

El proyecto está publicado usando **GitHub Pages**, por lo que el servidor web es GitHub.

---

## Git y control de versiones

Durante todo el desarrollo he utilizado **Git** para llevar un control de versiones. Esto me permite:

- Guardar cambios
- Volver atrás si algo se rompe
- Tener el proyecto organizado por versiones

El repositorio está alojado en **GitHub**, lo que además facilita el despliegue de la web.

---

## APIs, CDN y recursos externos

El proyecto utiliza recursos externos como:

- **Google Fonts**
- **ImageKit.io**

Estos servicios funcionan mediante **APIs**, que permiten que mi proyecto se comunique con otros servicios. ImageKit además actúa como un **CDN**, lo que mejora el rendimiento al servir imágenes desde servidores optimizados para contenido multimedia.

---

## Animaciones y GSAP

He trabajado con **GSAP**, una librería de JavaScript para animaciones. La idea era enriquecer la experiencia visual del portfolio y hacerlo más dinámico.

No todas las animaciones previstas han llegado a implementarse del todo, pero el proyecto está preparado para seguir ampliándose en ese sentido.

---

## Modal de proyecto (no implementado)

Una de las cosas que me habría gustado implementar es un **modal para los proyectos**. La idea era que, al hacer clic en una tarjeta, se abriera un modal encima de la página con más información del proyecto (imágenes, texto ampliado, detalles técnicos, etc.), sin necesidad de cambiar de página.

Este tipo de modal es una solución bastante óptima a nivel de experiencia de usuario, ya que:

- Mantiene al usuario en el mismo contexto
- Evita recargas o saltos bruscos
- Permite ampliar contenido sin romper la navegación

No he conseguido implementarlo correctamente porque la parte de **JavaScript se me ha complicado**, y preferí no forzar una solución que no funcionara bien.

---

## Cursor personalizado (estrella)

Otra idea que no he podido cerrar del todo es la del **cursor personalizado en forma de estrella**. La intención era que el cursor dejara un pequeño rastro visual, como una estrella o shooting star, para reforzar el carácter visual del proyecto.

Aunque he trabajado el CSS y parte del JavaScript, no he conseguido que funcione de forma estable, así que se ha quedado como una idea a mejorar en futuras versiones.

---

## Conclusión personal

Este proyecto no pretende ser perfecto ni definitivo, sino una **base sólida** sobre la que seguir construyendo. Me ha servido para entender mejor cómo estructurar una web, cómo hacerla responsive, cómo usar HTML semántico y cómo pensar un diseño que pueda crecer con el tiempo.

También me ha ayudado a identificar mis límites actuales, sobre todo en JavaScript, y a tener claro qué partes me gustaría mejorar o ampliar en el futuro.

Encuentra aqui el proyecto desplegado:[https://aanaanimo.github.io/PortfolioAnaGarcia/](https://aanaanimo.github.io/PortfolioAnaGarcia/)
