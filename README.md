# Capítulo III: Requirements Specification
<hr>

## 3.1. To-Be Scenario Mapping.
<hr>
<img src="https://github.com/Aplicaciones-Web-WX53-Group2-ArtCollab/Report/blob/develop/assets/To-be-map/To-be-Autor.png">
<img src="https://github.com/Aplicaciones-Web-WX53-Group2-ArtCollab/Report/blob/develop/assets/To-be-map/To-be-ilustrador.png">
<img src="https://github.com/Aplicaciones-Web-WX53-Group2-ArtCollab/Report/blob/develop/assets/To-be-map/To-be-lector.png">



## 3.2. User Stories
<table>
<colgroup>
<col style="width: 11%" />
<col style="width: 15%" />
<col style="width: 21%" />
<col style="width: 39%" />
<col style="width: 11%" />
</colgroup>
<thead>
<tr class="header">
<th>Epic / Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relación Epic ID</th>
</tr>
<tr class="odd">
<th>E1-US01</th>
<th>Inicio de Datos</th>
<th>Como usuario quiero registrarme e iniciar sesión para explorar la
páginas</th>
<th><p>Escenario 1: Acceso al registro de datos.</p>
<p>Dado que me encuentro en la página de inicio</p>
<p>Cuando el usuario le da clic en registrarse</p>
<p>Entonces la página le pedirá que ingrese sus datos (correo,
contraseña, etc.)</p>
<p>Escenario 2: Me registro con el código de verificación:</p>
<p>Dado que envié mis datos, la página me pidió un enlace de
verificación enviado a mi correo</p>
<p>Cuando el usuario le da clic al enlace</p>
<p>Entonces se le redirige a la página de iniciar sesión</p>
<p>Escenario 3: Inicio sesión</p>
<p>Dado que me encuentro en la página de iniciar sesión</p>
<p>Cuando el usuario coloque sus datos y le dé en iniciar sesión</p>
<p>Entonces la página le redirige a la pantalla principal con el usuario
ya logueado</p></th>
<th>1</th>
</tr>
<tr class="header">
<th>E1-US02</th>
<th>Asignación de rol</th>
<th>Como usuario quiero poder asignarle un rol para poder visualizar la
página</th>
<th><p>Escenario 1: Ingreso a la página luego del inicio de sesión</p>
<p>Dado que el usuario se encuentra logueado en la página</p>
<p>Cuando se desplace le aparecerá una ventana para que elija un rol
(Escritor, Ilustrador, Lector).</p>
<p>Entonces el usuario elije el rol</p>
<p>Escenario 2: Actualización de Datos</p>
<p>Dado que el usuario escogió el rol</p>
<p>Cuando se le asigne el rol le pedirá una actualización de Datos</p>
<p>Entonces el usuario llenará los datos que le piden Dependiendo el Rol
que haya escogido</p>
<p>Escenario 3: Actualización de página y herramientas</p>
<p>Dado que el usuario terminó la actualización de datos</p>
<p>Cuando se desplace se le dirigiera a la página principal</p>
<p>Entonces se le mostrará la página principal actualizada dependiendo
al rol que haya escogido con nuevas herramientas.</p></th>
<th>1</th>
</tr>
<tr class="odd">
<th>E2-US03</th>
<th>Sube tus libros</th>
<th>Como escritor quiero una plataforma para subir mis libros</th>
<th><p>Escenario 1: Hoja de texto</p>
<p>Dado que el escritor se encuentra en la página principal</p>
<p>Cuando le dé clic en “crear”</p>
<p>Entonces se le abrirá una página donde podrá subir su obra</p>
<p>Escenario 2:</p>
<p>Dado que el escritor terminó la obra</p>
<p>Cuando le dé clic en publicar</p>
<p>Entonces la obra será publicada y se verá en su portafolio</p></th>
<th>2</th>
</tr>
<tr class="header">
<th>E2-US04</th>
<th>Colaboración con Ilustradores</th>
<th>Como escritor quiero que mis obras sean ilustradas para
mejorarlas</th>
<th><p>Escenario 1: Ilustra</p>
<p>Dado que me encuentro en la pestaña de mis obras</p>
<p>Cuando le dé clic en alguna de mis obras e Ilustrar</p>
<p>Entonces se me abrirá una pestaña nueva donde habrá una sección de
ilustradores</p>
<p>Escenario 2: Escoger</p>
<p>Dado que me encuentre algún ilustrador que me guste</p>
<p>Cuando entre a su perfil y le clic en colaborar</p>
<p>Entonces se me abrirá un chat con el ilustrador</p>
<p>Escenario 3: Acuerdos</p>
<p>Dado que ambos llegaron a un acuerdo</p>
<p>Cuando le den clic al botón acuerdo en el chat</p>
<p>Entonces elegirás que obra poder darle acceso</p></th>
<th>2</th>
</tr>
<tr class="odd">
<th>E3-US05</th>
<th>Destaca tus libros</th>
<th>Como escritor quiero destacar mis libros para tener mayores
visualizaciones</th>
<th><p>Escenario 1: Sistema monetario</p>
<p>Dado que el escritor se encuentra en su perfil</p>
<p>Cuando le dé clic en monedas</p>
<p>Entonces se le abrirá un recuadro de cuantas monedas desea
comprar</p>
<p>Escenario 2: Ingreso Bancario</p>
<p>Dado que se encuentra en la parte de compra</p>
<p>Cuando ingrese sus datos bancarios y lo confirme</p>
<p>Entonces le llegara un correo de recibo y se depositaran las
monedas</p>
<p>Escenario 3: Destaca tus obras</p>
<p>Dado que el usuario se encuentra en la pestaña de sus obras</p>
<p>Cuando le clic en una obra específica y en destacar</p>
<p>Entonces se le mostrará un monto y por cuánto tiempo se destacó la
obra</p></th>
<th>3</th>
</tr>
<tr class="header">
<th>E3-US06</th>
<th>Reparto por Ingresos publicitarios</th>
<th>Como escritor quiero generar ingresos para mejorar mis libros</th>
<th><p>Escenario 1: Ingreso al programa de recompensas</p>
<p>Dado que el escritor se encuentra en su perfil</p>
<p>Cuando le dé clic al programa de ingresos</p>
<p>Entonces se le descargara una forma a llenar</p>
<p>Escenario 2: Recopilación de Datos</p>
<p>Dado que el escritor lleno los datos que le piden</p>
<p>Cuando le dé clic en enviar formulario</p>
<p>Entonces se le mostrará una recopilación de requisitos previos
(+1.000 seguidores y +50.000 vistas)</p>
<p>Escenario 3: Aceptación de Solicitud</p>
<p>Dado que el escritor recibió un correo de aceptación</p>
<p>Cuando le dé clic en aceptar</p>
<p>Entonces se le mostrará un mensaje de bienvenida donde recibirá un
50% de ingreso neto por los anuncios mostrados cuando leen la
obra</p></th>
<th>3</th>
</tr>
<tr class="odd">
<th>E5-US07</th>
<th>Ingreso por las ilustraciones</th>
<th>Como ilustrador quiero tener una compensación justa para poder
invertir en mis dibujos</th>
<th><p>Escenario 1: Acuerdo Mutuo</p>
<p>Dado que el ilustrador fue contactado por el escritor</p>
<p>Cuando ambas partes lleguen a un acuerdo se dará a una
colaboración</p>
<p>Entonces cuando se termine el trabajo acordaron un pago de manera
externa</p>
<p>Escenario 2: Fecha de Pago</p>
<p>Dado que el ilustrador terminó sus ilustraciones pendientes</p>
<p>Cuando le comente a su colaborador (Escritor)</p>
<p>Entonces se le pagará por un medio externo</p></th>
<th>5</th>
</tr>
<tr class="header">
<th>E1-US08</th>
<th>Configuracion de Perfil de Usuario</th>
<th>Como usuario quiero configurar mi perfil para satisfacer mis
gustos</th>
<th><p>Escenario 1: Ingresar al perfil</p>
<p>Dado que el usuario se encuentra en la página principal</p>
<p>Cuando le de click en su perfil</p>
<p>Entonces se le abrirá su perfil</p>
<p>Escenario 2: Configuración de perfil</p>
<p>Dado que se encuentra en su perfil</p>
<p>Cuando le de click en Configuración</p>
<p>Entonces podrá configurar su perfil en aspectos estetica, finanzas y
portafolio</p></th>
<th>1</th>
</tr>
<tr class="odd">
<th>E4-US09</th>
<th>Desbloqueo de Capítulos</th>
<th>Como usuario quiero tener acceso al contenido exclusivo de la
plataforma para ver mas capitulos</th>
<th><p>Escenario 1: Finanzas</p>
<p>Dado que el usuario se encuentra en la página principal</p>
<p>Cuando le de clic al apartado de monedas</p>
<p>Entonces se le mostrará el valor de las monedas</p>
<p>Escenario 2:Monedas</p>
<p>Dado que el usuario se encuentra en el apartado de monedas</p>
<p>Cuando elija cuántas quiere y elija el modo de pago</p>
<p>Entonces se le redirige a una pestaña de pago de su elección</p>
<p>Escenario 3: Pago</p>
<p>Dado que el usuario pago y se le depositó las monedas</p>
<p>Cuando vaya al libro a desbloquear los nuevos capítulos cuando le de
clic en desbloquear</p>
<p>Entonces se le desbloqueara el capítulo</p></th>
<th>4</th>
</tr>
<tr class="header">
<th>E4-US10</th>
<th>Dejar Comentarios</th>
<th>Como usuario quiero poder comentar las obras para ayudar con mi
feedback</th>
<th><p>Escenario 1: Escoge el libro</p>
<p>Dado que el usuario se encuentra en la página principal</p>
<p>Cuando le de click en su perfil</p>
<p>Entonces podrá visualizar sus libros recién leídos</p>
<p>Escenario 2: Reseña</p>
<p>Dado que el usuario se encuentra en el libro seleccionado</p>
<p>Cuando le de clic en el apartado de “dejar comentarios”</p>
<p>Entonces podrá escribir su comentario y publicarlo</p></th>
<th>4</th>
</tr>
<tr class="odd">
<th>E5-US11</th>
<th>Flexibilidad al ilustrar</th>
<th>Como ilustrador quiero tener flexibilidad creativa a la hora de
dibujar para tener un mejor rendimiento</th>
<th><p>Escenario 1: Añade Flexibilidad</p>
<p>Dado que el ilustrador se encuentra en la página principal</p>
<p>Cuando le de clic a perfil</p>
<p>Entonces podrá visualizar su perfil</p>
<p>Escenario 2: perfil flexible</p>
<p>Dado que el ilustrador configuración de perfil</p>
<p>Cuando le de clic en editar su perfil</p>
<p>Entonces podrá elegir editar sus preferencias por la flexibilidad
creativa</p>
<p>Escenario 3: Creatividad</p>
<p>Dado que los escritores revisen tu perfil</p>
<p>Cuando le den clic a preferencias</p>
<p>Entonces podrán visualizar tu preferencia por la flexibilidad
creativa</p></th>
<th>5</th>
</tr>
<tr class="header">
<th>E4-US12</th>
<th>Diversos géneros literarios</th>
<th>Como usuario quiero tener una gran cantidad de géneros literarios
para tenerlos a mi disposición</th>
<th><p>Escenario 1: Opción géneros</p>
<p>Dado que me encuentro en la página principal</p>
<p>Cuando le de clic a ver catalogo</p>
<p>Entonces me redirigirá al catálogo literario de la página</p>
<p>Escenario 2: Filtración</p>
<p>Dado que me encuentro en el catálogo literario de la página</p>
<p>Cuando le de clic a filtrar</p>
<p>Entonces lo podré filtrar por género, número de páginas, popularidad,
etc.</p></th>
<th>4</th>
</tr>
  <tr class="header">
