---
name: prompt-to-slide
description: Automates the creation of professional, Gemini Enterprise branded PowerPoint slides from text prompts, notes, or research. Use this skill whenever a user wants to "create a slide," "build a pitch deck," or "visualize strategy points" in an editable PPTX format.
---

# Prompt to Professional Slide

Create high-impact, editable PowerPoint slides using the Gemini Enterprise aesthetic.

## Triggering
- User says: "Turn these points into a slide"
- User says: "Create a Gemini Enterprise style pitch deck about [Topic]"
- User provides research and asks for a "visual summary" in PPTX.

## Core Principles
1. **Gemini Enterprise Aesthetic:** Deep charcoal backgrounds (`#131314`), rounded "Bento Box" cards, and blue-to-pink signature gradients.
2. **Typography:** Always use **Google Sans** (fallback to Arial if unavailable in the environment).
3. **Editability:** The output must be a standard `.pptx` file with editable shapes and text boxes.
4. **Data Focus:** Prioritize bold statistics and clear, concise headers.

## Workflow

1. **Extract Points:** Parse the user's prompt into:
   - A high-level **Headline**.
   - 3-4 key **Points** (each with a Title, Body text, and an optional Statistic).
2. **Execute Script:** Use the bundled `generate_slide.py` script to build the PPTX.
3. **Deliver:** Save the file to the user's home directory and inform them of the path.

## Usage Example

Input: "Make a slide about our AI strategy: 1. 83% need infra upgrades, 2. 4/5 cite security as a barrier, 3. 52% use hybrid cloud."

Action:
- Headline: "AI Strategy: Infrastructure & Security"
- Points:
  - {stat: "83%", title: "Infra Upgrades", body: "Organizations require upgrades for production AI."}
  - ...
- Run: `python3 scripts/generate_slide.py '[JSON_DATA]'`
