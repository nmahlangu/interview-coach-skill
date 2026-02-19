# Interview Coach — End-to-End Testing Guide

This guide walks through every major feature in order. Each section includes what to type, what to expect, and where to take screenshots.

---

## Setup

**Get the files:**

```bash
git clone https://github.com/noamseg/interview-coach-skill.git
cd interview-coach-skill
```

Or: click the green **Code** button on GitHub → **Download ZIP**, unzip it, and open the folder.

**Activate the skill:**

```bash
cp SKILL.md CLAUDE.md
```

**Start Claude Code** in this directory (terminal, Claude App, or Cursor). `CLAUDE.md` auto-loads.

---

## Test 1: kickoff

**Goal**: Initialize profile, verify session state creation.

**Type**:
```
kickoff
```

**Provide when asked** (one at a time — the skill should ask sequentially):
- Track: `Full System`
- Target role: `Senior Product Manager`
- Feedback directness: `5`
- Interview timeline: `3 weeks`
- Biggest concern: `I tend to ramble and lose structure under pressure`

**Then paste this resume summary**:
```
Sarah Chen — Senior Product Manager
8 years experience. Currently at Datadog (3 years), previously Shopify (3 years) and early-stage startup (2 years).

Key accomplishments:
- Led migration of Datadog's alerting pipeline, reducing false positive alerts by 40% across 2,000+ enterprise customers
- Launched Shopify's merchant analytics dashboard (used by 150K+ merchants, $2M ARR impact)
- Built and shipped v1 of a developer tools startup's core product with 3 engineers in 4 months
- Managed cross-functional team of 12 across 3 time zones for Datadog's enterprise onboarding redesign
- Drove pricing model change at Shopify that increased average contract value by 22%

Strengths: data-driven decision making, cross-functional leadership, technical depth (former engineer), startup-to-scale experience.
Gaps: No people management title (IC track), limited international market experience.
```

**Screenshot opportunities**:
- The sequential question flow (showing one-at-a-time)
- Kickoff summary output
- Verify `coaching_state.md` was created (check file system)

---

## Test 2: stories

**Goal**: Build initial storybank, test earned secret extraction.

**Type**:
```
stories
```

**Select**: `Add`

**Provide this story**:
```
At Datadog, our alerting pipeline was generating so many false positives that enterprise customers were ignoring real alerts. I analyzed 6 months of alert data and found that 70% of false positives came from just 3 threshold patterns. I proposed a dynamic thresholding system that adapted to each customer's baseline. The engineering lead initially pushed back — said it was too complex and would take 6 months. I scoped a phased rollout: start with the top 3 patterns only, validate with 50 customers, then expand. We shipped phase 1 in 8 weeks. False positives dropped 40% across 2,000+ customers. Support tickets for alert fatigue dropped 60%.
```

**Watch for**:
- Earned secret extraction question ("What did you learn that most people in your role wouldn't know?")
- Earned secret validation (the three gates test)
- Story strength rating

**Then add one more story**:
```
At Shopify, I noticed our merchant analytics dashboard had high adoption (150K merchants) but terrible engagement — average session was 45 seconds. Nobody was actually using the insights. I ran 30 merchant interviews in 2 weeks and found the core issue: merchants didn't distrust the data, they didn't know what action to take from it. I redesigned the dashboard around "recommended next actions" instead of raw metrics. Each insight linked to a specific Shopify feature. Engagement jumped from 45 seconds to 3.5 minutes average. Merchants who used the action-oriented dashboard had 15% higher GMV growth over 6 months. The insight: dashboards that show data without showing what to do with it are furniture, not tools.
```

**Screenshot opportunities**:
- Earned secret extraction flow
- Completed storybank table
- Verify `coaching_state.md` was updated with stories

---

## Test 3: prep [company]

**Goal**: Test company prep with format awareness and story mapping.

**Type**:
```
prep Stripe
```

**Provide when asked**:
```
Role: Senior Product Manager, Payments Platform
Format: 5-round loop — recruiter screen, hiring manager 1:1, two cross-functional behavioral, one system design/case study

Job description highlights:
- Own product strategy for payment method expansion (BNPL, crypto, local payment methods)
- Partner with engineering, design, data science, and go-to-market teams
- Drive decisions with data while navigating ambiguity
- Experience with platform products serving developers
- Strong track record of shipping at scale

Stripe values: Move with urgency. Be meticulous. Think rigorously.
```

