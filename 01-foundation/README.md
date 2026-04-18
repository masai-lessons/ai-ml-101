# Session 1: AI Foundations, Models & Agentic Coding

> **Duration:** 2 hours  
> **Format:** Concept + hands-on build  
> **You need:** Browser, Google account, Cursor (recommended) or any code editor, Antigravity (optional)

---

## Learning outcomes
By the end of this session, you will be able to:
- Explain how computers run programs (high-level code → interpreter/compiler → machine code)
- Explain what modern AI/LLMs do (pattern prediction) and the limits
- Write strong prompts using a structured framework (CO-STAR)
- Use Cursor basics for “agentic coding”
- Create a free Gemini API key and use it safely
- Build a small AI app (“Fridge Hero”) using HTML/CSS/JS + Gemini API

---

## 1) How computers “understand” code
- Computers ultimately operate on **machine instructions** (binary at the lowest level).
- Human-friendly languages (Python/JS/Java/etc.) are translated into machine-executable steps by:
  - **Interpreters** (run code step-by-step, common in Python setups)
  - **Compilers** (translate code before running, common in C/C++)
- Key idea: programming languages are **translation layers** between human instructions and machine execution.

---

## 2) What is AI (practical understanding)
- AI systems perform tasks that usually require human intelligence.
- Most modern AI (like ChatGPT/Gemini/Claude) is not “magic” or “conscious.”
- LLMs generate outputs by predicting what comes next based on patterns learned from large data.
- Important consequence: **better inputs (prompts) → better outputs**.

---

## 3) Prompting: the CO-STAR framework (must know)
A strong prompt usually includes:

- **C — Context**: background + situation  
- **O — Objective**: what you want  
- **S — Style**: bullet points/table/steps, etc.  
- **T — Tone**: friendly, professional, strict, etc.  
- **A — Audience**: who it’s for  
- **R — Response format**: exact structure you want

### Prompt template
```
Context:
Objective:
Style:
Tone:
Audience:
Response format:
Constraints:
```

### Useful prompting techniques
- **Role assignment**: “You are a senior frontend engineer…”
- **Few-shot examples**: provide 1–2 examples of the output you want
- **Constraints**: “exactly 3 steps”, “under 120 words”, “return JSON only”

### Prompt examples used in lecture (copy-paste)
**Example 1: Bad vs good prompt (travel itinerary)**

Bad (too vague):
```
Tell me about Jaipur
```

Good (specific + structured):
```
You are an experienced Rajasthani travel guide who has lived in Jaipur for 20 years.
Create a 1-day Jaipur itinerary for a college student visiting for the first time. Include:
- Morning, afternoon, evening plan with timings
- Must-visit spots (not just tourist traps — include local favorites)
- Street food recommendations with specific stall names/areas
- Budget estimate in INR
- Travel tips (auto vs cab vs walking)
Tone: Friendly, like a local friend showing them around.
```

**Example 2: Few-shot prompting (generate similar captions)**
```
Here are good Instagram caption examples:
- "Chai, sunset, and zero notifications." (travel)
- "Beta, placement ho gayi!" (college)

Now write 5 captions for my Ladakh trip photos.
```

**Example 3: Structured comparison (decide between two ideas)**
```
I'm deciding between two startup ideas. Think step-by-step:

Idea A: A tiffin delivery app for hostel students
Idea B: An AI tutor for competitive exam prep (JEE/NEET)

Evaluate each on:
1. Market size in India
2. How hard is it to build?
3. Can a solo founder do it?
4. Revenue potential

Then give your recommendation with reasoning.
```

---

## 4) Model landscape (which model to use?)
Different models have different strengths:

- **GPT (OpenAI)**: strong reasoning + coding quality
- **Claude (Anthropic)**: great for long documents and structured writing
- **Gemini (Google)**: strong multimodal + large context; good free options

### Quick cheat sheet
- **Need best overall reasoning/coding** → GPT-class models  
- **Need to analyze long docs** → Claude-class models  
- **Need free + large context + easy onboarding** → **Gemini Flash** (we’ll use this)

---

## 5) Agentic coding with Cursor (basics)
You are shifting from “typing every line” to “directing + reviewing”.

### Shortcuts
- `Cmd+K` → inline AI edit in current file
- `Cmd+L` → chat with your project/codebase
- `@file` → reference a specific file in chat

---

## 6) Get your Gemini API key (free)
We’ll use **Gemini 1.5 Flash** for the hands-on project.

### Steps
1. Open `https://aistudio.google.com/`
2. Sign in with your Google account
3. Click **Get API Key**
4. Click **Create API Key** (new project is fine)
5. Copy the key (looks like `AIza...`)

### API key safety (very important)
- **Never hardcode keys** in frontend code that you publish.
- **Never commit keys** to GitHub.
- Store keys in `.env` locally and ensure `.env` is in `.gitignore`.

---

## 6.1) Download Antigravity (optional)
Antigravity is an optional tool we referenced in the lecture for fast “voice-to-app / prompt-to-app” building.

### Steps
1. Download and install Antigravity (shared by the instructor in class).
2. Open Antigravity and complete the first-time setup.
3. Keep it ready for later sessions where we’ll build quicker prototypes.

---

## 7) Hands-on: Build “Fridge Hero” (AI Recipe Generator)
**Goal:** Input 3 ingredients → click button → AI generates a dish name + 3 cooking steps.

### What you will build
- A simple webpage with:
  - 3 ingredient inputs
  - “Cook Magic” button
  - Result card (dish name + steps)
  - Loading + error states

### Suggested folder/files
- `index.html`
- `style.css`
- `script.js`

### Prompt you’ll send to Gemini (recommended)
Ask for a machine-readable output to avoid messy parsing:

```
You are a creative Michelin-star chef.
Given these ingredients: {ing1}, {ing2}, {ing3}

Create:
1) A fancy dish name
2) Exactly 3 short cooking steps

Return JSON only in this format:
{ "dishName": "string", "steps": ["step1", "step2", "step3"] }
```

### Testing ideas
- Paneer + Tomato + Cream
- Aloo + Jeera + Green chilli
- Chicken + Curd + Garam masala

---

## 8) Deploy (optional)
Choose one:
- **Netlify**: drag & drop the project folder
- **GitHub Pages**: push repo → enable Pages in Settings
- **Vercel**: deploy with Vercel CLI (optional)

---

## 9) Homework (optional but recommended)
- Improve Fridge Hero:
  - Cuisine selector (North Indian / South Indian / Chinese)
  - Veg/non-veg toggle
  - Spice level
  - Better UI + mobile responsiveness
- Build “Samjha Kya”:
  - Enter a topic → explanation in simple Hindi + English
- Start a “prompt library”:
  - 10 prompts for different tasks (learning, coding, writing, planning)

---

## Next sessions (preview)
- **Session 2**: Research, Deep Research, MCP, Voice AI
- **Session 3**: Latent space, diffusion, HuggingFace, running models locally
- **Session 4**: Reinforcement learning, deployment, autonomous agents
