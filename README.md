# TP_3_UI_UX-2026-

Se completaron todas las actividades 1-20.

(Para las act. 1-4, no se decidió comentar, por el hecho de simplemente funcionar con html y tener objetivos sencillos)
(De la 5 hasta la 14, solamente se comento el código .html, .scc u ambos. Ya que no se tomaron decisiones de diseño que se crean importantes)

Por último de la act. 15 en adelante, se colocaran las decisiones que se tomaron, aparte de también haberse comentado el código de c/u:


Actividad 15: 
Diseño responsivo con Media Queries: Se partió del layout grid de la Actividad 10 (header, sidebar, contenido principal y footer) y se adaptó con un enfoque desktop-first, ya que ese ejercicio base fue pensado primero para pantallas de escritorio. Se definieron dos breakpoints: 
-En pantallas menores a 768px el sidebar se oculta y el grid pasa a una sola columna (header, contenido principal y footer apilados).
-En pantallas menores a 480px se reducen el padding y el gap para mantener una transición fluida sin overflow horizontal. Se usó box-sizing: border-box y max-width en el contenedor .sitio para evitar desbordes en anchos chicos.


Ejercicio 16:
Decidí combinar las dos animaciones con @keyframes en la misma página(por razones de práctica): 
-Un spinner de carga (rotación infinita con animation-timing-function: linear) y;
-Una tarjeta con efecto fade-in + slide-up que se ejecuta una sola vez al cargar. 
Se usaron las propiedades animation-duration, animation-timing-function y animation-iteration-count por separado, en lugar de la propiedad abreviada animation, para que cada requisito quede explícito y sea más fácil de identificar en el código.


Ejercicio 17:
El menú de navegación se resolvió con el truco del checkbox oculto (input type='checkbox' + label asociado). 
El ícono de despliegue(conocido como "hamburguesa", siendo que decidí definirlo de otra forma) solo se muestra en pantallas menores a 768px mediante una media query; en pantallas grandes el menú se mantiene siempre visible en formato horizontal. 


Ejercicio 18:
La galería tipo mosaico se construyó con CSS Grid usando: 
-grid-template-columns: repeat(auto-fill, minmax(180px, 1fr)) para que la cantidad de columnas se ajuste automáticamente al ancho disponible.
-grid-auto-flow: dense para que los elementos más chicos rellenen los huecos que deja el elemento destacado (que ocupa 2 columnas y 2 filas mediante grid-column/grid-row: span). 


Ejercicio 19:
El formulario multi-step se resolvió con el truco de radio buttons ocultos (en lugar de :target), ya que permite pasar de un paso a otro usando simplemente labels como botones 'Siguiente' y 'Atrás'. 
La validación visual se implementó únicamente con las pseudo-clases nativas :required, :invalid y :valid, mostrando bordes rojos o verdes según el estado del campo. Por lo tanto, los campos obligatorios aparecen en rojo antes de ser completados, ya que :invalid se activa apenas el campo está vacío.


Ejercicio 20:
Se combinó Flexbox (navbar y carrusel de testimonios) con CSS Grid (sección de servicios) sobre una estructura HTML semántica (header, main, section, footer). 
Se usaron variables CSS en :root para colores, espaciados y transiciones, reutilizadas en toda la hoja de estilos. 
La navbar es fija (position: fixed) y se activó scroll-behavior: smooth para la navegación entre secciones mediante anclas. 
La sección hero incorpora una imagen de fondo y una animación de aparición con @keyframes (fade-in + slide-up) al cargar. 
Los testimonios se maquetaron como un carrusel simple con overflow-x: auto y scroll-snap-type: x mandatory. 
Se definieron dos breakpoints (768px y 480px) con enfoque desktop-first, ajustando la navbar a columna, el grid de servicios a una sola columna y el ancho de las tarjetas de testimonios, evitando overflow horizontal en cualquier tamaño de pantalla. 
