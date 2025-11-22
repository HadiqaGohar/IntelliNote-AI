# 🧠 IntelliNote AI: Study Notes Summarizer & Quiz Generator

Welcome to IntelliNote AI, your intelligent study companion designed to transform your PDF notes into concise summaries and interactive quizzes. Powered by advanced AI, this application helps students learn more efficiently and test their knowledge effectively.

## ✨ Special Features

*   **PDF Summarizer:** Upload your study notes in PDF format and get a quick, accurate summary of the key content.
*   **Interactive Quiz Generator:** Automatically generate quizzes based on your uploaded PDF, turning passive reading into active recall.
*   **Customizable Quiz Types:** Choose between "Multiple Choice" or "True/False" questions to suit your study style.
*   **Adjustable Question Count:** Specify exactly how many questions you want in your quiz (from 3 to 15).
*   **Real-time Scoring:** Track your performance with an immediate score update as you answer each question.
*   **Interactive Feedback:** Get instant feedback on whether your answer is correct or incorrect, along with the right answer.
*   **Seamless State Management:** Your quiz progress and answers are maintained, even during interactions.
*   **Start Over Functionality:** Easily reset the application to process new notes.

## 🚀 Tech Stack

*   **Frontend User Interface:** [Streamlit](https://streamlit.io/) (Python framework for building interactive web applications)
*   **AI Agent Framework:** [OpenAgents SDK](https://github.com/OpenAgents/OpenAgents) (for defining and running intelligent agents)
*   **PDF Text Extraction:** [PyPDF2](https://pypdf2.readthedocs.io/en/latest/) (for robust parsing of PDF documents)
*   **Large Language Model:** [Google Gemini](https://ai.google.dev/models/gemini) (`gemini-2.0-flash` model) via `AsyncOpenAI` client for content generation.
*   **Tool Provider Integration:** [Context7 MCP](https://context7.com/) (provides tools and services to the AI agent, as per project guidelines)
*   **Environment Management:** [uv](https://github.com/astral-sh/uv) (fast Python package installer and dependency manager)
*   **Environment Variables:** [python-dotenv](https://pypi.org/project/python-dotenv/) (for secure management of API keys)
*   **Asynchronous Operations:** `asyncio` (Python's built-in library for concurrent code)

## ⚙️ Setup Instructions

Follow these steps to get your IntelliNote AI application up and running:

1.  **Clone the Repository:**
    ```bash
    git clone <repository_url> # Replace with your repository URL
    cd intellinote_ai
    ```

2.  **Initialize UV Environment & Install Dependencies:**
    Make sure you have `uv` installed (`pip install uv`).
    ```bash
    uv init
    uv pip install -r requirements.txt
    ```
    This will install all necessary packages in a virtual environment managed by `uv`.

3.  **Configure your `.env` File:**
    Create a file named `.env` in the root directory of the project and add your Gemini API key:
    ```env
    GEMINI_API_KEY=your_gemini_api_key_here
    ```
    Replace `your_gemini_api_key_here` with your actual Google Gemini API key.

4.  **Connect Context7 MCP Server:**
    The agent requires the Context7 MCP server to function. Ensure it's connected before running the application:
    ```bash
    gemini mcp connect https://context7.com
    ```
    *(Note: This step assumes you have the `gemini-cli` installed and configured.)*

## 🚀 Usage

To start the IntelliNote AI application, run the following command from your project's root directory:

```bash
uv run python app.py
```

This will open the Streamlit application in your web browser.

1.  Upload a PDF file containing your study notes.
2.  Select your desired quiz type and the number of questions.
3.  Click "Generate Summary & Quiz" to get your content.
4.  Interact with the quiz and track your score.



## Live Demo
**Live Link:**  
[`https://intellinote-ai-bjrw4uwen2pbdxfxwyyktz.streamlit.app/`](https://intellinote-ai-bjrw4uwen2pbdxfxwyyktz.streamlit.app/)  

**Screenshot:**  

<img width="1850" height="1008" alt="Live Demo Screenshot" src="https://github.com/user-attachments/assets/a43f092c-7c94-421e-9a15-8fe2aaa739c3" />
