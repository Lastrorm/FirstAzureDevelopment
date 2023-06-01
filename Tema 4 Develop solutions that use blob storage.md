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
