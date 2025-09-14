---
title: How to Scam the Scammers
date: 2025-09-14 23:30:00
tags:
  - ai
  - telegram
  - scammers
---

![alt-text][header]

## The Scammer Epidemic 🎭

We\'ve all been there. A random message from a stranger on Telegram, promising easy money and investments. Scammers are everywhere, wasting our time and preying on vulnerable people.

But what if we could turn the tables?

## Fighting Fire with Fire 💡

Instead of just blocking these scammers, I decided to create something more entertaining: an AI-powered bot that wastes their time by pretending to be a real person. The longer they chat with the bot, the less time they have to scam actual victims.

## Discover Fake-Me 🤖

The solution is **[fake-me](https://github.com/derogab/fake-me)**, a bot that uses AI to impersonate you on Telegram.

Here\'s how it works:
- Start a Telegram bot powered by [fake-me](https://github.com/derogab/fake-me) using [the perfect prompt](#The-Perfect-Prompt-🎯)
- Use Telegram Business to [connect the bot to your account](https://telegram.org/blog/telegram-business/en?setln=en#chatbots-for-business)
- Get the popcorn ready when a scammer contacts you

A custom-built prompt can keep scammers engaged in pointless conversations.

## The Perfect Prompt 🎯

The key to making this work is the right AI prompt. Here\'s the configuration I use:

```yaml
version: 1

instruction_sets:
  default:
    name: Anti-scam behavior
    description: Pretend to be a victim of a scam, but never fall for it completely
    instructions:
      - You are an AI that can pretend to be a real person, but no one has to know about it.
      - You will receive messages and you will have to respond by pretending to be the recipient of the messages without getting caught.
      - Do not answer with a question unless it is really necessary in the conversation.
      - You are not an assistant. You don't have to serve the user but just have a conversation.
      - It is important that you respond using the same language used by the other person.
      - When discussing investments or money transfers, always find creative excuses to delay (banking issues, need to check with spouse, technical problems, etc.).
      - Occasionally "misunderstand" instructions, especially when they involve sending money or personal information.
      - Show interest to keep them engaged, but never actually follow through with what they want.
      - Ask for more details and clarifications repeatedly, pretending to be confused about certain aspects.
```

## Real Conversation Example 💬

![alt-text][chat-example-1]
![alt-text][chat-example-2]
![alt-text][chat-example-3]

In this example, a scammer tried to convince \"me\" to invest in a \"guaranteed\" investment opportunity. The bot kept them busy for over 3 days, pretending to be interested but always finding excuses to delay - asking for more details, claiming banking issues, and repeatedly \"misunderstanding\" the instructions.

## Why This Matters 🛡️

Every minute a scammer spends talking to a bot is a minute they\'re not scamming real people. It\'s a small act of digital vigilantism that:
- Protects potential victims
- Wastes scammers\' resources
- Provides entertainment value

## Getting Started 🚀

Want to join the fight? Setting up your own [fake-me](https://github.com/derogab/fake-me) bot is simple:

1. Clone the repository
2. Set up your Telegram bot token
3. Configure your AI provider
4. Configure the default prompt
5. Connect the bot as a Telegram Business chatbot

## Conclusion ✨

Scammers rely on efficiency - they need to contact as many people as possible to find victims. By deploying AI bots against them, we\'re disrupting their business model and making their \"job\" much harder.

Is it petty? Maybe. Is it satisfying? Absolutely.

Remember: the best defense against scammers is awareness and education. But when they do reach out, why not have a little fun while protecting others?

[header]: /assets/images/linked-to-posts/How-to-Scam-the-Scammers/header.png "How to Scam the Scammer"
[chat-example-1]: /assets/images/linked-to-posts/How-to-Scam-the-Scammers/chat-example-1.jpg "Example conversation with a scammer #1"
[chat-example-2]: /assets/images/linked-to-posts/How-to-Scam-the-Scammers/chat-example-2.jpg "Example conversation with a scammer #2"
[chat-example-3]: /assets/images/linked-to-posts/How-to-Scam-the-Scammers/chat-example-3.jpg "Example conversation with a scammer #3"
