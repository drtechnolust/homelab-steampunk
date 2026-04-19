# AI Stack

A local AI and voice-services layer built around self-hosted model inference, browser-based interaction, speech processing, and assistant-oriented tooling.

> Core runtime: Ollama  
> Main interface: Open WebUI  
> Voice services: faster-whisper, Piper, openWakeWord  
> Role in homelab: local AI experimentation and practical AI-assisted workflows

---

# At a Glance

| Area | Design |
|:--|:--|
| Model runtime | Ollama |
| Main interface | Open WebUI |
| Speech-to-text | faster-whisper |
| Text-to-speech | Piper |
| Wake-word detection | openWakeWord |
| Deployment model | Local and self-hosted |
| Primary value | Private AI workflows and experimentation |

---

# Stack Layout

| Component | Role | Notes |
|:--|:--|:--|
| Ollama | Model runtime | Runs local LLMs and provides the core inference layer |
| Open WebUI | User interface | Browser-based front end for interacting with local models |
| faster-whisper | Speech-to-text | Local transcription service for voice workflows |
| Piper | Text-to-speech | Local neural voice synthesis |
| openWakeWord | Wake-word detection | Supports assistant-style voice triggering |

---

# Design Intent

This stack exists to keep AI workflows local, flexible, and useful inside the broader homelab.

It is designed to support:

- local model inference
- browser-based AI interaction
- speech-to-text workflows
- text-to-speech workflows
- wake-word driven experimentation
- AI integration with other homelab services

The goal is not just to run models, but to build a private AI layer that can support real workflows over time.

---

# Core Runtime

Ollama is the foundation of the AI stack.

Its role includes:

- running local language models
- providing a self-hosted inference runtime
- supporting experimentation with different models
- acting as the backend for browser-based AI interfaces

This makes Ollama the key service that turns the homelab into a usable local AI environment.

---

# Browser Interface

Open WebUI is the main user-facing layer of the stack.

Its role includes:

- providing a browser-based interface for local AI usage
- making local model interaction easier and more approachable
- giving the AI layer a practical day-to-day front end
- acting as the main human-facing entry point into the model stack

Together, Ollama and Open WebUI form the core interaction model for local AI use.

---

# Voice Services

| Service | Function |
|:--|:--|
| faster-whisper | Local speech-to-text transcription |
| Piper | Local neural text-to-speech |
| openWakeWord | Wake-word detection for assistant-style workflows |

These services extend the stack beyond text-only interaction and make it possible to experiment with voice-aware local AI workflows.

---

# Workflow View

```text
User Input / Prompt / Voice
            ↓
   Open WebUI / Voice Services
            ↓
          Ollama
            ↓
    Local Model Inference
            ↓
 Response / Text / Speech Output
