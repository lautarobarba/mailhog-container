# Mailhog

MailHog es una herramienta de pruebas de correo electrónico para desarrolladores.

## Descripción

Configura tu aplicación para usar MailHog como servidor SMTP, visualiza los mensajes en la interfaz web o recúpalos con la API JSON. También puedes liberar mensajes a servidores SMTP reales para entrega.

## Configuración

### Variables de entorno

Crea un archivo `.env` con las siguientes variables:

```bash
MAILHOG_SMTP_SERVER_PORT=1025
MAILHOG_WEB_PORT=8025
```

### Puertos

- **1025**: Servidor SMTP
- **8025**: Interfaz web

## Uso

### Iniciar los servicios

```bash
docker compose up -d
```

### Acceder a la interfaz web

Abre tu navegador en: `http://localhost:8025`

### Configurar tu aplicación

Configura tu aplicación para usar SMTP con los siguientes parámetros:

- **Host**: localhost
- **Puerto**: 1025
- **Usuario**: (vacío)
- **Contraseña**: (vacío)

### API REST

Obtener todos los mensajes:

```bash
curl http://localhost:8025/api/v2/messages
```

Obtener un mensaje específico:

```bash
curl http://localhost:8025/api/v1/messages/<id>
```

### Detener los servicios

```bash
docker compose down
```
