# Phase 3: Mobile App Pedagogy Research

**Date:** 2026-05-11

## Summary

Research into mobile learning, gamification, and curriculum design points toward a clear pedagogical model for a Racing Rules of Sailing app: **scenario-based microlearning with spaced repetition and lightweight gamification**. The evidence strongly favors short sessions (5-10 minutes), active recall through quizzing, and organizing content by racing situation rather than rule number. Duolingo's layered gamification architecture provides a proven template, though it should be applied judiciously -- a niche sailing audience differs from a mass-market language audience.

---

## Core Learning Framework

### Three Evidence-Based Pillars

**1. Spaced Repetition**

Studying material over spaced intervals significantly improves long-term retention compared to massed learning, even when total study time is identical. Recent research (2024-2025) confirms this across domains.

Key findings:
- Users who review material at increasing intervals show 150% better retention
- Optimal review gaps range from 3 days (for 1-week recall) to 27 days (for 1-year recall)
- Combining spaced repetition with active recall ("spaced retrieval") is the strongest combination
- AI-adaptive spacing that adjusts intervals based on individual performance further improves outcomes

**Application to RRS app:** After a user answers a Rule 18 scenario correctly, the app should surface it again at increasing intervals. Missed questions should return sooner. The system should track mastery per rule/concept, not just per question.

**2. Active Recall**

Pulling information out of memory (answering questions, solving scenarios) builds stronger retention than passive review (re-reading rules). This is well-established cognitive science.

Key formats for active recall:
- Multiple-choice scenario questions ("Which boat must keep clear?")
- Diagram-based identification ("Which boat has mark-room?")
- True/false rule statements
- "What rule applies?" classification questions

**Application to RRS app:** Every interaction should require the user to recall and apply rules, not just read them. Rule text should be shown *after* the user attempts a question, as explanation, not before.

**3. Scenario-Based Learning**

Research shows that contextual, scenario-based learning closes the gap between theory and application far more effectively than sequential rule memorization. Learners connect new information to what they already know and to realistic contexts.

**Application to RRS app:** Organize primary learning paths by *racing situations* (starting line, windward leg, mark rounding, downwind, finishing), not by *rule number*. Each scenario naturally pulls in the relevant rules. The same rule (e.g., Rule 11, Same Tack Overlapped) appears in multiple scenario contexts, reinforcing it through varied application.

---

## Microlearning Design

### Session Length

Research converges on optimal mobile learning sessions of **5-10 minutes**:

| Finding | Source |
|---|---|
| 2-5 minute modules deliver information without overwhelming | General microlearning research |
| Engagement drops significantly after 6-9 minutes | Video/content engagement studies |
| 8-12 minutes aligns with working memory and attention limits | Cognitive load research |
| 5-10 minutes, 3-5x weekly produces best mobile outcomes | Evidence-based implementation guidelines |

### Completion and Retention

- Microlearning courses: **80% completion rate** (vs. 20% for long-form)
- Spaced microlearning: **20% better retention** than other formats
- Best retention from revisiting concepts **4-6 times** with 24-hour gaps between tests

### Recommended Session Structure

```
Session (~5-8 minutes)
|
|-- Brief context setup (10-15 seconds)
|   "You're approaching the windward mark on starboard tack..."
|
|-- 3-5 scenario questions (1-2 minutes each)
|   - Diagram shown
|   - User answers
|   - Immediate feedback with rule citation
|   - Brief explanation if wrong
|
|-- Session summary (15-30 seconds)
|   - Score
|   - Rules practiced
|   - Progress indicator
```

---

## Gamification Strategy

### Lessons from Duolingo

Duolingo's gamification has been extensively studied. Key transferable principles:

| Mechanic | Duolingo Impact | RRS App Application |
|---|---|---|
| **Streaks** | 3.6x more likely to stay engaged at 7-day streak; loss aversion drives daily return | Daily practice streak; streak freeze for missed days |
| **XP system** | Common currency across all activities; 40% more engagement via leaderboards | XP for correct answers, bonus for streaks, scaled by difficulty |
| **Badges/achievements** | 30% boost to completion rates | "Rule 18 Master", "Clean Start", "Perfect Round" achievements |
| **Leaderboards** | Weekly competition drives engagement | Optional weekly/monthly boards; sailing club groups |
| **Progressive unlock** | Motivates completion of fundamentals before advanced | Unlock mark rounding after mastering basic right-of-way |

### Principles for a Niche App

