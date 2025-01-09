# Chat application using RAG (Retrieval-augmented generation) and LangChain

### Importance of RAG and how it is better than fine-tuning the LLM or building it from scratch

1. Fine-tuning is much more expensive as it requires trillions and trillions of data to train the LLM and also takes a lot of time.
2. Fine-tuning needs custom serving and maintenance.
3. Fine-tuning doesn't give you the auto-update feature.

### RAG Workflow:

1. **Retrieve**: Extract relevant information from a knowledge base or documents.
2. **Generate**: Use an LLM to generate human-like responses based on the retrieved information.

### Key Components of this Project:

1. **Knowledge Base/Vector Store** - To store the relevant documents in a searchable format (vector embeddings).
2. **LLM (Language Model)** - For generating intelligent and context-related answers.
3. **LangChain** - Acts as the glue to connect components (retriever, LLM, database).
4. **Frontend** - Using Streamlit

## Imported libraries

- **os**: Provides functions to interact with the operating system, such as accessing environment variables.
- **dotenv**: Loads environment variables from a .env file into the Python environment.
- **Path**: A module from pathlib used for manipulating file paths in a cross-platform manner.
- **AIMessage**: Represents a message from the AI in a conversational context within LangChain.
- **HumanMessage**: Represents a message from the human user in a conversation with the AI within LangChain.
- **TextLoader**: A document loader for reading and processing text files into LangChain.
- **WebBaseLoader**: A document loader for fetching content from a web page into LangChain.
- **PyPDFLoader**: A document loader for extracting text from PDF files.
- **Docx2txtLoader**: A document loader for extracting text from .docx files.
- **Chroma**: A vector store used in LangChain to index and retrieve document embeddings for search and retrieval.
- **RecursiveCharacterTextSplitter**: A text splitter that breaks documents into smaller chunks based on character length to fit within model input limits.
- **OpenAIEmbeddings**: Generates vector embeddings using OpenAI models, which are used for document similarity and search.
- **ChatOpenAI**: An OpenAI model wrapper for generating responses in a conversational context using GPT models.
- **ChatAnthropic**: A wrapper for Anthropic's models, enabling conversational interactions with them.
- **ChatPromptTemplate**: A LangChain utility for creating structured prompt templates for ChatGPT-like models.
- **MessagesPlaceholder**: A placeholder for inserting dynamically generated messages within a prompt or conversation chain.
- **create_history_aware_retriever**: A function that creates a retriever capable of considering historical context when retrieving documents.
- **create_retrieval_chain**: Constructs a retrieval-based chain that can process queries and fetch relevant documents from a vector store.
- **create_stuff_documents_chain**: Creates a chain that processes and combines documents, useful for document summarization or question answering.
