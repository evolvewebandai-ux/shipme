# ShipMe - Google AI Studio Integration

A Node.js project integrated with **Google AI Studio** (Gemini API) for AI-powered features.

## 🚀 Setup Instructions

### 1. Get Your API Key

1. Visit [Google AI Studio](https://ai.google.dev/)
2. Click **"Get API Key"** button
3. Create a new API key in Google Cloud Console
4. Copy your API key

### 2. Configure Environment Variables

1. Copy the example file:
   ```bash
   cp .env.example .env
   ```

2. Add your API key to `.env`:
   ```
   GOOGLE_AI_API_KEY=your_actual_api_key_here
   ```

### 3. Install Dependencies

```bash
npm install
```

### 4. Run the Integration

```bash
npm start
```

You should see a response from Google's Gemini AI model!

## 📁 Project Structure

```
shipme/
├── index.js              # Main integration file
├── package.json          # Dependencies and scripts
├── .env.example          # Environment variables template
├── .gitignore            # Git ignore rules
└── README.md             # This file
```

## 🛠️ Usage

### Basic Example (Already Included)

The `index.js` file shows a simple example of querying Gemini:

```javascript
const model = genAI.getGenerativeModel({ model: "gemini-pro" });
const result = await model.generateContent("Your prompt here");
const text = await result.response.text();
```

### Advanced Features

For more advanced features like:
- Vision API (analyze images)
- Streaming responses
- Multi-turn conversations
- Custom parameters

Check [Google Generative AI Documentation](https://ai.google.dev/tutorials/nodejs_quickstart)

## 🔒 Security Best Practices

⚠️ **Never commit your `.env` file!**

- Keep API keys in environment variables
- Use `.gitignore` to prevent accidental commits
- For production, use GitHub Secrets or your deployment platform's secret management

### GitHub Actions Setup (Optional)

To use this in GitHub Actions, add a secret:

1. Go to your repository settings
2. Navigate to **Secrets and variables → Actions**
3. Create a new repository secret: `GOOGLE_AI_API_KEY`
4. Paste your API key

Then use it in workflows:

```yaml
env:
  GOOGLE_AI_API_KEY: ${{ secrets.GOOGLE_AI_API_KEY }}
```

## 📚 Resources

- [Google AI Studio](https://ai.google.dev/)
- [Node.js SDK Documentation](https://ai.google.dev/tutorials/nodejs_quickstart)
- [Gemini API Models](https://ai.google.dev/models/gemini)
- [API Reference](https://ai.google.dev/api)

## 🤝 Next Steps

1. Customize `index.js` with your own prompts
2. Add more AI features to your project
3. Explore advanced capabilities like vision and streaming

## 📝 License

MIT

---

**Built with ❤️ using Google Generative AI**
