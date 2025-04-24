# AI-Powered Website Testing Automation

This repository automates the end-to-end process of website testing using LLMs and Selenium. It allows users to simply input a website and a task/query, and the AI will:

1. Generate relevant test cases automatically.
2. Execute those test cases using Selenium via an undetectable Chrome driver.
3. Optionally validate results with live Google data for verification.

---

## 📌 Use Case
Imagine you want to test whether the Amazon login page is working correctly. Instead of writing test cases manually, you simply input:

> "Test the login functionality of Amazon"

The LLM will:
- Interpret the intent.
- Write proper test scenarios.
- Execute them automatically.
---

## 🏗️ High-Level Architecture

```mermaid
flowchart TD
    A[📝 User Input (Test Description)] --> B[🤖 LLM (Groq - LLaMA 3)]
    B --> C[🧪 Generate Test Cases]
    C --> D[🌐 Selenium (Undetected ChromeDriver)]
    D --> E[🔍 Website Interaction]
    E --> F[✅ Test Execution]
    F --> G[📸 Results / Screenshots]
    G --> H[🧠 Optional Validation (Google Search)]
""" 

### 🧩 Tech Stack
- **Language**: Python 🐍
- **LLM**: LLaMA 3 (via Groq API)
- **Automation**: Selenium with `undetected_chromedriver`
- **Env Management**: `python-dotenv`
- **Debugging**: Screenshots, logs

---

## 🚀 How It Works

1. **User Input**: You provide a prompt like "Test search functionality on Flipkart".
2. **LLM Call**: Groq API sends the prompt to LLaMA for test case generation.
3. **Selenium Execution**: Test cases are run headlessly using undetected Chrome driver.
4. **Screenshots & Logs**: Stored locally for debugging.
5. **Google Comparison (Optional)**: Extracts live snippet data for comparing expected vs actual result.

---

## 🔧 Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/ai-website-testing.git
cd ai-website-testing
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Set Up Environment Variables
Create a `.env` file with your Groq API key:
```
GROQ_API_KEY=your_api_key_here
```

### 4. Run the Main Script
```bash
python main.py
```

---

## 📂 Folder Structure
```
├── main.py                 # Main script
├── test_generator.py       # LLM-powered test case generator
├── executor.py             # Selenium logic for test execution
├── .env                    # API keys
├── screenshots/            # Debug screenshots
├── logs/                   # Test logs
```

---

## 📈 Future Enhancements
- [ ] Integrate voice input for test case generation.
- [ ] Support mobile web testing (Appium).
- [ ] CI/CD integration (GitHub Actions).
- [ ] Natural language validation of outcomes.
- [ ] Dashboard for real-time test results.

---

## 🤝 Contributing
Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to change.

---

## 📜 License
MIT License.

---

## 📬 Contact
Feel free to reach out via [LinkedIn](https://www.linkedin.com/in/satyam-gupta-41606a28a/) or raise an issue.

Happy testing! 🎯

