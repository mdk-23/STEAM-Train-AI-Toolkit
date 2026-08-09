# STEAM Train AI Career Toolkit

AI assistant skills for graduates and students of STEAM Train's Fast Track Academy (FTA). Each skill turns a general-purpose AI chat platform (Claude, ChatGPT, Microsoft Copilot, or Google Gemini) into a focused career coach for entry-level IT job seekers in Connecticut.

Developed by UConn MSBAPM Capstone Team 3 in partnership with STEAM Train, Inc. (Summer 2026). The guidance inside each skill is grounded in the team's analysis of Connecticut IT-support job postings and FTA program outcomes.

**Platform details in this README were verified in August 2026.** AI vendors change their free tiers, model access, and message limits frequently. Where a platform detail matters to you, confirm it before relying on it; the "Verifying the toolkit still works" section below gives a one-minute test.

## The three skills

| Skill | Full version | Lite version | What it does |
|---|---|---|---|
| Job Search | `job-search/SKILL.md` | `lite/job-search-lite.md` | Actively searches for and suggests current openings, evaluates postings, applies the "60% rule" against degree inflation, keeps the search organized |
| Resume Builder | `resume-builder/SKILL.md` | `lite/resume-builder-lite.md` | Interviews the user about their real history, translates non-IT experience into IT-framed resume bullets, tailors to postings, with strict no-fabrication guardrails |
| Interview Prep | `interview-prep/SKILL.md` | `lite/interview-prep-lite.md` | Runs mock interviews one question at a time, coaches the STAR method, reviews Tier 1 technical questions, debriefs real interviews |

Every file is fully self-contained. Use the **full version** whenever the platform allows it; use the **lite version** only where message length is limited (see table below). The lite versions keep the same workflows and ethics rules but drop the detailed statistics and examples.

**A note on the file format:** each full SKILL.md starts with a short metadata block between two `---` lines. Claude uses that block to decide when to activate the skill. Every other platform should receive only the **body**: everything below the second `---`. The lite files have no metadata block; paste them whole.

## Which version on which platform

| Platform | Version to use | Why |
|---|---|---|
| Claude (any plan, including Free, installed as a Skill) | Full file, including metadata | Native skill support; requires code execution to be enabled |
| Claude (any plan, pasted into chat) | Full body | Long pastes supported |
| ChatGPT Custom GPT (built on Plus or higher) | Full body | Fits the 8,000-character instruction limit, but see the budget warning below |
| ChatGPT free (pasted into chat) | Full body | Long pastes supported |
| Google Gemini (Gem or pasted, any plan including Free) | Full body | Long pastes supported |
| Microsoft Copilot, signed in / M365 | Full body | Long pastes generally supported |
| Microsoft Copilot, free or not signed in | **Lite** | Copilot has enforced input limits as low as 2,000 to 8,000 characters at various times; full versions may be cut off |

Reported Copilot input limits have changed repeatedly and have differed between accounts and surfaces, so treat the Copilot rows as the least stable line in this table. If any platform truncates a paste, or the assistant behaves as if it only saw part of the instructions, switch to the lite version.

**A note on plan requirements:** the free tiers of these platforms cover more than they used to, and no student needs a paid subscription to use this toolkit.

- **Claude:** Skills can be installed on Free, Pro, Max, Team, and Enterprise plans. The feature depends on **code execution being enabled**, not on the plan. If the Skills menu is missing or greyed out, that setting is almost always the reason.
- **Google Gemini:** Gems are free on every Gemini plan. Gems can only be created and edited in the Gemini web app on a computer, not in the mobile app, but they can be shared by link and used on any device. Free accounts have lower usage limits, but the Gem itself works for them.
- **ChatGPT:** Building a Custom GPT requires Plus or higher. Students on the free plan can either use a Custom GPT that someone else built and shared, or simply paste the skill body into a normal chat, which works the same way.
- **Microsoft Copilot:** No paid plan is required to paste a skill into a chat.

**A note on the Job Search skill:** it works best where the AI can search the web, which current free tiers of ChatGPT, Gemini, and Copilot all support (make sure search or browsing is enabled in the chat). On Claude, students can additionally connect a job board connector such as Indeed (Customize, then Connectors), and the skill will query it directly for live postings. Connector availability on the Claude Free plan has changed recently and Anthropic's own documentation has not been fully consistent about it, so check whether the connector appears on the account in question rather than assuming. If a session has no search access, the skill detects this and falls back to coaching the student through searching manually. The skill instructs the AI never to present job listings from memory, but students should still verify any posting at the source before applying.

## Setup and use instructions

**Claude (claude.ai):** First go to Settings, then Capabilities, and turn on **Code execution and file creation**; the Skills menu will not appear without it. Then go to Customize, then Skills, click the "+" button, choose "Create skill," select "Upload a skill," and upload the ZIP for that skill. Claude will use it automatically when relevant. This works on Free, Pro, and Max plans. On any plan, you can instead paste the skill body into a new chat and say "Act according to these instructions."