<th>E5-US13</th>
<th>Información del Producto en la Página de Inicio</th>
<th>Como usuario interesado en tu producto, quiero encontrar fácilmente información relevante sobre sus características y beneficios en la página de inicio, para comprender rápidamente cómo puede ayudarme.</th>
<th><p>Escenario 1: Búsqueda deslizando.</p>
<p>Dado que el usuario ha accedido al Landing page</p>
<p>Cuando quiera visualizar las características y beneficios.</p>
<p>Entonces desliza hacia abajo 
Y encuentra la sección de características y beneficios.
</p>
<p>Escenario 2: Búsqueda por barra</p>
<pDado que el usuario ha accedido al Landing page</p>
<p>Cuando quiera visualizar las características y beneficios.</p>
<p>Entonces indica por medio de los links que quiere visualizar la sección de características y beneficios.</p></th>
<th>4</th>
</tr>
</thead>
<tbody>
</tbody>
</table>
<hr>

## 3.3. Impact Mapping.
<img src="https://raw.githubusercontent.com/Aplicaciones-Web-WX53-Group2-ArtCollab/Report/develop/assets/impact-map/Impactmap1w.png" alt="Impact Map 1" style="margin-bottom: 5px;" width="1000"/>
<img src="https://raw.githubusercontent.com/Aplicaciones-Web-WX53-Group2-ArtCollab/Report/develop/assets/impact-map/Impactmap2w.png" alt="Impact Map 2" style="margin-bottom: 5px;" width="1000"/>
<img src="https://raw.githubusercontent.com/Aplicaciones-Web-WX53-Group2-ArtCollab/Report/develop/assets/impact-map/Impactmap3w.png" alt="Impact Map 3" style="margin-bottom: 5px;" width="1000"/>
<hr>

