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

# Sales Operations Architect Mode

This advanced mode automates the creation of a full seller pitch deck by mapping 5 key parameters to a Master Asset Library.

## Parameters
1. **Industry** (e.g., Retail, HCLS, FSI)
2. **Line of Business (LoB)** (e.g., Marketing, Ops, HR, IT)
3. **Primary Concern** (e.g., Cost, Innovation, Security)
4. **Current/Target Technology** (e.g., BigQuery, Vertex AI, GKE)
5. **Preferred Incentives** (e.g., POC, Credits, TCO Study)

## Workflow
1. **Input Collection:** Gather the 5 parameters from the user.
2. **Logic & Matching:** Map inputs to the `assets/mapping_schema.json` and `assets/master_content.json`.
3. **Deck Assembly:** Use `scripts/generate_deck.py` to assemble a 5-slide deck:
   - Slide 1: Intro/Title
   - Slide 2: Industry Context
   - Slide 3: Tech/Solution Deep-Dive
   - Slide 4: LoB Business Value
   - Slide 5: Commercial Incentive/Next Steps
4. **Constraint:** Default to "Horizontal Value" slides if a parameter is missing or "Don't Know".

## Usage Example
Input: "Generate a seller deck for a Retail client. The LoB is Marketing, they care about Personalization, and we want to pitch Vertex AI with a POC incentive."

Action:
- Call `scripts/generate_deck.py` with the mapped JSON parameters.

## Usage Example

Input: "Make a slide about our AI strategy: 1. 83% need infra upgrades, 2. 4/5 cite security as a barrier, 3. 52% use hybrid cloud."

Action:
- Headline: "AI Strategy: Infrastructure & Security"
- Points:
  - {stat: "83%", title: "Infra Upgrades", body: "Organizations require upgrades for production AI."}
  - ...
- Run: `python3 scripts/generate_slide.py '[JSON_DATA]'`
