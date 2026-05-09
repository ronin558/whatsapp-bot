[README.md](https://github.com/user-attachments/files/27557470/README.md)
# WhatsApp Bot with Claude AI 🤖

A complete WhatsApp chatbot powered by Claude AI, deployed on Railway.

## Features ✨

- ✅ Real-time WhatsApp messaging
- ✅ Claude AI responses
- ✅ Webhook verification
- ✅ Typing indicators
- ✅ Error handling
- ✅ Runs 24/7 on Railway

---

## Quick Setup (5 minutes)

### Step 1: Get Your Credentials

#### **A) WhatsApp Credentials**
1. Go to https://developers.facebook.com/apps
2. Select your app
3. Go to "WhatsApp" → "Getting started"
4. Copy your **Phone Number ID**
5. Go to "System Users" → Create new user → Generate token
6. Copy your **Access Token**

#### **B) Claude API Key**
1. Go to https://console.anthropic.com/account/keys
2. Click "Create New Key"
3. Copy your **API Key**

#### **C) Verify Token**
Just create any random string (you'll remember it):
```
my_verify_token_12345
```

### Step 2: Create GitHub Repository

1. Go to https://github.com/new
2. Name: `whatsapp-bot`
3. Description: `WhatsApp Bot with Claude AI`
4. Public ✓
5. Add README file ✓
6. Click **Create repository**

### Step 3: Upload Files to GitHub

1. Click **"Add file"** → **"Create new file"**
2. Name: `server.js` → Paste server code
3. Click **Commit**

4. Repeat for:
   - `package.json` (paste package.json content)
   - `.env` (paste .env content)

### Step 4: Deploy to Railway

1. Go to https://railway.app
2. Click **"New Project"**
3. Select **"Deploy from GitHub"**
4. Choose `whatsapp-bot` repository
5. Click **Deploy**

### Step 5: Add Environment Variables

1. In Railway dashboard, click your project
2. Click **"Variables"** tab
3. Add these 4 variables:

```
PHONE_NUMBER_ID=1173982849122291
WHATSAPP_API_TOKEN=EAABs8Co1234xxxxx
VERIFY_TOKEN=my_verify_token_12345
CLAUDE_API_KEY=sk-ant-v4-xxxxx
```

4. Click **Save**

### Step 6: Get Your Railway URL

1. Go to **Settings** tab
2. Find **"Public URL"** or **"Domain"**
3. Copy your URL (like: `https://whatsapp-bot.railway.app`)

### Step 7: Configure WhatsApp Webhook

1. Go to https://developers.facebook.com/apps/YOUR_APP_ID/whatsapp/
2. Find **"Configure Webhook"**
3. Fill in:
   - **Callback URL:** `https://your-railway-url/webhook`
   - **Verify token:** `my_verify_token_12345`
4. Click **"Verify and save"**
5. Done! ✅

---

## Test Your Bot

Send a message to your WhatsApp number. The bot should:
1. Show "typing..." indicator
2. Send back a Claude AI response
3. Work 24/7 automatically

---

## Troubleshooting

**"Webhook verification failed"**
- Make sure verify token matches in Railway variables
- Check callback URL includes `/webhook` at the end
- Wait 2 minutes for Railway to deploy

**"Bot doesn't reply"**
- Check all 4 environment variables are set in Railway
- Verify phone number ID is correct
- Check WhatsApp token is still valid

**"Claude API error"**
- Verify Claude API key is correct
- Check you have sufficient API credits
- Try again in 30 seconds

---

## How It Works

1. User sends WhatsApp message
2. Facebook sends webhook to Railway
3. Railway verifies the request
4. Claude AI generates response
5. Response sent back to WhatsApp
6. Done! ✅

---

## File Structure

```
whatsapp-bot/
├── server.js          (Main bot code)
├── package.json       (Dependencies)
├── .env              (Your credentials)
└── README.md         (This file)
```

---

## Environment Variables

| Variable | Value | Example |
|----------|-------|---------|
| PHONE_NUMBER_ID | Your WhatsApp phone ID | `1173982849122291` |
| WHATSAPP_API_TOKEN | WhatsApp access token | `EAABs8Co1234...` |
| VERIFY_TOKEN | Your secret token | `my_verify_token_12345` |
| CLAUDE_API_KEY | Anthropic API key | `sk-ant-v4-xxxxx` |

---

## Costs

- **Railway:** Free tier available (perfect for testing)
- **WhatsApp:** Free (up to 1000 messages/day on Business Account)
- **Claude API:** Pay as you go (~$0.01 per request)

---

## Support

If webhook fails:
1. Check Railway logs
2. Verify all credentials
3. Make sure Firebase URL has `/webhook` at end
4. Restart Railway deployment

---

## License

MIT

---

**Your WhatsApp bot is ready to go! 🚀**
