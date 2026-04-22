# Prompt to Professional Slides

Automate the creation of high-impact, **Gemini Enterprise** branded PowerPoint slides directly from text prompts, research notes, or strategy documents.

This repository contains a specialized skill for the [Gemini CLI](https://github.com/google-gemini/gemini-cli) that transforms natural language into editable `.pptx` files.

## ✨ Features

- **Gemini Enterprise Aesthetic:** Deep charcoal backgrounds (`#131314`), rounded "Bento Box" cards, and signature blue-to-pink gradients.
- **Google Sans Typography:** Optimized for high-end professional presentations.
- **Fully Editable:** Generates standard PowerPoint files with editable shapes and text boxes.
- **Automated Layout:** Intelligently parses your points into a structured, visual-first slide.
- **Sales Operations Architect:** A sophisticated multi-slide engine that maps 5 customer parameters to a customized 5-slide pitch deck.

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
- *"Generate a 5-slide seller deck for a Retail client in Marketing looking at Vertex AI."*
- *"Turn these 3 points into a professional slide: [Points]*"

### Example Workflow

**Prompt:** 
> "Make a Gemini Enterprise slide about our AI strategy: 1. 83% need infra upgrades, 2. 4/5 cite security as a barrier, 3. 52% use hybrid cloud."

**Result:**
Generates an editable `strategy_slide.pptx` in your current directory with a modern bento-box layout and bold statistics.

## 🎨 Fun Example: The AI-Powered Taco Shop

Here is a look at how the skill handles creative prompts:

**Prompt:**
> "Create a Gemini Enterprise slide for 'Taco-Bot 9000: The Future of Fast Casual'. Points: 1. 4.2M flavors with Generative Salsa, 2. 12s fulfillment with Agentic Assembly, 3. 0% waste using Predictive Guac."

**Resulting Slide Structure:**
- **Headline:** Taco-Bot 9000: The Future of Fast Casual
- **Card 1 (4.2M):** *Generative Salsa* — ML-optimized spice levels tailored to every palate.
- **Card 2 (12s):** *Agentic Assembly* — Autonomous precision for the perfect taco every time.
- **Card 3 (0%):** *Predictive Guac* — BigQuery-driven ripening forecasts to eliminate waste.

## 📁 Repository Structure

- `SKILL.md`: The instruction set and triggers for the Gemini CLI agent.
- `scripts/generate_slide.py`: The Python automation engine that builds the `.pptx` files.

---
*Created for the Gemini Enterprise ecosystem.*
