<div align="center">

# ⚡ `jc-agent`
### The Hyper-Fast, Provider-Agnostic Terminal AI Workstation & Persistent MCP Hub
**Zero-bloat native Rust. Zero-JSON configuration. Hardware-grade security. Single-hotkey model switching.**

---

### 🌐 Know More About Me & My Creations
[![Portfolio](https://img.shields.io/badge/Portfolio-ashim.dev-FF6B6B?style=for-the-badge&logo=googlechrome&logoColor=white)](https://ashim.dev)
[![GitHub](https://img.shields.io/badge/GitHub-MaitohAshimHu-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/MaitohAshimHu)

### 🤝 Hire • Collaborate • Discuss • Connect
[![WhatsApp](https://img.shields.io/badge/WhatsApp-Chat_Now-25D366?style=for-the-badge&logo=whatsapp&logoColor=white)](https://wa.me/916204312017)
[![Email](https://img.shields.io/badge/Email-ashim.dev.sec@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:ashim.dev.sec@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-bharydangerous-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/bharydangerous)
[![Instagram](https://img.shields.io/badge/Instagram-@bharydangerous-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://instagram.com/bharydangerous)

<p align="center">
  <b><a href="https://ashim.dev">🌐 Portfolio Website</a></b> •
  <b><a href="https://github.com/MaitohAshimHu">🐙 Public GitHub</a></b> •
  <b><a href="mailto:ashim.dev.sec@gmail.com">💼 Hire & Collaborate</a></b> •
  <b><a href="https://wa.me/916204312017">💬 WhatsApp (+91 6204312017)</a></b> •
  <b><a href="https://linkedin.com/in/bharydangerous">🔗 LinkedIn</a></b> •
  <b><a href="https://instagram.com/bharydangerous">📸 Instagram</a></b>
</p>

---

[![Rust](https://img.shields.io/badge/Language-Rust_2021-DEA584?style=for-the-badge&logo=rust&logoColor=white)](https://www.rust-lang.org/)
[![Linux](https://img.shields.io/badge/Platform-Linux_%2F_Omarchy_%2F_Arch-FCC624?style=for-the-badge&logo=arch-linux&logoColor=black)](https://archlinux.org/)
[![Architecture](https://img.shields.io/badge/Core-Tokio_%2B_Ratatui-FF6B6B?style=for-the-badge)](https://ratatui.rs/)
[![Security](https://img.shields.io/badge/Security-OS_Keyring_Native-4EBA6F?style=for-the-badge&logo=keepassxc&logoColor=white)](https://specifications.freedesktop.org/secret-service/)
[![Providers](https://img.shields.io/badge/Providers-100%25_Agnostic-8A2BE2?style=for-the-badge)](https://openrouter.ai/)
[![Status](https://img.shields.io/badge/Status-Private_Beta_%2F_VC_Stage-FF4500?style=for-the-badge)](#-the-startup-vision--investors)

<br/>

```text
 ╔══════════════════════════════════════════════════════════════════════════════╗
 ║  [deepseek-r1] | Venice AI | Tools: 263 (All) | Tokens: 1,842 | F2: Next    ║
 ╠══════════════════════════════════════════════════════════════════════════════╣
 ║  User: Decompile main() in the target binary and check for buffer overflows  ║
 ║                                                                              ║
 ║  Assistant: Scanning target section headers...                               ║
 ║  [tool] rea_ghidra_decompile · running                                       ║
 ║                                                                              ║
 ║  ┌── Approve Tool Call: rea_ghidra_decompile ─────────────────────────────┐  ║
 ║  │ [Y] Approve once   [N] Deny   [A] Always allow for session             │  ║
 ║  │ { "function": "main", "decompiler": "Ghidra-11.2", "verbose": false }  │  ║
 ║  └────────────────────────────────────────────────────────────────────────┘  ║
 ╠══════════════════════════════════════════════════════════════════════════════╣
 ║ > Input: Analyze stack frame allocation and propose mitigation... ⠋          ║
 ╚══════════════════════════════════════════════════════════════════════════════╝
```

</div>

---

## 🎯 The Problem: Why Does Every AI Dev Tool Feel Broken?

Let’s be honest for a second. If you’re a software engineer, reverse engineer, or offensive security researcher living in the terminal, modern AI tools are driving you crazy:

- 💸 **The $20–$40/Month "Wrapper Tax"**: Closed-source tools (Cursor, Windsurf, Copilot) charge heavy monthly seat subscriptions just to act as an Electron wrapper around standard API inference.
- 🦣 **RAM-Guzzling Electron Bloat**: Why should an editor agent eat 4 GB to 8 GB of RAM and spin up your laptop fans just to stream text?
- 🔒 **Cloud Lock-in & Corporate Hostage**: You’re stuck with whatever models *they* approve. Want to use **Venice AI**, **NVIDIA NIM**, **OpenRouter**, local **Ollama**, or uncensored models for vulnerability analysis? Good luck hacking custom proxy servers.
- 💥 **The "Model Switch Amnesia"**: In almost every existing tool, switching from a fast 8B model to a 70B reasoning model mid-thought resets your chat session, clears context, and kills all running tool processes.
- 🌊 **The 300-Tool Context Burn**: When you hook up serious tooling (like Ghidra / REA with 260+ native tools), existing agents blindly dump all 260 JSON schemas into the prompt on every turn, burning your token budget and inducing hallucinations.
- 🔑 **Plaintext API Keys in Dotfiles**: Putting raw production keys into plaintext JSON or YAML files on disk is an opsec nightmare.

---

## 🚀 The Solution: Meet `jc-agent`

`jc-agent` is an ultra-fast, native Rust terminal AI platform built specifically for Linux power users, developers, and security pros. It’s built from the ground up on **Tokio** and **Ratatui** with a single uncompromising philosophy: **Zero bloat, zero lock-in, zero plaintext secrets, and absolute freedom.**

### 💎 What Sets It Apart:

| Feature | Legacy AI Dev Tools | `jc-agent` |
| :--- | :---: | :---: |
| **Engine Runtime** | Heavy Electron / Node.js (2GB+ RAM) | **Native Rust (< 25MB RAM, instant launch)** |
| **Provider Freedom** | Walled garden or restricted proxies | **100% Agnostic (Venice, NIM, Ollama, DeepSeek, etc.)** |
| **Mid-Chat Model Switching** | Wipes context & restarts tools | **1-Hotkey (`F2` / `Ctrl+M`) — Context & Tools Stay Live!** |
| **Tool Hub (MCP)** | Fleeting, fragile child processes | **Persistent stdio hub (Ghidra, REA, custom servers)** |
| **Context Protection** | Dumps every tool into every prompt | **Scoped Profiles (`Ctrl+T` All / RE / ChatOnly)** |
| **API Key Security** | Plaintext config files on disk | **Linux OS Keyring (`libsecret` / Secret Service)** |
| **Setup Experience** | Manual JSON / YAML editing | **Interactive Zero-JSON terminal wizards** |
| **Cybersecurity / Reversing** | Censors security queries | **100% Uncensored pass-through ready** |

---

## ⚡ Core Features

### 1. 🔄 Instant Hotkey Model Switching (`F2` & `Ctrl+M`)
Need a lightning-fast model for scaffolding, but want to switch to a heavyweight reasoning model (like DeepSeek-R1 or Claude 3.5 Sonnet) for a complex bug or decompilation analysis?
- Hit **`F2`** to immediately cycle to your next model in 1 millisecond.
- Hit **`Ctrl+M`** (or `Alt+M`) to pop up a sleek, fuzzy-searchable model picker overlay.
- **Your conversation history stays intact. Your running MCP tools stay connected. No restart needed.**

### 2. 🧰 Persistent MCP Tool Hub with Scoped Profiles (`Ctrl+T`)
`jc-agent` runs a persistent JSON-RPC 2.0 stdio hub. Connect tools like **REA (Reverse Engineering Agents) + Ghidra** once, and they stay connected across your entire working session.
- **260+ REA tools auto-discovered** on startup.
- **Scoped Tool Profiles**: Hit **`Ctrl+T`** to toggle instantly between:
  - 🌐 **All Tools**: Full access to all connected MCP servers.
  - 🔬 **RE / Ghidra Only**: Automatically isolates reverse engineering tools by namespace.
  - 💬 **Chat Only**: Shuts off tool schemas completely so 260 tools don't burn tokens during normal coding or ideation.

### 3. 🛡️ Interactive Inline Tool Approvals
Never worry about an autonomous agent running wild. 
- When an LLM calls a tool, a high-contrast modal pops up with formatted, scrollable JSON arguments.
- **`[Y]`** Approve once.
- **`[N]`** / **`Esc`** Deny gracefully.
- **`[A]`** Always allow this specific tool for the current session.

### 4. 🧙 Zero-JSON Interactive Wizards
Never edit a messy `.json` or `.yaml` file again. `jc-agent` includes clean, foolproof interactive wizards:
```bash
# Add any LLM provider with auto-detection & secure keyring storage:
jc-agent model add

# Manage your models with a single command:
jc-agent model list
jc-agent model set-default venice-deepseek

# Add & test persistent MCP tools (e.g. REA + Ghidra):
jc-agent mcp add
jc-agent mcp test rea
```

### 5. 🔐 Linux OS Keyring Native
`jc-agent` stores your precious API keys directly in the **Linux OS Keyring** (`libsecret` / Secret Service / kernel keyring). Your keys are never written to disk in plaintext, never leaked into git, and never stored in dotfiles.

### 6. 🎨 High-Contrast Minimalist Dark & Coral TUI
Designed for Omarchy and Arch Linux terminal aesthetics:
- High-contrast obsidian dark palette (`#0F0F12`) with vibrant coral borders (`#FF6B6B`).
- Non-blocking Tokio worker thread: UI stays buttery smooth even when waiting on 30-second model generations or heavy Ghidra decompilation passes.
- Live token accounting: Prompt tokens, completion tokens, and session totals rendered live in the status bar.
- Live Server-Sent Events (SSE) streaming with graceful JSON fallback.

---

## 🏁 Quickstart

### 📦 Build & Run(CONTACT FOR ACCESS!)
```bash
# Clone the repository
git clone https://github.com/your-username/jc-agent.git
cd jc-agent

# Build optimized release binary
cargo build --release

# Run the interactive model wizard (takes 30 seconds)
./target/release/jc-agent model add

# Launch the TUI chat!
./target/release/jc-agent chat
```
### 🌐 WEB BASED GUI APPLICATION(COMING SOON!)

*(Prefer a plain UNIX stdout/stdin REPL for scripting or minimal shells? Just run `jc-agent chat --plain`!)*

### ⌨️ TUI Keyboard Shortcuts Cheat Sheet

| Shortcut | Action |
| :---: | :--- |
| **`F2`** | Cycle immediately to the next configured model |
| **`Ctrl+M`** / **`Alt+M`** | Open Model Switcher Modal (Up/Down or j/k to select, Enter to confirm) |
| **`Ctrl+T`** | Open Scoped Tool Profile Modal (`All` ⇄ `RE / Ghidra` ⇄ `ChatOnly`) |
| **`Y` / `N` / `A`** | Inline tool approval: **[Y]**es once, **[N]**o deny, **[A]**lways allow |
| **`Shift+Enter`** | Insert newline in multi-line prompt |
| **`Enter`** | Submit prompt |
| **`Up` / `Down`** | Scroll conversation transcript |
| **`PgUp` / `PgDn`** | Scroll transcript by page |
| **`Ctrl+L`** | Clear transcript and reset agent conversation memory |
| **`Ctrl+C`** / **`Esc`** | Clean, panic-safe terminal teardown & exit |

---

## 🗺️ What's Next? (The Roadmap)

We believe high-performance AI tools should belong to engineers, not closed corporations charging $40/month rent.

- **✅ Phase 1 & 2 (Complete & Verified)**: Rock-solid Rust engine, SQLite metadata, OS Keyring, stdio MCP hub, Ratatui TUI, live SSE streaming, scoped profiles, single-hotkey model switching.
- **🔄 Phase 3 (Active)**: Reboot-proof Secret Service keyring upgrade, custom skills & system prompts (`jc-agent skill`), persistent chat sessions (`--resume`), and rate-limit auto-failover.
- **🔮 Future Phase A — Lightweight VS Code Extension**: Exposing `jc-agent` as a local Unix socket daemon (`~/.run/jc-agent.sock`) with a thin TypeScript extension. Zero extra memory footprint, sharing the exact same models, keyring, and MCP hub!
- **🔮 Future Phase B — Standalone GUI Desktop App**: Making native, blazing-fast GUI tools powered by the exact same Rust core **at virtually zero cost for the community**.

---

## 💼 The Startup Vision & Investors

> *"The future of AI engineering isn't a bloated, proprietary browser masquerading as an IDE. It's modular, sovereign, hyper-fast infrastructure that respects the developer's privacy, keys, and workflow."*

We are actively developing `jc-agent` into a premier developer workstation and security analysis platform. With zero-rent economics, native Linux/Rust performance, persistent multi-tool protocol support, and uncensored enterprise-grade model switching, we are building the tool that hackers, reverse engineers, and top-tier developers actually want to live in.

Interested in early design partnership, commercial deployments, venture funding, or hiring?
- **Founder & Lead Architect**: **Ashim** ([ashim.dev](https://ashim.dev) | [@MaitohAshimHu](https://github.com/MaitohAshimHu))
- **Direct Connect**: [WhatsApp (+91 6204312017)](https://wa.me/916204312017) | [ashim.dev.sec@gmail.com](mailto:ashim.dev.sec@gmail.com)
- **Professional & Socials**: [LinkedIn](https://linkedin.com/in/bharydangerous) | [Instagram (@bharydangerous)](https://instagram.com/bharydangerous)

---

<div align="center">

**Built with 🦀 Rust, passion, and uncompromising terminal ergonomics.**  
*© 2026 jc-agent team. All rights reserved.*

</div>
