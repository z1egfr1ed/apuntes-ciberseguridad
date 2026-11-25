# Tríada CIA y principios de seguridad

## La tríada CIA

Modelo base de la seguridad de la información. Cada ataque o control se puede analizar según cuál de estas propiedades afecta o protege.

| Propiedad | Qué garantiza | Ejemplo de ataque | Controles típicos |
|---|---|---|---|
| **Confidencialidad** | Solo acceden a la información quienes están autorizados | Robo de datos, sniffing, filtraciones | Cifrado, control de acceso, MFA |
| **Integridad** | La información no se altera sin autorización | Modificación de registros, man-in-the-middle | Hashes, firmas digitales, control de versiones |
| **Disponibilidad** | Los sistemas y datos están accesibles cuando se necesitan | DDoS, ransomware | Redundancia, backups, balanceo de carga |

## Extensiones habituales

- **Autenticidad:** verificar que alguien o algo es quien dice ser.
- **No repudio:** impedir que un emisor niegue haber realizado una acción (firmas digitales, logs firmados).
- **Trazabilidad / Accountability:** poder atribuir acciones a una identidad concreta (logging y auditoría).

## Principios de diseño seguro

- **Mínimo privilegio:** dar solo los permisos estrictamente necesarios.
- **Defensa en profundidad:** varias capas de control, no una sola.
- **Separación de funciones:** ninguna persona controla un proceso crítico de principio a fin.
- **Fallo seguro (fail-safe):** ante un error, el sistema debe quedar en un estado seguro.
- **Seguridad por diseño:** incorporar la seguridad desde el inicio, no al final.
- **Menor superficie de ataque:** deshabilitar o eliminar lo que no se usa.
- **Zero Trust:** nunca confiar por defecto, verificar siempre ("never trust, always verify").
- **Seguridad por oscuridad:** no es una medida válida por sí sola.

## Preguntas de repaso

- ¿Qué propiedad de la tríada se ve afectada por un ataque de ransomware? (Disponibilidad y, a menudo, confidencialidad si hay exfiltración)
- ¿Qué diferencia hay entre integridad y autenticidad?
