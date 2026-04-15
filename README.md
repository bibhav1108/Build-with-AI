# 🛡️ CyberGuard AI – URL & Log Analyzer Agent

CyberGuard AI is an intelligent cybersecurity assistant designed to protect users from phishing links and monitor system logs for potential attacks like brute force attempts. Built with **Pydantic AI** and powered by **Groq**, it provides structured risk assessments and actionable recommendations.

## 🚀 Features

- **URL Analysis**: Detects insecure protocols (HTTP), unusually long URLs, and suspicious keywords common in phishing.
- **Log Monitoring**: Parses system logs to identify failed login sequences and unauthorized access patterns.
- **Structured Risk Assessment**: Returns a standardized JSON output containing:
    - **Summary**: A brief overview of safety concerns.
    - **Risk Level**: Categorized as `LOW`, `MEDIUM`, or `HIGH`.
    - **Suggestions**: Actionable security advice (e.g., "Enable 2FA", "Block URL").
- **Interactive UI**: A sleek **Gradio** web interface for easy URL and log submission.

## 🛠️ Tech Stack

- **[Pydantic AI](https://github.com/pydantic/pydantic-ai)**: For building the AI agent and ensuring structured data outputs.
- **[Gradio](https://gradio.app/)**: For the user-friendly web interface.
- **[Groq](https://groq.com/)**: Utilizing Llama 3.3 for high-speed reasoning and tool use.
- **[LiteLLM](https://github.com/BerriAI/litellm)**: For managing LLM interactions.

## ⚙️ Setup

### 1. Prerequisites
Ensure you have Python 3.10+ installed.

### 2. Install Dependencies
```bash
pip install litellm pydantic-ai gradio python-dotenv
```

### 3. Environment Configuration
You'll need a Groq API key. You can set it in your environment or directly in the notebook/script:

```python
import os
os.environ["GROQ_API_KEY"] = "your_groq_api_key_here"
```

## 🖥️ Usage

1. Open the `CyberGuardAI.ipynb` notebook.
2. Run the cells to initialize the agent and tools.
3. Launch the Gradio UI at the end of the notebook.
4. Enter a suspected URL or paste system logs to get an instant security assessment.

## 🔍 Examples

- **Suspicious URL**: `http://secure-login-verify.com/auth`
- **Brute Force Logs**: 
  ```text
  10:00:01 - User 'admin' login failed
  10:00:02 - User 'admin' login failed
  10:00:03 - User 'admin' login failed
  ```

---
*Built with ❤️ for AI-based security analysis.*
