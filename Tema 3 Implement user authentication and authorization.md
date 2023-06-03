# Tema 3: Implement user authentication and authorization

#### ¿Qué es la Plataforma de Identidad de Microsoft y cómo se utiliza para la autenticación de usuarios?

La plataforma de identidad de Microsoft es una evolución de la plataforma de desarrollo Azure Active Directory (Azure AD). Permite a los desarrolladores crear aplicaciones que inician sesión de usuarios y acceder a recursos en aplicaciones externas como Microsoft 365,la Azure Portal y miles de otras aplicaciones SaaS y recursos internos, como aplicaciones en la red corporativa e intranet, junto con las aplicaciones en la nube desarrolladas por su propia organización.

#### ¿Cuál es el flujo de autenticación más común al utilizar la Plataforma de Identidad de Microsoft?

El flujo de autenticación más común al utilizar la Plataforma de Identidad de Microsoft es el flujo de código de autorización de OAuth 2.0. Este flujo requiere un agente de usuario que admita el redireccionamiento desde el servidor de autorización (la plataforma de identidad de Microsoft) a la aplicación.

#### ¿Cómo se obtienen y se utilizan los tokens de acceso para autorizar solicitudes a recursos protegidos?

La Plataforma de identidad de Microsoft autentica a los usuarios y proporciona tokens de seguridad, como los tokens de acceso, los tokens de actualización y los tokens de id

1. El usuario inicia sesión en el sitio web.
2. El navegador redirige al usuario a la pagina de inicio de sesió de Azure Active Directory(Azure AD).
3. El usuario inicia sesión.
4. Azure AD redirige la sesion del usuario a la aplicacion web. Donde la URL incluye un token de acceso.
5. La aplicacion web llama a una API e incluye el token de acceso en el encabezado de autenticacion, El id de la aplicacion es enviado como el reclamo de audiencia ('aud') en el token de acesso.
6. La API de Back-end valida el acceso.

# Preguntas

1.  QUESTION 4 - Page 131
    You need to authenticate the user to the corporate website as indicated by the architectural diagram.
    Which two values should you use? Each correct answer presents part of the solution.

    ```
    A. ID token signature
    B. ID token claims
    C. HTTP response code
    D. Azure AD endpoint URI
    E. Azure AD tenant ID
    
      Correct Answer: AD
      Section: (none)
      Explanation:
      A: Claims in access tokens
      JWTs (JSON Web Tokens) are split into three pieces:
      Header - Provides information about how to validate the token including information about the type of
      token and how it was signed.
      Payload - Contains all of the important data about the user or app that is attempting to call your service.
      Signature - Is the raw material used to validate the token.
      E: Your client can get an access token from either the v1.0 endpoint or the v2.0 endpoint using a variety of
      protocols.
      Scenario: User authentication (see step 5 below)
      The following steps detail the user authentication process:
        1. The user selects Sign in in the website.
        1.The browser redirects the user to the Azure Active Directory (Azure AD) sign in page.
        2.The user signs in.
        3.Azure AD redirects the user’s session back to the web application. The URL includes an access token.
        4.The web application calls an API and includes the access token in the authentication header. The
            application ID is sent as the audience (‘aud’) claim in the access token.
        5.The back-end API validates the access token.
    
    ```

2.  QUESTION 3 - Page 130 - HOTSPOT
    You need to configure API Management for authentication.
    Which policy values should you use? To answer, select the appropriate options in the answer area.
    ![QUESTION](https://cdn.discordapp.com/attachments/713046248034271355/1114574152846819458/image.png)

    

    Explanation:
    Box 1: Validate JWT
    The validate-jwt policy enforces existence and validity of a JWT extracted from either a specified HTTP
    Header or a specified query parameter.
    Scenario: User authentication (see step 5 below)
    The following steps detail the user authentication process:

        1.  The user selects Sign in in the website.
        2.  The browser redirects the user to the Azure Active Directory (Azure AD) sign in page.
        3.  The user signs in.
        4.  Azure AD redirects the user’s session back to the web application. The URL includes an access token.
        5.  The web application calls an API and includes the access token in the authentication header. The
            application ID is sent as the audience (‘aud’) claim in the access token.
        6.  The back-end API validates the access token.
            A6319EC1AC83D57E5BA185C098116365

    Incorrect Answers:
    Limit call rate by key - Prevents API usage spikes by limiting call rate, on a per key basis.
    Restrict caller IPs - Filters (allows/denies) calls from specific IP addresses and/or address ranges.
    Check HTTP header - Enforces existence and/or value of a HTTP Header.
    Box 2: Outbound

3.  QUESTION 1 - page 121 -
    You need to secure the Shipping Function app.
    How should you configure the app? To answer, select the appropriate options in the answer area.
    ![Question 1 page 121](https://cdn.discordapp.com/attachments/713046248034271355/1114584088179904662/image.png)
    Correct Answer
    ![Correct Answer Question 1 page 121](https://cdn.discordapp.com/attachments/713046248034271355/1114584088179904662/image.png)
    ```
    Explanation:
    Scenario: Shipping Function app: Implement secure function endpoints by using app-level security and
    include Azure Active Directory (Azure AD).
    Box 1: Function
    Box 2: JSON based Token (JWT)
    Azure AD uses JSON based tokens (JWTs) that contain claims
    Box 3: HTTP
    How a web app delegates sign-in to Azure AD and obtains a token
    User authentication happens via the browser. The OpenID protocol uses standard HTTP protocol
    messages.
    ```
