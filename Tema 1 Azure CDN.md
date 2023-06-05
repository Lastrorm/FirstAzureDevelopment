## Tema 1: Azure CDN (Content Delivery Network)

#### ¿Qué es Azure CDN y cuál es su propósito en el despliegue de aplicaciones web?

Azure CDN (Content Delivery Network) es un servicio proporcionado por Microsoft Azure que se utiliza  en el despliegue de aplicaciones web para mejorar la velocidad de carga de los recursos estáticos, reducir la latencia y ofrecer una mejor experiencia al usuario final al entregar contenido de manera eficiente a través de una red global de servidores de borde.

#### ¿Cuáles son los beneficios de utilizar Azure CDN en términos de rendimiento y escalabilidad?

- Mejora del rendimiento
- Mayor velocidad de carga
- Reducción de carga del servidor
- Escalabilidad global
- Capacidad para manejar los picos de tráfico
- Ahorro de ancho de banda

#### ¿Cómo se configura y se utiliza Azure CDN para acelerar la entrega de contenido estático y dinámico en una aplicación web?

1. Crear una cuenta de Azure CDN
2. Configurar un punto de conexión (endpoint) de CDN
3. Configurar reglas de caché
4. Configurar dominios personalizados
5. Configurar reglas de redireccionamiento
6. Implementar cambios en la aplicación web
7. Monitorear y optimizar el rendimiento

## Batería de preguntas sobre CDN

#### You need to configure Azure CDN for the Shipping web site. Which configuration options should you use? To answer, select the appropriate options in the answer area

 - Tier:
   - **Standard**
   - Premium
 - Profile:
   - **Akamai**
   - Microsoft
 - Optimization:
   - general web delivery
   - large file download
   - **dynamic site acceleration**
   - video-on-demand media streaming

#### You need to correct the VM issues. Which tools should you use? To answer, select the appropriate options in the answer area.

 - Backup and Restore:
   - Azure Site Recovery
   - **Azure Backup**
   - Azure Data Box
   - Azure Migrate
 - Performance:
   - Azure Network Watcher
   - Azure Traffic Manager
   - ExpressRoute
   - **Accelerated Networking**

#### You are developing an Azure App Service hosted ASP.NET Core web app to deliver video-on-demand streaming media. You enable an Azure Content Delivery Network (CDN) Standard or the web endpoint. Customer videos are downloaded from the web app by using the following example URL: (http://www.contoso.com/content.mp4?quality=1). All media content must expire from the cache after one hour. Customer videos with varying quality must be delivered to the closest regional point of presence (POP) node. You need to configure Azure CDN caching rules. Which options should you use? To answer, select the appropriate options in the answer area.

 - Caching Behavior:
   - Bypass cache
   - **Override**
   - Set if missing
 - Cache expiration duration:
   - 1 second
   - 1 minute
   - **1 hour**
   - 1 day
 - Query string caching behavior:
   - Ignore query strings
   - Bypass caching for query strings
   - **Cache every unique URL**