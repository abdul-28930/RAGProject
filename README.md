# AI Documentation Assistant (RAG Project)

A Retrieval-Augmented Generation (RAG) system that provides intelligent assistance for AI framework documentation, specifically focusing on Pydantic AI, Hugging Face, and LangChain.

## 🌟 Features

- **Smart Documentation Search**: Uses embeddings and semantic search to find relevant documentation
- **Interactive Chat Interface**: Streamlit-based UI for natural conversation
- **Multi-Framework Support**: Covers multiple AI frameworks in one place
- **Real-time Response Streaming**: Immediate feedback with streamed responses
- **Intelligent Chunking**: Smart document splitting that respects code blocks and context

## 🛠️ Technology Stack

- **Core Framework**: Python with async support
- **Language Models**: OpenAI GPT-4o-mini and Embeddings API
- **Vector Database**: Supabase with pgvector
- **Web Interface**: Streamlit
- **Documentation Crawler**: Custom crawler using Crawl4AI
- **Additional Tools**:
  - `pydantic-ai`: For AI agent framework
  - `logfire`: For logging
  - `httpx`: For async HTTP requests

## 📋 Prerequisites

- Python 3.8+
- OpenAI API key
- Supabase account and credentials
- Required Python packages (see requirements.txt)

## 🚀 Getting Started

1. **Clone the repository**

```bash
git clone https://github.com/abdul-28930/RAGProject
cd RAGProject
```

2. **Set up environment variables**

Create a `.env` file based on `.example.env`:

```env
OPENAI_API_KEY=your_openai_api_key
SUPABASE_URL=your_supabase_url
SUPABASE_SERVICE_KEY=your_supabase_service_key
LLM_MODEL=gpt-4o-mini  # or your preferred model
```

3. **Install dependencies**

```bash
pip install -r requirements.txt
```

4. **Initialize the database**

```bash
python crawl_docs.py
```

5. **Start the application**

```bash
streamlit run streamlit_ui.py
```

## 🏗️ Project Structure

- `ai_expert.py`: Core AI assistant implementation with RAG functionality
- `crawl_docs.py`: Documentation crawler and processor
- `streamlit_ui.py`: Web interface implementation
- `site_pages.sql`: Database schema and functions
- `requirements.txt`: Project dependencies

## 💡 How It Works

1. **Documentation Crawling**:
   - Crawls specified documentation sites
   - Chunks content intelligently
   - Generates embeddings using OpenAI
   - Stores in Supabase with vector search capability

2. **Query Processing**:
   - Converts user queries to embeddings
   - Performs semantic search in the vector database
   - Retrieves relevant documentation chunks

3. **Response Generation**:
   - Combines retrieved documentation with LLM capabilities
   - Generates contextual and accurate responses
   - Streams responses in real-time

## 🔧 Configuration

The system can be configured through environment variables and code constants:

- `LLM_MODEL`: Choice of OpenAI model
- Crawler settings in `crawl_docs.py`
- UI customization in `streamlit_ui.py`

## 🙏 Acknowledgments

- OpenAI for providing the language models and embeddings
- Supabase for the vector database functionality
- Streamlit for the web interface framework
- Pydantic AI, Hugging Face, and LangChain for their excellent documentation 