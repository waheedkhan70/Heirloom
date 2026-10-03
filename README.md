# Heirloom AI — Grandpa's Voice-to-Recipe & Family Memoir Archiver

## What I Built

### Heirloom AI — A Sovereign Family Recipe & Memoir Archiver Built for a Friend

I built **Heirloom AI** for my 82-year-old grandfather, **Nonno Matteo**, and my roommate, **Leo**, who suffers from severe Celiac disease and tree nut allergies.

The problem wasn't that our family didn't have recipes.

The problem was that our recipes weren't in books or apps—they were stored entirely inside an elderly man's memories.

Nonno doesn't type on keyboards or navigate smartphone apps. When asked how to make his legendary Sunday braised short rib sugo or holiday olive oil polenta cake, he records 10-minute stream-of-consciousness audio memos:
* An important ingredient measurement is mentioned 8 minutes after it was put into the pot.
* A crucial culinary technique is mixed with childhood stories from Calabria in 1954.
* Heated arguments about how modern canned tomatoes are too acidic interrupt the cooking steps.
* Crucial steps are unwritten: *"You know when it's done when the meat gives up when you look at it."*

At the same time, when we bring friends and roommates together for Sunday dinners, Leo's severe Celiac disease and nut allergies made traditional family meals terrifying. Nonno always forgot which ingredients contained hidden gluten or tree nuts.

So I built **Heirloom AI**—a local, open-source AI assistant that turns rambling family voice memos into a **searchable, structured heirloom cookbook ledger** while actively auditing recipes for roommate dietary safety.

You can record Grandpa speaking naturally or drop in raw audio:

> "Hey son, back in 1954 in Calabria, we browned the short ribs bone-in until dark like oak... Oh, did I tell you about cousin Gianni's wedding? No wait, toast the tomato paste in the beef fat for 3 minutes first, that kills the sourness!"

Heirloom AI processes the voice memo, executes a **Dual-Disentanglement Pipeline**, extracts the structured culinary blueprint, preserves the nostalgic lore in a dedicated memoir card, and automatically suggests verified allergen substitutions for roommates.

---

## How I Built It

Heirloom AI is built around **open-source AI, local client-side processing, and private inference**.

The architecture looks like this:

```text
                ┌──────────────────────────────────────┐
                │          Grandpa's Voice             │
                │   Live Mic / Audio Memo / Transcript │
                └──────────────────┬───────────────────┘
                                   │
                                   ▼
                ┌──────────────────────────────────────┐
                │        Open-Source AI Layer          │
                │                                      │
                │  Local Ollama (Gemma 2 / Llama 3.2)  │
                │   + Web Audio API & In-Browser NLP   │
                └──────────────────┬───────────────────┘
                                   │
                                   ▼
                ┌──────────────────────────────────────┐
                │     Dual-Disentanglement Engine      │
                │                                      │
                │   Emotional Lore  │  Culinary Blueprint│
                │   • 1954 Calabria │  • Metric Scaling │
                │   • Secret Rules  │  • Phase Timelines│
                └──────────┬───────────────────┬───────┘
                           │                   │
                           ▼                   ▼
                ┌──────────────────┐   ┌───────────────┐
                │ Heirloom Memoir  │   │   SafeBite    │
                │ Keepsake Lore &  │   │ Roommate Celiac│
                │ Wine Pairing     │   │ & Allergy Guard│
                └──────────┬───────┘   └───────┬───────┘
                           │                   │
                           └─────────┬─────────┘
                                     │
                                     ▼
                ┌──────────────────────────────────────┐
                │        Family Kitchen Ledger         │
                │                                      │
                │    Printable Card • Dynamic Servings │
                │    Offline LocalStorage Vault • .md  │
                └──────────────────────────────────────┘
```

### Technology Stack

**Frontend & Client Architecture**
* **Core:** Semantic HTML5, Vanilla Modern CSS with Custom Design Tokens.
* **Audio Studio:** Web Audio API (`AnalyserNode` for live frequency oscilloscope canvas), `MediaRecorder` for microphone capture, and HTML5 Web Speech recognition.
* **Print Studio:** Dedicated `@media print` styling that transforms digital recipe cards into elegant, physical physical keepsake index cards with zero UI chrome.

**Open AI & Inference Layer**
* **Local Daemon:** Ollama (`http://localhost:11434`) running open-weight models (**Gemma 2**, **Llama 3.2**, **Mistral**, **Phi-3**) with automatic local model detection.
* **Zero-Latency In-Browser Engine:** Client-side rule-based and semantic heuristic parser that works instantaneously without network requests or large downloads.
* **Dual-Disentanglement Prompt Harness:** Custom prompt schema designed to separate emotional narrative lore from structured, reproducible culinary metrics.

