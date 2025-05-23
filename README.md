# Telegram Bot Setup Guide

A simple and beginner-friendly guide to help you create a Telegram bot and get your chat ID. This is especially useful for projects like the [KTU Revaluation Notifier Bot](https://github.com/your-username/ktu-revalbot) that send automated messages via Telegram.

---

## 📌 What You’ll Learn

- How to create a Telegram bot
- How to get your bot token
- How to find your chat ID (for individuals or groups)
- How to test sending messages

---

## 🔧 Step-by-Step Instructions

### 1. Create a Telegram Bot

1. Open Telegram and search for [@BotFather](https://t.me/BotFather)
2. Start the chat and type `/newbot`
3. Follow the prompts to:
   - Set a name (e.g., `MyNotifierBot`)
   - Set a username (must end in `bot`, e.g., `my_notifier_bot`)
4. You will receive a **bot token** like:  
   `123456789:ABCdefGhIjKlMnOpQrStUvWxYz`

Save this token — it will be used in your code.

---

### 2. Get Your Chat ID

#### If sending to yourself:
1. Start a chat with your new bot on Telegram
2. Send a random message to the bot
3. Go to this URL in your browser (replace `BOT_TOKEN`):  
https://api.telegram.org/bot<BOT_TOKEN>/getUpdates
4. Look for `"chat":{"id":YOUR_CHAT_ID,...}` in the response

#### If sending to a group:
1. Add the bot to the group
2. Send a message in the group
3. Use the same `getUpdates` URL to find the group chat ID  
*(It will be a negative number, e.g., `-123456789`)*

---

### 3. Test Sending a Message

Use this URL (replace the token and chat ID):

https://api.telegram.org/bot<BOT_TOKEN>/sendMessage?chat_id=<CHAT_ID>&text=Hello+from+your+bot

You should receive the message in Telegram.

---

## ✅ Done!

You’re now ready to use your bot in scripts

---

## 💡 Tip

Do **not** share your bot token publicly. Treat it like a password.