Duolingo serves hundreds of millions of users. A sailing rules app serves thousands to tens of thousands. Key adjustments:

1. **Start simple.** Launch with 1-2 core mechanics (streaks + XP). Add leaderboards and badges later based on user feedback.
2. **Avoid empty leaderboards.** With a small user base, leaderboards feel dead. Consider "beat your own best" or club-level competition instead of global.
3. **Earn, don't just award.** Badges that everyone gets easily lose motivational power. Tie them to genuine mastery milestones.
4. **Don't let gamification overshadow learning.** The goal is rules mastery, not points accumulation. Gamification is the engagement layer, not the product.

---

## Curriculum Structure

### Sequential vs. Scenario-Based

| Approach | Pros | Cons |
|---|---|---|
| **Sequential** (Part 1, Part 2, etc.) | Mirrors rulebook; systematic; nothing skipped | Boring; abstract without context; poor retention |
| **Scenario-based** (Start, Mark, Open Water) | Contextual; engaging; mirrors real racing experience | Rules appear out of order; some rules span multiple scenarios |
| **Hybrid** | Best of both; scenarios for primary learning, sequential for reference/completeness | More complex to design |

**Recommendation: Hybrid approach.**

Primary learning path is scenario-based (organized by racing situations). A secondary "Rule Reference" mode lets users study rules sequentially and test themselves on individual rules.

### Proposed Learning Path (Scenario-Based)

```
Module 1: Fundamentals
  - Definitions: port/starboard, windward/leeward, overlap, keep clear
  - Rule 10: Opposite tacks (the most basic rule)
  - Rule 11: Same tack, overlapped
  - Rule 12: Same tack, not overlapped

Module 2: The Starting Line
  - Pre-start positioning and right-of-way
  - Rule 13: While tacking
  - Rule 15: Acquiring right of way
  - Rule 16: Changing course
  - Starting penalties and recalls (Part 3 excerpts)

Module 3: Upwind Legs
  - Tacking duels and right-of-way
  - Rule 13 in depth
  - Rule 14: Avoiding contact
  - Rule 17: Proper course limitation

Module 4: Mark Rounding -- Basics
  - Definitions: zone, mark-room, room
  - Rule 18.1: When Rule 18 applies (and when it doesn't)
  - Rule 18.2(a): Same tack, overlapped at marks

Module 5: Mark Rounding -- Advanced
  - Rule 18.2 continued: not overlapped, zone entry snapshot
  - Rule 18.3: Tacking in the zone (2025-2028 changes)
  - Rule 19: Obstructions
  - Rule 20: Room to tack at an obstruction

Module 6: Downwind and Finishing
  - Leeward mark approaches
  - Proper course considerations
  - Finishing rules

Module 7: Penalties and Protests
  - Rule 44: Penalty turns (when and how)
  - Rule 14: Contact situations
  - Filing a protest (simplified Part 5)
  - Exoneration (Rule 21)

Module 8: Advanced Scenarios
  - Multi-boat situations
  - Case book scenarios
  - Edge cases and common misunderstandings
  - 2025-2028 rule changes in context
```

### Mastery and Progression

Use a skill-tree model with prerequisites:

- Modules 1-3 must be completed before Module 4 (mark rounding requires fundamental right-of-way knowledge)
- Within each module, progressive difficulty: easy scenarios first, then intermediate, then tricky edge cases
- Each concept requires multiple correct answers at spaced intervals before being marked "mastered"
- Mastery degrades over time if not reviewed (spaced repetition loop)

---

## Visual Design for Boat Scenarios

### The Challenge

Racing rules scenarios require showing boat positions, headings, wind direction, mark locations, and zones on a small mobile screen. This is the app's core UX challenge.

### Design Principles

1. **Top-down view.** Boat-position diagrams in sailing are always shown from above. This is a well-established convention.
2. **Minimal elements.** Show only what the question requires: boats, wind arrow, mark (if relevant), zone circle (if relevant). No background clutter.
3. **Color coding.** Distinguish boats by color (e.g., green = right-of-way, red = give-way, blue = neutral). Use the same colors consistently.
4. **Touch-friendly targets.** Answer buttons and interactive elements must be large enough for thumb interaction. Place primary actions in the lower half of the screen (thumb zone).
5. **Progressive disclosure.** Show the scenario first, then reveal the answer with rule overlay (dotted zone lines, overlap indicators, etc.) after the user answers.
6. **Wind indicator always visible.** A consistent wind arrow in a fixed screen position (top corner) anchors orientation.

