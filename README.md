# Prompt to Professional Slides

Automate the creation of high-impact, **Gemini Enterprise** branded PowerPoint slides directly from text prompts, research notes, or strategy documents.

This repository contains a specialized skill for the [Gemini CLI](https://github.com/google-gemini/gemini-cli) that transforms natural language into editable `.pptx` files.

## ✨ Features

- **Gemini Enterprise Aesthetic:** Deep charcoal backgrounds (`#131314`), rounded "Bento Box" cards, and signature blue-to-pink gradients.
- **Google Sans Typography:** Optimized for high-end professional presentations.
- **Fully Editable:** Generates standard PowerPoint files with editable shapes and text boxes.
- **Automated Layout:** Intelligently parses your points into a structured, visual-first slide.

## 🚀 Getting Started

### Prerequisites

To generate the PowerPoint files, you'll need the `python-pptx` library installed on your system:

```bash
python3 -m pip install python-pptx
```

### Installation

1. Clone this repository or link it as a skill in your Gemini CLI environment:
   ```bash
   gemini skills link /path/to/Prompt-to-Professional-Slides
   ```
2. Restart your Gemini CLI session or run `/skills reload`.

## 🛠 Usage

Simply trigger the skill in your Gemini CLI session using natural language:

- *"Create a Gemini Enterprise style slide about our AI roadmap."*
- *"Turn these 3 points into a professional slide: [Points]*"
- *"Make a Gemini Enterprise pitch deck about the benefits of Model Context Protocol."*

### Example Workflow

**Prompt:** 
> "Make a Gemini Enterprise slide about our AI strategy: 1. 83% need infra upgrades, 2. 4/5 cite security as a barrier, 3. 52% use hybrid cloud."

**Result:**
Generates an editable `strategy_slide.pptx` in your current directory with a modern bento-box layout and bold statistics.

## 📁 Repository Structure

- `SKILL.md`: The instruction set and triggers for the Gemini CLI agent.
- `scripts/generate_slide.py`: The Python automation engine that builds the `.pptx` files.

---
*Created for the Gemini Enterprise ecosystem.*
