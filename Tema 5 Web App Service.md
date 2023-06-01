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



## Tema 6: Troubleshoot solutions by using Application Insights

#### ¿Qué es Azure Application Insights y cómo se utiliza para el monitoreo de aplicaciones?

Azure Application Insights es un servicio de monitoreo y análisis de aplicaciones en la nube ofrecido por Microsoft Azure. Proporciona información detallada sobre el rendimiento y el comportamiento de las aplicaciones, lo que permite detectar y solucionar problemas, optimizar el rendimiento y mejorar la experiencia del usuario. 

Para controlar otras aplicaciones se debe integrar la SDK de Application Insights en ellas, luego se usara para recuperar datos de telemetria de la aplicacion en tiempo real. Luego es posible ver esa informacion en los paneles de control del App y, en base a esa informacion, diagnosticar los problemas del programa y crear soluciones para el.

#### ¿Cuáles son las principales características y beneficios de Application Insights?

- Monitoreo en tiempo real: Application Insights recopila y muestra datos de telemetría en tiempo real.
- Rendimiento de la aplicación: Puedes monitorear métricas clave de rendimiento, como tiempos de respuesta, rendimiento de la base de datos, uso de CPU y memoria.

- Detección de errores y excepciones: Puedes capturar y registrar excepciones no controladas en tu aplicación, lo que te permite identificar y solucionar problemas antes de que afecten a los usuarios.

- Análisis avanzado: Puedes realizar consultas y segmentaciones personalizadas en los datos de telemetría, lo que permite realizar análisis detallados y obtener información específica sobre el comportamiento de tu aplicación.

- Alertas y notificaciones: Puedes configurar alertas personalizadas basadas en umbrales específicos para métricas y eventos importantes. Esto te permite recibir notificaciones cuando ocurran eventos críticos o cuando se supere un límite predefinido.

- Integración con Azure DevOps: Application Insights se puede integrar con Azure DevOps, lo que permite correlacionar los eventos de telemetría con el ciclo de vida del desarrollo de la aplicación.

- Escalabilidad y disponibilidad: Application Insights está diseñado para escalar y manejar cargas de trabajo de cualquier tamaño.



#### ¿Cómo se configura y se utiliza Application Insights para el diagnóstico y solución de problemas en una aplicación?

1. Crear un recurso de Application Insights: En el portal de Azure, crea un nuevo recurso de Application Insights. Proporciona un nombre, selecciona la suscripción, el grupo de recursos y la región.
2. Integrar Application Insights en tu aplicación: Para comenzar a recopilar datos de telemetría, debes integrar el SDK de Application Insights en tu aplicación. El SDK está disponible para diferentes lenguajes y plataformas.
3. Configurar el Instrumentation Key: Después de integrar el SDK, se te proporcionará un Instrumentation Key único. Este key es necesario para que tu aplicación se comunique con el recurso de Application Insights.
4. Recopilar datos de telemetría: Una vez integrado el SDK y configurado el Instrumentation Key, la App comenzará a recopilar datos de telemetría de tu aplicación. Estos datos incluyen métricas de rendimiento, eventos personalizados, excepciones, trazas de registro, etc.
5. Utilizar los paneles de Application Insights: Accede al portal de Azure y abre el recurso de Application Insights que has creado. Aquí encontrarás paneles de control y herramientas de análisis que te permitirán visualizar y analizar los datos de telemetría recopilados. Explora los diferentes paneles y métricas disponibles para obtener información sobre el rendimiento de tu aplicación.
6. Configurar alertas: Puedes configurar alertas personalizadas en Application Insights para recibir notificaciones cuando ocurran eventos o métricas específicas superen los umbrales definidos. Configura las alertas según tus necesidades para estar informado sobre problemas críticos en tu aplicación.
7. Solucionar problemas: Utiliza los datos de telemetría de Application Insights para solucionar los problemas que se hayan detectado.