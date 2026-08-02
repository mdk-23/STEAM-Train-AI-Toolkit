# STEAM-Train-AI-Toolkit
This repo hosts a collection of skills to be used with AI platforms like ChatGPT, Claude, Google Gemini, and Microsoft Copilot to help FTA students with job searching, resume building, and interview preparation.

# STEAM Train AI Career Toolkit

AI assistant skills for graduates and students of STEAM Train's Fast Track Academy (FTA). Each skill turns a general-purpose AI chat platform (Claude, ChatGPT, Microsoft Copilot, or Google Gemini) into a focused career coach for entry-level IT job seekers in Connecticut.

Developed by UConn MSBAPM Capstone Team 3 in partnership with STEAM Train, Inc. (Summer 2026). The guidance inside each skill is grounded in the team's analysis of Connecticut IT-support job postings and FTA program outcomes.

## The three skills

| Skill | File | What it does |
|---|---|---|
| Job Search | `job-search/SKILL.md` | Finds the right job titles to search, evaluates postings the user pastes in, applies the "60% rule" against degree inflation, and builds a sustainable weekly search routine |
| Resume Builder | `resume-builder/SKILL.md` | Interviews the user about their real history, translates non-IT experience into IT-framed resume bullets, and tailors resumes to specific postings, with strict no-fabrication guardrails |
| Interview Prep | `interview-prep/SKILL.md` | Runs realistic mock interviews one question at a time, coaches the STAR method, reviews Tier 1 technical questions, and debriefs real interviews |

Each file is fully self-contained. A student only needs the one skill relevant to their current task.

## How to use each skill, by platform

### Claude (claude.ai)
Paid plans support Skills directly: go to Settings, then Capabilities, then Skills, and upload the SKILL.md file (or the skill folder). Claude will automatically use it when relevant. On any plan, you can instead start a new chat, attach or paste the SKILL.md contents, and say "Act according to these instructions."

### ChatGPT (chat.openai.com)
Option A (best, requires Plus): create a Custom GPT. Go to Explore GPTs, then Create, and paste the full SKILL.md body (everything below the second `---`) into the Instructions field. Name it (for example "FTA Resume Builder") and share the link with students.
Option B (free): start a new chat, paste the SKILL.md contents, and say "Follow these instructions for this conversation."

### Microsoft Copilot
Start a new chat, paste the SKILL.md contents, and say "Follow these instructions for this conversation." Organizations with Copilot Studio can instead create a dedicated agent and paste the skill body into its instructions.

### Google Gemini
Option A: create a Gem (Gemini menu, then Gem manager, then New Gem) and paste the SKILL.md body into the instructions. Save and share.
Option B: paste the contents into a new chat and say "Follow these instructions for this conversation."

## Keeping the toolkit current

The skills cite Connecticut labor market statistics from a 2026 posting analysis (for example, which skills and certifications appear most often in IT-support postings). These numbers will drift. A once-a-year refresh is enough:

1. Pull a current sample of CT IT-support postings (CareerOneStop's free API, Indeed, or CTHires).
2. Recount the share of postings mentioning each skill and certification listed in the skills.
3. Edit the numbers in the three SKILL.md files and commit the change.

Everything else (workflows, guardrails, question banks) is evergreen.

## For maintainers

- Each SKILL.md uses YAML frontmatter (`name`, `description`) followed by a markdown instruction body. The frontmatter is what Claude uses to decide when to trigger the skill; the body is the actual instructions and is what you paste into other platforms.
- Keep the no-fabrication guardrails intact in any edit. They are the toolkit's ethical core.
- Questions about the original analysis can be directed to the UConn Digital Frontiers Initiative MSBAPM capstone program.

## License

Copyright STEAM Train, Inc. Released for use by STEAM Train staff, students, and program graduates.
