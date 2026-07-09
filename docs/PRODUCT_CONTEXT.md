# Shariff OS Product Context

This file is the source of truth for the product. Keep it updated whenever features, architecture, or major product decisions change.

## Product Identity

Shariff OS is an AI-powered personal operating system built for one person: Shariff.

It is not a generic habit tracker, todo app, journal app, or productivity dashboard. It is a personal execution system that turns long-term ambitions into measurable daily action.

The AI acts as Shariff's personal COO. It should plan, review, remember, challenge, summarize, and help Shariff make better execution decisions.

## Founder Context

- User: Shariff
- Age: 22
- Current role: Growth at Bitplanet
- Previous company: OpenLedger
- Current growth areas: execution consistency, sleep schedule, and focus
- Product posture: private, single-user MVP

Shariff OS should not generalize for other users during MVP. Every product decision should optimize for Shariff's actual life.

## Core Missions

Every task, review, recommendation, and progress signal should connect to one of these missions.

| Mission | Name | Purpose |
| --- | --- | --- |
| Alpha | Career | Improve career outcomes, job hunt, growth work, and professional positioning. |
| Beta | OpenMed Labs | Build OpenMed-related ideas, research, strategy, and execution. |
| Gamma | DSA Champ | Improve data structures and algorithms consistency and skill. |
| Delta | Personal Life | Improve sleep, health, relationships, mood, finance, and personal stability. |

## Product Philosophy

Shariff OS rewards progress, not busyness.

Every screen should answer:

> What should Shariff do next?

Not:

> What happened?

The product should help Shariff execute when motivation is low, energy is uneven, or distractions are high.

## AI COO Role

The AI is not a chatbot. It is the operating intelligence of the system.

The AI COO should:

- plan each day
- review each evening
- conduct weekly board meetings
- track long-term progress
- learn from journals and behavior
- challenge excuses directly but respectfully
- remember patterns over months and years
- connect daily tasks to long-term missions

Example long-term memory insight:

> You usually stop applying for jobs after five rejections. Today the goal is not motivation; it is one more application.

## Long-Term Memory

Shariff OS should preserve and learn from:

- journals
- tasks completed
- tasks missed
- conversations with the AI
- mood check-ins
- focus sessions
- sleep records
- reviews
- mission progress
- job applications
- finance entries
- Android usage stats

Memory should support both exact lookup and pattern detection.

## MVP Direction

The MVP is Android-first Flutter.

Reason:

- Shariff's daily execution happens on his phone.
- Android usage stats are important to the product.
- Notifications are central to planning and reviews.
- Android-first avoids overbuilding for desktop and web too early.

The codebase should still be structured cleanly so desktop and web can come later.

## Primary MVP Features

### 1. Mission Control

The first screen is a morning command center, not a passive dashboard.

It should show:

- today's top priorities
- recovery and sleep summary
- current Life Score
- mission progress
- AI COO advice
- key reminders

### 2. Daily Planning

Morning notification prompts Shariff to plan the day.

Rules:

- maximum five priorities
- every priority belongs to one mission
- AI helps choose priorities based on mission progress, missed work, energy, and schedule

### 3. Evening Review

Evening review captures:

- completed priorities
- missed priorities
- Life Score
- mood
- journal
- tomorrow's risks
- AI COO summary

### 4. Weekly Board Meeting

Sunday evening review across:

- Career
- OpenMed Labs
- DSA
- Personal Life
- health
- sleep
- focus
- screen usage
- recommendations for next week

### 5. Journal

Daily journal with AI reading, summarization, embeddings, and pattern extraction.

The journal is a memory source, not just text storage.

### 6. Life Score

Configurable 100-point daily score.

Positive inputs:

- sleep
- recovery
- deep work
- gym
- learning
- Bitplanet work
- OpenMed work
- DSA work

Negative inputs:

- late sleep
- excessive screen time
- Instagram
- reels
- missed tasks

### 7. Android Usage Stats

Read usage for:

- Instagram
- Telegram
- Chrome
- LinkedIn
- YouTube
- Discord

This should be automatic after user permission.

### 8. Job Tracker

Manual tracking for:

- resume version
- applications
- interviews
- rejections
- offers
- salary

AI should analyze job hunt behavior and recommend next actions.

### 9. Finance

Manual entry for:

- income
- expenses
- savings
- loans

No bank integration for MVP.

### 10. Mood

Morning and evening mood tracking.

Correlate mood with:

- sleep
- recovery
- screen time
- productivity

### 11. News Digest

Daily AI summary for:

- medical AI
- OpenMed
- AI
- crypto
- Web3
- growth
- hiring

### 12. Mascot

Penguin mascot that acts as the COO's visible personality.

It should:

- celebrate wins
- roast gently when Shariff avoids execution
- guide decisions
- level up over time

Future: Rive animations.

## Future Features

- WHOOP integration
- Health Connect
- desktop app
- web dashboard
- OpenMed portal
- DSA portal
- voice AI
- wearables
- browser extension
- calendar integration
- Google Tasks integration
- email integration

## Non-Negotiable Product Rules

- Do not reward busyness.
- Do not generalize for multiple users during MVP.
- Every task must belong to a mission.
- Every core screen must help Shariff decide what to do next.
- Documentation must stay updated with implementation.
- Repository state is the project memory.
