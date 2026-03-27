# 📐 Multi – Consolidated Mermaid Architecture Diagrams

Below are all architecture, workflow, authentication, and component diagrams for the **Multi AI Assistant** — fully GitHub‑compatible Mermaid.

---

## 1️⃣ High‑Level Architecture

```mermaid
flowchart TD

    A[User] -->|Voice Command| B[Voice Listener - Whisper or Vosk Portable]
    B -->|Text Output| C[Router Logic]

    C -->|Personal Query| D[Multi-Personal Agent]
    C -->|Technical Query| E[Multi-Tech Agent]

    D --> F[OpenWebUI Portable Backend]
    E --> F

    F -->|AI Response| G[Mascot UI Window]

    subgraph Security
        H[PIN Authentication]
    end

    A -->|Unlock App| H --> G
