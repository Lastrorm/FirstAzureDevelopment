## Tema 2: Implement Azure Functions

#### ¿Qué son las Azure Functions y para qué se utilizan?

Azure Functions es un servicio de cómputo sin servidor ofrecido por Microsoft Azure. Proporciona una plataforma en la nube para ejecutar código en respuesta a eventos específicos sin la necesidad de administrar la infraestructura subyacente. Las Azure Functions permiten ejecutar fragmentos de código (funciones) de manera independiente, escalable y bajo demanda.

Las Azure Functions se utilizan para:

- Procesamiento de eventos
- Integración de sistemas y servicios
- Desarrollo de API y servicios web
- Tareas programadas y procesamiento por lotes
- Eventos basados en IoT
- Extensiones y personalización

#### ¿Cuáles son los desencadenadores (triggers) más comunes en Azure Functions?

- HTTP Trigger
- Timer Trigger
- Blob Trigger
- Queue Trigger
- Event Grid Trigger
- Cosmos DB Trigger
- Service Bus Trigger

#### ¿Cómo se configura y se despliega una Azure Function?

1. Crear una Azure Function
2. Configurar la Function App
3. Crear una función
4. Implementar el código de la función
5. Probar y depurar la función
6. Configurar las opciones de despliegue
7. Desplegar la Function App
8. Monitorear y administrar la Function App


## Batería de preguntas sobre Azure Functions

#### You need to resolve a notification latency issue. Which two actions should you perform? Each correct answer presents part of the solution.

 A. Set Always On to true.
 B. Ensure that the Azure Function is using an App Service plan.
 C. Set Always On to false.
 D. Ensure that the Azure Function is set to use a consumption plan.

#### You are developing an Azure Function App that processes images that are uploaded to an Azure Blob container. Images must be processed as quickly as possible after they are uploaded, and the solution must minimize latency. You create code to process images when the Function App is triggered. You need to configure the Function App. What should you do?

 A. Use an App Service plan. Configure the Function App to use an Azure Blob Storage input trigger.
 B. Use a Consumption plan. Configure the Function App to use an Azure Blob Storage trigger.
 C. Use a Consumption plan. Configure the Function App to use a Timer trigger.
 D. Use an App Service plan. Configure the Function App to use an Azure Blob Storage trigger.
 E. Use a Consumption plan. Configure the Function App to use an Azure Blob Storage input trigger.

#### You develop an HTTP triggered Azure Function app to process Azure Storage blob data. The app is triggered using an output binding on the blob. The app continues to time out after four minutes. The app must process the blob data. You need to ensure the app does not time out and processes the blob data.Solution: Configure the app to use an App Service hosting plan and enable the Always On setting. Does the solution meet the goal?

 No, instead pass the HTTP trigger payload into an Azure Service Bus queue to be processed by a queue trigger function and return an immediate HTTP success response.