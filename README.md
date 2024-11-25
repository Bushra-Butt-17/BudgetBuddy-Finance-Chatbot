
# Budget Buddy - Finance Chatbot

Budget Buddy is a chatbot built using **Chainlit** and powered by the **LLaMA** language model. It leverages PDF resources like bank statements and budget reports to assist users with managing their finances. The chatbot uses **Hugging Face** for model integration and provides personalized financial insights and advice based on the uploaded data.

## Project Structure

The directory structure of this project is as follows:

```
- .chainlit/            # Chainlit specific files
- .files/               # File-related resources
- __pycache__/          # Python bytecode files
- data/                 # Financial data
- vectorstore/          # Vector database for storing financial data
- venv/                 # Virtual environment
- chainlit/             # Chainlit app configuration and files
- ingest/               # Scripts for ingesting PDF data
- model/                # Machine learning models (LLaMA and Hugging Face)
- README.md             # Project documentation
- requirements.txt      # Project dependencies
```

## Requirements

- Python 3.8 or later
- Chainlit
- LLaMA model integration
- Hugging Face Transformers
- Libraries for PDF processing (e.g., `PyPDF2`, `pdfplumber`)
- Virtual environment (recommended)

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/Bushra-Butt-17/BudgetBuddy.git
   cd BudgetBuddy
   ```

2. **Set up the virtual environment** (recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate   # For Linux/MacOS
   venv\Scripts\activate      # For Windows
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the chatbot**:
   Once the setup is complete, you can run the chatbot with Chainlit:
   ```bash
   chainlit run
   ```

   The chatbot will start and be accessible for interaction through the Chainlit interface.

## Features

- **PDF Resource Integration**: The chatbot can process and analyze financial data from PDF documents, such as bank statements or budget reports.
- **Powered by LLaMA**: The chatbot is built using the LLaMA language model, which provides advanced language understanding for accurate and insightful responses.
- **Hugging Face Integration**: Utilizes Hugging Face for model management and integration, allowing for seamless updates and optimizations.
- **Personalized Financial Advice**: Based on the content of the PDFs, the chatbot provides personalized financial insights and recommendations.
- **Interactive Conversations**: Users can ask the chatbot various financial questions, and it will assist based on the uploaded resources.

## Usage

1. **Upload a PDF**: Upload a financial PDF (e.g., budget report, bank statement) for the chatbot to analyze.
2. **Ask Questions**: Ask the chatbot questions about your finances. It will interpret the data from the PDFs to provide answers.
3. **Get Insights**: Based on your uploaded PDFs, the chatbot can help with budgeting, managing expenses, saving tips, and more.

## Configuration

The project uses default Chainlit settings. You can customize the chatbot's behavior by modifying the configuration files in the `.chainlit/` directory.

## Testing

To run tests (if available), use the following command:

```bash
python -m unittest discover -s tests
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
```

