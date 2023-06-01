## Tema 5: Implement Azure App Service Web Apps

#### ¿Cuáles son las características principales de Azure App Service?

- Compatibilidad multiplataforma: Soporta ASP.NET, ASP.NET Core, Java, Ruby, Node.js, PHP o Python.
- Entorno de producción administrado: App Service parchea y mantiene los marcos del sistema operativo y del lenguaje de forma automática
- Contenedores y Docker: aplique Docker a la aplicación y hospede un contenedor de Windows o Linux personalizado en App Service.
- Integracion total: Integrado a VScode, VS y todos los servicios de azure
- Codigo serverless: Ejecutar codigo sin necesidad de administrar el servidor o su infraestructura
- Compatibilidad para APIs: compatibilidad CORS llave en mano para escenarios de la API RESTful
- Escala global con alta disponibilidad: escale verticalmente u horizontalmente de forma manual o automática.
- Plantillas de aplicación: elija entre una amplia lista de plantillas de aplicación listas para usar.

#### ¿Cómo se configura y escala una aplicación web en Azure App Service?

1. Crear un recurso de Azure App Service: En el portal de Azure, crea un nuevo recurso de Azure App Service. Proporciona un nombre único, selecciona la suscripción, el grupo de recursos y la región donde deseas implementar tu aplicación.
2. Configurar la pila de lenguaje y la versión: Durante la creación del App Service, elige el lenguaje y la versión que deseas utilizar para la aplicacion.
3. Configurar la escala automática: Azure App Service permite la escalabilidad automática para adaptarse a las demandas de la aplicación. En la sección de Escala, puedes configurar reglas basadas en métricas como CPU, memoria o solicitudes por segundo para aumentar o disminuir automáticamente las instancias de tu aplicación según la carga de trabajo.
4. Configurar las variables de entorno y las configuraciones de la aplicación: Puedes establecer variables de entorno y configuraciones específicas de tu aplicación en la sección Configuración de la aplicación. Estas configuraciones se pueden acceder desde tu código para personalizar el comportamiento de la aplicación.

#### ¿Qué es un plan de App Service y cómo se relaciona con las aplicaciones web?

En Azure App Service, un plan de App Service es un recurso que define los recursos y las características disponibles para hospedar y ejecutar aplicaciones web. Un plan de App Service proporciona la infraestructura y los recursos necesarios para alojar las aplicaciones web, incluyendo potencia de procesamiento, memoria, almacenamiento, conectividad de red y características adicionales. 

Al crear una aplicacion web en Azure se debe seleccionar un plan App Service y este determina los recursos que la aplicación poseerá, como la potencia de calculo o la memoria, las características que tendra y las opciones de escalabilidad que tendra 

