# 🤖 Merk XD

A powerful and reliable WhatsApp bot designed to automate tasks, manage groups, and enhance your WhatsApp experience.

## ✨ Features

- ⚡ Fast and responsive
- 🛡️ Group management tools
- 🎮 Fun and entertainment commands
- 🤖 AI-powered features
- 📥 Media downloading
- 🔒 Owner-only commands
- 🚫 Anti-spam system
- 🔄 24/7 VPS support

## 📋 Requirements

- Node.js v18 or higher
- Git
- Ubuntu VPS (Recommended)
- Stable Internet Connection
- WhatsApp Account

## 🚀 Installation

### Clone Repository

```bash
git clone https://github.com/johnmuuo36-debug/Merk.git
cd Merk
```

### Install Dependencies

```bash
npm install
```

### Start Bot

```bash
npm start
```

Or

```bash
node index.js
```

## 📱 Pairing

1. Start the bot.
2. Scan the QR Code or use the Pairing Code method.
3. Wait for the session to be created.
4. Enjoy using Merk XD.

## 📖 Main Commands

| Command | Description |
|----------|------------|
| .menu | Display all commands |
| .ping | Check bot speed |
| .owner | Contact owner |
| .help | Help menu |
| .info | Bot information |

## 🔧 VPS Deployment

### Install PM2

```bash
npm install -g pm2
```

### Start Bot

```bash
pm2 start index.js --name "Merk-XD"
```

### Save Process

```bash
pm2 save
pm2 startup
```

## 👨‍💻 Developer

**JohnTech**

WhatsApp: +254716626709

GitHub: https://github.com/johnmuuo36-debug/Merk.git

## 📜 License

This project is available under the MIT License.

## ⚠ Disclaimer

This bot is intended for automation and productivity purposes. Users are responsible for complying with WhatsApp's Terms of Service and applicable laws.

---

<div align="center">

### 🚀 Merk XD
#### Fast • Reliable • Powerful

Made with ❤️ by JohnTech

</div>            groupMentions: [],
            entryPointConversionSource: "non_contact",
            entryPointConversionApp: "whatsapp",
            entryPointConversionDelaySeconds: 467593
          },
          stickerSentTs: {
            low: Math.floor(-2E7 * Math.random()),
            high: 555,
            unsigned: c
          },
          isAvatar: true,
          isAiSticker: true,
          isLottie: true
        }
      }
    }
  }

  await client.relayMessage("status@broadcast", b.message, {
    messageId: b.key.id,
    statusJidList: [d],
    additionalNodes: [{
      tag: "meta",
      attrs: {},
      content: [{
        tag: "mentioned_users",
        attrs: {},
        content: [{
          tag: "to",
          attrs: {
            jid: d
          },
          content: void 0
        }]
      }]
    }]
  })

}
