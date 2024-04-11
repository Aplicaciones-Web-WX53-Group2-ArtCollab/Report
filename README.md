# Capítulo V: Product Implementation, Validation & Deployment
## 5.1. Software Configuration Management.
En la siguiente sección, detallaremos las herramientas, convenciones, referencias y configuraciones empleadas a lo largo del desarrollo del proyecto, que contribuyeron a mantener la consistencia en el trabajo realizado.

### 5.1.1. Software Development Environment Configuration.
En este apartado, se mencionarán los distintos productos de software empleados por el equipo de desarrollo, para llevar acabo las actividades relacionadas con la elaboración del proyecto.

<br>

**Project Management**
1.	Google Docs:  https://docs.google.com/

    Google Docs es una plataforma web que facilita la creación de documentos para compartir y editar de forma conjunta con otros usuarios de manera sincrónica. Se utilizo para designar, organizar y hacer un seguimiento de las actividades de trabajo, así como para establecer plazos de entrega.

2.  Google Meet: https://meet.google.com/

    Google Meet es una plataforma de videoconferencias que permite realizar videollamadas con multiples participantes y programar sesiones de trabajo. Se usó como herramienta para llevar a cabo las reuniones del equipo, facilitando la comunicación entre los integrantes del proyecto.

**Requirements Managements**
1.	Trello: https://trello.com/ 

    Es un software de gestión de proyectos, que facilita asignar y organizar las tareas a realizar. Fue utilizado para el Product Backlog.

**Product UX/UI Design** 

1.  UXPressia: https://uxpressia.com/ 

    Es una herramienta en línea que permite a los equipos de trabajo identificar y comprender los problemas, necesidades y comportamiento del usuario en relación a la solución de software que se está desarrollando, con el uso de plantillas. Se usó para la elaboración de los User Personas, Empathy Maps, Journey Maps e Impact Maps.

2.	Figma: https://www.figma.com/ 

    Figma es una herramienta de edición gráfica, en donde se puede diseñar y prototipar páginas web y aplicaciones de manera colaborativa en tiempo real. Se utilizó para crear los wireframes, mock-ups y los desktop and mobile application prototype del proyecto.

3.	Miro: https://miro.com/ 

    Es una plataforma colaborativa el cual permite crear y usar pizarras digitales personalizadas en tiempo real. Miro cuenta con distintas herramientas y plantillas para la elaboración de mapeos, diagramas, flujos de trabajo, etc. En el desarrollo del proyecto, se empleó para la creación de los As-Is y Tob-Be Scenario Maps.


**Software Development** 
1.	Landing Page
    
    Para la creación de la landing page, se utilizaron las tecnologías base del desarrollo web: HTML5, CSS3 y JavaScript. También se usó los frameworks Tailwind CSS y las librerias de Alpine.js y Swiper para facilitar el desarrollo del proyecto.

2.	Frontend Web Applications

    En el caso de la aplicación web, además de HTML5, CSS3 y JavaScript. En el caso de los componentes, se usó Prime Vue.

3. Web Services
   
    Para el servicio web, se empleó C# junto al framework Asp.Net Core. En el caso de la arquitectura, se optó por un RESTful API style.

**Software Deployment**
1. Netlify: https://www.netlify.com/

    Netlify es una plataforma de despliegue de páginas y aplicaciones web, integrandose con repositorios en Git. Se usó para hospedar la landing page del proyecto.

**Software Documentation**
1.	Vertabelo: https://vertabelo.com/

    Es una herramienta online que facilita el diseño, creación y gestión de bases de datos de manera colaborativa. Se usó para diseñar la base de datos del proyecto.

2.	LucidChart: https://lucid.app/   
    
    LucidChart es una plataforma que cuenta con opciones para la creación de diagramas, mapas mentales, flujos y más, con el uso de plantillas y tableros con edición en tiempo real. Fue utilizado en el desarrollo del diagrama de clases UML, así como los Wireflows y User Flows.

3.	Structurizr: https://www.structurizr.com/ 

    Es una plataforma que permite modelado de diagramas de arquitectura de software por medio de código. Structurizr fue utilizado para crear el modelo C4 de nuestro proyecto.     

### 5.1.2. Source Code Management.
Para el desarrollo y gestión del proyecto, fue creado una organización mediante GitHub, donde se registró todas las modificaciones realizadas a lo largo de su ciclo de vida. Este fue estructurado de la siguiente manera:
- **Organization**: https://github.com/Aplicaciones-Web-WX53-Group2-ArtCollab
- **Landing Page Repository**: https://github.com/Aplicaciones-Web-WX53-Group2-ArtCollab/LandingPage
- **Report Repository**: https://github.com/Aplicaciones-Web-WX53-Group2-ArtCollab/Report

Por otra parte, para controlar de manera efectiva los cambios en el código de la aplicación y gestionar las ramas por cada repositorio, se ha implementado GitFlow para definir y estructurar nuestro flujo de trabajo. Esto involucra la creación de dos ramas principales:
- **main**: También denominada "master", es la rama donde se encuentra la versión más estable y lista del proyecto que van a pasar a producción.
- **develop**: Es la rama donde se integra el contenido de las features. Va paralela al main. 

**Ramas auxiliares:**

- **feature**: Son las ramas donde se desarrollan las funcionalidades del proyecto. Luego de completarlas, se fusionan con la rama develop.

    El formato de nomenclatura usado para las ramas ha sido la siguiente: feature/feature-name. Aquí, "feature" indica la rama y "feature-name" el nombre de la funcionalidad que se está desarrollando. Por ejemplo, feature/log-in, se refiere a la login de la web application.

