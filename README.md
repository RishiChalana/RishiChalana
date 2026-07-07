<!--
  RISHI CHALANA · GitHub profile README
  Repo:  RishiChalana/RishiChalana   (must match your username exactly)
  Files: README.md + status-board.svg  (commit BOTH to the repo root)
  Fill the 3 <<FILL>> links below, then commit.
-->

<div align="center">

<img src="https://raw.githubusercontent.com/RishiChalana/RishiChalana/main/status-board.svg" width="100%" alt="Rishi Chalana — system status board" />

<p>&nbsp;</p>

<b>Final-year CS @ VIT Vellore.</b> I build real-time multi-agent AI, applied-ML research, and production backends — and I ship them.

<p>
<a href="<<FILL: LinkedIn URL>>">LinkedIn</a> &nbsp;·&nbsp;
<a href="mailto:<<FILL: email>>">Email</a> &nbsp;·&nbsp;
<a href="<<FILL: portfolio / resume URL>>">Portfolio</a> &nbsp;·&nbsp;
<a href="https://echo-room-ten.vercel.app">EchoRoom (live)</a>
</p>

</div>

---

## Flagship builds

> Three I'd defend line-by-line. Each notes **the hard part** — the bug or design call that actually took engineering, not the feature list.

### 🎙️ EchoRoom — real-time multi-agent AI speech coach
`FastAPI` · `Next.js 14` · `PostgreSQL` · `Redis` · `Celery` · `LangGraph` · `faster-whisper` · `Gemini 2.5`
&nbsp;·&nbsp; [code](https://github.com/RishiChalana/EchoRoom) · [live](https://echo-room-ten.vercel.app)

Live audio → transcription → engagement scoring → coaching report, streamed over WebSockets. Full production stack: NextAuth + JWT auth, GitHub Actions CI, Redis-backed rate limiting, Sentry, **57 passing tests**.

**The hard part** — identity originally trusted a spoofable `X-User-Email` header. Replaced it with JWT-backed auth, and got rate limiting to read the *real* client IP through Railway's reverse proxy via `X-Forwarded-For`. Added WebSocket reconnection with exponential backoff + a 60s audio buffer so a dropped socket never loses a session.

### 🛡️ SENTINEL — runtime ML model-integrity monitoring
`Behavioral fingerprinting` · `PostgreSQL` · `Redis` · `MinIO` · `WebSockets` · `Docker (12-service stack)`
&nbsp;·&nbsp; repo private — **patent-track**

Detects model **substitution and backdoor tampering at runtime** via black-box behavioral fingerprinting — no access to model weights. Provisional filing under review with the VIT IPR cell.

**The hard part** — proving it fires. On a live backdoor swap the composite integrity score dropped **1.000 (GREEN) → 0.483 (RED)** and the WebSocket alert triggered end-to-end. The defensible novelty is the integrated runtime-rotation + composite-scoring mechanism, narrowed against prior art (IPGuard, ASIA CCS '21).

### 🪐 AstroFoundation — multi-modal exoplanet classification
`Cross-attention fusion` · `LangGraph agent` · `Kepler data` · `W&B`
&nbsp;·&nbsp; capstone, in development

Classifies Kepler objects across five valid classes by fusing **three modalities** — light curves, centroid / pixel-difference time series, and stellar catalog metadata — with a cross-attention fusion head, plus a LangGraph agent that writes the scientific report. Baseline: Google's AstroNet.

**The hard part** — getting the science right, not just the model. Dropped gamma-ray bursts and supernovae (not Kepler-observable) and swapped a FITS/ViT modality for centroid time-series + metadata, keeping the whole pipeline physically honest instead of chasing benchmark noise.

<sub>More on the <a href="https://github.com/RishiChalana?tab=repositories">repositories tab</a> — Helm (AI finance copilot), LeakGuard Industrial, SEO Content Intelligence Pipeline.</sub>

---

## Stack

**Languages** `Python` `TypeScript` `JavaScript` `Java` `C++`
**AI / ML** `TensorFlow` `Keras` `scikit-learn` `LangGraph` `Hugging Face` `Gemini`
**Backend** `FastAPI` `Django` `Celery` `Redis` `PostgreSQL`
**Frontend** `Next.js` `React` `React Native` `Tailwind`
**Infra** `Docker` `GitHub Actions` `Railway` `Vercel` `Sentry`
