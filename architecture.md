### Arquitectura para Proyectos de Frontend



#### Tipos de componente que se pueden utilizar 



##### Element components

Son componentes sumamente modulares y reutilizables. No deben acoplarse a lógica de negocio ni plugins o librerias externas de Vue que no sean de componentes. El objetivo de estos componentes es lograr tener componentes fácilmente reutilizables y que permitan responder rápidamente al cambio. Ejemplos de element components serían:

- **ButtonElement**: Elemento base de boton
- **AvatarElement**: Elemento base de avatar

  

##### Feature components

Los feature components son componentes que implementan la interfaz de un caso de uso, pero que de ninguna manera, deben acoplarse a un estado explicito. Los feature components deben contar con props que modifiquen su estado e incluso permitan extender algunas funcionalidades. Ejemplos de feature components serían:

- **SearchBarComponent**: Componente para de barra de busquedas 
- **UserCardComponent**: Componente que presente información de usuario



##### Layout components (Nuxt.js Layouts)

Componentes con poco nivel de reusabilidad. Contienen el esquema o diseño de la interfaz que se repite a lo largo de varias páginas.  Como ejemplos claros de layouts components en una aplicación común sería el siguiente:

- **DashboardLayout:** contiene los elementos de un dashboard que se mantienen a lo largo de la navegación (ej: NavigationBar, AppSidebar, AppFooter)



##### Page components  (Nuxt.js Pages)

Representan una ruta en la navegación. Estos componentes pueden contener  implementaciones de lógica de negocio o casos de uso especificos. Pueden valerse de feature y element components para realizar dichas implementaciones. También pueden consultar consumer methods a traves de CompositionAPI. En estos componentes también se pueden definir propiedades como middlewares para autorizar o denegar accesos a determinadas funcionalidades, así como definir meta etiquetas usando la propiedad head. Podríamos mencionar como ejemplo de page components:

- **UserLoginPage (/login):** la página de inicio de sesión
- **ReportCreatePage (/dashboard/reports/create):** pagina para crear reporte
- **ReportEditPage (/dashboard/reports/{id}/edit):** pagina para editar reporte 