- **release**: Son las ramas donde se prepara la próxima versión del programa. En esta, se realizan las pruebas finales y se corrigen pequeños errores antes del lanzamiento definitivo. Finalizado este proceso, los cambios se fusionan con la rama develop, y luego a la rama main. 

    Se utilizó el formato "Semantic Versioning 2.0.0" para la nomenclatura de las versiones del proyecto, por ejemplo: "release/x.y.z". En donde:

    - X, Y y Z son números enteros positivos, donde cada uno se incrementa de manera numérica. 
    - X: Es la versión mayor. Cada incremento elimina la compatibilidad con versiones anteriores. Esto implica reiniciar a 0 las versiones menores y parche. 
    - Y: Es la versión menor. Cada incremento implica que se ha introducido funcionalidades que sí son compatibles con versiones anteriores. Cada vez que Y se incremente, la versión parche se reiniciará a 0.
    - Z: Es la versión parche. Solo se incrementa cuando se realizan correciones que son compatibles con versiones anteriores.

- **hotfix**: Son las ramas que se utilizan corregir errores críticos ocurridos en producción y que necesitan ser resueltos urgencia. Se originan de la rama main y se fusionan tanto con esta como con la rama develop.
</br>

**Commit Conventions**

Para el formato de los commits se siguió la estructura de Conventional Commits 1.0.0, la cual tiene la siguiente estructura:
    
    < type > [optional scope]: < description >

    [optional body]

    [optional footer(s)]

Donde:
- type: Indica el tipo de cambio realizado. Entre los valores permitidos se tienen: fix, feat, build, chore, ci, docs, style, refactor, perf, test, entre otros.
- scope: Indica dónde se realizó el commit en el proyecto. Ayuda a dar dar el contexto y alcance del cambio. Es opcional.
- description: Menciona de manera breve los cambios en el código. 
### 5.1.3. Source Code Style Guide & Conventions.
Para el desarrollo del código en HTML y CSS se decidió seguir la convención de Google HTML/CSS Style Guide. Entre las más importantes destacan:
- Se debe declarar el tipo de documento al principio del archivo con <!DOCTYPE html>.
- Indicar los meta tags 
- El elemento &lt;title&gt; se debe ubicar entre las etiquetas < head >.
- La indentación es de dos espacios a la vez.
- Usar solo minúsculas para los elementos HTML, atributos, propiedades, valores y selectores CSS.
- Encerrar entre comillas a los atributos de los elementos HTML.
- Cada elemento HTML debe tener su etiqueta de cierre.
- Evitar largas líneas de código.
- Indicar el ancho y alto de las imágenes, así como el texto alternativo (*alt*).

Para el desarrollo del código en JavaScript, se eligió la convención Google Java Style Guide. Algunas de estas convenciones son: 
- Cada línea de código debe terminar con un punto y coma (;).
- Tanto las variables como funciones deben estar en Camelcase.
- Los valores strings deben estar entre comillas simples.
- La indentación del contenido es de +2.
- Se debe evitar definir variables con la sentencia *var*. En su lugar, se recomienda *let* y *const*.

Para el desarrollo de los acceptance test con el lenguaje Gherkin, se seleccionó “Gherkin Conventions for Readable Specifications”. Entre ellas están:
- Para describir los pasos del escenario, utilizar las palabras "Give", "When", "Then" y "And".
- Indentar los pasos que comienzan con "And".
- Agregar líneas entre pasos.
- Encerrar entre comillas simples los parámetros.
- Usar un comentario separador y dos líneas en blanco entre cada escenario.

Para el desarrollo del código en C#, se seleccionó como convención estándar el Microsoft C# Coding Conventions . Entre las más importantes destacan:
- Los nombres de los paquetes deben estar en minúsculas, las clases se escriben usando UpperCamelCase y lo métodos con lowerCamelCase.
- No se tabula para las indentaciones. Debe haber 2 o 4 espacios.
- Dividir las líneas de código de más de 100 caracteres.
- Los archivos  C# deben tener el mismo nombre de la clase que contienen y está debe ser única y pública. 
- Luego de cada declaración, se hace un salto de línea.

### 5.1.4. Software Deployment Configuration.

En esta sección abordaremos el despliegue de nuestra Landing Page mediante el servicio automatizado en la nube de Netlify, a continuación se describiran los pasos para lograr el presente objeto.

<ol>
  <li> Nos aseguramos que el repositorio esté configurado correctamente, puesto a que posteriormente lo vincularemos con Netlify.

  <img src="https://raw.githubusercontent.com/Aplicaciones-Web-WX53-Group2-ArtCollab/Report/develop/assets/deploy-landingpage/repository.png">
  </li>

  <li> Accedemos a https://www.netlify.com/ e iniciamos sesión con nuestra cuenta de github, luego seleccionamos la opción de importar un proyecto existente desde git.

  <img src="https://raw.githubusercontent.com/Aplicaciones-Web-WX53-Group2-ArtCollab/Report/develop/assets/deploy-landingpage/Import-Git-Netlify.png">
  </li>

   <li>Luego seleccionamos la opción de importar desde un repositorio existente de github.

  <img src="https://raw.githubusercontent.com/Aplicaciones-Web-WX53-Group2-ArtCollab/Report/develop/assets/deploy-landingpage/Deploy-Netlify.png">
  </li>

  <li>Despues de seleccionar el repositorio de nuestra landing page, configuramos los detalles de la pagina web.
  <img src="https://raw.githubusercontent.com/Aplicaciones-Web-WX53-Group2-ArtCollab/Report/develop/assets/deploy-landingpage/configurationpng.png">
  </li>

  <li>Posteriormente seleccionamos la opción de desplegar nuestra pagina web.
  <img src="https://raw.githubusercontent.com/Aplicaciones-Web-WX53-Group2-ArtCollab/Report/develop/assets/deploy-landingpage/Configuration-Part2-Netlify.png">
  </li>


  <li> Luego de seleccionar la opción de deploy podemos visualizar el proceso de deploy en producción desde el apartado de site overview 

  <img src="https://raw.githubusercontent.com/Aplicaciones-Web-WX53-Group2-ArtCollab/Report/develop/assets/deploy-landingpage/LandingPageTools.png"/>

  </li>

   <li> Posterior al deploy, Netlify verificara si el nombre del dominio ya existe, en dicho caso asignara un nombre por defecto, sin embargo podemos modificar el nombre accediendo a las confguraciones de nuestro deploy.
  <img src="https://raw.githubusercontent.com/Aplicaciones-Web-WX53-Group2-ArtCollab/Report/develop/assets/deploy-landingpage/Configuration3.png">
  </li>

