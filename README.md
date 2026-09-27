# 🤖 RAG Knowledge Bot

A Retrieval-Augmented Generation (RAG) application that combines **text embeddings, vector search, and an LLM** to answer questions using information retrieved from a knowledge base.

The project was built with **Python, Sentence Transformers, Supabase, Groq, and Streamlit**.

🔗 **Live App:** https://a-company-knowledge-bot.streamlit.app

---

## 📌 Project Overview

The RAG Knowledge Bot is designed to retrieve relevant information from stored documents before generating an answer.

Instead of relying only on the language model's existing knowledge, the application:

1. Converts text into numerical embeddings.
2. Stores the embeddings in a vector database.
3. Converts the user's question into an embedding.
4. Searches for similar information in the database.
5. Sends the retrieved context to the LLM.
6. Generates an answer based on the retrieved information.

### RAG Workflow

```text
User Question
      ↓
Generate Embedding
      ↓
Vector Similarity Search
      ↓
Retrieve Relevant Documents
      ↓
Send Context + Question to LLM
      ↓
Generate Answer
🛠️ Technologies Used
Python
Sentence Transformers – text embeddings
Supabase – database and vector search
pgvector – vector similarity search
Groq – LLM inference
Streamlit – web interface
python-dotenv – environment variable management
📂 Project Structure
RAG-Knowledge-Bot/
│
├── app.py
├── requirements.txt
├── supabase_setup.sql
├── README.md
├── .gitignore
└── screenshots/
File Descriptions
File	Description
app.py	Main Streamlit application and RAG pipeline
requirements.txt	Python dependencies
supabase_setup.sql	Supabase database and vector search setup
README.md	Project documentation
.gitignore	Prevents sensitive and unnecessary files from being committed
screenshots/	Project screenshots
🧠 Embeddings

Embeddings represent text as numerical vectors that capture semantic meaning.

This allows the application to compare the meaning of a user's question with stored document content and identify relevant information.

🔎 Vector Search

The project uses Supabase with pgvector to store and search vector embeddings.

When a user submits a question, the application generates an embedding for that question and performs a similarity search against the stored document embeddings.

This makes it possible to find information that is semantically related to the question rather than relying only on exact keyword matches.

🔗 Retrieval-Augmented Generation

The application follows a RAG workflow:

Question
   ↓
Embedding
   ↓
Similarity Search
   ↓
Relevant Context
   ↓
LLM
   ↓
Grounded Response

The retrieved information is passed to the language model as context so that the generated response is based on the available knowledge base.

💬 Streamlit Interface

The project includes a Streamlit chat interface where users can:

Enter questions
Retrieve relevant information
Receive AI-generated responses
View supporting source information where available
⚙️ Environment Variables

Create a .env file in the project directory:

GROQ_API_KEY=your_groq_api_key
SUPABASE_URL=your_supabase_url
SUPABASE_SERVICE_KEY=your_supabase_service_key

Do not upload your .env file to GitHub.

For deployment, configure these values using the platform's secrets/environment-variable settings.

🚀 Running the Project Locally
1. Clone the repository
git clone https://github.com/ajeksmarvins/Week11-RAG-Knowledge-Bot.git
cd Week11-RAG-Knowledge-Bot
2. Create a virtual environment
python -m venv venv

Activate it on Windows:

venv\Scripts\activate
3. Install dependencies
pip install -r requirements.txt
4. Configure Supabase

Run the SQL commands in:

supabase_setup.sql

inside the Supabase SQL Editor.

5. Configure environment variables

Create your .env file and add:

GROQ_API_KEY=your_groq_api_key
SUPABASE_URL=your_supabase_url
SUPABASE_SERVICE_KEY=your_supabase_service_key
6. Run the application
streamlit run app.py

The application will open in your browser.

☁️ Deployment

The application was deployed using Streamlit Community Cloud.

🔗 Live Application:
https://a-company-knowledge-bot.streamlit.app

For deployment:

Connect the GitHub repository to Streamlit Community Cloud.
Select app.py as the main application file.
Add the required environment variables/secrets.
Deploy the application.
🔐 Security

Sensitive credentials should never be committed to the repository.

The following should remain private:

Groq API key
Supabase URL credentials
Supabase service key
.env file

Use environment variables locally and deployment secrets in the hosted application.

🎯 Learning Objectives

This project helped me understand and practice:

Text embeddings
Semantic similarity
Vector databases
Supabase and pgvector
Retrieval-Augmented Generation (RAG)
LLM integration
Streamlit application development
AI application deployment
📚 What I Learned

Building this project helped me understand that practical AI applications are not only about generating responses.

The process also involves:

representing information → storing it → retrieving relevant information → providing context → generating a response.

This project gave me hands-on experience connecting these components into a working AI application.

🔗 Project Links

Live App:
https://a-company-knowledge-bot.streamlit.app

GitHub Repository:
https://github.com/ajeksmarvins/Week11-RAG-Knowledge-Bot

👨‍💻 Author

Ajekuko Marvellous

Advanced AI Automation Engineering 2026