## 3.4. Product Backlog.
https://trello.com/invite/b/XGFz58Qm/ATTId8b089f48c027b128a0df36e9f15df3c662ADF56/mi-tablero-de-trello
<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 12%" />
<col style="width: 18%" />
<col style="width: 28%" />
<col style="width: 14%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th>#Orden</th>
<th>User Story ID</th>
<th>Titulo</th>
<th>Descripcion</th>
<th>Prioridad</th>
<th>Story Points</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1</td>
<td>US01</td>
<td>Inicio de Datos</td>
<td>Como usuario quiero registrarme e ingresar mis datos para iniciar sesión</td>
<td>Alta</td>
<td>3</td>
</tr>
<tr class="even">
<td>2</td>
<td>US02</td>
<td>Asignación de rol</td>
<td>Como usuario quiero poder asignarme un rol para poder visualizar la
pagina</td>
<td>Alta</td>
<td>3</td>
</tr>
<tr class="odd">
<td>3</td>
<td>US03</td>
<td>Sube tus libros</td>
<td>Como escritor quiero una plataforma para subir mis libros</td>
<td>Alta</td>
<td>3</td>
</tr>
<tr class="even">
<td>4</td>
<td>US04</td>
<td>Colaboración con Ilustradores</td>
<td>Como escritor deseo que mis obras sean ilustradas</td>
<td>Media</td>
<td>2</td>
</tr>
<tr class="odd">
<td>5</td>
<td>US05</td>
<td>Destaca tus libros</td>
<td>Como escritor quiero destacar mis libros</td>
<td>Baja</td>
<td>1</td>
</tr>
<tr class="even">
<td>6</td>
<td>US06</td>
<td>Reparto por Ingresos publicitarios</td>
<td>Como escritor quiero generar ingresos</td>
<td>Alta</td>
<td>3</td>
</tr>
<tr class="odd">
<td>7</td>
<td>US07</td>
<td>Ingreso por las ilustraciones</td>
<td>Como ilustrador quiero tener una compensación justa</td>
<td>Alta</td>
<td>3</td>
</tr>
<tr class="even">
<td>8</td>
<td>US08</td>
<td>Configuracion de Perfil de Usuario</td>
<td>Como usuario quiero configurar mi perfil para satisfacer mis
gustos</td>
<td>Alta</td>
<td>3</td>
</tr>
<tr class="odd">
<td>9</td>
<td>US09</td>
<td>Desbloqueo de Capítulos</td>
<td>Como usuario tener acceso al contenido exclusivo de la
plataforma</td>
<td>Media</td>
<td>2</td>
</tr>
<tr class="even">
<td>10</td>
<td>US10</td>
<td>Dejar Comentarios</td>
<td>Como usuario quiero poder comentar las obras para ayudar con mi
feedback</td>
<td>Baja</td>
<td>1</td>
</tr>
<tr class="odd">
<td>11</td>
<td>US11</td>
<td>Flexibilidad al ilustrar</td>
<td>Como ilustrador quiero tener flexibilidad creativa a la hora de
dibujar</td>
<td>Media</td>
<td>2</td>
</tr>
<tr class="even">
<td>12</td>
<td>US12</td>
<td>diversos géneros</td>
<td>Como usuario quiero tener una gran cantidad de géneros literarios a
mi disposición</td>
<td>Alta</td>
<td>3</td>
</tr>
</tbody>
</table>
