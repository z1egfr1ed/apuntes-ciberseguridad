# Autenticación, autorización y AAA

## Conceptos clave

| Concepto | Pregunta que responde | Ejemplo |
|---|---|---|
| **Identificación** | ¿Quién dices ser? | Nombre de usuario |
| **Autenticación** | ¿Puedes demostrarlo? | Contraseña, huella, token |
| **Autorización** | ¿Qué puedes hacer? | Permisos de lectura/escritura |
| **Accounting (auditoría)** | ¿Qué hiciste? | Logs de acceso y acciones |

Juntos forman el modelo **AAA** (Authentication, Authorization, Accounting).

## Factores de autenticación

- **Algo que sabes:** contraseña, PIN.
- **Algo que tienes:** token, tarjeta, app autenticadora, llave FIDO2.
- **Algo que eres:** huella, rostro, iris.
- **Dónde estás / cómo te comportas:** ubicación, patrones de uso (factor contextual).

**MFA (autenticación multifactor):** combinar dos o más factores de *categorías distintas*. Dos contraseñas no son MFA.

## Buenas prácticas con contraseñas

- Largas (frases de paso) mejor que complejas y cortas.
- Únicas para cada servicio.
- Usar un gestor de contraseñas.
- Almacenarlas con hash lento y salt (bcrypt, scrypt, Argon2), nunca en texto plano.
- Evitar la rotación forzada sin motivo; cambiar solo ante sospecha de compromiso.

## Modelos de control de acceso

| Modelo | Descripción |
|---|---|
| **DAC** (Discretionary) | El propietario del recurso decide quién accede |
| **MAC** (Mandatory) | El sistema impone políticas según etiquetas de clasificación |
| **RBAC** (Role-Based) | Los permisos se asignan a roles, y los roles a usuarios |
| **ABAC** (Attribute-Based) | Decisiones según atributos (usuario, recurso, contexto) |

## Protocolos y tecnologías habituales

- **Kerberos:** autenticación por tickets en entornos Windows/Active Directory.
- **LDAP / Active Directory:** directorios de identidades.
- **OAuth 2.0:** delegación de *autorización*.
- **OpenID Connect:** capa de *autenticación* sobre OAuth 2.0.
- **SAML:** federación de identidad (SSO) en entornos corporativos.
- **RADIUS / TACACS+:** AAA para acceso a red y dispositivos.

## Ataques comunes

- Fuerza bruta, password spraying, credential stuffing
- Phishing de credenciales
- Pass-the-Hash, Pass-the-Ticket
- Robo de tokens/sesiones
- Fatiga de MFA (bombardeo de notificaciones)