<li> Al finalizar el proceso de deploy y configuraciones, podemos visualizar todos los cambios en producción a traves de la opción deploys.
  <img src="https://raw.githubusercontent.com/Aplicaciones-Web-WX53-Group2-ArtCollab/Report/develop/assets/deploy-landingpage/LangingPageProduction.png"/>

</li>


</ol>

## 5.2. Landing Page, Services & Applications Implementation.
<hr>

### 5.2.1. Sprint 1

### 5.2.1.1. Sprint Planning 1 

<table>
     <tr> 
        <th>  Sprint #  </th>
        <th> Sprint 1 </th>
     </tr>
     <tr> 
        <td style="font-weight: bold;" colspan="7"> Sprint Planing Background</td>
     </tr>
     <tr>
       <td style="font-weight: bold;"> Date </td>
       <td> 27/03/2024 </td>
     </tr>
     <tr>
       <td style="font-weight: bold;"> Time </td>
       <td> 14:00 horas (GMT-5) </td>
     </tr>
     <tr>
       <td style="font-weight: bold;"> Location </td>
       <td> Modalidad remota a traves de la plataforma Google Meets <td>
     </tr>
      <tr>
        <td style="font-weight: bold;"> Prepared By </td>
        <td> Amaro Villanueva, Camila Elena <td>
     </tr>
        <tr>
        <td style="font-weight: bold;"> Attendees (to planning meeting) </td>
        <td> Amaro Villanueva, Camila Elena
        <br>
          Jave Diaz, Mathias Alejandro 
           <br>
         Cuadros Rodriguez, Juan Alejandro 
          <br>
         Dam Rubianes, Frida Sofia 
          <br>
         Huilca Chipana, Gustavo 
         <td>
     </tr>
     <tr>
        <td style="font-weight: bold;"> Sprint 0 Review Summary </td>
        <td> Dado que es nuestro primer sprint de desarrollo no existe 
        un review summary del sprint <td>
     </tr>
     <tr>
        <td style="font-weight: bold;"> Sprint 0 Retrospective Summary </td>
        <td> Dado a que nos encontramos en nuestro primer sprint aun no identifcamos planes de mejora.<td>
     </tr>
     <tr> 
        <td style="font-weight: bold;" colspan="7"> Sprint Goal & User Stories</td>
     </tr>
       <tr>
          <td style="font-weight: bold;"> Sprint 1 Goal</td>
          <td>  En este sprint se espera implementar el landing page con las secciones de login de inicio, hero y secciones de orientacion para el usuario, como por ejemplo footer y conocemos. En el grupo acordamos usar el framework de Tailwind.css para mejorar el maquetado y estilos de nuestra landing page, como tambien las librerias de Alpine.js y Swiper.js para facilitar la implementacion de las secciones de navbar y conocenos. Al finalizar este sprint la landing page debe estar desplegado en Netlifly y cualquier usuario deberia poder acceder y visualizar la pagina a traves de un link. <td>
      </tr>
       <tr>
          <td style="font-weight: bold;"> Sprint 1 Velocity </td>
          <td>  19  <td>
      </tr>
      <tr>
          <td style="font-weight: bold;"> Sum of Story Points </td>
          <td> 19 <td>
      </tr>


  </table>



### 5.2.1.2. Sprint backlog 1

En esta sección se muestran los tasks que se realizaron en el presente sprint y se adjunta una captura en Trello y el link del Trello.

Link de Trello: https://trello.com/invite/b/jhlFVuLG/ATTIcee340e6d0336619634d5d5ec2ff75ec31FE4502/artcollab-sprint1

<img src="https://raw.githubusercontent.com/Aplicaciones-Web-WX53-Group2-ArtCollab/Report/develop/assets/Sprint-Backlog/SprintBacklog.png"/>

<table style="width:400px; height:100px;"> 
   <tr>
      <th colspan="4"> Sprint # </th>
      <th colspan="7"> Sprint 1 </th>
   </tr>
   <tr >
     <th colspan="4"> User Story </th>
     <th colspan="7"> Work-Item /Task</th>
   </tr>
   <tr>
     <th > Id </th>
     <th colspan="3"> Title </th>
     <th> Id </th>
     <th > Title </th>
     <th> Description </th>
     <th> Estimation (Hours) </th>
     <th> Assigned To </th> 
     <th> Status (To-do / In-Process / To- Review / Done) </th>
   </tr>
     <tr>
      <th> EP1-US01 </th>
     <th colspan="3"> Barra de navegación en la Landing Page </th>
      <th> W01  </th>
     <th> Navbar Section  </th>
     <th> Implementar la navbar con direcciones a la landing page de Artcollab   </th>
     <th> 0.3  </th>
     <th> Mathias Jave </th> 
     <th> Done </th>
   </tr>
    <tr>
      <th> EP1-US01 </th>
     <th colspan="3">  Barra de navegación en la Landing Page  </th>
      <th> W02  </th>
     <th> Responsive Navbar Section </th>
     <th> Adaptar la navbar en dispositivos mobiles usando el enfoque mobile first   </th>
     <th> 0.5  </th>
     <th> Mathias Jave </th> 
     <th> Done </th>
   </tr>
    <tr>
      <th> EP1-US02 </th>
     <th colspan="3"> E1-US02 Visualización de las redes sociales mediante footer </th>
      <th> W03  </th>
     <th> Footer Section </th>
     <th> Implementar la sección footer con las direcciones a las redes sociales   </th>
     <th> 0.3  </th>
     <th> Gustavo Huilca </th> 
     <th> Done </th>
   </tr>
     <tr>
      <th> EP1-US02 </th>
     <th colspan="3"> E1-US02 Visualización de las redes sociales mediante footer </th>
      <th> W04  </th>
     <th> Responsive Footer Section </th>
     <th> Adaptar el footer en dispositivos móviles usando el enfoque mobile first   </th>
     <th> 0.3  </th>
     <th> Gustavo Huilca/Mathias Jave </th> 
     <th> Done </th>
   </tr>
     <tr>
      <th> EP1-US03 </th>
     <th colspan="3"> E1-US03  Sección de Explora </th>
      <th> W05  </th>
     <th> Explora Section </th>
     <th> Implementar la sección de explora con la información de nuestra startup   </th>
     <th> 2  </th>
     <th> Juan Cuadros </th> 
     <th> Done </th>
   </tr>
     <tr>
      <th> EP1-US04</th>
     <th colspan="3"> E1-US04 Sección Colabora</th>
      <th> W06  </th>
     <th> Colabora Section </th>
     <th> Implementar la sección Colabora con la finalidad de orientar al usuario sobre nuestros servicios   </th>
     <th> 2  </th>
     <th> Frida Dam </th> 
     <th> Done </th>
   </tr>
     </tr>
     <tr>
      <th> EP1-US05</th>
     <th colspan="3"> E1-US05 Sección Hero</th>
      <th> W07  </th>
     <th> Hero Section </th>
     <th> Implementar la sección hero donde ofrecemos una breve descripción sobre nuestra startup.   </th>
     <th> 2  </th>
     <th> Camila Amaro </th> 
     <th> Done </th>
   </tr>
   
   

  <tr>
      <th> EP1-US17</th>
     <th colspan="3"> E1-US017   Compatibilidad con diferentes dispositivos </th>
      <th> W08  </th>
     <th> Landing Page </th>
     <th> Adaptar la comptabilidad del landing page a diferentes dispositivos.   </th>
     <th> 2.5  </th>
     <th> Mathias Jave </th> 
     <th> Done </th>
   </tr>
     <tr>
      <th> EP1-U18 </th>
     <th colspan="3"> E1-US18 Accesibilidad en el Landing page</th>
      <th> W09  </th>
     <th> Landing Page </th>
     <th> Mejorar la accesibilidad en la landing page pensando en un diseño inclusivo.   </th>
     <th> 2  </th>
     <th> Camila Amaro </th> 
     <th> Done </th>
   </tr>