**Dietary Safety & Math Engine ("SafeBite")**
* Dynamic portion scaler ($1\times \to 12\times$) with automatic culinary fraction formatting (`1 1/2`, `2 1/4`).
* Instant Imperial (cups, lbs, oz, °F) $\longleftrightarrow$ Metric (grams, ml, kg, °C) unit conversion.
* Real-time allergen tagging (Gluten/Celiac, Tree Nuts, Peanuts, Dairy, Soy, Nightshades) with verified culinary substitutions (e.g., bronze-die brown rice rigatoni, creamy polenta, coconut aminos, seed flours).

**Persistence & Archival**
* 100% offline browser `localStorage` ledger vault.
* One-click JSON database export and import backup.
* One-click Markdown (`.md`) export for Notion, Obsidian, and family wikis.

---

## Why Does Open Innovation Matter?

For a tool built around elderly loved ones and family heritage, **privacy is not an optional feature—it is the entire foundation**.

Heirloom AI handles deeply personal and intimate data:
* Unreleased 70-year-old family secret recipes.
* Voice recordings of aging relatives sharing childhood memories and stories of deceased loved ones.
* Private family health and dietary vulnerabilities.

When I first showed Nonno commercial AI options, he refused:
> *"Non voglio che queste corporazioni vendano le ricette di mia madre!"*  
> *(“I don’t want these corporations selling my mother’s recipes!”)*

### 1. Zero Cloud Surveillance & Absolute Data Sovereignty
With open-weight models running locally through Ollama or client-side scripts, **not a single audio byte or word of text ever touches a corporate server**. The data stays on the family laptop.

### 2. Off-Grid Cabin Resilience
Grandparents often live in rural towns, mountain cabins, or areas with spotty Wi-Fi. Heirloom AI was built to run completely offline: you can take your laptop into an off-grid kitchen with no internet, plug in a microphone, and preserve family recipes with zero network connection.

### 3. $0 Marginal Cost & Multi-Generational Longevity
Commercial AI APIs charge per token, deprecate models every six months, and lock your history behind subscription paywalls. Open innovation ensures that this family ledger will run 10, 20, or 50 years from now exactly as it does today, at zero recurring cost.

### 4. Deterministic Dual-Disentanglement
Closed commercial chat interfaces either sanitize recipes into sterile, lifeless bullet points or leave the rambling story so tangled that cooking from it is impossible. Open weights gave me complete freedom to craft a dual-pipeline harness that preserves the soul of the memory while organizing the culinary science.

---

## My Agent Session

Development was tracked and orchestrated using an agentic pair-programming workflow:
* Rapid architectural prototyping of the dual-pane alchemist layout.
* Audio visualization integration using Web Audio API canvas contexts.
* Dynamic culinary calculation logic and verified allergen substitution mapping.
* Full print-ready stylesheet engineering for physical keepsake generation.

---

## Prize Categories

### Best Use of Gemma / Open-Weight Models
Heirloom AI relies on open-weight LLMs (like **Gemma 2** and **Llama 3.2**) as core reasoning engines rather than a cosmetic chatbot wrapper:
* Parsing unstructured spoken dialects, colloquial expressions, and stream-of-consciousness kitchen ramblings.
* Extracting temporal culinary phases, heat levels, and implicit unstated steps (like sweating onions until translucent).
* Isolating historical biographical narratives into keepsake quotes.
* Cross-referencing dietary safety databases to protect friends with Celiac disease.

---

## Built for One Person

The most important part of this project isn't the code.

It's the people I built it for.

I didn't start with:
> *"What AI hype project should I build?"*

I started with:
> **"How do I save my 82-year-old grandfather's life recipes before they are lost forever, while keeping my roommate Leo safe from allergic reactions at our dinner table?"**

Nonno Matteo already had an old voice recorder. Leo already had allergy cards. Our family already had recipe notebooks with missing pages.

What was missing was a private, respectful bridge that turns spoken love and culinary wisdom into a lasting family heirloom.

### What Nonno Said When We Handed Him the Laptop:
We sat down at his kitchen table, loaded his 1954 Sunday Gravy recording, and hit Extract. Within seconds, his voice transformed into an artisanal cookbook card with his childhood story quoted on top, his golden rule about toasting tomato paste highlighted, and a safe gluten-free pasta swap for Leo.

Nonno took off his glasses, looked closely at the screen, and smiled:
> *"Guarda! It actually listened. It remembered that you have to toast the tomato paste in the beef fat to kill the acidity. And you're sure nothing went into the internet? Good. That is how our family secrets stay safe."*
