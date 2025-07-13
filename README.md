# Agentic Ethereum Hackathon India

**🛠 Project Title - FarmVerse (Team FarmVerse)**

Welcome to our submission for the Agentic Ethereum Hackathon by Reskilll & Geodework! This repository includes our project code, documentation, and related assets.

---

📌 Problem Statement  
*Brief Description of the Challenge and Why It Matters*

India’s 600 million farmers are largely excluded from formal financial systems. Despite driving a ₹50 lakh crore agricultural economy, most have no credit history, face exploitative interest rates from loan sharks, and suffer immense losses from poor market access and lack of climate protection. Every 30 minutes, a farmer dies by suicide due to debt distress.

This systemic exclusion—rooted in lack of data visibility, infrastructure, and financial intelligence—represents a ₹400 billion gap in agri-finance and a massive untapped opportunity for inclusive development.

*Why It Matters:*
Addressing this challenge is critical not only for economic justice but also for food security, climate action, and rural empowerment. Bridging this gap through autonomous AI agents and decentralized finance (DeFi) has the potential to uplift millions of lives, unlock new markets, and turn rural farms into investable digital enterprises.

FarmVerse aims to build a future where every farmer can access credit, insurance, and markets through a simple WhatsApp message—transforming India's agricultural economy from survival-driven to opportunity-driven.---

💡 Our Solution  
We built FarmVerse, a WhatsApp-first, AI-powered financial system that brings micro-loans, insurance, carbon credits, and market access to farmers—without apps or paperwork. Designed for smallholder farmers in India, it uses real-time satellite and weather data to automatically trigger smart contracts on Ethereum.

Think of it as an invisible, always-on financial agent that turns every farm into a digital business—creditworthy, insurable, and investable. Farmers simply interact in their local language on WhatsApp, while behind the scenes, our AI agents handle everything from loan approvals to crop sales. It’s impactful because it doesn’t ask farmers to change how they work—it meets them where they are, and lifts them into the formal economy, one decision at a time.

---

🧱 Tech Stack  

Frontend:
 React (v18)
 Tailwind CSS for styling (WhatsApp-native theme)
 React Router v6 for client-side routing
 Axios for HTTP requests
Backend:
 Node.js (v18) with Express.js
 MongoDB for data storage (policies, loans, alerts)
 Ethers.js for on-chain interactions
AI & Automation:
 Python 3.10 with FastAPI (LLM prompt optimization & proxy)
 LangChain for prompt orchestration
 OpenAI GPT-4 (where applicable)
LLM Serving:
 Meta Llama 2 (7B Chat) via Hugging Face Inference API (“Hugging Chain” integration)
 FastAPI /generate endpoint to proxy Llama 2 calls
Smart Contracts & Blockchain:
 Solidity contracts (Lending, Insurance, MarketPrice)
 Hardhat for compilation, testing, and deployment to Sepolia
 deployments/sepolia.json for address/ABI artifacts
Infrastructure & Orchestration:
 Docker & Docker Compose to containerize all services
 Ngrok (development) for WhatsApp webhook tunneling
 PM2 (or similar) for process management
Messaging UI:
 Twilio WhatsApp API (Node.js) for conversational flows
 Python proxy for LLM-based intent classification & repliesesign)

--


---
Here’s a copy-&-paste-ready directory structure for the entire FarmVerseH2 monorepo:

```
farmverseH2/
├── Makefile
├── docker-compose.yml
├── README.md
├── .env.example
│
├── contract/
│   ├── hardhat.config.js
│   ├── scripts/
│   │   └── deploy.js
│   ├── contracts/
│   │   ├── Lending.sol
│   │   ├── Insurance.sol
│   │   └── MarketPrice.sol
│   └── deployments/
│       └── sepolia.json
│
├── backend/
│   ├── .env.example
│   ├── package.json
│   ├── src/
│   │   ├── app.js
│   │   ├── routes/
│   │   ├── controllers/
│   │   └── utils/
│   └── deployments/        ← symlink or volume from contract/deployments
│
├── ai-agents/
│   ├── .env.example
│   ├── package.json
│   ├── weatherTrigger.js
│   ├── satelliteTrigger.js
│   ├── priceTrigger.js
│   └── llmPromptOptimizer.py
│
├── whatsapp-bot/
│   ├── .env.example
│   ├── package.json
│   ├── twilioWebhook.js
│   ├── dialogManager.js
│   ├── sessionStore.js
│   ├── chatResponder.py
│   └── flows/
│       ├── loanFlow.js
│       ├── insuranceFlow.js
│       └── priceFlow.js
│
├── llm-server/
│   ├── .env.example
│   ├── requirements.txt
│   ├── Dockerfile
│   ├── app.py
│   └── models/             ← optional local model folder
│
└── frontend/
    ├── .env.example
    ├── package.json
    ├── tailwind.config.js
    ├── postcss.config.js
    ├── public/
    │   └── index.html
    └── src/
        ├── index.css
        ├── index.js
        ├── App.jsx
        ├── api.js
        ├── components/
        │   ├── Sidebar.jsx
        │   ├── ChatWindow.jsx
        │   ├── ChatInput.jsx
        │   ├── LoanStatus.jsx
        │   ├── PolicyStatus.jsx
        │   └── PriceDisplay.jsx
        └── pages/
            ├── Dashboard.jsx
            └── Analytics.jsx
```  **https://github.com/varshan007/farmverseH1.git**
