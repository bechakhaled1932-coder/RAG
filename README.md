# ENISo AI Pilot — Intelligent Administrative Assistant

An AI-powered administrative assistant designed to help ENISo students access institutional information through a multilingual conversational interface.

ENISo AI Pilot uses Retrieval-Augmented Generation (RAG) to retrieve relevant information from a knowledge base and generate context-aware answers using Large Language Models (LLMs).

## Features

- **Retrieval-Augmented Generation (RAG):** grounds answers in relevant retrieved documents.
- **Multilingual support:** automatic language detection for more than six languages.
- **LLM integration:** support for locally hosted models through Ollama and API-based inference through Groq.
- **Semantic search:** vector-based document retrieval using ChromaDB.
- **Authentication:** JWT-based user authentication.
- **Conversation persistence:** MongoDB integration for storing conversation history.
- **Interactive interface:** Streamlit-based user interface.
- **Local inference:** designed to support local model execution, including Mistral 7B.

## Technology Stack

| Category | Technologies |
|---|---|
| Language | Python |
| LLM orchestration | LangChain, LangGraph |
| Local inference | Ollama, Mistral 7B |
| API-based inference | Groq |
| Vector database | ChromaDB |
| Embeddings | Sentence Transformers, Hugging Face |
| Frontend | Streamlit |
| Authentication | JWT |
| Persistence | MongoDB |
| Deployment | Streamlit Cloud |

## Architecture

The application follows a RAG-based workflow:

1. **User input:** the student submits a question.
2. **Language detection:** the application identifies the user's language.
3. **Document retrieval:** ChromaDB retrieves relevant information from the knowledge base.
4. **Context construction:** retrieved passages are combined with the user's question.
5. **Answer generation:** an LLM generates a context-aware response.
6. **Conversation management:** the application handles authentication and conversation persistence.

## Getting Started

### Prerequisites

- Python compatible with the project's dependencies.
- Git.
- An Ollama installation and a supported local model, if using local inference.
- A Groq API key, if using Groq inference.
- Access to MongoDB, if required by the selected application configuration.

### Installation

Clone the repository:

```bash
git clone (https://github.com/bechakhaled1932-coder/RAG.git)
cd <REPOSITORY_DIRECTORY>
```

Create and activate a virtual environment.

**Windows:**

```powershell
python -m venv .venv
.venv\Scripts\activate
```

**Linux / macOS:**

```bash
python3 -m venv .venv
source .venv/bin/activate
```

Install the dependencies:

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

### Configuration

Configure the environment variables required by your application. Store credentials and API keys in a local `.env` file when supported.

Never commit secrets, private keys, database credentials, or API tokens to version control.

### Running the Application

Once the application's entry point and configuration have been identified, launch the application using the command corresponding to its actual implementation.

For example, if the Streamlit entry point is `app.py`:

```bash
streamlit run app.py
```

## Project Structure

The repository structure will be documented here once the source files have been reviewed.

```text
ENISo-AI-Pilot/
├── requirements.txt
├── README.md
├── .gitignore
├── .env.example
└── ...
```

## Security

- Keep API keys and authentication secrets outside the source code.
- Do not commit `.env` files containing real credentials.
- Review authentication, session management, and database access before deploying the application publicly.

## Future Improvements

Potential improvements include enhanced retrieval quality, document citation, evaluation of generated answers, and additional administrative knowledge sources.

## License

Specify the project's license before distributing or reusing the code.
