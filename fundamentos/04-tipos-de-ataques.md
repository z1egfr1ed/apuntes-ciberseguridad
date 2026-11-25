# Tipos de ataques

## Ingeniería social

Manipulan a las personas, no a los sistemas.

- **Phishing:** correos fraudulentos que suplantan a entidades legítimas.
  - *Spear phishing:* dirigido a una persona concreta.
  - *Whaling:* dirigido a directivos.
  - *Smishing / Vishing:* por SMS / por llamada telefónica.
- **Pretexting:** inventar un escenario creíble para obtener información.
- **Baiting:** dejar un cebo (ej. USB infectado).
- **Tailgating / Piggybacking:** colarse tras una persona autorizada en un acceso físico.
- **Shoulder surfing:** mirar por encima del hombro para ver credenciales.

## Ataques a contraseñas

- **Fuerza bruta:** probar todas las combinaciones posibles.
- **Ataque de diccionario:** probar palabras de una lista.
- **Password spraying:** probar pocas contraseñas comunes contra muchas cuentas.
- **Credential stuffing:** reutilizar credenciales filtradas de otros servicios.
- **Rainbow tables:** tablas precalculadas de hashes (se mitigan con *salt*).

## Ataques de red

- **Sniffing:** captura de tráfico.
- **Man-in-the-Middle (MitM):** el atacante se interpone entre dos partes.
- **ARP spoofing / DNS spoofing:** falsificación de resoluciones para redirigir tráfico.
- **DoS / DDoS:** saturar un servicio para dejarlo no disponible.
- **Port scanning:** reconocimiento de puertos y servicios abiertos.
- **Session hijacking:** robar una sesión activa.

## Ataques a aplicaciones web

- **Inyección SQL (SQLi):** manipular consultas a la base de datos.
- **Cross-Site Scripting (XSS):** inyectar scripts en páginas vistas por otros usuarios.
- **CSRF:** forzar a un usuario autenticado a ejecutar acciones no deseadas.
- **Inclusión de archivos (LFI/RFI)**, **SSRF**, **XXE**, **deserialización insegura**.
- Referencia principal: [OWASP Top 10](https://owasp.org/www-project-top-ten/).

## Ataques a software y sistemas

- **Desbordamiento de búfer (buffer overflow).**
- **Escalada de privilegios:** de usuario normal a administrador.
- **Movimiento lateral:** saltar de un equipo a otro dentro de una red.
- **Ataques a la cadena de suministro:** comprometer a un proveedor o dependencia.
- **Ataques de día cero (zero-day).**

## Ataques de criptografía

- **Downgrade attacks:** forzar el uso de protocolos más débiles.
- **Ataques de colisión sobre hashes débiles (MD5, SHA-1).**
- **Side-channel:** obtener información por tiempo, consumo, etc.

## Cyber Kill Chain (Lockheed Martin)

Fases típicas de un ataque dirigido:

1. Reconocimiento
2. Armamento
3. Entrega
4. Explotación
5. Instalación
6. Comando y control (C2)
7. Acciones sobre el objetivo
