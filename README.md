# Budget Buddy - Finance Chatbot 💸🤖

**Budget Buddy** is your personal finance assistant! Built with **Chainlit** and powered by the **LLaMA** language model, Budget Buddy helps you manage your finances by analyzing PDF resources like bank statements and budget reports. Using **Hugging Face Transformers** and cutting-edge embeddings, it delivers personalized financial insights and advice.  

🚀 **Key Features**:  
- Upload PDFs 📄  
- Analyze financial data 📊  
- Get personalized advice 💡  
- Ask budget-related questions interactively 🗨️  

---

## **How It Works**

Budget Buddy utilizes **Hugging Face Embeddings** to convert uploaded PDFs into meaningful vector representations, enabling smart, efficient financial analysis.  

🔧 **Embedding Configuration**:  
Budget Buddy uses the `sentence-transformers/all-MiniLM-L6-v2` model for embedding generation:  

```python
from langchain.embeddings import HuggingFaceEmbeddings

# Create embeddings for financial PDFs
embeddings = HuggingFaceEmbeddings(
    model_name='sentence-transformers/all-MiniLM-L6-v2',
    model_kwargs={'device': 'cpu'}  # Optimized for devices without GPU
)
```

These embeddings allow the chatbot to:  
- Extract key financial details.  
- Provide accurate and insightful responses.  
- Enable quick information retrieval for better user experience.

---

## **Project Structure** 🗂️

Here’s how the project is organized:  

```
- .chainlit/            # Chainlit-specific configuration and settings
- .files/               # Temporary or supporting file storage
- __pycache__/          # Python bytecode files
- data/                 # 📂 Upload your financial PDFs here!
- vectorstore/          # 🧠 Vector database storing financial embeddings
- venv/                 # 🛡️ Virtual environment for dependencies
- chainlit/             # Chainlit app configuration and scripts
- ingest/               # 📜 Scripts for processing PDFs into embeddings
- model/                # 🤖 Machine learning models (LLaMA & Hugging Face)
- tests/                # 🧪 Unit and integration test files
- README.md             # 📖 Project documentation
- requirements.txt      # 📋 Project dependencies
```

---

## **Getting Started** 🚀

### 1. **Clone the Repository** 🛠️
```bash
git clone https://github.com/Bushra-Butt-17/BudgetBuddy.git
cd BudgetBuddy
```

### 2. **Set Up the Virtual Environment** 🐍
```bash
python -m venv venv
source venv/bin/activate   # For Linux/MacOS
venv\Scripts\activate      # For Windows
```

### 3. **Install Dependencies** 📦
```bash
pip install -r requirements.txt
```

---

## **How to Use Budget Buddy** 🤖💬

### Step 1: Upload Financial PDFs  
   - Save your PDF files (e.g., bank statements, budget reports) in the `data/` directory.  

### Step 2: Process PDFs 📜 ➡️ 🧠  
   - Generate embeddings from the uploaded PDFs by running the `ingest_data.py` script:  
     ```bash
     python ingest.py
     ```
   - This step converts the financial data into **vector embeddings** stored in the `vectorstore/` directory.  

### Step 3: Run the Chatbot 💬  
   - Launch the chatbot using Chainlit:  
     ```bash
     chainlit run
     ```
   - The chatbot interface will open in your browser, ready to analyze your financial data and answer your questions.

---

## **Features** 🌟

### 📝 **PDF Analysis**  
- Analyze structured and semi-structured financial PDFs.  
- Extract transaction summaries, income/expense patterns, and more!  

### 🧠 **Powered by LLaMA & Hugging Face**  
- Combines the power of **LLaMA** for language understanding with **Hugging Face embeddings** for deep financial insights.  

### 💬 **Interactive Conversations**  
- Ask questions like:  
  - *"What is my total spending for October?"*  
  - *"How much did I save last month?"*  
  - *"What’s the largest expense in my uploaded PDF?"*  

### 📊 **Personalized Financial Insights**  
- Provides tailored recommendations based on your financial habits, such as:  
  - Expense categorization.  
  - Saving strategies.  
  - Budget optimization tips.

### ⚡ **Efficient Data Retrieval**  
- Uses **vector embeddings** stored in the `vectorstore/` directory for quick and accurate responses.  

---

## **Tips for Best Results** 🎯

1. **Upload PDFs** to the `data/` folder for consistent processing.  
2. Always **run the `ingest_data.py` script** after adding new PDFs to update embeddings.  
3. Use a **virtual environment** to manage dependencies and prevent conflicts.  

---

## **Future Enhancements** 🔮

- 📈 Add support for dynamic dashboards.  
- 📥 Real-time PDF uploads directly via the chatbot.  
- 🌍 Integration of external APIs for currency conversion and stock market data.  

---

## **License** 📄

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.  

---

Get started today and take control of your finances with Budget Buddy! 💸
