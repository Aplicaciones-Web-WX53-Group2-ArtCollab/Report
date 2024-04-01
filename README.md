# Capítulo III: Requirements Specification
<hr>

## 3.1. To-Be Scenario Mapping.
<hr>

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
<th>User Story ID</th>
<th>Título</th>
<th>Descripción</th>
<th>Criterios de Aceptación</th>
<th>Relación Epic ID</th>
</tr>
<tr class="odd">
<th>US01</th>
<th>Inicio de Datos</th>
<th>Como usuario quiero registrarme e iniciar sesión</th>
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
<th>EP01</th>
</tr>
<tr class="header">
<th>US02</th>
<th>Asignación de rol</th>
<th>Como usuario quiero poder asignarme un rol para poder visualiza</th>
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
<th>EP01</th>
</tr>
<tr class="odd">
<th>US03</th>
<th>Escribe tus libros</th>
<th>Como escritor quiero una herramienta para escribir mis libros</th>
<th><p>Escenario 1: Hoja de texto</p>
<p>Dado que el escritor se encuentra en la página principal</p>
<p>Cuando le dé clic en “crear”</p>
<p>Entonces se le abrirá una página aparte de escritora</p>
<p>Escenario 2: Herramientas</p>
<p>Dado que el escritor se encuentra en el apartado de creación</p>
<p>Cuando le dé clic en empezar</p>
<p>Entonces se le mostrará las diversas herramientas de fuente, estilos
y edición</p>
<p>Escenario 3:</p>
<p>Dado que el escritor terminó la obra</p>
<p>Cuando le dé clic en publicar</p>
<p>Entonces la obra será publicada</p></th>
<th>EP02</th>
</tr>
<tr class="header">
<th>US04</th>
<th>Comunidad</th>
<th>Como Usuario quiero estar en una comunidad para poder expresarme
libremente</th>
<th><p>Escenario 1: Comunidad</p>
<p>Dado que el escritor se encuentra en la página principal</p>
<p>Cuando le de clic a Comunidad</p>
<p>Entonces se le mostrará la comunidad dependiendo su rol</p>
<p>Escenario 2: Publicaciones</p>
<p>Dado que el escritor se encuentra en la página de comunidad</p>
<p>Cuando le dé clic a Publicaciones</p>
<p>Entonces podrá interactuar, publicar y comentar estas.</p>
<p>Escenario 3: Chats</p>
<p>Dado que el escritor se encuentre en la página de comunidad habrá un
apartado de chats</p>
<p>Cuando le dé clic al botón chatear</p>
<p>Entonces entrará a un chat general donde podrá chatear con otras
personas en público o privado</p></th>
<th>EP01</th>
</tr>
<tr class="odd">
<th>US05</th>
<th>Colaborar otros escritores</th>
<th>Como escritor quiero colaborar con otros escritores para escribir
obras</th>
<th><p>Escenario 1: Comunidad</p>
<p>Dado que el escritor se encuentra en la página principal</p>
<p>Cuando le dé clic a Comunidad</p>
<p>Entonces se le va a redirigir a una pestaña diferente</p>
<p>Escenario 2: Comunidad</p>
<p>Dado que el escritor se encuentra en la pestaña comunidad
(escritores) podrá visualizar las publicaciones y los diversos rankings
de escritores.</p>
<p>Cuando elija alguno y le de conectar</p>
<p>Entonces se le abrirá un chat donde el otro escritor le responderá
primero</p>
<p>Escenario 3: Conectar</p>
<p>Dado que el escritor se encuentra en el chat con otro escritor</p>
<p>Cuando ambos hayan llegado a un acuerdo, en el chat darán clic en
colaborar</p>
<p>Entonces ambos escritores tendrán acceso a una obra elegida o
creada.</p></th>
<th>EP02</th>
</tr>
<tr class="header">
<th>US06</th>
<th>Ilustradores</th>
<th>Como escritor deseo que mis obras sean ilustradas</th>
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
<th></th>
</tr>
<tr class="odd">
<th>US07</th>
<th>Destaca tus libros</th>
<th>Como escritor quiero destacar mis libros</th>
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
<th>EP02</th>
</tr>
<tr class="header">
<th>US08</th>
<th>Reparto por Ingresos publicitarios</th>
<th>Como escritor quiero generar ingresos</th>
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
<th>EP02</th>
</tr>
<tr class="odd">
<th>US09</th>
<th></th>
<th></th>
<th></th>
<th></th>
</tr>
<tr class="header">
<th>US10</th>
<th></th>
<th></th>
<th></th>
<th></th>
</tr>
<tr class="odd">
<th>US11</th>
<th></th>
<th></th>
<th></th>
<th></th>
</tr>
</thead>
<tbody>
</tbody>
</table>
<hr>

## 3.3. Impact Mapping.
<img src="https://github.com/Open-Source-SW54-Group-3-ArtCollab/Report/blob/develop/assets/images/Impactmap1.png?raw=true" alt="Impact Map 1" style="margin-bottom: 5px;" width="1000"/>
<img src="https://github.com/Open-Source-SW54-Group-3-ArtCollab/Report/blob/develop/assets/images/Impactmap2.png?raw=true" alt="Impact Map 2" style="margin-bottom: 5px;" width="1000"/>
<img src="https://github.com/Open-Source-SW54-Group-3-ArtCollab/Report/blob/develop/assets/images/Impactmap3.png?raw=true" alt="Impact Map 3" style="margin-bottom: 5px;" width="1000"/>
<hr>

## 3.4. Product Backlog.
