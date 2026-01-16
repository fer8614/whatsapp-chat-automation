# WhatsApp Chat Automation

Automated WhatsApp messaging with artificial intelligence using n8n. This workflow implements an intelligent chatbot to manage automatic conversations on WhatsApp.

## 📋 Description

This n8n workflow automates WhatsApp conversations with:

- **AI Agent**: Automatically responds to messages using OpenAI
- **Audio Processing**: Transcribes audio messages to text
- **Image Analysis**: Analyzes images sent by users
- **Conversation Memory**: Maintains context from previous conversations
- **Intelligent Routing**: Directs messages based on their type (text, audio, image)

## 🚀 Features

- ✅ Automatic responses with AI
- ✅ Audio to text transcription
- ✅ Image analysis and description
- ✅ Conversation context management
- ✅ Integration with Evolution API for WhatsApp
- ✅ Integration with OpenAI for language processing

## 📦 Requirements

- n8n account
- OpenAI API credentials
- Evolution API credentials (for WhatsApp)
- PostgreSQL database (optional, for persistent memory)

## 🔧 Installation

1. Access your n8n instance
2. Import the `workflow.json` file
3. Configure the necessary credentials:
   - OpenAI API Key
   - Evolution API credentials
   - PostgreSQL connection (if using persistent memory)

## 📝 Configuration

### Environment Variables

```bash
OPENAI_API_KEY=your_key_here
EVOLUTION_API_KEY=your_key_here
EVOLUTION_API_URL=your_url_here
```

### Main Nodes

- **Webhook1**: Receives WhatsApp messages
- **Switch**: Routes based on message type
- **AI Agent**: Processes and responds to messages
- **Send Message**: Sends response to WhatsApp

## 🎯 Use Cases

- Automatic customer support
- Sales and product inquiries
- General information and support
- Order processing

## 📞 Support

For more information about n8n, visit: https://n8n.io/docs/

## 📄 License

This project is available under an open license.

## 👤 Author

Created by: Yesid Fernando Cepeda B.

---

**Last updated**: 2026-01-16
