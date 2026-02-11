# You should be using AI to land your next job

👋 Hey there, I'm Lenny. Each week, I answer reader questions about building product, driving growth, and accelerating your career. For more: Lenny's Podcast | How I AI | Lennybot | Lenny's Reads | Favorite AI and PM courses | Favorite public speaking course

P.S. Insider subscribers get a free year of Lovable, Manus, Replit, Gamma, n8n, Canva, ElevenLabs, Amp, Factory, Devin, Bolt, Wispr Flow, Linear, PostHog, Framer, Railway, Granola, Warp, Perplexity, Magic Patterns, Mobbin, ChatPRD, and Stripe Atlas. Yes, this is for real. Learn more.

---

Many of you have been asking how AI is changing the job market for tech roles.

To find out, my Community Research Lead, Noam Segal, interviewed dozens of candidates and hiring managers to learn how AI is transforming both sides of the hiring process.

Part 1 focuses on candidates. When Noam started analyzing what he learned, he realized the findings didn't compress into a tidy list of tips. The best candidates had built interconnected systems, workflows that adapted to their gaps and compounded over time. So he took a different approach: he encoded his research into a Claude Skill you can use yourself.

If you're on the job market and want to use AI to land your next role, this post is for you.

For more from Noam, find him on [**LinkedIn**](https://www.linkedin.com/in/noamsegal/).

P.S. You can listen to this post in convenient podcast form: **Spotify** / **Apple** / **YouTube**.

**tl;dr:**

1. Interview prep is broken — you get zero feedback on what you actually said
2. I interviewed 30+ tech professionals and found the best candidates had built AI feedback loops that didn't exist before
3. I encoded their techniques into a free, open-source Claude Skill that handles the whole thing
4. The skill scores your real interview answers, predicts company-specific questions, runs mock interviews, and debriefs rejections
5. The biggest trap: AI on default settings makes you sound like every other candidate — push it harder
6. Lead with insights only you can claim, and set your AI coach to maximum pressure

***Author's note**: Names have been changed to preserve participant anonymity.*

---

\[Hero image\]

Logan hadn't interviewed for a new job in eight years. He'd been at one of the hottest companies in San Francisco, promoted several times, never feeling the need to look elsewhere. When he decided to pursue a senior architect role at Anthropic, he hit a wall experienced engineers know well: interviewing is its own skill. Day-to-day, Logan solved architecture problems with full context and ample time. Interviews required him to grind LeetCode, whiteboard system designs on the spot, and compress years of expertise into rehearsed stories that fit a rubric.

Normally, preparing for senior engineering loops takes months. Logan had two weeks. "I had to learn how to interview for architecture roles from scratch," he told me.

He got the job. When I asked what mattered most, he pointed to his AI workflows — not as a nice-to-have, but as the primary reason he pulled it off in two weeks.

He's not alone. I interviewed over 30 tech professionals about how they use AI throughout the interview process. What I found went beyond polishing resumes. People had built entire systems: ways to get feedback on what they *actually said* in interviews, methods to predict questions before walking in, workflows to surface stories they didn't know they had. Each person had figured out a piece of the puzzle.

If you've ever walked out of an interview with no idea whether your answers landed, or spent the night before wondering if you're highlighting the wrong experiences, you already know why.

**So I did the work for you.**

I took every technique that worked, combined them with professional coaching methods, and built a Claude Skill that handles the whole thing. It's free, it's open source, and it's yours. But first, let me show you what's broken about interview prep today and why these candidates had to build something new.

# The feedback loop that didn't exist

Interview prep hasn't changed much in the last decade. You rehearse your stories, maybe run through a mock interview with a friend, and walk into the real thing hoping it clicks. Afterward, you're left guessing. Companies don't tell you why they passed. Friends don't know what interviewers actually look for. You're prepping blind.

**Of the issues candidates raised, three came up again and again:**

1. **The impostor spiral.** Lindsey, a senior PM who'd been at the same company for 10 years, sent out applications and heard nothing. "I started having creeping impostor syndrome," she told me. "Am I actually a good PM? What's going on?" Without feedback, you can't tell if it's your resume, your approach, your skills, or just bad luck.
2. **The blind grind.** Charles spent hours tailoring each resume, hoping to highlight the right experiences. Joan researched companies thoroughly but had no way to know if she was focusing on what interviewers actually cared about. Neither had any signal their effort was pointed in the right direction.
3. **The practice gap.** You can't get better at something you only do once every few years. And the common advice — interview at companies you don't care about to get your reps in — wastes everyone's time.

# What the best candidates built

The candidates who landed roles at top companies all did the same thing: they closed the feedback loop themselves.

Greg fed his interview transcripts to Claude, trained it on best practices, and got line-by-line feedback on answers he *thought* went well but didn't. Ella built a workflow where she'd paste a job description alongside her resume and have ChatGPT surface the exact gaps a hiring manager would flag, then help her close them before the review. Sean stopped guessing which experiences to highlight. He'd simulate the interview beforehand, test which stories landed, and refine them before the real thing.

Each person had developed their own system. Some overlapped, some didn't. All took real work to build. The problem: assembling those puzzle pieces yourself takes weeks, and turning them into a working system is a challenge most people won't take on.

So I took what they learned, combined it with professional coaching techniques, and encoded everything into a Claude Skill. The tool you'll find in this post is the research itself, packaged so you don't have to build your own system from scratch.

Until now, this kind of coaching required a $300/hour career coach. But even a great coach can't analyze a full interview transcript in minutes, track your patterns across sessions, or be available at 11 pm when you're anxious about tomorrow.

# The Interview Coach: a free tool to put this into practice

**[Download the Interview Coach skill here →](https://github.com/noamseg/interview-coach-skill)**

Claude Skills are instructions you add to Claude that shape its behavior. Think of them as a way to give Claude domain expertise. I could have written "here are 15 things great candidates do." Instead, I put all my efforts into a Claude Skill. Every technique, workflow, and hard-won lesson from these interviews is baked into how it coaches you.

It's free. It's open source. Go use it to land that dream job.

The skill handles everything those candidates were doing manually:

- Scores your actual interview answers and tells you exactly what to fix, based on what you said, not what you think you said
- Generates company-specific prep with predicted questions, your positioning, and likely concerns about your background
- Runs mock interviews that push back, interrupt, and force you to think on your feet
- Mines your experience for stories you didn't know you had
- Strengthens weak stories and retires ones that aren't landing
- Debriefs rejections so you learn something from every no

## How to set it up (5 minutes)

**Claude Pro/Max users:**

1. Download the `interview-coach-skill.zip` from [GitHub](https://github.com/noamseg/interview-coach-skill)
2. In Claude: **Settings > Capabilities > Skills**
3. Upload the zip file
4. Start a new conversation, upload your resume (and optionally LinkedIn)
5. Type: `/setup`

**Free Claude users:**

1. Go to [GitHub](https://github.com/noamseg/interview-coach-skill) and copy the contents of `SKILL.md`
2. Paste it into a new Claude conversation with your resume
3. Type: `/setup`

*Note: Free users won't retain context between sessions. The core coaching still works, but tracking progress across interviews requires a paid plan.*

## Two modes, depending on your timeline

**Basic mode (~30 min per interview):** Share the job description, type `/prep [company name]`, and get a one-page brief: what they optimize for, predicted questions, your positioning, and likely concerns about your background with counters. If you know your interviewers, share their LinkedIn profiles for a "Know Your Interviewer" card on each person. After the interview, paste your transcript and type `/analyze` for a scored breakdown of every answer.

**Advanced mode (~2-3 hours upfront):** Everything in basic, plus: build your storybank (`/stories`) so Claude mines your career for stories you didn't know you had. Practice under pressure (`/practice`) with mock interviews that push back and interrupt. Stand out (`/standout`) by extracting "earned secrets" from your experience and sharpening your point of view. Track patterns across interviews (`/progress`). Generate a 60-second confidence boost before you walk in (`/hype`). Debrief rejections so every no teaches you something.

## What the outputs look like

Here's an actual company prep brief (for a Growth PM role at a Series B fintech):

**COMPANY SNAPSHOT** Series B fintech ($47M raised), ~120 employees. Core product: B2B expense management for mid-market companies. Differentiator: industry-specific integrations (construction, healthcare).

**PREDICTED QUESTIONS**

1. "Tell me about a time you identified and scaled a new growth channel."
2. "How would you approach entering a new vertical with our product?"
3. "Walk me through how you'd measure success in the first 90 days."

**YOUR GAPS** No direct fintech experience — bridge with payments work at \[Company X\]. Growth experience is more B2C — emphasize the enterprise motion at \[Company Y\].

And a post-interview scorecard:

**OVERALL: 7/10** Solid fundamentals, but two answers hurt you.

**STRONG MOMENTS** Prioritization answer was crisp (1:45, clear structure, specific example). Good recovery when pushed on metrics: you admitted uncertainty, then pivoted to your approach.

**PROBLEM AREAS** Question 3 (cross-functional conflict): You talked for 3:20 without a clear outcome. Interviewer interrupted twice. Question 5 (product tradeoffs): "I think" appeared seven times. State positions directly.

**FILLER WORD COUNT:** 23 "um/uh," 12 "sort of"

**FOR NEXT ROUND:** Tighter conflict story with a concrete outcome. Practice stating opinions without hedging.

That level of specificity — answer duration, filler word counts, the exact moment where confidence dropped — is what separates AI coaching from asking a friend "how'd I do?"

# How to not sound like everyone else

The skill handles the mechanics. But there's a trap: if you use AI on default settings, you'll sound like every other candidate who prepped with AI. Polished, competent, forgettable. Here's how to avoid that.

**Lead with insights only you can claim.** Patterns you noticed from direct experience. Counterintuitive lessons that most people in your field get wrong. Not "communication is important" (generic) but "The highest-performing teams I led actually had *more* conflict, not less. We'd institutionalized productive disagreement, and it made our decisions faster" (specific, surprising, defensible).

What did you learn that contradicted the conventional wisdom? What would you tell your past self that they wouldn't believe? Those become your differentiated talking points.

**Share spiky points of view.** When you catch yourself giving a textbook response, push further.

**Safe answer**: "I believe in user research before building."

**Spiky POV**: "I've stopped running user research before building entirely. We ship a stripped-down version in two weeks, watch what people actually do, and iterate from there. Traditional upfront research gave us confidence in the wrong things. Real usage data is faster and more honest."

The second version has a stance. It might be wrong. That's what makes it interesting.

**Set your AI coach to maximum pressure.** AI defaults to cheerleader mode. It tells you your answer was "solid" when it was forgettable. It suggests "small tweaks" when the whole story needs to go. If you use AI on default settings, you'll *feel* prepared and show up underprepared.

The fix: stop letting it be nice.

Logan told Claude: "You are a competing staff engineer who wants to find every flaw in my understanding." Another candidate used: "Give me feedback as if you're a skeptical VP who's seen a hundred candidates this week and is just looking for reasons to say no."

Instead of "How did I do?" try "What's the weakest part of that answer?" Instead of "Any feedback?" try "Where would an interviewer lose confidence in me?" One candidate asked: "Your job is to find reasons to reject me. What would you tell the hiring committee?" That surfaces the concerns the polite version would never mention.

Treat your AI coach like a sparring partner, not a friend who didn't want to hurt your feelings.

# Two warnings

**Recording interviews.** Tools like Granola transcribe calls without announcing a bot. Some candidates see this as note-taking; others feel uncomfortable, especially in two-party consent states. My take: if you're using the transcript to improve afterward, that's fair game. If it feels wrong, skip it and use the skill for prep and mock interviews instead.

**Preparation vs. performance.** AI can help you predict questions, craft answers, and walk in ready. But the interview still has to be *you*. The goal is to surface your real experience more effectively, not to manufacture a version of yourself that doesn't exist. If you're rehearsing answers you don't believe, that's not an AI problem. That's a you problem.

# Your action checklist

**Today (10 minutes)**

- [ ] Download the Interview Coach skill from [GitHub](https://github.com/noamseg/interview-coach-skill)
- [ ] Upload your resume and LinkedIn profile
- [ ] Type `/setup`

**This week (1-2 hours)**

- [ ] Build your storybank: `/stories`
- [ ] Practice telling the same story at different lengths: `/practice ladder`
- [ ] Handle pushback: `/practice pushback`

**Before your next interview**

- [ ] Share the job description: `/prep [company name]`
- [ ] If you know your interviewers, share their LinkedIn profiles
- [ ] Right before you walk in: `/hype`

**After every interview**

- [ ] Paste your transcript: `/analyze`
- [ ] Work on the specific fixes it identifies
- [ ] If rejected, tell Claude what happened for a structured debrief

**Weekly (during active search)**

- [ ] Check patterns and set focus: `/progress`

---

Every technique in this skill came from someone who used it to get hired. Interviewing isn't a talent — it's a feedback loop you never had. Now you do.

**[Download the Interview Coach skill →](https://github.com/noamseg/interview-coach-skill)**
