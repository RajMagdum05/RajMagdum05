<!-- Dynamic Header -->
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=180&section=header&text=Raj%20Magdum&fontSize=42&fontAlignY=35&animation=twinkling&fontColor=ffffff" width="100%" />
</p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&duration=3000&pause=1000&color=36BCF7&center=true&vCenter=true&width=600&height=45&lines=People+-%3E+Problems+-%3E+Products;Python%2C+Applied+AI+%26+Product+Engineering" alt="Typing SVG" />
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/rajmagdum05/"><img src="https://img.shields.io/badge/-LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" /></a>&nbsp;
  <a href="https://rajmagdum05.github.io/RajPersonalPortfolio/"><img src="https://img.shields.io/badge/-Portfolio-000000?style=for-the-badge&logo=vercel&logoColor=white" /></a>&nbsp;
  <a href="mailto:rajmagdum6844@gmail.com"><img src="https://img.shields.io/badge/-Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" /></a>
</p>

---

### `$ whoami`

I don't start with technology. I start with **people**.  
I find what's quietly broken, then build AI systems and products that fix it — reliably.

`Python` · `FastAPI` · `OpenTelemetry` · `LLM Pipelines & Evals` · `Reinforcement Learning`

---

### 🔭 What I'm Building Now

**Retry-safe payments for MCP agents** — An agent calls a payment tool, the response times out, and it can't tell whether the money moved. I'm prototyping idempotent execution and outcome classification for [Peakflo's open-source pfMCP](https://github.com/peakflo/pfMCP) Xero server. → [**`Peakflo`**](https://github.com/RajMagdum05/Peakflo)

---

### 🏗️ Featured Projects

<table>
<tr>
<td width="50%" valign="top">

<h4>🔬 <a href="https://github.com/RajMagdum05/Pipeline-Autopsy">Pipeline Autopsy</a></h4>
<sub><b>Root-cause analysis for multi-stage AI pipelines</b></sub>
<br/><br/>

When an AI pipeline gives a bad result, the stage that fails is often not the one that caused it. Pipeline Autopsy ingests OpenTelemetry traces, rebuilds the execution graph, follows artifact lineage, and separates root causes from downstream symptoms.

**What makes it interesting:**
- 🎯 **Deterministic core** picks the root cause — LLM only explains it
- 🏭 Comes with a full **claims-processing pipeline** (OCR → quality gate → classification → extraction → validation)
- ✅ **340+ automated tests** across service, SDK, and claims backend
- 🔌 Pipelines connect via thin SDK over standard OTLP — no Autopsy-specific code needed

<p>
<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" />
<img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" />
<img src="https://img.shields.io/badge/OpenTelemetry-7B61FF?style=flat-square&logo=opentelemetry&logoColor=white" />
<img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" />
</p>

<sub>Status: Working prototype, run locally with Docker Compose. Synthetic data only.</sub>

</td>
<td width="50%" valign="top">

<h4>🚗 <a href="https://github.com/RajMagdum05/ML_Vehicle-Insurance-Prediction">Vehicle Insurance Prediction</a></h4>
<sub><b>End-to-end ML pipeline for insurance claim prediction</b></sub>
<br/><br/>

Predicts whether a vehicle insurance policy will result in a claim — a real-world risk assessment problem. Full pipeline from raw data to a live **Streamlit prediction app** where users input vehicle & policy details and get instant claim probability.

**What makes it interesting:**
- 📊 Complete **EDA → feature engineering → model training → deployment** pipeline
- 🖥️ **Interactive Streamlit UI** — select vehicle specs, policy details, get real-time predictions
- 🔄 Handles mixed data: text-numeric extraction, categorical encoding, feature scaling
- 📈 Multiple model comparison (Logistic Regression, KNN) with probability outputs

<p>
<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" />
<img src="https://img.shields.io/badge/Scikit--Learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white" />
<img src="https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white" />
<img src="https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white" />
</p>

<sub>Status: Complete. ML project with Streamlit prediction interface.</sub>

</td>
</tr>

<tr>
<td width="50%" valign="top">

<h4>🩺 <a href="https://github.com/RajMagdum05/Composio-tool-schema-doctor">Tool Schema Doctor</a></h4>
<sub><b>QA for AI tool definitions · <a href="https://tool-schema-doctor.netlify.app">live report ↗</a></b></sub>
<br/><br/>

Composio's tool schemas get translated for each model provider, and some translations silently drop constraints. I ran **930 tool schemas** through Composio's real provider adapters and turned what I found into a CLI, regression tests, and an evidence dashboard.

**What I found:**
- 🔴 Gemini conversion **dropped `enum` on 179 of 182 tools** that used it
- ⚠️ **114 of 930 tools** couldn't use OpenAI strict mode
- 🐛 **6 tools failed Vertex conversion** — issue later fixed upstream by Composio
- 🔒 Compatibility checks block network access and never execute tools

<p>
<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" />
<img src="https://img.shields.io/badge/HTML-E34F26?style=flat-square&logo=html5&logoColor=white" />
<img src="https://img.shields.io/badge/Netlify-00C7B7?style=flat-square&logo=netlify&logoColor=white" />
</p>

<sub>Status: Complete. Independent analysis, not affiliated with Composio.</sub>

</td>
<td width="50%" valign="top">

<h4>🦈 <a href="https://github.com/RajMagdum05/loan-shark-escape-env">Loan Shark Escape</a></h4>
<sub><b>RL environment for escaping predatory debt traps</b></sub>
<br/><br/>

A production-ready Reinforcement Learning challenge built to the [OpenEnv](https://github.com/meta-pytorch/OpenEnv) spec. Forces an AI agent to handle **sequential decision-making under uncertainty** — balancing short-term debt payments against compound interest and psychological spiral lock.

**What makes it interesting:**
- 🧠 **ReAct Agent Memory** — reasoning + acting architecture with strategic memory log
- 🎮 **Interactive Streamlit Dashboard** — visual debt tracking and manual play mode
- 🎲 **Deterministic evaluation** via seeded RNG tied to `task_id`
- 📏 Mathematically bounded `(0, 1)` grading schema validated with pytest

<p>
<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" />
<img src="https://img.shields.io/badge/Gymnasium-0081A5?style=flat-square&logo=openaigym&logoColor=white" />
<img src="https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white" />
<img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" />
</p>

<sub>Status: Working. OpenEnv-compliant server with Streamlit demo.</sub>

</td>
</tr>

<tr>
<td width="50%" valign="top">

<h4>💰 <a href="https://github.com/RajMagdum05/Peakflo">Peakflo — Retry-Safe Payments</a></h4>
<sub><b>Idempotent execution for MCP agent payment calls</b></sub>
<br/><br/>

If an AI agent's payment call times out, did the money move? Today the agent can't tell, so a retry pays twice. I reproduced this bug against Peakflo's open-source MCP server and built a fix.

**What I found & built:**
- 🐛 **Reproduced the duplicate-payment bug** — timeout → retry → 2 payments
- 🔑 Built **idempotency key system** for safe retries
- 🧪 **94-test suite** with fault-injection mock of the Xero API
- 📝 Found the error message is just `"Error: "` — agent can't reason about it

<p>
<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" />
<img src="https://img.shields.io/badge/MCP-FF6B35?style=flat-square" />
<img src="https://img.shields.io/badge/Xero_API-13B5EA?style=flat-square&logo=xero&logoColor=white" />
<img src="https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white" />
</p>

<sub>Status: Independent prototype. Not an official Peakflo project. Local mock only, no real money.</sub>

</td>
<td width="50%" valign="top">

<h4>🎧 <a href="https://github.com/RajMagdum05/Hearly">Hearly</a> · <a href="https://rajmagdum05.github.io/RajPersonalPortfolio/">🌐 Portfolio</a></h4>
<sub><b>More work worth checking out</b></sub>
<br/><br/>

**Hearly** — Chrome extension (Manifest V3) for Meet, Zoom, Teams. Keeps nearby voices out of your meeting using MFCC voice-profile gating. Transcription with Deepgram + on-device Whisper. Co-built with Rehan Sanadi. *Part of YC Startup School.*

<br/>

**Portfolio** — Clean, responsive personal portfolio built with Next.js and TypeScript. <a href="https://rajmagdum05.github.io/RajPersonalPortfolio/">Visit live site ↗</a>

<br/>

<p>
<img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" />
<img src="https://img.shields.io/badge/Chrome_Extension-4285F4?style=flat-square&logo=googlechrome&logoColor=white" />
<img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" />
<img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white" />
</p>

</td>
</tr>
</table>

---

### ⚡ Tech Stack

<p align="center">
  <img src="https://skillicons.dev/icons?i=python,typescript,javascript,fastapi,react,nextjs,docker,postgres,git,linux&perline=10" />
</p>

<details>
<summary><b>📋 Full breakdown</b></summary>
<br>

| Area | Technologies |
|:-----|:------------|
| **Languages** | Python, TypeScript, JavaScript, SQL, C++ |
| **Backend** | FastAPI, PostgreSQL, SQLAlchemy, Docker |
| **AI/ML** | LLM pipelines & evals, OpenTelemetry, OCR (Tesseract, PyMuPDF), Reinforcement Learning, Gymnasium, Scikit-Learn |
| **Agent Systems** | MCP, tool-calling, guardrails, schema validation |
| **Frontend** | React, Next.js, Streamlit, Chrome Extensions (Manifest V3) |
| **DevOps** | Docker Compose, GitHub Actions, Netlify |

</details>

---

### 🧠 How I Work

```
├── Understand the problem before the technology
│   └── I reproduce the failure before I design the fix
├── Make wrong answers visible
│   └── Quality gates, evidence-backed outputs, deterministic checks around the model
└── Keep scope honest
    └── Every project says what works, what doesn't, and what data it ran on
```

---

### 📊 GitHub Activity

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=RajMagdum05&show_icons=true&theme=tokyonight&hide_border=true&count_private=true&bg_color=0d1117" width="48%" />
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=RajMagdum05&theme=tokyonight&hide_border=true&background=0d1117" width="48%" />
</p>

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=RajMagdum05&theme=tokyo-night&hide_border=true&bg_color=0d1117&color=36BCF7&line=36BCF7&point=ffffff" width="96%" />
</p>

<!-- Snake Animation -->
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/RajMagdum05/RajMagdum05/output/github-snake-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/RajMagdum05/RajMagdum05/output/github-snake.svg">
  <img alt="github contribution snake animation" src="https://raw.githubusercontent.com/RajMagdum05/RajMagdum05/output/github-snake.svg" width="100%">
</picture>

---

### 📬 Let's Connect

I'm looking for an **AI engineering internship** on a team putting LLM or agent systems in front of real users. Mumbai, Bangalore, or remote.

> *The best way to evaluate me is to open any repo above and ask me why I made one of its decisions.*

<p align="center">
  <a href="https://www.linkedin.com/in/rajmagdum05/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" /></a>&nbsp;
  <a href="https://rajmagdum05.github.io/RajPersonalPortfolio/"><img src="https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=vercel&logoColor=white" /></a>&nbsp;
  <a href="mailto:rajmagdum6844@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" /></a>
</p>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=RajMagdum05&style=for-the-badge&color=36BCF7" />
</p>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=100&section=footer" width="100%" />
</p>
