# Claudian Mobile

**Transform Claude Code into an AI collaborator on your Android phone or tablet!**

An optimized Obsidian Mobile plugin that embeds Claude (or OpenAI) as a coding assistant directly in your vault.

## ✨ Features

- 💬 **AI Chat** - Talk to Claude or GPT right in Obsidian Mobile
- 📱 **Full Mobile Support** - Works on Android 7.0+ and iOS
- 🤖 **Multiple AI Providers** - Anthropic Claude or OpenAI GPT
- 📝 **Inline Editing** - Ask AI to modify selected text
- ⚡ **Fast & Lightweight** - ~50KB plugin, minimal battery drain
- 🔒 **Secure** - API keys stored locally, no data tracking
- 🎨 **Touch-Optimized** - Designed specifically for mobile

## 📱 Supported Devices

- ✅ Obsidian Mobile v0.15.0+
- ✅ Android 7.0+ with Obsidian
- ✅ iOS 14+ with Obsidian
- ✅ Termux (for building on Android)

## 🚀 Quick Start

### 1. Build (Termux on Android)

```bash
git clone https://github.com/Spartanis/claudian.git
cd claudian
npm install --legacy-peer-deps
npm run build
```

### 2. Install

Copy `main.js` + `manifest.json` to:
```
/storage/emulated/0/Obsidian/YOUR-VAULT/.obsidian/plugins/claudian-mobile/
```

### 3. Enable

- Obsidian → Settings → Community Plugins
- Disable **Restricted Mode**
- Enable **Claudian Mobile**

### 4. Configure

- Settings → Claudian Mobile
- Enter API Key (Claude or OpenAI)
- Choose model and adjust settings

### 5. Use

- Click 💬 icon in sidebar, or
- Select text → "Ask Claude" command

## 🔧 Configuration

### API Keys

**Anthropic Claude:**
1. Visit https://console.anthropic.com/
2. Get your API key
3. Paste in plugin settings

**OpenAI GPT:**
1. Visit https://platform.openai.com/api-keys
2. Get your API key
3. Paste in plugin settings

### Settings Options

| Setting | Default | Notes |
|---------|---------|-------|
| **Provider** | Claude | Choose Anthropic or OpenAI |
| **Model** | claude-3-haiku | Lighter model for mobile |
| **Max Tokens** | 1024 | Response length |
| **Temperature** | 0.7 | Creativity level |
| **Auto Scroll** | ON | Scroll to latest response |
| **Compact Mode** | ON | Save screen space |

## 📖 Usage Examples

### Ask a Question
1. Open plugin (💬 icon)
2. Type your question
3. Press Send
4. Get response from AI

### Modify Selected Text
1. Select text in note
2. Command Palette (Ctrl+P)
3. Search "Ask Claude"
4. AI shows modified version

### Code Review
1. Paste code in chat
2. Ask "Review this code"
3. Get suggestions

## 🛠️ Development

### Build
```bash
npm install
npm run build
```

### Development Mode
```bash
npm run dev  # Watch mode with auto-rebuild
```

### Type Checking
```bash
npm run typecheck
```

### Lint
```bash
npm run lint --fix
```

## 📁 Project Structure

```
claudian/
├── src/
│   ├── main.ts           # Entry point
│   ├── plugin.ts         # Main plugin
│   ├── ui/               # Mobile UI components
│   ├── api/              # AI API handlers
│   ├── settings/         # Settings management
│   └── utils/            # Helper utilities
├── manifest.json         # Plugin metadata
├── package.json          # Dependencies
└── esbuild.config.mjs    # Build configuration
```

## 🐛 Troubleshooting

### Plugin won't enable
```bash
# 1. Check manifest
cat manifest.json

# 2. Check file size
wc -c main.js  # Should be < 100KB

# 3. Check file permissions
chmod 644 main.js manifest.json
```

### API errors
- ✅ Verify API key is correct
- ✅ Check internet connection
- ✅ Ensure API has credits
- ✅ Check rate limits

### Performance issues
- ✅ Reduce max tokens
- ✅ Use lighter model (haiku/turbo)
- ✅ Close other apps

### Plugin not appearing
- ✅ Restart Obsidian
- ✅ Check plugin folder path
- ✅ Disable Restricted Mode

## 📊 Performance

| Metric | Value |
|--------|-------|
| **Plugin Size** | ~50KB |
| **Memory Usage** | ~20MB |
| **Startup Time** | <500ms |
| **API Latency** | 1-5s (network dependent) |
| **Battery Impact** | Minimal (network calls only) |

## 🔒 Security & Privacy

- 🔐 API keys stored locally in Obsidian vault
- 🔐 All requests use HTTPS encryption
- 📵 No data sent except to AI provider
- 🗑️ No conversations logged
- ✅ Open source (audit-able)

## 🎨 Mobile Optimizations

- ✅ Touch-friendly buttons (44px minimum)
- ✅ Responsive layout
- ✅ Proper text sizing (prevents zoom)
- ✅ Optimized for both portrait & landscape
- ✅ Battery-efficient
- ✅ Works with slow connections

## 📝 License

MIT License - See LICENSE file

## 🤝 Contributing

1. Fork the repo
2. Create feature branch
3. Make changes
4. Test on Obsidian Mobile
5. Submit PR

## 🔗 Links

- 🌐 [GitHub](https://github.com/Spartanis/claudian)
- 📚 [Obsidian Docs](https://docs.obsidian.md/)
- 🤖 [Anthropic Claude](https://www.anthropic.com/)
- 🔌 [OpenAI API](https://openai.com/api/)

## ⚡ Version History

### v1.0.0 (Current)
- Initial mobile release
- Claude & OpenAI support
- Touch-optimized UI
- Android & iOS compatible

---

**Made with ❤️ for mobile developers**

*Transform your Obsidian vault into an AI-powered notebook on the go!* 📱✨
