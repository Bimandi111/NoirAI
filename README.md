# NoirAI — Your Premium AI Companion

NoirAI is a full-featured, modern AI chat application powered by the OpenRouter API. It provides a sleek interface with multiple AI personas, local chat history, and real-time streaming responses.

## Features

✨ **Multi-Model Support**
- NVIDIA Nemotron 3 Super (default, free tier)
- NVIDIA Llama Nemotron Embed VL 1b V2 (free tier)
- StepFun Step-3.5 Flash (free tier)
- Switch models instantly without interrupting your workflow

🎭 **Dynamic Personas**
- **Default**: Helpful, intelligent, and friendly assistant
- **Coder**: Senior software engineer focused on code quality and best practices
- **Creative**: Imaginative storyteller and creative partner
- **Study**: Patient tutor that breaks down complex topics step by step

💬 **Chat Management**
- Persistent chat history stored locally
- Rename and delete individual conversations
- Auto-load your most recent chat
- Welcome screen with smart suggestions

🔐 **Privacy First**
- All data stored locally in browser storage
- API key stored securely (never sent to our servers)
- No accounts required — use as a guest or create a local account

🎨 **Modern UI**
- Dark theme optimized for readability
- Responsive design works on desktop and mobile
- Syntax-highlighted code blocks
- Real-time message streaming
- Typing indicators for better UX

## Getting Started

### Prerequisites

- A modern web browser (Chrome, Firefox, Safari, Edge)
- An OpenRouter API key (free at [openrouter.ai](https://openrouter.ai))

### Installation

1. **Clone or download** this repository to your local machine
2. **Open `index.html`** in your browser
3. **Sign in or continue as a guest** using the auth screen
4. **Add your OpenRouter API key** when prompted (or via API Settings)
5. **Start chatting!** Select a persona and model, then begin typing

### No Build Required

NoirAI is a pure client-side application — no npm install, no build process, no server needed. Just open and use!

## Usage

### Switching Models

Click the model dropdown in the top-right corner to select a different AI model. Your choice is saved automatically.

### Changing Personas

Select a persona from the sidebar:
- **Default** — balanced for most tasks
- **Coder** — optimized for programming questions and code reviews
- **Creative** — for storytelling and imaginative tasks
- **Study** — for learning and explanations

### File Attachments

Click the attachment button to include images, PDFs, or text files with your message (file support depends on model capabilities).

### Keyboard Shortcuts

- **Enter** — Send message
- **Shift + Enter** — New line in message
- **Click chat titles** — Rename chats

### Chat History

All conversations are stored automatically. Access previous chats from the **Recent Chats** section in the sidebar. Delete chats with the ✕ button.

## Configuration

### API Key

Your OpenRouter API key is stored only in your browser's local storage. To update it:
1. Click **API Settings** in the sidebar
2. Paste your new key
3. Click **Save & Continue**

### Default Model

To change the default model that loads on startup, edit `script.js`:
```javascript
const DEFAULT_MODEL = 'nvidia/nemotron-3-super-120b-a12b:free';
```

Change this to any supported model ID.

### Supported Models

Edit the `SUPPORTED_MODELS` set in `script.js` to add or remove available models:
```javascript
const SUPPORTED_MODELS = new Set([
  'nvidia/nemotron-3-super-120b-a12b:free',
  'nvidia/llama-nemotron-embed-vl-1b-v2:free',
  'stepfun/step-3.5-flash:free',
  // Add more models here
]);
```

## Architecture

### Files

- **`index.html`** — Page structure and modals
- **`script.js`** — Core app logic, chat management, API integration
- **`style.css`** — Responsive design and animations

### Key Technologies

- **OpenRouter API** — Multi-model LLM access
- **Marked.js** — Markdown rendering
- **Highlight.js** — Code syntax highlighting
- **LocalStorage** — Persistent data storage
- **Fetch API** — Streaming responses

## Troubleshooting

### "Only background shows"
- Clear browser cache and reload
- Check browser console for errors (F12)
- Ensure `script.js` and `style.css` are in the same folder as `index.html`

### API key not working
- Verify your key starts with `sk-or-v1-`
- Check that your OpenRouter account has API credits
- Try clearing browser storage and re-entering the key

### Messages not sending
- Confirm your API key is saved
- Check your browser's internet connection
- Look for error messages in the browser console

## Privacy & Security

- ✅ No backend server — all processing happens in your browser
- ✅ API key stored locally only — never transmitted to third parties
- ✅ Chat history never leaves your device
- ✅ No tracking or analytics

## License

This project is provided as-is for personal and educational use.

## Support

For issues, feature requests, or questions:
1. Check the troubleshooting section above
2. Verify your OpenRouter API key and account status
3. Clear browser storage and try again

---

**Built with ❤️ for AI enthusiasts, coders, and creative minds.**
