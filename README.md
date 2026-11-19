# Raj Magdum

I build AI systems that **fail loudly instead of silently**, and the tools that show *why* they failed.

Most of my work starts with something quietly broken in a real workflow, like a claims pipeline that returns a confident wrong answer, a tool schema that loses its constraints on the way to the model, or a payment retry that charges twice. I reproduce the problem first and then build the smallest system that fixes it.

`Python` · `FastAPI` · `OpenTelemetry` · `LLM pipelines & evals` · Kolhapur, India

---

### Now building

**Retry-safe payments for MCP agents.** An agent calls a payment tool, the response times out, and it can't tell whether the money moved. I'm prototyping idempotent execution and outcome classification for [Peakflo's open-source pfMCP](https://github.com/peakflo/pfMCP) Xero server. So far: a fault-injection mock of the Xero API, a reproduction of the duplicate-payment bug, and a 94-test suite. This is an independent prototype, not an official Peakflo project. → [`Peakflo`](https://github.com/RajMagdum05/Peakflo)

---

### Selected work

#### [Pipeline Autopsy](https://github.com/RajMagdum05/Pipeline-Autopsy): root-cause analysis for multi-stage AI pipelines
When an AI pipeline gives a bad result, the stage that fails is often not the one that caused it. Pipeline Autopsy ingests standard OpenTelemetry traces, rebuilds the execution graph, follows artifact lineage (which stage read and wrote what), and separates the root cause from downstream symptoms.
- A **deterministic core picks the root cause**. The LLM only helps explain it, and the output falls back to a template when evidence is thin.
- Pipelines connect through a small SDK over plain OTLP, so they need no Autopsy-specific code.
- The system it diagnoses is a **claims-processing pipeline I built in the same repo**: OCR → quality gate → document classification → schema-specific extraction → validation. Every extracted field must cite a quote and page, so a bad scan stops the pipeline instead of producing a confident wrong value.
- 340+ automated tests across the service, SDK and claims backend, plus recorded diagnosis cases in CI.

*Status: working prototype, run locally with Docker Compose. Synthetic data only, not deployed.*

#### [Tool-Schema Doctor](https://github.com/RajMagdum05/Composio-tool-schema-doctor): QA for AI tool definitions · [live report](https://tool-schema-doctor.netlify.app)
Composio's tool schemas get translated for each model provider, and some translations fail or silently drop constraints. I ran 930 tool schemas through Composio's real provider adapters at a pinned commit and turned what I found into a CLI, regression tests and an evidence dashboard.
- Found that Gemini conversion dropped `enum` on 179 of 182 tools that used it. Separately, 114 of the 930 tools couldn't use OpenAI strict mode, and 6 failed Vertex conversion (an issue Composio later fixed upstream).
- Compatibility checks block network access and never execute tools. Live model evaluation is opt-in.

*Status: complete for the analyzed snapshot. Independent analysis, not affiliated with Composio.*

#### [Hearly](https://github.com/RajMagdum05/Hearly): keep other people's voices out of your meetings
If you join calls from a hostel, lab or shared room, people near you end up in the meeting. Hearly is a Chrome extension (Manifest V3) for Meet, Zoom and Teams. It captures meeting audio, transcribes it with Deepgram streaming or on-device Whisper (Transformers.js), and tests an MFCC voice-profile gate in an AudioWorklet so only the enrolled speaker reaches the call.
- Co-built with Rehan Sanadi. I built the voice enrollment and profile-gating engine and the settings and transcript flows.

*Status: MVP. Transcription works; voice filtering is experimental. Part of YC Startup School.*

---

### What I work with
**Languages:** Python, JavaScript/TypeScript, SQL
**Backend:** FastAPI, PostgreSQL, SQLAlchemy, Docker
**AI systems:** LLM extraction with strict schemas, OCR pipelines (Tesseract, PyMuPDF), guardrails & evals, agent tool-calling, MCP
**Observability:** OpenTelemetry, Jaeger
**Frontend (when needed):** React, Next.js, Chrome extensions

---

### How I work
- **Understand the problem before the technology.** I reproduce the failure before I design the fix.
- **Make wrong answers visible.** I use quality gates, evidence-backed outputs and deterministic checks around the model, not just a better prompt.
- **Keep scope honest.** Every project above says what works, what doesn't yet, and what data it ran on.

Outside code: I was a Campus Ambassador for E-Cell IIT Bombay, a MumbaiHacks finalist, and a B.Tech CSE (AI & ML) student, graduating 2027.

---

### Let's talk
I'm looking for an AI engineering role, internship or early-career, on a team putting LLM or agent systems in front of real users. Mumbai, Bangalore or remote.
The best way to evaluate me is to open any repo above and ask me why I made one of its decisions.

[LinkedIn](https://www.linkedin.com/in/rajmagdum05/) · [Email](mailto:rajmagdum6844@gmail.com)
