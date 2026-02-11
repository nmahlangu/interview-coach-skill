# Interview Coach - AI-Powered Interview Preparation

A Claude Skill that transforms Claude into a systematic interview coach informed by professional coaching methodology (ICF-aligned). Built from research with 30+ tech professionals on how they're using AI to land better jobs faster.

**Featured in:** [Lenny's Newsletter - "You should be using AI to land your next job"](LINK_TBD)

---

## What This Does

Instead of generic interview advice, this skill gives you:

* **Coaching-informed approach** — self-reflection before feedback, strengths-first delivery, co-created action plans. Claude holds you as resourceful and capable, not as someone to be fixed.
* **Slash commands** for instant access to any feature (`/prep`, `/analyze`, `/practice`, `/hype`, and more)
* **LinkedIn integration** that enriches your profile and analyzes your interviewers
* **Company-specific prep** with predicted questions, competitive positioning, and strategic counters
* **Transcript analysis** that scores directly across multiple dimensions (no sycophantic praise, but strengths recognized)
* **Practice drills**: constraint ladder, adversarial follow-ups, interruption handling, recovery tactics
* **Storybank management** to track, improve, and retire your interview stories
* **Differentiation coaching** to escape the "AI-polished middle" where everyone sounds the same
* **Mindset and inner game** — addresses anxiety patterns, limiting beliefs, and avoidance behaviors

---

## Quick Start (5 minutes)

### Option 1: Claude Pro ($20/month) - Recommended

1. Download the skill files from this repo (or clone it)
2. In Claude, create a new Project called "Interview Coach"
3. Go to Project Settings → Skills → Upload the skill files
4. Upload your resume to the project
5. Type: `/setup`

### Option 2: Claude Free

1. Copy the contents of `SKILL.md` from this repo
2. In Claude, create a new conversation
3. Paste the SKILL.md content at the start
4. Upload your resume
5. Type: `/setup`

*Note: Free tier won't retain context between conversations. You'll need to re-paste the skill each session.*

---

## Slash Commands

Type any of these commands at any time:

| Command | What it does |
|---------|--------------|
| `/setup` | Initial setup — gather resume, LinkedIn, target role, preferences |
| `/prep [company]` | Generate a 1-page prep brief for a specific company/role |
| `/analyze` | Score and analyze an interview transcript |
| `/practice` | Open the practice drill menu |
| `/stories` | Review or add to your storybank |
| `/hype` | Pre-interview confidence boost (60-second hype reel) |
| `/concerns` | Generate likely concerns about your background + counters |
| `/questions` | Generate smart questions to ask your interviewers |
| `/thankyou` | Draft a post-interview thank you note |
| `/progress` | Review your patterns and improvement areas |
| `/help` | Show all available commands |

---

## How to Use

### First Time Setup

Type `/setup`. Upload your resume and LinkedIn profile URL. Tell Claude your target role. That's it.

**Why LinkedIn?** It provides richer context than a resume alone—career narrative, endorsements, recommendations, and how you present yourself publicly.

### Before an Interview

```
/prep Stripe
```

Then share the job description. Claude generates:

* What they optimize for (based on JD + values)
* Your unique positioning
* 7-10 predicted questions
* Concerns about your background + how to counter them
* Non-generic questions to ask them
* **Know Your Interviewer cards** (if you share interviewer LinkedIn profiles)

### After an Interview

```
/analyze
```

Paste your transcript (use [Granola](https://granola.ai), [Otter](https://otter.ai), or [Tactiq](https://tactiq.io) to capture interviews).

Claude analyzes from multiple perspectives:

* Hiring manager (would they advance you?)
* Skeptical specialist (where did you lack depth?)
* Values alignment (which principles did you miss?)
* Calibration (verbosity, hedging, jargon density)

You get a one-page "delta sheet" with exactly what to fix. **Expect harsh scores.** A 3/5 is average.

### Practice Mode

```
/practice
```

Options include:

* `/practice ladder` — Same story at 15s, 45s, 90s, 3min
* `/practice pushback` — Adversarial follow-ups to your stories
* `/practice role` — Deep pressure test for your function
* `/practice panel` — Mock panel with different interviewer types
* `/practice pivot` — Handle interruptions and topic shifts

### Pre-Interview Boost

```
/hype
```

Get a 60-second "hype reel" of your wins to read aloud, plus a 3x3 sheet (3 likely concerns + counters, 3 questions to ask).

### Manage Your Stories

```
/stories
```

View, add, improve, or retire stories in your storybank. Claude tracks which stories you've used, how they performed, and when to retire them.

---

## What's Included

```
interview-coach-skill/
├── SKILL.md                     # Core coaching instructions with slash commands
├── interview-coach.skill        # Skill manifest file
└── references/
    ├── rubrics-detailed.md      # Full 1-5 scoring scales
    ├── role-drills.md           # PM, Eng, Design, Data Science, Research, Ops, Marketing drills
    ├── differentiation.md       # Earned secrets, spiky POV, clarity under pressure
    ├── transcript-processing.md # How to clean, parse, and analyze transcripts
    └── storybank-guide.md       # Building and maintaining your story index
```

---

## Two Tracks: Quick Prep vs Full System

**Quick Prep** (~30 min per interview)

* Company prep brief
* Basic transcript scoring
* Key improvements to focus on

**Full System** (~2-3 hours initially, then compounds)

* Storybank with gap analysis
* Multi-lens scoring from 4 perspectives
* Pattern tracking across interviews
* Weekly reviews with trend analysis
* Differentiation coaching

Choose your track during `/setup`. You can upgrade later.

---

## Tips for Best Results

1. **Share your LinkedIn** — Richer context = better coaching
2. **Share interviewer profiles** — Get "Know Your Interviewer" cards with rapport builders and likely focus areas
3. **Use real transcripts** — Recording your interviews is the fastest way to improve
4. **Expect harsh feedback** — The skill defaults to critical. A 3/5 is average.
5. **Use slash commands** — They're faster than explaining what you want

---

## Frequently Asked Questions

**Q: Does this work for non-tech roles?**
A: The core coaching works for any role. The role-specific drills currently cover PM, Engineering, Design, Data Science, Research, Operations, and Marketing.

**Q: Can I use this with ChatGPT or Gemini?**
A: The skill is designed for Claude, but you can adapt the prompts. Copy relevant sections from SKILL.md into your preferred AI.

**Q: Why is the feedback so direct?**
A: Because sycophantic praise doesn't help you improve. The candidates who landed jobs in our research explicitly asked AI to be adversarial. That said, the skill leads with what's working before addressing gaps, and invites you to self-assess before receiving feedback — so the directness lands constructively.

**Q: Is it ethical to use AI for interview prep?**
A: Using AI to prepare is no different than using books, coaches, or mock interviews. The skill helps you articulate your real experiences better—it doesn't fabricate credentials.

---

## What's New in v3

* **Coaching-informed delivery** — Self-reflection before feedback, strengths-first structure, co-created action plans, powerful questions over prescriptions
* **Mindset layer** — Addresses anxiety, avoidance patterns, and limiting beliefs. Reframes interviews as conversations, not performances.
* **Adaptive pacing** — More directive when urgent, more reflective when there's time
* **Guided story exploration** — Reflective prompts surface richer stories than brainstorm lists
* **Accountability structures** — Session check-ins, commitment invitations, progress reflection

### Previously in v2

* **Slash commands** — Instant access to any feature
* **LinkedIn integration** — Richer candidate profiles, interviewer analysis
* **Know Your Interviewer cards** — Background overlap, likely focus areas, rapport builders
* **Practice sub-commands** — `/practice ladder`, `/practice pushback`, etc.
* **Storybank management** — `/stories` menu for viewing, adding, improving, retiring

---

## Contributing

Found a bug? Have a suggestion? Open an issue or PR.

---

## Credits

Created by [Noam Segal](https://www.linkedin.com/in/noamsegal/) based on research with 30+ tech professionals for [Lenny's Newsletter](https://www.lennysnewsletter.com/).

---

## License

MIT License - Use freely, attribution appreciated.
