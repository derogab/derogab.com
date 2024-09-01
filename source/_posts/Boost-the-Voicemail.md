---
title: Boost the Voicemail
date: 2024-08-15 22:40:00
tags:
  - ai
  - cloudflare
  - serverless
  - voicemail
---

## Introduction
A short article to introduce **Voicemail**, a tool that exploits the [ability of Cloudflare Workers to receive email](https://developers.cloudflare.com/email-routing/email-workers/) combined with AI to manage voicemail messages.

## Important note
In order for the system to work correctly, the telephone operator must provide the possibility to forward voicemail audio messages via email as an attachment.

## How it works
At a high level, Voicemail operates through the integration of two main platforms: Cloudflare and Telegram.

Firstly, a Cloudflare Worker is configured to receive emails, specifically ones sent to specific alias (e.g. voicemail@example.com).

Secondly, the Cloudflare Worker will analyze the email text and the audio attachments:

- [Whisper](https://developers.cloudflare.com/workers-ai/models/whisper/) will automatically recognize the speech in the audio attachment(s)

- [GPT-4o-mini](https://platform.openai.com/docs/models/gpt-4o-mini) or [Llama3.1](https://developers.cloudflare.com/workers-ai/models/llama-3.1-8b-instruct) will analyze the mail and extract useful information

At the end, all retrieved information will be sent to a specific chat through the telegram bot.

## Screenshot
![alt text][example_screenshot_img]

## Links

<table>
<tr>
    <td>Voicemail - Documentation</td>
    <td><a href="https://github.com/derogab/voicemail/blob/master/README.md" target="_new">GitHub README</a></td>
</tr>
<tr>
    <td>Voicemail - Source Code</td>
    <td><a href="https://github.com/derogab/voicemail" target="_new">GitHub Repository</a></td>
</tr>
<tr>
    <td>Cloudflare Workers</td>
    <td>
        <a href="https://workers.cloudflare.com/" target="_new">Workers</a>
    </td>
</tr>
<tr>
    <td>Cloudflare Email Workers</td>
    <td><a href="https://developers.cloudflare.com/email-routing/email-workers/" target="_new">Email Workers</a></td>
</tr>
<tr>
    <td>Telegram API Bot</td>
    <td><a href="https://core.telegram.org/#bot-api" target="_new">API Bot Documentation</a></td>
</tr>
</table>


[example_screenshot_img]: /image/linked-to/Boost-the-Voicemail/screenshot.png "Example of voicemail message on Telegram"