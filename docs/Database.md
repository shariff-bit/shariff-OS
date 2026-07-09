# Database

## Direction

Supabase Postgres is the system of record for Shariff OS.

The database stores execution history, AI memory, mission progress, reviews, and future analytics.

## MVP Tables

### profiles

Stores the single Shariff profile.

Key fields:

- id
- display_name
- timezone
- created_at
- updated_at

### missions

Stores the four core missions.

Key fields:

- id
- code
- name
- description
- sort_order
- is_active
- created_at
- updated_at

Initial records:

- alpha: Career
- beta: OpenMed Labs
- gamma: DSA Champ
- delta: Personal Life

### tasks

Stores mission-linked work items and daily priorities.

Key fields:

- id
- mission_id
- title
- notes
- task_date
- priority_rank
- status
- execution_value
- created_at
- completed_at
- updated_at

Rules:

- daily priority rank should be 1 to 5 when set
- every task must belong to a mission

### daily_plans

Stores the morning plan.

Key fields:

- id
- plan_date
- mood_morning
- energy_level
- ai_summary
- created_at
- updated_at

### evening_reviews

Stores the evening review.

Key fields:

- id
- review_date
- mood_evening
- wins
- misses
- tomorrow_risk
- ai_summary
- created_at
- updated_at

### journals

Stores journal text and AI summaries.

Key fields:

- id
- journal_date
- content
- ai_summary
- extracted_patterns
- created_at
- updated_at

### memory_embeddings

Stores embeddings for long-term memory search.

Key fields:

- id
- source_type
- source_id
- content
- embedding
- metadata
- created_at

### life_score_entries

Stores daily score totals and explanation.

Key fields:

- id
- score_date
- total_score
- positive_points
- negative_points
- explanation
- created_at
- updated_at

### life_score_events

Stores individual scoring inputs.

Key fields:

- id
- score_date
- category
- points
- source_type
- source_id
- notes
- created_at

### mood_entries

Stores morning and evening mood.

Key fields:

- id
- mood_date
- period
- mood_score
- label
- notes
- created_at

### android_usage_entries

Stores app usage signals.

Key fields:

- id
- usage_date
- package_name
- app_name
- duration_seconds
- open_count
- created_at

### job_applications

Stores job hunt activity.

Key fields:

- id
- company
- role
- status
- resume_version
- salary_range
- applied_at
- notes
- created_at
- updated_at

### finance_entries

Stores manual finance records.

Key fields:

- id
- entry_date
- type
- category
- amount
- notes
- created_at
- updated_at

## Future Tables

- whoop_sleep_entries
- whoop_recovery_entries
- health_connect_entries
- news_digest_items
- weekly_reviews
- mascot_state
- focus_sessions

## Data Rule

If a feature changes what Shariff OS remembers, this document must be updated.
