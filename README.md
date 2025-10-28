# 🌺 Poetic Chatbot 🌺

This repository contains the code for a simple but elegant console-based chatbot. Instead of standard replies, this bot uses generative AI to transform any user message into a short, emotional, two-line rhyming poem.

## 🤖 Technology & Model

This project leverages Google's powerful generative AI capabilities to create its poetic responses.

* **Model:** The core of the bot is **`gemini-2.0-flash`**. This is a fast and capable generative model from Google used to understand the user's input and craft the poetic reply.
* **API/SDK:** The script uses the **Google Gemini API** accessed via the official `google-generativeai` Python client library.
* **Language:** The chatbot is written entirely in **Python 3**.
* **Core Libraries:**
    * `google.generativeai`: Used to configure the API and send content requests to the Gemini model.
    * `time`: Used to create the `typing_effect` function, which prints the poem character-by-character for a more dramatic, "thoughtful" presentation.

---

## 📝 How It Works

The bot's logic is straightforward:

1.  **Prompt Engineering**: When a user sends a message (e.g., "I am happy"), the code does not just send that message to the AI. Instead, it wraps it in a specific system prompt:
    > "You are a poetic chatbot. Convert the user's message into a short, beautiful 2-line poem (a rhyming couplet). Keep it emotional and elegant."

2.  **API Call**: This structured prompt is sent to the `gemini-2.0-flash` model using the `model.generate_content()` function.

3.  **Poetic Response**: The model generates a 2-line rhyming couplet that creatively interprets the user's original message.

4.  **Typing Effect**: The `typing_effect` function prints the received poem to the console one character at a time, simulating the act of writing.

5.  **Chat Loop**: The script runs a `while True:` loop to continuously ask for user input until the user types `exit`.

---

