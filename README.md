# WhatsApp Chat Automation

Automatización de WhatsApp con inteligencia artificial usando n8n. Este workflow implementa un chatbot inteligente para gestionar conversaciones automáticas en WhatsApp.

## 📋 Descripción

Este workflow de n8n automatiza las conversaciones en WhatsApp con:

- **Agente de IA**: Responde automáticamente a mensajes usando OpenAI
- **Procesamiento de Audio**: Transcribe mensajes de audio a texto
- **Análisis de Imágenes**: Analiza imágenes enviadas por los usuarios
- **Memoria de Conversación**: Mantiene contexto de conversaciones anteriores
- **Enrutamiento Inteligente**: Dirige mensajes según su tipo (texto, audio, imagen)

## 🚀 Características

- ✅ Respuestas automáticas con IA
- ✅ Transcripción de audio a texto
- ✅ Análisis y descripción de imágenes
- ✅ Gestión de contexto de conversación
- ✅ Integración con Evolution API para WhatsApp
- ✅ Integración con OpenAI para procesamiento de lenguaje

## 📦 Requisitos

- Cuenta en n8n
- Credenciales de OpenAI API
- Credenciales de Evolution API (para WhatsApp)
- Base de datos PostgreSQL (opcional, para memoria persistente)

## 🔧 Instalación

1. Accede a tu instancia de n8n
2. Importa el archivo `workflow.json`
3. Configura las credenciales necesarias:
   - OpenAI API Key
   - Evolution API credentials
   - PostgreSQL connection (si usas memoria persistente)

## 📝 Configuración

### Variables de Entorno

```bash
OPENAI_API_KEY=tu_clave_aqui
EVOLUTION_API_KEY=tu_clave_aqui
EVOLUTION_API_URL=tu_url_aqui
```

### Nodos Principales

- **Webhook1**: Recibe mensajes de WhatsApp
- **Switch**: Enruta según tipo de mensaje
- **Agente de IA**: Procesa y responde mensajes
- **Enviar Mensaje**: Envía respuesta a WhatsApp

## 🎯 Casos de Uso

- Soporte al cliente automático
- Ventas y consultas de productos
- Información y atención general
- Procesamiento de órdenes

## 📞 Soporte

Para más información sobre n8n, visita: https://n8n.io/docs/

## 📄 Licencia

Este proyecto está disponible bajo licencia abierta.

## 👤 Autor

Creado por: Yesid Fernando Cepeda B.

---

**Última actualización**: 2026-01-16
