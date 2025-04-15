# 🤖 LinkedIn Quiz GPT Bot

**Automatically answer LinkedIn Learning quizzes using GPT-4 and Selenium**

---

## 📌 Overview

This bot:
- Logs in through LinkedIn and Microsoft SSO
- Detects questions and multiple-choice options
- Uses GPT-4 to find the correct answer
- Simulates human behavior (28–59 sec delay)
- Clicks the correct option(s)
- Saves all questions and answers to a file

---

## ⚙️ Installation

```bash
pip install selenium openai pandas
```

Make sure [ChromeDriver](https://chromedriver.chromium.org/downloads) is installed and matches your Chrome version.

---

## 🔐 Configuration

In `linkedin_quiz_auto_login.py`, set your credentials:

```python
LINKEDIN_EMAIL = 'your LinkedIn email'
LINKEDIN_PASSWORD = 'your LinkedIn password'
MICROSOFT_EMAIL = 'your Microsoft email'
MICROSOFT_PASSWORD = 'your Microsoft password'
openai.api_key = 'sk-...'
```

---

## ▶️ Run the bot

```bash
python linkedin_quiz_auto_login.py
```

1. The script will log in to LinkedIn → Microsoft SSO
2. Wait for 2FA verification manually
3. Open your quiz and press Enter
4. GPT-4 will answer questions automatically
5. At the end, click “Finish Exam” manually and press Enter again
6. Answers are saved to `linkedin_gpt_qa.txt`

---

## 🗂 Project Structure

```
LinkedIn_Test_Answer_Bot/
├── linkedin_quiz_auto_login.py
├── README.md
├── .gitignore
├── requirements.txt
└── linkedin_gpt_qa.txt
```

---

## 📄 Example Output (`linkedin_gpt_qa.txt`)

```
🟢 Question 1:
What is the primary benefit of a project charter?

📋 Options:
 - It authorizes the project
 - It defines scope
 - It assigns team members

✅ GPT Answer:
 - It authorizes the project
============================================================
```

---

## 🤝 Contributing

Feel free to fork the project, submit pull requests, or suggest improvements!

---

## 📜 License

MIT License — use at your own risk and for educational purposes only.

---

© 2025 – GPT Test Bot by Arapova-Elena