### Diagram Complexity Tiers

| Tier | Elements | Example |
|---|---|---|
| Basic | 2 boats, wind arrow | "Port or starboard?" |
| Intermediate | 2-3 boats, wind arrow, mark, zone | "Who has mark-room?" |
| Advanced | 3+ boats, wind, mark, zone, course legs | "Which boat(s) broke a rule?" |

### Animation Potential

Simple animations showing boat movement (approach, overlap change, zone entry) would significantly improve understanding of temporal rules (e.g., "overlapped at the time the first boat entered the zone"). Start with static diagrams; consider animation as a future enhancement.

---

## Feedback and Explanation Design

### Immediate Feedback

After each answer:
- **Correct:** Brief positive indicator + rule citation + optional "Why" expansion
- **Incorrect:** Show correct answer + rule text + diagram annotation showing why

### Explanation Depth

Offer two levels:
1. **Quick:** Rule number and one-sentence summary ("Rule 11: Windward boat must keep clear when overlapped on the same tack.")
2. **Deep:** Full rule text, relevant case/appeal reference, link to related scenarios

This respects both the time-constrained user doing a quick session and the deep learner who wants to understand the reasoning.

---

## Handling the 4-Year Rules Cycle

The RRS changes every 4 years (next update: 2029-2032). The app must plan for this:

- **Content architecture:** Separate rule text/citations from scenario logic. Scenarios may survive across cycles; rule numbers and exact wording will change.
- **"What Changed" module:** When a new cycle begins, offer a focused module on changes (like the 18.2/18.3 rewrite in 2025-2028).
- **Versioning:** Clearly label all content with the rules cycle it applies to.

---

## Recommendations Summary

| Decision | Recommendation | Evidence |
|---|---|---|
| Session length | 5-8 minutes | Microlearning research |
| Learning method | Active recall via scenario quizzes | Cognitive science consensus |
| Retention mechanism | Spaced repetition with adaptive intervals | 150% retention improvement |
| Content organization | Scenario-based primary, sequential secondary | Contextual learning research |
| Gamification | Streaks + XP at launch; badges and boards later | Duolingo data; "start simple" principle |
| Difficulty progression | Mastery-gated skill tree with prerequisites | Progressive difficulty research |
| Visual format | Top-down boat diagrams, color-coded, touch-friendly | Mobile UX best practices |
| Feedback | Immediate, two-depth (quick + deep) | Active recall best practices |
| Rules cycle | Decouple content from scenario logic | Long-term maintainability |

---

## Questions for Phase 4 (Pricing Research)

- What do comparable niche education apps charge on iOS?
- What pricing model works best for small audiences: one-time purchase, subscription, freemium?
- What are Apple's policies and economics for education apps?
- What is the effective market size (number of racing sailors in the US)?

---

## Sources

- [Spaced Repetition and Retrieval Practice (2025)](https://journals.zeuspress.org/index.php/IJASSR/article/view/425)
- [Spaced-Repetition in Paediatrics Education (PMC)](https://pmc.ncbi.nlm.nih.gov/articles/PMC12343689/)
- [Microlearning Statistics and Trends 2025](https://elearningindustry.com/microlearning-statistics-facts-and-trends)
- [Mobile Microlearning and Knowledge Retention (PMC)](https://pmc.ncbi.nlm.nih.gov/articles/PMC6716752/)
- [Microlearning Best Practices 2025](https://www.arist.co/post/microlearning-research-benefits-and-best-practices)
- [Duolingo Gamification Case Study 2026](https://trophy.so/blog/duolingo-gamification-case-study)
- [Duolingo Gamification Secrets](https://www.orizon.co/blog/duolingos-gamification-secrets)
- [Gamification in Mobile Learning Engagement](https://www.techclass.com/resources/learning-and-development-articles/the-role-of-gamification-in-mobile-learning-engagement)
- [Scenario-Based Learning in Education](https://elearningdoc.com/scenario-based-learning/)
- [Context-Based Learning Survey (Frontiers)](https://www.frontiersin.org/journals/education/articles/10.3389/feduc.2023.1210968/full)
- [Skill Trees for Adaptive Learning (Prodigy)](https://medium.com/prodigy-engineering/skill-trees-for-adaptive-learning-729760e5dd00)
- [Quiz App UI Design Patterns (Mobbin)](https://mobbin.com/explore/mobile/screens/quiz)
- [NauticEd Sailing Simulator](https://www.nauticed.org/sailing-simulator)