**Watch for**:
- Interview format identification and scoring weight adjustments
- Company culture read (Stripe-specific)
- Story mapping against predicted questions
- Gap identification (questions where no story exists)

**Screenshot opportunities**:
- Full prep brief output
- Story mapping section
- Questions to ask section

---

## Test 4: analyze

**Goal**: Test transcript analysis, triage decision tree, and scoring.

**Type**:
```
analyze
```

**Wait for the self-assessment question, then respond**:
```
I think it went okay — maybe a 3 overall. I felt strong on the first two questions but lost my thread on the conflict question. Probably 3.5 on Substance, 2.5 on Structure, 3 on the rest.
```

**Then paste this mock transcript**:
```
Interviewer: Tell me about a time you used data to make a product decision that wasn't obvious.

Candidate: Sure, so at Datadog we had this alerting problem — basically enterprise customers were getting way too many alerts and they were ignoring them. So I looked at the data and found that most of the false positives were coming from a few patterns. We built a dynamic thresholding system and it reduced false positives by 40%. The customers were much happier after that and support tickets went down.

Interviewer: How did you get engineering alignment on that approach?

Candidate: The engineering lead was skeptical at first because he thought it would take too long. So I proposed doing it in phases — start small, prove it works, then expand. That worked and we shipped it in about 8 weeks.

Interviewer: Tell me about a time you had a significant conflict with a stakeholder and how you resolved it.

Candidate: So at Shopify there was this situation where the VP of Sales wanted us to build a custom dashboard for enterprise clients. But I thought we should focus on improving the existing analytics dashboard for all merchants first because the data showed most merchants weren't even using what we had. We went back and forth on it for a while. Eventually I put together some data showing that improving the existing dashboard would actually help enterprise clients too, and the VP came around. We ended up doing the merchant dashboard improvements and it worked out — engagement went up significantly and enterprise clients benefited too.

Interviewer: What metrics did you track to measure success?

Candidate: We tracked engagement time, which went from about 45 seconds to over 3 minutes. And we looked at GMV growth for merchants using the dashboard versus those who weren't. The dashboard users had about 15% higher growth.

Interviewer: Tell me about a time you had to make a decision with incomplete information.

Candidate: At the startup I was at before Shopify, we had to decide whether to build our product for individual developers or for teams. We didn't have much data — only about 200 users. I talked to as many users as I could and looked at the usage patterns. It seemed like team features were getting more traction even though we hadn't built many. So we pivoted to focus on teams. It was a tough call with limited data but it turned out to be the right one — our team features drove most of our growth after that.

Interviewer: How did you manage the risk of that pivot?

Candidate: We kept some individual developer features running and didn't fully sunset anything. We just shifted our roadmap priorities. If the team bet didn't work out, we could have shifted back without losing too much ground.
```

**Watch for**:
- Transcript quality gate assessment
- Per-answer 5-dimension scoring
- Self-assessment delta (their 3.5/2.5/3/3/3 vs. coach scores)
- Triage decision tree activation (which bottleneck gets prioritized)
- Root cause pattern identification
- Answer rewrite offer
- Anti-pattern detection

**If offered a rewrite, say**: `Yes, rewrite Q3 (the conflict question)`

**Screenshot opportunities**:
- Per-answer score blocks
- Triage decision with coaching path
- Self-assessment delta
- Answer rewrite (before/after with annotations)
- Verify `coaching_state.md` was updated with scores

---

## Test 5: practice

**Goal**: Test drill progression and self-assessment calibration.

**Type**:
```
practice ladder
```

**When given a question, respond with**:
```
At Datadog, I led the alerting pipeline overhaul. The core problem was false positive fatigue — enterprise customers were ignoring real alerts because they got too many fake ones. I analyzed 6 months of data and found 70% of false positives came from 3 threshold patterns. I proposed dynamic thresholding. Engineering pushed back on complexity, so I scoped a phased rollout: 50 customers first, then expand. We shipped phase 1 in 8 weeks. False positives dropped 40% across 2,000+ customers. Support tickets for alert fatigue dropped 60%. The lesson: when the problem is overwhelming, don't try to solve all of it — find the 3 patterns that drive 70% of the pain and start there.
```