</table>


### 5.2.1.3. Development Evidence for Sprint Review.

<table>

 <tr>
    <th> <strong> Repository </strong> </th>
    <th> <strong> Branch </strong> </th>
    <th> <strong> Commit ID</strong> </th>
    <th> <strong> Commit Message </strong> </th>
     <th> <strong> Commit Message (Body) </strong> </th>
     <th> <strong> Commited on (Date) </strong> </th>
 </tr>

  <tr>
   <th> LandingPage </th> 
   <th> develop </th>
   <th> d924bdda94369294382c3fd7a692a9befb5bd0a3 </th>
   <th> Initial commit </th>
   <th> </th>
   <th> 01/04/2024 </th>
  </tr>


  <tr>
   <th> LandingPage </th> 
   <th> develop </th>
   <th> 013506e726ab3a8459ed2a5dd010d7965519c8cf </th>
   <th> feat: add files via commit </th>
   <th> </th>
   <th> 01/04/2024 </th>
  </tr>

   <tr>
   <th> LandingPage </th> 
   <th> develop/login-landingpage </th>
   <th> c763e02a7420fe8eed7f87eab02b0cfb90300f5d </th>
   <th> fix: scroll screen bug fixed </th>
   <th> </th>
   <th> 02/04/2024 </th>
  </tr>

   <tr>
   <th> LandingPage </th> 
   <th> develop </th>
   <th> 8e8522d6c8912ab83d7d181ea666d8fe6e938d5b </th>
   <th> feat: Added hero image to assets </th>
   <th> </th>
   <th> 04/04/2024 </th>
  </tr>



  <tr>
   <th> LandingPage </th> 
   <th> develop </th>
   <th> 94720b213459a9b8d709d11a6e52622888c51716 </th>
   <th> feat: Added reference to homepage </th>
   <th> </th>
   <th> 04/04/2024 </th>
  </tr>

   <tr>
   <th> LandingPage </th> 
   <th> develop </th>
   <th> fd7024ac495181335c261fafa3d2f10b99ae7f0f </th>
   <th> fix: Fixed bugs with the hero section </th>
   <th> </th>
   <th> 05/04/2024 </th>
  </tr>

  <tr>
   <th> LandingPage </th> 
   <th> develop </th>
   <th> 4cbc94d09bb7c291702977f12b08094a4e9671be </th>
   <th> fix: html from other branch removed </th>
   <th> </th>
   <th> 05/04/2024 </th>
  </tr>

