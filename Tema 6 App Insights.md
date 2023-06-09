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

### QUESTION 1 Pag 175
You need to investigate the Azure Function app error message in the development environment.
What should you do?
- A. Connect Live Metrics Stream from Application Insights to the Azure Function app and filter the metrics.
- B. Create a new Azure Log Analytics workspace and instrument the Azure Function app with Application Insights.
- C. Update the Azure Function app with extension methods from Microsoft.Extensions.Logging to log events by using the log instance.
- D. Add a new diagnostic setting to the Azure Function app to send logs to Log Analytics.

Correct Answer: A

Explanation:
Azure Functions offers built-in integration with Azure Application Insights to monitor functions.
The following areas of Application Insights can be helpful when evaluating the behavior, performance, and
errors in your functions:
Live Metrics: View metrics data as it's created in near real-time.
Failures
Performance
Metrics

### QUESTION 6 Pag 197
You are developing an ASP.NET Core Web API web service. The web service uses Azure Application
Insights for all telemetry and dependency tracking. The web service reads and writes data to a database
other than Microsoft SQL Server.
You need to ensure that dependency tracking works for calls to the third-party database.
Which two dependency telemetry properties should you use? Each correct answer presents part of the
solution.

A. Telemetry.Context.Cloud.RoleInstance

B. Telemetry.Id

C. Telemetry.Name

D. Telemetry.Context.Operation.Id

E. Telemetry.Context.Session.Id

Correct Answer: BD

Para realizar un seguimiento adecuado de las dependencias en las llamadas a bases de datos de terceros, se debe emplear las propiedades "Telemetry.Id" y "Telemetry.Context.Operation.Id".

Estas propiedades facilitan la correlación de operaciones entre diversos componentes de la aplicación, asegurando así un rastreo preciso de las dependencias a travez de Azure Application Insights.

### QUESTION 4 Pag 195
You develop and deploy an ASP.NET web app to Azure App Service. You use Application Insights
telemetry to monitor the app.
You must test the app to ensure that the app is available and responsive from various points around the
world and at regular intervals. If the app is not responding, you must send an alert to support staff.
You need to configure a test for the web app.
Which two test types can you use? Each correct answer presents a complete solution.

- A. integration
- B. multi-step web
- C. URL ping
- D. unit
- E. load

Correct Answer: BC

Explanation:
There are three types of availability tests:
URL ping test: a simple test that you can create in the Azure portal.
Multi-step web test: A recording of a sequence of web requests, which can be played back to test more
complex scenarios. Multi-step web tests are created in Visual Studio Enterprise and uploaded to the portal for execution.
Custom Track Availability Tests: If you decide to create a custom application to run availability tests, the TrackAvailability() method can be used to send the results to Application Insights.
