
# Budget Buddy - Your Personal Finance Chatbot 💸🤖

**Budget Buddy** is a finance-focused chatbot designed to help you manage your personal finances with ease. It uses advanced natural language processing (NLP) technologies, including **Chainlit**, **LLaMA**, and **Hugging Face Sentence Transformers**, to analyze your financial documents, answer budget-related questions, and provide actionable insights.

---

## 📌 **What is a Chatbot?**

A **chatbot** is a software application designed to simulate human-like conversations using text or voice. Chatbots use NLP to understand and respond to user queries intelligently. Budget Buddy acts as a financial assistant, leveraging machine learning and NLP to interpret your uploaded financial data and provide meaningful advice.

---

## 📌 **How Budget Buddy Works**

Budget Buddy processes your uploaded financial documents (e.g., bank statements, budget reports) and provides insights by:  

1. **Embedding Generation:** Converts the content of your PDFs into meaningful numerical representations (embeddings) using **Hugging Face Sentence Transformers**.  
2. **Financial Data Storage:** Stores these embeddings in a **vector database** for quick retrieval and analysis.  
3. **Interactive Conversations:** Answers user questions using the generated embeddings and the **LLaMA language model** for natural and context-aware responses.  

---

## 🔍 **What are Sentence Transformers?**

**Sentence Transformers** are deep learning models designed to convert text into dense numerical vectors (embeddings). These vectors capture the semantic meaning of sentences, enabling advanced tasks like:

- Information retrieval.
- Question answering.
- Semantic similarity comparison.

Budget Buddy uses the `sentence-transformers/all-MiniLM-L6-v2` model, a lightweight and efficient transformer-based model, ideal for creating embeddings for financial data.

### **How It Works in Budget Buddy**:
1. Text is extracted from uploaded PDFs.
2. The extracted text is passed through the Sentence Transformer model to generate embeddings.
3. These embeddings are stored in a **vectorstore** for efficient and quick query matching.

---

## 🔗 **Role of Hugging Face**

**Hugging Face** is a leading platform for state-of-the-art NLP models and tools. In Budget Buddy, it plays a critical role by providing:

1. **Pretrained Models:** The `sentence-transformers/all-MiniLM-L6-v2` model is accessed via Hugging Face for creating embeddings.  
2. **Ease of Integration:** Hugging Face tools simplify integrating advanced NLP capabilities into the chatbot.  
3. **Customizability:** Allows fine-tuning and adapting pretrained models for specific financial use cases.

---

## 🚀 **Key Features**

### 1. **Upload Financial PDFs** 📄  
- Upload documents like bank statements, expense reports, and budgets.  

### 2. **PDF Analysis** 📊  
- Extract structured information, such as income, expenses, and transaction summaries.  

### 3. **Interactive Conversations** 💬  
- Ask questions like:  
  - *"What’s my total spending for October?"*  
  - *"How much did I save last month?"*  
  - *"What’s the largest expense in my uploaded PDF?"*  

### 4. **Personalized Financial Advice** 💡  
- Get tailored insights and suggestions for improving savings, managing budgets, and optimizing expenses.  

### 5. **Fast and Accurate Responses** ⚡  
- Leverages vector embeddings for efficient and context-aware query handling.

---

## 🛠️ **Project Structure**

Here’s how the project is organized:  

```
- .chainlit/            # Chainlit-specific configuration and settings
- .files/               # Temporary or supporting file storage
- data/                 # 📂 Upload your financial PDFs here!
- vectorstore/          # 🧠 Vector database storing financial embeddings
- venv/                 # 🛡️ Virtual environment for dependencies
- chainlit/             # Chainlit app configuration and scripts
- ingest/               # 📜 Scripts for processing PDFs into embeddings
- model/                # 🤖 Machine learning models (LLaMA & Hugging Face)
- README.md             # 📖 Project documentation
- requirements.txt      # 📋 Project dependencies
```

> **Note**: There are currently no test files in the project. Testing will involve manual verification of the chatbot’s responses using different financial PDFs.

---

## 📖 **How to Get Started**

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

## 🤖 **How to Use Budget Buddy**

### Step 1: Upload Financial PDFs  
   - Save your PDF files (e.g., bank statements, budget reports) in the `data/` directory.  

### Step 2: Process PDFs 📜 ➡️ 🧠  
   - Run the `ingest_data.py` script to generate embeddings from the PDFs:  
     ```bash
     python ingest.py
     ```
   - Embeddings are stored in the `vectorstore/` directory for quick access.  

### Step 3: Run the Chatbot 💬  
   - Launch the chatbot using Chainlit:  
     ```bash
     chainlit run
     ```
   - Open your browser to interact with Budget Buddy, upload financial PDFs, and ask questions.

---

## 🌟 **Behind the Scenes**

### **Embedding Generation**  
The chatbot uses **Hugging Face Embeddings** to generate dense numerical representations (embeddings) of financial PDFs. These embeddings allow the chatbot to:  
- Extract and summarize critical information.  
- Retrieve relevant details when answering user questions.  
- Offer precise and personalized financial insights.

Here’s how embeddings are created in Budget Buddy:
```python
from langchain.embeddings import HuggingFaceEmbeddings

# Create embeddings for financial PDFs
embeddings = HuggingFaceEmbeddings(
    model_name='sentence-transformers/all-MiniLM-L6-v2',
    model_kwargs={'device': 'cpu'}  # Optimized for devices without GPU
)
```

### **Vectorstore**  
The embeddings are stored in a vector database (`vectorstore/`), enabling efficient similarity searches and instant retrieval of relevant data.

---

## 🚀 **Future Plans**

- **Automated Testing Framework:** Add unit and integration tests for validating chatbot responses.  
- **Data Visualization:** Visualize financial trends and summaries (e.g., income vs. expenses).  
- **Support for More File Formats:** Expand support to Excel and CSV files.  
- **Advanced NLP Models:** Fine-tune LLaMA for financial-specific tasks.  

---

## 🙌 **Contributing**

We welcome contributions to make Budget Buddy better! Feel free to fork the repository, make changes, and submit a pull request.  

---

## 📧 **Contact**

For questions, suggestions, or feedback, contact: **bsdsf21m020@pucit.edu.pk**  

---

**Happy Budgeting!** 💸🎉
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