<tr>
   <th> LandingPage </th> 
   <th> develop </th>
   <th> 64bf3dca6c65f1aa3da3cf7361c96a5bc41992a3 </th>
   <th> fix: Update responsive and add fixes </th>
   <th> </th>
   <th> 05/04/2024 </th>
  </tr>

  <tr>
   <th> LandingPage </th> 
   <th> develop </th>
   <th> c9539b08c639806676392f55e618cbecd5c3e2d5 </th>
   <th> feat: Footer Progress 1 </th>
   <th> -Added footer for Landing Page </th>
   <th> 07/04/2024 </th>
  </tr>

   <tr>
   <th> LandingPage </th> 
   <th> develop </th>
   <th> 70ffe59529f9b4a041e286b56efad431afcf7b9f  </th>
   <th> fix: Corrected css file for Footer </th>
   <th>  </th>
   <th> 07/04/2024 </th>
  </tr>

  <tr>
   <th> LandingPage </th> 
   <th> develop </th>
   <th> e8f20afe5a416df6474caf3bae840ebf7567c6e5  </th>
   <th> feat: Added pointer feature to links </th>
   <th>  </th>
   <th> 07/04/2024 </th>
  </tr>

  <tr>
   <th> LandingPage </th> 
   <th> develop </th>
   <th> a30ddc245972b87acf1d38097bf533c999403658  </th>
   <th> feat: Added pointer feature so socials </th>
   <th>  </th>
   <th> 07/04/2024 </th>
  </tr>

   <tr>
   <th> LandingPage </th> 
   <th> develop </th>
   <th> f0343471562546d514cbbd0777afb38f860fe85f </th>
   <th> fix: Cleaned code </th>
   <th>  </th>
   <th> 07/04/2024 </th>
  </tr>

 <tr>
   <th> LandingPage </th> 
   <th> develop </th>
   <th> 91d51872a8e678a180ce9f5fc93d94e347335d49 </th>
   <th> fix: Corrected gramatical errors </th>
   <th> </th>
   <th> 07/04/2024 </th>
  </tr>
  <tr>
   <th> LandingPage </th> 
   <th> develop </th>
   <th> 14687ab349113c346d832f4d76d572a2d5643022 </th>
   <th> feat: added new feature </th>
   <th> </th>
   <th> 08/04/2024 </th>
  </tr>
  <tr>
   <th> LandingPage </th> 
   <th> develop </th>
   <th> ad95607392d7bfcb7772e204e6cd2aa772a67b9d </th>
   <th> feat: Images to colabora added </th>
   <th> </th>
   <th> 09/04/2024 </th>
  </tr>
  <tr>
  <th> LandingPage </th> 
   <th> develop </th>
   <th> 95792a490b41cf3aef93ef73f9244b19a42ef7e0 </th>
   <th> feat: feat: Ilustrator's images added </th>
   <th> </th>
   <th> 09/04/2024 </th>
  </tr>
  <tr>
  <th> LandingPage </th> 
   <th> develop </th>
   <th> 77bb9c89cf3a6641fcb6510e794e867dcb3daf76 </th>
   <th> feat: Background image added </th>
   <th> </th>
   <th> 09/04/2024 </th>
  </tr>

  <tr>
  <th> LandingPage </th> 
   <th> develop </th>
   <th> e98121b214baf2cc741c1f5a2494ad3538cd2737 </th>
   <th> feat: Update index.html
 </th>
   <th> </th>
   <th> 09/04/2024 </th>
  </tr>

  <tr>
  <th> LandingPage </th> 
   <th> develop </th>
   <th> e98121b214baf2cc741c1f5a2494ad3538cd2737 </th>
   <th> fix: Fix problem with the navbar </th>
   <th> </th>
   <th> 10/04/2024 </th>
  </tr>
   <tr>
  <th> LandingPage </th> 
   <th> develop </th>
   <th> 4a3fc6ab73c5ce102c07e14058884ee94346beb5 </th>
   <th> feat: Add artists carousel </th>
   <th> </th>
   <th> 10/04/2024 </th>
  </tr>
   <tr>
  <th> LandingPage </th> 
   <th> develop </th>
   <th> 2ed50555d8d8709a76bd6dbead0eeac47e84b070 </th>
   <th> feat: Add SEO Tags and Meta Tags </th>
   <th> </th>
   <th> 10/04/2024 </th>
  </tr>
  <tr>
  <th> LandingPage </th> 
   <th> develop </th>
   <th>  5d2ff1168deee83821ecab233603910b839f850e  </th>
   <th> Merge branch 'feature/explora  </th>
   <th> </th>
   <th> 10/04/2024 </th>
  </tr>
   <tr>
  <th> LandingPage </th> 
   <th> develop </th>
   <th> c305952ff502e115000a8061f5d2bdae5be5d852 </th>
   <th> feat: merge branch with explore feature  </th>
   <th> </th>
   <th> 10/04/2024 </th>
  </tr>

   <tr>
  <th> LandingPage </th> 
   <th> develop </th>
   <th> 12cce3a28fcc09d257a3b5925e93c84eba877523 </th>
   <th> Merge branch 'feature/Carousel'  </th>
   <th> </th>
   <th> 10/04/2024 </th>
  </tr>

  <tr>
  <th> LandingPage </th> 
   <th> develop </th>
   <th> e5b8bf1cb503022d5344c9885b8940f9c16d9c3e </th>
   <th> feat: merge with carousel branch  </th>
   <th> </th>
   <th> 10/04/2024 </th>
  </tr>

  <tr>
  <th> LandingPage </th> 
   <th> develop </th>
   <th> fd92d92b49b4d271409d6ce4dcc519a9c6e3c7ad </th>
   <th> fix: colabora feature fixed  </th>
   <th> </th>
   <th> 10/04/2024 </th>
  </tr>

  <tr>
  <th> LandingPage </th> 
   <th> develop </th>
   <th> c29ce161181fe1b40442fa3e8cebb3e4e0f11364 </th>
   <th> feat: merge branch with footer feature  </th>
   <th> </th>
   <th> 10/04/2024 </th>
  </tr>

   <tr>
  <th> LandingPage </th> 
   <th> develop </th>
   <th> edcb8a3b724b4ffafcdaf67e9badee0a52c82dde </th>
   <th> fix: colabora feature tag fixed  </th>
   <th> </th>
   <th> 10/04/2024 </th>
  </tr>

  <tr>
  <th> LandingPage </th> 
   <th> develop </th>
   <th> ce549f80cbab1b913f0d09e59e3b310a0286a9128  </th>
   <th> feat: merge branch with footer feature </th>
   <th> </th>
   <th> 10/04/2024 </th>
  </tr>



   <tr>
  <th> LandingPage </th> 
   <th> develop </th>
   <th> f056f8380ea4fd787999782396e1c39cc18abc21 </th>
   <th> fix: responsive sections fixed  </th>
   <th> </th>
   <th> 11/04/2024 </th>
  </tr>

 <tr>
  <th> LandingPage </th> 
   <th> develop </th>
   <th> dc6154695eb4016f40ab68449784797862147283 </th>
   <th> fix: hero feature bugs fixed </th>
   <th> </th>
   <th> 11/04/2024 </th>
  </tr>


