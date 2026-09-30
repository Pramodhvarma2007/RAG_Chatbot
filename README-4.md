# RAG Bot (FoodExpress Support)

A Retrieval-Augmented Generation (RAG) chatbot built in Google Colab using the Google Gemini API. Instead of relying only on the model's own knowledge, the bot first looks up the most relevant FoodExpress support information for the user's question and then uses it to write the answer. This keeps the replies accurate and based on the provided data.

**Author:** A. Pramodh Varma
**GitHub:** [Pramodhvarma2007](https://github.com/Pramodhvarma2007)

---

## Features

- Answers FoodExpress customer support questions (delivery delays, password reset, wrong food and more)
- Uses RAG: retrieves relevant information first, then generates the answer
- Runs as a continuous chat loop in the notebook
- Type `bye` or `quit` to exit

## Tech Stack

- Python
- Google Colab / Jupyter Notebook
- Google Gemini API (`google-genai` library)

## Installation

Run this in the first cell of the notebook:

```python
!pip install -q -U google-genai
```

## Setup

1. Get a free API key from [Google AI Studio](https://aistudio.google.com/).
2. Add it to the notebook as `GEMINI_API_KEY`. In Colab, use **Secrets** (the key icon on the left sidebar).
3. Do **not** paste your API key directly into the code or upload it to GitHub.

## How to Run

1. Open `RAG_Bot.ipynb` in Google Colab.
2. Run the install cell.
3. Run all cells (**Runtime → Run all**).
4. Type your question when you see `You:`.
5. Type `bye` or `quit` to end the chat.

## How It Works

1. The support information is stored as a knowledge base.
2. When the user asks a question, the bot retrieves the most relevant information from the knowledge base.
3. The question and the retrieved information are sent to Gemini through the `answer_question()` function.
4. Gemini writes the final answer using that information, and the bot prints it.

## Example Run

```
===== FoodExpress RAG Bot =====
Type 'bye' to exit.

You: My order is delayed
Bot: Check the estimated delivery time in My Orders. If the order is
significantly delayed, contact customer support through the Help section.

You: How do I reset my password
Bot: On the login screen, select Forgot Password and follow the instructions
to reset your password.

You: I received the wrong food. What should I do?
Bot: Open My Orders, select the order and go to Help. Report the incorrect
item.
```

## Project Structure

```
rag-bot/
├── RAG_Bot.ipynb   # Main notebook
└── README.md       # Project description
```

## Future Improvements

- Add more support topics (refunds, payments, offers)
- Load the knowledge base from PDF or text files
- Build a web interface for the chatbot

## License

This project is for educational purposes.
