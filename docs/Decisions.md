# Decisions

This file records important product and engineering decisions.

## 2026-07-09: Android-first MVP

Decision: build the MVP as an Android-first Flutter app.

Reason:

- Shariff's execution system needs to live on his phone first.
- Android usage stats are a core MVP signal.
- Notifications are central to morning planning and evening review.
- Desktop and web can come later after the daily loop works.

## 2026-07-09: Single-user product

Decision: Shariff OS is built for Shariff only during MVP.

Reason:

- The product value comes from deep personal context.
- Generalizing too early would weaken the operating system.
- Multi-user features add complexity without helping Shariff execute.

## 2026-07-09: AI as COO, not chatbot

Decision: AI should be designed as a COO layer across workflows, not a free-form chat feature.

Reason:

- The goal is execution, not conversation.
- AI must plan, review, summarize, remember, and challenge.
- Chat can exist later, but the product should not depend on chat as the main interface.

## 2026-07-09: Supabase backend

Decision: use Supabase for auth, Postgres, storage, and edge functions.

Reason:

- Fast MVP backend.
- Strong Postgres foundation.
- Works well for structured memory and future embeddings.
- Edge functions can protect AI keys.

## 2026-07-09: Feature-first Flutter architecture

Decision: organize Flutter code by product feature.

Reason:

- Shariff OS has clear feature domains.
- Feature boundaries reduce duplicated code.
- It stays easier to maintain as the app grows.

## 2026-07-09: Docs are living project memory

Decision: product and architecture docs must be updated whenever implementation changes.

Reason:

- The GitHub repository is the project source of truth.
- Future work should be based on repo state, not chat memory.
- Good docs prevent accidental product drift.