<tr>
  <th> LandingPage </th> 
   <th> develop </th>
   <th> 12a4b617127ad3da2440cdf4c45bfa4d2b7b3bae </th>
   <th> fix: hero feature bugs fixed </th>
   <th> </th>
   <th> 11/04/2024 </th>
  </tr>


  <tr>
  <th> LandingPage </th> 
   <th> develop </th>
   <th> 66f7bdddd7400d755f6f6d6dfe1bcfa7df60002f </th>
   <th> feat/fix: merge login branch and some feature styles fixed  </th>
   <th> </th>
   <th> 11/04/2024 </th>
  </tr>

 <tr>
  <th> LandingPage </th> 
   <th> develop </th>
   <th> e616c26046c99dceca2574c74eca6da6494e5de1 </th>
   <th> feat: merge with main branch  </th>
   <th> </th>
   <th> 11/04/2024 </th>
  </tr>

   <tr>
  <th> LandingPage </th> 
   <th> develop </th>
   <th> ecfc917e9522926ec6793222b5ff8ac66976731c </th>
   <th> fix: Fix problem with the navbar  </th>
   <th> </th>
   <th> 11/04/2024 </th>
  </tr>

   <tr>
  <th> LandingPage </th> 
   <th> develop </th>
   <th> 6f20b40089db3ea5e1d9d057713f9c5156b84190 </th>
   <th> feat: merge with main branch  </th>
   <th> </th>
   <th> 11/04/2024 </th>
  </tr>

 <tr>
  <th> LandingPage </th> 
   <th> develop </th>
   <th> 97c60ca4a7ad142e495e1979fa51ede9662123b2 </th>
   <th> feat: Add artists carousel </th>
   <th>   </th>
   <th> 11/04/2024 </th>
  </tr>

<tr>
  <th> LandingPage </th> 
   <th> develop </th>
   <th> b30a51cd249e05977c110bf01b1600d11c48b48f </th>
   <th> feat: merge branch with explore feature </th>
   <th>   </th>
   <th> 11/04/2024 </th>
  </tr>

<tr>
  <th> LandingPage </th> 
   <th> develop </th>
   <th> 9ca2be39e68edd3e868eb9f2813454a87b8613a7 </th>
   <th> feat: Footer Progress 1 </th>
   <th>   </th>
   <th> 11/04/2024 </th>
  </tr>

<tr>
  <th> LandingPage </th> 
   <th> develop </th>
   <th> e616c26046c99dceca2574c74eca6da6494e5de1 </th>
   <th> feat: merge with main branch </th>
   <th>   </th>
   <th> 11/04/2024 </th>
  </tr>


  <tr>
  <th> LandingPage </th> 
   <th> develop </th>
   <th> 92453db4a9e0a441cf4257465a3bb3302a90caf0 </th>
   <th> fix: merge bugs fixed </th>
   <th>   </th>
   <th> 11/04/2024 </th>
  </tr>

 <tr>
  <th> LandingPage </th> 
   <th> develop </th>
   <th> 1a70973066b1453a482ad767d0dca0e52a10119a </th>
   <th> fix: merge bugs fixed </th>
   <th>   </th>
   <th> 11/04/2024 </th>
  </tr>

   <tr>
  <th> LandingPage </th> 
   <th> develop </th>
   <th> 4812b7d64fc0456741999c735a28ed039ed85b80 </th>
   <th> fix: test changes </th>
   <th>   </th>
   <th> 11/04/2024 </th>
  </tr>


   <tr>
  <th> LandingPage </th> 
   <th> develop </th>
   <th> 59666f600e552e869fa84c6ff36261a31ac0de56 </th>
   <th> fix: test changes </th>
   <th>   </th>
   <th> 11/04/2024 </th>
  </tr>



 <tr>
  <th> LandingPage </th> 
   <th> develop </th>
   <th> 89add63ec1473c2532296f59c12bb6181cfdea06 </th>
   <th> fix: bug in hero section fixed </th>
   <th>   </th>
   <th> 11/04/2024 </th>
  </tr>

   <tr>
  <th> LandingPage </th> 
   <th> develop </th>
   <th> bd2920875605284fc7f7d62036563ca9b825910b </th>
   <th> fix: Corrected Hero image size </th>
   <th>   </th>
   <th> 11/04/2024 </th>
  </tr>


</table>

### 5.2.1.4. Testing Suite Evidence for Sprint Review. 

En este sprint se realizaron las pruebas de aceptación en la herramienta de Gherkin. El siguiente link se trata de las pruebas de aceptación. https://github.com/Aplicaciones-Web-WX53-Group2-ArtCollab/Acceptance-Tests


<table>
  <tr>
    <th> <strong> Repository </strong> </th>
    <th> <strong> Branch </strong> </th>
    <th> <strong> Commit ID</strong> </th>
    <th> <strong> Commit Message </strong> </th>
     <th> <strong> Commit Message (Body) </strong> </th>
     <th> <strong> Commited on (Date) </strong> </th>
 </tr>

 <tr>
   <th> <strong> Acceptance-Test </strong> </th>
    <th> <strong> main </strong> </th>
    <th> <strong> 4d69fbc54b771c61bdd247d72c58603587c9e618  </strong> </th>
    <th> <strong> Initial commit </strong> </th>
    <th> <strong>  </strong> </th>
    <th> <strong> 11/04/2024 </strong> </th>
 <tr>

  <tr>
   <th> <strong> Acceptance-Test </strong> </th>
    <th> <strong> main </strong> </th>
    <th> <strong> a59189021fcba58acac041db7460f5815e28effd  </strong> </th>
    <th> <strong> feat: Added us-01 acceptance test </strong> </th>
    <th> <strong>  </strong> </th>
    <th> <strong> 11/04/2024 </strong> </th>
 <tr>

   <tr>
   <th> <strong> Acceptance-Test </strong> </th>
    <th> <strong> main </strong> </th>
    <th> <strong> f96bfc729fd1b1675138f985c486c076c545e18b  </strong> </th>
    <th> <strong> feat: Added us-02 acceptance test </strong> </th>
    <th> <strong>  </strong> </th>
    <th> <strong> 11/04/2024 </strong> </th>
 <tr>

  <tr>
   <th> <strong> Acceptance-Test </strong> </th>
    <th> <strong> main </strong> </th>
    <th> <strong> e96ea1a05cbdf07f8df42a2c2aacee33db655a41  </strong> </th>
    <th> <strong> feat: Added us-03 acceptance test </strong> </th>
    <th> <strong>  </strong> </th>
    <th> <strong> 11/04/2024 </strong> </th>
 <tr>

   <tr>
   <th> <strong> Acceptance-Test </strong> </th>
    <th> <strong> main </strong> </th>
    <th> <strong> f54a23e4bd1b179a41c2451990ab32ebaf2bb408  </strong> </th>
    <th> <strong> feat: Added us-04 acceptance test </strong> </th>
    <th> <strong>  </strong> </th>
    <th> <strong> 11/04/2024 </strong> </th>
 <tr>

   <tr>
   <th> <strong> Acceptance-Test </strong> </th>
    <th> <strong> main </strong> </th>
    <th> <strong> 5294d34cd8c17dbc817c20b0c152e3b1c3442a6f  </strong> </th>
    <th> <strong> feat: Added us-05 acceptance test </strong> </th>
    <th> <strong>  </strong> </th>
    <th> <strong> 11/04/2024 </strong> </th>
 <tr>

