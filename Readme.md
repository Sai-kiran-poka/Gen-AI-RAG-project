### README for FastAPI LLM-based Query API

# FastAPI LLM-based Query API

This project sets up a FastAPI application that leverages a language model to handle inquiries related to animals' laws, acts, and overall well-being. It uses various modules for loading, processing, and querying a document to generate responses based on input questions.

## Overview of Modules

### FastAPI
- **FastAPI**: A modern, fast (high-performance) web framework for building APIs with Python.

### Pydantic
- **Pydantic**: Used for data validation and settings management using Python type annotations.

### LangChain Community Modules
- **Chroma**: A vector store used to store and retrieve document embeddings.
- **PyPDFLoader**: Loads PDF documents.
- **RecursiveCharacterTextSplitter**: Splits the document into manageable chunks for processing.

### LangChain Schema & Core
- **StrOutputParser**: Parses the output from the language model.
- **RunnablePassthrough**: A utility to pass data through the chain.
- **ChatPromptTemplate**: Defines the prompt template used to interact with the language model.

### HuggingFace
- **HuggingFaceEndpoint**: Interacts with the HuggingFace model endpoint.
- **HuggingFaceEmbeddings**: Embeddings model from HuggingFace.

### Additional Modules
- **os**: Provides a way of using operating system dependent functionality.
- **huggingface_hub**: Used for logging into HuggingFace to access the models.

## Project Initialization

### Prerequisites

- Python 3.8+
- Pip (Python package installer)

### Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/your-username/fastapi-llm-query.git
    cd fastapi-llm-query
    ```

2. Create a virtual environment and activate it:
    ```sh
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3. Install the required packages:
    ```sh
    pip install -r requirements.txt
    ```


### Running the Application

1. Ensure you have the PDF document (`animal.pdf`) in the project directory.
2. Start the FastAPI server:
    ```sh
    uvicorn main:app --reload
    ```

### Testing the API

Use a tool like Postman or cURL to test the API endpoint:

```sh
curl -X POST http://127.0.0.1:5000/api/query -H "Content-Type: application/json" -d '{"question":"What are the animal laws in India?"}'
```

### Project Structure

```
fastapi-llm-query/
│
├── main.py                 # Main application file
├── animal.pdf              # PDF document to be processed
├── requirements.txt        # Project dependencies
├── chroma_db_animals_huggingface/  # Directory to store vectorstore data
├── venv/                   # Virtual environment directory
└── README.md               # This README file
```

### Dependencies

- `fastapi`
- `pydantic`
- `langchain-community`
- `langchain-core`
- `langchain-huggingface`
- `uvicorn`
- `huggingface-hub`








## FRONT-END
# Chatbot Application

This is a React-based chatbot application that utilizes OpenAI's GPT model to generate responses to user inputs. The chatbot interface allows users to communicate with an AI in real-time.

## Features

- User-friendly chat interface
- Real-time response generation using OpenAI's GPT model
- Timestamps for each message
- Loading indicator while the AI generates a response

## Getting Started

### Prerequisites

- Node.js and npm installed
- OpenAI API key

### Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/your-username/chatbot-app.git
    cd chatbot-app
    ```

2. Install the dependencies:

    ```bash
    npm install
    ```

3. Create a `.env` file in the root directory and add your OpenAI API key:

    ```
    VITE_APP_OPENAI_API_KEY=your_openai_api_key
    ```

4. Start the development server:

    ```bash
    npm run dev
    ```

### Usage

- Open your browser and go to `http://localhost:3000`.
- Type a message in the input box and press Enter or click the send button.
- The chatbot will respond in real-time.

### Project Structure

- `src/components/GenerateAns.js`: Main component handling the chat interface and API calls.
- `src/components/Loader.js`: Loader component displayed while waiting for the AI response.
- `public/index.html`: Main HTML file.
- `src/index.js`: Entry point of the application.

### Dependencies

- `axios`: For making HTTP requests.
- `react`: JavaScript library for building user interfaces.
- `react-icons`: Collection of icons for React.
- `vite`: Next-generation front-end tooling.

### Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

### License

This project is licensed under the MIT License.

