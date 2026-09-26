# TP_3_UI_UX-2026-


(Para las act. 1-4, no se decidió comentar, por el hecho de simplemente funcionar con html y tener objetivos sencillos)
(De la 5 hasta la 14, solamente se comento el código .html y .scc. Ya que no se tomaron decisiones de diseño que se crean importantes)

Por último de la act. 15 en adelante, se colocaran las decisiones que se tomaron, aparte de también haberse comentado el código.

Actividad 15: 
Diseño responsivo con Media Queries: Se partió del layout grid de la Actividad 10 (header, sidebar, contenido principal y footer) y se adaptó con un enfoque desktop-first, ya que ese ejercicio base fue pensado primero para pantallas de escritorio. Se definieron dos breakpoints: 
-En pantallas menores a 768px el sidebar se oculta y el grid pasa a una sola columna (header, contenido principal y footer apilados).
-En pantallas menores a 480px se reducen el padding y el gap para mantener una transición fluida sin overflow horizontal. Se usó box-sizing: border-box y max-width en el contenedor .sitio para evitar desbordes en anchos chicos.