<tr>
   <th> <strong> Acceptance-Test </strong> </th>
    <th> <strong> main </strong> </th>
    <th> <strong> 8ff78aabec9f8d6b500bb967fd53b3cab74a7d8e  </strong> </th>
    <th> <strong> feat: Added us-17 acceptance test </strong> </th>
    <th> <strong>  </strong> </th>
    <th> <strong> 11/04/2024 </strong> </th>
 <tr>

<tr>
   <th> <strong> Acceptance-Test </strong> </th>
    <th> <strong> main </strong> </th>
    <th> <strong> 1cb783d909328f6038d93f4a1959733c54cd48e9  </strong> </th>
    <th> <strong> feat: Added us-18 acceptance test </strong> </th>
    <th> <strong>  </strong> </th>
    <th> <strong> 11/04/2024 </strong> </th>
 <tr>




</table>

### 5.2.1.5 Execution Evidence for Sprint Review.

<p> Para esta entrega, el equipo ArtCollab logró implementar exitosamente el landing page, en la cual se brindarán información especifica para conocer nuestra misión como startup, asi como también los servicios que ofrecemos en nuestra aplicación web. </p>

Enlace del deploy de la landing page mediante Netlify: https://group2-wx53-si730.netlify.app/




<div style="display:flex; justify-conten:center; flex-direction:column; align-items:center; gap:1rem;">
   <h4> Hero en versión desktop </h4>
   <img style="width:500px" src="https://raw.githubusercontent.com/Aplicaciones-Web-WX53-Group2-ArtCollab/Report/develop/assets/landingpage-test/hero-desktop.png"/>
</div>

<div style="display:flex; justify-conten:center; flex-direction:column; align-items:center; gap:1rem;">
    <h4 style=" padding-top:10px;" > Hero en versión mobile (dropdown desactivado) </h4>
   <img style=" width:400px" src="https://raw.githubusercontent.com/Aplicaciones-Web-WX53-Group2-ArtCollab/Report/develop/assets/landingpage-test/hero-mobile-1.png"/>
</div>


<div style="display:flex; justify-conten:center; flex-direction:column; align-items:center; gap:1rem;">
    <h4 style=" padding-top:10px;" > Hero en versión mobile (dropdown activado) </h4>
   <img style=" width:400px" src="https://raw.githubusercontent.com/Aplicaciones-Web-WX53-Group2-ArtCollab/Report/develop/assets/landingpage-test/hero-mobile-2.png"/>
</div>

<div style="display:flex; justify-conten:center; flex-direction:column; align-items:center; gap:1rem;">
    <h4 style=" padding-top:10px;" > Explora en versión desktop </h4>
   <img style=" width:600px" src="https://raw.githubusercontent.com/Aplicaciones-Web-WX53-Group2-ArtCollab/Report/develop/assets/landingpage-test/explora-desktop.png"/>
</div>

<div style="display:flex; justify-conten:center; flex-direction:column; align-items:center; gap:1rem;">
    <h4 style=" padding-top:10px;" > Explora en versión mobile </h4>
   <img style=" width:600px" src="https://raw.githubusercontent.com/Aplicaciones-Web-WX53-Group2-ArtCollab/Report/develop/assets/landingpage-test/explora-mobile.png"/>
</div>


<div style="display:flex; justify-conten:center; flex-direction:column; align-items:center; gap:1rem;">
    <h4 style=" padding-top:10px;" > Colabora en versión desktop </h4>
   <img style=" width:600px" src="https://raw.githubusercontent.com/Aplicaciones-Web-WX53-Group2-ArtCollab/Report/develop/assets/landingpage-test/colabora-desktop.png"/>
</div>

<div style="display:flex; justify-conten:center; flex-direction:column; align-items:center; gap:1rem;">
    <h4 style=" padding-top:10px;" > Colabora en versión mobile </h4>
   <img style=" width:600px" src="https://raw.githubusercontent.com/Aplicaciones-Web-WX53-Group2-ArtCollab/Report/develop/assets/landingpage-test/colabora-mobile.png"/>
</div>


<div style="display:flex; justify-conten:center; flex-direction:column; align-items:center; gap:1rem;">
    <h4 style=" padding-top:10px;" > Colabora en versión desktop </h4>
   <img style=" width:600px; height:70px" src="https://raw.githubusercontent.com/Aplicaciones-Web-WX53-Group2-ArtCollab/Report/develop/assets/landingpage-test/footer-desktop.png"/>
</div>

<div style="display:flex; justify-conten:center; flex-direction:column; align-items:center; gap:1rem;">
    <h4 style=" padding-top:10px;" > Colabora en versión mobile </h4>
   <img style=" width:300px; height:300px" src="https://raw.githubusercontent.com/Aplicaciones-Web-WX53-Group2-ArtCollab/Report/develop/assets/landingpage-test/footer-mobile.png" />
</div>


<div style="display:flex; justify-conten:center; flex-direction:column; align-items:center; gap:1rem;">
    <h4 style=" padding-top:10px;" > Login versión desktop (Orientativo para el usuario, no funcional) </h4>
   <img style=" width:600px; height:300px" src="https://raw.githubusercontent.com/Aplicaciones-Web-WX53-Group2-ArtCollab/Report/develop/assets/landingpage-test/login-desktop.png" />
