# Práctica RA5 - Lucas Aldave

---

## A5.1 - Filtres al Gmail

| Qué envías | Qué esperas | Qué ha pasado |
| :--- | :--- | :--- |
| 1. Correo con `puig` en el asunto | Que llegue con la etiqueta verde `institut` | Ha llegado con la etiqueta verde `institut` aplicada |
| 2. Correo con `publicitat` | Que no salga en recibidos y vaya a `promocions` | No ha salido en recibidos y ha ido directo a `promocions` |
| 3. Correo de dos profesores | Que se marque siempre como importante | Se ha marcado automáticamente como importante |
| 4. Correo desde otra cuenta | Que responda solo con `Estic de vacances!` | Se ha enviado la respuesta automática correctamente |

---

## A5.2 - Protocolos IMAP/POP3 y Cabeceras

### 1. Parámetros de entrada y salida de Gmail
| Servicio | Servidor | Puerto | Seguridad |
| :--- | :--- | :--- | :--- |
| Entrada (IMAP) | imap.gmail.com | 993 | SSL/TLS |
| Salida (SMTP) | smtp.gmail.com | 465 / 587 | SSL / TLS |

### 2. Diferencia entre IMAP y POP3
El protocolo IMAP sincroniza los correos directamente en el servidor, permitiendo consultar y gestionar la misma bandeja desde varios dispositivos en tiempo real. En cambio, POP3 descarga los mensajes a un único dispositivo local y, por defecto, los borra del servidor, por lo que no se mantienen sincronizados entre diferentes equipos.

### 3. Datos del mensaje original
* **SPF:** PASS (IP: 209.85.220.41)
* **DKIM:** PASS (Dominio: elpuig-xeill-net.20260707.gappssmtp.com)
* **DMARC:** PASS

**Saltos de servidor (4 servidores):**
1. Origen interno Google: `2002:a17:907:2d28:b0:c50:53cb:69fe` (03:32:09)
2. Servidor de salida Google: `mail-sor-f41.google.com` / `209.85.220.41` (03:32:09)
3. Procesamiento interno Google: `2002:a17:907:1b16:b0:c3f:7e8:235d` (03:32:10)
4. Entrega final al buzón: `2002:a05:6638:ad50:b0:620:3445:ffc7` para `laldave@elpuig.xeill.net` (03:32:10)

### 4. Tabla de pruebas (A5.2)
| Qué pruebas | Cómo lo pruebas | Qué esperas | Qué ha pasado |
| :--- | :--- | :--- | :--- |
| 1. Acceso IMAP | Mirando la configuración de correo POP/IMAP en Gmail | Que esté activado | Está activado |
| 2. Dos sesiones | Abriendo dos ventanas con dos cuentas distintas | Poder usar las dos cuentas a la vez | Funcionan las dos a la vez sin problema |
| 3. Filtro `puig` | Enviando un correo de la cuenta A a la B con `puig` | Que llegue con la etiqueta `institut` | Ha llegado con la etiqueta `institut` |
| 4. Respuesta | Respondiendo desde la cuenta B a la A | Que la respuesta llegue a la cuenta A | Ha llegado correctamente a la cuenta A |
| 5. SPF, DKIM y DMARC | Pulsando en "Mostrar original" en el correo recibido | Que los tres pongan PASS | Los tres salen como PASS |
| 6. Servidores | Mirando las líneas `Received` en el original | Ver por cuántos servidores ha pasado | Ha pasado por 4 servidores |

---

## A5.3 - Viaje de 7 días (Google Maps y Calendar)

* **Destino:** 24 Horas de Le Mans (Francia), ida y vuelta desde Barcelona
* **Fechas:** Del 9 al 15 de julio de 2028
* **Calendario:** CALENDARI_LUCAS_ALDAVE
* **Enlace Google Maps:** (Pega aquí tu enlace de Google Maps)

### Presupuesto (Máximo 1.500 €)
* **Vuelo ida y vuelta Barcelona – Lyon (Iberia):** 83 €
* **Hotel Lyon (Lagrange Apart'HOTEL, 2 noches):** 110 €
* **Traslados y Tren TGV París – Le Mans (ida y vuelta):** 180 €
* **Entrada Oficial Semana Completa + Grada:** 219 €
* **Hotel Le Mans (Eklo Hôtels, 5 noches a 37 €):** 185 €
* **Comidas, bebida y extras:** 280 €
* **Total:** 1.057 €

* <iframe src="https://calendar.google.com/calendar/embed?src=laldave%40elpuig.xeill.net&ctz=Europe%2FMadrid&dates=20280709%2F20280716&mode=WEEK" style="border: 0" width="800" height="600" frameborder="0" scrolling="no"></iframe>
