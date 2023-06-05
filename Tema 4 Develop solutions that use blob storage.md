# Tema 4: Develop solutions that use blob storage

#### ¿Qué es Azure Blob storage y cómo se utiliza para almacenar datos no estructurados?

Azure Blob Storage es la solución de almacenamiento de objetos de Microsoft para la nube. Blob Storage está optimizado para el almacenamiento de cantidades masivas de datos no estructurados. Los datos no estructurados son datos que no se ciñen a ningún un modelo de datos o definición concretos, como texto o datos binarios.

#### ¿Cuáles son los tipos de blobs que se pueden almacenar en Azure Blob storage?

Azure Storage admite tres tipos de blobs:

- Los **blobs en bloques** almacenan texto y datos binarios. Los blobs en bloques se componen de bloques de datos que se pueden administrar de forma individual. Los blobs en bloques pueden almacenar hasta aproximadamente 190,7 TiB.
- Los **blobs en anexos** constan de bloques, como los blobs en bloques, pero están optimizados para operaciones de anexión. Los blobs en anexos resultan muy convenientes para escenarios como el registro de datos de máquinas virtuales.
- Los **blobs en páginas** almacenan archivos de acceso aleatorio con un tamaño máximo de 8 TiB. Para más información sobre los blobs en páginas, consulte la Introducción a los blobs en páginas de Azure

#### ¿Cómo se accede y se administra el almacenamiento de blobs en Azure?

Para acceder y administrar el almacenamiento de blobs en Azure, los usuarios o las aplicaciones cliente pueden acceder a los objetos del almacenamiento Blob a través de HTTP/HTTPS desde cualquier parte del mundo. Se puede acceder a los objetos del almacenamiento Blob a través de la API REST de Azure Storage, Azure PowerShell, Azure CLI o una biblioteca cliente de Azure Storage.

# Preguntas

1.  QUESTION 12 - Page 237

    You are developing an Azure solution to collect point-of-sale (POS) device data from 2,000 stores located
    throughout the world. A single device can produce 2 megabytes (MB) of data every 24 hours. Each store
    location has one to five devices that send data.
    You must store the device data in Azure Blob storage. Device data must be correlated based on a device
    identifier. Additional stores are expected to open in the future.
    You need to implement a solution to receive the device data.
    Solution: Provision an Azure Event Grid. Configure event filtering to evaluate the device identifier.
    Does the solution meet the goal?

        A. Yes
        B. No

    Correct Answer: B
    Explanation:
    Instead use an Azure Service Bus, which is used order processing and financial transactions.
    Note: An event is a lightweight notification of a condition or a state change. Event hubs is usually used
    reacting to status changes.

2.  QUESTION 11 - Page 236

    You are developing an Azure solution to collect point-of-sale (POS) device data from 2,000 stores located
    throughout the world. A single device can produce 2 megabytes (MB) of data every 24 hours. Each store
    location has one to five devices that send data.
    You must store the device data in Azure Blob storage. Device data must be correlated based on a device
    identifier. Additional stores are expected to open in the future.
    You need to implement a solution to receive the device data.
    Solution: Provision an Azure Service Bus. Configure a topic to receive the device data by using a correlation
    filter.
    Does the solution meet the goal?
    A. Yes
    B. No
    Correct Answer: A

    Explanation:
    A message is raw data produced by a service to be consumed or stored elsewhere. The Service Bus is for
    high-value enterprise messaging, and is used for order processing and financial transactions.

3.  QUESTION 6 - Page 147
    You develop an app that allows users to upload photos and videos to Azure storage. The app uses a
    storage REST API call to upload the media to a blob storage account named Account1. You have blob
    storage containers named Container1 and Container2.
    Uploading of videos occurs on an irregular basis.
    You need to copy specific blobs from Container1 to Container2 when a new video is uploaded.
    What should you do?
    
        A. Copy blobs to Container2 by using the Put Blob operation of the Blob Service REST API
        B. Create an Event Grid topic that uses the Start-AzureStorageBlobCopy cmdlet
        C. Use AzCopy with the Snapshot switch to copy blobs to Container2
        D. Download the blob to a virtual machine and then upload the blob to Container2

    Explanation:
    The Start-AzureStorageBlobCopy cmdlet starts to copy a blob.
    Example 1: Copy a named blob
    C:\PS>Start-AzureStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives" -
    SrcContainer "ContosoUploads"
    This command starts the copy operation of the blob named ContosoPlanning2015 from the container
    named ContosoUploads to the container named ContosoArchives.