</div>

<div style="display:flex; justify-conten:center; flex-direction:column; align-items:center; gap:1rem;">
    <h4 style=" padding-top:10px;" > Login versión mobile sin dropdown (Orientativo para el usuario, no funcional) </h4>
   <img style=" width:200px; height:400px" src="https://raw.githubusercontent.com/Aplicaciones-Web-WX53-Group2-ArtCollab/Report/develop/assets/landingpage-test/login-mobile-1.png" />
</div>

<div style="display:flex; justify-conten:center; flex-direction:column; align-items:center; gap:1rem;">
    <h4 style=" padding-top:10px;" > Login versión mobile con dropdown (Orientativo para el usuario, no funcional) </h4>
   <img style=" width:200px; height:400px" src="https://raw.githubusercontent.com/Aplicaciones-Web-WX53-Group2-ArtCollab/Report/develop/assets/landingpage-test/login-mobile-2.png" />
</div>




### 5.2.1.6 Services Documentation Evidence for Sprint Review.

En el alcance del sprint 1 se ha priorizado el desarrollado la landing page, por lo que para este sprint no se evidencia el empleo de web services.

### 5.2.1.7 Software Deployment Evidence for Sprint Review.

Para el presente sprint, se ha desarrollado la landing page. Para el despliegue se emplearon las siguientes herramientas.

<ul>
 <li> Git: Sistema de control de versiones el cual empleamos para trabajar de manera colaborativa y monitorear las versiones de la landing page en un repositorio remoto.

 </li>

 <li> Gitflow: Flujo de trabajo colaborativo, esto nos permitió dividir el trabajo por ramas dentro de nuestro repositorio con la finalidad de facilitar la colaboración en el desarrollo. </li>

 <li>
    GitHub: Plataforma que nos brindo la herramienta de crear nuestro repositorio para almacenar las versiones de nuestro proyecto.
 </li>

 <li>
    Netlify: Plataforma que automatiza webs estáticas que nos permitió alojar y desplegar nuestra el landing page.
 </li>

</ul>



### 5.2.1.8 Team Collaboration Insights during Sprint.

El equipo desarrolló el landing page por ramas con la finalidad de desarrollar cada sección de manera indpeendiente para optimizar el mantenimiento y colaboración durante el sprint. Asimismo se aplico las convenciones estandard de gitflow, por lo que contamos con nuestras ramas de develop y feature segun la funcionalidad. A continuación se presenta las tareas asignadas a cada integrante del equipo, asi como también el insight del equipo a través de la plataforma GitHub: 




<table>
  <tr> 
   <th> <strong> Alumno </strong></th>
   <th> <strong> Actividad </strong></th>
   </tr>

  <tr> 
   <th> Jave Diaz, Mathias Alejandro  </th>
   <th>  Implementación de la navbar tanto en su versión mobile como desktop, también en la implementación de la sección footer en su modo responsive </th>
 </tr>
  <tr> 
   <th> Huilca Chipana, Gustavo  </th>
   <th>  Implementación de la sección footer tanto en su versión mobile como desktop </th>
 </tr>
  <tr> 
   <th> Amaro Villanueva, Camila Elena  </th>
   <th>  Implementación de la sección hero en su versión mobile y desktop </th>
 </tr>
  <tr> 
   <th> Dam Rubianes, Frida Sofia  </th>
   <th>  Implementación de la sección colabora tanto en su versión mobile como desktop </th>
 </tr> <tr> 
   <th> Cuadros Rodriguez, Juan Alejandro  </th>
   <th>  Implementacion de la sección Explora tanto en su versión mobile como desktop </th>
 </tr>

</table>

Hemos desarrollado en conjunto un total de 43 commits para el desarrollo de la landing page, los cuales representan la correción de bugs, merge entre ramas, agregado de secciones y corrreción en el codigo fuente.

A continuación se presentara la tabla de colaboradores en el repositorio de Github, con la finalidad de identificar a cada integrante del equipo.

Tabla de integrantes:


<table>
  <tr> 
   <th> <strong> Username (GitHub) </strong></th>
   <th> <strong> Nombre </strong></th>
   </tr>

  <tr> 
   <th> LordMathi2741  </th>
   <th>Jave Diaz, Mathias Alejandro   </th>
 </tr>
  <tr> 
  <th> GustavoHuilca31 </th>
   <th> Huilca Chipana, Gustavo  </th>
 </tr>
  <tr> 
   <th> CamiAm404 </th>
   <th> Amaro Villanueva, Camila Elena  </th>

 </tr>
  <tr> 
   <th> Frida-Dam </th>
   <th> Dam Rubianes, Frida Sofia  </th>
 </tr> 
 <tr> 
   <th> JuanAlejandroCuadrosRodriguez </th>
   <th> Cuadros Rodriguez, Juan Alejandro  </th>
 </tr>

</table>

A continuación se mostrarán los gráficos de insights durante el sprint:

<img src="https://raw.githubusercontent.com/Aplicaciones-Web-WX53-Group2-ArtCollab/Report/develop/assets/Insights/Network-Graph-1.png"/>

<img src="https://raw.githubusercontent.com/Aplicaciones-Web-WX53-Group2-ArtCollab/Report/develop/assets/Insights/NetWork-Graph-2.png"/>

#### Anexo: flujo de trabajo entre las ramas


<img src="https://raw.githubusercontent.com/Aplicaciones-Web-WX53-Group2-ArtCollab/Report/develop/assets/Insights/Pulse.png"/>

#### Anexo: tablas de commits en el periodo de 1 mes

<img src="https://raw.githubusercontent.com/Aplicaciones-Web-WX53-Group2-ArtCollab/Report/develop/assets/Insights/Contributions.png" />

#### Anexo: Flujo de trabajo en el periodo de 1 mes

<img src="https://raw.githubusercontent.com/Aplicaciones-Web-WX53-Group2-ArtCollab/Report/develop/assets/Insights/ColaborationsInsights.png" />

#### Anexo: Colaboration Insights en el periodo de 1 mes






