# Guía de Configuración - WhatsApp Chat Automation

## Paso 1: Preparar Credenciales

### OpenAI API
1. Ve a https://platform.openai.com/api-keys
2. Crea una nueva API key
3. Copia la clave (la necesitarás en n8n)

### Evolution API
1. Accede a tu instancia de Evolution API
2. Obtén tu API key y URL base
3. Configura tu instancia de WhatsApp

### PostgreSQL (Opcional)
Si deseas mantener historial de conversaciones:
1. Configura una base de datos PostgreSQL
2. Crea la tabla `conversaciones` con los campos necesarios
3. Obtén la cadena de conexión

## Paso 2: Importar en n8n

1. Abre tu instancia de n8n
2. Ve a "Workflows" → "Import"
3. Carga el archivo `workflow.json`
4. Haz clic en "Import"

## Paso 3: Configurar Credenciales en n8n

1. En el workflow, busca los nodos que requieren credenciales
2. Para cada nodo:
   - Haz clic en el nodo
   - Ve a la sección de credenciales
   - Selecciona "Create New" o usa credenciales existentes
   - Ingresa los datos correspondientes

### Nodos que requieren credenciales:

- **Transcribir Audio**: OpenAI API
- **Agente de IA**: OpenAI API
- **Analyze image**: OpenAI API
- **Obter média em base64**: Evolution API
- **Obter média em base**: Evolution API
- **Enviar Mensaje**: Evolution API

## Paso 4: Configurar el Webhook

1. En el nodo "Webhook1", copia la URL del webhook
2. En tu configuración de Evolution API, establece esta URL como webhook
3. Asegúrate de que los eventos de WhatsApp se envíen a este webhook

## Paso 5: Probar el Workflow

1. Activa el workflow (botón "Active" en la esquina superior derecha)
2. Envía un mensaje de prueba a tu número de WhatsApp
3. Verifica que recibas una respuesta automática

## Paso 6: Monitoreo

- Usa la sección "Executions" para ver el historial de ejecuciones
- Revisa los logs para diagnosticar problemas
- Monitorea el uso de la API de OpenAI en tu dashboard

## Troubleshooting

### El webhook no recibe mensajes
- Verifica que la URL del webhook sea correcta
- Comprueba que el workflow esté activo
- Revisa los logs de Evolution API

### Las respuestas no se envían
- Verifica las credenciales de Evolution API
- Comprueba que el número de WhatsApp esté configurado correctamente
- Revisa los errores en las ejecuciones

### Errores de OpenAI
- Verifica que tu API key sea válida
- Comprueba que tengas créditos disponibles
- Revisa los límites de rate limiting

## Personalización

### Cambiar el prompt del Agente de IA

1. Abre el nodo "Agente de IA"
2. Edita el campo "System Message"
3. Personaliza el comportamiento del chatbot según tus necesidades

### Agregar nuevos tipos de mensajes

1. Modifica el nodo "Switch" para agregar nuevas condiciones
2. Crea nuevos nodos para procesar esos tipos de mensajes
3. Conecta los nodos al flujo principal

## Recursos Útiles

- [Documentación de n8n](https://n8n.io/docs/)
- [API de OpenAI](https://platform.openai.com/docs/)
- [Evolution API Docs](https://evolution-api.gitbook.io/)

---

¿Necesitas ayuda? Revisa los logs del workflow para más detalles sobre los errores.
