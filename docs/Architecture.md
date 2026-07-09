# Architecture

## Direction

Shariff OS is an Android-first Flutter app backed by Supabase.

The architecture should keep the first MVP simple while preserving room for desktop, web, AI memory, and future integrations.

## Main Parts

| Area | Choice | Purpose |
| --- | --- | --- |
| Mobile app | Flutter | Android-first UI and local app logic. |
| UI system | Material 3 | Premium dark interface with consistent components. |
| Backend | Supabase | Auth, Postgres, storage, and edge functions. |
| Database | Postgres | Structured product memory and analytics. |
| AI | OpenAI API | COO planning, review, summaries, and memory reasoning. |
| Notifications | Firebase Cloud Messaging | Morning, evening, focus, and mission reminders. |
| Android usage | Android UsageStats APIs | Screen and app usage signals. |

## Flutter Architecture

Use a feature-first structure with clear layers.

Recommended structure:

```text
frontend/
  shariff_os/
    lib/
      app/
      core/
      features/
        mission_control/
        planning/
        review/
        journal/
        life_score/
        missions/
        ai_coo/
        android_usage/
        job_tracker/
        finance/
      shared/
```

Each feature should prefer:

- models
- repositories
- services
- view models
- screens/widgets

The app should avoid duplicated business logic inside UI widgets.

## State Management

Initial recommendation: Riverpod.

Reason:

- clean separation from UI
- good testability
- works well with feature-based architecture
- avoids heavy boilerplate during MVP

## Backend Architecture

Supabase should manage:

- authentication
- Postgres data
- row-level security
- file storage for future assets
- edge functions for privileged AI/backend operations

The client should not call sensitive AI workflows directly when secrets are involved.

## AI Architecture

AI should be treated as a product service, not a random chat box.

Core AI services:

- morning planning
- evening review
- weekly board meeting
- journal summarization
- memory retrieval
- mission recommendations
- Life Score explanation

AI requests should include only relevant context, not the entire database.

## Memory Architecture

Memory has three layers:

1. Structured memory: tasks, reviews, sleep, mood, usage, scores.
2. Narrative memory: journals, AI summaries, meeting notes.
3. Semantic memory: embeddings for search and pattern recall.

The AI should combine these layers to produce recommendations.

## Security

Because this is a private one-user app, the MVP can be simpler than a public SaaS product, but it must still protect sensitive data.

Rules:

- never expose API keys in the Flutter app
- use Supabase RLS
- store AI secrets in backend/edge function environment variables
- avoid logging private journal contents unnecessarily

## Scalability Position

The MVP is single-user, but code should still be maintainable.

Do not build:

- organizations
- teams
- complex permissions
- public user profiles

Do build:

- clean feature boundaries
- clear data models
- testable scoring logic
- documented AI behavior

## Development Workflow

- Read docs before implementing.
- Keep docs updated when behavior changes.
- Use feature branches for meaningful work.
- Keep commits small and descriptive.
- Prefer simple, maintainable code over clever shortcuts.
