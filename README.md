# Self-Evaluating Shakespearean X Post Generator (CrewAI)

This project uses CrewAI with a self-evaluation loop to create and refine humorous, Shakespearean-style X posts (tweets) on a given topic, adhering to rules like character limits and structure.

## Overview

Two agents collaborate:

1.  **Shakespearean Bard:** Generates and refines the X post.
2.  **X Post Verifier:** Evaluates the post against criteria (length, emojis, 1-3-1 structure: 1 bold statement, 3 supporting lines, 1 summary) and provides feedback.

The Bard creates a post, the Verifier checks it, and if invalid, the feedback loops back to the Bard for revisions. This repeats until valid or the maximum retry count is reached.

## Example Iteration (Shortened)

**Iteration 1:**

Bard: `Oh, flying cars! A wondrous feat...`
Verifier: `{"valid": false, "feedback": "Lacks bold statement, supporting lines, and summary."}`

**Iteration 2:**

Bard: `O, flying cars, a grand jest indeed!...`
Verifier: `{"valid": false, "feedback": "Exceeds 280 characters."}`

**Final Attempt (Max Retries):**

Bard: `Lo, flying cars, a delight most rare!...`
Verifier's last feedback: `The post contains unnecessary commentary and employs archaic language that detracts from clarity...`

The loop refines the post based on feedback. The final output shows the post and the *last* feedback, even after maximum retries.

## Key Features

*   Self-evaluation and iterative improvement.
*   Uses CrewAI for agent collaboration.
*   Generates Shakespearean-style text.
*   Enforces content rules (length, no emojis, structure).
*   Provides actionable feedback.
*   Retry mechanism.

## Installation and Usage
(Instructions to install (e.g., `pip install crewai`) and run the code would go here, including API key setup if needed.)

## Future Improvements

*   Better error handling.
*   Dynamic difficulty adjustment.
*   Improved contextual awareness (avoid repeating mistakes).
*   Multiple topics.
* Refined Shakespearean language model.
