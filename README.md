# Práctica RA5 - Instalación de aplicaciones web de escritorio
**Autor:** Lucas Aldave (`laldave@elpuig.xeill.net`)[cite: 1, 2]

---

## A5.1 - Filtres al Gmail

### Tabla de pruebas (A5.1)
| Qué envías | Qué esperas | Qué ha pasado |
| :--- | :--- | :--- |
| **1. Correo con `puig` en el asunto/cuerpo**[cite: 7] | Que llegue a la bandeja de entrada con la etiqueta verde `institut` aplicada[cite: 7]. | El mensaje ha llegado correctamente y se le ha asignado la etiqueta `institut` de color verde. |
| **2. Correo con `publicitat` en el asunto/cuerpo**[cite: 7] | Que no aparezca en la bandeja de entrada y vaya directo a `promocions`[cite: 7]. | El mensaje ha omitido la bandeja principal y se ha clasificado directamente en `promocions`. |
| **3. Correo desde la dirección de dos profesores**[cite: 7] | Que los correos se marquen automáticamente con el indicador de importante[cite: 7]. | Los mensajes han entrado marcados como importantes de forma automática. |
| **4. Correo normal desde una cuenta externa** | Que la cuenta responda automáticamente con el texto `Estic de vacances!`[cite: 7]. | La cuenta externa ha recibido la respuesta automática con el texto configurado. |

### Capturas de evidencia (A5.1)
* **Filtros y etiqueta `institut`:**
  `![Filtros Gmail](ruta/a/tu/captura_filtros.png)`
* **Respuesta automática de vacaciones:**
  `![Respuesta vacaciones](ruta/a/tu/captura_vacaciones.png)`

---

## A5.2 - Protocolos de correo (IMAP/POP3) y análisis de cabeceras

### 1. Parámetros de entrada y salida de Gmail
| Servicio | Servidor | Puerto | Cifrado / Seguridad |
| :--- | :--- | :--- | :--- |
| **Correo entrante (IMAP)** | `imap.gmail.com` | `993` | SSL/TLS |
| **Correo saliente (SMTP)** | `smtp.gmail.com` | `465` (SSL) o `587` (TLS) | SSL/TLS o STARTTLS |

### 2. Diferencia entre IMAP y POP3
El protocolo **IMAP** sincroniza los correos directamente en el servidor, permitiendo consultar y gestionar la misma bandeja desde varios dispositivos en tiempo real[cite: 1]. En cambio, **POP3** descarga los mensajes a un único dispositivo local y, por defecto, los borra del servidor, por lo que no se mantienen sincronizados entre diferentes equipos
