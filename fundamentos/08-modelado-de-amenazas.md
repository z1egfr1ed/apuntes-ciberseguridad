# Modelado de amenazas

Proceso estructurado para identificar qué puede salir mal, qué es importante proteger y cómo priorizar las defensas. Idealmente se hace **en la fase de diseño**.

## Las cuatro preguntas básicas

1. ¿Qué estamos construyendo? (diagramas, flujos de datos)
2. ¿Qué puede salir mal? (amenazas)
3. ¿Qué vamos a hacer al respecto? (mitigaciones)
4. ¿Hemos hecho un buen trabajo? (validación)

## Pasos generales

1. **Definir el alcance y los activos.**
2. **Diagramar el sistema:** DFD (Data Flow Diagram) con procesos, almacenes de datos, entidades externas y *límites de confianza*.
3. **Identificar amenazas** con una metodología (STRIDE, por ejemplo).
4. **Evaluar y priorizar** según probabilidad e impacto.
5. **Definir mitigaciones.**
6. **Documentar y revisar** periódicamente.

## STRIDE

Metodología de Microsoft. Cada letra es una categoría de amenaza y se relaciona con una propiedad de seguridad vulnerada.

| Letra | Amenaza | Propiedad afectada | Ejemplo |
|---|---|---|---|
| **S** | Spoofing (suplantación) | Autenticidad | Usar credenciales robadas |
| **T** | Tampering (manipulación) | Integridad | Alterar datos en tránsito |
| **R** | Repudiation (repudio) | No repudio | Negar haber realizado una acción sin logs |
| **I** | Information disclosure | Confidencialidad | Filtración de datos |
| **D** | Denial of Service | Disponibilidad | Saturar el servicio |
| **E** | Elevation of privilege | Autorización | Pasar de usuario a admin |

## Otras metodologías

- **DREAD:** puntuación de riesgo (Damage, Reproducibility, Exploitability, Affected users, Discoverability).
- **PASTA:** modelo de siete etapas centrado en el riesgo y el negocio.
- **Attack Trees:** árboles con el objetivo del atacante en la raíz y las formas de lograrlo como ramas.
- **MITRE ATT&CK:** base de conocimiento de tácticas y técnicas reales de atacantes.
- **LINDDUN:** enfocado en amenazas a la privacidad.

## Herramientas

- Microsoft Threat Modeling Tool
- OWASP Threat Dragon
- draw.io / diagrams.net para los DFD
