# Conceptos básicos

## Vocabulario esencial

| Término | Definición | Ejemplo |
|---|---|---|
| **Activo** | Cualquier cosa con valor para la organización | Base de datos de clientes, servidor, reputación |
| **Amenaza** | Posible causa de un incidente que dañe un activo | Un atacante, un malware, un desastre natural |
| **Vulnerabilidad** | Debilidad que puede ser aprovechada por una amenaza | Software sin parchear, contraseña débil |
| **Exploit** | Código o técnica que aprovecha una vulnerabilidad | Script que explota un desbordamiento de búfer |
| **Riesgo** | Probabilidad de que una amenaza explote una vulnerabilidad × impacto | Riesgo alto de filtración por un servidor expuesto |
| **Ataque** | Acción deliberada que intenta explotar una vulnerabilidad | Phishing, inyección SQL |
| **Incidente** | Evento que compromete la seguridad | Acceso no autorizado confirmado |
| **Payload** | Parte del exploit que ejecuta la acción maliciosa | Reverse shell |
| **Vector de ataque** | Camino que usa el atacante para llegar al objetivo | Correo, USB, servicio web expuesto |
| **Superficie de ataque** | Conjunto de todos los puntos de entrada posibles | Puertos abiertos, apps web, empleados |
| **Zero-day** | Vulnerabilidad desconocida para el fabricante, sin parche | CVE explotado antes de ser publicado |
| **IoC** | Indicador de compromiso: evidencia de que hubo intrusión | Hash de malware, IP maliciosa |
| **TTP** | Tácticas, técnicas y procedimientos de un atacante | Descritos en MITRE ATT&CK |

## Relación entre los conceptos

```
Amenaza ──explota──▶ Vulnerabilidad ──afecta──▶ Activo
                                                  │
                                         Riesgo = Probabilidad × Impacto
```

## Gestión del riesgo

Opciones ante un riesgo identificado:

- **Mitigar:** aplicar controles para reducirlo.
- **Transferir:** trasladarlo a un tercero (seguros, outsourcing).
- **Aceptar:** asumirlo de forma consciente cuando es bajo o inevitable.
- **Evitar:** eliminar la actividad que lo genera.

## Vulnerabilidades: CVE, CVSS, CWE

- **CVE:** identificador público de una vulnerabilidad concreta (ej. `CVE-2021-44228`, Log4Shell).
- **CVSS:** puntuación de severidad de 0.0 a 10.0 (Baja, Media, Alta, Crítica).
- **CWE:** catálogo de *tipos* de debilidades de software (ej. CWE-79: XSS).
- **NVD:** base de datos nacional de vulnerabilidades de EE. UU. (https://nvd.nist.gov).

## Ciclo de vida de una vulnerabilidad

1. Descubrimiento
2. Divulgación (responsable o pública)
3. Publicación del parche
4. Aplicación del parche
5. Explotación activa (puede ocurrir antes de la divulgación en el caso de un zero-day)
