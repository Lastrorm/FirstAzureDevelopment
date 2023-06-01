# Tema 3: Implement user authentication and authorization

- ¿Qué es la Plataforma de Identidad de Microsoft y cómo se utiliza para la autenticación
  de usuarios?

La plataforma de identidad de Microsoft es una evolución de la plataforma de desarrollo Azure Active Directory (Azure AD). Permite a los desarrolladores crear aplicaciones que inician sesión de usuarios y acceder a recursos en aplicaciones externas como Microsoft 365,la Azure Portal y miles de otras aplicaciones SaaS y recursos internos, como aplicaciones en la red corporativa e intranet, junto con las aplicaciones en la nube desarrolladas por su propia organización.

- ¿Cuál es el flujo de autenticación más común al utilizar la Plataforma de Identidad de
  Microsoft?

  El flujo de autenticación más común al utilizar la Plataforma de Identidad de Microsoft es el flujo de código de autorización de OAuth 2.0. Este flujo requiere un agente de usuario que admita el redireccionamiento desde el servidor de autorización (la plataforma de identidad de Microsoft) a la aplicación.

- ¿Cómo se obtienen y se utilizan los tokens de acceso para autorizar solicitudes a
  recursos protegidos?

  La Plataforma de identidad de Microsoft autentica a los usuarios y proporciona tokens de seguridad, como los tokens de acceso, los tokens de actualización y los tokens de id

  1. El usuario inicia sesión en el sitio web.
  2. El navegador redirige al usuario a la pagina de inicio de sesió de Azure Active Directory(Azure AD).
  3. El usuario inicia sesión.
  4. Azure AD redirige la sesion del usuario a la aplicacion web. Donde la URL incluye un token de acceso.
  5. La aplicacion web llama a una API e incluye el token de acceso en el encabezado de autenticacion, El id de la aplicacion es enviado como el reclamo de audiencia ('aud') en el token de acesso.
  6. La API de Back-end valida el acceso.