**When asked for self-assessment, say**:
```
I'd rate that a 4 on Substance, 3.5 on Structure, 4 on Relevance, 3.5 on Credibility, 3 on Differentiation.
```

**Watch for**:
- Round debrief format
- Self-assessment delta tracking
- Specific next-round adjustment
- Drill progression gate check

**Screenshot opportunities**:
- Practice round debrief
- Self-assessment delta section
- Next round adjustment

---

## Test 6: mock behavioral Stripe

**Goal**: Test full mock interview simulation.

**Type**:
```
mock behavioral Stripe
```

**Important**: The skill should deliver 4-6 questions one at a time with NO feedback between questions. Answer each one naturally — use your storybank stories and improvise. Keep answers 60-90 seconds (roughly 150-200 words each).

**Watch for**:
- Questions delivered one at a time
- No feedback until the end
- At least one question targeting a known story gap
- Holistic arc feedback (not just per-question)
- Energy trajectory and story diversity analysis

**Screenshot opportunities**:
- A mid-mock question (showing the simulation feel)
- Full post-mock debrief
- Arc analysis section
- Signal-reading notes

---

## Test 7: concerns

**Goal**: Test concern anticipation.

**Type**:
```
concerns
```

**When asked what concerns you expect, say**:
```
They'll probably worry about my lack of payments domain experience and that I've never had a people management title.
```

**Screenshot opportunities**:
- Concern-counter-evidence map (showing concerns you missed)

---

## Test 8: questions

**Goal**: Test interviewer question generation.

**Type**:
```
questions
```

**Screenshot opportunities**:
- Questions with "they might ask back" follow-up prep

---

## Test 9: hype

**Goal**: Test pre-interview boost with psychological warmup.

**Type**:
```
hype
```

**Screenshot opportunities**:
- 60-second hype reel
- 3x3 sheet
- 10-minute warmup routine
- Mid-interview recovery scripts

---

## Test 10: progress

**Goal**: Test trend review and self-assessment calibration across the session.

**Type**:
```
progress
```

**When asked for self-reflection, say**:
```
I think I'm at about a 3.5 on Substance, 3 on Structure, 3.5 on Relevance, 3 on Credibility, 2.5 on Differentiation. My biggest weakness is still structure under pressure.
```

**Watch for**:
- Self-assessment calibration (your ratings vs. coach scores across the session)
- Pattern signals and root causes
- Coaching meta-check
- Outcome tracking prompt (asks about real interview results)

**Screenshot opportunities**:
- Self-assessment calibration table
- Dimension trends
- Coaching meta-check section

---

## Test 11: negotiate

**Goal**: Test post-offer negotiation coaching.

**Type**:
```
negotiate
```

**Provide when asked**:
```
Offer from Stripe:
- Base: $210K
- Equity: 1,500 RSUs over 4 years (current price ~$30/share)
- Signing bonus: $25K
- Level: L5 (Senior)
- Location: San Francisco (hybrid)

Ideal outcome: $230K base, 2,000 RSUs, $40K signing
Walk-away: $200K base minimum

No competing offers, but I'm currently employed and not in a rush.
```

**Screenshot opportunities**:
- Offer analysis with market positioning
- Negotiation scripts (exact language)
- Fallback language for pushback

---

## Test 12: thankyou

**Goal**: Test follow-up generation.

**Type**:
```
thankyou
```

**Provide context**:
```
Just finished the hiring manager round at Stripe with Maria Chen. We talked about payment method expansion strategy and my Datadog alerting work. She seemed most interested in how I handled the engineering pushback.
```

**Screenshot opportunities**:
- Thank-you draft
- Reinforcement points

---

## Verification Checklist

After completing all tests, verify:

- [ ] `coaching_state.md` exists and contains all session data
- [ ] Storybank has both stories with earned secrets
- [ ] Score history shows entries from analyze, practice, and mock
- [ ] Session log shows all commands run
- [ ] Drill progression reflects current stage
- [ ] Interview loop for Stripe is tracked

**Final screenshot**: The complete `coaching_state.md` file showing full session state.
