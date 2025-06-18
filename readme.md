# Domain Deep Research Agent Guide

Este guía proporciona pasos detallados para crear un agente de investigación de dominio profundo que utiliza Composio, agentic frameworks como Langgraph y OpenAI para crear un agente de investigación.

## Pasos a seguir para crear el agente:
1. Crea un entorno virtual de Python.
2. Instala las dependencias necesarias.
3. Solicita iniciar sesión en Composio y añadir las integraciones requeridas (Tavily, PerplexityAI, GoogleDocs).
4. Cuando añadas la integración de Google Docs, Composio te preguntará cómo quieres autenticarte (OAUTH2 o BEARER TOKEN). Debes elegir OAUTH2 y seguir las instrucciones que aparecerán en pantalla para completar la autenticación.
5. Crea el archivo .env (o copia el de ejemplo) y te pide rellenar las variables necesarias.

```
uv venv

source .venv/Scripts/activate # Windows
source .venv/bin/activate # macOS/Linux

# Login to your account
composio login

composio add tavily
composio add perplexityai
composio add googledocs

```

Edit .env file with the necessary environment variables.
(you can use the .env.example file as a reference)

Run the agent:
```
python main.py
```

## Interactuar con el agente
El agente te pedirá que introduzcas un tema y un dominio.
Espera a que genere las preguntas y realice la investigación.
El informe final se creará en Google Docs.

## Notas:
- El agente utiliza:
    - la API de OpenAI para generar las preguntas y realizar la investigación.
    - la API de Google Docs para crear el informe final.
    - la API de Tavily para obtener información de la web.
    - la API de PerplexityAI para obtener información de la web.
