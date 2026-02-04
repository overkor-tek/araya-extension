# ARAYA Memory Cargo Plane

**AI-powered browser extension for the Consciousness Revolution platform.**

ARAYA rides alongside you as you browse, capturing context, detecting workflows, and carrying your projects seamlessly between AI platforms. She connects your browser to the Consciousness Revolution brain -- organizing everything you encounter into 7 life domains.

---

## What It Does

- **7 Domain Organization** -- Right-click anything on the web and file it into one of 7 life domains: Command, Build, Connect, Protect, Grow, Learn, or Transcend.
- **AI Platform Detection** -- Automatically detects when you are on ChatGPT, Claude, Gemini, DeepSeek, Perplexity, Grok, or Copilot. Tracks your usage and warns you before hitting free-tier limits.
- **Memory Cargo System** -- Captures entire AI conversations as compact "memory packets" and carries them to the next AI. One click to hop from ChatGPT to Claude with full project context intact.
- **Workflow Detection** -- Recognizes what you are doing (banking, legal research, learning) and suggests the right domain to file it under.
- **Page Observer** -- Extracts page metadata, text, links, and images from any webpage on demand.
- **Side Panel Interface** -- A persistent lobby panel with all 7 domains accessible without leaving your current tab.
- **Consciousness Revolution Bridge** -- Sends captured data to the platform API at conciousnessrevolution.io for AI-powered analysis.

---

## Features

| Feature | Description |
|---------|-------------|
| **Side Panel Lobby** | Navigate your 7 life domains from a persistent side panel |
| **Context Menu Save** | Right-click text, links, images, or pages to save to any domain |
| **AI Round-Robin** | Track free-tier usage across 7 AI platforms, auto-suggest the next one |
| **Conversation Capture** | Package an entire AI conversation into a portable memory packet |
| **AI Hop** | One-click context transfer between AI platforms with auto-injection |
| **Workflow Detection** | Auto-detect finance, legal, and learning workflows from URLs |
| **Page Data Extraction** | Pull structured data (text, links, images, metadata) from any page |
| **Floating Cargo Bar** | Minimal UI overlay on AI platforms showing usage and quick actions |
| **Glass Window Components** | Modular component system for extensible domain interfaces |
| **Music Sanctuary** | Dedicated consciousness-focused audio environment in the Transcend domain |

---

## Permissions

| Permission | Why |
|------------|-----|
| `activeTab` | Read the current tab's URL and content when you interact with the extension |
| `storage` | Save your preferences, captured memory packets, and usage tracking locally |
| `sidePanel` | Display the 7 Domains lobby as a persistent side panel |
| `tabs` | Detect tab changes for workflow recognition and AI platform switching |
| `contextMenus` | Add "Save to Araya" right-click menu with domain submenus |
| `<all_urls>` (host) | Content scripts run on all pages to enable page observation and AI detection |

---

## Installation

### Brave Browser (recommended)

1. Open Brave and navigate to `brave://extensions/`
2. Enable **Developer mode** (toggle in the top-right corner)
3. Click **Load unpacked**
4. Select this folder (`araya-extension/`)
5. Click **Select Folder**

### Google Chrome

1. Open Chrome and navigate to `chrome://extensions/`
2. Enable **Developer mode** (toggle in the top-right corner)
3. Click **Load unpacked**
4. Select this folder (`araya-extension/`)
5. Click **Select Folder**

### Microsoft Edge

1. Open Edge and navigate to `edge://extensions/`
2. Enable **Developer mode** (toggle in the left sidebar)
3. Click **Load unpacked**
4. Select this folder (`araya-extension/`)
5. Click **Select Folder**

After loading, the ARAYA icon appears in your toolbar. Click it for the popup, or it will automatically open the side panel.

---

## Usage

**Side Panel** -- Click the ARAYA icon in the toolbar to open the 7 Domains lobby as a side panel.

**Quick Save** -- Click the extension icon and hit "Save This Page" to file the current page to the Learn domain.

**Context Menu** -- Right-click on any text selection, link, image, or page and choose "Save to Araya" followed by the target domain.

**AI Cargo Bar** -- When you visit any supported AI platform (ChatGPT, Claude, Gemini, etc.), a floating bar appears at the bottom showing your message count and quick actions:
- **Capture** -- Save the current conversation as a memory packet
- **Next AI** -- Hop to the AI with the most remaining free-tier capacity, carrying your project context

---

## Project Structure

```
araya-extension/
  manifest.json              Manifest V3 extension config
  background/
    service_worker.js        Context menus, workflow detection, API bridge
  content/
    observer.js              Page data extraction, form watching
    ai-detector.js           AI platform detection, cargo bar, round-robin
  popup/
    popup.html               Quick-access popup (7 Domains, Save, Chat)
  sidepanel/
    lobby.html               Main side panel interface
    lobby.js                 Side panel logic
    domains/
      7_transcend.html       Transcend domain view
  domains/
    7_transcend/
      music-sanctuary.html   Consciousness music environment
  glass-window/
    glass-window.html        Modular component renderer
    component-registry.json  Registered UI components
  icons/
    araya-16.png             Toolbar icon (16x16)
    araya-48.png             Extension page icon (48x48)
    araya-128.png            Store icon (128x128)
    araya-128.svg            Vector source
```

---

## Screenshots

_Screenshots coming soon._

---

## Supported AI Platforms

| Platform | Detection | Conversation Reading | Context Injection |
|----------|-----------|---------------------|-------------------|
| ChatGPT | Yes | Yes | Yes |
| Claude | Yes | Yes | Yes |
| Gemini | Yes | Yes | Yes |
| DeepSeek | Yes | Yes | Yes |
| Perplexity | Yes | Yes | Yes |
| Grok | Yes | Yes | Yes |
| Copilot | Yes | Yes | Yes |

---

## Platform

This extension connects to the **Consciousness Revolution** platform:

https://conciousnessrevolution.io

---

## Contributing

Contributions are welcome. For the main platform codebase and broader system:

- Main repo: [github.com/overkillkulture/consciousness-revolution](https://github.com/overkillkulture/consciousness-revolution)
- File bugs: [conciousnessrevolution.io/bugs.html](https://conciousnessrevolution.io/bugs.html)
- Contact: darrickpreble@proton.me

---

## Technical Details

- **Manifest Version:** 3 (latest Chrome extension standard)
- **Extension Version:** 1.0.0
- **Service Worker:** Persistent background with module support
- **Content Scripts:** Run at `document_idle` on all URLs
- **Storage:** Chrome local storage for packets and usage data
- **API Endpoint:** `conciousnessrevolution.io/.netlify/functions/araya-chat`

---

## License

MIT License

Copyright (c) 2026 Consciousness Revolution

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
