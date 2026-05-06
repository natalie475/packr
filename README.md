# packr ✈️

A personal travel packing list tool. Answer a few questions, brain-dump what you want to bring, and get a clean organized checklist back.

## Setup

### 1. Clone / create repo
Push this folder to a new GitHub repo.

### 2. Get your Anthropic API key
Go to [console.anthropic.com](https://console.anthropic.com) → API Keys → Create key.

### 3. Deploy to Vercel
1. Go to [vercel.com](https://vercel.com) → New Project → Import your GitHub repo
2. In **Environment Variables**, add:
   - Key: `ANTHROPIC_API_KEY`
   - Value: `sk-ant-...` (your key)
3. Deploy!

That's it. Your app will be live at `your-project.vercel.app`.

## Customizing your defaults

Open `public/index.html` and find the three arrays near the top of the `<script>` tag:

```js
const MY_TOILETRIES = [ ... ]
const MY_ELECTRONICS = [ ... ]
const MY_MEDICATIONS = [ ... ]
```

Edit these to match your actual go-to items. They'll appear automatically on every packing list.

## Local development

No build step needed — it's plain HTML + a serverless function.

To test locally with the Vercel CLI:
```bash
npm i -g vercel
vercel dev
```

Then open `http://localhost:3000`.

Make sure you have a `.env` file locally:
```
ANTHROPIC_API_KEY=sk-ant-...
```
(Never commit this file — it's in .gitignore by default)