**ChatGPT:** With Plus, create a Custom GPT (Explore GPTs, then Create) and paste the skill body into the Instructions field; name it (for example "FTA Resume Builder") and share the link with students. On the free plan, paste the skill body into a new chat and say "Follow these instructions for this conversation."

**Google Gemini:** On a computer, open the Gemini web app, go to Explore Gems, then New Gem, paste the skill body into the instructions, save, and share. Or paste the body into a new chat with "Follow these instructions for this conversation."

**Microsoft Copilot:** Paste the appropriate version (see table) into a new chat and say "Follow these instructions for this conversation." Organizations with Copilot Studio can create a dedicated agent and paste the skill body into its instructions.

**Tip for students:** start a fresh chat for each session. In very long conversations any AI can drift from its instructions; each skill includes a reset phrase ("reset to coach mode" or "reset to interviewer mode") that tells the assistant to return to the rules.

## Packaging skills for Claude upload

Claude expects a ZIP containing a **folder**, with `SKILL.md` inside that folder. The folder name must match the skill name declared in the metadata block at the top of the file:

```
fta-job-search/SKILL.md          -> zip as fta-job-search.zip
fta-resume-builder/SKILL.md      -> zip as fta-resume-builder.zip
fta-interview-prep/SKILL.md      -> zip as fta-interview-prep.zip
```

All three files are named `SKILL.md`, which is required, so they must stay in separate folders. Keeping them in one folder, or renaming them to something like `job-search-SKILL.md`, will break the upload or overwrite one file with another.

The most common upload failures are a folder name that does not match the skill name, a missing `SKILL.md`, and invalid characters in the skill name or description. If an upload is rejected, check those three things first.

## Keeping the toolkit current

The full skills cite Connecticut labor market statistics from a 2026 posting analysis. These numbers will drift, so refresh them about once a year:

1. Pull a current sample of CT IT-support postings (CareerOneStop's free API, Indeed, or CTHires).
2. Recount the share of postings mentioning each skill and certification.
3. Find the block marked `UPDATE ANNUALLY` in each full SKILL.md. It is word-for-word identical in all three files. Update the figures **in all three files** and change the "Last updated" date.
4. The lite versions name only two findings (top skills and top certification) without percentages; update them only if those findings change direction.
5. Re-check the character budgets below before saving, and run the verification test at the end of this README.

Everything else (workflows, guardrails, question banks) is evergreen.

## Character budget: STEAM TRAIN personnel read this before editing

ChatGPT Custom GPT instructions are capped at 8,000 characters. Two of the three skills are close to that ceiling, so edits must be roughly **net-neutral in length**: if you add a sentence, cut one of similar size.

| File | Body characters | Remaining before 8,000 |
|---|---|---|
| `job-search/SKILL.md` | ~7,300 | ~700 |
| `resume-builder/SKILL.md` | ~7,850 | ~150 |
| `interview-prep/SKILL.md` | ~7,900 | ~100 |

Resume Builder and Interview Prep have room for about one or two sentences each, not more. Adding a paragraph to either will push it over the limit, and ChatGPT will refuse to save the Custom GPT.

To recount after an edit, run this from the repository root. It counts the body only, excluding the metadata block:

```
for f in */SKILL.md; do
  echo "$f: $(awk 'BEGIN{n=0} /^---$/{n++; next} n>=2{print}' "$f" | wc -c) characters"
done
```

If a skill needs to grow past the limit, the cleanest fix is to trim examples rather than rules. The guardrails and workflows are what make the skill work; the illustrative examples are the compressible part.

## Verifying the toolkit still works

After any edit, and any time a platform behaves oddly, run this one-minute check on that platform:

1. Paste the skill body (or install the skill) as you normally would.
2. Send this message: **"Before we start, tell me the reset phrase and the last rule under Guardrails."**
3. A correct answer means the entire document arrived intact. A vague or wrong answer means the paste was truncated, and that platform needs the lite version.

For the Job Search skill, add one more check: ask it to find jobs, and confirm it either presents postings with working links it actually retrieved, or states plainly that it cannot search. An assistant that produces employers and salaries without searching has lost the anti-fabrication guardrail, and that version should not be given to students.

## For maintainers

- Keep the no-fabrication guardrails intact in any edit. They are the toolkit's ethical core.
- Keep edits net-neutral in length (see the character budget above).
- If STEAM Train adds career pathways beyond IT support, the skills already instruct the AI to adapt their methods and flag that the statistics were IT-support specific; a fuller update would add a data block for the new pathway.
- Platform tiers, model access, and message limits change often. When a plan detail in this README stops matching reality, correct it here so students are not sent to a setting that no longer exists.
- Questions about the original analysis can be directed to the UConn Digital Frontiers Initiative MSBAPM capstone program.

## License

Copyright STEAM Train, Inc. Released for use by STEAM Train staff, students, and program graduates.
