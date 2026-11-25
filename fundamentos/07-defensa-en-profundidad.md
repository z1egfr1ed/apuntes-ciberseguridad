# Defensa en profundidad y tipos de controles

## Defensa en profundidad

Estrategia de varias capas de protección independientes: si una falla, las otras siguen protegiendo.

```
┌─────────────────────────────────────────┐
│ Políticas, procedimientos y formación   │
│ ┌─────────────────────────────────────┐ │
│ │ Seguridad física                    │ │
│ │ ┌─────────────────────────────────┐ │ │
│ │ │ Perímetro (firewall, IDS/IPS)   │ │ │
│ │ │ ┌─────────────────────────────┐ │ │ │
│ │ │ │ Red interna (segmentación)  │ │ │ │
│ │ │ │ ┌─────────────────────────┐ │ │ │ │
│ │ │ │ │ Host (EDR, hardening)   │ │ │ │ │
│ │ │ │ │ ┌─────────────────────┐ │ │ │ │ │
│ │ │ │ │ │ Aplicación          │ │ │ │ │ │
│ │ │ │ │ │ ┌─────────────────┐ │ │ │ │ │ │
│ │ │ │ │ │ │ Datos (cifrado) │ │ │ │ │ │ │
│ │ │ │ │ │ └─────────────────┘ │ │ │ │ │ │
│ │ │ │ │ └─────────────────────┘ │ │ │ │ │
│ │ │ │ └─────────────────────────┘ │ │ │ │
│ │ │ └─────────────────────────────┘ │ │ │
│ │ └─────────────────────────────────┘ │ │
│ └─────────────────────────────────────┘ │
└─────────────────────────────────────────┘
```

## Tipos de controles

### Por naturaleza

| Tipo | Ejemplos |
|---|---|
| **Administrativos** | Políticas, procedimientos, formación, gestión de riesgos |
| **Técnicos (lógicos)** | Firewalls, cifrado, MFA, antivirus, ACLs |
| **Físicos** | Cerraduras, cámaras, vigilantes, control de acceso a salas |

### Por función

| Función | Objetivo | Ejemplos |
|---|---|---|
| **Preventivo** | Evitar que ocurra el incidente | Firewall, MFA, parches |
| **Detectivo** | Identificar que ocurrió o está ocurriendo | IDS, SIEM, cámaras, auditorías |
| **Correctivo** | Reducir el impacto y restaurar | Backups, plan de respuesta, restauración |
| **Disuasorio** | Desalentar al atacante | Carteles de aviso, banners legales |
| **Compensatorio** | Sustituir un control que no se puede aplicar | Segmentación si no se puede parchear |
| **De recuperación** | Volver a la operación normal | Sitios alternativos, DRP |

## Herramientas de seguridad de red (visión general)

- **Firewall:** filtra tráfico según reglas (stateless, stateful, NGFW, WAF).
- **IDS:** detecta actividad sospechosa y alerta.
- **IPS:** detecta y bloquea.
- **Proxy / Proxy inverso:** intermediarios para filtrado y protección.
- **VPN:** túnel cifrado entre redes o dispositivos.
- **DMZ:** zona intermedia para servicios expuestos a Internet.
- **Segmentación / VLANs:** separar la red para limitar el movimiento lateral.
- **SIEM:** centraliza y correlaciona logs.
- **EDR/XDR:** detección y respuesta en endpoints y otras fuentes.

## Hardening (endurecimiento)

- Eliminar software y servicios innecesarios.
- Cambiar credenciales por defecto.
- Aplicar parches con regularidad.
- Aplicar configuraciones seguras (ej. benchmarks CIS).
- Habilitar logging y monitorización.
