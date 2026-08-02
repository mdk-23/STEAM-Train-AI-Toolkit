# STEAM Train AI Career Toolkit

AI assistant skills for graduates and students of STEAM Train's Fast Track Academy (FTA). Each skill turns a general-purpose AI chat platform (Claude, ChatGPT, Microsoft Copilot, or Google Gemini) into a focused career coach for entry-level IT job seekers in Connecticut.

Developed by UConn MSBAPM Capstone Team 3 in partnership with STEAM Train, Inc. (Summer 2026). The guidance inside each skill is grounded in the team's analysis of Connecticut IT-support job postings and FTA program outcomes.

## The three skills

| Skill | Full version | Lite version | What it does |
|---|---|---|---|
| Job Search | `job-search/SKILL.md` | `lite/job-search-lite.md` | Recommends job titles, evaluates pasted postings, applies the "60% rule" against degree inflation, builds a weekly search routine |
| Resume Builder | `resume-builder/SKILL.md` | `lite/resume-builder-lite.md` | Interviews the user about their real history, translates non-IT experience into IT-framed resume bullets, tailors to postings, with strict no-fabrication guardrails |
| Interview Prep | `interview-prep/SKILL.md` | `lite/interview-prep-lite.md` | Runs mock interviews one question at a time, coaches the STAR method, reviews Tier 1 technical questions, debriefs real interviews |

Every file is fully self-contained. Use the **full version** whenever the platform allows it; use the **lite version** only where message length is limited (see table below). The lite versions keep the same workflows and ethics rules but drop the detailed statistics and examples.

**A note on the file format:** each full SKILL.md starts with a short metadata block between two `---` lines. Claude uses that block to decide when to activate the skill. Every other platform should receive only the **body**: everything below the second `---`. The lite files have no metadata block; paste them whole.

## Which version on which platform

| Platform | Version to use | Why |
|---|---|---|
| Claude (paid plans, installed as a Skill) | Full file, including metadata | Native skill support |
| Claude (any plan, pasted into chat) | Full body | Long pastes supported |
| ChatGPT Custom GPT (Plus plan) | Full body | Fits the 8,000-character instruction limit |
| ChatGPT free (pasted into chat) | Full body | Long pastes supported |
| Google Gemini (Gem or pasted) | Full body | Long pastes supported |
| Microsoft Copilot, signed in / M365 | Full body | Long pastes supported |
| Microsoft Copilot, free or not signed in | **Lite** | Free Copilot limits message length; full versions may be cut off |

If any platform truncates a paste or the assistant behaves as if it only saw part of the instructions, switch to the lite version.

## Setup instructions

**Claude (claude.ai):** On paid plans, go to Settings, then Capabilities, then Skills, and upload the SKILL.md file. Claude will use it automatically when relevant. On any plan, you can instead paste the skill body into a new chat and say "Act according to these instructions."

**ChatGPT:** With Plus, create a Custom GPT (Explore GPTs, then Create) and paste the skill body into the Instructions field; name it (for example "FTA Resume Builder") and share the link with students. On the free plan, paste the skill body into a new chat and say "Follow these instructions for this conversation."

**Google Gemini:** Create a Gem (Gem manager, then New Gem), paste the skill body into the instructions, save, and share. Or paste the body into a new chat with "Follow these instructions for this conversation."

**Microsoft Copilot:** Paste the appropriate version (see table) into a new chat and say "Follow these instructions for this conversation." Organizations with Copilot Studio can create a dedicated agent and paste the skill body into its instructions.

**Tip for students:** start a fresh chat for each session. In very long conversations any AI can drift from its instructions; each skill includes a reset phrase ("reset to coach mode" or "reset to interviewer mode") that tells the assistant to return to the rules.

## Keeping the toolkit current

The full skills cite Connecticut labor market statistics from a 2026 posting analysis. These numbers will drift, so refresh them about once a year:

1. Pull a current sample of CT IT-support postings (CareerOneStop's free API, Indeed, or CTHires).
2. Recount the share of postings mentioning each skill and certification.
3. Find the block marked `UPDATE ANNUALLY` in each full SKILL.md. It is word-for-word identical in all three files. Update the figures **in all three files** and change the "Last updated" date.
4. The lite versions name only two findings (top skills and top certification) without percentages; update them only if those findings change direction.

Everything else (workflows, guardrails, question banks) is evergreen.

## For maintainers

- Keep the no-fabrication guardrails intact in any edit. They are the toolkit's ethical core.
- If STEAM Train adds career pathways beyond IT support, the skills already instruct the AI to adapt its methods and flag that the statistics were IT-support specific; a fuller update would add a data block for the new pathway.
- If editing the full versions for Custom GPT use, keep each body under 8,000 characters (the current versions leave headroom).
- Questions about the original analysis can be directed to the UConn Digital Frontiers Initiative MSBAPM capstone program.

## License

Copyright STEAM Train, Inc. Released for use by STEAM Train staff, students, and program graduates.
