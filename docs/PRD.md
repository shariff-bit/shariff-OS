# Shariff OS PRD

## Goal

Build an Android-first personal operating system that helps Shariff convert long-term missions into daily execution.

The MVP should prove one thing:

> Can Shariff OS help Shariff plan, execute, review, and improve consistency every day?

## Target User

Shariff only.

The product should not include generic onboarding, teams, public profiles, social features, or multi-user settings during MVP.

## MVP Success Criteria

The MVP is successful if Shariff can:

- open the app each morning and know the five most important actions for the day
- connect every task to one of the four missions
- review the day each evening in under five minutes
- see a meaningful Life Score
- journal and have the AI remember patterns
- receive useful AI COO recommendations
- see basic Android usage impact on execution

## MVP Scope

### In Scope

- Android Flutter app
- Supabase authentication
- mission model
- task and priority tracking
- daily planning flow
- evening review flow
- journal entries
- Life Score calculation
- mood check-ins
- basic Android usage stats ingestion
- AI COO summaries and recommendations
- simple job tracker
- manual finance tracker
- dark Material 3 design system

### Out of Scope for MVP

- multi-user support
- public launch
- web dashboard
- desktop app
- WHOOP integration
- bank integration
- calendar integration
- email integration
- browser extension
- advanced mascot animations
- complex gamification

## Core User Flows

### Morning Planning

1. Shariff receives a morning notification.
2. Shariff opens Mission Control.
3. AI COO suggests priorities based on missions, yesterday's review, mood, and known patterns.
4. Shariff confirms up to five priorities.
5. Each priority is assigned to a mission.

### During the Day

1. Shariff checks Mission Control.
2. The app shows the next best action.
3. Focus and mission reminders appear only when useful.
4. Android usage signals are collected in the background where allowed.

### Evening Review

1. Shariff receives an evening notification.
2. Shariff marks priorities completed or missed.
3. Shariff logs mood and journal.
4. Life Score is calculated.
5. AI COO summarizes the day and identifies tomorrow's risk.

### Weekly Board Meeting

1. Sunday evening review opens.
2. The app summarizes each mission.
3. AI COO highlights patterns, wins, misses, and recommendations.
4. Next week's focus is set.

## Product Requirements

### Missions

- The app must ship with the four fixed missions.
- Every priority and task must belong to one mission.
- Mission names can be edited later, but the MVP should treat them as fixed.

### Priorities

- A day can have a maximum of five primary priorities.
- Priorities should be scored by mission importance, urgency, and execution value.
- Completion should feed into Life Score and AI memory.

### Journal

- Journal entries should support free text.
- Each journal should be summarized by AI.
- Embeddings should be stored for long-term memory search.

### Life Score

- Life Score should be configurable.
- The first version can use a default scoring configuration.
- The score should be explainable, not mysterious.

### AI COO

- AI responses should be direct, useful, and context-aware.
- The AI should avoid generic motivation.
- The AI should connect advice to missions and past behavior when memory exists.

### Android Usage

- The app should request usage access clearly.
- The MVP should track target app usage durations.
- Usage should affect reviews and Life Score where configured.

## Risks

- Overbuilding before daily planning and review work well.
- Creating a generic productivity app instead of Shariff's operating system.
- Making AI chat the center instead of execution.
- Capturing data without converting it into decisions.

## MVP Principle

Ship the smallest version that can run Shariff's day.
